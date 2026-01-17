# CS 598: Systems for Generative AI (S'26)

## Logistics
**Lectures**: 0216 Siebel Center for Computer Science, WF: 12:30 PM – 01:45 PM
| Member (NetID) | Role | Office Hours |
| :---------------- | :--- | :----------- |
| [Fan Lai](https://fanlai.me/) (fanlai) | Instructor | 3128 Siebel Center. F 2 PM – 3 PM
| [Jimmy Shong](https://jiminator.github.io/PersonalSite/) (jimmys2) <br> Yuhan Ding (yuhand7) | TAs | [Zoom](https://illinois.zoom.us/j/82278931782?pwd=OuM7Ep1OOXMeSuXXexmTAIuUOJz1bE.1). W 7:00 PM - 8:00 PM

**Canvas**:  *ALL* communication regarding this course must be via [Canvas](https://canvas.illinois.edu/courses/67788). This includes questions, discussions, announcements, assignments, as well as private messages.

Presentation slides should be submitted to Canvas.

## Course Description
**Learning Objectives**: This course will introduce the key concepts and the state-of-the-art in practical, scalable, and fault-tolerant software systems for emerging Generative AI (GenAI). At the end of the course you will be able to: 

-   Critique and evaluate the design details of state-of-the-art GenAI systems
-   Develop and utilize tools to profile and understand the performance of GenAI systems
-   Propose new research ideas in topics related to support practical GenAI

**Structure**: The course will be a mix of lectures, student presentations, seminar-style discussions, and a semester-long project on GenAI topics.  We will cover GenAI topics from top conferences that take a systems view to the relevant challenges, including:  
- Basics of GenAI models from a systems perspective; 
- Systems for GenAI lifecycle (pre-training, training, fine-tuning/alignment, inference serving, and grounding); 
- GenAI for systems and etc. 

Note that this course is **NOT focused on AI methods**.  Instead, we will *focus on how one can build software systems* so that existing AI methods can be used in practice and new AI methods can emerge. 

**Prerequisites**:  Students are expected to have good programming skills and must have taken at least one undergraduate-level systems-related course (from operating systems, databases, distributed systems, or networking). Having an undergraduate ML/AI course is helpful but not required.

## Tentative Schedule and Reading List  
*This is an evolving list and subject to changes due to the breakneck pace of GenAI innovations.*

| Date | Readings | Presenter | Companion | Reviewer |
|------|----------|-----------|-----------|----------|
| Jan 21 <br>(GenAI Systems) | **Introduction**<br>[How to Read a Paper](http://svr-sk818-web.cl.cam.ac.uk/keshav/papers/07/paper-reading.pdf) <br>[How to Give a Bad Talk](http://www.cs.berkeley.edu/~pattrsn/talks/BadTalk.pdf) <br>[The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) |     Fan      |           |          |
|   | **GenAI Basics**
| Jan 23 <br>(LLM Fundamentals) | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)<br>[Flash Attention](https://arxiv.org/abs/2205.14135) | Jimmy | | |
| Jan 28 <br>(Transformers Deep Dive) |  [FlashAttention-V2](https://arxiv.org/pdf/2307.08691)<br> [Native Sparse Attention](https://arxiv.org/abs/2502.11089) | Fan | | |
| Jan 30 <br> (Scalable ML) | [Scaling Distributed Machine Learning with the Parameter Server](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-li_mu.pdf) <br> [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/pdf/1909.08053) | Fan | | |
| Feb 4 <br> (Diffusion Models) | [The Illustrated Stable Diffusion](https://jalammar.github.io/illustrated-transformer/) <br>[Scalable Diffusion Models with Transformers](https://arxiv.org/pdf/2212.09748) (Required) | | | |
|   | **Pre-Training**
| Feb 6 <br> (Hybrid Parallelism) | [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473) (Required)<br>[Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://www.usenix.org/system/files/osdi22-zheng-lianmin.pdf) | | | |
| Feb 6 <br> (Training MoEs) | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://openreview.net/pdf?id=B1ckMDqlg) (Required)<br>[FSMoE: A Flexible and Scalable Training System for Sparse Mixture-of-Experts Models](https://arxiv.org/abs/2501.10714) | | | |
| Feb 11 <br> (Fault Tolerance) | [TrainVerify: Equivalence-Based Verification for Distributed LLM Training](https://www.arxiv.org/pdf/2506.15961) (Required)<br>[Oobleck: Resilient Distributed Training of Large Models Using Pipeline Templates](https://arxiv.org/abs/2309.08125) | | | |
|   | **Post-Training**
| Feb 13 <br> (Finetuning Techniques) | [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685) (Required)<br>[S-LoRA: Serving Thousands of Concurrent LoRA Adapters](https://arxiv.org/abs/2311.03285) |  | | |
| Feb 18 <br> (Exploiting Sparsity) | [AWQ: Activation-aware Weight Quantization](https://arxiv.org/abs/2306.00978) (Required)<br>[Radial Attention: O(n log n) Sparse Attention with Energy Decay for Long Video Generation](https://arxiv.org/pdf/2506.19852) | | | |
| Feb 20 <br>(RLHF Systems) | [DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948) (Required)<br>[AReaL: A Large-Scale Asynchronous Reinforcement Learning System for Language Reasoning](https://arxiv.org/abs/2505.24298) | | | |
| Feb 25 <br>(RLHF Systems) | [Optimizing RLHF Training for Large Language Models with Stage Fusion](https://www.usenix.org/system/files/nsdi25-zhong.pdf) (Required)<br>[RLBoost: Harvesting Preemptible Resources for Cost-Efficient Reinforcement Learning on LLMs](https://arxiv.org/pdf/2510.19225) | | | |
|   | **Inference**
| Feb 27 <br> (Inference Runtime) | [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://arxiv.org/abs/2309.06180) (Required)<br>[Orca: A Distributed Serving System for Transformer-Based Generative Models](https://www.usenix.org/system/files/osdi22-yu.pdf) |  | | |
| Mar 4 <br> (Optimizing Throughput) | [Fast Inference from Transformers via Speculative Decoding](https://arxiv.org/abs/2211.17192) (Required)<br>[NanoFlow: Towards Optimal Large Language Model Serving Throughput](https://arxiv.org/abs/2408.12757)  | | | |
| Mar 6 <br> (Optimizing Latency) | [Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://arxiv.org/abs/2403.02310) (Required)<br>[DistServe: Disaggregating Prefill and Decoding for Goodput-optimized Large Language Model Serving](https://arxiv.org/abs/2401.09670) | | | |
| Mar 11 <br> (Optimizing User Experience) | [JITServe: SLO-aware LLM Serving with Imprecise Request Information](https://arxiv.org/abs/2504.20068) (Required)<br>[Mooncake: Trading More Storage for Less Computation](https://www.usenix.org/system/files/fast25-qin.pdf) | | | |
| Mar 14–22 | **Spring Break**
| Mar 25 <br> (Optimizing MLLMs) | [ModServe: Scalable and Resource-Efficient Large Multimodal Model Serving](https://haoran-qiu.com/pdf/modserve-preprint.pdf) (Required)<br>[Cornserve: Efficiently Serving Any-to-Any Multimodal Models](https://arxiv.org/abs/2512.14098) | | | |
| Mar 30  | **Mid-Semester Project Feedback Session** | | | |
| Apr 3 | **Mid-Semester Project Feedback Session** | | | |
| Apr 8 <br> (In-Context Caching) | [IC-Cache: Efficient Large Language Model Serving via In-context Caching](https://arxiv.org/abs/2501.12689) (Required)<br>[Approximate Caching for Efficiently Serving Text-to-Image Diffusion Models](https://www.usenix.org/system/files/nsdi24-agarwal-shubham.pdf) | | | |
| Apr 10 <br> (Diffusion Serving) | [PipeFusion: Patch-level Pipeline Parallelism for Diffusion Transformers Inference](https://arxiv.org/pdf/2405.14430) (Required)<br>[StreamDiffusionV2: A Streaming System for Dynamic and Interactive Video Generation](https://arxiv.org/abs/2511.07399) | | | |
| | **Agentic AI Systems** | | | |
| Apr 15 <br> (RAG Systems) | [CacheBlend: Fast Large Language Model Serving for RAG with Cached Knowledge Fusion](https://arxiv.org/abs/2405.16444) (Required)<br>[AVA: Towards Agentic Video Analytics with Vision Language Models](https://arxiv.org/abs/2505.00254v5) | | | |
| Apr 17 <br> (Agent for Sys) | [Measuring Agents in Production](https://arxiv.org/pdf/2512.04123) (Required)<br>[Intent-Driven Network Management with Multi-Agent LLMs: The Confucius Framework](https://minlanyu.seas.harvard.edu/writeup/sigcomm25.pdf) | | | |
| Apr 22 <br> (Agent Coordination) | [In-the-Flow Agentic System Optimization for Effective Planning and Tool Use](https://arxiv.org/abs/2510.05592) (Required)<br>[Towards End-to-End Optimization of LLM-based Applications with Ayo](https://dl.acm.org/doi/10.1145/3676641.3716278) | | | |
| Apr 24 <br> (Agent Failures) | [Why Do Multi-Agent LLM Systems Fail?](https://arxiv.org/pdf/2503.13657) (Required)<br>[Where LLM Agents Fail and How They can Learn From Failures](https://arxiv.org/abs/2509.25370) | | | |
| Apr 29  | Final Project Presentation | | | |
| May 1  | Final Project Presentation | | | |
| May 6 | Final Project Presentation | | | |

 ## Tentative Grading
**Groups**:  Panel discussion and research project will be performed in groups of 4-5 students. Form a group and [declare your group's membership and paper preferences](https://forms.gle/TVkqSQAvUfKzsZGA7) by **Feb 1**. After this date, we will form groups from the remaining students.

|                         | Weight | 
| ------------------------| :------| 
| [Attendance](#participation)           | 10%    | 
| [Reading summary](#paper-summaries)           | 20% (opt-in 14 out of 19 readings)    | 
| [Paper presentation](#paper-presentation)          | 15%    | 
| [Panel discussion](#Post-Lecture-Panel-Discussion)           | 5% (two panels)    | 
| [Final project presentation](#project)          | 15%    | 
| [Project report](#project)   | 35% (5% + 10% + 20%)    |

**Academic integrity**: [The University's Honor Code](https://siebelschool.illinois.edu/academics/honor-code) applies to all activities related to this course. All material you submit in this course (reading summary, project reports, and presentation materials) must be your own. If you use someone else’s material, you must cite them properly. 

**AI Tool Policy**: AI tools may be used for grammar checking and refining initial brainstorms, but the final reviews and codes **must** be authored by the student. Students are responsible for the entire content and must adhere to the Academic Integrity Policy. 

## Policies

### Participation
**Before Each Lecture**: Some lectures may include one required reading. You must submit a summary of the paper to Canvas by 11:59 PM on the due date.

**During Lectures**: Active participation is crucial for both your own understanding and to improve the overall quality of the course. You are expected to attend **all** lectures (up to 2 absences allowed for legitimate reasons), and more importantly, participate in class discussions. Not everyone must have add something every day, but it is expected that everyone has something to share over the semester.

### Paper Summaries
You need to select and write paper summaries from **14 papers out of 19 listed papers**. The summary should be done independently and include the following contents (five paragraphs):

- P1: The problem the paper is trying to tackle. What's the impact of the work, e.g., why is it an important problem to solve? 
- P2: The main proposed idea(s). 
- P3: A summary of your understanding of different components of the proposed technique, e.g., the purpose of critical design choices.
- P4: Your perceived strengths and weaknesses of the work, e.g., novelty, significance of improvements, quality of the evaluation, easy-to-use.
- P5: Is there room for improvement? If so, what idea do you have for improving the techniques? 

You do not need to write super long paragraphs, as long as you have the key points listed out in each paragraph. You can discuss the paper with other students, but all of your writing work should be your own. DO NOT use AI tools to draft it!

In terms of grading criteria, each summary has 10 points in total. For each review item above, you get:

- 2: The summary item demonstrates a clear understanding of the paper.
- 1: The summary item misses the point of the paper.
- 0: The summary item is missing.

Due to selecting the 14/19 paper summaries, late submissions will NOT be accepted and will receive 0 points.

### Paper Presentation
The course will be conducted as a seminar. Only one group will present in each class. Each group will be assigned *one lecture* over the course of the semester. Presentations should last **at most 45 minutes** without interruption.
However, presenters should expect questions and interruptions throughout. 

In the presentation, you should:

* Provide a brief background to motivate the problem (e.g., simplifying this by referencing previous talks)
* Present the high level idea, approach, and/or insight (using examples, whenever appropriate) in the required reading. 
* Discuss technical details so that one can understand key details without carefully reading (quickly skim the evaluations).
* Explain the differences between related works as well as the additional reading.
* Identify strengths and weaknesses of the required reading and propose directions of future research.

*The slides for a presentation must be submitted to Canvas (in \*.pptx format) at least 24 hours prior to the corresponding class for feedbacks.*

### Post-Lecture Panel Discussion 
To foster a deeper understanding of the papers and encourage critical thinking, lectures with paper summary will be followed by a panel discussion. This discussion will involve three distinct roles played by different student groups, simulating an interactive and dynamic scholarly exchange. 

#### Roles and Responsibilities

1. **The Companion (Author) Group**
- Responsibility: As authors, you are expected to defend your paper against critiques, answer questions, and discuss how you might improve or extend your research in the future, akin to writing a rebuttal during the peer-review process.


2. **The Reviewer Group**
- Responsibility: Reviewers critically assess the paper, posing challenging questions and highlighting potential weaknesses or areas for further investigation. 
Your goal is to engage in a constructive critique of the paper, simulating a peer review scenario.

 
3. **Rest of the Class**
- Responsibility: During the panel discussions, feel free to actively **ask questions** and engage in the dialogue. 

The lecturer will also pose challenging questions to both the companion and reviewer groups, so please come well-prepared!

### Project
You will have to complete substantive work an instructor-approved problem and have original contribution. Surveys are not permitted as projects; instead, each project must contain a survey of background and related work.

You must meet the following milestones (unless otherwise specified in future announcements) to ensure a high-quality project at the end of the semester:

* Turn in a 2-page draft proposal ([template](https://www.overleaf.com/read/bsrcbphcvyzc#d075e8)), plus as many pages as needed for references, by **February 21**. Remember to include the names and UIUC email addresses of the group members. 
* Each group must turn in a 4-page mid-semester report, plus as many pages as needed for references, via email **on or before 6:00PM CST on March 27.** 
* Each group must schedule project discussion with the instructor during class hours or office hours in the week of **March 30** and **April 3**.
* Each group must turn in an 8-page final report, plus as many pages as needed for references, and your code via email **on or before 6:00PM CST on May 15.** The report must be submitted as a PDF file, with formatting similar to that of the papers you've read in the class. The self-contained (i.e., include ALL dependencies) code must be submitted to Canvas as a zip file. Each zip file containing the code must include a README file with a step-by-step guide on how to compile and run the provided code.
* You can find how to access GPU resources [here](./Resources/cloudlab.md).

### **Acknowledgements**
This course is heavily inspired by other excellent system seminar courses, particularly [UMich CSE 585](https://github.com/mosharaf/eecs598/tree/w24-genai). Acknowledgments to [SymbioticLab](https://symbioticlab.org/).	
