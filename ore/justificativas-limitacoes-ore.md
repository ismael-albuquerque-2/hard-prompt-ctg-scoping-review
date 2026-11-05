## Fundamentação das restrições de elegibilidade nesta revisão

Esta seção explica e defende as decisões de configuração do ORE para esta revisão, isto é, as restrições que compõem a operação `isIOPT()` (R3) e a invariante `EligibleExperiment` (R4). O ORE foi estruturado de modo que essas regras sejam parâmetros de configuração, e não parte imutável do arcabouço (ver Limitações); as escolhas descritas a seguir refletem o escopo desta revisão e não pretendem ser as únicas defensáveis. Nenhuma das decisões foi submetida a análise de sensibilidade, isto é, não se quantificou quantos estudos ou experimentos passariam a ser elegíveis caso cada restrição fosse relaxada. Trata-se de limitação assumida e de agenda natural para trabalhos futuros.

### Restrições de R3 (`isIOPT`)

#### Ausência de `persistenceMechanisms`

Uma técnica só é considerada IOPT se `persistenceMechanisms` for vazio, o que exclui tanto `conditional_retry` quanto `noise_filter`. As duas exclusões têm fundamentos distintos.

A exclusão de `conditional_retry` tem fundamento causal. Nesse mecanismo, a saída avaliada é aquela que satisfez um critério de qualidade, formato, estrutura ou desempenho depois de uma ou mais tentativas, como em (Ruiz-Torrubiano et al., 2026), ou foi escolhida entre múltiplas saídas geradas (Ramirez et al., 2023). O resultado reportado deixa, portanto, de ser fruto apenas do texto do prompt e passa a incorporar o efeito da persistência: uma técnica pode superar outra porque foi tentada até acertar, e não porque seu prompt seja melhor.

A exclusão de `noise_filter` não tem esse fundamento. Descartar saídas manifestamente sem sentido, sem avaliar qualidade, formato ou desempenho, não seleciona resultados favoráveis à técnica, e portanto não compromete a atribuição causal da mesma forma. A exclusão decorre de outra razão: reduzir subjetividade. Delimitar quando uma saída é "manifestamente sem sentido" e distinguir esse critério de uma validação de qualidade é fronteira que suscita zonas cinzentas na aplicação do arcabouço, e optou-se por evitá-las excluindo o mecanismo por inteiro. Reconhece-se que a decisão é de precaução, e não de dano comprovado à validade causal, e que ela pode excluir dados que uma configuração mais tolerante aceitaria.

#### Níveis de interação `l1` a `l5`

Nesta configuração, todos os cinco níveis de `interactionLevel` são aceitos, de modo que o segundo termo da disjunção em `isIOPT()` é sempre verdadeiro. Sua permanência na OCL é deliberada. O motivo é de parametrização: manter os cinco valores explícitos na regra deixa claro, a quem leia a OCL, que todos os 5 níveis são elegíveis. A divisão em níveis e permite que outros pesquisadores que desejem fazer uso do ORE o adaptem selecionando os níveis que desejarem sem alterar a estrutura da regra.

A aceitação dos níveis `l4` e `l5`, que admitem chamadas de API, cálculos por programa e o uso de outras IAs na montagem do prompt, apoiam-se na lógica seguinte. O `InteractionProcess` monta uma string que é enviada a um `Model`; tudo o que ocorre nesse processo ocorre antes da geração e fora do modelo avaliado. É análogo ao caso de um usuário que digita um prompt a um programa intermediário, o qual executa diversas operações, entrega outro prompt ao mesmo modelo e repassa ao usuário a saída obtida. A saída avaliada continua sendo produzida por uma única geração do `Model` alvo, a partir de uma string construída de antemão.

### Restrições de R4 (`EligibleExperiment`)

#### `PromptTechnique` do tipo `HardPromptTechnique`

Excluem-se técnicas de soft prompt, que operam por parâmetros contínuos aprendidos, como as empregadas em (Ajwani et al., 2024). Trata-se de intervenção sobre o modelo que não se reduz ao texto fornecido em tempo de inferência, o que é contrário ao objeto de interesse da revisão. A exclusão é inerente ao escopo e não envolve zona cinzenta.

#### Modelo do tipo `instruction_tuned`

Exclui-se `base` e `block` por não terem sido preparados para uso conversacional, o que introduz variação no comportamento diante de instruções que não é atribuível à técnica. Exclui-se `specialized` porque o ajuste fino adicional voltado a uma tarefa confunde o efeito do prompt com o efeito do treinamento: um resultado favorável pode refletir a especialização do modelo, e não a técnica. Reconhece-se que muitos modelos usados na prática são especializados e que a exclusão restringe a generalização dos achados a modelos de propósito geral.

#### Modo de geração `default`

Excluem-se `constrained_decoding`, `json_mode_alternative_type` e `json_mode_unspecified`. No caso de `constrained_decoding`, a geração é restringida por sintaxe imposta durante a amostragem de tokens CITEPRID14, o que constitui intervenção fora do texto do prompt e compromete a atribuição do resultado à técnica. Há registros de que esse mecanismo pode alterar o desempenho do modelo em relação à geração sem restrição (Chen e Ou, 2026). Os dois valores `json_mode_*` foram excluídos por razão distinta: o provedor pode garantir a estrutura por meios que o usuário não controla e, em `json_mode_unspecified`, que o estudo sequer especifica. A exclusão de ambos visa evitar subjetividade, zonas cinzentas e o tratamento de mecanismos desconhecidos. Reconhece-se que, sobretudo em `json_mode_alternative_type`, a exclusão pode alcançar dados em que o mecanismo do provedor não alterava a amostragem, e que se trata de escolha conservadora.

#### Saída do tipo `string`, sem restrição de `contextType`

Exige-se que a `FinalOutput` seja textual, por coerência com o escopo de geração de texto. Não se restringe `contextType`: entradas com anexos (`with_media`) são aceitas. O critério é a natureza da técnica, e não a modalidade da entrada. Uma técnica de few-shot, por exemplo, continua sendo few-shot com ou sem imagens, vídeos ou outros arquivos anexados ao prompt. Reconhece-se que um anexo não é texto e que a definição de hard prompt como "texto fornecido ao modelo" poderia sugerir o contrário; adota-se aqui o entendimento de que o elemento relevante é a estratégia de construção do prompt, aplicável independentemente do tipo de dado de entrada.

#### Tipos de `Measurement` aceitos

O experimento precisa ter ao menos uma medição de tipo `ctg_hard_control`, `ctg_soft_control`, `schema_adherence` ou `code_syntax_of_non_native_language`. A restrição decorre de a revisão tratar de geração controlada de texto (CTG), e não de qualquer tarefa executada por meio de prompt. Por isso, medições exclusivamente de `quality` ou `performance_maximization` não bastam para tornar um experimento elegível.

A delimitação do que conta como CTG apoia-se na ideia de controle de conteúdo (*hard control*) e controle de atributos (*soft control*) proposta por (Liang et al., 2024) e é operacionalizada pelo teste das quatro perguntas descrito na definição de `Measurement`. Sem esse critério, a noção de controle seria infinitamente extensível: em sentido amplo, qualquer instrução restringe a saída, e mesmo um prompt como "gere algo" poderia ser dito controlar a geração, já que uma resposta vazia ou em branco seria uma quebra de formato ou, filosoficamente, apenas outro "algo". A taxonomia da literatura e o teste operacional impedem que o conceito perca sentido.

A inclusão de `schema_adherence` e `code_syntax_of_non_native_language` é decisão de escopo e não pretende resolver a questão de se a aderência a formato constitui CTG. A área não dispõe de definição consolidada: alguns estudos sobre aderência a JSON se declaram CTG, e outros não. Optou-se por incluí-los por serem objeto de investigação frequente na literatura de restrição de saída e por estarem próximos do controle estrutural. A mesma lógica vale, por analogia, para XML.

Excluiu-se `code_syntax_of_native_language`, isto é, a mera correção sintática em linguagens amplamente dominadas pelos modelos, por não ser considerada, neste estudo, como um tipo de avaliação de CTG. Trata-se, mais uma vez, de definição operacional de escopo, e não de uma tentativa de definir o termo.

### Custo assumido

Em conjunto, essas restrições delimitam um subconjunto deliberadamente estreito da literatura sobre engenharia de prompt e sobre CTG. Estudos e experimentos que empregam retry, modelos especializados, geração restringida, modos JSON ou medições exclusivas de qualidade ficam fora do escopo, ainda que sejam relevantes para outros objetivos. As restrições que se fundamentam na validade causal (`conditional_retry`, `constrained_decoding`, `specialized`) buscam preservar a atribuição do resultado ao texto do prompt; as que se fundamentam em redução de subjetividade (`noise_filter`, `json_mode_*`) e em convenção de escopo (tipos de `Measurement`) refletem escolhas dos autores e podem ser revistas por quem adaptar o ORE a outros objetivos.