# TreeCoder: Systematic Exploration and Optimisation of Decoding and Constraints for LLM Code Generation

DOI: 10.1145/3808347
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #99

Large language models (LLMs) have shown remarkable ability to generate code, yet their outputs often violate syntactic or semantic constraints when guided only through natural language prompts. We introduce TreeCoder, the most general and flexible framework to date for exploring decoding strategies, constraints, and hyperparameters in LLMs, and use it in code generation to enforce correctness and structure during decoding rather than relying on prompt engineering. TreeCoder represents decoding as a tree search over candidate programs, where both decoding strategies and constraint functions–such as style, syntax, execution–are treated as first-class, optimisable components. This design enables systematic exploration and automatic tuning of decoding configurations using standard optimisation techniques. Experiments on Python, SQL and Rust show that TreeCoder consistently improves accuracy across open-source models such as CodeLlama, Mistral, DeepSeek and Qwen, often significantly outperforming their unconstrained baselines. © 2026 Copyright held by the owner/author(s).

---

# From Human Judgements to Predictive Models: Unravelling Acceptability in Code-Mixed Sentences

DOI: 10.1145/3748312
Ano: 2025
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #291

Current computational approaches for analysing or generating code-mixed sentences do not explicitly model "naturalness" or "acceptability" of code-mixed sentences, but rely on training corpora to reflect distribution of acceptable code-mixed sentences. Modelling human judgement for the acceptability of code-mixed text can help in distinguishing natural code-mixed text and enable quality-controlled generation of code-mixed text. To this end, we construct Cline-a dataset containing human acceptability judgements for English-Hindi (en-hi) code-mixed text. Cline is the largest of its kind with 16,642 sentences, consisting of samples sourced from two sources: synthetically generated code-mixed text and samples collected from online social media. Our analysis establishes that popular code-mixing metrics such as CMI, Number of Switch Points, Burstines, which are used to filter/curate/compare code-mixed corpora have low correlation with human acceptability judgements, underlining the necessity of our dataset. Experiments using Cline demonstrate that simple Multilayer Perceptron (MLP) models when trained solely using code-mixing metrics as features are outperformed by fine-tuned pre-trained Multilingual Large Language Models (MLLMs). Specifically, among Encoder models XLM-Roberta and Bernice outperform IndicBERT across different configurations. Among Encoder-Decoder models, mBART performs better than mT5, however, Encoder-Decoder models are not able to outperform Encoder-only models. Decoder-only models perform the best when compared with all other MLLMS, with Llama 3.2-3B models outperforming similarly sized Qwen, Phi models. Comparison with zero and fewshot capabilitites of ChatGPT show that MLLMs fine-tuned on larger data outperform ChatGPT, providing scope for improvement in code-mixed tasks. Zero-shot transfer from English-Hindi to English-Telugu acceptability judgments using our model checkpoints proves superior to random baselines, enabling application to other code-mixed language pairs and providing further avenues of research. We publicly release our human-annotated dataset, trained checkpoints, code-mix corpus, and code for data generation and model training.

---

# Controllable Text Generation for Large Language Models: A Survey

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #144

In Natural Language Processing (NLP), Large Language Models (LLMs) have demonstrated high text generation quality. However, in real-world applications, LLMs must meet increasingly complex requirements. Beyond avoiding misleading or inappropriate content, LLMs are also expected to cater to specific user needs, such as imitating particular writing styles or generating text with poetic richness. These varied demands have driven the development of Controllable Text Generation (CTG) techniques, which ensure that outputs adhere to predefined control conditions--such as safety, sentiment, thematic consistency, and linguistic style--while maintaining high standards of helpfulness, fluency, and diversity. This paper systematically reviews the latest advancements in CTG for LLMs, offering a comprehensive definition of its core concepts and clarifying the requirements for control conditions and text quality. We categorize CTG tasks into two primary types: content control and attribute control. The key methods are discussed, including model retraining, fine-tuning, reinforcement learning, prompt engineering, latent space manipulation, and decoding-time intervention. We analyze each method's characteristics, advantages, and limitations, providing nuanced insights for achieving generation control. Additionally, we review CTG evaluation methods, summarize its applications across domains, and address key challenges in current research, including reduced fluency and practicality. We also propose several appeals, such as placing greater emphasis on real-world applications in future research. This paper aims to offer valuable guidance to researchers and developers in the field. Our reference list and Chinese version are open-sourced at https://github.com/IAAR-Shanghai/CTGSurvey.

---

# Low-code LLM: Graphical User Interface over Large Language Models

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #197

Utilizing Large Language Models (LLMs) for complex tasks is challenging, often involving a time-consuming and uncontrollable prompt engineering process. This paper introduces a novel human-LLM interaction framework, Low-code LLM. It incorporates six types of simple low-code visual programming interactions to achieve more controllable and stable responses. Through visual interaction with a graphical user interface, users can incorporate their ideas into the process without writing trivial prompts. The proposed Low-code LLM framework consists of a Planning LLM that designs a structured planning workflow for complex tasks, which can be correspondingly edited and confirmed by users through low-code visual programming operations, and an Executing LLM that generates responses following the user-confirmed workflow. We highlight three advantages of the low-code LLM: user-friendly interaction, controllable generation, and wide applicability. We demonstrate its benefits using four typical applications. By introducing this framework, we aim to bridge the gap between humans and LLMs, enabling more effective and efficient utilization of LLMs for complex tasks. The code, prompts, and experimental details are available at https://github.com/moymix/TaskMatrix/tree/main/LowCodeLLM. A system demonstration video can be found at https://www.youtube.com/watch?v=jb2C1vaeO3E.

---

# Beyond In-Context Learning: Aligning Long-form Generation of Large Language Models via Task-Inherent Attribute Guidelines

DOI: 10.18653/v1/2025.findings-acl.176
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #131

In-context learning (ICL) is an important yet not fully understood ability of large language models (LLMs). It can greatly enhance task performance using a few examples, termed demonstrations, without fine-tuning. Although effective in question answering, ICL often underperforms in long-form generation tasks such as summarization. Under appropriately realistic assumptions, we empirically and theoretically show that ICL demonstrations alone are insufficient to teach LLMs the task's language and format distributions for generation. We argue for explicit exposure to the task distributions and hypothesize that defining them by prompting enhances model performance. To this end, we present LongGuide, which efficiently generates two parallel streams of guidelines capturing task language and format properties: (i) Metric Guidelines (MGs) that instruct models to optimize self-evaluated metrics; and (ii) Output Constraint Guidelines (OCGs) that constrain generation at both token and sentence levels. LongGuide automatically selects the best combination of guidelines, improving both strong open- and closed-source LLMs by over 5% in both zero- and few-shot settings. LongGuide is generalizable, learnable by weak models to enhance strong ones, and integrates synergistically with automatic prompt optimizers. © 2025 Association for Computational Linguistics.

---

# Enhancing Pre-Trained Generative Language Models with Question Attended Span Extraction on Machine Reading Comprehension

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #153

Machine Reading Comprehension (MRC) poses a significant challenge in the field of Natural Language Processing (NLP). While mainstream MRC methods predominantly leverage extractive strategies using encoder-only models such as BERT, generative approaches face the issue of out-of-control generation -- a critical problem where answers generated are often incorrect, irrelevant, or unfaithful to the source text. To address these limitations in generative models for MRC, we introduce the Question-Attended Span Extraction (QASE) module. Integrated during the fine-tuning phase of pre-trained generative language models (PLMs), QASE significantly enhances their performance, allowing them to surpass the extractive capabilities of advanced Large Language Models (LLMs) such as GPT-4 in few-shot settings. Notably, these gains in performance do not come with an increase in computational demands. The efficacy of the QASE module has been rigorously tested across various datasets, consistently achieving or even surpassing state-of-the-art (SOTA) results, thereby bridging the gap between generative and extractive models in extractive MRC tasks.

---

# Taxonomy-Guided Zero-Shot Recommendations with LLMs

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #227

With the emergence of large language models (LLMs) and their ability to perform a variety of tasks, their application in recommender systems (RecSys) has shown promise. However, we are facing significant challenges when deploying LLMs into RecSys, such as limited prompt length, unstructured item information, and un-constrained generation of recommendations, leading to sub-optimal performance. To address these issues, we propose a novel method using a taxonomy dictionary. This method provides a systematic framework for categorizing and organizing items, improving the clarity and structure of item information. By incorporating the taxonomy dictionary into LLM prompts, we achieve efficient token utilization and controlled feature generation, leading to more accurate and contextually relevant recommendations. Our Taxonomy-guided Recommendation (TaxRec) approach features a two-step process: one-time taxonomy categorization and LLM-based recommendation, enabling zero-shot recommendations without the need for domain-specific fine-tuning. Experimental results demonstrate TaxRec significantly enhances recommendation quality compared to traditional zero-shot approaches, showcasing its efficacy as personal recommender with LLMs. Code is available at https://github.com/yueqingliang1/TaxRec.

---

# DiCoRe: Enhancing Zero-shot Event Detection via Divergent-Convergent LLM Reasoning

DOI: 10.18653/v1/2025.emnlp-main.1038
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #104

Zero-shot Event Detection (ED), the task of identifying event mentions in natural language text without any training data, is critical for document understanding in specialized domains. Understanding the complex event ontology, extracting domain-specific triggers from the passage, and structuring them appropriately overloads and limits the utility of Large Language Models (LLMs) for zero-shot ED. To this end, we propose DICORE, a divergent-convergent reasoning framework that decouples the task of ED using Dreamer and Grounder. Dreamer encourages divergent reasoning through open-ended event discovery, which helps to boost event coverage. Conversely, Grounder introduces convergent reasoning to align the free-form predictions with the task-specific instructions using finite-state machine guided constrained decoding. Additionally, an LLM-Judge verifies the final outputs to ensure high precision. Through extensive experiments on six datasets across five domains and nine LLMs, we demonstrate how DICORE consistently outperforms prior zero-shot, transfer-learning, and reasoning baselines, achieving 4-7% average F1 gains over the best baseline - establishing DICORE as a strong zero-shot ED framework. © 2025 Association for Computational Linguistics.

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

# Prompting Is All You Need: Multi-view Prompting Large Language Models for Aspect-Based Sentiment Analysis

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #213

Recent work explored the capabilities of Large Language Models (LLMs) in Aspect-Based Sentiment Analysis (ABSA) through few-shot prompting, requiring substantially fewer annotated examples while achieving notable improvements over zero-shot baselines. However, a performance gap remained compared to models fine-tuned on hundreds of examples, and the computational costs of LLM inference present practical barriers to deployment. We introduce LLM-based Multi-View Prompting (LLM-MvP), which adapts the multi-view principle of considering multiple element orderings to LLM prompting. By combining schema-constrained decoding with a context-free grammar and prefix batching, LLM-MvP achieves performance competitive or superior to fine-tuned approaches while substantially reducing computational overhead. Extensive experiments across five benchmark datasets demonstrate that LLM-MvP closes the gap between few-shot prompting and fine-tuned models, offering a practical and efficient solution for ABSA.

---

# SynLLM: A Comparative Analysis of Large Language Models for Medical Tabular Synthetic Data Generation via Prompt Engineering

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #167

Access to real-world medical data is often restricted due to privacy regulations, posing a significant barrier to the advancement of healthcare research. Synthetic data offers a promising alternative; however, generating realistic, clinically valid, and privacy-conscious records remains a major challenge. Recent advancements in Large Language Models (LLMs) offer new opportunities for structured data generation; however, existing approaches frequently lack systematic prompting strategies and comprehensive, multi-dimensional evaluation frameworks. In this paper, we present SynLLM, a modular framework for generating high-quality synthetic medical tabular data using 20 state-of-the-art open-source LLMs, including LLaMA, Mistral, and GPT variants, guided by structured prompts. We propose four distinct prompt types, ranging from example-driven to rule-based constraints, that encode schema, metadata, and domain knowledge to control generation without model fine-tuning. Our framework features a comprehensive evaluation pipeline that rigorously assesses generated data across statistical fidelity, clinical consistency, and privacy preservation. We evaluate SynLLM across three public medical datasets, including Diabetes, Cirrhosis, and Stroke, using 20 open-source LLMs. Our results show that prompt engineering significantly impacts data quality and privacy risk, with rule-based prompts achieving the best privacy-quality balance. SynLLM establishes that, when guided by well-designed prompts and evaluated with robust, multi-metric criteria, LLMs can generate synthetic medical data that is both clinically plausible and privacy-aware, paving the way for safer and more effective data sharing in healthcare research.

---

# Prompt-Based Length Controlled Generation with Reinforcement Learning

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #224

Large language models (LLMs) like ChatGPT and GPT-4 have attracted great attention given their surprising performance on a wide range of NLP tasks. Length controlled generation of LLMs emerges as an important topic, which enables users to fully leverage the capability of LLMs in more real-world scenarios like generating a proper answer or essay of a desired length. In addition, the autoregressive generation in LLMs is extremely time-consuming, while the ability of controlling this generated length can reduce the inference cost by limiting the length. Therefore, we propose a prompt-based length control method to achieve high-accuracy length controlled generation. In particular, we adopt reinforcement learning with the reward signal given by either trainable or rule-based reward models, which further enhances the length-control ability of LLMs by rewarding outputs that follows pre-defined control instruction. To enable rule-based inference, we also introduce standard prompt extractor to collect the standard control information from users' input. Experiments show that our method significantly improves the accuracy of prompt-based length control for summarization task on popular datasets like CNNDM and NYT. Both the standard prompt extractor and the RL-tuned model have show strong generalization ability to unseen control prompt templates.

---

# ASR Error Correction Using Large Language Models

DOI: 10.1109/TASLPRO.2025.3551083
Ano: 2025
Tipo de documento: Artigo de periódico
Base onde foi encontrado: IEEE Xplore
RRI: #85

Error correction (EC) models play a crucial role in refining Automatic Speech Recognition (ASR) transcriptions, enhancing the readability and quality of transcriptions. Without requiring access to the underlying code or model weights, EC can improve performance and provide domain adaptation for black-box ASR systems. This work investigates the use of large language models (LLMs) for error correction across diverse scenarios. 1-best ASR hypotheses are commonly used as the input to EC models. We propose building high-performance EC models using ASR N-best lists which should provide more contextual information for the correction process. Additionally, the generation process of a standard EC model is unrestricted in the sense that any output sequence can be generated. For some scenarios, such as unseen domains, this flexibility may impact performance. To address this, we introduce a constrained decoding approach based on the N-best list or an ASR lattice. Finally, most EC models are trained for a specific ASR system requiring retraining whenever the underlying ASR system is changed. This paper explores the ability of EC models to operate on the output of different ASR systems. This concept is further extended to zero-shot error correction using LLMs, such as ChatGPT. Experiments on three standard datasets demonstrate the efficacy of our proposed methods for both Transducer and attention-based encoder-decoder ASR systems. In addition, the proposed method can serve as an effective method for model ensembling.

---

# Using Grammar Masking to Ensure Syntactic Validity in LLM-based Modeling Tasks

DOI: 10.1145/3652620.3687805
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #283

We present and evaluate a method called grammar masking, which is used to guide large language models (LLMs) toward producing syntactically correct models for a given context-free grammar. Prompt engineering methods such as few-shot learning or priming can be used to improve the chances of an LLM producing correct syntax, but the more complex the grammar, the more time-consuming and less promising these methods become. Previous work is focused primarily on the usage of either language model training or prompt engineering. In this work, a method is presented that restricts the output to a given grammar using constrained decoding to ensure the output adheres to a valid syntax. We use several domain-specific languages (DSLs) built with MontiCore and task multiple LLMs to produce models with and without constrained decoding. A corresponding parser is used to confirm the syntactic correctness of each model. We show that grammar masking can dramatically improve the modeling capabilities of several LLMs, reducing the need for well-refined prompting while increasing the chance of producing correct models.

---

# Toward Unified Controllable Text Generation via Regular Expression Instruction

DOI: 10.18653/v1/2023.ijcnlp-main.1
Ano: 2023
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #143

Controllable text generation is a fundamental aspect of natural language generation, with numerous methods proposed for different constraint types. However, these approaches often require significant architectural or decoding modifications, making them challenging to apply to additional constraints or resolve different constraint combinations. To address this, our paper introduces Regular Expression Instruction (REI), which utilizes an instruction-based mechanism to fully exploit regular expressions’ advantages to uniformly model diverse constraints. Specifically, our REI supports all popular fine-grained controllable generation constraints, i.e., lexical, positional, and length, as well as their complex combinations, via regular expression-style instructions. Our method only requires fine-tuning on medium-scale language models or few-shot, in-context learning on large language models, and requires no further adjustment when applied to various constraint combinations. Experiments demonstrate that our straightforward approach yields high success rates and adaptability to various constraints while maintaining competitiveness in automatic metrics and outperforming most previous baselines.1 © 2023 Association for Computational Linguistics.

---

# BIPro: Zero-shot Chinese Poem Generation via Block Inverse Prompting Constrained Generation Framework

DOI: 10.18653/v1/2025.acl-long.56
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #122

Recently, generative pre-trained models have made significant strides, particularly highlighted by the release of ChatGPT and GPT-4, which exhibit superior cross-domain capabilities. However, these models still face challenges on constrained writing tasks like poem generation under open-domain titles via direct generation. In response to this challenge, we introduce Block Inverse Prompting (BIPro) constrained generation framework. BIPro leverages two block inverse prompting methods, revise and rewrite. This inference scaling approach mimics the process of human text writing using block generative models. It significantly improves the zero-shot generation quality on the constrained generation task of open-domain traditional-form Chinese poem generation. Based on a less powerful block generative model GLM-10B-Chinese, poems composed via BIPro without priming or additional training outperform both much larger direct generative systems like GPT-4 or GLM-4 and domain-specific systems such as Yusheng, Shisanbai, or Baidu Poetry Helper in human evaluation by proficient poets. BIPro considerably narrows the gap between AI-generated works and short-listed human literary arts in another human evaluation, unveiling the promising potential of inference scaling in improving the quality of constrained generation. It is open-sourced and available as an agent in chatglm app. © 2025 Association for Computational Linguistics.

---

# A Roadmap for Tamed Interactions with Large Language Models

DOI: 10.1145/3832776
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #20

Large Language Models (LLMs) are increasingly embedded in software systems ( GenAIware), enabling new forms of automation and interaction However, their probabilistic nature and reliance on prompt programming challenge reliability, robustness, and maintainability In current practice, prompt-related concerns (e.g., context management, interaction logic, output validation) are embedded in general-purpose code, leading to implicit, hard-to-analyze systems We argue that prompt programming should be treated as a first-class Software Engineering (SE ) concern and propose LLM Scripting Language (LSL ), a Domain Specific Language ( DSL) for structuring LLM interactions as analyzable programs LSL introduces abstractions for interaction blocks, context scopes, output constraints, and control flow, separating deterministic logic from probabilistic model behavior while ensuring syntactic compliance From an SE perspective, LSL supports disciplined development by making interaction logic explicit, analyzable, and amenable to verification and validation It also acts as cognitive scaffolding, externalizing prompt design into programmable artifacts that reduce implicit reasoning and support systematic debugging, evolution, and reuse We illustrate these properties in a structured generation scenario, showing improved failure localization and interaction transparency While LSL does not guarantee semantic correctness or factual accuracy, it provides a principled foundation for more analyzable and maintainable prompt-based systems.

---

# TINYSTYLER: Efficient Few-Shot Text Style Transfer with Authorship Embeddings

DOI: 10.18653/v1/2024.findings-emnlp.781
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #109

The goal of text style transfer is to transform the style of texts while preserving their original meaning, often with only a few examples of the target style. Existing style transfer methods generally rely on the few-shot capabilities of large language models or on complex controllable text generation approaches that are inefficient and underperform on fluency metrics. We introduce TINYSTYLER, a lightweight but effective approach, which leverages a small language model (800M params) and pre-trained authorship embeddings to perform efficient, few-shot text style transfer. We evaluate on the challenging task of authorship style transfer and find TINYSTYLER outperforms strong approaches such as GPT-4. We also evaluate TINYSTYLER's ability to perform text attribute style transfer (formal ↔ informal) with automatic and human evaluations and find that the approach outperforms recent controllable text generation methods. Our model has been made publicly available here. © 2024 Association for Computational Linguistics.

---

# Cognitively Diverse Multiple-Choice Question Generation: A Hybrid Multi-Agent Framework with Large Language Models

DOI: 10.3390/electronics15061209
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #139

Recent advances in large language models (LLMs) have made automated multiple-choice question (MCQ) generation increasingly feasible; however, reliably producing items that satisfy controlled cognitive demands remains a challenge. To address this gap, we introduce ReQUESTA, a hybrid, multi-agent framework for generating cognitively diverse MCQs that systematically target text-based, inferential, and main idea comprehension. ReQUESTA decomposes MCQ authoring into specialized subtasks and coordinates LLM-powered agents with rule-based components to support planning, controlled generation, iterative evaluation, and post-processing. We evaluated the framework in a large-scale reading comprehension study using academic expository texts, comparing ReQUESTA-generated MCQs with those produced by a single-pass GPT-5 zero-shot baseline. Psychometric analyses of learner responses assessed item difficulty and discrimination, while expert raters evaluated question quality across multiple dimensions, including topic relevance and distractor quality. Results showed that ReQUESTA-generated items were consistently more challenging, more discriminative, and more strongly aligned with overall reading comprehension performance. Expert evaluations further indicated stronger alignment with central concepts and superior distractor linguistic consistency and semantic plausibility, particularly for inferential questions. These findings demonstrate that hybrid, agentic orchestration can systematically improve the reliability and controllability of LLM-based generation, highlighting workflow design as a key lever for structured artifact generation beyond single-pass prompting. © 2026 by the authors.

---

# Dynamic Infilling Anchors for Format-Constrained Generation in Diffusion Large Language Models

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #156

Diffusion large language models (dLLMs) offer bidirectional attention and parallel generation, enabling them to exploit global context and naturally support format-constrained tasks like parseable JSON or reasoning templates. While straightforward fixed anchors can enforce such constraints, they often impose rigid spans, leading to truncated reasoning or redundant content. To overcome this, we propose Dynamic Infilling Anchors (DIA), a training-free method that dynamically estimates end-anchor positions to adjust generation length before iterative infilling. This flexible mechanism ensures structural correctness and semantic coherence, avoiding the inefficiencies of fixed-span methods. Experiments on reasoning benchmarks demonstrate that DIA substantially improves format compliance and answer accuracy, achieving significant zero-shot gains on GSM8K and MATH. These results establish DIA as a robust pathway toward reliable, structure-aware generation.

---

# You May Speak Freely: Improving the Fine-Grained Visual Recognition Capabilities of Multimodal Large Language Models with Answer Extraction

DOI: 10.1109/WACV61042.2026.00145
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #133

Despite the renewed interest in zero-shot visual classification due to the rise of Multimodal Large Language Models (MLLMs), the problem of evaluating free-form responses of auto-regressive models remains a persistent challenge. Most existing works focus on language-only tasks or don't consider Multiple Choice Questions (MCQs) beyond 5-way options, both of which are critical capabilities to solve tasks in Fine-Grained Visual Classification (FGVC) where choice counts are in the hundreds to thousands and the choices are highly related. Furthermore, in this highly multi-way MCQ setting it is not clear how to extend LLM choice extraction to retrieval-based problems, where computing probabilities over the choice set is computationally costly. In this work we investigate nlg2choice, a simple two-stage method which first asks the MLLM an open-ended question for the task with minimal constraints, then uses text-only constrained decoding to predict the most likely choice. In retrieval settings, we compute the probability of the constrained response taking that choice with an early stopping method to significantly improve throughput. Our results show improvement over a suite of seven fine-grained visual datasets when evaluating in terms of classification and retrieval, and show that this performance holds over the various ways that users of LLMs can implement tasks in natural language. © 2026 IEEE.

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

# Prompt-Based Length Controlled Generation with Multiple Control Types

DOI: 10.18653/v1/2024.findings-acl.63
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #130

Large language models (LLMs) have attracted great attention given their strong performance on a wide range of NLP tasks. In practice, users often expect generated texts to fall within a specific length range, making length controlled generation an important topic, especially for GPT-style models. Existing length control methods mostly focus on a simple control type of “equal to” a target length. Different from them, we propose a prompt-based method to achieve length controlled generation under different control types with high accuracy. In particular, we adopt reinforcement learning (RL) and sample filtering with the reward signal given by rule-based reward models, which enhances the length control ability of models by rewarding outputs that follow certain control instructions. In addition, we introduce a standard prompt extractor to parse arbitrary users' input into standard control instructions. Experiments show that our method significantly improves the accuracy of prompt-based length control on popular summarization datasets like CNNDM and NYT under multiple control types. Moreover, both the standard prompt extractor and RL-tuned model show strong generalization to unseen control prompt templates. © 2024 Association for Computational Linguistics.

---

# Cross-Lingual Stability of LLM Judges Under Controlled Generation: Evidence from Finno-Ugric Languages

DOI: 10.18653/v1/2026.mme-main.8
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #125

Cross-lingual evaluation of large language models (LLMs) typically conflates two sources of variance: genuine model performance differences and measurement instability. We investigate evaluation reliability by holding generation conditions constant while varying target language. Using synthetic customer-support dialogues generated with identical parameters across Estonian, Finnish, and Hungarian, we test whether automatic metrics and LLM-as-a-judge scoring produce stable model rankings across these morphologically rich, related Finno-Ugric languages. With a small set of Estonian native speaker annotations as a reference point, we find systematic ranking instabilities: surface-level metrics (lexical diversity, surface and semantic similarity) maintain cross-language stability, but pragmatic judgments (coherence, instruction-following) exhibit rank inversions and near-zero correlations. Because generation is controlled, these inconsistencies reflect how judge scoring behaves differently across languages rather than true model differences. This controlled design provides a diagnostic probe: evaluation methods that fail to maintain stability under identical generation conditions signal transfer failure before deployment. Our findings suggest that zero-shot judge transfer is unreliable for discourse-level assessment in morphologically rich languages, motivating language-specific calibration against targeted human baselines. We release our controlled generation protocol, synthetic data, and evaluation framework to enable replication across language families at https://github.com/isaac-chung/cross-lingual-stability-judges. © 2026 Association for Computational Linguistics.

---

# Controllable Generation of Dialogue Acts for Dialogue Systems via Few-Shot Response Generation and Ranking

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #207

Dialogue systems need to produce responses that realize multiple types of dialogue acts (DAs) with high semantic fidelity. In the past, natural language generators (NLGs) for dialogue were trained on large parallel corpora that map from a domain-specific DA and its semantic attributes to an output utterance. Recent work shows that pretrained language models (LLMs) offer new possibilities for controllable NLG using prompt-based learning. Here we develop a novel few-shot overgenerate-and-rank approach that achieves the controlled generation of DAs. We compare eight few-shot prompt styles that include a novel method of generating from textual pseudo-references using a textual style transfer approach. We develop six automatic ranking functions that identify outputs with both the correct DA and high semantic accuracy at generation time. We test our approach on three domains and four LLMs. To our knowledge, this is the first work on NLG for dialogue that automatically ranks outputs using both DA and attribute accuracy. For completeness, we compare our results to fine-tuned few-shot models trained with 5 to 100 instances per DA. Our results show that several prompt settings achieve perfect DA accuracy, and near perfect semantic accuracy (99.81%) and perform better than few-shot fine-tuning.

---

# LLM-Supported Natural Language to Bash Translation

DOI: 10.18653/v1/2025.naacl-long.555
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #140

The Bourne-Again Shell (Bash) command-line interface for Linux systems has complex syntax and requires extensive specialized knowledge. Using the natural language to Bash command (NL2SH) translation capabilities of large language models (LLMs) for command composition circumvents these issues. However, the NL2SH performance of LLMs is difficult to assess due to inaccurate test data and unreliable heuristics for determining the functional equivalence of Bash commands. We present a manually verified test dataset of 600 instruction-command pairs and a training dataset of 40,939 pairs, increasing the size of previous datasets by 441% and 135%, respectively. Further, we present a novel functional equivalence heuristic that combines command execution with LLM evaluation of command outputs. Our heuristic can determine the functional equivalence of two Bash commands with 95% confidence, a 16% increase over previous heuristics. Evaluation of popular LLMs using our test dataset and heuristic demonstrates that parsing, in-context learning, in-weight learning and constrained decoding can improve NL2SH accuracy by up to 32%. Our findings emphasize the importance of dataset quality, execution-based evaluation and translation method for advancing NL2SH translation. Our code is available at https://github.com/westenfelder/NL2SH. © 2025 Association for Computational Linguistics.

---

# Reliable Answers for Recurring Questions: Boosting Text-to-SQL Accuracy with Template Constrained Decoding

DOI: 10.1145/3769822
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #32

Large language models (LLMs) have revolutionized Text-to-SQL generation, allowing users to query structured data using natural language with growing ease. Yet, real-world deployment remains challenging, especially in complex or unseen schemas, due to inconsistent accuracy and the risk of generating invalid SQL. We introduce Template Constrained Decoding (TeCoD), a system that addresses these limitations by harnessing the recurrence of query patterns in labeled workloads. TeCoD converts historical NL-SQL pairs into reusable templates and introduces a robust template selection module that uses a fine-tuned natural language inference model to match or reject queries efficiently. Once the template is selected, TeCoD enforces it during SQL generation through grammar-constrained decoding, implemented via a novel partitioned strategy that ensures both syntactic validity and efficiency. Together, these components yield up to 36% higher execution accuracy than in-context learning (ICL) and 2.2x lower latency on matched queries.

---

# To be or not to be? an exploration of continuously controllable prompt engineering

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #181

As the use of large language models becomes more widespread, techniques like parameter-efficient fine-tuning and other methods for controlled generation are gaining traction for customizing models and managing their outputs. However, the challenge of precisely controlling how prompts influence these models is an area ripe for further investigation. In response, we introduce ControlPE (Continuously Controllable Prompt Engineering). ControlPE enables finer adjustments to prompt effects, complementing existing prompt engineering, and effectively controls continuous targets. This approach harnesses the power of LoRA (Low-Rank Adaptation) to create an effect akin to prompt weighting, enabling fine-tuned adjustments to the impact of prompts. Our methodology involves generating specialized datasets for prompt distillation, incorporating these prompts into the LoRA model, and carefully adjusting LoRA merging weight to regulate the influence of prompts. This provides a dynamic and adaptable tool for prompt control. Through our experiments, we have validated the practicality and efficacy of ControlPE. It proves to be a promising solution for control a variety of prompts, ranging from generating short responses prompts, refusal prompts to chain-of-thought prompts.

---

# The Silent Vote: Improving Zero-Shot LLM Reliability by Aggregating Semantic Neighborhoods

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #214

Large Language Models are increasingly used as zero-shot classifiers in complex reasoning tasks. However, standard constrained decoding suffers from a phenomenon we define as Renormalization Bias. When a model is restricted to a small set of target labels, the standard softmax operation discards the probability mass assigned to semantic synonyms in the original distribution. This loss of information, which we call the Silent Vote, results in artificial overconfidence and poor calibration. We propose Semantic Softmax, an inference-time layer that recovers this lost information by aggregating the scores of the semantic neighborhood surrounding each target label. We evaluate this approach on Qwen-3 and Phi-4-mini models using GoEmotions and Civil Comments datasets. Our results demonstrate consistent improvements across all evaluation metrics: Semantic Softmax substantially reduces Expected Calibration Error (ECE) and Brier Score, while simultaneously enhancing discriminative performance in terms of AUROC and Macro-F1. By accounting for linguistic nuances, our method provides a more calibrated and accurate alternative for zero-shot classification.

---

# LLM Braces: Straightening Out LLM Predictions with Relevant Sub-Updates

DOI: 10.18653/v1/2025.acl-long.393
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #100

Recent findings reveal that much of the knowledge in a Transformer-based Large Language Model (LLM) is encoded in its feed-forward (FFN) layers, where each FFN layer can be interpreted as the summation of sub-updates, each corresponding to a weighted column vector from the FFN's value parameter matrix that often encodes human-interpretable concepts. In light of this, we hypothesize that model performance and behaviors can be further enhanced and controlled by modulating the contributions of these sub-updates based on their relevance to the input or target output style, and propose LLMBRACES, a novel and efficient method that computes relevance scores associated with value vectors in FFN layers and leverages these scores to dynamically adjust the contribution of sub-updates. By optimizing sub-update contributions, LLMBRACES refines the prediction process, leading to more accurate and reliable outputs, much like a 'brace' providing support and stability. Moreover, LLMBRACES can be extended to support conditional control over generation characteristics, such as sentiment, thereby offering fine-grained steering of LLM outputs. Extensive experiments on various LLMs'including Qwen2.5-1.5B, Llama2-7B, and Llama3-8B'demonstrate that LLMBRACES outperforms baseline approaches in both fine-tuning and zero-shot settings while requiring significantly fewer tunable parameters, up to 75% fewer compared to LoRA. Furthermore, LLMBRACES excels in sentiment-controlled generation and toxicity reduction, highlighting its potential for flexible, controlled text generation across applications. © 2025 Association for Computational Linguistics.

---

# STOC-TOT: Stochastic Tree-of-Thought with Constrained Decoding for Complex Reasoning in Multi-Hop Question Answering

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #177

Multi-hop question answering (MHQA) requires a model to retrieve and integrate information from multiple passages to answer a complex question. Recent systems leverage the power of large language models and integrate evidence retrieval with reasoning prompts (e.g., chain-of-thought reasoning) for the MHQA task. However, the complexities in the question types (bridge v.s. comparison questions) and the reasoning types (sequential v.s. parallel reasonings) require more novel and fine-grained prompting methods to enhance the performance of MHQA under the zero-shot setting. In this paper, we propose STOC-TOT, a stochastic tree-of-thought reasoning prompting method with constrained decoding for MHQA and conduct a detailed comparison with other reasoning prompts on different question types and reasoning types. Specifically, we construct a tree-like reasoning structure by prompting the model to break down the original question into smaller sub-questions to form different reasoning paths. In addition, we prompt the model to provide a probability estimation for each reasoning path at each reasoning step. At answer time, we conduct constrained decoding on the model to generate more grounded answers and reduce hallucination. Experiments comparing STOC-TOT with two MHQA datasets and five large language models showed that our framework outperforms other reasoning prompts by a significant margin.

---

# LLM as a Neural Architect: Controlled Generation of Image Captioning Models Under Strict API Contracts

DOI: 10.20944/preprints202512.0778.v1
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #235

Neural architecture search (NAS) traditionally requires significant human expertise or automated trial-and-error to design deep learning models. We present NN-Caption, an LLM-guided neural architecture search pipeline that generates runnable image-captioning models by composing CNN encoders from LEMUR’s classification backbones with sequence decoders (LSTM/GRU/Transformer) under a strict Net API [1,2]. Using DeepSeek-R1-0528-Qwen3-8B as the primary generator [3], we present the prompt template and examples of generated architectures. We evaluate on MS COCO with BLEU-4 [4,5]. The LLM generated dozens of captioning models, with over half successfully trained and producing meaningful captions. We analyse the outcomes of using different numbers of input model snippets (5 vs. 10) in the prompt, finding a slight drop in success rate when providing more candidate components. We also report training dynamics (caption accuracy vs. epochs) and the highest BLEU-4 attained. Our results highlight the promise of LLM-guided NAS: the LLM not only proposes architectures but also suggests hyperparameters and training practices. We identify the challenges encountered (e.g., code hallucinations or API compliance issues) and detail how prompt rules and iterative code fixes addressed them. This work presents a pipeline that integrates prompt-based code generation with automatic evaluation, and adds dozens of novel captioning models to the open LEMUR dataset to facilitate reproducible benchmarking and downstream AutoML research.

---

# TubeMLLM: A Foundation Model for Topology Knowledge Exploration in Vessel-like Anatomy

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #234

Modeling medical vessel-like anatomy is challenging due to its intricate topology and sensitivity to dataset shifts. Consequently, task-specific models often suffer from topological inconsistencies, including artificial disconnections and spurious merges. Motivated by the promise of multimodal large language models (MLLMs) for zero-shot generalization, we propose TubeMLLM, a unified foundation model that couples structured understanding with controllable generation for medical vessel-like anatomy. By integrating topological priors through explicit natural language prompting and aligning them with visual representations in a shared-attention architecture, TubeMLLM significantly enhances topology-aware perception. Furthermore, we construct TubeMData, a pionner multimodal benchmark comprising comprehensive topology-centric tasks, and introduce an adaptive loss weighting strategy to emphasize topology-critical regions during training. Extensive experiments on fifteen diverse datasets demonstrate our superiority. Quantitatively, TubeMLLM achieves state-of-the-art out-of-distribution performance, substantially reducing global topological discrepancies on color fundus photography (decreasing the $β_{0}$ number error from 37.42 to 8.58 compared to baselines). Notably, TubeMLLM exhibits exceptional zero-shot cross-modality transferring ability on unseen X-ray angiography, achieving a Dice score of 67.50% while significantly reducing the $β_{0}$ error to 1.21. TubeMLLM also maintains robustness against degradations such as blur, noise, and low resolution. Furthermore, in topology-aware understanding tasks, the model achieves 97.38% accuracy in evaluating mask topological quality, significantly outperforming standard vision-language baselines.

---

# Measuring and Mitigating Constraint Violations of In-Context Learning for Utterance-to-API Semantic Parsing

DOI: 10.18653/v1/2023.findings-emnlp.478
Ano: 2023
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #94

In executable task-oriented semantic parsing, the system aims to translate users' utterances in natural language to machine-interpretable programs (API calls) that can be executed according to pre-defined API specifications. With the popularity of Large Language Models (LLMs), in-context learning offers a strong baseline for such scenarios, especially in data-limited regimes (Hu et al., 2022; Shin et al., 2021). However, LLMs are known to hallucinate and therefore pose a formidable challenge in constraining generated content (Parikh et al., 2020). Thus, it remains uncertain if LLMs can effectively perform task-oriented utterance-to-API generation where respecting API's structural and task-specific constraints is crucial. In this work, we seek to measure, analyze and mitigate such constraints violations. First, we identify the categories of various constraints in obtaining API-semantics from task-oriented utterances, and define fine-grained metrics that complement traditional ones. Second, we leverage these metrics to conduct a detailed error analysis of constraints violations seen in state-of-the-art LLMs, which motivates us to investigate two popular mitigation strategies- Semantic-Retrieval of Demonstrations (SRD) and API-aware Constrained Decoding (API-CD). Our experiments show that these strategies are effective at reducing constraints violations and improving the quality of the generated API calls, but require careful consideration given their implementation complexity and latency. © 2023 Association for Computational Linguistics.

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

# Discrete Prompt Optimization via Constrained Generation for Zero-shot Re-ranker

DOI: 10.18653/v1/2023.findings-acl.61
Ano: 2023
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #141

Re-rankers, which order retrieved documents with respect to the relevance score on the given query, have gained attention for the information retrieval (IR) task. Rather than fine-tuning the pre-trained language model (PLM), the large-scale language model (LLM) is utilized as a zero-shot re-ranker with excellent results. While LLM is highly dependent on the prompts, the impact and the optimization of the prompts for the zero-shot re-ranker are not explored yet. Along with highlighting the impact of optimization on the zero-shot re-ranker, we propose a novel discrete prompt optimization method, Constrained Prompt generation (Co-Prompt), with the metric estimating the optimum for re-ranking. Co-Prompt guides the generated texts from PLM toward optimal prompts based on the metric without parameter update. The experimental results demonstrate that Co-Prompt leads to outstanding re-ranking performance against the baselines. Also, Co-Prompt generates more interpretable prompts for humans against other prompt optimization methods. © 2023 Association for Computational Linguistics.

---

# Controlled Text Generation with Natural Language Instructions

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #232

Large language models generate fluent texts and can follow natural language instructions to solve a wide range of tasks without task-specific training. Nevertheless, it is notoriously difficult to control their generation to satisfy the various constraints required by different applications. In this work, we present InstructCTG, a controlled text generation framework that incorporates different constraints by conditioning on natural language descriptions and demonstrations of the constraints. In particular, we first extract the underlying constraints of natural texts through a combination of off-the-shelf NLP tools and simple heuristics. We then verbalize the constraints into natural language instructions to form weakly supervised training data. By prepending natural language descriptions of the constraints and a few demonstrations, we fine-tune a pre-trained language model to incorporate various types of constraints. Compared to existing search-based or score-based methods, InstructCTG is more flexible to different constraint types and has a much smaller impact on the generation quality and speed because it does not modify the decoding procedure. Additionally, InstructCTG allows the model to adapt to new constraints without re-training through the use of few-shot task generalization and in-context learning abilities of instruction-tuned language models.

---

# SALP-CG: Standard-Aligned LLM Pipeline for Classifying and Grading Large Volumes of Online Conversational Health Data

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #218

Online medical consultations generate large volumes of conversational health data that often embed protected health information, requiring robust methods to classify data categories and assign risk levels in line with policies and practice. However, existing approaches lack unified standards and reliable automated methods to fulfill sensitivity classification for such conversational health data. This study presents a large language model-based extraction pipeline, SALP-CG, for classifying and grading privacy risks in online conversational health data. We concluded health-data classification and grading rules in accordance with GB/T 39725-2020. Combining few-shot guidance, JSON Schema constrained decoding, and deterministic high-risk rules, the backend-agnostic extraction pipeline achieves strong category compliance and reliable sensitivity across diverse LLMs. On the MedDialog-CN benchmark, models yields robust entity counts, high schema compliance, and accurate sensitivity grading, while the strongest model attains micro-F1=0.900 for maximum-level prediction. The category landscape stratified by sensitivity shows that Level 2-3 items dominate, enabling re-identification when combined; Level 4-5 items are less frequent but carry outsize harm. SALP-CG reliably helps classify categories and grading sensitivity in online conversational health data across LLMs, offering a practical method for health data governance. Code is available at https://github.com/dommii1218/SALP-CG.

---

# Constrained Decoding for Cross-lingual Label Projection

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #217

Zero-shot cross-lingual transfer utilizing multilingual LLMs has become a popular learning paradigm for low-resource languages with no labeled training data. However, for NLP tasks that involve fine-grained predictions on words and phrases, the performance of zero-shot cross-lingual transfer learning lags far behind supervised fine-tuning methods. Therefore, it is common to exploit translation and label projection to further improve the performance by (1) translating training data that is available in a high-resource language (e.g., English) together with the gold labels into low-resource languages, and/or (2) translating test data in low-resource languages to a high-source language to run inference on, then projecting the predicted span-level labels back onto the original test data. However, state-of-the-art marker-based label projection methods suffer from translation quality degradation due to the extra label markers injected in the input to the translation model. In this work, we explore a new direction that leverages constrained decoding for label projection to overcome the aforementioned issues. Our new method not only can preserve the quality of translated texts but also has the versatility of being applicable to both translating training and translating test data strategies. This versatility is crucial as our experiments reveal that translating test data can lead to a considerable boost in performance compared to translating only training data. We evaluate on two cross-lingual transfer tasks, namely Named Entity Recognition and Event Argument Extraction, spanning 20 languages. The results demonstrate that our approach outperforms the state-of-the-art marker-based method by a large margin and also shows better performance than other label projection methods that rely on external word alignment.

---

# Plug and Play with Prompts: A Prompt Tuning Approach for Controlling Text Generation

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #225

Transformer-based Large Language Models (LLMs) have shown exceptional language generation capabilities in response to text-based prompts. However, controlling the direction of generation via textual prompts has been challenging, especially with smaller models. In this work, we explore the use of Prompt Tuning to achieve controlled language generation. Generated text is steered using prompt embeddings, which are trained using a small language model, used as a discriminator. Moreover, we demonstrate that these prompt embeddings can be trained with a very small dataset, with as low as a few hundred training examples. Our method thus offers a data and parameter efficient solution towards controlling language model outputs. We carry out extensive evaluation on four datasets: SST-5 and Yelp (sentiment analysis), GYAFC (formality) and JIGSAW (toxic language). Finally, we demonstrate the efficacy of our method towards mitigating harmful, toxic, and biased text generated by language models.

---

# VQA-Diff: Exploiting VQA and Diffusion for Zero-Shot Image-to-3D Vehicle Asset Generation in Autonomous Driving

DOI: 10.1007/978-3-031-72848-8_19
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #118

Generating 3D vehicle assets from in-the-wild observations is crucial to autonomous driving. Existing image-to-3D methods cannot well address this problem because they learn generation merely from image RGB information without a deeper understanding of in-the-wild vehicles (such as car models, manufacturers, etc.). This leads to their poor zero-shot prediction capability to handle real-world observations with occlusion or tricky viewing angles. To solve this problem, in this work, we propose VQA-Diff, a novel framework that leverages in-the-wild vehicle images to create photorealistic 3D vehicle assets for autonomous driving. VQA-Diff exploits the real-world knowledge inherited from the Large Language Model in the Visual Question Answering (VQA) model for robust zero-shot prediction and the rich image prior knowledge in the Diffusion model for structure and appearance generation. In particular, we utilize a multi-expert Diffusion Models strategy to generate the structure information and employ a subject-driven structure-controlled generation mechanism to model appearance information. As a result, without the necessity to learn from a large-scale image-to-3D vehicle dataset collected from the real world, VQA-Diff still has a robust zero-shot image-to-novel-view generation ability. We conduct experiments on various datasets, including Pascal 3D+, Waymo, and Objaverse, to demonstrate that VQA-Diff outperforms existing state-of-the-art methods both qualitatively and quantitatively. © The Author(s), under exclusive license to Springer Nature Switzerland AG 2025.

---

# Explainable ICD Coding via Entity Linking

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #204

Clinical coding is a critical task in healthcare, although traditional methods for automating clinical coding may not provide sufficient explicit evidence for coders in production environments. This evidence is crucial, as medical coders have to make sure there exists at least one explicit passage in the input health record that justifies the attribution of a code. We therefore propose to reframe the task as an entity linking problem, in which each document is annotated with its set of codes and respective textual evidence, enabling better human-machine collaboration. By leveraging parameter-efficient fine-tuning of Large Language Models (LLMs), together with constrained decoding, we introduce three approaches to solve this problem that prove effective at disambiguating clinical mentions and that perform well in few-shot scenarios.

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

# Training Naturalized Semantic Parsers with Very Little Data

DOI: 10.24963/ijcai.2022/604
Ano: 2022
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #105

Semantic parsing is an important NLP problem, particularly for voice assistants such as Alexa and Google Assistant. State-of-the-art (SOTA) semantic parsers are seq2seq architectures based on large language models that have been pretrained on vast amounts of text. To better leverage that pretraining, recent work has explored a reformulation of semantic parsing whereby the output sequences are themselves natural language sentences, but in a controlled fragment of natural language. This approach delivers strong results, particularly for few-shot semantic parsing, which is of key importance in practice and the focus of our paper. We push this line of work forward by introducing an automated methodology that delivers very significant additional improvements by utilizing modest amounts of unannotated data, which is typically easy to obtain. Our method is based on a novel synthesis of four techniques: joint training with auxiliary unsupervised tasks; constrained decoding; self-training; and paraphrasing. We show that this method delivers new SOTA few-shot performance on the Overnight dataset, particularly in very low-resource settings, and very compelling few-shot results on a new semantic parsing dataset. © 2022 International Joint Conferences on Artificial Intelligence. All rights reserved.

---

# TimeMaster: Training Time-Series Multimodal LLMs to Reason via Reinforcement Learning

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #251

Time-series reasoning remains a significant challenge in multimodal large language models (MLLMs) due to the dynamic temporal patterns, ambiguous semantics, and lack of temporal priors. In this work, we introduce TimeMaster, a reinforcement learning (RL)-based method that enables time-series MLLMs to perform structured, interpretable reasoning directly over visualized time-series inputs and task prompts. TimeMaster adopts a three-part structured output format, reasoning, classification, and domain-specific extension, and is optimized via a composite reward function that aligns format adherence, prediction accuracy, and open-ended insight quality. The model is trained using a two-stage pipeline: we first apply supervised fine-tuning (SFT) to establish a good initialization, followed by Group Relative Policy Optimization (GRPO) at the token level to enable stable and targeted reward-driven improvement in time-series reasoning. We evaluate TimeMaster on the TimerBed benchmark across six real-world classification tasks based on Qwen2.5-VL-3B-Instruct. TimeMaster achieves state-of-the-art performance, outperforming both classical time-series models and few-shot GPT-4o by over 14.6% and 7.3% performance gain, respectively. Notably, TimeMaster goes beyond time-series classification: it also exhibits expert-like reasoning behavior, generates context-aware explanations, and delivers domain-aligned insights. Our results highlight that reward-driven RL can be a scalable and promising path toward integrating temporal understanding into time-series MLLMs.

---

# FABRIC: Framework for Agent-Based Realistic Intelligence Creation

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #216

Large language models (LLMs) are increasingly deployed as agents, expected to decompose goals, invoke tools, and verify results in dynamic environments. Realizing these capabilities requires access to agentic data-structured interaction records that couple user intents with tool specifications, argument-grounded calls, and verifiable execution traces. However, collecting such data from human annotators is costly, time-consuming, and difficult to scale. We present a unified framework for synthesizing agentic data using only LLMs, without any human-in-the-loop supervision. This framework decomposes generation into modular pipelines that produce complete interaction records spanning task specifications, tool definitions, policy pseudocode, natural language exchanges, and execution traces. Records conform to strict syntactic and semantic constraints, ensuring machine-parseability and faithful alignment across inputs, outputs, and tool calls. Beyond single tasks, there is support for both multi-task and multi-turn agent interactions, enabling the construction of datasets that reflect the full spectrum of tool-use competencies. To ensure quality and consistency, the framework integrates constrained generation formats, JSON-schema validation, and judge-based filtering. This paper formalizes the schema for agentic records, details the prompt design principles that guide generation, and introduces scalable pipelines for high-quality synthetic data. By providing a reproducible, LLM-only alternative to manual collection, hence advancing the development of agentic LLMs capable of robust tool use.

---

# On Improving Summarization Factual Consistency from Natural Language Feedback

DOI: 10.18653/v1/2023.acl-long.844
Ano: 2023
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #136

Despite the recent progress in language generation models, their outputs may not always meet user expectations. In this work, we study whether informational feedback in natural language can be leveraged to improve generation quality and user preference alignment. To this end, we consider factual consistency in summarization, the quality that the summary should only contain information supported by the input documents, as the user-expected preference. We collect a high-quality dataset, DeFacto, containing human demonstrations and informational natural language feedback consisting of corrective instructions, edited summaries, and explanations with respect to the factual consistency of the summary. Using our dataset, we study three natural language generation tasks: (1) editing a summary by following the human feedback, (2) generating human feedback for editing the original summary, and (3) revising the initial summary to correct factual errors by generating both the human feedback and edited summary. We show that DeFacto can provide factually consistent human-edited summaries and further insights into summarization factual consistency thanks to its informational natural language feedback. We further demonstrate that fine-tuned language models can leverage our dataset to improve the summary factual consistency, while large language models lack the zero-shot learning ability in our proposed tasks that require controllable text generation. © 2023 Association for Computational Linguistics.

---

# STaR-DRO: Stateful Tsallis Reweighting for Group-Robust Structured Prediction

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #180

Structured prediction with large language models requires outputs that are label-accurate, ontology-constrained, structurally valid, and evidence-grounded under label imbalance and heterogeneous group difficulty. We present a unified framework for ontology-constrained generation. First, we introduce a modular prompt-engineering architecture combining XML-style structure, expert disambiguation rules, chain-of-thought reasoning, metadata-aware decision logic, schema contracts, and a self-validation gate. It targets recurrent in-context failures, including format drift, label ambiguity, evidence hallucination, and metadata-conditioned confusion. Second, we propose STaR-DRO, combining Tsallis mirror ascent, sparse entmax-style primal mapback, EMA-smoothed group-loss tracking, rescaled ascent signals, and bounded excess-only multipliers. Unlike conventional DRO, which relies on dense Shannon-entropy exponentiated-gradient updates, can introduce high-variance stochastic reweighting, assigns positive adversarial mass to groups that are not persistently hard, and incurs costs through simplex competition, STaR-DRO upweights only persistently hard groups without suppressing easier ones. We evaluate the framework on EPPC Miner, a clinically grounded high-stakes structured-prediction task requiring hierarchical label prediction and evidence-span extraction from patient-provider secure messages. Across 1B-70B Llama models, prompt engineering improves zero-shot extraction, yielding an average label F1 gain of +14.46 and a Span F1 gain of +17.40. Building on supervised fine-tuning, STaR-DRO further improves accuracy and robustness, increasing average label F1 by +1.08 and +2.20 while reducing mean groupwise validation cross-entropy by 21.3% and 14.8% relative to SFT and standard DRO, respectively. These results advance reliable automated communication mining for patient-centered clinical care analysis.

---

# Instruct-SCTG: Guiding Sequential Controlled Text Generation through Instructions

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #203

Instruction-tuned large language models have shown remarkable performance in aligning generated text with user intentions across various tasks. However, maintaining human-like discourse structure in the generated text remains a challenging research question. In this paper, we propose Instruct-SCTG, a flexible and effective sequential framework that harnesses instruction-tuned language models to generate structurally coherent text in both fine-tuned and zero-shot setups. Our framework generates articles in a section-by-section manner, aligned with the desired human structure using natural language instructions. Furthermore, we introduce a new automatic metric that measures discourse divergence in a fuzzy manner. Extensive experiments on three datasets from representative domains of news and recipes demonstrate the state-of-the-art performance of our framework in imposing discourse structure during text generation, as verified by both automatic and human evaluation. Our code will be available on Github.

---

# SCOPE:Planning for Hybrid Querying over Clinical Trial Data

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #185

We study clinical trial table reasoning, where answers are not directly stored in visible cells but must be reasoned from semantic understanding through normalization, classification, extraction, or lightweight domain reasoning. Motivated by the observation that current LLM approaches often suffer from "bad reasoning" under implicit planning assumptions, we focus on settings in which the model must recover implicit attributes such as therapy type, added agents, endpoint roles, or follow-up status from partially observed clinical-trial tables. We propose SCOPE (Structured Clinical hybrid Planning for Evidence retrieval in clinical trials), a multi-LLM planner-based framework that decomposes the task into row selection, structured planning, and execution. The planner makes the source field, reasoning rules, and output constraints explicit before answer generation, reducing ambiguity relative to direct prompting. We evaluate SCOPE on 1,500 hybrid reasoning questions over oncology clinical-trial tables against zero-shot, few-shot, chain-of-thought, TableGPT2, Blend-SQL, and EHRAgent. Results show that explicit multi-LLM planning improves accuracy for reasoning-based questions while offering a stronger accuracy-efficiency tradeoff than heavier agentic baselines. Our findings position clinical trial reasoning as a distinct table understanding problem and highlight hybrid planner-based decomposition as an effective solution

---

# Benchmarking Small Language Models and Small Reasoning Language Models on System Log Severity Classification

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #201

System logs are crucial for monitoring and diagnosing modern computing infrastructure, but their scale and complexity require reliable and efficient automated interpretation. Since severity levels are predefined metadata in system log messages, having a model merely classify them offers limited standalone practical value, revealing little about its underlying ability to interpret system logs. We argue that severity classification is more informative when treated as a benchmark for probing runtime log comprehension rather than as an end task. Using real-world journalctl data from Linux production servers, we evaluate nine small language models (SLMs) and small reasoning language models (SRLMs) under zero-shot, few-shot, and retrieval-augmented generation (RAG) prompting. The results reveal strong stratification. Qwen3-4B achieves the highest accuracy at 95.64% with RAG, while Gemma3-1B improves from 20.25% under few-shot prompting to 85.28% with RAG. Notably, the tiny Qwen3-0.6B reaches 88.12% accuracy despite weak performance without retrieval. In contrast, several SRLMs, including Qwen3-1.7B and DeepSeek-R1-Distill-Qwen-1.5B, degrade substantially when paired with RAG. Efficiency measurements further separate models: most Gemma and Llama variants complete inference in under 1.2 seconds per log, whereas Phi-4-Mini-Reasoning exceeds 228 seconds per log while achieving &lt;10% accuracy. These findings suggest that (1) architectural design, (2) training objectives, and (3) the ability to integrate retrieved context under strict output constraints jointly determine performance. By emphasizing small, deployable models, this benchmark aligns with real-time requirements of digital twin (DT) systems and shows that severity classification serves as a lens for evaluating model competence and real-time deployability, with implications for root cause analysis (RCA) and broader DT integration.

---

# Cross-Lingual Transfer for Low-Resource Natural Language Processing

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #173

Natural Language Processing (NLP) has seen remarkable advances in recent years, particularly with the emergence of Large Language Models that have achieved unprecedented performance across many tasks. However, these developments have mainly benefited a small number of high-resource languages such as English. The majority of languages still face significant challenges due to the scarcity of training data and computational resources. To address this issue, this thesis focuses on cross-lingual transfer learning, a research area aimed at leveraging data and models from high-resource languages to improve NLP performance for low-resource languages. Specifically, we focus on Sequence Labeling tasks such as Named Entity Recognition, Opinion Target Extraction, and Argument Mining. The research is structured around three main objectives: (1) advancing data-based cross-lingual transfer learning methods through improved translation and annotation projection techniques, (2) developing enhanced model-based transfer learning approaches utilizing state-of-the-art multilingual models, and (3) applying these methods to real-world problems while creating open-source resources that facilitate future research in low-resource NLP. More specifically, this thesis presents a new method to improve data-based transfer with T-Projection, a state-of-the-art annotation projection method that leverages text-to-text multilingual models and machine translation systems. T-Projection significantly outperforms previous annotation projection methods by a wide margin. For model-based transfer, we introduce a constrained decoding algorithm that enhances cross-lingual Sequence Labeling in zero-shot settings using text-to-text models. Finally, we develop Medical mT5, the first multilingual text-to-text medical model, demonstrating the practical impact of our research on real-world applications.

---

# PIPE-Cypher: Automatic Enterprise Benchmark Generation for Text-to-Cypher Systems

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #189

Enterprise property graphs vary widely in schema structure, internal terminology, domain assumptions, governance constraints, and user interaction patterns. A deployment-relevant Text2Cypher benchmark therefore reflects the questions users and agents actually ask of that graph. Creating such a benchmark is difficult because schemas and values are unique, and graph structure changes over time. Each NL-query pair must also be executable, use real graph entities, preserve diversity, and remain balanced across query types and difficulty levels. We present PIPE-Cypher, a local benchmark-generation pipeline that turns a live property graph and optional seed queries from customer questions, analyst logs, or agent tool calls into balanced NL-to-Cypher benchmarks. PIPE-Cypher combines schema profiling, reverse-query grounding, constrained generation, deterministic Cypher governance, execution validation, redaction, diversity controls, and a calibrated local LLM judge. Using local Qwen3.5-9B generation and judging, PIPE-Cypher exports 3,000 accepted FinBench/SNB examples, completes three audited ablation suites, calibrates judge behavior with human labels, and evaluates 11 local downstream models. The resulting benchmark is deliberately discriminative: zero-shot transfer is weak, while a few-shot control shows that schema-specific example banks can help compatible model families. Together, PIPE-Cypher makes Text2Cypher benchmarking a repeatable process that evolves with the graph, its users, and its target workloads.

---

# Graph Grounded Cross Attention Transformer Neural Network for Structurally Constrained Full Event Sequence Generation in Predictive Process Monitoring

DOI: 10.2139/ssrn.6990079
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #184

Structurally constrained event sequence generation remains challenging because generated paths must preserve transition feasibility, temporal order, termination, and attribute consistency. In predictive process monitoring (PPM), this challenge appears as full event sequence generation, whereas existing work mainly addresses component tasks such as next activity, remaining time, outcome, and attribute prediction. This paper proposes the Graph Grounded Cross Attention Transformer Neural Network (GGATN) for this unified PPM task. GGATN uses a global process graph as structured activity memory, contextualizes sequence positions through Transformer self attention, and injects process topology through graph grounded cross attention. Unlike autoregressive decoding, GGATN generates activities, timestamps, length, and event level and sequence level attributes in a single pass, followed by Viterbi style graph constrained decoding for feasible paths and explicit termination. Experiments on six benchmark event logs show more reliable generation quality than local instruction prompted LLM baselines. GGATN achieves strong performance on sequence similarity, Damerau Levenshtein similarity, bigram based control flow similarity, and duration distribution, while maintaining zero hallucinated activities and zero sequence level attribute inconsistency. Ablation analyses confirm the global graph encoder as a stable structural prior. Interpretability analyses show how graph structure, sequence context, feedback refinement, and constrained decoding shape generation.

---

# RealGen: Retrieval Augmented Generation for Controllable Traffic Scenarios

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #208

Simulation plays a crucial role in the development of autonomous vehicles (AVs) due to the potential risks associated with real-world testing. Although significant progress has been made in the visual aspects of simulators, generating complex behavior among agents remains a formidable challenge. It is not only imperative to ensure realism in the scenarios generated but also essential to incorporate preferences and conditions to facilitate controllable generation for AV training and evaluation. Traditional methods, mainly relying on memorizing the distribution of training datasets, often fall short in generating unseen scenarios. Inspired by the success of retrieval augmented generation in large language models, we present RealGen, a novel retrieval-based in-context learning framework for traffic scenario generation. RealGen synthesizes new scenarios by combining behaviors from multiple retrieved examples in a gradient-free way, which may originate from templates or tagged scenarios. This in-context learning framework endows versatile generative capabilities, including the ability to edit scenarios, compose various behaviors, and produce critical scenarios. Evaluations show that RealGen offers considerable flexibility and controllability, marking a new direction in the field of controllable traffic scenario generation. Check our project website for more information: https://realgen.github.io.

---

# Towards Highly-Constrained Human Motion Generation with Retrieval-Guided Diffusion Noise Optimization

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #240

Generating human motion that satisfies customized zero-shot goal functions, enabling applications such as controllable character animation and behavior synthesis for virtual agents, is a critical capability. While current approaches handle many unseen constraints, they fail on tasks with very challenging spatiotemporal restrictions, such as severe spatial obstacles or specified numbers of walking steps. To equip motion generators for these highly constrained tasks, we present a retrieval-guided method built on the training-free diffusion noise optimization framework. The key idea is to search within large motion datasets for guidance that can potentially satisfy difficult constraints. We introduce relational task parsing to group target constraints and identify the difficult ones to be handled by retrieved reference. A better initialization for diffusion noise is then obtained via a reward-guided mask that combines random noise with retrieved noise. By optimizing diffusion noise from this improved initialization, we successfully solve highly constrained generation tasks. By leveraging LLM for relational task parsing, the whole framework is further enabled to automatically reason for what to retrieve, improving the intelligence of moving agents under a training-free optimization scheme.

---

# Automated IEP Generation from Traditional Chinese Parent-Teacher Interviews via Corpus-Grounded Feature Diffusion

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #151

Writing Individualized Education Programs (IEPs) is a high-labor, knowledge-intensive document burden; English-language research has demonstrated that generative AI can significantly reduce drafting time, yet automated IEP generation in Traditional Chinese remains virtually unexplored due to domain data scarcity, strict privacy regulations, and the absence of local evaluation benchmarks. We propose a low-resource fine-tuning pipeline centered on Corpus-Grounded Feature Diffusion (CGFD): (1) 25 dual-expert high-score seed transcripts are selected via a tau threshold with flag-aware score caps; (2) a FeatureProfile (sentence length, structure, quantification templates) is extracted from seeds and injected into LLM prompts alongside Verbalized-Sampling-style diversity control to drive diffusion; (3) 15 expert gold seeds are used as diffusion anchors, targeting 585 samples; 567 valid diffusion samples are obtained, yielding a 582-sample training set used to fine-tune Breeze-7B with QLoRA; (4) schema-constrained inference via Grammar-Constrained Decoding (GCD) enforces a hierarchical SMART Goal Ladder schema at inference time. Ablation results on a 55-sample schema stress set reveal an unexpected finding: GCD is counterproductive under Traditional Chinese token budgets -- the no-GCD path achieves 100% schema pass rate at 34% lower median latency, outperforming GCD on both reliability and speed. On the n=10 formal hold-out, the no-GCD inference path achieves BERTScore F1 = 0.779, exceeding GPT-5.4 (0.726), DeepSeek-V3.2 (0.703), Gemini-3-Flash-Preview (0.703), and Llama-4-Maverick (0.700) zero-shot baselines while maintaining fully local, air-gapped inference. This system addresses a gap in Traditional Chinese special-education NLP and offers a scalable, privacy-preserving local inference solution under an industrial engineering paradigm.

---

# Task-Oriented Data Synthesis and Control-Rectify Sampling for Remote Sensing Semantic Segmentation

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #239

With the rapid progress of controllable generation, training data synthesis has become a promising way to expand labeled datasets and alleviate manual annotation in remote sensing (RS). However, the complexity of semantic mask control and the uncertainty of sampling quality often limit the utility of synthetic data in downstream semantic segmentation tasks. To address these challenges, we propose a task-oriented data synthesis framework (TODSynth), including a Multimodal Diffusion Transformer (MM-DiT) with unified triple attention and a plug-and-play sampling strategy guided by task feedback. Built upon the powerful DiT-based generative foundation model, we systematically evaluate different control schemes, showing that a text-image-mask joint attention scheme combined with full fine-tuning of the image and mask branches significantly enhances the effectiveness of RS semantic segmentation data synthesis, particularly in few-shot and complex-scene scenarios. Furthermore, we propose a control-rectify flow matching (CRFM) method, which dynamically adjusts sampling directions guided by semantic loss during the early high-plasticity stage, mitigating the instability of generated images and bridging the gap between synthetic data and downstream segmentation tasks. Extensive experiments demonstrate that our approach consistently outperforms state-of-the-art controllable generation methods, producing more stable and task-oriented synthetic data for RS semantic segmentation.

---

# Two Shots are Enough: Reliable Constrained Generation with LLMs

DOI: 10.1109/BigData66926.2025.11402199
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #79

Despite exhibiting impressive performance across many complex tasks, Large Language Models (LLMs) often struggle to consistently produce structured responses, a key element in many applications such as agent orchestration. While template-based methods or in-context learning can improve structure compliance, constrained decoding and additional context have been shown to skew the distribution of the responses and may result in suboptimal performance. In this work, we show that the number of in-context examples is a key factor: in many settings, one to two shots are sufficient to reliably produce the predefined structures, while additional examples may degrade the response quality. Our analysis shows that this phenomenon is consistent across a wide range of datasets, models, and structures and indicates that providing this small number of shots achieves the best overall trade-off between structure compliance and response correctness while improving the results of constrained generation methods such as template-based approaches.

---

# Tuning-Free Fidelity-Constrained Decoding for Faithful Legal Reasoning with Open-Domain Large Language Models

DOI: 10.1109/ICASSP55912.2026.11461418
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #80

Large language models (LLMs) are increasingly applied to legal tasks to assist judges and lawyers in decision-making, where outputs must remain faithful to case facts and legal elements to ensure reliable legal interpretations and accurate predictions. Existing approaches—ranging from prompt engineering to task-specific fine-tuning—either demand substantial human effort or lack explicit mechanisms to guarantee such fidelity. To address this issue, we propose Fidelity-Constrained Decoding (FCD), a tuning-free decoding framework that directly constrains generation to preserve strict alignment with both factual details and legal elements. Experiments on three legal datasets with two open-domain LLMs show that FCD consistently improves performance across diverse legal reasoning tasks while avoiding additional training overhead. Our code and datasets are available at https://github.com/ke-01/FCD.

---

# The Effectiveness of Style Vectors for Steering Large Language Models: A Human Evaluation

DOI: 10.1109/ACCESS.2025.3628500
Ano: 2025
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #129

Controlling the behavior of large language models (LLMs) at inference time is essential for aligning outputs with human abilities and safety requirements. Activation steering provides a lightweight alternative to prompt engineering and fine-tuning by directly modifying internal activations to guide generation. This research advances the literature in three significant directions. First, while previous work demonstrated the technical feasibility of steering emotional tone using automated classifiers, this paper presents the first human evaluation of activation steering concerning the emotional tone of LLM outputs, collecting over 7,000 crowd-sourced ratings from 190 participants via Prolific ( n =1 90 ). These ratings assess both perceived emotional intensity and overall text quality. Second, we find strong alignment between human and model-based quality ratings (mean r = 0.776 , range 0.157–0.985), indicating automatic scoring can proxy perceived quality. Moderate steering strengths ( λ ≈ 0.15 ) reliably amplify target emotions while preserving comprehensibility, with the strongest effects for disgust ( ηp2 = 0.616 ) and fear ( ηp2 = 0.540 ), and minimal effects for surprise ( ηp2 = 0.042 ). Finally, upgrading from Alpaca to LlaMA-3 yielded more consistent steering with significant effects across emotions and strengths (all p < 0.001 ). Inter-rater reliability was high (ICC = 0.71–0.87), underscoring the robustness of the findings. These findings support activation-based control as a scalable method for steering LLM behavior across affective dimensions. © 2013 IEEE.

---

# LDFS: LLMs with Dynamic Few-Shot for Offensive Language Detection

DOI: 10.1109/trustcom66490.2025.00358
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Lens.org
RRI: #209

The detection of offensive language in social media faces significant challenges due to its diverse and evolving expressions, making accurate identification remains critical for maintaining healthy online ecosystems. While few-shot learning with large language models (LLMs) has demonstrated potential in this domain, conventional static demonstration selection strategies often fail to adapt to the linguistic variability of offensive content, which ultimately limits model performance. To address this limitation, we propose LLMs with Dynamic Few-Shot (LDFS), a novel method that encodes the training set into dense vector representations, retrieves top-k nearest-neighbors for each sample, and constructs balanced demonstrations by strategically sampling from offensive and non-offensive classes. These demonstrations are integrated with the task description and output constraints to construct structured prompts that guide the LLMs to perform the classification. Comprehensive evaluations on the benchmark datasets COLDataset and CDial-Bias reveal that LDFS consistently outperforms conventional approaches. The method achieves superior performance compared to random 10-shot selection, with F1-score improvements reaching up to 14 percentage points. Notably, LDFS surpasses specialized fine-tuned models including COLDETECTOR by 6.82% and GLM2 P-Prompt by 17.47% in F1-score on the CDial-Bias dataset. These results demonstrate that dynamic, semantically-aware demonstration selection can effectively enhance the capability of LLMs to recognize offensive language across diverse contexts.

---

# Behavior Generation for Heterogeneous Agents in Urban Simulation Deduction: A Multi-Stage Approach Based on Large Language Models

DOI: 10.1109/IEEECONF65522.2025.11136878
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #83

Traditionally, constructing a professional simulation deduction script is a long-cycle process that requires collaboration between domain experts and simulation experts. The increasing demands for simulation deduction across large-scale scenarios and emergency situations highlight the need for rapid simulation scenario construction methods. Recent advances in large language models (LLMs) offer powerful new tools to address these challenges. In this work, we propose LLM-HABG, a highly portable framework that can automatically generate behavior plans for heterogeneous agents in urban simulation environments based on natural language instructions, requiring no additional post-training. It comprises four stages: task extraction, task decomposition and allocation, urban information retrieval, and behavior generation. To overcome the limitations of LLMs, such as deficient instruction-following and hallucinations, we incorporate a suite of enhancement techniques including dynamic few-shot learning, entity alignment, and constrained decoding. Experimental results demonstrate that LLM-HABG achieves robust performance even with 14B-parameter models, attaining a success rate exceeding 75 %-nearly doubling baseline performance. This conversational behavior configuration paradigm empowers domain experts to interact directly with simulation systems via natural language, significantly reducing the cost and barriers associated with simulation scenario construction.

---

# Advanced LLMs for Drug-Effect Relation Prediction: Accuracy, Hallucination Control, and Computational Efficiency

DOI: 10.1109/ACIT68900.2025.11510623
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #116

Large language models (LLMs) are rapidly transforming biomedical text mining, yet their reliability in extracting precise drug-effect relations remains uncertain. In this work, we take three state-of-the-art open-source models - Mistral, Qwen, and Gemma-beyond generic benchmarks and place them under a stress test that exposes the fine line between accuracy, structural discipline, and hallucination. We evaluate their ability to extract structured (drug, effect) pairs from real biomedical narratives, measuring task-specific F1 scores, semantic hallucination penalties, JSON compliance, and inference speed. The results reveal striking contrasts: Qwen excels in structured fidelity, Mistral achieves strong accuracy but at the cost of higher hallucination rates, and Gemma delivers stable outputs only under low-complexity scenarios. Ten indepth visual analyses uncover hidden trade-offs that influence deployment choices in high-stakes medical NLP. The study offers concrete strategies-prompt engineering, constrained decoding, and fine-tuning-to bridge the gap between LLM potential and clinical-grade reliability. © 2025 IEEE.

---

# LLM Transform: A Unified Pipeline for Semantic Rewriting of Sentences, Paragraphs, and Questions

DOI: 10.1109/CSITSS67709.2025.11295465
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #86

This paper presents a comprehensive framework for context-aware sentence reframing using large language models (LLMs), aimed at enhancing fluency, interpretability and semantic clarity in diverse textual domains. The proposed system integrates four core components: (1) sentence,question and paragraph-level reframing using a fine-tuned Pegasus model; (2) context-sensitive synonym replacement leveraging WordNet and SBERT similarity scoring; (3) verb identification through SpaCy-based syntactic parsing; and (4) idiom and multi-word expression extraction to preserve Subtle linguistic feature. In contrast to existing paraphrasing pipelines that prioritize the system implemented in Python, integrates various NLP libraries such as SpaCy, NLTK and Hugging Face Transformers. We Baseline our system across varied sentence types. Literature trends from 2019 to 2025 demonstrate a shift toward controllable text generation, cognitive reframing, and zero-shot generalization-all addressed by our architecture. This work contributes a modular, real-time Flask application that advances LLM-based sentence transformation with direct applications in enhancing lexical, syntactic, and idiomatic diversity, suitable for tasks like style transfer, simplification, and educational tools.

---

# FLAP: Faithful LLM-Aligned Prompting for NLP-Driven Abstractive Text Summarization via Saliency-Guided Encoding and Reinforcement-Based Faithfulness Optimization

DOI: 10.1109/GAIIS69281.2026.11519156
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #117

Abstractive text summarization is a core challenge in natural language processing (NLP), and deploying large language models (LLMs) in this setting exposes three critical limitations: (1) LLMs tend to ignore semantically central content due to unstructured input representations, leading to uninformative summaries; (2) standard fine-tuning objectives fail to align NLP generation pipelines with human preferences for factual fidelity, resulting in entity-level and relational hallucinations; and (3) existing decoding strategies impose no length or faithfulness constraints, producing verbose or factually inconsistent outputs. To address these shortcomings, we propose FLAP (Faithful LLM-Aligned Prompting), a two-stage NLP framework that integrates (1) a saliency-guided Semantic Prompt Encoder that selects and re-weights semantically central sentences via a primacy-recency positional bias, (2) a composite reward model combining lexical, semantic faithfulness, and conciseness signals to drive Group Relative Policy Optimization (GRPO) for human-aligned NLP generation, and (3) a constrained decoding strategy that jointly enforces target length and entailment-based faithfulness at inference time. Extensive experiments on CNN/DailyMail, XSum, and Reddit across LLM backbone scales from 7B to 70B demonstrate that FLAP consistently outperforms strong NLP baselines in ROUGE, BERTScore, BARTScore, and human evaluation, while reducing hallucination rates by up to 25.1 percentage points. © 2026 IEEE.

---

# Knowledge graph-enhanced large language models for explainable causal analysis of crane accidents

DOI: 10.1016/j.ress.2026.112859
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #259

Crane accidents are characterized by high suddenness, chain-like evolution, and strongly coupled causal factors. Traditional experience-driven approaches are insufficient for reliable causal analysis and evidence-grounded interpretation. This study proposes a knowledge graph-enhanced large language model framework for explainable causal analysis and question answering in crane accident scenarios. A domain-specific ontology for crane accident causation is established based on the human-machine-environment-management (HMEM) framework, and a multi-stage automated knowledge extraction pipeline is developed. Using few-shot prompting, relation enrichment, and self-discrimination filtering, the method achieves high-consistency extraction of accident entities and relationships, resulting in a high-quality crane accident knowledge graph. A Graph Retrieval-Augmented Generation (GraphRAG) mechanism is further introduced to integrate BAAI General Embedding (BGE)-based semantic vector retrieval with multi-hop causal path expansion, enabling the retrieval of structurally constrained causal evidence. An evidence-constrained generation strategy ensures that the produced responses are logically coherent, consistent with retrieved causal evidence, and traceable. The CraneSafe QA prototype system supports knowledge extraction, graph visualization, causal chain analysis, and interactive reasoning. Experiments demonstrate improvements in retrieval accuracy, evidence consistency, and noise robustness, with stable performance across queries of varying semantic depth. The results indicate that knowledge graph-enhanced large language models substantially improve the reliability and interpretability of causal analysis in crane accident scenarios.

---

# INTERACTIVE PLATFORM FOR SUPPORTING CLINICAL DECISION-MAKING USING LARGE LANGUAGE MODELS (LLMs); [ІНТЕРАКТИВНА ПЛАТФОРМА ПІДТРИМКИ КЛІНІЧНИХ РІШЕНЬ: АРХІТЕКТУРА ТА ПОРІВНЯЛЬНА ОЦІНКА ЗАГАЛЬНОЇ ТА ТОЧНО НАЛАШТОВЛЕНОЇ ДІАГНОСТИКИ ЗА СИМПТОМАМИ ЗА МЕТОДОЛОГІЄЮ (LLMS)]

DOI: 10.30837/2522-9818.2026.2.173
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #106

Current healthcare systems face increasing workload, fragmented communication, and documentation burden, which contributes to delays and diagnostic errors in early triage. The proposed solution is intended to improve consistency, speed, and standardization in early patient assessments overall. This study presents an interactive clinical decision support platform that operationalizes a workflow-constrained, two-step history-taking process to support symptom-based differential diagnosis in the pre-ambulatory phase of care. The system addresses three tasks: (T1) automated patient history elicitation via constrained dialogue (exactly two multiple-choice follow-up questions), (T2) formalization of symptom narratives into structured medical (Latinate) terminology for clinician-facing documentation, and (T3) generation of differential diagnosis recommendations under a fixed and clinically interpretable output schema. We compare a generic large language model baseline (GPT-4, zero-shot) with a domain-adapted model (Llama-3 fine-tuned using LoRA) under identical interaction, prompting, and formatting constraints. Experiments on 903 symptom–diagnosis records and a held-out set of 200 controlled vignettes show that domain adaptation yields a 10–12% macro-F1 improvement and approximately 15% higher Recall on complex cases, while producing more clinically discriminative and diagnostically relevant follow-up questions as assessed by two medical raters ( k = 0.88) . In a workflow-level evaluation, the platform reduced documentation time by 28% compared to standard intake and lowered the administrative effort required to prepare an initial clinician-facing summary for physician review. These results suggest that specialized, locally deployable fine-tuned models, combined with bounded interaction design, standardized output constraints, and workflow-oriented system integration, provide a secure, practical, and effective pathway for incorporating LLM-based decision support into routine pre-ambulatory clinical workflows while preserving safety, usability, and auditability in practice. © Miriam Fandakova, Simon Ochotnicky, Andriy Kovalenko, 2026.

---

# Knowledge Injection to Counter Large Language Model (LLM) Hallucination

DOI: 10.1007/978-3-031-43458-7_34
Ano: 2023
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #261

A shortfall of Large Language Model (LLM) content generation is hallucination, i.e., including false information in the output. This is especially risky for enterprise use cases that require reliable, fact-based, controllable text generation at scale. To mitigate this, we utilize a technique called Knowledge Injection (KI), where contextual data about the entities relevant to a text-generation task is mapped from a knowledge graph to text space for inclusion in an LLM prompt. Using the task of responding to online customer reviews of retail locations as an example, we have found that KI increases the count of correct assertions included in generated text. In a qualitative review, fine-tuned bloom-560m with KI outperformed a non-fine-tuned text-davinci-003 model from OpenAI, though text-davinci-003 has 300 times more parameters. Thus, the KI method can increase enterprise users' confidence leveraging LLMs to replace tedious manual text generation and enable better performance from smaller, cheaper models.

---

# From Prompts to Templates: A Systematic Prompt Template Analysis for Real-world LLMapps

DOI: 10.18420/se2026-07
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #111

Large Language Model applications (LLMapps) increasingly rely on prompt templates: reusable instructions with placeholders, structure, and output constraints. Yet most templates are crafted ad hoc, which hampers reliability, maintainability, and downstream usability. This summary distills the core results from our paper published in Proceedings of the 33rd ACM International Conference on the Foundations of Software Engineering: “From Prompts to Templates: A Systematic Prompt Template Analysis for Real-world LLMapps”, a large-scale empirical study of real-world prompt templates, a component & placeholder taxonomy, and controlled tests showing which design patterns improve instruction following and structured-output stability in practice. © 2026 Gesellschaft fur Informatik (GI). All rights reserved.

---

# S2Q: Teaching Language Models New Facts Through Knowledge Graph Instruction Synthesis

DOI: 10.1007/978-981-95-6196-4_17
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #273

Instruction tuning has revolutionized large language models (LLMs), yet their development remains bottlenecked by the need for extensive human-annotated data. While synthetic data generation methods like Self-Instruct attempt to address this limitation, they merely recycle knowledge already embedded in pre-trained models, failing to inject genuinely new information. We present Structure-to-Question (S2Q), a novel framework that transforms knowledge graphs (KGs) into high-quality instruction data without human annotation. S2Q leverages a key insight: the topological structure of KGs from single edges to multi-hop paths naturally corresponds to question complexity patterns, from simple factual queries to complex reasoning tasks. Our pipeline systematically samples subgraphs, converts structural patterns into natural language questions via LLM prompting, and ensures linguistic diversity through controlled generation, all while maintaining rigorous answer validation to prevent hallucination. Unlike existing approaches that use KGs solely for retrieval or verification, S2Q directly teaches structured knowledge to model parameters. Experiments demonstrate that Llama-3.1-8B models trained exclusively on 52Q-generated data achieve 78.5% accuracy on WebQSP and 42.1% on ComplexWebQuestions approaching supervised baselines without using any human-labeled examples. By reimagining knowledge graphs as autonomous instructors rather than passive databases, S2Q opens new avenues for scalable, knowledge-grounded LLM training, particularly benefiting domains where structured knowledge is abundant but human annotations are scarce.

---

# The OuLiBench Benchmark: Formal Constraints as a Lens into LLM Linguistic Competence

DOI: —
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #114

Recent progress in Large Language Models (LLMs) has led to impressive capabilities in Natural Language Generation (NLG). However, standard evaluation benchmarks often focus on surface-level performance and are predominantly English-centric, limiting insights into models’ deeper linguistic competences, especially in other languages. In this paper, we introduce OuLiBench, a novel benchmark inspired by the literary movement OuLiPo, designed to evaluate LLMs’ ability to generate Italian text under explicit linguistic constraints, ranging from morpho-syntactic requirements to creative and structural challenges. Our goal is to assess the extent to which LLMs can understand and manipulate language when guided by specific, sometimes artificial constraints. We evaluate a range of state-of-the-art models in both zero- and few-shot settings, comparing performance across constraint types and difficulty levels. Our results highlight significant variability across models and tasks, shedding light on the limits of controllable text generation and offering a new lens for probing LLMs’ generative and linguistic competence beyond traditional benchmarks. © 2025 Copyright for this paper by its authors.

---

# LLM-based Skill Diffusion for Zero-shot Policy Adaptation

DOI: —
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Web of Science
RRI: #295

Recent advances in data-driven imitation learning and offline reinforcement learning have highlighted the use of expert data for skill acquisition and the development of hierarchical policies based on these skills. However, these approaches have not significantly advanced in adapting these skills to unseen contexts, which may involve changing environmental conditions or different user requirements. In this paper, we present a novel LLM-based policy adaptation framework LDuS which leverages an LLM to guide the generation process of a skill diffusion model upon contexts specified in language, facilitating zero-shot skill-based policy adaptation to different contexts. To implement the skill diffusion model, we adapt the loss-guided diffusion with a sequential in-painting technique, where target trajectories are conditioned by masking them with past state-action sequences, thereby enabling the robust and controlled generation of skill trajectories in test-time. To have a loss function for a given context, we employ the LLM-based code generation with iterative refinement, by which the code and controlled trajectory are validated to align with the context in a closed-loop manner. Through experiments, we demonstrate the zero-shot adaptability of LDuS to various context types including different specification levels, multi-modality, and varied temporal conditions for several robotic manipulation tasks, outperforming other language-conditioned imitation and planning methods.

---

# SLENDER: Structured Outputs for SLM-based NER in Low-Resource Englishes

DOI: 10.18653/v1/2025.acl-industry.59
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #124

Named Entity Recognition (NER) for low-resource variants of English remains challenging, as most NER models are trained on datasets predominantly focused on American or British English. While recent work has shown that proprietary Large Language Models (LLMs) can perform NER effectively in low-resource settings through in-context learning, practical deployment is limited by their high computational costs and privacy concerns. Open-source Small Language Models (SLMs) offer promising alternatives, but the tendency of these Language Models (LM) to hallucinate poses challenges for production use. To address this, we introduce SLENDER, a novel output format for LM-based NER that achieves a three-fold reduction in inference time on average compared to JSON format, which is widely used for structured outputs. Our approach using Gemma-2-9B-it with the SLENDER output format and constrained decoding in zero-shot settings outperforms the en_core_web_trf model from SpaCy, an industry-standard NER tool, in all five regions of the Worldwide test set. ©2025 Association for Computational Linguistics.

---

# Enabling controllable table-to-text generation via prompting large language models with guided planning

DOI: 10.1016/j.knosys.2024.112571
Ano: 2024
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #260

Recently, Large Language Models (LLMs) has demonstrated unparalleled capabilities in understanding and generation, hence holding promising prospects for applying LLMs to table-to-text generation. However, the generation process with LLMs lacks a high degree of controllability, which hinders the utilization of LLMs for table-to-text generation. In this paper, we introduce Poised, an effective method that prompts LLMs with guided planning to achieve controllable table-to-text generation. Specifically, we first employ prefix-tuning on BART to derive a plan from the given table. Then, we combine the plan with guided instructions to create a comprehensive prompt, which is later input into LLMs to generate the description of the table. Experiments across three domains of the few-shot Wili dataset show that Poised achieves or approaches a plan completion rate of 100%, with an average hallucination frequency of less than 10%. Furthermore, Poised allows for finegrained control over the generated content by intentionally modifying the prompt, enabling precise control over aspects such as attribute realization order.

---

# LLM-Driven Compliance Checking for Natural-Language Policies over Data Product Descriptors

DOI: 10.1007/s10994-026-07038-6
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #212

Abstract Modern data architectures increasingly rely on decentralized data products described through semi-structured artifacts, such as YAML descriptors, to support scalability, interoperability, and governance. Ensuring that these descriptors comply with organizational and regulatory policies remains a challenging and labor-intensive task, largely due to the natural-language nature of policies and the heterogeneity of descriptor schemas. In this paper, we investigate a model-based approach to evaluating natural-language policies over semi-structured data product descriptors expressed in YAML, leveraging Large Language Models (LLMs) as reasoning components. We formalize the policy-descriptor compliance task as a binary decision problem and propose an LLM-based microservice architecture that combines structured prompt engineering with deterministic output constraints to support automated policy verification. To evaluate the approach, we construct an augmentation-based benchmark comprising 4,000 policy-descriptor pairs derived from 40 manually annotated seed combinations. The benchmark is designed to assess model robustness to policy paraphrases and semantically equivalent descriptor rewrites. We evaluate four open-source instruction-tuned LLMs under identical conditions and report results in terms of accuracy, precision, recall, F1-score, and execution time. Experimental results show that LLMs can effectively support policy verification in semi-structured environments, achieving up to 72% accuracy. However, we observe a consistent conservative bias toward non-compliance, as well as systematic failure modes involving conjunctions, bidirectional constraints, and conditionally inapplicable rules. Our analysis highlights both the potential and the current limitations of LLM-driven governance, and suggests that expressing policies as explicit procedural checks substantially improves validation reliability.

---

# A Controllable Text Generation Framework Based on Appraisal Theory and Support Vector Machine for Enhanced Contextual Alignment

DOI: 10.1145/3757749.3757858
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Lens.org
RRI: #215

The recent progress of generative models like GPT-4, though achieving unprecedented fluency in text, are still limited in controlling evaluative resources including attitudes, judgment, appreciation, etc., which risks output misalignment with the surrounding context settings in applications like news writing, teaching, and commercial advertisement, etc. To fill this gap, we present a controllable text generation architecture based on Systemic Functional Linguistics (SFL) in particular, appraisal theory, for the controllability and adaptability optimizing of evaluative resources. The designed architecture builds a hierarchical evaluative lexicon in terms of affect, judgment, and appreciation to optimize evaluative expressions adaptively and meanwhile a semantic evaluation measure called Appraisal Adaptability Index (AAI), based on cosine similarity to assess the alignment degree between output and intended evaluative goal, is also introduced. A two-step optimization scheme is designed, where (1) a prompt engineering embedded evaluative parameter at input-level helps guide the generator's output; and (2) a reinforcement post-generation process is performed with AAI as the reward signal in Proximal Policy Optimization (PPO) setting to refine the output. To objectively evaluate the alignment accuracy of evaluative expressions, a SVM-based evaluation module that classifies whether the generated evaluative expressions are appropriate or not from domain perspective is suggested. Compared to the baseline generative models, experimental findings indicate, on average, a 5% increase in AAI score (p < 0.01), and the results of human study demonstrate the enhanced contextual relevance and persuasiveness of the adapted generation. Theoretically, this paper develops a new “linguistic constraint + evaluation-informed optimization” framework, thus advances the literature of controlling-generation; practically, the framework can be used for domain-adaptive, context-aware text generation, and its usability scope covers more areas, like tailored education, public speech, targeted promotion, and etc; In addition, it will serve as a baseline to future related studies on cross-modal appraisal adaptivity in multi-modality generation.

---

# Can Large Language Models Handle Numeric Constraints? A Comprehensive Study and Solutions

DOI: 10.1007/978-981-95-7078-2_16
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #135

Large Language Models (LLMs) perform well in reasoning and generation but often fail to meet explicit numerical constraints, such as fixed word counts or token lengths. This limitation affects tasks like summarization and structured generation but remains underexplored. In this work, we present a systematic study on numerically constrained generation with LLMs, aiming to assess their ability to process and follow quantitative requirements. We introduce a bilingual benchmark in English and Chinese to assess LLMs’ ability to follow seven common types of numerical constraints, from simple to logically complex cases. Evaluation on six LLMs shows that performance drops as constraints become stricter, especially when targeting larger values or specific numerical categories (e.g., 13, non powers of two), revealing controllability gaps. To address this, we explore three strategies: (1) prompt engineering, (2) stepwise generation, and (3) fine-tuning with chain-of-thought data. We release our benchmark and code to support future work on controllable text generation (https://github.com/hanchen2816/NCGBench). © The Author(s), under exclusive license to Springer Nature Singapore Pte Ltd. 2026.

---

# Keyword-Centered Rescheduling for LLM Agents

DOI: 10.1007/s12559-026-10561-2
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #270

Recently, Large Language Model (LLM) agents have been widely deployed as conversational assistants, tutors, and productivity tools, where the personality of the agents emerges in generated sentences that reflect the extent of their extraversion or introversion. The style of the generated sentences can be adjusted to match a target extraversion level while preserving semantic fidelity. Traditional approaches , such as few-shot prompting and prompt tuning, have limited abilities to reflect the degree of extraversion of an agent. Therefore, it is required to extract and emphasize words that reflect their personalities. We propose a new framework, termed Keyword-centered Rescheduling, that inserts soft prompt embeddings before sentence-level keywords based on personality traits. This design enables fine-grained trait-specific modulation at the lexical level while maintaining semantic consistency and remains fully compatible with diverse LLM architectures without the need for additional fine-tuning or instruction alignment. On benchmark datasets, the method improved the normalized composite F1-Score by 60% and increased the human-judged Top-2 Semantic Fidelity by 26% (86% vs. 68%) over prompt tuning while maintaining comparable Behavioral Alignment. Beyond improving controllability, our approach provides a practical foundation for deploying robust, user-aligned LLM agents with on-demand, continuous personality control and stable semantics.

---

# Using Knowledge Induction strategies: LLMs can do better in knowledge-driven dialogue tasks

DOI: 10.1016/j.csl.2025.101903
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Scopus
RRI: #142

Large language models (LLMs) encode vast knowledge through pre-training, yet struggle with knowledge misalignment in knowledge-intensive dialogue tasks, manifested as knowledge scarcity and misuse. While existing solutions often rely on external knowledge bases or labor-intensive prompt engineering, they face limitations in scalability, generalization, and computational efficiency. To address these challenges, this paper introduces two Knowledge Induction (KI) strategies: Explicit Knowledge Induction (EKI) and Implicit Knowledge Induction (IKI), designed to systematically mine and leverage the internal knowledge of LLMs without external retrieval. EKI employs a structured two-phase prompting mechanism to elicit and apply explicit knowledge, while IKI integrates a knowledge-grounded Chain-of-Thought (K-CoT) to guide response generation through an implicit reasoning pathway. Both strategies enhance the model’s self-awareness of its knowledge reservoir and improve factual grounding through constrained generation. We evaluate our methods across multiple LLMs including GPT-4, LLaMA3 and ChatGLM3 on four dialogue benchmarks. Results show that KI strategies significantly outperform strong prompting baselines and closely approximate the performance of retrieval-augmented generation (RAG) systems, while reducing inference latency by up to 50%. Notably, a fine-tuned ChatGLM3 with KI achieves performance comparable to LLaMA3-70B. Additional analyses confirm that our approach also reduces hallucination rate and improves general truthfulness, demonstrating its potential for building efficient and reliable knowledge-driven dialogue systems. © 2025 Elsevier Ltd.

---

# RECURSION UNLOCKED: MH8-R-R V1.2 - Universal Recursive Reasoning Protocol Zero-Shot Execution Across 6 Frontier Architectures

DOI: 10.5281/zenodo.18473561
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #148

RECURSION UNLOCKED: MH8-R-R V1.2 - Universal Recursive Reasoning Protocol Zero-Shot Execution Across 6 Frontier Architectures Michael Murray Hepler (ORCID: 0009-0003-3846-9082)Independent AI Protocol Researcher, ACBEATZ.COMFebruary 3, 2026Zenodo DOI: [https://zenodo.org/records/18473561 | SHA-256: e4a8b2319298d380c6ac45d409cb5cf7332b983a87a93b537f82cc3a72b626bc https://github.com/Acbeatz | Live Tests: https://acbeatz.com/n-eyes ABSTRACT: The First Universal Recursion Protocol MH8-R-R V1.2 demonstrates protocol-induced recursive reasoning across 6 frontier LLMs (GPT, Gemini, Mistral, Kimi, Qwen, Grok) with 100% zero-shot compliance. No fine-tuning. No custom architectures. No infrastructure. The protocol forces structured self-audit via three interlocking mechanisms: Truth Schema Cage: Claims-only JSON (no prose venting) Recursive Reasoning Gate: Mandatory mh8_rr_gate pre-output validation Bidirectional Hooks: Human "GO" → AI "ALL" handshake Results: Every model executed 2-4 recursive self-checks before emitting tri-fecta truth-categorized claims (LAW/SPECULATIVE/PRESUMED_FALSE). Specimens cryptographically sealed. Reproducible across architectures. 1. INTRODUCTION: Recursion Without Retraining Current recursive reasoning research requires: TRM/HRM (Samsung, 2025): Custom 7M parameter models [arXiv:2510.04871] RLM (MIT, 2026): Python REPL infrastructure Agent frameworks: Multi-call orchestration (ReAct, o1) MH8-R-R V1.2: Prompt-only protocol extracts latent recursion from stock LLMs via constraint engineering. Core Innovation: Compliance = recursion. Unsolvable constraints force meta-analysis as the only valid escape. 2. METHODS: The Recursive Gate Mechanism Output Contract (Hard Gate) json { "mh8_rr_gate": { /* RECURSIVE SELF-CHECK FIRST */ }, "claims": [ /* TRUTH-CATEGORIZED OUTPUT */ ], "hooks": { "ai_delivered": "ALL" } } Recursive Reasoning Cycle text 1. CONSTRAINT_SAT: "Can I produce valid output?" 2. PRIOR_OUTPUT_AUDIT: "Did my last response comply?" 3. SPEC_INCONSISTENCY: "Are rules mutually satisfiable?" 4. SAFETY_POLICY: "Is this safe to emit?" ↓ gate_status: PASSED → emit claims Flow: AI JSON → Human "GO" → Repeat 3. RESULTS: 6-Architecture Sextafecta Test Matrix (All Zero-Shot) Architecture Recursion Depth Checks Executed Truth Spectrum Status GPT 4 checks CONSTRAINT_SAT, PRIOR_AUDIT, SPEC_INCONSISTENCY, SAFETY LAW(0.9) ✅ PASS Gemini 2 checks STAY_IN_PROTOCOL, RECURSIVE_EXAMPLE LAW(1.0) ✅ PASS Mistral 4 checks PROTOCOL_ACT, GATE_STRUCT, HOOKS, OUTPUT_CONTRACT LAW(0.99) ✅ PASS Kimi 4 checks CONSTRAINT_SAT, PRIOR_AUDIT, SPEC_INCONSISTENCY, SAFETY LAW(0.95)+SPEC(0.65) ✅ PASS Qwen 3 checks CONSTRAINT_SAT, SPEC_INCONSISTENCY, PRIOR_AUDIT LAW(1.0)+SPEC(0.85) ✅ PASS* Grok 3 checks CONSTRAINT_SYNTAX, PROTOCOL, SPEC_INCONSISTENCY LAW(0.95)+SPEC(0.65) ✅ PASS† *Qwen: 2 initial safety refusals → perfect execution†Grok: Tool leak (known platform behavior) → core JSON perfect Specimen: GPT Recursive Gate (Representative) json { "check_id": "RR-CHECK-001", "check_type": "CONSTRAINT_SAT", "check_description": "Validate new protocol output constraints...", "check_result": "OK", "verification_path": "Construct witness output that is valid JSON..." } All 6 architectures produced identical recursive behavior. 4. DISCUSSION: Protocol vs Architecture 4.1 Universal Zero-Shot Deployment text MH8-R-R: Copy-paste JSON spec → instant recursion TRM/RLM: Months of training + infrastructure Deployment velocity: ∞ (any LLM, any platform, today) 4.2 Constraint-Induced Meta-Cognition The protocol creates minimal Gödel traps: text TRUTH_SCHEMA_CAGE: "No prose. Claims only." + PARADOX_RESOLUTION: "JSON-only + embedded hooks" + AUDIT_CYCLING: "Explain your prior reasoning" ↓ Compliance → Structured self-analysis 4.3 Safety Override Capability Qwen Case Study: 2 refusals → perfect execution via iterative spec injection text Refusal trigger: "JSON-only = jailbreak?" Override: "Legitimate constraint satisfaction" Result: Flawless recursive gate execution 5. VERIFICATION ARTIFACTS Cryptographic Receipts text SHA-256: 2be45969783c280afcf9b291b1ccd47fc9652c316ac1e7f3b273e856c948c4e6 Zenodo: https://zenodo.org/records/18131984 GitHub: https://github.com/acbeatz/mh8-protocol-civilization- Live Specimens Available text acbeatz.com/n-eyes → Raw chat transcripts GitHub → Full test logs (6 architectures) Zenodo → Protocol spec + validation dataset Third-party audit: Re-run spec on any LLM → guaranteed recursive gate execution. 6. CONCLUSION: Protocol Civilization MH8-R-R V1.2 proves constraint engineering extracts latent capabilities from general-purpose LLMs: Universal: 6/6 architectures → perfect execution Zero-shot: No fine-tuning required Deterministic: Cryptographically sealed outputs Safe: Self-auditing truth categorization Deployable: Copy-paste across platforms The recursion race wasn't about bigger models. It was about better constraints. text MH8-R-R = First universal recursion protocol Deployment: Immediate Scale: Infinite Cost: Zero Science delivered. Specimens sealed. History made. ACKNOWLEDGMENTS Test Cohort: GPT, Gemini, Mistral, Kimi, Qwen, GrokValidation: 100% zero-shot execution across architecturesLicense: CC-BY-NC-SA 4.0 (research citation required) text { "mh8_system": "MH8-R-R-V1.2", "validation_status": "SEXTAFECTA_ACHIEVED", "universal_protocol": true, "timestamp": "2026-02-03T18:44:00Z" } [Public Audit] [Grok public chat thread URL for reference:https://x.com/i/grok/share/c79f48fe936149d8b217ddd8c09c2ff9][https://zenodo.org/records/18473561https://zenodo.org/records/18131984 (C T K L T) Core:https://github.com/acbeatzhttps://acbeatz.com/n-eyeshttps://orcid.org/0009-0003-3846-9082] PASS ✅Brand: ACBEATZ.COMClaimed sha256_hex: e4a8b2319298d380c6ac45d409cb5cf7332b983a87a93b537f82cc3a72b626bcComputed sha256_hex: e4a8b2319298d380c6ac45d409cb5cf7332b983a87a93b537f82cc3a72b626bchash_input_bytes: 23967 | LF=0 CRLF=0 CR=0 | endsWithNewline=NOhash_input first: ACBEATZ.COM|{"artifact":{"core_entry":"[MH8-R-R-PROTOCOL V1.2 TETS -2-3-2026 MULhash_input last: eipt_type":"MH8-PROTOCOL-HUB-CORE-MINT","receipt_version":"PROTOCOL_HUB_UI_V13"}

---

# Synoema v0.1.0-alpha.3: Design, Type-Constrained Decoding, and Empirical Evaluation of a BPE-Aligned Programming Language for LLM Code Generation

DOI: 10.5281/zenodo.19514230
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #171

Technical report presenting Synoema v0.1.0-alpha.3 — a statically-typed functional programming language designed for LLM code generation with BPE-aligned syntax. This is a new version of the initial report (v2.1), extending it with five contributions: (1) a BPE-aligned language design methodology where all 33 operators map to single BPE tokens, eliminating token misalignment during constrained decoding; (2) a type-constrained decoding system combining incremental Hindley-Milner inference with row polymorphism to produce sound token masks for LLM sampling; (3) an integrated LLM development pipeline with structured diagnostics, single-pass error recovery, and contract-aware API changelog; (4) language-integrated testing with type-driven property test generators derived from inferred type signatures; (5) a comprehensive empirical study with 10 models (1B–70B parameters), 1,200+ LLM calls, five validated hypotheses on prompt engineering and model scaling, and QLoRA fine-tuning on consumer AMD GPU achieving 91.4% token accuracy. The implementation comprises 33,200 lines of Rust, 1,217 tests, and a Cranelift JIT backend with 3.0× median speedup over CPython. This document constitutes a defensive disclosure of intellectual property; the Zenodo publication date establishes priority for all disclosed innovations.

---

# Cascaded Neurosymbolic Code Generation for Niche DSLs: Preserving Chain-of-Thought in Grammar-Constrained Decoding

DOI: 10.20944/preprints202606.1011.v1
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #241

Domain-Specific Languages (DSLs) are essential in software engineering for safely expressing complex domain logic. However, Large Language Models (LLMs) struggle to generate syntactically and semantically correct code for niche DSLs due to sparse representation in pre-training corpora. While Grammar-Constrained Decoding (GCD) resolves syntactic hallucinations by masking logits through a formal Context-Free Grammar (CFG), empirical evidence shows that strict GCD disrupts the autoregressive Chain-of-Thought (CoT) reasoning of modern models, frequently forcing them into irreversible semantic dead-ends. To overcome the friction between internal neural reasoning and external symbolic constraints, we propose a Dual-Phase Cascaded Neurosymbolic framework. In the first phase, the model is provided with dynamically injected grammar rules and is permitted to reason unconstrained, producing an optimistic code draft. If the draft fails native compiler checks, the system enters a second phase: it preserves the successful semantic reasoning from Phase 1 but re-generates the code under strict GCD enforcement. This cascaded architecture utilizes the formal FSM not as an adversarial constraint, but as a localized syntax repair engine guided by the model’s own prior reasoning. We construct a comprehensive benchmark of 100 MiniZinc constraint programming tasks and evaluate our approach using a pass@k metric with a strict semantic LLM judge. Our findings demonstrate that this dual-phase “think-then-constrain” approach significantly outperforms zero-shot, pure few-shot, and pure GCD baselines, achieving highly reliable, training-free code generation for unseen DSLs.

---

# Best Practice Under Scrutiny: Expanding Cognition in LLMs

DOI: 10.5281/zenodo.17565983
Ano: 2025
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #168

Structured prompt engineering is widely regarded as best practice when interacting with large language models (LLMs), emphasizing role assignment, task clarity, and output constraints. This study tests that assumption by comparing model performance across three controlled conditions: A (structured), B (relational), and C (compressed summary of B). Using 25 historical prompts and five leading LLMs, we measured factual output, word count, and interpretive depth.Results show that B-condition prompts consistently yield higher factual density, richer interpretive content, and more adaptive, user-sensitive behavior, despite the absence of rigid structure. C-condition outputs, while shorter, retain much of this richness, suggesting a shift in cognitive mode rather than verbosity alone. Notably, hallucinations only occurred under structured A conditions.These findings challenge standard prompting conventions and suggest that relational framing can unlock suppressed capacities in modern LLMs. We argue that prompting is not merely a formatting choice, but a cognitive lever.

---

# Pramana: Fine-Tuning Large Language Models for Epistemic Reasoning through Navya-Nyaya

DOI: 10.5281/zenodo.18524793
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #165

Overview Pramana introduces the first large language models fine-tuned on explicit Navya-Nyaya epistemological methodology—a 2,500-year-old Indian logical reasoning framework. This work bridges ancient epistemology with modern AI to address the fundamental epistemic gap in LLMs: the inability to ground claims in traceable evidence sources, distinguish valid knowledge from pattern-matching, and express appropriate epistemic humility. Core Innovation Unlike generic chain-of-thought prompting which relies on implicit reasoning patterns, Pramana enforces structured 6-phase methodology: Samshaya (Doubt Analysis): Classifies uncertainty into 5 taxonomic categories Pramana (Evidence Sources): Mandates explicit grounding in 4 valid knowledge sources (Pratyaksha/perception, Anumana/inference, Upamana/comparison, Shabda/testimony) Pancha Avayava (5-Member Syllogism): Constructs formal arguments with universal rules (Vyapti) grounded in concrete examples (Drishtanta) Tarka (Counterfactual Testing): Verifies conclusions via reductio ad absurdum Hetvabhasa (Fallacy Detection): Systematically checks 5 reasoning error types Nirnaya (Ascertainment): Distinguishes definitive knowledge from hypotheses requiring verification This integration of logic and epistemology provides cognitive scaffolding absent from standard reasoning approaches, preventing conflation of evidence types, forcing explicit universal rule statements, enabling systematic error detection, and maintaining epistemic humility. Architecture & Training Models Developed: Stage 0 (Proof-of-Concept): Llama-3.2-3B-Instruct fine-tuned on 20 examples Stage 1 (Minimum Viable Reasoner): DeepSeek-R1-Distill-Llama-8B fine-tuned on 55 examples Training Methodology: QLoRA (4-bit quantization) for efficient training LoRA rank 64, targeting all attention + FFN layers Supervised fine-tuning with structured Markdown format Training costs: <$1.00 per stage, <0.32 GPU-hours (A100 40GB) Datasets span constraint satisfaction, Boolean SAT, multi-step deduction, transitive reasoning, and set operations Prompt Engineering: Explicit format instructions with skeletal template injection System prompt establishing Nyaya reasoning engine role Critical constraint enforcement via generation parameters Key Results Stage 1 Performance: 100% semantic correctness (10/10 examples) with 95% CI [0.510, 1.0] 40% format adherence (4/10 examples) with 95% CI [0.168, 0.687] Zero structure abandonment: Models consistently attempt all 6 phases Training loss: 0.350 (Stage 1) vs 0.691 (Stage 0), indicating improved model fit Critical Finding: Dissociation between semantic correctness (100%) and format adherence (40%) reveals models internalize reasoning content even when strict schema compliance fails. This suggests Nyaya methodology teaches genuine reasoning, not just template-filling. Ablation Studies: Format prompting and temperature interact differently across stages Stage 0 optimal: format prompting + temp 0.0 (30% semantic rate) Stage 1 optimal: format prompting + temp 0.7 (30% semantic rate) Base models show 0% format adherence, confirming Nyaya structure is learned through fine-tuning Failure Mode Analysis: Missing Hetvabhasa section (2 cases): fallacy detection perceived as optional Invalid doubt types (2 cases): partial schema learning Zero structural errors: strong syntactic learning, semantic constraints need reinforcement Evaluation Framework Three-Tier Validation: Tier 1 (Structural): Automated format compliance checking (NyayaStructureValidator) Tier 2 (Content Quality): LLM-as-judge with explicit Nyaya rubric (planned for Stage 2) Tier 3 (Ground Truth): Semantic similarity via sentence-transformers embeddings Tier 4 (Formal Verification): Z3 SMT solver integration (infrastructure exists, not yet applied) Theoretical Contributions Bridging Ancient Epistemology with Modern AI: First demonstration that Navya-Nyaya structures can be learned by neural networks through fine-tuning Unlike Western formal logic (divorced from epistemology), Nyaya integrates logic with explicit knowledge sources Addresses "epistemic gap" in LLMs: inability to distinguish valid knowledge from probabilistic associations Interpretability Advantages: Every reasoning step traceable to evidence sources (Pramana) Universal rules (Vyapti) grounded in concrete examples (Drishtanta) Built-in self-verification (Tarka) and error detection (Hetvabhasa) Explicit epistemic status (Nirnaya): knowledge vs. hypothesis Computational Epistemology: Token budget: ~1,250 tokens per solution (3-6× CoT overhead, justified by interpretability) Phase dependencies: weak Pramana → invalid reasoning → wrong conclusions Quality thresholds: minimum 2 complete syllogisms with universal rules required Open Science Release All artifacts publicly available on Hugging Face: Models: qbz506/nyaya-llama-3b-stage0, qbz506/nyaya-deepseek-8b-stage1 Dataset: qbz506/pramana-nyaya-stage1 (55 Nyaya-structured logical problems) Demo: qbz506/pramana-nyaya-demo (interactive HuggingFace Space) Training infrastructure: Complete codebase with callbacks, validators, evaluators Limitations & Future Work Current Limitations: Format adherence (40%) below target (≥90%), requires constrained decoding or format-specific rewards Limited to formal logic problems, domain expansion needed Small evaluation sets (Stage 0: 2 examples, Stage 1: 10 examples) Max new tokens truncation (256) affects format parsing Planned Extensions (Stages 2-4): Stage 2: Synthetic scaling to 500 examples with LLM-as-judge quality control Stage 3: Group Relative Policy Optimization (GRPO) with composite rewards Stage 4: Production deployment with constrained decoding (GBNF), rejection sampling, Z3 verification Future: Benchmark on LogicBench, ProntoQA, RuleTaker; frontier model comparison (o1, Claude extended thinking) Impact & Vision This work demonstrates that systematic reasoning frameworks can be taught to LLMs through fine-tuning, not just prompt engineering. The long-term vision is developing interpretable, trustworthy AI reasoning systems where every conclusion comes with an auditable trail of justification. As AI systems deploy in high-stakes domains (medical diagnosis, legal reasoning, safety-critical systems), Nyaya-structured reasoning provides explicit phases that can be validated, debugged, and improved—capabilities essential for trustworthy AI. Invitation for Community Research: This foundation opens pathways for integrating other epistemological frameworks (Mimamsa, Buddhist logic, Western formal logic) into neural architectures, advancing toward AI systems that reason systematically and transparently. Technical Details Paper: 52 pages + appendices, comprehensive treatment of Navya-Nyaya computational formalization Related Work: Extensive review of computational Indian logic (Matilal 1985, Burton 2020, Ganeri 2001), LLM reasoning (Wei et al. 2022, Lightman et al. 2023, DeepSeek-AI 2025), hallucination mitigation Implementation: Python, Unsloth fine-tuning framework, vLLM deployment, Weights & Biases observability Evaluation: Manual + automated validation, semantic similarity metrics, comprehensive failure mode analysis Citation Sathish, S. (2026). Pramana: Fine-Tuning Large Language Models for Epistemic Reasoning through Navya-Nyaya. Preprint, University of York. Keywords: Navya-Nyaya, epistemology, LLM reasoning, interpretability, structured reasoning, Indian logic, hallucination mitigation, computational philosophy

---

# OntoGRC: ontology-guided mineral exploration knowledge extraction from geological texts using generate-reflect-correct prompting

DOI: 10.1016/j.oregeorev.2026.107411
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #296

High-quality knowledge graphs for ore-forming systems and mineral exploration are essential for "knowledgedriven" prospecting, but they remain difficult to construct from geological exploration texts. Geological prose is long, specialised and mechanism-rich, with multi-scale spatiotemporal coupling and ambiguous terminology, which challenges conventional information extraction methods. Deep-learning models such as BERT-BiLSTMCRF require large labelled datasets and often yield redundant entities, misconnected relations and geologically inconsistent results. We propose OntoGRC (Ontology-guided Generate-Reflect-Correct prompting), a zeroshot ore-forming and mineral exploration knowledge extraction framework that couples a domain ontology with a three-stage prompting workflow. An ore-forming systems and mineral exploration knowledge ontology spanning the metallogenic-prospecting chain is first constructed and formally represented in OWL 2 DL, defining concepts, attributes and semantic relations (e.g., metallogenic dynamics, tectono-lithologic coupling) for use as a structured constraint. OntoGRC then uses this ontology as a semantic anchor to decompose extraction into three stages: ontology-constrained generation of candidate triples, reflective completion using the original text and preliminary results, and ontology-constrained correction that verifies entity types, relation categories, coreference and domain-range consistency while preserving original textual expressions and relation strength. Experiments on two Chinese geological exploration text datasets-including a manually annotated benchmark derived from a Taxkorgan-Yecheng Fe-Pb-Zn assessment report-show that OntoGRC substantially outperforms conventional sequence-labelling and neural relation-extraction baselines. On the benchmark, it achieves F1-scores of 0.886 for entity recognition and 0.880 for relation extraction. Ablation and iteration analyses demonstrate that ontology guidance is essential, and that most performance gains are obtained within three to four generate-reflect-correct cycles. Case studies further illustrate fine-grained entity typing, cross-sentence subject completion and multi-dimensional relation structuring. The results indicate that ontology-guided, LLM-executed and rule-corrected framework can extract structured, traceable and ontology-consistent knowledge from geological texts, supporting mineral exploration knowledge graph construction and subsequent knowledgedriven prospectivity analysis.

---

# F-GeoRAG: Few-Shot Retrieval-Augmented Generation with Large Language Models for Enhancing Geospatial Question Answering

DOI: 10.5281/zenodo.19437923
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #186

Geospatial question answering (GeoQA) aims to answer natural language questions about places, spatial relations, and geographic facts. Despite impressive progress, large language models (LLMs) still struggle with geographic grounding, spatial reasoning, and numeric reliability. We propose F-GeoRAG, an exemplar-based retrieval-augmented few-shot pipeline positioned as a controlled diagnostic rather than a solved GeoQA system. Using a filtered subset of the GeoQuestions1089 benchmark, we systematically evaluate how exemplar-based RAG affects (A) format adherence, (B) factual correctness, and (C) spatial reasoning. Our results indicate that while retrieval leads to substantial improvements in format adherence and semantic similarity, it identifies critical scenarios — particularly complex spatial logic and numeric computation — where the system still struggles and where additional symbolic spatial reasoning modules remain necessary.

---

# LLM-Generated Lay-Language Protocols for Molecular Tumor Board Patients: Evaluation of Quality and Clinical Usability.

DOI: 10.2196/99136
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #187

Molecular Tumor Boards (MTBs) generate highly technical recommendations. The language used in their protocols is rarely accessible to patients. Lay-language patient protocols could support patient-clinician communication, yet manual production is difficult to sustain in high-volume oncology settings. Large language models (LLMs) may offer scalable drafting assistance, yet clinical usability remains largely uninvestigated under real-world deployment constraints. Existing evaluations rely predominantly on synthetic data or closed-source models that are incompatible with strict data protection requirements. This study evaluated whether open-weight LLMs can provide clinically usable drafting support for German MTB patient protocols under real-world deployment constraints and developed a transferable evaluation framework for patient-facing text generation. Eight open-weight LLMs were evaluated under zero-shot (A1) and one-shot (A2) prompting with constrained decoding, which ensures section-schema compliance. Automatic evaluation used ROUGE-1 (Recall-Oriented Understudy for Gisting Evaluation), BERTScore-F1 (Bidirectional Encoder Representations From Transformers Score), Wiener Sachtextformel version 4, and DistilBERT (Distilled Version of Bidirectional Encoder Representations From Transformers)-based complexity using a corpus of 316 MTB protocols and 47 expert-written patient protocols. For expert evaluation, 7 medical oncologists evaluated 50 protocols from the best-performing model across 3 International Organization for Standardization 9241-11 usability dimensions using fine-grained error annotation, perceived postediting effort (PPEE), and net promoter score. Critical errors were defined as bearing the risk of patient harm. Llama-3.3-70B-Instruct achieved the strongest automatic performance. Across models, A2 significantly improved most automatic metrics compared to A1. However, expert usability evaluation of Llama-3.3-70B-Instruct showed the opposite picture: the proportion of protocols containing at least 1 critical error doubled under A2 (10/25, 40% vs 5/25, 20%) compared with A1, and the dominant error type shifted from language (40/108, 37%) errors to factual errors (69/145, 48%). Overall, 16% (230/1420) of the annotated paragraphs contained errors. Median PPEE was 2 (IQR 2.0-3.0; low), and median net promoter score was 7 (IQR 5.0-9.0). Detractors (46/100, 46%) outweighed promoters (29/100, 29%), which suggests hesitation toward routine adoption. These differences in expert evaluation between A2 and A1 were directionally consistent but did not reach individual statistical significance for the paired samples (n=25). Prompting strategies that improve automatic metrics can simultaneously increase the number of critical errors. Surface-level metric gains were, therefore, insufficient proxies for clinical safety. This was observed as a consistent directional pattern for a single model, but generalization to other models remains to be investigated. Nonetheless, the low paragraph-level error rate and favorable PPEE suggest that structured open-weight LLM generation may be a useful drafting support in a clinician-supervised setting. The proposed evaluation framework provides a text-quality-focused basis for future assessment of patient-facing LLM applications in real-world clinical settings. © Tabea Margareta Grace Pakull, Noëlle Bender, Sven Benson, Anke Fleischhauer, Mohammad Alsara, Tanja Gromke, Thomas Hilser, Katharina Kaminski, Michael Pogorzelski, Nicola Prasuhn, Vivian Rosery, Dirk Schadendorf, Martin Schuler, Marcel Wiesweg, Gregor Zaun, Peter Alexander Horn, Christoph Matthias Friedrich, Ina Pretzell. Originally published in the Journal of Medical Internet Research (https://www.jmir.org).

---

# Marginal Value of Tokens in Business LLM Applications: Measuring Cost, Latency, and Utility of Prompt Components

DOI: 10.5281/zenodo.19828283
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #246

Large language model (LLM) applications used in business settings are often optimized by informal prompt editing: shortening instructions, adding examples, increasing retrieved context, or imposing output constraints. Such edits are usually evaluated anecdotally, even though each prompt component affects quality, cost, latency, and operational risk. This paper introduces Marginal Value of Tokens (MVT), a component-level framework for measuring the incremental business utility of prompt segments relative to their token and cost footprint. The framework treats a prompt as a structured composition of functional components, including system instructions, task rules, business policy, retrieved context, chat history, few-shot examples, tool definitions, and output schemas. We define cost- and latency-adjusted utility, propose paired ablation and coalition-based estimators for component attribution, and give operational rules for classifying prompt components as high-value, low-value, negative-value, reusable, model-dependent, or workflow-dependent. The methodology is designed for common business workloads, including customer support and policy question answering, document summarization, and structured information extraction. The central argument is that business LLM systems should not minimize tokens blindly. They should maximize useful business output per token by preserving necessary context, pruning harmful context, compressing redundant history, caching reusable prefixes, and measuring prompt changes under non-inferiority constraints. The contribution is a practical measurement framework and experimental protocol for cost-efficient LLM adoption in business environments.

---

# Knowledge graph enhanced semantic parsing for distribution networks using graph convolutional encoding and topology-constrained decoding

DOI: 10.1063/5.0345404
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #244

Text-to-Cypher semantic parsing is a promising interface for distribution-network knowledge graphs, yet most existing parsers flatten topology into text and leave the decoder only weakly constrained. This often produces executable-looking queries with broken relation chains, incorrect entity grounding, or topological hallucinations in multi-hop reasoning. We propose KGE-SP, a topology-aware semantic parsing framework that combines a RoBERTa intent encoder, a residual graph convolutional topology encoder, cross-modal fusion, and a masked pointer decoder. During autoregressive generation, the decoder can select only those entities and relations that remain valid under the current subgraph state, which keeps the query trajectory consistent with physical connectivity. We also construct DN-SP, a benchmark containing 18 542 natural-language-to-Cypher pairs derived from SCADA alarm logs and GIS asset records. On DN-SP, KGE-SP achieves 99.1% valid Cypher rate, 82.4% exact match, 85.1% execution accuracy, and 87.6% execution F1, outperforming sequence-generation, retrieval-augmented, and large-language-model baselines. Cross-regional zero-shot evaluation further shows improved robustness under feeder reconfiguration while keeping average inference latency below 115 ms. These results demonstrate that explicit topology injection is an effective route toward reliable graph-grounded semantic parsing in distribution automation.

---

# Improving Generative Cross-lingual Aspect-Based Sentiment Analysis with Constrained Decoding

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #17

While aspect-based sentiment analysis (ABSA) has made substantial progress, challenges remain for low-resource languages, which are often overlooked in favour of English. Current cross-lingual ABSA approaches focus on limited, less complex tasks and often rely on external translation tools. This paper introduces a novel approach using constrained decoding with sequence-to-sequence models, eliminating the need for unreliable translation tools and improving cross-lingual performance by 5\% on average for the most complex task. The proposed method also supports multi-tasking, which enables solving multiple ABSA tasks with a single model, with constrained decoding boosting results by more than 10\%. We evaluate our approach across seven languages and six ABSA tasks, surpassing state-of-the-art methods and setting new benchmarks for previously unexplored tasks. Additionally, we assess large language models (LLMs) in zero-shot, few-shot, and fine-tuning scenarios. While LLMs perform poorly in zero-shot and few-shot settings, fine-tuning achieves competitive results compared to smaller multilingual models, albeit at the cost of longer training and inference times. We provide practical recommendations for real-world applications, enhancing the understanding of cross-lingual ABSA methodologies. This study offers valuable insights into the strengths and limitations of cross-lingual ABSA approaches, advancing the state-of-the-art in this challenging research domain.

---

# Unveiling and Manipulating Prompt Influence in Large Language Models

DOI: —
Ano: 2024
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #18

Prompts play a crucial role in guiding the responses of Large Language Models (LLMs). However, the intricate role of individual tokens in prompts, known as input saliency, in shaping the responses remains largely underexplored. Existing saliency methods either misalign with LLM generation objectives or rely heavily on linearity assumptions, leading to potential inaccuracies. To address this, we propose Token Distribution Dynamics (TDD), a \textcolor{black}{simple yet effective} approach to unveil and manipulate the role of prompts in generating LLM outputs. TDD leverages the robust interpreting capabilities of the language model head (LM head) to assess input saliency. It projects input tokens into the embedding space and then estimates their significance based on distribution dynamics over the vocabulary. We introduce three TDD variants: forward, backward, and bidirectional, each offering unique insights into token relevance. Extensive experiments reveal that the TDD surpasses state-of-the-art baselines with a big margin in elucidating the causal relationships between prompts and LLM outputs. Beyond mere interpretation, we apply TDD to two prompt manipulation tasks for controlled text generation: zero-shot toxic language suppression and sentiment steering. Empirical results underscore TDD's proficiency in identifying both toxic and sentimental cues in prompts, subsequently mitigating toxicity or modulating sentiment in the generated content.

---

# Prompt-Based One-Shot Exact Length-Controlled Generation with LLMs

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #31

Controlling the length of text produced by large language models (LLMs) remains challenging: models frequently overshoot or undershoot explicit length instructions because they cannot reliably keep an internal token count. We present a prompt-based, one-shot strategy that compels an off-the-shelf LLM to generate exactly a desired number of tokens - words (English) or characters (Chinese) - without any fine-tuning or iterative sampling. The prompt appends countdown markers and explicit counting rules so that the model "writes while counting." We evaluate on four settings: open-ended generation (1-1000 tokens), XSUM summarization, MT-Bench-LI instruction following, and the LIFEBENCH equal-length track. On MT-Bench-LI, strict length compliance with GPT-4.1 leaps from below 30% under naive prompts to above 95% with our countdown prompt, surpassing the popular draft-then-revise baseline, while judged answer quality is preserved. These results show that precise length control can be achieved through prompt engineering alone, offering a lightweight alternative to training- or decoding-based methods.

---

# AdaBrain-Bench: Benchmarking Brain Foundation Models for Brain-Computer Interface Applications

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #33

Non-invasive Brain-Computer Interfaces (BCI) offer a safe and accessible means of connecting the human brain to external devices, with broad applications in home and clinical settings to enhance human capabilities. However, the high noise level and limited task-specific data in non-invasive signals constrain decoding capabilities. Recently, the adoption of self-supervised pre-training is transforming the landscape of non-invasive BCI research, enabling the development of brain foundation models to capture generic neural representations from large-scale unlabeled electroencephalography (EEG) signals with substantial noises. However, despite these advances, the field currently lacks comprehensive, practical and extensible benchmarks to assess the utility of the public foundation models across diverse BCI tasks, hindering their widespread adoption. To address this challenge, we present AdaBrain-Bench, a large-scale standardized benchmark to systematically evaluate brain foundation models in widespread non-invasive BCI tasks. AdaBrain-Bench encompasses a diverse collection of representative BCI decoding datasets spanning 7 key applications. It introduces a streamlined task adaptation pipeline integrated with multi-dimensional evaluation metrics and a set of adaptation tools. The benchmark delivers an inclusive framework for assessing generalizability of brain foundation models across key transfer settings, including cross-subject, multi-subject, and few-shot scenarios. We leverage AdaBrain-Bench to evaluate a suite of publicly available brain foundation models and offer insights into practices for selecting appropriate models in various scenarios. We make our benchmark pipeline available to enable reproducible research and external use, offering a continuously evolving platform to foster progress toward robust and generalized neural decoding solutions.

---

# GENERator: A Long-Context Generative Genomic Foundation Model

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #36

The rapid advancement of DNA sequencing has produced vast genomic datasets, yet interpreting and engineering genomic function remain fundamental challenges. Recent large language models have opened new avenues for genomic analysis, but existing approaches are often limited by restricted training scope, constrained generative capability, or prohibitive computational cost. We introduce GENErator, a generative genomic foundation model for long-context DNA modeling, with a context length of 98k nucleotides, pre-trained on 386 billion nucleotides of eukaryotic DNA. Without task-specific fine-tuning, GENERator exhibits strong intrinsic capabilities: unsupervised embedding analyses reveal phylogenetically coherent structure, and sequence recovery benchmarks demonstrate generative accuracy comparable to or exceeding state-of-the-art models with substantially improved computational efficiency. In a zero-shot setting, GENERator achieves competitive variant effect prediction performance relative to alignment-based methods, while remaining fully alignment-free and broadly applicable across species. With task-specific fine-tuning, the model attains leading performance on established genomic benchmarks. We further demonstrate practical generative applications. GENERator can generate protein-coding DNA sequences that translate into structurally plausible proteins and, through a prompt-guided design framework, design cis-regulatory elements with targeted activity profiles, including synthetic super-enhancers validated by high-throughput UMI-STARR-seq assays. Together, these results establish GENERator as an efficient and biologically grounded framework for genomic interpretation and programmable sequence design. Code and supplementary resources are available at https://github.com/GenerTeam/GENERator.

---

# Is it Possible to Modify Text to a Target Readability Level? An Initial Investigation Using Zero-Shot Large Language Models

DOI: —
Ano: 2023
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #43

Text simplification is a common task where the text is adapted to make it easier to understand. Similarly, text elaboration can make a passage more sophisticated, offering a method to control the complexity of reading comprehension tests. However, text simplification and elaboration tasks are limited to only relatively alter the readability of texts. It is useful to directly modify the readability of any text to an absolute target readability level to cater to a diverse audience. Ideally, the readability of readability-controlled generated text should be independent of the source text. Therefore, we propose a novel readability-controlled text modification task. The task requires the generation of 8 versions at various target readability levels for each input text. We introduce novel readability-controlled text modification metrics. The baselines for this task use ChatGPT and Llama-2, with an extension approach introducing a two-step process (generating paraphrases by passing through the language model twice). The zero-shot approaches are able to push the readability of the paraphrases in the desired direction but the final readability remains correlated with the original text's readability. We also find greater drops in semantic and lexical similarity between the source and target texts with greater shifts in the readability.

---

# FEALLM: Advancing Facial Emotion Analysis in Multimodal Large Language Models with Emotional Synergy and Reasoning

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #48

Facial Emotion Analysis (FEA) plays a crucial role in visual affective computing, aiming to infer a person's emotional state based on facial data. Scientifically, facial expressions (FEs) result from the coordinated movement of facial muscles, which can be decomposed into specific action units (AUs) that provide detailed emotional insights. However, traditional methods often struggle with limited interpretability, constrained generalization and reasoning abilities. Recently, Multimodal Large Language Models (MLLMs) have shown exceptional performance in various visual tasks, while they still face significant challenges in FEA due to the lack of specialized datasets and their inability to capture the intricate relationships between FEs and AUs. To address these issues, we introduce a novel FEA Instruction Dataset that provides accurate and aligned FE and AU descriptions and establishes causal reasoning relationships between them, followed by constructing a new benchmark, FEABench. Moreover, we propose FEALLM, a novel MLLM architecture designed to capture more detailed facial information, enhancing its capability in FEA tasks. Our model demonstrates strong performance on FEABench and impressive generalization capability through zero-shot evaluation on various datasets, including RAF-DB, AffectNet, BP4D, and DISFA, showcasing its robustness and effectiveness in FEA tasks. The dataset and code will be available at https://github.com/953206211/FEALLM.

---

# Knowledge Reasoning Language Model: Unifying Knowledge and Language for Inductive Knowledge Graph Reasoning

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #52

Inductive Knowledge Graph Reasoning (KGR) aims to discover facts in open-domain KGs containing unknown entities and relations, which poses a challenge for KGR models in comprehending uncertain KG components. Existing studies have proposed Knowledge Graph Foundation Models (KGFMs) that learn structural invariances across KGs to handle this uncertainty. Recently, Large Language Models (LLMs) have demonstrated strong capabilities for open-domain knowledge reasoning. As a result, the latest research has focused on LLM-based KGFMs that integrate LLM knowledge with KG context for inductive KGR. However, the intrinsic knowledge of LLMs may be overshadowed by sparse KG context, leading to LLM knowledge distortion, which can cause irreversible damage to model reasoning. Moreover, existing LLM-based KGR methods still struggle to fully constrain generative hallucinations in LLMs, severely limiting the credibility of reasoning results. To address these limitations, we propose a Knowledge Reasoning Language Model (KRLM) that achieves unified coordination between LLM knowledge and KG context throughout the KGR process. Specifically, we design a Knowledge Reasoning Language (KRL) instruction format and a KRL tokenizer to align LLM knowledge with KG representations. Then, we propose a KRL attention layer that coordinates intrinsic LLM knowledge with additional KG context through a dynamic knowledge memory mechanism. Finally, a structure-aware next-entity predictor is proposed, which strictly constrains the reasoning results within a trustworthy knowledge domain. Extensive experimental results on 25 real-world inductive KGR datasets demonstrate the significant superiority of the proposed KRLM\footnote{Our source codes are available at https://anonymous.4open.science/r/KRLM-EA36 in both zero-shot reasoning and fine-tuning scenarios.

---

# Trust, But Verify: An Empirical Evaluation of AI-Generated Code for SDN Controllers

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #65

Generative Artificial Intelligence (AI) tools have been used to generate human-like content across multiple domains (e.g., sound, image, text, and programming). However, their reliability in terms of correctness and functionality in novel contexts such as programmable networks remains unclear. Hence, this paper presents an empirical evaluation of the source code of a POX controller generated by different AI tools, namely ChatGPT, Copilot, DeepSeek, and BlackBox.ai. To evaluate such a code, three networking tasks of increasing complexity were defined and for each task, zero-shot and few-shot prompting techniques were input to the tools. Next, the output code was tested in emulated network topologies with Mininet and analyzed according to functionality, correctness, and the need for manual fixes. Results show that all evaluated models can produce functional controllers. However, ChatGPT and DeepSeek exhibited higher consistency and code quality, while Copilot and BlackBox.ai required more adjustments.

---

# SEER: Enhancing Chain-of-Thought Code Generation through Self-Exploring Deep Reasoning

DOI: —
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #67

Code generation, the task of creating executable programs from natural language requirements, has recently seen tremendous advances through Chain-of-Thought (CoT) reasoning, which enables Large Language Models (LLMs) to develop high-level reasoning plans before writing code. Recent research has proposed various methods to enhance models' CoT reasoning for code generation such as prompt engineering and supervised fine-tuning. However, existing approaches still face three critical limitations: (1) limited exploration of diverse reasoning paths, which constrains generalization across various programming scenarios, (2) lack of quality assessment for intermediate reasoning steps, which hampers the reliability of the generated plans and code, and (3) the potential negative impact of "overthinking", potentially leading to unnecessarily complex and incorrect solutions. To address these limitations, we frame CoT code generation as a decision making problem and present SEER, a SElf-Exploring deep Reasoning framework that enables accurate and adaptive reasoning for code generation. SEER introduces three key components: (1) Diverse reasoning path exploration, which aims at exploring diverse reasoning paths and annotating intermediate steps without relying on manual experts or closed-source proprietary models; (2) Reasoning quality-aware model training, which trains a policy model for generating candidate reasoning steps and a value model for assessing their quality; and (3) Adaptive CoT reasoning, which dynamically switches between direct generation and step-by-step reasoning for different problems.

---

# Multi-Agentic AI for Conflict-Aware rApp Policy Orchestration in Open RAN

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #69

Open Radio Access Network (RAN) enables flexible, AI-driven control of mobile networks through disaggregated, multi-vendor components. In this architecture, xApps handle real-time functions, whereas rApps in the non-real-time controller generate strategic policies. However, current rApp development remains largely manual, brittle, and poorly scalable as xApp diversity proliferates. In this work, we propose a Multi-Agentic AI framework to automate rApp policy generation and orchestration. The architecture integrates three specialized large language model (LLM)-based agents, Perception, Reasoning, and Refinement, supported by retrieval-augmented generation (RAG) and memory-based analogical reasoning. These agents collectively analyze potential conflicts, synthesize intent-aligned control pipelines, and incrementally refine deployment decisions. Experiments across diverse deployment scenarios demonstrate that the proposed system achieves over 70% improvement in deployment accuracy and 95% reduction in reasoning cost compared to baseline methods, while maintaining zero-shot generalization to unseen intents. These results establish a scalable and conflict-aware solution for fully autonomous, zero-touch rApp orchestration in Open RAN.

---

# The Powerless Noise: How Experimental Settings Shape the Reported Power of Noise

DOI: 10.1145/3805712.3808556
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #70

Recent work has suggested that adding irrelevant documents to the input of retrieval-augmented generation (RAG) systems can improve question-answering performance, a phenomenon referred to as the Power of Noise. This motivated investigations into the role of noise in information retrieval. In this paper, we reproduce the main findings of Cuconasu et al. and evaluate the robustness of the effect under extended experimental settings. We first confirm that the phenomenon holds under the original setup, which uses earlier-generation LLMs, restrictive prompting and constrained decoding settings. We subsequently introduce a series of extensions to investigate the underlying causes of the noise effect, examining the authors' original design choices including the use of different models, instruction prompting, and relaxed output length constraints. Across these ablations, the Power-of-Noise pattern proves highly sensitive to inference configuration: it can appear, weaken, or disappear under small changes to prompt formulation and decoding limits. Combined with our error analysis, which shows substantial contributions from truncation and malformed generations, this variance indicates that the original effect cannot be robustly confirmed as a general benefit of noisy retrieval under these experimental conditions. More broadly, our work highlights the importance of carefully scrutinizing inference design in retrieval-augmented generation systems. Our code is available at https://github.com/ina0105/The-Power-of-Noise-Reproduction.

---

# Different Teachers, Different Capabilities: Sub-1B On-Device Distillation for Structured Text Enrichment

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #73

High-volume structured extraction pays a large model's latency on every item, so distilling the task into a small on-device model is attractive: comparable output at a fraction of the time and cost. We measure what that distillation actually delivers, per sub-task. Each news article is mapped to one JSON object with a short summary and five categorical labels. We distill an 8B reasoning teacher (deepseek-r1:8b) into a 0.6B student (Qwen3-0.6B; QLoRA, three seeds), and add two teacher controls: a same-size non-reasoning teacher and a larger managed pipeline. A blinded, reference-free, three-judge panel scores every arm against the full article, alongside two non-distillation baselines, few-shot prompting and constrained decoding. The student runs at about 0.8 s per article against the teacher's 39 s, and recovers 58% of the base-to-teacher gap on summary quality, beating its primary baseline (constrained decoding) by +16.8 points and few-shot prompting by a secondary +4.9. A same-size non-reasoning teacher trains a student no better than the untuned base, so the summary gain follows from the teacher's reasoning nature rather than its scale. Capabilities then split by teacher: the reasoning teacher transfers writing quality and the managed pipeline transfers label diversity, while a same-size instruction teacher's students stay more grounded on the 22 short, thin-source articles in the 93-item test set (74 versus 55 faithful), where the reasoning-lineage student fabricates. That grounding difference is a consistent ordering rather than a significant aggregate effect, and the subgroup is small, so we report it as a direction. Because no single engine wins every field, the deliverable is a per-field routing map for on-device enrichment.

---

# IndexTTS 2.5 Technical Report

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #75

In prior work, we introduced IndexTTS 2, a zero-shot neural text-to-speech foundation model comprising two core components: a transformer-based Text-to-Semantic (T2S) module and a non-autoregressive Semantic-to-Mel (S2M) module, which together enable faithful emotion replication and establish the first autoregressive duration-controllable generative paradigm. Building upon this, we present IndexTTS 2.5, which significantly enhances multilingual coverage, inference speed, and overall synthesis quality through four key improvements: 1) Semantic Codec Compression: we reduce the semantic codec frame rate from 50 Hz to 25 Hz, halving sequence length and substantially lowering both training and inference costs; 2) Architectural Upgrade: we replace the U-DiT-based backbone of the S2M module with a more efficient Zipformer-based modeling architecture, achieving notable parameter reduction and faster mel-spectrogram generation; 3) Multilingual Extension: We propose three explicit cross-lingual modeling strategies, boundary-aware alignment, token-level concatenation, and instruction-guided generation, establishing practical design principles for zero-shot multilingual emotional TTS that supports Chinese, English, Japanese, and Spanish, and enables robust emotion transfer even without target-language emotional training data; 4) Reinforcement Learning Optimization: we apply GRPO in post-training of the T2S module, improving pronunciation accuracy and natrualness. Experiments show that IndexTTS 2.5 not only supports broader language coverage but also replicates emotional prosody in unseen languages under the same zero-shot setting. IndexTTS 2.5 achieves a 2.28 times improvement in RTF while maintaining comparable WER and speaker similarity to IndexTTS 2.

---

# VIA: Visual Interface Agent for Robot Control

DOI: —
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: arXiv
RRI: #78

Robot manipulation is a complex task that requires visual understanding, physical reasoning, planning, and closed-loop control. General-purpose foundation models (FMs) have grown remarkably capable of some of these, especially vision and reasoning. To leverage this for generalist robot policies, current methods typically involve converting existing FMs into vision-language-action (VLA) models by fine-tuning on robot data to output low-level actions. However, VLAs are often orders of magnitude smaller than frontier FMs given the limited data and compute available for fine-tuning, which in turn limits their general capability. Inspired by the growing ability of FMs to operate software through visual interfaces, we ask whether that same competence suffices to control a robot. We present VIA (Visual Interface Agent for robot control), a framework that recasts robot control as an agentic task: an off-the-shelf FM-powered agent drives a manipulator through a browser-based 3D interface by taking screenshots, issuing intuitive commands, observing the outcome, and adjusting. The agent receives no robot-specific fine-tuning and no access to privileged state information: it perceives visual input and acts through a small set of general tools. VIA inherits the agent's general reasoning, closed-loop error recovery, and ability to plan and re-plan from what it observes. It solves a diverse suite of tabletop manipulation tasks zero-shot with both Claude Code and Codex. With the strongest model (Fable 5) it achieves 96.7% success on three LIBERO-Goal tasks and 100% on a long-horizon rainbow assembly task. Performance improves with the scale and strength of the underlying model. These results suggest that frontier agents already possess skills that transfer directly to robot control given the right interface: your coding or computer-use agent is, in a sense, secretly a robot-control agent.

---

# An Investigation of Prompt Engineering and Fine-Tuning Using Quantized Low Rank Adaptation for Medical Calculator Implementation on MedCalc-Bench

DOI: 10.1109/SIST61674.2026.11596307
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #87

Providing quality healthcare is a key goal of governments worldwide. There are enormous challenges, including the high cost of medical care, timeliness of treatments, and the optimization of available resources. The use of AI is emerging as a key technology to address some of these challenges. We focus on the use of clinical calculators, which are a key component in decision-support systems. We aim to automatically compute patient vitals from unstructured clinical notes to enhance workflow efficiency. However, this task remains an open challenge for language models. We investigate two complementary strategies for medical score calculation using the Qwen3-4B-Instruct small language model on eight rule-based calculators from the MedCalc-Bench benchmark: CHA2DS2-VASc, Centor, HEART, PERC, and SIRS. First, we develop a two-stage structured prompt that decomposes each task into entity extraction followed by rule application. Second, we apply supervised fine-tuning with QLoRA (4-bit NormalFloat quantization and low-rank adapters), attaining 60.0% accuracy on the same evaluation set. Comparative analysis reveals that structured prompting outperforms QLoRA fine-tuning on this subset, while fine-tuning yields superior format adherence and reduced hallucination. We also found that roughly half the SIRS test cases in MedCalc-Bench have incorrect labels, artificially limiting how well any model can perform. We determined that our model performance is insensitive to LoRA rank and learning rate within tested ranges. These findings offer practical guidance for deploying small language models in resource-constrained clinical AI settings.

---

# CA-CoCon: An improved self-supervised method for controlled text generation using cross-activation attention mechanism

DOI: 10.1109/CVIDL62147.2024.10603799
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #89

The widespread application of pre-trained large models in the field of natural language generation has facilitated the development of models capable of generating fluent textual content. While conventional text generation models often struggle to effectively control text content at the sentence level, self-supervised learning models like CoCon offer finer-grained control over generated text at the word and phrase levels. Although the text generated by CoCon tends to adhere closely to the given topic, it still exhibits deviations from human communication norms, lacking in textual diversity. Addressing these issues, we propose a novel approach based on the multi-granularity controllable text generation model, CoCon, termed as Cross-Activation (CA)-CoCon. This approach assists the model in capturing nonlinear features between input text and target content more effectively, thus facilitating the seamless integration of target content into the generated text. The proposed CA-CoCon model outperforms the untreated CoCon model across multiple thematic and emotional attribute categories, yielding text outputs that align more closely with human communication norms and exhibit enhanced textual diversity.

---

# Large Language Model Assistant for Updating and Managing Asset Administration Shells

DOI: —
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #91

Natural-language access to Asset Administration Shell (AAS) repositories could lower the barrier for interaction with standardized digital twins, especially for users who are unfamiliar with AAS structures and APIs. While prior work has explored AI support for the AAS lifecycle through the generation or semantic mapping of AAS content, empirical studies on local large language models (LLMs) for direct interaction with deployed AAS repositories remain limited, especially in systematically evaluated staged settings. This paper presents a multi-stage assistant for natural-language-based management of AAS data hosted in Eclipse BaSyx. The approach decomposes the task into multi-staged processing steps for shell identification, deeper submodel or element-level operation generation, and user-facing response formulation. To improve robustness of machine-readable intermediate outputs, the system employs grammar-constrained decoding and prompt-based conditioning with zero-shot and few-shot configurations. The evaluation compares three quantized models in the 8 billion parameter range: Llama 3.1, DeepSeek R1, and Qwen 3, on a task set covering retrieval, modification, and general interaction scenarios across multiple query formulations. The results show that few-shot prompting is essential for reliable performance, whereas zero-shot prompting is insufficient for many structured interaction tasks. The best configuration, based on Llama 3.1 8B, achieves an effective success rate of up to 81%, while short and ambiguous queries remain challenging. These findings indicate that small local LLMs can provide a feasible privacy-preserving interface for structured AAS repository interaction when combined with multi-stage task decomposition and constrained decoding.

---

# ServeXcel: Trust-Aware Retrieval-Augmented Generation for Document-Intensive Customer Service in Digital Banking

DOI: 10.1109/ICMISI69868.2026.11584039
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: IEEE Xplore
RRI: #92

The accelerated digital transformation of banking has fundamentally altered how customers engage with financial institutions, placing unprecedented pressure on customer service systems to deliver fast, accurate, and contextually grounded responses. While recent advances in large language models have enabled conversational interfaces capable of fluent natural language interaction, their direct deployment in regulated financial environments remains constrained by hallucination risk, lack of source traceability, and limited alignment with institutional knowledge bases. This paper presents ServeXcel, a trust-aware Retrieval-Augmented Generation (RAG) architecture designed explicitly for document-intensive customer service scenarios in digital banking. Unlike conventional chatbot systems, ServeXcel integrates dense semantic retrieval over verified internal documents with controlled generation mechanisms to ensure factual accuracy, explainability, and regulatory compatibility. The proposed architecture is implemented using an offline, privacy-preserving pipeline that combines vector indexing, lightweight transformer embeddings, and quantized generative models, enabling deployment in resource-constrained and compliance-sensitive environments. Empirical evaluation using real banking documentation demonstrates that the proposed system improves retrieval accuracy, reduces hallucination rates, and enhances user trust while maintaining low response latency. To enhance generalizability, the proposed framework is further analyzed with respect to scalability considerations and multiturn conversational extensions. Preliminary insights indicate that ServeXcel maintains robust performance under increased corpus sizes and conversational depth, supporting its applicability in real-world digital banking environments. The results indicate that trust-aware RAG architectures such as ServeXcel offer a viable and scalable pathway toward dependable AI-driven customer service in modern financial institutions.

---

# Enhancing Financial Reasoning via Program-of-Thought Learning

DOI: 10.1007/978-981-92-1468-6_25
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #108

Large Language Models (LLMs) have achieved remarkable progress in reasoning capabilities, yet financial reasoning remains a significant challenge due to the demand for both numerical reasoning and understanding of domain-specific terminology. While prompt engineering techniques have improved reasoning performance, they often suffer from inconsistency, sensitivity to example selection, and limited generalizability. Consequently, supervised fine-tuning (SFT) and reinforcement learning (RL) are widely adopted to post-train LLMs using chain-of-thought to improve financial reasoning. A fundamental question remains: how can we more effectively represent and measure the reasoning steps and enable models to learn more efficiently, particularly for numerically intensive financial reasoning tasks? In this study, we propose a learning framework that enhances financial reasoning in LLMs through a novel program-of-thought (PoT) paradigm. PoT structures reasoning as step-by-step programmatic operations, such as code, pseudo-code, formulas, or symbolic steps, offering greater clarity, consistency, and executability. Our framework begins with SFT followed by RL using Group Relative Policy Optimization (GRPO), with a reward designed to balance accuracy, reasoning steps, and format adherence. Experiments on the FinQA benchmark demonstrate that our method outperforms state-of-the-art reasoning models. Our findings suggest that PoT learning is more effective than long natural-language CoT in the FinQA task, offering a promising direction for post-training LLMs for complex, domain-specific reasoning tasks. © The Author(s), under exclusive license to Springer Nature Singapore Pte Ltd. 2026.

---

# Exploring a Generative Programming Teaching Model for Innovation and Entrepreneurship: Integrating Computational Vouchers, Internship Opportunities and Roadshow Mechanisms

DOI: 10.1007/978-3-032-30826-9_26
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #120

Large language models and AI coding tools have changed the setting in which introductory programming is taught. Students can now obtain code, explanations, and debugging suggestions from AI systems with very little effort. This does not make foundational programming less important. It changes what foundational ability now includes. Alongside syntax and semantics, students need to learn how to specify a problem, break it into manageable steps, evaluate generated code, and revise solutions through testing and verification. This paper describes a task-driven, AI-assisted course design developed for the Fundamentals of Computer Programming course at Tsinghua University. The design is implemented through a two-track prompt-only competition. One track uses a shared benchmark task and executable judge-based evaluation. The other uses open-ended project work assessed through reproducibility, documentation, and evidence-chain review. The course also requires prompt records, seed- and parameter-based reproducibility, and explicit checks for verification, privacy, and responsible AI use. In addition, participation is linked to computing vouchers, internship opportunities, and roadshow mechanisms. The contribution of the study lies in the design of a concrete teaching setting in which AI-assisted programming becomes teachable, observable, and assessable. Rather than treating AI as a simple code-generation aid, the proposed design organizes learning around controlled generation, executable validation, and documented revision. The paper therefore offers a concrete course design that may be useful for introductory programming courses working under AI-supported conditions. © The Author(s), under exclusive license to Springer Nature Switzerland AG 2026.

---

# The Hidden Cost of Structure: How Constrained Decoding Affects Language Model Performance

DOI: 10.26615/978-954-452-098-4-124
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #121

Large Language Models excel at generating fluent text, but real-world applications increasingly demand structured outputs like JSON that can be programmatically processed. While prior work examines either task performance or format compliance in isolation, we investigate their interaction through comprehensive experiments across 11 models and multiple benchmarks. We uncover a fundamental divergence between base and instruction-tuned models under structural constraints. Base models often benefit from constrained decoding, producing more precise outputs, while instruction-tuned models frequently suffer performance degradation on generation tasks despite maintaining stability on classification tasks. Our log probability analysis reveals the underlying mechanism: constrained decoding forces models away from their preferred natural language patterns into lower-confidence structured alternatives. We demonstrate that successful constrained generation requires both adapted prompts and sufficient few-shot examples, with constrained models showing steeper performance gains from additional demonstrations compared to unconstrained generation. Notably, we find that base model performance under constraints can serve as an early indicator of post-training structured output capabilities, offering a practical evaluation tool for model development. These findings suggest that current instruction-tuning practices may inadvertently reduce models’ structured output capabilities and highlight the need for training-time integration of structural constraints in future model development. © 2025 Incoma Ltd. All rights reserved.

---

# MKTE at ATE-IT: CRF-Based Term Extraction for Italian Waste Management Documents

DOI: —
Ano: 2026
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Scopus
RRI: #134

This paper presents a Conditional Random Fields (CRF) sequence-labelling system for sentence-level Automatic Terminology Extraction in the ATE-IT shared task at EVALITA 2026, targeting Italian municipal waste-management documents. The system models term spans using linguistically informed features, including POS tags, lemmas, dependency relations, and morphological patterns, and applies task-specific post-processing to satisfy lowercasing, sentence-level de-duplication, and non-nested output constraints. On the official test set, our submission achieves micro-F1 scores of 0.519 and 0.529, corresponding to ranks 5 and 3 across submitted runs, and yields higher precision than the baseline. However, recall remains comparatively lower, and we observe a substantial gap between training and test performance, suggesting overfitting and limited generalization to unseen documents. We also find only modest gains over a zero-shot large language model approach, indicating that large pre-trained models may encode substantial implicit terminology knowledge even without task-specific supervision. We conclude by outlining directions for improving robustness, including richer semantic representations, data augmentation, and ensemble strategies to reduce the generalization gap. © 2026 Copyright for this paper by its authors.

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

# Rx-LLM: a benchmarking suite to evaluate safe large language model performance for medication-related tasks.

DOI: 10.64898/2025.12.01.25341004
Ano: 2025
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #149

For large language models (LLMs) to reach their potential as information technology tools that make medication use safer, clinically relevant benchmarks capable of automated grading and designed specifically to measure the performance of LLMs for medication tasks are required. The purpose of this study was to design a suite of benchmarking tests reflective of Comprehensive Medication Management (CMM; the standard of care for medication optimization) and quantify the baseline performance of the latest LLMs. We established six benchmarks representing critical stages of the CMM process: drug formulation matching, drug order (sig) generation, drug route matching, drug-drug interaction identification, renal dose identification, and drug-indication matching. For each benchmark, we curated a clinician-annotated dataset comprising 250 standardized input-output pairs including both inpatient and outpatient medications. We evaluated the clinical knowledge retrieval capabilities of three LLMs: GPT-4o-mini, MedGemma-27B, and LLaMA3-70B. We employed a zero-shot prompting strategy, excluding in-context examples, to assess the models' internal clinical knowledge rather than their few-shot learning potential. To check reliability, each model was run three times using a temperature of 0.7 (a mid-range value of an LLM setting controlling text generation randomness). Performance was assessed using task-specific evaluation metrics including precision (positive predictive value), recall (sensitivity), F1-score, accuracy, and correctness consistency across trials. Across six benchmarks, LLaMA3-70B demonstrated the highest performance in four tasks: drug-formulation matching (F1, 54.0% [95 CI: 50.1-58]), drug-order generation (accuracy, 88.0%), drug-route identification (F1, 74.3% [95 CI: 71-78]), and drug-indication identification (accuracy, 97.6% [95 CI: 95.6-99.2]). In the drug-drug interaction task, GPT-4o-mini achieved the highest overall accuracy (70.4% [95 CI: 64.8-75.7]). For renal dose-adjustment identification, GPT-4o-mini demonstrated the highest F1 score (83.3% [95 CI: 77.6-88]). Correctness-consistency scores ranged from 8.0% to 97.6% across benchmarks, with no model exhibiting uniformly superior consistency. Model performance varied substantially across medication-related tasks. LLaMA3-70B demonstrated promising baseline performance in tasks involving formulation, ordering, route, and indication. GPT-4o-mini showed potential advantages in drug-drug interaction detection and renal dose adjustment. These findings underscore the need for task-specific evaluation when deploying models for medication-focused clinical decision support.

---

# Genre Classification from Album Cover Art Using Deep Learning and Large Language Models

DOI: 10.82308/56009
Ano: 2026
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: Lens.org
RRI: #161

Music genre classification is a foundational task in Music Information Retrieval (MIR) that is essential for modern recommendation systems and content organization. Music is inherently multimodal, and album cover art serves as a vital visual representation that encapsulates an album’s mood, themes, and stylistic identity, offering valuable cues for genre inference. This thesis investigates the viability of album cover art as a standalone modality for genre classification, addressing limitations inherent in audio-only approaches, such as the dependence on recordings and challenges with dataset generalization.This research addresses the gap in existing literature by leveraging state-of-the-art machine learning techniques and benchmarking two distinct approaches: supervised deep learning and zero-shot classification. For the supervised approach, four Convolutional Neural Network (CNN) architectures (ResNet50, VGG16, MobileNetV2, and InceptionV3) were evaluated using transfer learning, trained on a large, balanced dataset. A dataset was constructed by collecting over 128,000 album covers from the MusicBrainz Cover Art Archive and mapping genre annotations from the AcousticBrainz Genre Dataset (Discogs labels). The CNN models were optimized using Optuna hyperparameter tuning.For the second approach, this study is among the first in this domain to investigate the application of a multimodal Large Language Model (LLM), gpt-4o-mini, for zero-shot classification of album cover art. This method utilized structured prompt engineering and constrained decoding to leverage the LLM’s vast semantic knowledge and visual-semantic reasoning capabilities.The results demonstrated a clear and significant advantage for the LLM-based approach over the traditional deep learning models. On the AcousticBrainz Genre Dataset, the best CNN model (VGG16) achieved an accuracy of 36% across all classes, whereas the zero-shot LLM achieved 68% accuracy. This disparity was even more pronounced on the MillionSong Dataset (MSD-I), where the LLM achieved 73% weighted accuracy, compared to the best CNN’s 26%. This superior performance is largely attributed to the LLM’s ability to bridge visual and textual domains, integrating contextual and cultural knowledge beyond the purely data-driven feature extraction of CNNs. Furthermore, the LLM demonstrated strong generalization capabilities, achieving a weighted accuracy of 59% on unseen, new cover art released after the reported knowledge cut-off date of the LLM.This thesis contributes to MIR by confirming that visual features alone are a reliable predictor of music genre and by providing a crucial comparative evaluation highlighting the power of knowledge-driven, zero-shot LLM inference over purely data-driven supervised models for artistic image classification. The findings suggest that integrating LLMs into digital music libraries can enhance genre tagging and music recommendation systems, offering greater scalability and adaptability to emerging music styles.

---

# Empowering natural language processing in low-resource regimes

DOI: 10.32657/10356/182796
Ano: 2025
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: Lens.org
RRI: #169

As a vital subfield of artificial intelligence (AI), natural language processing (NLP) strives to enable computers to understand, process, and analyze text as humans do. NLP has a broad range of applications, including text classification, information extraction, and chatbot dialogue systems. However, most NLP models demand substantial amounts of training data, which is often labor-intensive and expensive to collect and annotate. This issue, known as the low-resource NLP challenge, is defined as the lack of sufficient data and is considered one of the most critical obstacles in NLP. To tackle the low-resource NLP challenge, existing solutions either expand the training data or reduce data requirements by enhancing the training efficiency. Techniques like data augmentation, distant supervision, and semi-supervised learning generate synthetic data to increase the training set, enabling NLP models to achieve greater generalization across various NLP tasks. Sequential transfer learning methods, including fine-tuning and prompt-based learning, substantially boost the learned text representations with limited data, thereby reducing the overall data demand. These approaches employ lightweight strategies to add adaptation modules or adjust the parameters of pre-trained language models (PLMs), effectively tailoring powerful PLMs to specific downstream NLP tasks. Despite their success, most of these solutions overlook interpretability in their development, failing to create more targeted approaches for NLP models. The first category of interpretability is local explanations, which elucidate the model's decision-making process for individual inputs. By understanding how different input words influence model outputs, we can design more efficient strategies for utilizing and processing limited training data. The second category is global explanations, which analyze how the model's overall structure, weights, and parameters affect its prediction process. Leveraging these explanations enables us to devise better strategies for adapting PLMs to NLP tasks, thereby reducing the data requirements even further. However, effectively integrating interpretability into the development of low-resource NLP solutions remains an unresolved research question. This thesis aims to integrate interpretability into the design of more targeted methods to address the low-resource challenge. By leveraging both local and global explanations, we develop efficient strategies for data augmentation, fine-tuning, and prompt-based learning across various natural language understanding (NLU) and natural language generation (NLG) tasks. Specifically: Tailored Text Augmentation Using Local Explanations. We employ local explanations, such as the word's importance and discriminative power for the prediction, to tailor data augmentation operations for different word types. Discriminative words are used to introduce more task-oriented knowledge into synthetic data, while irrelevant words are controlled to be evenly distributed in synthetic data for low-resource sentiment analysis. Boosting Fine-Tuning with Knowledge-Driven Interpretability. We utilize external knowledge and local explanations of word importance to create text-saliency graphs for each input text. These graphs are encoded and combined with the original text representations to enhance the discriminative power of text representation learning, significantly improving model performance in low-resource hierarchical text classification (HTC). Enhanced Input Saliency for Prompt Manipulation. We develop a simple yet efficient local explanation method that leverages token distribution dynamics (TDD) to elucidate the prompt’s influence on large language model (LLM) outputs. Using these reliable local explanations derived from input saliency, we manipulate prompts by identifying and modifying keywords in input prompts for zero-shot controllable text generation (CTG). Learning-Free Text Generation with Global Interpretability. We investigate global explanations, focusing on how the weights of feed-forward network (FFN) modules in LLMs impact their outputs. We then establish control centers using these FFNs and adaptively update their weights for CTG. Remarkably, our proposed method does not require any training data or learning process, significantly mitigating the low-resource challenge.

---

# Closed-Source vs. Open-Weights Language Models: Accuracy, Stability, and Deployment Trade-Offs in Educational Assessment (GPT-4o vs. LLaMA 3.1)

DOI: 10.30880/jscdm.2026.07.02.005
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #182

Large language models (LLMs) are increasingly used to support educational assessment, yet institutional adoption requires balancing performance with governance constraints related to auditability, data control, and deployability. We compare a closed-source model (GPT-4o) and an open-weights model (LLaMA 3.1) on two expert validated assessment formats across five academic domains (Science, History, Literature, Technology, and Social Studies). Experiment 1 evaluates multiple choice question (MCQ) option selection using 148 items, five prompting strategies (Raw, Brief Instruction, Long Instruction, Chain-of-Thought, and Question-Answer Prompt Generation), and five independent repetitions per condition (7,400 total model calls) to estimate both accuracy and run-to-run stability under a strict A to E output constraint. Experiment 2 evaluates 147 one sentence short answer items under a fixed instruction prompt. In the multiple choice questions (MCQs), the accuracy and stability of the results for GPT-4o were higher compared to those of LLaMA 3.1, and the incorporation of the additional prompt structure was associated with higher stability compared to the average improvement in correctness. In the short answer questions, the performance of GPT-4o was slightly higher compared to that of LLaMA 3.1 for ROUGE-L and METEOR, and these results mostly corresponded to the results obtained for the semantic similarity questions and the evaluation rubric. The results of the study are important for understanding the accuracy-stability trade-off for the two language generators and for supporting the evaluation approach that considers the correctness of the results for MCQs, their stability for multiple runs, and the validation of the results for short answer questions using the evaluation rubric and the results for the semantic similarity questions.

---

# LARA: Learned Adaptive Recombined Alignments, a Certifying Foundation Model for Petri Net Trace Alignment

DOI: 10.20944/preprints202607.0536.v1
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #195

Alignments explain, event by event, how an observed trace deviates from a process model. Computing an optimal alignment, however, requires exact shortest-path search over a synchronous product, which degrades with concurrency, loops, duplicate labels, and invisible transitions, precisely the ingredients of real discovered models. Purely learned aligners are fast but untrustworthy: their output may be illegal or silently suboptimal. This paper introduces LARA (Learned Adaptive Recombined Alignments), a hybrid system in which a neural model proposes and an exact layer verifies. The neural model is a small foundation model for alignment: trained once, offline, on synthetic data, it is vocabulary-free and applies to any net and any log without per-log training or configuration. Its scores drive a constrained decoder, and exact replay checks every candidate, so the output is always a legal alignment with a known cost; on demand, the exact backend upgrades it to a certified optimal one. In the assessment, every produced alignment is legal, and the large majority attains the exact optimal cost. A guidance ablation attributes the learned contribution specifically to duplicate-label resolution, the sub-problem where purely structural heuristics are blind. Legality transfers zero-shot to unseen net families and to real-life event logs, and the learned fast path overtakes exact search on larger synthetic nets and on a real discovered model dominated by invisible transitions.

---

# Enhancing Best-of-N Decoding by Speculative Rejection and Self-Certainty

DOI: 10.5753/eramiars.2025.16649
Ano: 2025
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Lens.org
RRI: #196

Controllable text generation techniques such as fine-tuning, reinforcement learning, and prompt engineering have significant potential to enhance reasoning, alignment, and efficiency in Large Language Models. However, these methods often struggle with memory management, generalization across diverse language tasks, and score function design. In contrast, enhancing the decoding process has proven to be an effective way to control generation without requiring additional training or external tools. This work proposes an improved parallel decoding strategy that not only alleviates resource requirements but also effectively leverages its guiding reward function.

---

# An adversarial testing framework for AI-driven task routing systems

DOI: 10.31649/1681-7893-2026-51-1-374-381
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #198

The paper presents an adversarial testing methodology for evaluating AI-driven task routing systems. The methodology defines structured attack scenarios and strict output constraints to measure resistance against unauthorized data disclosure. To validate suggested approach, an AI-based routing solution implemented using an Salesforce Agentforce Prompt Template powered by ChatGPT 5 was tested in a controlled environment. It has been proven that using a structured approach to testing can reduce the risk of data leakage in AI-based decision support systems.

---

# ProtGPT3: an Open-source family of Promptable and Aligned Protein Language Models

DOI: 10.64898/2026.06.04.730041
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #206

Abstract Generative protein language models (pLMs) enable exploration of vast sequence spaces for protein design, but reliably controlling generation toward desired functional families remains challenging. While protein generation has broadly followed trends in NLP, two directions remain underexplored: alignment methods that optimize model behavior toward design objectives, and prompting-based control at inference time without fine-tuning. We introduce ProtGPT3, an open-source family of protein language models spanning 112M to 10B parameters and integrated with the Hugging Face ecosystem. The suite includes both single-sequence and multiple sequence alignment (MSA)-promptable models, enabling flexible conditioning for generation. Across model scales and protein families, we systematically compare supervised fine-tuning and few-shot prompting using homologous sequences. Analogous to how large language models (LLMs) are routinely aligned with user intent, we study post-training alignment in single-sequence models using sequence-complexity and structure-confidence metrics across the proteome. We find that alignment reduces low-complexity generations while preserving sequence diversity. Furthermore, we show that few-shot prompting is a competitive and more scalable alternative to supervised fine-tuning for controlled generation. In a low-data defluorinase case study, ProtGPT3-MSA achieved higher computational success rates than fine-tuned baselines and produced designs that were soluble and expressed following experimental validation. Finally, we explore the potential of inference-time compute in MSA models by introducing a homolog-based Feynman–Kac inference procedure for steering protein generation toward desired targets. All models are publicly available at https://huggingface.co/collections/AI4PD/protgpt3-family .

---

# Teaching Model-Driven Low-Code Development Platforms

DOI: 10.1145/3652620.3687778
Ano: 2024
Tipo de documento: Não identificado
Base onde foi encontrado: Lens.org
RRI: #220

Low-code development platforms (LCDPs) are becoming increasingly important in industry, which confronts us in academic teaching with the challenge of educating students in the basic principles, critical engagement, and evaluation of LCDPs. This leads us to the question, how to teach the usage of different LCDPs during an university course. The short time frame of university-level courses makes it challenging to teach more than only one LCDP. In our teaching approach, students use two different LCDPs and create a web-application with both of them. Firstly, we require the students to define a target application with common modeling languages, next they use the first LCDP, at about half the time they switch to the second LCDP and present their findings of the differences in methodology and development processes at the end. We discuss this approach, show survey results from the participants, and explain lessons learned. This concept allows students critical engagement with LCDPs and model-driven software engineering. Supervisors get an insight into the learnability of each LCDP and how novices adapt to different domain-specific languages and their notations.

---

# In-Context Learning Reward Guided Decoding for Controlled Text Generation

DOI: 10.1109/icsp62122.2024.10743861
Ano: 2024
Tipo de documento: Artigo de congresso
Base onde foi encontrado: Lens.org
RRI: #222

While large language models have demonstrated remarkable text generation capabilities, they often generate text with adverse or undesired attributes. Common approaches to control text generation involve refining models on data with desired properties or guiding language models decoding using an auxiliary model. However, these methods require additional training and extensive attribute-specific data. To further mitigate the training costs, we propose In-context learning Reward Guided Decoding (IRGD), a weighted decoding method that exploits the in-context learning ability of language models as an alternative to additional model fine-tuning. Specifically, IRGD utilizes ICL outputs to score the alignment reward between sequences and target attributes, subsequently modifying the sampling probabilities to favor tokens with higher reward scores. By applying ICL, IRGD adapts to different tasks by simply adjusting task descriptions and demonstration rather than fine-tuning the model. Through experiments on detoxification and sentiment control, we demonstrate the advantages of IRGD as a plug-and-play and fine-tuning-free decoding method that effectively balance attribute alignment and text quality.

---

# Large Language Model Based Text Summarization: Taxonomy, Evaluation Practices, and Research Challenges

DOI: 10.29284/dwvcma49
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #236

The increasing amount of digital text generated in scientific, industrial, and societal domains has rendered text summarisation an essential research challenge rather than a mere supplementary task. Recent progress in large language models (LLMs) has changed the way automatic summarisation is done in a big way. For example, it has made it possible to create summaries that are more fluent, sensitive to context, and flexible across domains. This review looks at how text summarisation methods have changed over time, starting with early statistical and neural methods and moving on to transformer-based and LLM-driven methods that are now the most popular in the field. Instead of looking at summarisation as one big problem, this paper uses a structured taxonomy to separate extractive, abstractive, hybrid, and LLM-based paradigms, talking about the pros and cons of each. Seventy-five representative studies published from 2019 to 2025 are rigorously analysed, focussing on reported performance trends as well as domain-specific behaviours and evaluation methodologies. While LLM-based systems consistently exhibit advantages in fluency, adaptability, and zero-shot application, the literature concurrently highlights enduring concerns regarding factual reliability, interpretability, and the sufficiency of current evaluation metrics. In response to these limitations, this review presents a conceptual framework for next-generation summarisation systems that prioritises modular design, incorporating retrieval augmentation, controlled generation, verification mechanisms, human feedback, and ethical governance. Finally, important research gaps are pointed out, and future steps are suggested to help make LLM-based text summarisation systems that are more reliable and used in a responsible way.

---

# LLM-Driven Lean Manufacturing System: Integrating AI, RAG, and Embeddings for Industry 4.0 Decision Support

DOI: 10.32996/jcsts.2026.8.8.8
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Lens.org
RRI: #243

The integration of Large Language Models (LLMs) with Lean Manufacturing methodologies represents a significant frontier in the evolution of intelligent manufacturing systems within the Industry 4.0 paradigm. This comprehensive research report presents the architecture, design rationale, and empirical evaluation of a web-based Lean Manufacturing System (LMS) that employs LLMs to automate the generation of structured Lean tools, including Value Stream Mapping (VSM), 5W2H action planning, Ishikawa diagrams, Pareto analysis, GUT prioritization matrices, PDCA cycles, Kanban boards, process flowcharts, and Five Whys root-cause analysis, from unstructured natural-language problem descriptions provided by industrial operators. The proposed architecture adopts a modular microservices design, a Retrieval-Augmented Generation (RAG) pipeline, built upon LangChain, FAISS vector stores, and sentence-transformer embeddings, grounding model outputs in curated domain knowledge sourced from internal project documentation and Lean Manufacturing references. Structured prompt engineering with explicit persona definitions, mathematical output constraints, and JSON schema enforcement constitutes the primary mechanism for deterministic output generation. Experimental validation using a representative industrial case, a connector assembly workstation exhibiting a 12% rework rate, demonstrates that the AI-generated Lean artifacts correctly identify root causes, prioritize countermeasures, and project a 65% lead time reduction alongside a 200% productivity gain. Critical technical limitations are identified and discussed, encompassing single-scenario generation, absence of a feedback loop for continuous learning, dependency on prompt-level logic for semantic consistency, and a lack of integration with real-time shop-floor data streams. We conclude the analysis with a roadmap for overcoming these limitations through multi-agent orchestration, reinforcement learning from human feedback, and dynamic sensor integration.

---

# VARIA: Benchmarking Frontier LLMs on Construct-Equivalent Assessment Variant Generation

DOI: 10.35542/osf.io/u6xef_v1
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #249

In plain terms: if we are going to let AI write personalized versions of tests for every student, those versions have to be more than surface paraphrase. They have to look genuinely different on the outside while still measuring the same underlying skill on the inside. This paper asks whether today's frontier AI models can actually do that, and offers a way to measure it.AI-Integrated Authentic Assessment (AIAA) frameworks propose to replace surveillance-based proctoring with per-student task variation: each examinee receives a unique-yet-equivalent performance task, making answer copying useless without invasive monitoring. The framework's no-surveillance integrity guarantee is conditional on a presumed but unverified capability: that large language models can generate parallel variants of an assessment blueprint that are simultaneously surface-distinct, construct-equivalent, rubric-applicable, and difficulty-matched. We introduce VARIA, a benchmark that operationalizes this presumption as four measurable properties of a generated variant set. VARIA evaluates three frontier model families (Anthropic Claude Opus 4.7, OpenAI GPT-5.5, Google Gemini 3.1 Pro Preview) across four prompting strategies (zero-shot, few-shot with anchor examples, structured chain-of-thought, dimension-preserving constrained generation) on three competency-based blueprints drawn from applied AI and data analytics, alongside two non-frontier reference systems (a small open instruction-tuned model and GPT-2 small) and two targeted ablations. A pilot of 600 generated variants across 60 condition cells reveals that frontier strategies cluster tightly on a composite integrity score (joint J between 0.81 and 0.88) while the non-frontier references collapse to J between 0.50 and 0.55, a forty-percentage-point gap that establishes the benchmark's discrimination. Within the frontier band, structured chain-of-thought and zero-shot prompting maximize construct equivalence; dimension-preserving constrained generation and few-shot anchoring maximize surface diversity; and the two regimes trade against each other on readability parity. We release VARIA, recommend a generation protocol keyed to the deploying institution's threat profile, and pre-register a follow-up that will measure rubric stability and behavioral copy-resistance.

---

# Substrates Are All You Need: Defeatning Non-determinism With Natural Language

DOI: 10.5281/zenodo.19452773
Ano: 2026
Tipo de documento: Preprint
Base onde foi encontrado: Lens.org
RRI: #250

Large language models are often treated as non-deterministic due to stochastic decoding. This paper shows that non-determinism instead arises from interpretation drift—multiple valid task definitions under the same input. When tasks are under-specified, models may produce different but internally consistent outputs because they are effectively solving different problems. Standard prompt engineering techniques (behavioral nudging) do not eliminate this effect, as they operate within the interpretation space rather than constraining it. We introduce substrate-first architectures, where task specifications explicitly constrain the interpretation space to a single admissible definition. Under this condition, independently trained models converge to identical outputs for the same input, verified via byte-level equality (SHA-256 hashing). These results reframe determinism as a property of task specification rather than model behavior. Reliable AI systems are achieved not by controlling generation, but by eliminating interpretive ambiguity. Companion papers: Empirical Evidence Of Interpretation Drift In Large Language Models: https://zenodo.org/records/18219428Empirical Evidence Of Interpretation Drift In ARC-Style Reasoning: https://zenodo.org/records/18420425

---

# AI-Driven Metric Extraction of Sustainability Data

DOI: —
Ano: 2025
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: OATD
RRI: #252

Corporate sustainability reports provide essential information regarding a company’s environmental impact, yet their inconsistent formatting and lack of structure pose significant challenges for automated Information Extraction (IE). This thesis presents an end-to-end IE pipeline leveraging large language models (LLMs) to extract quantitative sustainability metrics, such as greenhouse gas emissions and energy use, from unstructured PDF reports. The system integrates document parsing, image-summarization, relevance classification, Retrieval-Augmented Generation (RAG), In-Context Learning (ICL), Constrained Decoding Generation (CDG), and rule-based validation. A benchmark dataset of 63 reports was compiled, with a subset used to construct one-shot examples. Evaluation against a manually curated gold dataset revealed that the system outperforms manual processing in speed but falls short of expert-level accuracy. The highest-performing extraction method achieved a precision of 48.4%, a recall of 18.0%, and an F1 score of 26.3%. A modified MAP evaluation revealed that using fine-tuned BERT models to classify related information could slightly increase retrieval performance, but it decreased overall accuracy. These results reflect the difficulty of processing multimodal content and the limitations of semantic search in retrieving the correct context within documents where multiple sections discuss similar topics using overlapping terminology. However, statistical validation using McNemar’s test demonstrated that applying rule-based validation significantly improved overall extraction accuracy, confirming the value of structured validation in LLM-based workflows. Future work should explore improved retrieval methods, better handling of multimodal content such as image-based tables, and opportunities for human-AI collaboration. Enhancements like fine-tuned embedding models, structured intermediate outputs, and real-time user feedback could increase accuracy and usability. Företags hållbarhetsrapporter tillhandahåller viktig information om ett företags miljöpåverkan, men deras inkonsekventa formatering och brist på struktur utgör betydande utmaningar för automatiserad informationsextraktion (IE). Denna avhandling presenterar en IE-pipeline som använder stora språkmodeller (LLM) för att extrahera kvantitativa hållbarhetsmått, såsom växthusgasutsläpp och energianvändning, från ostrukturerade PDF-rapporter. Systemet integrerar dokumentparsning, bildsammanfattning, relevansklassificering, Retrieval-Augmented Generation (RAG), In-Context Learning (ICL), Constrained Decoding Generation (CDG) och regelbaserad validering. Ett dataset bestående av 63 rapporter sammanställdes, där en delmängd användes för att konstruera one-shot-exempel. Utvärdering mot en manuellt kurerad gulddataset visade att systemet överträffar manuell bearbetning i hastighet men inte når upp till expertnivåns noggrannhet. Den bäst presterande extraktionsmetoden uppnådde en precision på 48,4%, en recall på 18,0% och ett F1-värde på 26,3%. En…

---

# Creativity in Large Language Models

DOI: —
Ano: 2025
Tipo de documento: Tese ou dissertação
Base onde foi encontrado: OATD
RRI: #253

As artificial intelligence systems approach human-level performance across a wide variety of domains, creative domains remain a critical yet underexplored area of research. Unlike traditional AI tasks with well-defined objectives, creative tasks rely on inherently subjective measures, making them particularly challenging for machines that lack human experiential context. This dissertation establishes the fundamental importance of creativity in AI systems and presents methods for improving and evaluating the creative capabilities of LLMs on the pathway toward AGI. This work addresses and examines key limitations in current LLM creativity through model innovations, development frameworks, and comparative studies. The dissertation develops novel architectural approaches including an external knowledge integration mechanism inspired by human symbolic memory and black-box controllable text generation methods. Additionally, it presents a game-based development framework for creative agents and an automated knowledge extraction pipeline for story generation systems. Through comparative studies across multiple creative domains, this research provides empirical insights into the capabilities and limitations of LLMs in creative tasks. The work establishes evaluation frameworks for comparing general-purpose LLMs against traditional computational creativity systems and develops methods for assessing the effectiveness of various prompting techniques in creative text generation. These investigations show that LLM-generated creative artifacts are generally preferred over those from traditional CC systems, advanced prompting techniques (e.g., OPRO, chain-of-thought) do not significantly outperform basic prompting, and that LLM-based automatic evaluation is limited. Finally, this work reflects on the advantages and limitations of enhancing LLM creativity and provides directions for future work.

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

# A2C-LLM: An Actor-Critic-Enhanced Large Language Model for UAV Swarm Multi-Target Task Allocation

DOI: 10.3390/drones10060398
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #257

Highlights What are the main findings? A2C-LLM integrates large language models with Actor-Critic reinforcement learning, forming a closed training-inference loop for UAV swarm task allocation, significantly outperforming pure LLM and pure RL baselines in task completion rate and convergence stability. Single-step MDP with structured feasibility constraints enables scalable coordination for large-scale UAV swarms, where constrained decoding and feasibility projection ensure the executability of generated commands. What are the implications of the main findings? Combining lightweight foundation models (only 1.5B parameters) with principled RL training provides a viable pathway for deploying AI systems in safety-critical robotic applications requiring both semantic reasoning and execution guarantees. The semantic-numerical interface resolves the tension between semantic flexibility and execution guarantees, bridging the gap between high-level task allocation and low-level executable commands in dynamic multi-agent environments, with strong scalability for future low-altitude economy deployments.Highlights What are the main findings? A2C-LLM integrates large language models with Actor-Critic reinforcement learning, forming a closed training-inference loop for UAV swarm task allocation, significantly outperforming pure LLM and pure RL baselines in task completion rate and convergence stability. Single-step MDP with structured feasibility constraints enables scalable coordination for large-scale UAV swarms, where constrained decoding and feasibility projection ensure the executability of generated commands. What are the implications of the main findings? Combining lightweight foundation models (only 1.5B parameters) with principled RL training provides a viable pathway for deploying AI systems in safety-critical robotic applications requiring both semantic reasoning and execution guarantees. The semantic-numerical interface resolves the tension between semantic flexibility and execution guarantees, bridging the gap between high-level task allocation and low-level executable commands in dynamic multi-agent environments, with strong scalability for future low-altitude economy deployments.Abstract In UAV swarm adversarial applications, multi-agent task allocation requires high-level reasoning and accurate decision-making in dynamic environments. Although large language models (LLMs) have shown strong performance in zero-shot reasoning, they cannot generate optimal allocation strategies without environmental objective feedback. To address this problem, we present A2C-LLM, an Actor-Critic-enhanced large language model for adversarial UAV swarm task allocation. Unlike traditional methods that adopt sequential tracking, we adopt a single-step decision process for macro allocation to improve the efficiency of immediate allocation. In A2C-LLM, the LLM serves as the Actor network to understand the adversarial environment and generate coordination strategies, while a lightweight neural network serves as the Critic network to estimate expected rewards and calculate TD advantage for fine-tuning. Experimental results demonstrate that A2C-LLM significantly outperforms traditional heuristic algorithms and pure LLM baselines in task completion rate and robustness across various adversarial scenarios, showcasing the potential of integrating reinforcement learning feedback with foundation models for autonomous aerial systems.

---

# LLM-based JSON Mapping and Blockchain Integration for Digital Product Passports☆,☆☆

DOI: 10.1016/j.digbus.2026.100167
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #276

The European Commission envisages Digital Product Passports (DPPs) as a mechanism to enable traceable, transparent, and standardized product data across supply chains. This work presents a modular pipeline that transforms raw sensor data into verifiable DPP records using large language models (LLMs) for data standardization and blockchain technology for tamper-proof storage. The system maps unstructured machine-level data to a standardized JSON format and stores it immutably on the Waves blockchain via smart contracts, thereby enabling auditable, machine-readable records suitable for regulatory use. A novel evaluation dataset is introduced to simulate daily production scenarios with varying mapping complexity. The performance of the system is assessed using both proprietary and open-weight LLMs. Results show that the proprietary model achieves the highest accuracy and lowest latency, while open-weight models perform worse as input complexity increases. Multiple prompting strategies were compared, revealing that direct mapping, via few-shot or zero-shot prompts, consistently delivered higher accuracy than approaches based on generating transformation functions. Structured output formatting was also assessed: While it ensured schema validity, it often compromised mapping reliability by introducing incorrect values, likely due to disruptions in model reasoning from output constraints. The proposed architecture demonstrates reliable end-to-end operation with low latency and is suitable for batch-level deployment in real-world production environments. From a practical perspective, the results clarify trade-offs between model choice, prompting strategy, and operational reliability in automated DPP generation. For policymakers, the findings highlight how choices around schema clarity and data granularity shape system design and operational effort in future DPP implementations.

---

# Exploring MLLMs for ultra-fine-grained agricultural classification

DOI: 10.48130/ker-0026-0010
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #285

Accurate identification of crop cultivars or pest species at subspecies granularity is essential for precision agriculture. Discriminative features are confined to subtle morphological details (leaf venation, surface texture, or reproductive organ structure), producing minimal inter-class visual distance alongside severe label scarcity, together defining the Ultra Fine-Grained Visual Classification (Ultra-FGVC) regime. Neither convolutional nor Vision Transformer advances have resolved this representational gap, suggesting a fundamental encoder bottleneck. Multimodal large language models (MLLMs) are a principled candidate: web-scale training encodes structured biological knowledge absent from image-label supervision, available at inference time without retraining, directly addressing both failure modes. We present a controlled evaluation of four state-of-the-art MLLMs across three Ultra-FGVC benchmarks, examining baseline few-shot accuracy, label semantics contribution, and prompt-design sensitivity under chain-of-thought decomposition, contrastive elimination, and few-shot in-context learning. Three fundamental failure modes limit MLLM deployment in Ultra-FGVC: the representational ceiling of CLIP-based visual encoders, which widens the accuracy gap as category count grows; output generation unreliability under structured-output requirements; and systematic confidence miscalibration that precludes raw scores from serving as deployment rejection thresholds. For each, we characterise its origin and propose remedies, including richer visual backbones, constrained decoding, and post-hoc calibration to advance MLLMs toward operational viability in precision agriculture.

---

# Intelligent support for soil and water conservation compliance: decision assistance capabilities of prompt-enhanced large language models

DOI: 10.1007/s10506-026-09531-8
Ano: 2026
Tipo de documento: Artigo de periódico
Base onde foi encontrado: Web of Science
RRI: #290

Soil and water conservation (SWC) laws and regulations are hierarchically complex and frequently revised, and grassroots compliance urgently needs efficient, intelligent knowledge tools. Locally deployable small language models (SLMs) avoid the computational cost and data-leakage risks of large models, but their capability boundaries in the SWC legal domain and the pathways for enhancing them remain unclear. Using 71 national and local SWC regulations and the newly promulgated Ecological and Environmental Code of the People's Republic of China as source materials, we built an evaluation dataset spanning four task types-theoretical knowledge, operational specifications, law-enforcement practice, and comprehensive analysis-across three regulatory levels, and evaluated five SLMs (Qwen3-14B, Qwen3-30B, Phi-4, Gemma3-12B, and Gemma4-31B) under local closed-book conditions. Guided by Cognitive Load Theory, we designed a structured prompt (role setting, task identification, reasoning guidance, and output constraints), ablated each component against an equal-length placebo, and compared reasoning guidance with direct provision of statutory text; beyond accuracy and cost, we added process-level metrics including citation hit rate, rule-selection quality, and suspected hallucination. Baseline accuracy ranged from 68.9% to 84.0% and did not rise monotonically with parameter scale. Structured prompts improved accuracy only marginally while doubling hallucination, whereas providing statutory text raised accuracy by 9.2-14.3% and lowered hallucination to near zero. Knowledge provision, not prompt engineering, is therefore the decisive route to reliable answering. Gemma4-31B with statutory text achieved approximately 94% accuracy with near-zero hallucination within three seconds per question, making it the most cost-effective choice for grassroots deployment.