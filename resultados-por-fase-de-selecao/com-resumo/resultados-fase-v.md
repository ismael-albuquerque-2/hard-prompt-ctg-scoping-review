# Beyond In-Context Learning: Aligning Long-form Generation of Large Language Models via Task-Inherent Attribute Guidelines

DOI: 10.18653/v1/2025.findings-acl.176
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #131

In-context learning (ICL) is an important yet not fully understood ability of large language models (LLMs). It can greatly enhance task performance using a few examples, termed demonstrations, without fine-tuning. Although effective in question answering, ICL often underperforms in long-form generation tasks such as summarization. Under appropriately realistic assumptions, we empirically and theoretically show that ICL demonstrations alone are insufficient to teach LLMs the task's language and format distributions for generation. We argue for explicit exposure to the task distributions and hypothesize that defining them by prompting enhances model performance. To this end, we present LongGuide, which efficiently generates two parallel streams of guidelines capturing task language and format properties: (i) Metric Guidelines (MGs) that instruct models to optimize self-evaluated metrics; and (ii) Output Constraint Guidelines (OCGs) that constrain generation at both token and sentence levels. LongGuide automatically selects the best combination of guidelines, improving both strong open- and closed-source LLMs by over 5% in both zero- and few-shot settings. LongGuide is generalizable, learnable by weak models to enhance strong ones, and integrates synergistically with automatic prompt optimizers. © 2025 Association for Computational Linguistics.

---

# Can Large Language Models Reliably Extract Physiology Index Values from Coronary Angiography Reports?

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #183

Coronary angiography (CAG) reports contain clinically relevant physiological measurements, yet this information is typically in the form of unstructured natural language, limiting its use in research. We investigate the use of Large Language Models (LLMs) to automatically extract these values, along with their anatomical locations, from Portuguese CAG reports. To our knowledge, this study is the first addressing physiology indexes extraction from a large (1342 reports) corpus of CAG reports, and one of the few focusing on CAG or Portuguese clinical text. We explore local privacy-preserving general-purpose and medical LLMs under different settings. Prompting strategies included zero-shot, few-shot, and few-shot prompting with implausible examples. In addition, we apply constrained generation and introduce a post-processing step based on RegEx. Given the sparsity of measurements, we propose a multi-stage evaluation framework separating format validity, value detection, and value correctness, while accounting for asymmetric clinical error costs. This study demonstrates the potential of LLMs in for extracting physiological indices from Portuguese CAG reports. Non-medical models performed similarly, the best results were obtained with Llama with a zero-shot prompting, while GPT-OSS demonstrated the highest robustness to changes in the prompts. While MedGemma demonstrated similar results to non-medical models, MedLlama's results were out-of-format in the unconstrained setting, and had a significant lower performance in the constrained one. Changes in the prompt techinique and adding a RegEx layer showed no significant improvement across models, while using constrained generation decreased performance, although having the benefit of allowing the usage of specific models that are not able to conform with the templates.

---

# PoeTone: A Framework for Constrained Generation of Structured Chinese Songci with LLMs

DOI: 10.1609/aaai.v40i39.40555
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #223

This paper presents a systematic investigation into the constrained generation capabilities of large language models (LLMs) in producing Songci, a classical Chinese poetry form characterized by strict structural, tonal, and rhyme constraints defined by Cipai templates. We first develop a comprehensive, multi-faceted evaluation framework that includes: (i) a formal conformity score, (ii) automated quality assessment using LLMs, (iii) human evaluation, and (iv) classification-based probing tasks. Using this framework, we evaluate the generative performance of 18 LLMs, including 3 proprietary models and 15 open-source models across 4 families, under five prompting strategies: zero-shot, one-shot, completion-based, instruction-based, and chain-of-thought. Finally, we propose a Generate-Critic architecture in which the evaluation framework functions as an automated critic. Leveraging the critic’s feedback as a scoring function for best-of-N selection, we fine-tune 3 lightweight open-source LLMs via supervised fine-tuning (SFT), resulting in improvements of up to 5.88% in formal conformity. Our findings offer new insights into the generative strengths and limitations of LLMs in producing culturally significant and formally constrained literary texts.

---

# Using Grammar Masking to Ensure Syntactic Validity in LLM-based Modeling Tasks

DOI: 10.1145/3652620.3687805
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #283

We present and evaluate a method called grammar masking, which is used to guide large language models (LLMs) toward producing syntactically correct models for a given context-free grammar. Prompt engineering methods such as few-shot learning or priming can be used to improve the chances of an LLM producing correct syntax, but the more complex the grammar, the more time-consuming and less promising these methods become. Previous work is focused primarily on the usage of either language model training or prompt engineering. In this work, a method is presented that restricts the output to a given grammar using constrained decoding to ensure the output adheres to a valid syntax. We use several domain-specific languages (DSLs) built with MontiCore and task multiple LLMs to produce models with and without constrained decoding. A corresponding parser is used to confirm the syntactic correctness of each model. We show that grammar masking can dramatically improve the modeling capabilities of several LLMs, reducing the need for well-refined prompting while increasing the chance of producing correct models.

---

# Cognitively Diverse Multiple-Choice Question Generation: A Hybrid Multi-Agent Framework with Large Language Models

DOI: 10.3390/electronics15061209
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #139

Recent advances in large language models (LLMs) have made automated multiple-choice question (MCQ) generation increasingly feasible; however, reliably producing items that satisfy controlled cognitive demands remains a challenge. To address this gap, we introduce ReQUESTA, a hybrid, multi-agent framework for generating cognitively diverse MCQs that systematically target text-based, inferential, and main idea comprehension. ReQUESTA decomposes MCQ authoring into specialized subtasks and coordinates LLM-powered agents with rule-based components to support planning, controlled generation, iterative evaluation, and post-processing. We evaluated the framework in a large-scale reading comprehension study using academic expository texts, comparing ReQUESTA-generated MCQs with those produced by a single-pass GPT-5 zero-shot baseline. Psychometric analyses of learner responses assessed item difficulty and discrimination, while expert raters evaluated question quality across multiple dimensions, including topic relevance and distractor quality. Results showed that ReQUESTA-generated items were consistently more challenging, more discriminative, and more strongly aligned with overall reading comprehension performance. Expert evaluations further indicated stronger alignment with central concepts and superior distractor linguistic consistency and semantic plausibility, particularly for inferential questions. These findings demonstrate that hybrid, agentic orchestration can systematically improve the reliability and controllability of LLM-based generation, highlighting workflow design as a key lever for structured artifact generation beyond single-pass prompting. © 2026 by the authors.

---

# Evaluating Prompting Strategies for Chart Question Answering with Large Language Models

DOI: 10.1007/978-3-032-14495-9_16
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #265

Prompting strategies affect LLM reasoning performance, but their role in chart-based QA remains underexplored. We present a systematic evaluation of four widely used prompting paradigms (Zero-Shot, Few-Shot, Zero-Shot Chain-of-Thought, and Few-Shot Chain-of-Thought) across GPT-3.5, GPT-4, and GPT-4o on the ChartQA dataset. Our framework operates exclusively on structured chart data, isolating prompt structure as the only experimental variable, and evaluates performance using two metrics: Accuracy and Exact Match. Results from 1,200 diverse ChartQA samples show that Few-Shot Chain-of-Thought prompting consistently yields the highest accuracy (up to 78.2%), particularly on reasoning-intensive questions, while Few-Shot prompting improves format adherence. Zero-Shot performs well only with high-capacity models on simpler tasks. These findings provide actionable guidance for selecting prompting strategies in structured data reasoning tasks, with implications for both efficiency and accuracy in real-world applications.

---

# Zero-Shot Strategies for Length-Controllable Summarization

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #245

Large language models (LLMs) struggle with precise length control, particularly in zero-shot settings. We conduct a comprehensive study evaluating LLMs' length control capabilities across multiple measures and propose practical methods to improve controllability. Our experiments with LLaMA 3 reveal stark differences in length adherence across measures and highlight inherent biases of the model. To address these challenges, we introduce a set of methods: length approximation, target adjustment, sample filtering, and automated revisions. By combining these methods, we demonstrate substantial improvements in length compliance while maintaining or enhancing summary quality, providing highly effective zero-shot strategies for precise length control without the need for model fine-tuning or architectural changes. With our work, we not only advance our understanding of LLM behavior in controlled text generation but also pave the way for more reliable and adaptable summarization systems in real-world applications.

---

# To be or not to be? an exploration of continuously controllable prompt engineering

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #181

As the use of large language models becomes more widespread, techniques like parameter-efficient fine-tuning and other methods for controlled generation are gaining traction for customizing models and managing their outputs. However, the challenge of precisely controlling how prompts influence these models is an area ripe for further investigation. In response, we introduce ControlPE (Continuously Controllable Prompt Engineering). ControlPE enables finer adjustments to prompt effects, complementing existing prompt engineering, and effectively controls continuous targets. This approach harnesses the power of LoRA (Low-Rank Adaptation) to create an effect akin to prompt weighting, enabling fine-tuned adjustments to the impact of prompts. Our methodology involves generating specialized datasets for prompt distillation, incorporating these prompts into the LoRA model, and carefully adjusting LoRA merging weight to regulate the influence of prompts. This provides a dynamic and adaptable tool for prompt control. Through our experiments, we have validated the practicality and efficacy of ControlPE. It proves to be a promising solution for control a variety of prompts, ranging from generating short responses prompts, refusal prompts to chain-of-thought prompts.

---

# Token-Oriented Object Notation vs JSON: A Benchmark of Plain and Constrained Decoding Generation

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #174

Recently presented Token-Oriented Object Notation (TOON) aims to replace JSON as a serialization format for passing structured data to LLMs with significantly reduced token usage. While showing solid accuracy in LLM comprehension, there is a lack of tests against JSON generation. Though never present in training data, TOON syntax is simple enough to suggest one-shot in-context learning could support accurate generation. The inevitable prompt overhead can be an acceptable trade-off for shorter completions. To test this, we conducted a benchmark creating several test cases with regard to structural complexity, a validation pipeline, and comparing plain JSON generation vs structured output (via constrained decoding) JSON generation vs TOON one-shot in-context learning generation. JSON structured output was included to establish a minimum token budget baseline and to set a starting point for future experiments testing TOON constrained decoding inference enforcement. Key findings: TOON shows promising accuracy/token consumption ratio for in-domain generation tasks, though this advantage is often reduced by the "prompt tax" of instructional overhead in shorter contexts. Plain JSON generation shows the best one-shot and final accuracy, even compared with constrained decoding structured output, where the only significant advantage is the lowest token usage as a trade-off for slightly decreased accuracy overall and significant degradation for some models. Notably, for simple structures, this "lowest token usage" of constrained decoding outperformed even TOON, hinting that TOON enforcing via frameworks such as xgrammar may not yield the desired results. Furthermore, the results suggest a scaling hypothesis: TOON's true efficiency potential likely follows a non-linear curve, shining only beyond a specific point where cumulative syntax savings amortize the initial prompt overhead.

---

# FANTAstic SEquences and Where to Find Them: Faithful and Efficient API Call Generation through State-tracked Constrained Decoding and Reranking

DOI: 10.18653/v1/2024.findings-emnlp.359
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #119

API call generation is the cornerstone of large language models' tool-using ability that provides access to the larger world. However, existing supervised and in-context learning approaches suffer from high training costs, poor data efficiency, and generated API calls that can be unfaithful to the API documentation and the user's request. To address these limitations, we propose an output-side optimization approach called FANTASE. Two of the unique contributions of FANTASE are its State-Tracked Constrained Decoding (SCD) and Reranking components. SCD dynamically incorporates appropriate API constraints in the form of Token Search Trie for efficient and guaranteed generation faithfulness with respect to the API documentation. The Reranking component efficiently brings in the supervised signal by leveraging a lightweight model as the discriminator to rerank the beam-searched candidate generations of the large language model. We demonstrate the superior performance of FANTASE in API call generation accuracy, inference efficiency, and context efficiency with DSTC8 and API Bank datasets. Our code is publicly available at https://github.com/Edillower/FANTASE. © 2024 Association for Computational Linguistics.

---

# STANDARDIZE: Aligning Language Models with Expert-Defined Standards for Content Generation

DOI: 10.18653/v1/2024.emnlp-main.94
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #98

Domain experts across engineering, healthcare, and education follow strict standards for producing quality content such as technical manuals, medication instructions, and children's reading materials. However, current works in controllable text generation have yet to explore using these standards as references for control. Towards this end, we introduce STANDARDIZE, a retrieval-style in-context learning-based framework to guide large language models to align with expert-defined standards. Focusing on English language standards in the education domain as a use case, we consider the Common European Framework of Reference for Languages (CEFR) and Common Core Standards (CCS) for the task of open-ended content generation. Our findings show that models can gain 45% to 100% increase in precise accuracy across open and commercial LLMs evaluated, demonstrating that the use of knowledge artifacts extracted from standards and integrating them in the generation process can effectively guide models to produce better standard-aligned content. © 2024 Association for Computational Linguistics.

---

# UltraGen: Extremely Fine-grained Controllable Generation via Attribute Reconstruction and Global Preference Optimization

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #155

Fine granularity is an essential requirement for controllable text generation, which has seen rapid growth with the ability of LLMs. However, existing methods focus mainly on a small set of attributes like 3 to 5, and their performance degrades significantly when the number of attributes increases to the next order of magnitude. To address this challenge, we propose a novel zero-shot approach for extremely fine-grained controllable generation (EFCG), proposing auto-reconstruction (AR) and global preference optimization (GPO). In the AR phase, we leverage LLMs to extract soft attributes (e.g., Emphasis on simplicity and minimalism in design) from raw texts, and combine them with programmatically derived hard attributes (e.g., The text should be between 300 and 400 words) to construct massive (around 45) multi-attribute requirements, which guide the fine-grained text reconstruction process under weak supervision. In the GPO phase, we apply direct preference optimization (DPO) to refine text generation under diverse attribute combinations, enabling efficient exploration of the global combination space. Additionally, we introduce an efficient attribute sampling strategy to identify and correct potentially erroneous attributes, further improving global optimization. Our framework significantly improves the constraint satisfaction rate (CSR) and text quality for EFCG by mitigating position bias and alleviating attention dilution.

---

# Instruct-SCTG: Guiding Sequential Controlled Text Generation through Instructions

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #203

Instruction-tuned large language models have shown remarkable performance in aligning generated text with user intentions across various tasks. However, maintaining human-like discourse structure in the generated text remains a challenging research question. In this paper, we propose Instruct-SCTG, a flexible and effective sequential framework that harnesses instruction-tuned language models to generate structurally coherent text in both fine-tuned and zero-shot setups. Our framework generates articles in a section-by-section manner, aligned with the desired human structure using natural language instructions. Furthermore, we introduce a new automatic metric that measures discourse divergence in a fuzzy manner. Extensive experiments on three datasets from representative domains of news and recipes demonstrate the state-of-the-art performance of our framework in imposing discourse structure during text generation, as verified by both automatic and human evaluation. Our code will be available on Github.

---

# Graph Grounded Cross Attention Transformer Neural Network for Structurally Constrained Full Event Sequence Generation in Predictive Process Monitoring

DOI: 10.2139/ssrn.6990079
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #184

Structurally constrained event sequence generation remains challenging because generated paths must preserve transition feasibility, temporal order, termination, and attribute consistency. In predictive process monitoring (PPM), this challenge appears as full event sequence generation, whereas existing work mainly addresses component tasks such as next activity, remaining time, outcome, and attribute prediction. This paper proposes the Graph Grounded Cross Attention Transformer Neural Network (GGATN) for this unified PPM task. GGATN uses a global process graph as structured activity memory, contextualizes sequence positions through Transformer self attention, and injects process topology through graph grounded cross attention. Unlike autoregressive decoding, GGATN generates activities, timestamps, length, and event level and sequence level attributes in a single pass, followed by Viterbi style graph constrained decoding for feasible paths and explicit termination. Experiments on six benchmark event logs show more reliable generation quality than local instruction prompted LLM baselines. GGATN achieves strong performance on sequence similarity, Damerau Levenshtein similarity, bigram based control flow similarity, and duration distribution, while maintaining zero hallucinated activities and zero sequence level attribute inconsistency. Ablation analyses confirm the global graph encoder as a stable structural prior. Interpretability analyses show how graph structure, sequence context, feedback refinement, and constrained decoding shape generation.

---

# Automated IEP Generation from Traditional Chinese Parent-Teacher Interviews via Corpus-Grounded Feature Diffusion

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #151

Writing Individualized Education Programs (IEPs) is a high-labor, knowledge-intensive document burden; English-language research has demonstrated that generative AI can significantly reduce drafting time, yet automated IEP generation in Traditional Chinese remains virtually unexplored due to domain data scarcity, strict privacy regulations, and the absence of local evaluation benchmarks. We propose a low-resource fine-tuning pipeline centered on Corpus-Grounded Feature Diffusion (CGFD): (1) 25 dual-expert high-score seed transcripts are selected via a tau threshold with flag-aware score caps; (2) a FeatureProfile (sentence length, structure, quantification templates) is extracted from seeds and injected into LLM prompts alongside Verbalized-Sampling-style diversity control to drive diffusion; (3) 15 expert gold seeds are used as diffusion anchors, targeting 585 samples; 567 valid diffusion samples are obtained, yielding a 582-sample training set used to fine-tune Breeze-7B with QLoRA; (4) schema-constrained inference via Grammar-Constrained Decoding (GCD) enforces a hierarchical SMART Goal Ladder schema at inference time. Ablation results on a 55-sample schema stress set reveal an unexpected finding: GCD is counterproductive under Traditional Chinese token budgets -- the no-GCD path achieves 100% schema pass rate at 34% lower median latency, outperforming GCD on both reliability and speed. On the n=10 formal hold-out, the no-GCD inference path achieves BERTScore F1 = 0.779, exceeding GPT-5.4 (0.726), DeepSeek-V3.2 (0.703), Gemini-3-Flash-Preview (0.703), and Llama-4-Maverick (0.700) zero-shot baselines while maintaining fully local, air-gapped inference. This system addresses a gap in Traditional Chinese special-education NLP and offers a scalable, privacy-preserving local inference solution under an industrial engineering paradigm.

---

# Two Shots are Enough: Reliable Constrained Generation with LLMs

DOI: 10.1109/BigData66926.2025.11402199
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #79

Despite exhibiting impressive performance across many complex tasks, Large Language Models (LLMs) often struggle to consistently produce structured responses, a key element in many applications such as agent orchestration. While template-based methods or in-context learning can improve structure compliance, constrained decoding and additional context have been shown to skew the distribution of the responses and may result in suboptimal performance. In this work, we show that the number of in-context examples is a key factor: in many settings, one to two shots are sufficient to reliably produce the predefined structures, while additional examples may degrade the response quality. Our analysis shows that this phenomenon is consistent across a wide range of datasets, models, and structures and indicates that providing this small number of shots achieves the best overall trade-off between structure compliance and response correctness while improving the results of constrained generation methods such as template-based approaches.

---

# Behavior Generation for Heterogeneous Agents in Urban Simulation Deduction: A Multi-Stage Approach Based on Large Language Models

DOI: 10.1109/IEEECONF65522.2025.11136878
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #83

Traditionally, constructing a professional simulation deduction script is a long-cycle process that requires collaboration between domain experts and simulation experts. The increasing demands for simulation deduction across large-scale scenarios and emergency situations highlight the need for rapid simulation scenario construction methods. Recent advances in large language models (LLMs) offer powerful new tools to address these challenges. In this work, we propose LLM-HABG, a highly portable framework that can automatically generate behavior plans for heterogeneous agents in urban simulation environments based on natural language instructions, requiring no additional post-training. It comprises four stages: task extraction, task decomposition and allocation, urban information retrieval, and behavior generation. To overcome the limitations of LLMs, such as deficient instruction-following and hallucinations, we incorporate a suite of enhancement techniques including dynamic few-shot learning, entity alignment, and constrained decoding. Experimental results demonstrate that LLM-HABG achieves robust performance even with 14B-parameter models, attaining a success rate exceeding 75 %-nearly doubling baseline performance. This conversational behavior configuration paradigm empowers domain experts to interact directly with simulation systems via natural language, significantly reducing the cost and barriers associated with simulation scenario construction.

---

# From Prompts to Templates: A Systematic Prompt Template Analysis for Real-world LLMapps

DOI: 10.18420/se2026-07
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #111

Large Language Model applications (LLMapps) increasingly rely on prompt templates: reusable instructions with placeholders, structure, and output constraints. Yet most templates are crafted ad hoc, which hampers reliability, maintainability, and downstream usability. This summary distills the core results from our paper published in Proceedings of the 33rd ACM International Conference on the Foundations of Software Engineering: “From Prompts to Templates: A Systematic Prompt Template Analysis for Real-world LLMapps”, a large-scale empirical study of real-world prompt templates, a component & placeholder taxonomy, and controlled tests showing which design patterns improve instruction following and structured-output stability in practice. © 2026 Gesellschaft fur Informatik (GI). All rights reserved.

---

# The OuLiBench Benchmark: Formal Constraints as a Lens into LLM Linguistic Competence

DOI: —
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #114

Recent progress in Large Language Models (LLMs) has led to impressive capabilities in Natural Language Generation (NLG). However, standard evaluation benchmarks often focus on surface-level performance and are predominantly English-centric, limiting insights into models’ deeper linguistic competences, especially in other languages. In this paper, we introduce OuLiBench, a novel benchmark inspired by the literary movement OuLiPo, designed to evaluate LLMs’ ability to generate Italian text under explicit linguistic constraints, ranging from morpho-syntactic requirements to creative and structural challenges. Our goal is to assess the extent to which LLMs can understand and manipulate language when guided by specific, sometimes artificial constraints. We evaluate a range of state-of-the-art models in both zero- and few-shot settings, comparing performance across constraint types and difficulty levels. Our results highlight significant variability across models and tasks, shedding light on the limits of controllable text generation and offering a new lens for probing LLMs’ generative and linguistic competence beyond traditional benchmarks. © 2025 Copyright for this paper by its authors.

---

# Enabling controllable table-to-text generation via prompting large language models with guided planning

DOI: 10.1016/j.knosys.2024.112571
Ano: 2024
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #260

Recently, Large Language Models (LLMs) has demonstrated unparalleled capabilities in understanding and generation, hence holding promising prospects for applying LLMs to table-to-text generation. However, the generation process with LLMs lacks a high degree of controllability, which hinders the utilization of LLMs for table-to-text generation. In this paper, we introduce Poised, an effective method that prompts LLMs with guided planning to achieve controllable table-to-text generation. Specifically, we first employ prefix-tuning on BART to derive a plan from the given table. Then, we combine the plan with guided instructions to create a comprehensive prompt, which is later input into LLMs to generate the description of the table. Experiments across three domains of the few-shot Wili dataset show that Poised achieves or approaches a plan completion rate of 100%, with an average hallucination frequency of less than 10%. Furthermore, Poised allows for finegrained control over the generated content by intentionally modifying the prompt, enabling precise control over aspects such as attribute realization order.

---

# Keyword-Centered Rescheduling for LLM Agents

DOI: 10.1007/s12559-026-10561-2
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #270

Recently, Large Language Model (LLM) agents have been widely deployed as conversational assistants, tutors, and productivity tools, where the personality of the agents emerges in generated sentences that reflect the extent of their extraversion or introversion. The style of the generated sentences can be adjusted to match a target extraversion level while preserving semantic fidelity. Traditional approaches , such as few-shot prompting and prompt tuning, have limited abilities to reflect the degree of extraversion of an agent. Therefore, it is required to extract and emphasize words that reflect their personalities. We propose a new framework, termed Keyword-centered Rescheduling, that inserts soft prompt embeddings before sentence-level keywords based on personality traits. This design enables fine-grained trait-specific modulation at the lexical level while maintaining semantic consistency and remains fully compatible with diverse LLM architectures without the need for additional fine-tuning or instruction alignment. On benchmark datasets, the method improved the normalized composite F1-Score by 60% and increased the human-judged Top-2 Semantic Fidelity by 26% (86% vs. 68%) over prompt tuning while maintaining comparable Behavioral Alignment. Beyond improving controllability, our approach provides a practical foundation for deploying robust, user-aligned LLM agents with on-demand, continuous personality control and stable semantics.

---

# Prompt-Based One-Shot Exact Length-Controlled Generation with LLMs

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #31

Controlling the length of text produced by large language models (LLMs) remains challenging: models frequently overshoot or undershoot explicit length instructions because they cannot reliably keep an internal token count. We present a prompt-based, one-shot strategy that compels an off-the-shelf LLM to generate exactly a desired number of tokens - words (English) or characters (Chinese) - without any fine-tuning or iterative sampling. The prompt appends countdown markers and explicit counting rules so that the model "writes while counting." We evaluate on four settings: open-ended generation (1-1000 tokens), XSUM summarization, MT-Bench-LI instruction following, and the LIFEBENCH equal-length track. On MT-Bench-LI, strict length compliance with GPT-4.1 leaps from below 30% under naive prompts to above 95% with our countdown prompt, surpassing the popular draft-then-revise baseline, while judged answer quality is preserved. These results show that precise length control can be achieved through prompt engineering alone, offering a lightweight alternative to training- or decoding-based methods.

---

# Is it Possible to Modify Text to a Target Readability Level? An Initial Investigation Using Zero-Shot Large Language Models

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #43

Text simplification is a common task where the text is adapted to make it easier to understand. Similarly, text elaboration can make a passage more sophisticated, offering a method to control the complexity of reading comprehension tests. However, text simplification and elaboration tasks are limited to only relatively alter the readability of texts. It is useful to directly modify the readability of any text to an absolute target readability level to cater to a diverse audience. Ideally, the readability of readability-controlled generated text should be independent of the source text. Therefore, we propose a novel readability-controlled text modification task. The task requires the generation of 8 versions at various target readability levels for each input text. We introduce novel readability-controlled text modification metrics. The baselines for this task use ChatGPT and Llama-2, with an extension approach introducing a two-step process (generating paraphrases by passing through the language model twice). The zero-shot approaches are able to push the readability of the paraphrases in the desired direction but the final readability remains correlated with the original text's readability. We also find greater drops in semantic and lexical similarity between the source and target texts with greater shifts in the readability.

---

# Different Teachers, Different Capabilities: Sub-1B On-Device Distillation for Structured Text Enrichment

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #73

High-volume structured extraction pays a large model's latency on every item, so distilling the task into a small on-device model is attractive: comparable output at a fraction of the time and cost. We measure what that distillation actually delivers, per sub-task. Each news article is mapped to one JSON object with a short summary and five categorical labels. We distill an 8B reasoning teacher (deepseek-r1:8b) into a 0.6B student (Qwen3-0.6B; QLoRA, three seeds), and add two teacher controls: a same-size non-reasoning teacher and a larger managed pipeline. A blinded, reference-free, three-judge panel scores every arm against the full article, alongside two non-distillation baselines, few-shot prompting and constrained decoding. The student runs at about 0.8 s per article against the teacher's 39 s, and recovers 58% of the base-to-teacher gap on summary quality, beating its primary baseline (constrained decoding) by +16.8 points and few-shot prompting by a secondary +4.9. A same-size non-reasoning teacher trains a student no better than the untuned base, so the summary gain follows from the teacher's reasoning nature rather than its scale. Capabilities then split by teacher: the reasoning teacher transfers writing quality and the managed pipeline transfers label diversity, while a same-size instruction teacher's students stay more grounded on the 22 short, thin-source articles in the 93-item test set (74 versus 55 faithful), where the reasoning-lineage student fabricates. That grounding difference is a consistent ordering rather than a significant aggregate effect, and the subgroup is small, so we report it as a direction. Because no single engine wins every field, the deliverable is a per-field routing map for on-device enrichment.

---

# The Hidden Cost of Structure: How Constrained Decoding Affects Language Model Performance

DOI: 10.26615/978-954-452-098-4-124
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #121

Large Language Models excel at generating fluent text, but real-world applications increasingly demand structured outputs like JSON that can be programmatically processed. While prior work examines either task performance or format compliance in isolation, we investigate their interaction through comprehensive experiments across 11 models and multiple benchmarks. We uncover a fundamental divergence between base and instruction-tuned models under structural constraints. Base models often benefit from constrained decoding, producing more precise outputs, while instruction-tuned models frequently suffer performance degradation on generation tasks despite maintaining stability on classification tasks. Our log probability analysis reveals the underlying mechanism: constrained decoding forces models away from their preferred natural language patterns into lower-confidence structured alternatives. We demonstrate that successful constrained generation requires both adapted prompts and sufficient few-shot examples, with constrained models showing steeper performance gains from additional demonstrations compared to unconstrained generation. Notably, we find that base model performance under constraints can serve as an early indicator of post-training structured output capabilities, offering a practical evaluation tool for model development. These findings suggest that current instruction-tuning practices may inadvertently reduce models’ structured output capabilities and highlight the need for training-time integration of structural constraints in future model development. © 2025 Incoma Ltd. All rights reserved.

---

# КОНСТРУЮВАННЯ ЗАПИТІВ ДЛЯ КЛАСИФІКАЦІЇ ЗЕМНОГО ПОКРИВУ БЕЗ НАВЧАЛЬНИХ ПРИКЛАДІВ ЗА ДОПОМОГОЮ МУЛЬТИМОДАЛЬНИХ МОВНИХ МОДЕЛЕЙ НА ЗНИМКАХ SENTINEL-2

DOI: 10.34185/1562-9945-4-165-2026-13
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #145

Multimodal language models (VLMs) enable land cover classification from satellite imagery without labeled training data. This paper, extending previous work [8], analyzes prompt engineering approaches for land cover classification on Sentinel-2 imagery within the ESA WorldCover 2021 taxonomy. The color leakage phenomenon is identified and described, where the model bases its predictions on segmentation mask colors rather than image content. A four-invariant prompt protocol is proposed, including TCI-first ordering, grayscale mask conversion, elimination of color descriptions, and a fixed JSON output format, which removes this effect and increases the format compliance rate (FCR) from ≈60% to 97%. Two inference strategies are compared: Variant A (multi-cluster, mIoU ≈ 7.1%) and Variant B (single-cluster, mIoU ≈ 13.2%) on 10 Sentinel-2 tiles. In Variant B, each segment is processed independently using a binary mask, which simplifies spatial interpretation and reduces inter-segment interference. The highest result (mIoU = 46.2%) is achieved with the UNet-encoder + GPT-4.1 + Variant B configuration, although this corresponds to a single case.
Problem Statement. Land cover mapping from satellite imagery is widely used in ecological monitoring, urban planning, and agronomy. Traditional semantic segmentation approaches require large labeled datasets and significant computational resources, especially when adapting to new regions. Recent multimodal language models, including GPT-4.1, Claude 3.7 Sonnet, and Gemini 2.5 Pro, enable zero-shot classification without task-specific training. However, such pipelines introduce specific failure modes, notably the color leakage effect, where predictions depend on segmentation mask colors instead of actual image content.
Recent Studies and Publications Analysis. VLMs are increasingly used in remote sensing owing to their capacity for open-vocabulary reasoning over satellite imagery. Yao et al. introduced Falcon, a remote sensing vision-language foundation model; Mall et al. developed RSVLM for satellite image understanding; Li et al. presented RS-CLIP for zero-shot scene classification. Liu et al. proposed RSHBench — a detailed benchmark for diagnosing hallucinations in multimodal LLMs applied to remote sensing. For zero-shot learning, Saha et al. demonstrated improved classification by adapting VLMs with attribute descriptions; Barzilai et al. analysed recipes for improving VLM zero-shot accuracy in remote sensing. In prompt engineering, Wei et al. established chain-of-thought prompting and White et al. catalogued reusable prompt patterns. Geirhos et al. documented shortcut learning in deep networks, providing theoretical grounding for the color leakage phenomenon. Despite these advances, systematic analysis of prompt design for eliminating color artifacts in VLM-based land cover classification remains unstudied.
Research Objective. The objective of this study is to improve classification accuracy (mIoU) and structured output correctness (FCR) in zero-shot land cover classification on Sentinel-2 imagery by developing a prompt engineering protocol for multimodal language models that eliminates the color leakage effect and enforces a fixed structure of inputs and outputs.
Main Body of Research. A two-stage processing pipeline is used, combining unsupervised segmentation with VLM-based classification under a four-invariant protocol: TCI-first ordering, grayscale mask, no color descriptions, and structured JSON output. Variant A performs classification of all segments in a single request, while Variant B processes each segment independently using a binary mask. This change in formulation improves mIoU from 7.1% to 13.2%. Ablation analysis (n = 5 tiles) shows that the JSON output constraint has the largest impact on FCR, while grayscale mask conversion most effectively reduces color leakage. Per-class analysis indicates that the improvement is primarily driven by the Cropland class (23.4% → 46.9%), whereas spectrally similar vegetation classes degrade.
Conclusions. The study addresses the problem of improving classification accuracy (mIoU) and structured output correctness (FCR) in zero-shot land cover classification on Sentinel-2 satellite imagery through the development of a prompt engineering protocol for multimodal language models. The proposed protocol, consisting of four mandatory rules, eliminates the color leakage effect and increases FCR from ≈60% to 97%.
It is shown that the use of the single-cluster processing strategy (Variant B), in which each segment is processed independently using a binary mask, improves classification accuracy from 7.1% to 13.2% compared to the multi-cluster strategy (Variant A). This approach eliminates inter-segment context contamination, simplifies segment interpretation for the model, and improves structured output correctness, as each request produces a single JSON object. The highest result (mIoU = 46.2%) is achieved with the UNet-encoder + GPT-4.1 + Variant B configuration; however, this corresponds to a single configuration and is not representative of overall performance across models and segmentation methods.

---

# An adversarial testing framework for AI-driven task routing systems

DOI: 10.31649/1681-7893-2026-51-1-374-381
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #198

The paper presents an adversarial testing methodology for evaluating AI-driven task routing systems. The methodology defines structured attack scenarios and strict output constraints to measure resistance against unauthorized data disclosure. To validate suggested approach, an AI-based routing solution implemented using an Salesforce Agentforce Prompt Template powered by ChatGPT 5 was tested in a controlled environment. It has been proven that using a structured approach to testing can reduce the risk of data leakage in AI-based decision support systems.

---

# VARIA: Benchmarking Frontier LLMs on Construct-Equivalent Assessment Variant Generation

DOI: 10.35542/osf.io/u6xef_v1
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #249

In plain terms: if we are going to let AI write personalized versions of tests for every student, those versions have to be more than surface paraphrase. They have to look genuinely different on the outside while still measuring the same underlying skill on the inside. This paper asks whether today's frontier AI models can actually do that, and offers a way to measure it.AI-Integrated Authentic Assessment (AIAA) frameworks propose to replace surveillance-based proctoring with per-student task variation: each examinee receives a unique-yet-equivalent performance task, making answer copying useless without invasive monitoring. The framework's no-surveillance integrity guarantee is conditional on a presumed but unverified capability: that large language models can generate parallel variants of an assessment blueprint that are simultaneously surface-distinct, construct-equivalent, rubric-applicable, and difficulty-matched. We introduce VARIA, a benchmark that operationalizes this presumption as four measurable properties of a generated variant set. VARIA evaluates three frontier model families (Anthropic Claude Opus 4.7, OpenAI GPT-5.5, Google Gemini 3.1 Pro Preview) across four prompting strategies (zero-shot, few-shot with anchor examples, structured chain-of-thought, dimension-preserving constrained generation) on three competency-based blueprints drawn from applied AI and data analytics, alongside two non-frontier reference systems (a small open instruction-tuned model and GPT-2 small) and two targeted ablations. A pilot of 600 generated variants across 60 condition cells reveals that frontier strategies cluster tightly on a composite integrity score (joint J between 0.81 and 0.88) while the non-frontier references collapse to J between 0.50 and 0.55, a forty-percentage-point gap that establishes the benchmark's discrimination. Within the frontier band, structured chain-of-thought and zero-shot prompting maximize construct equivalence; dimension-preserving constrained generation and few-shot anchoring maximize surface diversity; and the two regimes trade against each other on readability parity. We release VARIA, recommend a generation protocol keyed to the deploying institution's threat profile, and pre-register a follow-up that will measure rubric stability and behavioral copy-resistance.

---

# Generování Blockly XML pro detekci událostí z logů pomocí jazykových modelů: Generating Blockly XML to detect alerts in logs using language models

DOI: —
Ano: —
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: OATD
RRI: #254

This thesis examines large language models and their applications in log-based event detection, including their limitations and techniques for enhancing performance such as prompt engineering, retrieval-augmented generation (RAG), grammar-constrained decoding, and fine-tuning. The target environment Logmanager was examined, with emphasis on its alert rules in the platform-specific Blockly implementation. A system for automated alert generation from natural language was proposed and implemented, comprising an intermediate JSON representation, a deterministic parser for conversion to the target XML format, a RAG pipeline for dynamic retrieval of relevant log fields, and two alternative approaches to the generative model: fine-tuning a smaller model for local deployment or utilizing a cloud-based large language model. Evaluation showed that the best-performing configurations of both approaches were capable of generating syntactically and semantically valid alert structures, and of applying user-requested corrections to existing alerts. Enforcing output format constraints proved to be a critical factor in eliminating structurally invalid outputs in both cases. This thesis demonstrates that automated alert generation from natural language is feasible, with fine-tuned small models proving to be a competitive alternative to cloud-based solutions.

---

# Guidance Conditions in Generative Modeling: Elevating Discriminative Capabilities and Controllability

DOI: —
Ano: 2025
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: OATD
RRI: #255

Generative models, such as diffusion models and large language models (LLMs), play a crucial role in artificial intelligence due to their remarkable generative quality and versatility. These models leverage deep neural network architectures to sample new data points from complex data distributions that cannot be expressed in analytical form. Due to the demand for controllability in real-world applications, various guidance methods have emerged for conditional generation. For example, text-to-image generation and image captioning utilize encoded features as conditions, while in-context learning conditions generation directly on the input data. Achieving this level of conditional adherence requires a delicate balance between generative diversity and discriminative precision. My research focuses on leveraging generative models for generative tasks that require deterministic precision or discriminative tasks under uncertainty. The first section of this thesis introduces the development of the LRA-diffusion model, which is a stochastic classifier trained using noisy labels. This work formulates classification as an image-guided label generation task. It learns from noisy labels and generates label estimation based on learned label distribution for images by leveraging neighbor consistency in the feature space of pre-trained models, such as SimCLR and CLIP. The second section presents the development of LACE, a diffusion model for layout generation, which unifies various conditional layout generation tasks in a single model by masking partial attributes in training. By training diffusion models with differentiable constraints, LACE achieves superior performance across several metrics, including FID, MaxIoU, and Alignment, compared to existing discrete diffusion models. With the advent of large language models (LLMs) and their ability to understand and generate structured text, we explore how text guidance and content awareness can further enhance controlled generation in layout tasks. The third section introduces TextLap, an LLM customized for layout generation, where generation is explicitly conditioned on text prompts. By supervised fine-tuning on curated datasets, TextLap learns to arrange spatial relationships between layout elements and generate structured representations, such as CSS and JSON. The final section focuses on enhancing efficiency and accuracy in multi-modal large language models (MLLMs) through refined multimodal conditioning. This work introduces a self-visual-RAG framework that enables MLLMs to process multi-page, visually rich documents efficiently. It optimizes MLLMs as multimodal retrievers, reducing the input length by retrieving relevant pages from the document, allowing MLLMs to focus on a shorter context before generating responses. This structured approach refines multimodal conditions, ensuring that text generation remains accurate, contextually grounded, and computationally efficient. **To request an accessible version of the file(s) associated with this item, contact library@buffalo.edu.…

---

# LLM-based JSON Mapping and Blockchain Integration for Digital Product Passports☆,☆☆

DOI: 10.1016/j.digbus.2026.100167
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #276

The European Commission envisages Digital Product Passports (DPPs) as a mechanism to enable traceable, transparent, and standardized product data across supply chains. This work presents a modular pipeline that transforms raw sensor data into verifiable DPP records using large language models (LLMs) for data standardization and blockchain technology for tamper-proof storage. The system maps unstructured machine-level data to a standardized JSON format and stores it immutably on the Waves blockchain via smart contracts, thereby enabling auditable, machine-readable records suitable for regulatory use. A novel evaluation dataset is introduced to simulate daily production scenarios with varying mapping complexity. The performance of the system is assessed using both proprietary and open-weight LLMs. Results show that the proprietary model achieves the highest accuracy and lowest latency, while open-weight models perform worse as input complexity increases. Multiple prompting strategies were compared, revealing that direct mapping, via few-shot or zero-shot prompts, consistently delivered higher accuracy than approaches based on generating transformation functions. Structured output formatting was also assessed: While it ensured schema validity, it often compromised mapping reliability by introducing incorrect values, likely due to disruptions in model reasoning from output constraints. The proposed architecture demonstrates reliable end-to-end operation with low latency and is suitable for batch-level deployment in real-world production environments. From a practical perspective, the results clarify trade-offs between model choice, prompting strategy, and operational reliability in automated DPP generation. For policymakers, the findings highlight how choices around schema clarity and data granularity shape system design and operational effort in future DPP implementations.