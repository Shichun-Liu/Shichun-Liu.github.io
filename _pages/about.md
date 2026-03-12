---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

<!--
 My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
-->
I'm currently a Master's degree student (from September 2024) at the [School of Computer Science](https://cs.fudan.edu.cn/) of [Fudan University](https://www.fudan.edu.cn/) and a member of the [FudanNLP Lab](https://nlp.fudan.edu.cn/), co-advised by Prof. [Xuanjing Huang (黄萱菁)](https://xuanjing-huang.github.io/) and Associate Prof. [Tao Gui(桂 韬)](https://guitaowufeng.github.io/). Previously, I got my bachelor's degree in June 2024 from Fudan University, advised by Associate Prof. [Tao Gui](https://guitaowufeng.github.io/).

My previous research focused on **model reasoning** and **reward modeling**, and I am currently concentrating on **agent memory**. Feel free to reach out via [email✉️](mailto:liusc2020@gmail.com) or [RedNote (小红书)](https://xhslink.com/m/CWTAntd2dt) — I'm always open to academic discussions of any kind! 👏🏻

# 🔥 News

- *2026.01*: &nbsp;🎉🎉 **OctoBench** (benchmark for scaffold-aware instruction following in agentic coding) is released on [arXiv](https://arxiv.org/abs/2601.10343)!
- *2025.12*: &nbsp;🎉🎉 Our comprehensive survey on **Memory in the Age of AI Agents** is released on [arXiv](https://arxiv.org/abs/2512.13564)!
- *2025.09*: &nbsp;🎉🎉 **POLAR** and **Evalearn** are accepted by **NeurIPS 2025**!
- *2025.07*: &nbsp;🎉🎉 Our paper on Reward Model Pre-training, **POLAR**, is now available on [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2407.05197)!
- *2024.05*: &nbsp;🎉🎉 One paper on math reasoning & RL was accepted by **ICML-2024**!
- *2024.03*: &nbsp;🎉🎉 One paper on in-context learning was accepted by **NAACL-2024-Findings**!
- *2023.12*: &nbsp;🎉🎉 One paper on evaluation was accepted by **AAAI-2024**!


# 💻 Internships
<!-- - <span style="display: inline-flex; align-items: center; justify-content: center; width: 160px; height: 75px; vertical-align: middle; margin-right: 10px;"><img src="/images/N-logo-white.png" alt="NexAGI" style="max-width: 160px; max-height: 50px;"></span><span style="display: inline-block; vertical-align: middle;">**2025.3 - Present**<br>Algorithm Researcher at NexAGI (Shanghai Qiji Zhifeng Co., Ltd.)<br>Shanghai, China</span> -->
- <span style="display: inline-flex; align-items: center; justify-content: center; width: 160px; height: 75px; vertical-align: middle; margin-right: 10px;"><img src="/images/shanghai-ai-lab.png" alt="Shanghai AI Lab" style="max-width: 160px; max-height: 50px;"></span><span style="display: inline-block; vertical-align: middle;">**2025.1 - 2025.3**<br>Large Language Model Center Group of [Shanghai Artificial Intelligence Laboratory](https://www.shlab.org.cn/)<br>Shanghai, China.</span>
- <span style="display: inline-flex; align-items: center; justify-content: center; width: 160px; height: 75px; vertical-align: middle; margin-right: 10px;"><img src="/images/bytedance.png" alt="Bytedance" style="max-width: 160px; max-height: 50px;"></span><span style="display: inline-block; vertical-align: middle;">**2024.8 - 2024.12**<br>Bytedance, AI Lab Research<br>Shanghai, China</span>
- <span style="display: inline-flex; align-items: center; justify-content: center; width: 160px; height: 75px; vertical-align: middle; margin-right: 10px;"><img src="/images/shanghai-ai-lab.png" alt="Shanghai AI Lab" style="max-width: 160px; max-height: 50px;"></span><span style="display: inline-block; vertical-align: middle;">**2023.12 - 2024.3**<br>General Safety Group of [Shanghai Artificial Intelligence Laboratory](https://www.shlab.org.cn/)<br>Shanghai, China.</span>


# 📝 Publications

## **L3-Agent**

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv 2026</div><img src='../images/octobench.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### OctoBench: Benchmarking Scaffold-Aware Instruction Following in Repository-Grounded Agentic Coding

Deming Ding\*, **Shichun Liu**\*, Enhui Yang\*, Jiahang Lin\*, Ziying Chen, Shihan Dou, Honglin Guo, Weiyu Cheng, Pengyu Zhao, Chengjun Xiao, Qunhong Zeng, Qi Zhang, Xuanjing Huang, Qidi Xu, Tao Gui

- Modern coding scaffolds turn LLMs into capable software agents, but their ability to follow scaffold-specified instructions remains under-examined. OctoBench benchmarks scaffold-aware instruction following in repository-grounded agentic coding.
- OctoBench includes 34 environments and 217 tasks under three scaffold types, with 7,098 objective checklist items. We release an automated observation-and-scoring toolkit for full trajectories and fine-grained checks.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/abs/2601.10343) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/MiniMax-AI/mini-vela)

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv 2025</div><img src='../images/memory-main.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### Memory in the Age of AI Agents: A Survey

Yuyang Hu<small>†</small>, **Shichun Liu**<small>†</small>, Yanwei Yue<small>†</small>, Guibin Zhang<small>†</small>, etc.
<br><small>†Core Contributors with Names Listed Alphabetically.</small>

- Memory serves as the cornerstone of foundation model-based agents, underpinning their ability to perform long-horizon reasoning, adapt continually, and interact effectively with complex environments.
- We provide a comprehensive overview through three unified lenses: Forms, Functions, and Dynamics.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/abs/2512.13564) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/Shichun-Liu/Agent-Memory-Paper-List) ![GitHub Repo stars](https://img.shields.io/github/stars/Shichun-Liu/Agent-Memory-Paper-List) \| [![Semantic Scholar Citations](https://img.shields.io/badge/dynamic/json?label=Citations&query=%24.citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fd362b7619fcd2df4241696a19aec95961b8a729c%3Ffields%3DcitationCount&logo=semanticscholar&cacheSeconds=3600)](https://www.semanticscholar.org/paper/d362b7619fcd2df4241696a19aec95961b8a729c) \| [![](https://img.shields.io/badge/Blog-fff?logo=xiaohongshu&logoColor=FF2442)](https://www.xiaohongshu.com/discovery/item/69427b8e000000001b023288?source=webshare&xhsshare=pc_web&xsec_token=ABng7EtxkaQGMXTBKE23fzy2OLIRXgeVqKSp9cTzQD9YU=&xsec_source=pc_share) 

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv 2025</div><img src='../images/nex-n1.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">


### Nex-N1: Agentic Models Trained via a Unified Ecosystem for Large-Scale Environment Construction

Nex-AGI Team: Yuxuan Cai, Lu Chen, ..., **Shichun Liu**, ..., Xuanjing Huang, Xipeng Qiu

- We introduce a comprehensive method designed to systematically scale the diversity and complexity of interactive environments through three orthogonal dimensions: Complexity (NexAU), Diversity (NexA4A), and Fidelity (NexGAP).
- Nex-N1 consistently outperforms SOTA open-source models and achieves competitive performance against frontier proprietary models on complex agentic tasks (SWE-bench, tau2).
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/abs/2512.04987)

</div>
</div>




<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS 25</div><img src='../images/evalearn.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### EvaLearn: Quantifying the Learning Capability and Efficiency of LLMs via Sequential Problem Solving

Shihan Dou, Ming Zhang, Chenhao Huang, Jiayi Chen, Feng Chen, **Shichun Liu**, Yan Liu, Chenxiao Liu, Cheng Zhong, Zongzhang Zhang, Tao Gui, Chao Xin, Wei Chengzhi, Lin Yan, Qi Zhang, Yonghui Wu, Xuanjing Huang

- We introduce **EvaLearn**, a benchmark to evaluate the learning capability of LLMs through sequential problem-solving, where models learn from prior experience.
- It features 648 problems in 182 sequences and five metrics, revealing that static ability doesn't always correlate with learning capability, thus offering a new dimension for model evaluation.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/abs/2506.02672) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/ByteDance-Seed/EvaLearn)

</div>
</div>

## L2-Reasoner


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS 25</div><img src='../images/POLAR_method.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### POLAR: Pre-Trained Policy Discriminators are General Reward Models

Shihan Dou\*<small>‡</small>, **Shichun Liu**\*<small>‡</small>, Yuming Yang\*, Yicheng Zou\*<small>†</small>, Yunhua Zhou, Shuhao Xing, Chenhao Huang, Qiming Ge, Demin Song, Haijun Lv, Songyang Gao, Chengqi Lv, Enyu Zhou, Honglin Guo, Zhiheng Xi, Wenwei Zhang, Qipeng Guo, Qi Zhang, Xipeng Qiu, Xuanjing Huang, Tao Gui<small>†</small>, Kai Chen<small>†</small>
<br><small>\*Equal contributions. †Corresponding authors. ‡Work done during an internship at Shanghai AI Laboratory.</small>

- Say goodbye to reward models with poor generalization! POLAR (Policy Discriminative Learning) is a groundbreaking pre-training paradigm that trains reward models to distinguish policy distributions, eliminating heavy reliance on human preference data!
- Highly scalable and tailored for Reinforcement Fine-tuning (RFT)! POLAR assigns rewards based on ground truths, seamlessly integrating into the RFT framework and significantly reducing reward hacking across general tasks!
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2507.05197) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/InternLM/POLAR) ![GitHub Repo stars](https://img.shields.io/github/stars/InternLM/POLAR) \| [![](https://img.shields.io/badge/Model-fff?logo=huggingface&logoColor=000)](https://huggingface.co/internlm/POLAR-7B)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ACL 2025</div><img src='../images/lost-in-the-context.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### Lost in the Context: Insufficient and Distracted Attention to Contexts in Preference Modeling

Shihan Dou\*, Jiayi Chen\*, Chenhao Huang\*, Feng Chen, Wei Chengzhi, Huiyuan Zheng, **Shichun Liu**, Yan Liu, Chenxiao Liu, Chao Xin, Lin Yan, Zongzhang Zhang, Tao Gui, Qi Zhang, Xuanjing Huang

- The reward model (RM) in RLHF often overlooks crucial context, leading to poor preference alignment. We find that the RM allocates insufficient attention to the context and ignores relevant segments. 
- To address this, we propose **AttnRM**, a novel optimization framework that directs the RM's focus to important contextual information. Experimental results show that AttnRM significantly enhances preference modeling, generalizability, and alignment with human preferences.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://aclanthology.org/2025.acl-long.285/)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NAACL 2024</div><img src='../images/self-demos-overview.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### Self-Demos: Eliciting Out-of-Demonstration Generalizability in Large Language Models

Wei He, **Shichun Liu**, Jun Zhao, Yiwen Ding, Yi Lu, Zhiheng Xi, Tao Gui, Qi Zhang, Xuanjing Huang.

- Goal: develop a method that can enhance the generalizability of LLMs when encountering OOD queries, allowing them to better adapt to novel tasks.
- Through extensive experiments on the tool-using scenario (OOD-Toolset) and mathematical problem-solving tasks (GSM8K and MATH datasets), SELF-DEMOS demonstrated superior performance in handling OOD queries compared to existing state-of-the-art methods.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2404.00884) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/hewei2001/Self-Demos) 
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICML 2024</div><img src='../images/r3.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### Training Large Language Models for Reasoning through Reverse Curriculum Reinforcement Learning

Zhiheng Xi\*, Wenxiang Chen\*, Boyang Hong\*, Senjie Jin\*, Rui Zheng, Wei He, Yiwen Ding, **Shichun Liu**, Xin Guo, Junzhe Wang, Honglin Guo, Wei Shen, Xiaoran Fan, Yuhao Zhou, Shihan Dou, Xiao Wang, Xinbo Zhang, Peng Sun, Tao Gui, Qi Zhang, Xuanjing Huang

- We propose **R3**, a novel method that achieves the benefits of process supervision using only outcome supervision. R3 learns reasoning via a reverse curriculum, progressively moving from easy to hard tasks and enabling precise, step-level feedback.
- Our method surpasses RL baselines on eight reasoning tasks by 4.1 points on average, and with CodeLlama-7B, it performs comparably to much larger models without extra data.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2402.05808) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/WooooDyy/LLM-Reverse-Curriculum-RL)

</div>
</div>

<!-- - ![](https://img.shields.io/badge/ACL--Demo--2025-darkblue) **Multi-Programming Language Sandbox for LLMs**
<br> Shihan Dou\*, Jiazheng Zhang\*, Jianxiang Zang\*, Yunbo Tao, Weikang Zhou, Haoxiang Jia, **Shichun Liu**, Yuming Yang, Shenxi Wu, Zhiheng Xi, Muling Wu, Rui Zheng, Changze Lv, Limao Xiong, Shaoqing Zhang, Lin Zhang, Wenyu Zhan, Rongxiang Weng, Jingang Wang, Xunliang Cai, Yueming Wu, Ming Wen, Yixin Cao, Tao Gui, Xipeng Qiu, Qi Zhang, Xuanjing Huang
<br> [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://aclanthology.org/2025.acl-demo.5.pdf) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/Ablustrund/MPLSandbox) -->

## L1-Chatbot

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">AAAI 2024</div><img src='../images/llmeval.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### LLMEval: A Preliminary Study on How to Evaluate Large Language Models

Yue Zhang\*, Ming Zhang\*, Haipeng Yuan, **Shichun Liu**, Yongyao Shi, Tao Gui, Qi Zhang, Xuanjing Huang

- Addresses the crucial "how to evaluate" question for LLMs, analyzing various criteria, scoring methods, and ranking systems.
- Introduces the LLMEval dataset, based on evaluations of 20 LLMs with over 240,000 manual annotations, and offers 10 key insights for future evaluation.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2312.07398) \| [![](https://img.shields.io/badge/Code-fff?logo=github&logoColor=000)](https://github.com/llmeval)

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv 2023</div><img src='../images/eval-gpt3a5.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### A Comprehensive Capability Analysis of GPT-3 and GPT-3.5 Series Models

Junjie Ye\*, Xuanting Chen\*, Nuo Xu, Can Zu, Zekai Shao, **Shichun Liu**, Yuhan Cui, Zeyang Zhou, Chao Gong, Yang Shen, Jie Zhou, Siming Chen, Tao Gui, Qi Zhang, Xuanjing Huang

- We analyze the capability evolution of six GPT-3 and GPT-3.5 models on 21 NLU datasets.
- Our findings reveal that model capabilities do not uniformly improve with evolution, as strategies like RLHF can sometimes compromise performance on specific tasks while enhancing others.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2303.10420)

</div>
</div>


<!-- - ![](https://img.shields.io/badge/EMNLP--2024-darkblue) **TransferTOD: A Generalizable Chinese Multi-Domain Task-Oriented Dialogue System with Transfer Capabilities**
<br> Ming Zhang\*, Caishuang Huang\*, Yilong Wu\*, **Shichun Liu**, Huiyuan Zheng, Yurui Dong, Yujiong Shen, Shihan Dou, Jun Zhao, Junjie Ye, Qi Zhang, Tao Gui, Xuanjing Huang
<br> [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/pdf/2407.21693) -->


# 🎖 Honors and Awards
- *2024.06*，the Top Students Award in Computer Science in recognition of his exceptional academic performance in the National Top Talent Undergraduate Training Program.
- *2022.09*, the First prize (Top 0.6% of 49242 teams) of Contemporary Undergraduate Mathematical Contest in Modeling (CUMCM).
- *2021.12*, the Second Prize of the Scholarship for Outstanding Students at Fudan University in the 2020-2021 academic year.
- *2021.12*, the Second Prize Winner(Non-Physics A) in the 38th National Physics Competition for College Students.
- *2021.12, 2022.12*, the Second Prize Winner(Non-Math) in the 13, 14th National Mathematics Competition for College Students.


# 📖 Educations
- *2020.9 - 2024.6*, B.E. at Fudan University with a major in computer science and technology.


<!--
# 💬 Invited Talks
-->

# 💡Services
- Reviewer of ACL, NeurIPS.

# 🌏 Visitors

<div style="width: 15%; margin: auto;">
  <script type="text/javascript" id="clustrmaps" src="//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=300&t=tt&d=CbEyd1rFdqDWDFWN0o0y_IErdS84uYJElpB6uRCQPyI"></script>
</div>
