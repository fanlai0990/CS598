# CS 598: Systems for Generative AI (S'25)

## Logistics
**Lectures**: 0216 Siebel Center for Computer Science, WF: 12:30 PM – 01:45 PM
| Member (NetID) | Role | Office Hours |
| :---------------- | :--- | :----------- |
| [Fan Lai](https://fanlai.me/) (fanlai) | Instructor | 3128 Siebel Center. W 2:00 PM – 3:00 PM
| [Chengsong Zhang](https://continue-revolution.github.io/) (cz81)<br> [Jimmy Shong](https://jiminator.github.io/PersonalSite/) (jimmys2) | TAs | [Zoom](https://illinois.zoom.us/j/82278931782?pwd=OuM7Ep1OOXMeSuXXexmTAIuUOJz1bE.1). W 7:00 PM - 8:00 PM

**Piazza**:  *ALL* communication regarding this course must be via [Piazza](https://piazza.com/illinois/spring2025/cs598fla). This includes questions, discussions, announcements, as well as private messages.

Presentation slides and paper summaries should be emailed to [cs598-aisys-staff@lists.cs.illinois.edu](mailto:cs598-aisys-staff@lists.cs.illinois.edu).

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

| Date    | Readings                                                                                                             | Presenter | Companion | Reviewer |
| ------- | -------------------------------------------------------------------------------------------------------------------- | --------- | --------- | -------- |
| Jan 22 <br>(GenAI Systems) | **Introduction**<br>[How to Read a Paper](http://svr-sk818-web.cl.cam.ac.uk/keshav/papers/07/paper-reading.pdf) (Required)<br>[How to Give a Bad Talk](http://www.cs.berkeley.edu/~pattrsn/talks/BadTalk.pdf) (Required)<br>[Writing Reviews for Systems Conferences](http://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf)<br>[The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) |     [Fan](./Slides/fan-overview.pdf)      |           |          |
|   | **GenAI Basics**
| Jan 24 <br>(LLM Fundamentals)  | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) (Required)<br>[FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://papers.nips.cc/paper_files/paper/2022/hash/67d57c32e20fd0a7a302cb81d36e40d5-Abstract-Conference.html) (Required)<br>[Attention Is All You Need](https://dl.acm.org/doi/10.5555/3295222.3295349)<br>[The Transformer Family Version 2.0](https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/) |    [Jimmy](./Slides/Transformers.pptx)       |           |          |
| Jan 29 <br>(Diffusion Fundamentals)  | [The Illustrated Stable Diffusion](https://jalammar.github.io/illustrated-stable-diffusion/) (Required)<br>[Scalable Diffusion Models with Transformers](https://arxiv.org/pdf/2212.09748) (Required)<br>[Adding Conditional Control to Text-to-Image Diffusion Models](https://arxiv.org/pdf/2302.05543) <br> [Hierarchical Text-Conditional Image Generation with CLIP Latents](https://arxiv.org/abs/2204.06125) |    [Chengsong](https://docs.google.com/presentation/d/1J83N1gP4-4lJl1MyURT8caAaa-OcSd_KXBDFUE505Jo/edit?usp=sharing)       |           |          |
| Jan 31  | **No Lecture / Work on Project Proposal**<br>[Worse is Better](https://en.wikipedia.org/wiki/Worse_is_better) (Required)<br>[Hints and Principles for Computer System Design](https://arxiv.org/abs/2011.02455) |           |           |          |
| Feb 5 <br>(LMMs)  | [Multimodality and Large Multimodal Models (LMMs)](https://huyenchip.com/2023/10/10/multimodal.html) (Required)<br>[Visual Instruction Tuning](https://arxiv.org/abs/2304.08485)<br>[DeepSpeed-VisualChat: Multi-Round Multi-Image Interleave Chat via Multi-Modal Causal Attention](https://arxiv.org/abs/2309.14327) |[apirani2, divyam4, aryanb3, amang7](./Slides/mllm.pptx)|asanaka2, imathur3, abhakat2, gdurand2, jgosar2|amitp4, deeyaab2, lneti2, rishis5, sdedhia2|
| Feb 7 <br>(MoE)   | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://openreview.net/forum?id=B1ckMDqlg) (Required)<br>[DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://arxiv.org/abs/2201.05596) (Required)<br>[Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://dl.acm.org/doi/abs/10.5555/3586589.3586709)<br>[Scaling Vision-Language Models with Sparse Mixture of Experts](https://arxiv.org/abs/2303.07226) | [pokkali2, echen48, cy5, keshav6, wendi2](./Slides/moe.pptx)|jiaxili3, xinyue21, dk31, zihengc3|skatt24, akhils7, adit3, nu4|
| Feb 12 <br>(Video Generation)  | [VideoPoet: A Large Language Model for Zero-Shot Video Generation](https://arxiv.org/pdf/2312.14125) (Required)<br>[CogVideoX: Text-to-Video Diffusion Models with An Expert Transformer](https://arxiv.org/pdf/2408.06072) (Required)<br>[Movie Gen: A Cast of Media Foundation Models](https://arxiv.org/abs/2410.13720) | [amitp4, deeyaab2, lneti2, rishis5, sdedhia2](./Slides/video-gen.pptx) |colincl2, adishj2, bwz2, hshen14, zhong42|srm17, apillai7, dhruva7, mihirss3|
|   | **Pre-Training**    
| Feb 14 <br>(Training Infra)  | [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783) (Sec 1-4.2, Required)<br>[DeepSeek-V3 Technical Report](https://arxiv.org/pdf/2412.19437) (Sec 3.1-3.2, 3.4, Required) <br>[Gemini: A Family of Highly Capable Multimodal Models](https://arxiv.org/abs/2312.11805) |[skatt24, akhils7, adit3, nu4](./Slides/training_infra.pptx) |pokkali2, echen48, cy5, keshav6, wendi2|ruip4, yy28, xinzhuo4, shengya4, enguang2|
| Feb 19 <br>(Model Parallelism)  | [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053) (Required) <br>[Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://www.usenix.org/conference/osdi22/presentation/zheng-lianmin) (Required)<br>[LightSeq: Sequence Level Parallelism for Distributed Training of Long Context Transformers](https://openreview.net/pdf?id=qScA3fL49l) |kcli2, adita3, vsikand2, amaanmk2, jbyju2|gera3, dhruvk5, anua2, ppikale2, ritikh2|apirani2, divyam4, aryanb3, amang7|
| Feb 21 <br>(Infra for Parallelism)  | [MegaScale: Scaling Large Language Model Training to More Than 10,000 GPUs](https://arxiv.org/abs/2402.15627) (Required)<br>[RDMA over Ethernet for Distributed AI Training at Meta Scale](https://dl.acm.org/doi/10.1145/3651890.3672233) (Required)<br>[GEMINI: Fast Failure Recovery in Distributed Training with In-Memory Checkpoints](https://www.cs.rice.edu/~eugeneng/papers/SOSP23.pdf) |[srm17, apillai7, dhruva7, mihirss3](./Slides/training_infra.pptx)|siyuanc3, jiaweig3, xm20, sm138, mayankb3|haoyuc7, zihanz23, scui8, yiliut2|
| Feb 26 <br>(Energy Efficiency)  | [Perseus: Removing Energy Bloat from Large Model Training](https://arxiv.org/abs/2312.06902) (Required)<br>[Power-aware Deep Learning Model Serving with μ-Serve](https://www.usenix.org/system/files/atc24-qiu.pdf) (Required)<br>[GREEN: Carbon-efficient Resource Scheduling for Machine Learning Clusters]() |[asanaka2, imathur3, abhakat2, gdurand2, jgosar2](./Slides/energy.pdf)|amitp4, deeyaab2, lneti2, rishis5, sdedhia2|colincl2, adishj2, bwz2, hshen14, zhong42|
| Feb 28 <br>(Training Simulation)  | [SimAI: Unifying Architecture Design and Performance Tunning for Large-Scale Large Language Model Training with Scalability and Precision](https://ennanzhai.github.io/pub/nsdi25spring-simai.pdf) (Required)<br>[Vidur: A large-scale simulation framework for LLM inference](https://apanwariisc.github.io/publications/mlsys-2024-vidur/vidur_mlsys24.pdf) (Required)<br>[Pathways: Asynchronous Distributed Dataflow for ML](https://proceedings.mlsys.org/paper_files/paper/2022/hash/37385144cac01dff38247ab11c119e3c-Abstract.html) | [haoyuc7](./Slides/sim.pptx)|skatt24, akhils7, adit3, nu4 |allent3, nhari7, ps92, rohitmb2, vdas3|
| | **Alignment & Post-Training Optimization**  
| Mar 5 <br>(Sys for RLHF)  | [​​Training language models to follow instructions with human feedback](https://arxiv.org/pdf/2203.02155) (Required)<br>[RLHFuse: Efficient RLHF Training for Large Language Models with Inter- and Intra-Stage Fusion](https://arxiv.org/abs/2409.13221) (Required)<br>[Direct Preference Optimization: Your Language Model is Secretly a Reward Model](https://arxiv.org/abs/2305.18290) | [dhanker2, nishkdp2, arthurw3, danhn3, ytelang2](./Slides/rlhf.pptx)|kcli2, adita3, vsikand2, amaanmk2, jbyju2|ogurjar2, akshat7, bingxum2, jvsingh2|
| Mar 7 <br>(Serving LoRAs) | [LoRA: Low-Rank Adaptation of Large Language Models](https://openreview.net/forum?id=nZeVKeeFYf9) (Required)<br>[dLoRA: Dynamically Orchestrating Requests and Adapters for LoRA LLM Serving](https://www.usenix.org/system/files/osdi24-wu-bingyang.pdf) (Required)<br>[Stylus: Automatic Adapter Selection for Diffusion Models](https://arxiv.org/abs/2404.18928) |[pw26, benhaol2, ruiming5, zhiruig2, ziyue14](./Slides/lora.pptx)|apirani2, divyam4, aryanb3, amang7|pokkali2, echen48, cy5, keshav6, wendi2|
| Mar 12 <br>(Quantization) | [LLM.int8(): 8-bit Matrix Multiplication for Transformers at Scale](https://arxiv.org/abs/2208.07339) (Required)<br>[AWQ: Activation-aware Weight Quantization for On-Device LLM Compression and Acceleration](https://arxiv.org/abs/2306.00978) (Required)<br>[GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323) |ruip4, yy28, xinzhuo4, shengya4, enguang2|dhanker2, nishkdp2, arthurw3, danhn3, ytelang2|gera3, dhruvk5, anua2, ppikale2, ritikh2|
| | **Grounding**
| Mar 14 <br>(Optimizing Throughput)  | [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://dl.acm.org/doi/10.1145/3600006.3613165) (Required)<br>[Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://arxiv.org/abs/2403.02310) (Required)<br>[SGLang: Efficient Execution of Structured Language Model Programs](https://arxiv.org/abs/2312.07104) |siyuanc3, jiaweig3, xm20, sm138, mayankb3 |haoyuc7, zihanz23, scui8, yiliut2|tratiya2, arjunpn2, abajpai2, knguye71, dhekane2|
| Mar 26 <br>(Optimizing User Experience)  | [PowerInfer: Fast Large Language Model Serving with a Consumer-grade GPU](https://arxiv.org/abs/2312.12456) (Required)<br>[Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services (Required)](https://arxiv.org/abs/2404.16283) (Required)<br>[LLM in a flash: Efficient Large Language Model Inference with Limited Memory](https://arxiv.org/abs/2312.11514) |allent3, nhari7, ps92, rohitmb2, vdas3|ruip4, yy28, xinzhuo4, shengya4, enguang2|dhanker2, nishkdp2, arthurw3, danhn3, ytelang2|
| Mar 28 | **Mid-Semester Presentations** |           |           |          |
| Apr 2  | **Mid-Semester Presentations** |           |           |          |
| Apr 4  | **Mid-Semester Presentations** |           |           |          |
| | **Inference**
| Apr 9 <br>(RAG)   | [REALM: Retrieval-Augmented Language Model Pre-Training](https://proceedings.mlr.press/v119/guu20a.html) (Required)<br>[CacheBlend: Fast Large Language Model Serving for RAG with Cached Knowledge Fusion](https://arxiv.org/abs/2405.16444) (Required)<br>[MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) |yihanz8, hanbog2, zeyang2, xinyuc10, cmo8, mf46|ogurjar2, akshat7, bingxum2, jvsingh2|siyuanc3, jiaweig3, xm20, sm138, mayankb3 |
| Apr 11 <br>(KV Cache)   | [SnapKV: LLM Knows What You are Looking for Before Generation](https://arxiv.org/abs/2404.14469) (Required)<br>[H2O: Heavy-Hitter Oracle for Efficient Generative Inference of Large Language Models](https://arxiv.org/abs/2306.14048) (Required)<br>[Efficient Streaming Language Models with Attention Sinks](https://arxiv.org/abs/2309.17453) |tratiya2, arjunpn2, abajpai2, knguye71, dhekane2|pw26, benhaol2, ruiming5, zhiruig2, ziyue14|asanaka2, imathur3, abhakat2, gdurand2, jgosar2|
| Apr 16 <br>(Caching GenAI)  | [Approximate Caching for Efficiently Serving Text-to-Image Diffusion Models](https://arxiv.org/abs/2312.04429) (Required)<br>[EchoLM: Accelerating LLM Serving with Real-time Knowledge Distillation](https://arxiv.org/abs/2501.12689) (Required)<br>[CacheGen: KV Cache Compression and Streaming for Fast Large Language Model Serving](https://arxiv.org/abs/2310.07240) |ogurjar2, akshat7, bingxum2, jvsingh2|srm17, apillai7, dhruva7, mihirss3|jiaxili3, xinyue21, dk31, zihengc3|
| Apr 18 <br>(Compound AI)  | [OMS-DPM: Optimizing the Model Schedule for Diffusion Probabilistic Models](https://arxiv.org/abs/2306.08860) (Required)<br>[Self-Reflection in LLM Agents: Effects on Problem-Solving Performance](https://arxiv.org/abs/2405.06682) (Required)<br>[Vulcan: Automatic Query Planning for Live ML Analytics](https://www.usenix.org/system/files/nsdi24-zhang-yiwen.pdf) |gera3, dhruvk5, anua2, ppikale2, ritikh2|yihanz8, hanbog2, zeyang2, xinyuc10, cmo8, mf46|pw26, benhaol2, ruiming5, zhiruig2, ziyue14|
| Apr 23 <br>(LLM for Systems)  | [NetLLM: Adapting Large Language Models for Networking](https://arxiv.org/abs/2402.02338) (Required)<br>[Is Your Code Generated by ChatGPT Really Correct? Rigorous Evaluation of Large Language Models](https://arxiv.org/abs/2305.01210) (Required)<br>[LLM-ABR: Designing Adaptive Bitrate Algorithms via Large Language Models](https://arxiv.org/pdf/2404.01617) |jiaxili3, xinyue21, dk31, zihengc3|allent3, nhari7, ps92, rohitmb2, vdas3|kcli2, adita3, vsikand2, amaanmk2, jbyju2|
| Apr 25 <br>(New LLM Paradigms)  | [Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters](https://arxiv.org/abs/2408.03314) (Required)<br>[Linear-Time Sequence Modeling with Selective State Spaces](https://arxiv.org/abs/2312.00752) (Required)<br>[MiniMax-01: Scaling Foundation Models with Lightning Attention](https://arxiv.org/pdf/2501.08313) |colincl2, adishj2, bwz2, hshen14, zhong42|tratiya2, arjunpn2, abajpai2, knguye71, dhekane2|yihanz8, hanbog2, zeyang2, xinyuc10, cmo8, mf46|
| Apr 30  | **Final Presentations** |           |           |          |
| May 2   | **Final Presentations** |           |           |          |
| May 7  | **Final Presentations** |           |           |          |
| May 15   | **Final Report Submission Deadline** |           |           |          |

 
 ## Tentative Grading
**Groups**:  All activities of this course, except your own participation :), will be performed in groups of 4-5 students. Form a group and [declare your group's membership and paper preferences](https://forms.gle/hShgRG9mcfC8fm9d8) by **Jan 31**. After this date, we will form groups from the remaining students.

|                         | Weight | 
| ------------------------| ------:| 
| [Participation](#required-reading)           | 15%    | 
| [Paper Presentation](#student-lectures) & [Discussion](#post-presentation_panel_discussion)     | 15%    | 
| [Paper Summary](#lecture-summaries)           | 10%    | 
| [Project Proposal](#project)          | 5%    | 
| [Project Mid-Semester Presentations](#project)   | 10%    |
| [Project Final Presentations](#project)   | 10%    |
| [Project Final Report](#project)          | 35%    | 

**Academic integrity**: [The University's Honor Code](https://siebelschool.illinois.edu/academics/honor-code) applies to all activities related to this course. All material you submit in this course (reading responses, project reports, and presentation materials) must be your own. If you use someone else’s material, you must cite them properly. 

**AI Tool Policy**: AI tools may be used for grammar checking and refining initial brainstorms, but the final reviews and codes **must** be authored by the student. Students are responsible for the entire content and must adhere to the Academic Integrity Policy.

## Policies

### Participation
**Before Each Lecture**: Each lecture will include one or two required reading that everyone must read.   There will be *optional related reading(s)* that only the presenter(s) should be familiar with. They are optional for the rest of the class.  You are required to [submit](https://forms.gle/KA1AsBF46UiGouu88) **one insightful question** for each presented papers before each lecture. 

**During Lectures**: Active participation is crucial for both your own understanding and to improve the overall quality of the course. You are expected to attend **all** lectures (up to 2 absences allowed for legitimate reasons), and more importantly, participate in class discussions. Not everyone must have add something every day, but it is expected that everyone has something to share over the semester.

**After Lectures**: Participation also involves contributing to discussions on Piazza. The group responsible for the summary should initiate the (remaining) discussion, and the rest of the members are encouraged to participate.

### Student Lectures
The course will be conducted as a seminar. Only one group will present in each class. Each group will be assigned *at least one lecture* over the course of the semester. Presentations should last **at most 40 minutes** without interruption.
However, presenters should expect questions and interruptions throughout. 

In the presentation, you should:

* Provide a brief background to motivate the problem (e.g., simplifying this by referencing previous talks)
* Present the high level idea, approach, and/or insight (using examples, whenever appropriate) in the required reading. 
* Discuss technical details so that one can understand key details without carefully reading (quickly skim the evaluations).
* Explain the differences between related works as well as the additional reading.
* Identify strengths and weaknesses of the required reading and propose directions of future research.

*The slides for a presentation must be emailed to the instructor team (in \*.pptx format) at least 24 hours prior to the corresponding class.* 

### Post-Presentation Panel Discussion 
To foster a deeper understanding of the papers and encourage critical thinking, each lecture will be followed by a panel discussion. This discussion will involve three distinct roles played by different student groups, simulating an interactive and dynamic scholarly exchange.

#### Roles and Responsibilities

1. **The Authors**
- Group Assignment: The 'Companion' group will write the summary and play the role of the paper's authors.
- Responsibility: As authors, you are expected to defend your paper against critiques, answer questions, and discuss how you might improve or extend your research in the future, akin to writing a rebuttal during the peer-review process.


2. **The Reviewers**
- Group Assignment: The 'Reviewer' group will write the summary and will be assigned to one slot to play the role of reviewers.
- Responsibility: Reviewers critically assess the paper, posing challenging questions and highlighting potential weaknesses or areas for further investigation. 
Your goal is to engage in a constructive critique of the paper, simulating a peer review scenario.

 
3. **Rest of the Class** (including the presenters)
- Responsibility: During the panel discussions, feel free to actively **ask questions** and engage in the dialogue. 


### Lecture Summaries
Each group will also be assigned to **write summaries for roughly two lectures**: one in the 'Companion' role and the other in the 'Reviewer' role.
The summary assigned to a group will not be the reading they gave the lecture on.

A paper summary must address the following four questions in sufficient details (2-3 pages):

* What is the problem addressed in the lecture, and why is this problem important?
* What is the state of related works in this topic?
* What is the proposed solution, and what key insight guides their solution?
* What is one (or more) drawback or limitation of the proposal?
* What are potential directions for future research?

**Late reviews will not be counted.** *The paper summary of a paper must be emailed to the instructor team within 24 hours after its presentation.*  

You should use [this format](Summaries/Template.pdf) for writing your summary. Use Google doc to enable in-line comments and suggestions.

*Allocate enough time for your reading, discuss as a group, write the summary carefully, and finally, include key observations from the class discussion.*

### Project
You will have to complete substantive work an instructor-approved problem and have original contribution. Surveys are not permitted as projects; instead, each project must contain a survey of background and related work.

You must meet the following milestones (unless otherwise specified in future announcements) to ensure a high-quality project at the end of the semester:

* Turn in a 2-page draft proposal ([template](https://www.overleaf.com/read/bsrcbphcvyzc#d075e8)), plus as many pages as needed for references, by **February 26**. Remember to include the names and UIUC email addresses of the group members. 
* Each group must present mid-semester progress during class hours on **April 2 and April 4**.
* Each group must turn in an 8-page final report and your code via email **on or before 6:00PM CST on May 15.** The report must be submitted as a PDF file, with formatting similar to that of the papers you've read in the class. The self-contained (i.e., include ALL dependencies) code must be submitted as a zip file. Each zip file containing the code must include a README file with a step-by-step guide on how to compile and run the provided code.
* You can find how to access GPU resources [here](./Resources/cloudlab.md)

### **Acknowledgements**
This course is heavily inspired by other excellent system seminar courses, particularly [UMich CSE 585](https://github.com/mosharaf/eecs598/tree/w24-genai). Acknowledgments to [SymbioticLab](https://symbioticlab.org/).	
