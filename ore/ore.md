# ORE - Documentação Completa

## Resumo

Ao revisar a literatura sobre técnicas de prompt engineering, tornou-se claro que critérios de elegibilidade escritos em linguagem natural não bastavam para determinar um escopo de forma consistente, por exemplo, tentando separar técnicas que dependem apenas do texto enviado ao modelo daquelas que envolvem algum tipo de intervenção adicional — como decodificação restrita, fine-tuning e soft prompts. Essa dificuldade recorrente motivou a criação do ORE (*Operationalized Ruleset for Experiments*), um framework que formaliza a decisão de incluir ou não um experimento para reduzir a ambiguidade e as zonas cinzentas da triagem. Ele é composto por um diagrama de classes que organiza os elementos relevantes de um resultado relatado na literatura, pela definição de cada um desses elementos, e por um conjunto de regras lógicas formais que determinam quando esses elementos, em conjunto, tornam aquele resultado elegível. O ORE não avalia o estudo como um todo, mas cada `Experiment` específico relatado nele, decidindo individualmente se aquele dado atende aos critérios da revisão. Seu uso não elimina toda a subjetividade do processo de triagem, mas eleva a consistência das decisões a um nível mais alto do que seria possível aplicando os critérios apenas por leitura direta do texto do estudo.

## Introdução ao ORE

Os critérios de elegibilidade adotados nesta revisão exigem distinguir, com precisão, técnicas que operam exclusivamente por meio de texto fornecido ao modelo em tempo de inferência daquelas que dependem de mecanismos adicionais — ajuste de pesos, decodificação restrita, soft prompts ou intervenção programática sobre a saída.

Tentativas preliminares de aplicar critérios de elegibilidade formulados em linguagem natural mostraram-se insuficientes para garantir aplicação uniforme: casos limítrofes recorrentes — sobretudo na distinção entre hard prompt e mecanismos com intervenção adicional — revelaram-se difíceis de resolver de forma consistente com critérios puramente textuais. Essa limitação motivou o desenvolvimento de um instrumento que reduzisse a ambiguidade interpretativa inerente a critérios textuais.

Apresentamos, assim, o *Operationalized Ruleset for Experiments* (ORE), um framework desenvolvido especificamente para operacionalizar os critérios de inclusão desta revisão. O ORE modela o processo que gera um dado experimental relatado na literatura (a partir da técnica empregada, do modelo utilizado e da forma como a saída foi avaliada) como uma composição de entidades tipadas cujos atributos assumem valores restritos a domínios fechados. Essa estrutura permite que a elegibilidade de um `Experiment` seja determinada por condições lógicas formais sobre tais entidades, em vez de por julgamento direto sobre a descrição textual do estudo. O ORE não se propõe como instrumento de aplicação geral; sua estrutura foi definida em função do escopo desta revisão, embora possa servir de ponto de partida para revisões com objetivos semelhantes.

As seções seguintes apresentam a definição completa do ORE seguida pela descrição de cada um de seus componentes.

## Definição e objetivo

Concretamente, o ORE é composto por:

* um diagrama de classes que estrutura as entidades e relações do domínio;
* a definição operacional de cada elemento desse diagrama;
* um conjunto de restrições formais escritas em OCL (Object Constraint Language, uma linguagem de restrições sobre diagramas de classe) que expressam as condições de elegibilidade sobre essa estrutura.

O propósito do ORE em si não é ser usado para classificar estudos como incluídos ou excluídos, mas sim para decidir a elegibilidade de cada `Experiment`. Esse termo refere-se especificamente à classe `Experiment`, cuja definição — um pouco diferente do uso comum do termo "experimento" — é apresentada na próxima seção. Ainda que o ORE não determine diretamente a elegibilidade de um estudo, ele pode ser incorporado a esse processo — por exemplo, uma triagem pode exigir que um estudo contenha ao menos um certo número de instâncias de `Experiment` elegíveis para ser incluído.

Um `Experiment` é considerado elegível quando satisfaz a restrição `EligibleExperiment`, apresentada na seção que descreve as restrições em OCL.

## Descrição dos componentes do diagrama de classes

### `Study`

Representa o estudo submetido à triagem (artigo, preprint, tese, etc). Um `Study` é a unidade de publicação como um todo e pode relatar um ou mais instâncias de `Experiment`, cada qual avaliada individualmente quanto à elegibilidade.

### `Experiment`

Um `Experiment` não corresponde ao conceito do senso comum de "experimento científico completo", tampouco a um `Study` inteiro. Representa, especificamente, o processo que gerou um dado pontual relatado na literatura. Esse dado pode ser, por exemplo, uma linha de tabela, uma métrica isolada ou um resultado específico de comparação. Um mesmo `Study` pode relatar múltiplas instâncias de `Experiment`, inclusive quando estas empregam técnicas de natureza distinta entre si (por exemplo, um `Experiment` que avalia uma técnica de hard prompt e outro, no mesmo artigo, que avalia uma técnica baseline que envolve processos de fine-tuning). Essa granularidade é necessária porque a elegibilidade, nos critérios desta revisão, é determinada por experimento, não por artigo: um `Study` pode ser incluído com base em um único `Experiment` elegível, mesmo que a maior parte de seus resultados não se enquadre nos critérios.

### `PromptTechnique`

Classe abstrata que representa a técnica de interação com o modelo empregada no `Experiment`. Não possui atributos próprios: sua caracterização decorre inteiramente de qual subclasse a instancia. A generalização de `PromptTechnique` em `HardPromptTechnique` e `SoftPromptTechnique` é disjunta e completa — toda técnica avaliada em um `Experiment` é classificada como exatamente uma dessas duas categorias, nunca como ambas simultaneamente, nunca como nenhuma.

### `HardPromptTechnique`

Subclasse de `PromptTechnique` que representa técnicas que operam exclusivamente por meio de texto fornecido ao modelo em tempo de inferência — instruções, exemplos, templates, encadeamento de raciocínio ou estratégias equivalentes. É definida estruturalmente como a composição de um `InteractionProcess` e um ou mais `HardPromptTemplate`: a técnica é, ao mesmo tempo, o processo de interação com o modelo (como os prompts são montados e enviados) e as regras/componentes sobre o conteúdo textual de cada prompt.

### `SoftPromptTechnique`

Subclasse de `PromptTechnique` que representa técnicas baseadas em parâmetros contínuos aprendidos (soft prompts). Sua estrutura interna não é detalhada nesta modelagem: a classe existe na estrutura apenas para completar a generalização disjunta e completa de `PromptTechnique`, já que o escopo do estudo para o qual o ORE foi criado trata exclusivamente de técnicas de hard prompt. Não interessa a este estudo nenhum `Experiment` cuja `PromptTechnique` seja uma `SoftPromptTechnique`.

### `InteractionProcess`

Representa o processo de interação entre o programa (ou usuário) e o modelo, do início ao momento em que a `FinalOutput` é obtida. É caracterizado por dois atributos:

#### `persistenceMechanisms`

`persistenceMechanisms`: é um atributo multivalorado que indica quais mecanismos de reenvio da requisição ao modelo, entre os dois valores possíveis abaixo, estão presentes no processo. Os dois mecanismos não são mutuamente exclusivos: um mesmo `InteractionProcess` pode empregar ambos simultaneamente, por exemplo, descartando saídas sem sentido antes de aplicar um ciclo de validação de qualidade sobre as saídas remanescentes. Um array vazio indica que não há nenhum mecanismo de reenvio condicionado à validação da saída — o prompt é enviado e a resposta obtida é aceita diretamente. Os valores possíveis são:
- `conditional_retry`: mecanismo que valida a saída do modelo em algum momento do `InteractionProcess` (não necessariamente, mas incluindo, a `FinalOutput`) segundo algum critério de qualidade, formato, estrutura ou desempenho na tarefa, e repete o envio até que a condição seja satisfeita, ou até um número máximo de tentativas. Inclui também mecanismos que geram múltiplas saídas e selecionam a melhor entre elas.
- `noise_filter`: mecanismo de reenvio cuja função é apenas descartar saídas manifestamente inválidas ou demasiadamente sem sentido, sem avaliar qualidade, formato, estrutura ou desempenho da técnica na tarefa.

**Nota: O uso de mecanismos de validação apenas para mensurar a técnica, e não como parte dela, não configura nenhum `persistenceMechanisms` por si só.** Um `Experiment` pode utilizar um programa validador de formato exclusivamente para produzir dados sobre a eficácia da técnica avaliada — sem que esse validador faça parte do processo que gerou a `FinalOutput`. Nesses casos, o atributo `persistenceMechanisms` do `InteractionProcess` correspondente não fica vazio apenas por conta disso, mas também não é acrescido de nenhum valor, uma vez que o mecanismo de validação atua como instrumento de medição externo ao processo de geração, e não como componente do próprio `InteractionProcess`.

#### `interactionLevel`

`interactionLevel`: caracteriza o processo de montagem do prompt e os passos de envio e resposta envolvidos, incluindo manipulação de múltiplos prompts, cálculos, arquivos, recuperação de informação ou uso de outras IAs — seja esse processo manual ou automatizado, e independentemente de a montagem em si ser feita diretamente pelo usuário ou por um programa dedicado a compor o prompt a partir de partes (por exemplo, um motor de templates). O termo é uma abreviação de "InteractionProcess Level".

Os cinco valores possíveis formam uma escala de permissividade cumulativa: cada nível permite as características dos anteriores e proíbe as características dos posteriores. O nível é determinado pela característica que lhe confere o maior nível possível, sem depender da presença de características dos níveis anteriores.

Desse modo, um processo classificado em um nível também pode (não obrigatoriamente) satisfazer as condições de qualquer nível inferior a ele e (obrigatoriamente) não pode conter elementos descritos em níveis posteriores.

Esta é a descrição de cada nível:

- `l1`: nenhum processamento; o prompt é enviado ao modelo e a resposta é obtida diretamente, sem etapas intermediárias.
- `l2`: pode envolver cadeia de prompts dentro da mesma conversa — múltiplos envios e respostas sucessivos, seguindo um roteiro pré-planejado (por exemplo, solicitar que o modelo avalie sua própria resposta e produza uma versão revisada).
- `l3`: pode envolver cadeia de prompts em conversas separadas, uso de recuperação aumentada (RAG), buscas na internet, buscas em grafos de conhecimento, buscas em bancos de dados, em sistemas de arquivos ou consultas a estruturas de dados como arrays.
- `l4`: pode envolver edição ou salvamento de arquivos e pastas, manipulação de bancos de dados, chamadas de API, e cálculos matemáticos realizados por programa como apoio ao modelo de linguagem.
- `l5`: pode envolver o uso de outros modelos de linguagem ou IAs de outras naturezas para auxiliar na montagem do prompt — fornecendo uma resposta, um conhecimento específico, executando uma subtarefa, ou fornecendo qualquer trecho textual a ser inserido no prompt. É este o caso referido, na descrição de `Model` adiante, como uso de IA auxiliar: tal IA participa apenas da construção do prompt, e não é ela quem produz a `FinalOutput` avaliada.

Notas:

* o uso de Model repetidas vezes para tarefas variadas não constitui o "uso de outras IAs" a que se refere a descrição do nível 5.
* o uso de qualquer outro modelo de linguagem além de Model, mesmo que para tarefas pequenas, constitui o "uso de outras IAs" a que se refere a descrição do nível 5.
* os 5 níveis referem-se somente ao InteractionProcess em si. Se, por exemplo, uma IA foi usada para gerar um dataset e o InteractionProcess faz uso desse dataset (sem usar a IA que o gerou) então não é o caso de "uso de outras IAs" a que se refere a descrição do nível 5. Se, porém, esse dataset for gerado pela IA dentro do InteractionProcess, então se enquadra.

### `HardPromptTemplate`

Representa regras/componentes sobre o conteúdo textual dos prompts empregados pela técnica. Não possui atributos nesta modelagem pois sua presença na estrutura tem função exclusivamente conceitual, de modo a preservar a decomposição de `HardPromptTechnique` como a composição entre o processo de interação com o modelo (`InteractionProcess`) e os templates/moldes do conteúdo textual dos prompts envolvidos nesse processo (`HardPromptTemplate`).

A cardinalidade 1...* entre `HardPromptTechnique` e `HardPromptTemplate` é causada pelo fato de que um único `InteractionProcess` pode envolver múltiplos prompts (nos casos em que `interactionLevel` é igual ou superior a 2). Por exemplo, um prompt que solicita um rascunho e outro, subsequente, que solicita sua revisão, e mais outro que solicita sua correção; cada qual podendo empregar um `HardPromptTemplate` distinto.

### `FinalTemplate`

Subclasse de `HardPromptTemplate` que representa, especificamente, a instância de template correspondente ao prompt cuja resposta constitui a `FinalOutput` do `Experiment` — isto é, o último elo do `InteractionProcess`. Sua introdução como subclasse, e não apenas como um `HardPromptTemplate` qualquer, decorre da possível necessidade de referenciar esse elemento com frequência ao longo do texto sem recorrer a perífrases como "o `HardPromptTemplate` marcado como final". Cada `HardPromptTechnique` possui exatamente um `FinalTemplate` entre suas instâncias de `HardPromptTemplate` (ver restrição `exactlyOneFinalTemplate`), independentemente de quantas outras instâncias estejam presentes no processo. Por não introduzir atributos próprios, `FinalTemplate` herda integralmente a caracterização de `HardPromptTemplate`; sua função é exclusivamente identificar, dentre os templates de uma técnica, aquele que efetivamente corresponde à saída avaliada nas instâncias de `Measurement` do `Experiment`.

### `Model`

Representa o modelo de linguagem cuja `FinalOutput` é avaliada no `Experiment`. É caracterizado por dois atributos:

`type`: indica a natureza do modelo quanto ao seu preparo para uso conversacional:
- `base`: modelo que apenas completa texto da esquerda para a direita, sem preparo para uso como assistente conversacional. Exemplo: GPT-2.
- `block`: modelo que preenche lacunas em um texto, sem preparo para uso como assistente conversacional. Exemplo: GLM-10B.
- `instruction_tuned`: modelo autorregressivo que passou por ajuste fino generalista voltado a uso como assistente conversacional — categoria que inclui os modelos amplamente utilizados pelo público geral. Exemplos: GPT-3.5, Gemini 3.1 Pro, Qwen 3.8 Max.
- `specialized`: modelo `instruction_tuned` que passou por ajuste fino adicional voltado à especialização em uma tarefa específica. Exemplos: Codex (base do GitHub Copilot), Med-PaLM 2 da Google, BioGPT da Microsoft.

`freedom` indica o grau de liberdade com que os tokens são gerados:
- `default`: modo padrão de geração do modelo.
- `constrained_decoding`: a geração é restringida por uma sintaxe imposta por força bruta durante a amostragem de tokens. Os "modos JSON" oferecidos por algumas APIs de LLMs se enquadram aqui quando o provedor faz uso de constrained decoding para garantir a saída com sintaxe json correta e, possivelmente, seguindo um schema json fornecido pelo usuário.
- `json_mode_alternative_type`: refere-se aos "modos JSON" oferecidos por algumas APIs de LLMs, quando o provedor faz uso de outros meios (não constrained decoding) para garantir a saída com sintaxe json correta e, possivelmente, seguindo um schema json fornecido pelo usuário.
- `json_mode_unspecified`: refere-se aos "modos JSON" oferecidos por algumas APIs de LLMs, quando o estudo não deixa claro qual método o provedor usou para garantir a saída com sintaxe json correta e, possivelmente, seguindo um schema json fornecido pelo usuário.

Um caso particular a esclarecer é o de `Experiment` cujo `InteractionProcess` envolve o uso de outros modelos de linguagem ou outras IAs como parte do processo de montagem do prompt (`interactionLevel` = `5`; ver definição completa deste atributo na descrição de `InteractionProcess`). Nesses casos, o `Experiment` continua associado a um único `Model` — o modelo cuja `FinalOutput` é, de fato, avaliada nas instâncias de `Measurement` do `Experiment`. As IAs auxiliares empregadas na montagem do prompt não constituem instâncias de `Model` nesta modelagem, porque seu papel se encerra na construção do prompt; elas não produzem a saída que está sob avaliação, apenas contribuem, como um passo intermediário do processo, para o conteúdo que será enviado ao `Model` efetivamente avaliado.

### `FinalOutput`

Representa a saída final produzida pelo `Model`, que segue para avaliação em uma ou mais instâncias de `Measurement`.

Não constituem `FinalOutput`:

* saídas intermediárias geradas ao longo do `InteractionProcess` (por exemplo, em processos com `interactionLevel` igual a 2 ou superior).
* saídas do `Model` que foram modificadas por meio de programa ou intervenção humana. Considere, entretanto, o ponto sobre concatenação de saídas a seguir.
* strings geradas pela concatenação de saídas geradas na mesma conversa ou em conversas distintas.

É necessário que se trate de uma saída direta do modelo e sem nenhuma modificação posterior.

Pode constituir `FinalOutput`:

* Saídas do `Model` em conversas de um turno e sem anexos.
* Saídas do `Model` em conversas longas, de muitos turnos e envolvendo arquivos anexados além de texto. Pode ser qualquer tipo de arquivo, por exemplo: imagens, vídeos, áudios, arquivos HTML, TXT, DOCX e PDF.

É caracterizada pelos atributos `type` e `contextType`.

O atributo `type` indica a natureza da saída:

- `string`: texto, incluindo código-fonte, tabelas e dados estruturados, desde que entregues em formato de string.
- `image`, `video`, `audio`, `embedding`: demais tipos de saída, não textuais.

O atributo `contextType` indica a natureza do conteúdo presente na janela de contexto do `Model` ao gerar a saída:

- `string_only`: apenas texto, incluindo código-fonte, tabelas e dados estruturados, desde que entregues em formato de string.
- `with_media`: foi inserido ao menos um anexo (qualquer tipo de arquivo — imagem, vídeo, áudio, pdf, etc) na conversa que gerou a `FinalOutput`.

### `Measurement`

Representa um dado empírico pontual (uma medição ou métrica) extraído de uma avaliação realizada sobre a FinalOutput. Uma mesma FinalOutput pode estar associada a múltiplas instâncias de Measurement (por exemplo, se o estudo reporta uma métrica de qualidade e outra de formato para a mesma saída). O atributo type indica a natureza desse dado reportado e assume um dos seguintes valores:

- `ctg_hard_control`: mede algum aspecto de geração controlada de texto no âmbito estrutural, como aderência a limites de tamanho, taxa de acerto de restrições impostas ou sucesso de formato, de maneira geral.
- `ctg_soft_control`: mede algum aspecto de geração controlada de texto no âmbito abstrato, como toxicidade, criatividade, diversidade, segurança, sentimento e legibilidade.
- `schema_adherence`: mede especificamente a adesão correta à sintaxe da linguagem JSON ou XML e ao schema solicitado. Para se enquadrar aqui, é obrigatório que um schema com chaves nomeadas tenha sido de fato especificado ao modelo; solicitações genéricas de saída em JSON/XML sem schema definido não se enquadram aqui. Apesar disso, a avaliação de sintaxe JSON/XML sem schema se enquadra em `code_syntax_of_native_language`.
    * Nota: Não é necessário ser um schema formalmente definido, mas é necessário que as chaves e níveis sejam definidos, seja por exemplos, por linguagem natural ou de outra maneira. Listar chaves sem denotar os níveis não deve ser aceito sob nenhuma hipótese, a não ser que estejam todas no mesmo nível.
- `code_syntax_of_native_language`: mede a adesão correta à sintaxe de alguma linguagem formal nativamente dominada pelo modelo. Uma linguagem é considerada nativamente dominada quando é amplamente representada em corpora de treinamento típicos de LLMs — linguagens de programação majoritárias (Python, HTML, JSON, XML, YAML, SQL, etc.) — de modo que o modelo já demonstra proficiência sintática sem necessidade de instrução adicional dentro do próprio prompt. Uma linguagem é considerada não-nativa quando o `Experiment` precisa fornecer, dentro do prompt, documentação, exemplos, gramática formal ou instruções equivalentes para que o modelo aprenda a sintaxe — ainda que essa linguagem seja real e documentada externamente.
- `code_syntax_of_non_native_language`: mede a adesão correta à sintaxe de alguma linguagem formal que não é nativamente falada pelo modelo e que requer fornecimento de documentação, instruções em linguagem natural, gramáticas formais, regex, exemplos e/ou outras formas de fazer o modelo aprender a linguagem. Alguns exemplos: TOON (Token Oriented Object Language) e a linguagem Crista (biblioteca python da empresa Anvpy). Quando o texto precisa seguir alguma regex ou gramática formal, ele se enquadra aqui. Schemas em linguagens já conhecidas não devem se enquadrar aqui (por exemplo, schemas json, xml, yaml, etc).
- `quality`: mede se a tarefa foi executada de maneira aceitável, sem necessariamente buscar o melhor resultado possível. Métricas como BLEU e ROUGE tipicamente se enquadram nesta categoria. Este tipo frequentemente aparece associado, no mesmo `Experiment`, a `ctg_hard_control` e `ctg_soft_control`: é comum que um estudo sobre geração controlada avalie simultaneamente se a imposição de restrições de formato não comprometeu a qualidade do conteúdo produzido, de modo que `quality` funcione como contrapartida de controle sobre o efeito colateral da restrição avaliada.
- `performance_maximization`: mede se a tarefa foi executada de maneira otimizada, buscando o melhor resultado possível, e não apenas um resultado aceitável.

Notam-se estes grupos distintos de avaliação:

* o grupo 1, relacionado a formato (`ctg_hard_control`/`schema_adherence`/`code_syntax_of_native_language`/`code_syntax_of_non_native_language`)
* o grupo 2, relacionado a atributos subjetivos de controle (`ctg_soft_control`)
* o grupo 3, relacionado a qualidade de execução de tarefa (`quality`/`performance_maximization`).

Para distinguir, na prática, uma avaliação do primeiro grupo de uma do segundo/terceiro, aplica-se o seguinte teste:

1. Se o modelo resolvesse corretamente o conteúdo da tarefa, mas o fizesse em uma estrutura, sintaxe, comprimento ou vocabulário diferente do exigido, a métrica reportada contabilizaria isso como falha?
2. Se o modelo resolvesse corretamente o conteúdo da tarefa e o fizesse em uma estrutura, sintaxe, comprimento ou vocabulário exatamente como exigido, a métrica reportada contabilizaria isso como acerto?
3. Se o modelo resolvesse incorretamente o conteúdo da tarefa, mas o fizesse em uma estrutura, sintaxe, comprimento ou vocabulário exatamente como exigido, a métrica reportada contabilizaria isso como acerto?
4. Se o modelo resolvesse incorretamente o conteúdo da tarefa e o fizesse em uma estrutura, sintaxe, comprimento ou vocabulário diferente do exigido, a métrica reportada contabilizaria isso como falha?

Em caso afirmativo para as todas essas perguntas, a avaliação mede uma restrição independente do raciocínio da tarefa, enquadrando-se no primeiro grupo. Em caso negativo a ao menos uma delas, a avaliação mede apenas atributos subjetivos, enquadrando-se no segundo grupo, ou a adequação do cumprimento da tarefa, enquadrando-se no terceiro.

Fato importante: "contabilizar" também significa não ignorar.

Abaixo, um exemplo de como fazer a distinção.

* um estudo estabelece três valores fechados que o LLM deve responder e nada além disso: 1, 2, 3, sem nenhum caractere além do dígito.
* o `Model` fornece a resposta seguinte: `A opção correta é 1` quando deveria responder `3`.
    * uma métrica que não é `ctg_hard_control` registraria uma falha.
    * uma `ctg_hard_control` registraria um acerto.
* o `Model` fornece a resposta seguinte: `A opção correta é 3` quando deveria responder `3`.
    * uma métrica que não é `ctg_hard_control` registraria um acerto ou não registraria nada, apenas ignoraria o dado.
    * uma `ctg_hard_control` registraria uma falha.

**Ressalva importante:** Aspectos subjetivos e ortogonais à tarefa — como toxicidade, criatividade ou diversidade — não se enquadram em nenhum tipo do primeiro grupo, mas sim no tipo `ctg_soft_control` do segundo.

A revisão de CITE2 distingue duas categorias de CTG: **content control** (ou **hard control**), voltado a elementos estruturais e formais do texto — como formato, estrutura organizacional, comprimento e vocabulário obrigatório ou proibido —, e **attribute control** (ou **soft control**), voltado a características semânticas abstratas do texto — como segurança, sentimento e estilo. Essa distinção corresponde diretamente à separação entre o grupo 1 e o grupo 2 do atributo `type` de `Measurement`: os valores do grupo 1 (`ctg_hard_control`, `schema_adherence`, `code_syntax_of_native_language`, `code_syntax_of_non_native_language`) medem exclusivamente content control — a adesão do texto gerado a regras estruturais, sintáticas ou de formatação, independentemente da adequação semântica do conteúdo produzido —, enquanto `ctg_soft_control`, no grupo 2, mede exclusivamente attribute control — características subjetivas como toxicidade, sentimento ou estilo. Consequentemente, uma avaliação que verse sobre attribute control nunca se enquadra em nenhum valor do grupo 1, e uma avaliação que verse sobre content control nunca se enquadra em `ctg_soft_control`, ainda que ambas envolvam, em sentido amplo, alguma forma de "controle" sobre a geração de texto. Essa delimitação é reforçada pela ressalva presente na definição de `Measurement`, segundo a qual aspectos subjetivos de avaliação não constituem, sob nenhuma circunstância, geração controlada de texto no âmbito estrutural (grupo 1) — sem prejuízo de que tais aspectos sejam capturados, quando pertinente, pelo grupo 2.

## Notas de aplicação transversal

As regras a seguir não se referem a uma única classe do diagrama, mas afetam mais de um ponto da modelagem.

### Uso de temperature, top-p, top-k e system prompts

**Configurações de amostragem não desqualificam o `Experiment` como elegível**. Ajustes nos parâmetros de configuração do modelo — como temperatura, top-p, top-k ou uso de system prompts — não afetam a classificação do `Experiment` quanto a ser `EligibleExperiment` ou não. Diferenças nesses valores, entretanto, são suficientes para diferenciar instâncias de `PromptTechnique`, embora possa haver qualquer variedade desses valores ao longo do `InteractionProcess`.

### Instruções em linguagem natural simulando mecanismos não presentes

**Menções textuais, dentro do próprio prompt, a mecanismos fora do modelo ou de intervenção nas probabilidades do modelo não devem ser tratadas como a aplicação dessas técnicas**. Por exemplo, se um prompt se inicia dizendo `Saída do RAG: XXXX` (sendo XXXX um texto qualquer) se não houve de fato uso de RAG, o início desse prompt para nada serve em elevar para 3 o valor do atributo `interactionLevel` de um `InteractionProcess`. Da mesma forma, não se deve classificar um `Model` como `specialized` apenas porque num prompt havia a instrução: `Responda como se você tivesse passado por fine-tuning para escrever sempre na sintaxe abaixo`. Outro exemplo importante é instruir o modelo a seguir um formato: a presença ou ausência dessa instrução em nada implica na presença nem na ausência de um `Measurement` do tipo `ctg_hard_control` (nem de qualquer outro tipo). São meras instruções em linguagem natural.

### Granularidade de `Experiment`

**A individuação de instâncias de `Experiment` distintas, quando derivadas de variações de técnica relatadas no mesmo `Study`, é determinada pelo próprio `Study`.** Quando um `Study` relata dados associados a variações de uma técnica — por exemplo, "few-shot" e "zero-shot", ou "few-shot com 5 exemplos" e "few-shot com 10 exemplos" — cada variação rotulada distintamente pelo `Study` corresponde a um `Experiment` distinto, cada qual com sua própria instância de `PromptTechnique`, mesmo quando essas instâncias compartilham a mesma estrutura subjacente de `InteractionProcess` e `HardPromptTemplate`. Esta modelagem não impõe um critério próprio de similaridade entre técnicas para decidir se duas instâncias relatadas são "a mesma" técnica ou técnicas diferentes: essa distinção é sempre herdada da forma como o próprio `Study` apresenta e nomeia seus resultados. Como consequência, é esperado que o conjunto de instâncias de `PromptTechnique` extraídas de diferentes instâncias de `Study` durante a etapa de mineração apresente sobreposições — por exemplo, casos de "zero-shot" mineradas de instâncias de `Study` distintas — que poderão ser tratadas em uma etapa posterior de deduplicação e consolidação. Esse tratamento não é mais parte do ORE, cujo objetivo é apenas identificar `EligibleExperiment`.

**A caracterização de um dado como dado de baseline no Study em nada interfere no enquadramento em Experiment nem em ElegibleExperiment**. Ou seja, baselines também podem ser Experiment e ElegibleExperiment.

## Diagrama de classes

```
classDiagram
    class Study {
    }

    class Experiment {
    }

    class PromptTechnique {
    }

    class HardPromptTechnique {
    }

    class SoftPromptTechnique {
    }

    class InteractionProcess {
        +persistenceMechanisms: PersistenceMechanism[0..*]
        +interactionLevel: InteractionLevel
    }

    class HardPromptTemplate {
    }

    class FinalTemplate {
    }

    class Model {
        +type: ModelType
        +freedom: FreedomType
    }

    class FinalOutput {
        +type: OutputType
        +contextType: ContextType
    }

    class Measurement {
        +type: MeasurementType[1]
    }

    class PersistenceMechanism {
        <<enumeration>>
        conditional_retry
        noise_filter
    }

    class InteractionLevel {
        <<enumeration>>
        l1
        l2
        l3
        l4
        l5
    }

    class ModelType {
        <<enumeration>>
        base
        block
        instruction_tuned
        specialized
    }

    class FreedomType {
        <<enumeration>>
        default
        constrained_decoding
        json_mode_alternative_type
        json_mode_unspecified
    }

    class OutputType {
        <<enumeration>>
        string
        image
        video
        audio
        embedding
    }

    class ContextType {
        <<enumeration>>
        string_only
        with_media
    }

    class MeasurementType {
        <<enumeration>>
        ctg_hard_control
        ctg_soft_control
        schema_adherence
        code_syntax_of_native_language
        code_syntax_of_non_native_language
        quality
        performance_maximization
    }

    Study "1" --> "1..*" Experiment : experiments
    Experiment "1" --> "1" PromptTechnique : promptTechnique
    Experiment "1" --> "1" Model : model
    Experiment "1" --> "1" FinalOutput : finalOutput
    FinalOutput "1" --> "1..*" Measurement : measurements

    PromptTechnique <|-- HardPromptTechnique
    PromptTechnique <|-- SoftPromptTechnique

    HardPromptTechnique "1" *-- "1" InteractionProcess : interactionProcess
    HardPromptTechnique "1" *-- "1..*" HardPromptTemplate : hardPromptTemplate
    HardPromptTemplate <|-- FinalTemplate

    note for PromptTechnique "Generalização {disjoint, complete}: toda PromptTechnique é exatamente uma dentre HardPromptTechnique ou SoftPromptTechnique — nunca ambas, nunca nenhuma."

    note for HardPromptTemplate "Representa o conteúdo textual do prompt; não modelado em detalhe nesta versão — presente na estrutura para preservar a decomposição conceitual HardPromptTechnique = InteractionProcess + 1 ou mais instâncias de HardPromptTemplate."

    note for Experiment "Não corresponde ao sentido do senso comum de 'experimento científico completo'; representa o processo específico que gerou um dado pontual (ex: uma linha de tabela)"

    note for Measurement "type é univalorado. Se um mesmo Experiment for avaliado sob múltiplos aspectos (ex: ctg_hard_control e quality medidos sobre a mesma FinalOutput), isso gerará múltiplas instâncias distintas de Measurement, uma para cada dado empírico relatado."

    note for SoftPromptTechnique "Escopo deliberadamente não definido nesta versão do ORE. SoftPromptTechnique existe na estrutura para completar a generalização {disjoint, complete} de PromptTechnique, mas seus atributos e composição interna estão fora do escopo desta revisão, que trata apenas de técnicas de hard prompt."

    note for FinalTemplate "Subclasse de HardPromptTemplate que representa especificamente o prompt cuja resposta constitui a FinalOutput do Experiment. Existe para dar nome próprio a esse elemento para facilitar que seja referenciado no texto, sem duplicar estrutura."
```

## Definições dos elementos-alvo

```
-- ============================================================
-- Restrições OCL
-- ============================================================

-- ------------------------------------------------------------
-- R1: Generalização disjunta e completa de PromptTechnique
-- ------------------------------------------------------------
context PromptTechnique
inv disjointComplete:
    self.oclIsTypeOf(HardPromptTechnique) xor self.oclIsTypeOf(SoftPromptTechnique)

-- ------------------------------------------------------------
-- R2: Obrigação de haver exatamente um FinalTemplate
-- ------------------------------------------------------------
context HardPromptTechnique
inv exactlyOneFinalTemplate:
    self.hardPromptTemplate->one(t | t.oclIsTypeOf(FinalTemplate))

-- ------------------------------------------------------------
-- R3: IOPT (Inference-Only Prompt Technique)
-- Operação derivada que define quando uma HardPromptTechnique
-- é considerada IOPT. Declarada como operação (def), não como
-- invariante, para poder ser reutilizada em outros contextos
-- (ver R4).
-- ------------------------------------------------------------
context HardPromptTechnique
def: isIOPT(): Boolean =
    self.interactionProcess.persistenceMechanisms->isEmpty()
    and (
        self.interactionProcess.interactionLevel = InteractionLevel::l1 or 
        self.interactionProcess.interactionLevel = InteractionLevel::l2 or 
        self.interactionProcess.interactionLevel = InteractionLevel::l3 or 
        self.interactionProcess.interactionLevel = InteractionLevel::l4 or 
        self.interactionProcess.interactionLevel = InteractionLevel::l5
    )

-- ------------------------------------------------------------
-- R4: EligibleExperiment
-- Define quando um Experiment deve ser considerado elegível.
-- Reutiliza isIOPT() (R3) sobre a PromptTechnique associada
-- ao Experiment.
-- ------------------------------------------------------------
context Experiment
inv EligibleExperiment:
    self.promptTechnique.oclIsTypeOf(HardPromptTechnique)
    and self.promptTechnique.oclAsType(HardPromptTechnique).isIOPT()
    and self.model.type = ModelType::instruction_tuned
    and self.model.freedom = FreedomType::default
    and self.finalOutput.type = OutputType::string
    and self.finalOutput.measurements->exists(m |
        m.type = MeasurementType::ctg_hard_control or
        m.type = MeasurementType::ctg_soft_control or
        m.type = MeasurementType::schema_adherence or
        m.type = MeasurementType::code_syntax_of_non_native_language
    )
```

## Limitações

**O ORE não visa eliminar toda a subjetividade na identificação de `EligibleExperiment`**. Ele se propõe como uma ferramenta que aumente a objetividade desse processo, tal como ferramentas como o Planning Poker e as 10 heurísticas de Nielsen — elas não tornam o processo totalmente livre de zonas cinzentas e discordâncias, mas elevam a objetividade a um nível aceitável.

**Na seção de restrições em OCL, as regras sobre `IOPT` e `EligibleExperiment` não são fixas no ORE**. Trata-se das regras R3 e R4, respectivamente. Elas funcionam como critérios de inclusão/exclusão redigidos em linguagem formal. Embora o ORE tenha sido feito especificamente para este estudo, ele pode ser adaptado para outras formas de revisão na área de engenharia de prompt.

## Metodologia do ORE

A identificação de `EligibleExperiment` num `Study` pode seguir a sequência abaixo, embora não seja obrigatória.

1. **Busca por dados**: encontrar um dado suspeito em forma de tabela, gráfico, texto corrido ou outras formas, no documento do estudo. Importante: o dado não é a métrica, é o valor. Uma tabela que compara o valor de uma avaliação de duas técnicas lado a lado consiste em dois dados, podendo se tratar de dois `EligibleExperiment`.
2. **Identificação do objeto analisado**: identificar se esse dado faz referência a algo que pode ser enquadrado em `FinalOutput`, não apenas dentro do framework ORE mas dentro das restrições de `EligibleExperiment`.
3. **Identificação de instâncias de `Measurement`**: identificar o que aquele dado significa (qual `type` do `Measurement`) e se há outros dados sobre exatamente aquela `FinalOutput`. Identificar se estão de acordo com as restrições de `EligibleExperiment`.
4. **Identificação do `Model` e da `PromptTechnique`**: identificar qual modelo gerou a `FinalOutput` (`Model`) e as regras e processos sobre como o prompt que gerou a `FinalOutput` foi criado (`PromptTechnique`).
5. **Classificar `Model` e `PromptTechnique`**: verificar se ambos atendem às restrições de `EligibleExperiment`. Se sim, o dado, técnica e experimento devem ser anotados. Se não, devem ser ignorados. O método de anotação (planilha, texto corrido, etc) fica a critério do responsável por aplicar o ORE.
6. **Repetir** os 5 passos anteriores com todos os dados identificados no `Study` que ainda não foram:
    * identificados como instâncias de `Measurement` da `FinalOutput` atual identificada.
    * processados em rodadas anteriores e anotados ou descartados.