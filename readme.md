# Técnicas de Hard Prompt para Geração Controlada de Texto em LLMs — Material Suplementar

> **Hard Prompt Techniques for Controlled Text Generation in LLMs — Supplementary Material**

---

## Sumário

1. [Sobre este repositório](#sobre-este-repositório)
2. [Estrutura do repositório](#estrutura-do-repositório)
3. [Identificadores da pesquisa](#identificadores-da-pesquisa)

---

## Sobre este repositório

Este é o **material suplementar oficial** da pesquisa *"Técnicas de Hard Prompt para Geração Controlada de Texto em LLMs: Uma Revisão de Escopo"*. O repositório contém todos os artefatos necessários para auditoria, reprodução e reuso integral do estudo:

- o arcabouço formal **ORE** (*Operationalized Ruleset for Experiments*), descrito por completo no arquivo localizado em `ore/ore.md`;
- os **dados brutos de busca** em 7 bases (ACM, arXiv, IEEE Xplore, Lens.org, OATD, Scopus, Web of Science);
- o **rastro de seleção** fase a fase, das 5 fases de seleção de estudos (I a V);
- os **dados extraídos** dos estudos, em JSON (`eligible-experiments.json`, `iopts.json`, `iopt-task-categories.json`, `model-families.json`);
- os **apêndices** (`apendices.docx`), que reúnem fundamentação teórica, trabalhos correlatos, tabelas extensas, respostas a questões de pesquisa e análises complementares.

**Números-chave do estudo:**

| Grandeza | Valor |
|---|---|
| Estudos selecionados | 31 |
| Experimentos elegíveis | 1.168 |
| IOPTs | 253 |
| Modelos de linguagem distintos | 96 |
| Resultados iniciais da busca (RRIs) | 296 |

---

## Estrutura do repositório

```
/
├── apendices.docx                          # Compilação dos 10 apêndices do manuscrito
├── readme.md                               # Este arquivo
├── referencias.bib                         # Base BibTeX completa das citações efetuadas no manuscrito principal e no apendices.docx, sem repetições
│
├── /busca-nas-bases                        # Artefatos da busca de estudos
│   ├── detalhes-da-busca.html              # Strings, filtros e sintaxes por base
│   ├── extrator-arxiv.html                 # Ferramenta de busca no arXiv, de autoria dos autores da pesquisa
│   ├── /arquivos-de-exportacao             # Exports brutos das 7 bases
│   │   ├── acm-digital-library.bib
│   │   ├── arxiv.xml
│   │   ├── ieee-xplore.csv
│   │   ├── lens.jsonl
│   │   ├── oatd.ris
│   │   ├── scopus.csv
│   │   └── web-of-science.bib
│   └── /arquivos-de-exportacao-modificados # Versões que sofreram certas alterações descritas no detalhes-da-busca.html
│       ├── lens.jsonl
│       └── web-of-science.bib
│
├── /ore                                    # Arcabouço formal ORE
│   ├── ore.md                              # Especificação completa (descrição + diagrama em mermaid + OCL)
│   ├── justificativas-limitacoes-ore.md    # Justificativas do escopo e restrições
│   ├── diagrama.png                        # Diagrama visual do ore (raster)
│   └── diagrama.svg                        # Diagrama visual do ore (vetor)
│
├── /resultados-da-extracao                 # Dados extraídos (fases VI-VII)
│   ├── eligible-experiments.json           # 1.168 experimentos elegíveis
│   ├── iopts.json                          # 253 IOPTs mapeadas
│   ├── iopt-task-categories.json           # Categorização de tarefas/objetivos (Q4)
│   ├── model-families.json                 # Agrupamento dos 96 modelos em 12 famílias
│   └── /graficos                           # Todos os gráficos utilizados no estudo
│       ├── grafico1.png / grafico1.svg
│       ├── grafico2.png / grafico2.svg
│       └── grafico3.png / grafico3.svg
│
└── /resultados-por-fase-de-selecao          # Rastreamento das fases de seleção (I a V). Metadados dos estudos com e sem resumo.
    ├── /com-resumo
    │   ├── resultados-fase-i.md
    │   ├── resultados-fase-ii.md
    │   ├── resultados-fase-iii.md
    │   ├── resultados-fase-iv.md
    │   └── resultados-fase-v.md
    └── /sem-resumo
        ├── resultados-fase-i.md
        ├── resultados-fase-ii.md
        ├── resultados-fase-iii.md
        ├── resultados-fase-iv.md
        └── resultados-fase-v.md
```


## Identificadores da pesquisa

Abaixo, detalhes sobre identificadores utilizados ao longo da pesquisa. Para mais informações, veja a seção 4.1 do manuscrito principal.

| Identificador | Formato | Exemplo | Descrição |
|---|---|---|---|
| **SID** (*Study ID*) | Letra + número | `C5`, `P9`, `A1` | Identifica um estudo selecionado. A letra indica o tipo: **A** = artigos de periódico, **C** = artigos de congresso, **P** = preprints, **T** = teses/dissertações |
| **RRI** (*Research Result ID*) | # + número | `#42` | Identificador atribuído aos 296 resultados iniciais da busca, mantido para auditoria das 5 fases de seleção |
| **technique_id** | SID + `.tech` + número | `A1.tech7`, `C6.tech42` | Identificador único de cada IOPT |
| **experiment_id** | SID + `.exp` + número | `C5.exp23`, `P9.exp101` | Identificador único de cada experimento elegível |