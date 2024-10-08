# Paper List for In-context Learning

<!-- omit in toc -->

## Contents

- [Paper List for In-context Learning](#paper-list-for-in-context-learning)
  - [Contents](#contents)
  - [Introduction](#introduction)
    - [Keywords Convention](#keywords-convention)
  - [Papers](#papers)
    - [Survey](#survey)
    - [Model Training for ICL](#model-warmup-for-icl)
      - [Pre-training](#pre-training)
      - [Warmup](#warmup)
    - [Prompt Tuning for ICL](#prompt-tuning-for-icl)
    - [Analysis of ICL](#analysis-of-icl)
      - [Influence Factors for ICL](#influence-factors-for-icl)
        - [Pre-training Stage](#pre-training-stage)
        - [Inference Stage](#inference-stage)
      - [Working Mechanism of ICL](#working-mechanism-of-icl)
    - [Evaluation and Resources](#evaluation-and-resources)
    - [Application](#application)
    - [Problems](#problems)
    - [Challenges and Future Directions](#challenges-and-future-directions)
  - [Blogs](#blogs)
  - [How to contribute?](#how-to-contribute)
  - [Reference](#reference)

## Introduction

This is a paper list (working in progress) about **In-context learning**

<!-- , for the following paper:

> [**A Survey for In-context Learning**](https://arxiv.org/abs/2301.00234),
> Qingxiu Dong, Lei Li, Damai Dai, Ce Zheng, Zhiyong Wu, Baobao Chang, Xu Sun, Jingjing Xu, Lei Li, Zhifang Sui.
> *arXiv preprint ([arXiv 2301.00234](https://arxiv.org/abs/2301.00234))* -->

### Keywords Convention

![](https://img.shields.io/badge/MetaICL-DCE7F1) abbreviation

![](https://img.shields.io/badge/Analysis-EAD8D9) section in our survey

![](https://img.shields.io/badge/MetaTraining-D8D0E1) main feature

![](https://img.shields.io/badge/ACL2022CL2022-FAEFCA) conference

## Papers

### Survey

1. **A Survey for In-context Learning**. ![](https://img.shields.io/badge/ICL_survey-DCE7F1)

   *Qingxiu Dong, Lei Li, Damai Dai, Ce Zheng, Zhiyong Wu, Baobao Chang, Xu Sun, Jingjing Xu, Lei Li, Zhifang Sui*.  [[pdf](https://arxiv.org/abs/2301.00234)], 2022.12, ![](https://img.shields.io/badge/arxiv-FAEFCA)

### Model Training for ICL

This section contains the pilot works that might contributes to the training strategies of ICL.


#### Pre-training
1. **MEND: meta demonstration distillation for efficient and effective in-context learning.** ![](https://img.shields.io/badge/MEND-DCE7F1)
    *Yichuan Li, Xiyao Ma, Sixing Lu, Kyumin Lee, Xiaohu Liu, Chenlei Guo.* [[pdf](https://arxiv.org/pdf/2403.06914)], [[project](https://github.com/bigheiniu/MEND)], 2024.3, ![](https://img.shields.io/badge/ICLR2024-FAEFCA) 
2. **Pre-training to learn in context.** ![](https://img.shields.io/badge/PICL-DCE7F1)
   *Yuxian Gu, Li Dong, Furu Wei, Minlie Huang.* [[pdf](https://arxiv.org/pdf/2305.09137.pdf)], [[project](https://github.com/thu-coai/PICL)], 2023.7, ![](https://img.shields.io/badge/ACL2023-FAEFCA)
3. **In-context pretraining: Language modeling beyond document boundaries.** ![](https://img.shields.io/badge/ICLM-DCE7F1) 
   *Weijia Shi, Sewon Min, Maria Lomeli, Chunting Zhou, Margaret Li, Gergely Szilvasy, Rich James, Xi Victoria Lin, Noah A. Smith, Luke Zettlemoyer, Scott Yih, Mike Lewis.* [[pdf](https://arxiv.org/pdf/2310.10638)], [[project](https://github.com/swj0419/in-context-pretraining)], 2023.7, ![](https://img.shields.io/badge/ICLR2024-FAEFCA)


#### Warmup

1. **MetaICL: Learning to Learn In Context NAACL 2022 a pretrained language model is tuned to do in-context learning on a large set of training tasks.**. ![](https://img.shields.io/badge/MetaICL-DCE7F1)

   *Sewon Min, Mike Lewis, Luke Zettlemoyer, Hannaneh Hajishirzi*.  [[pdf](https://arxiv.org/pdf/2110.15943)], [[project](https://github.com/facebookresearch/metaicl)], 2021.10, ![](https://img.shields.io/badge/NAACL2022-FAEFCA)
   ![](https://img.shields.io/badge/Warmup-EAD8D9) ![](https://img.shields.io/badge/MetaTraining-D8D0E1)
2. **Improving In-Context Few-Shot Learning via Self-Supervised Training.**.

   *Mingda Chen, Jingfei Du, Ramakanth Pasunuru, Todor Mihaylov, Srini Iyer, Veselin Stoyanov, Zornitsa Kozareva*.  [[pdf](https://aclanthology.org/2022.naacl-main.260.pdf)], [[project]()], 2022.5, ![](https://img.shields.io/badge/NAACL2022-FAEFCA)
   ![](https://img.shields.io/badge/Warmup-EAD8D9) ![](https://img.shields.io/badge/Self_Supervised_Training-D8D0E1)
3. **Calibrate Before Use: Improving Few-shot Performance of Language Models.**.

   *Zihao Zhao, Eric Wallace, Shi Feng, Dan Klein, Sameer Singh*.  [[pdf](http://proceedings.mlr.press/v139/zhao21c.html)], [[project](https://github.com/tonyzhaozh/fewshot_learning)], 2021.2, ![](https://img.shields.io/badge/ICML2021-FAEFCA)
   ![](https://img.shields.io/badge/Warmup-EAD8D9) ![](https://img.shields.io/badge/additional_calibration_parameters-D8D0E1)

   - Using N/A string to calibrate LMs away from common token bias
4. **Symbol tuning improves in-context learning in language models.** ![](https://img.shields.io/badge/Symbol_tuning-DCE7F1)
   *Jerry Wei, Le Hou, Andrew Lampinen, Xiangning Chen, Da Huang, Yi Tay, Xinyun Chen, Yifeng Lu, Denny Zhou, Tengyu Ma, Quoc V. Le.*   [[pdf](https://arxiv.org/pdf/2305.08298)], [[project](https://github.com/tonyzhaozh/fewshot_learning)], 2023.5, ![](https://img.shields.io/badge/EMNLP2023-FAEFCA)
5. **Fine-tune language models to approximate unbiased in-context learning.** ![](https://img.shields.io/badge/RICL-DCE7F1)
   *Timothy Chu, Zhao Song, Chiwun Yang.* [[pdf](https://arxiv.org/pdf/2310.03331)], 2023.10, ![](https://img.shields.io/badge/arxiv-FAEFCA)

6. **ICL Markup: Structuring In-Context Learning using Soft-Token Tags.** ![](https://img.shields.io/badge/ICL_Markup-DCE7F1)
   *Marc-Etienne Brunet, Ashton Anderson, Richard Zemel.* [[pdf](https://arxiv.org/pdf/2312.07405)], 2023.12, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)


7. **Cross-task generalization via natural language crowdsourcing instructions.**
   *Swaroop Mishra, Daniel Khashabi, Chitta Baral, Hannaneh Hajishirzi.:* [[pdf](https://doi.org/10.18653/v1/2022.acl-long.244)], [[project](https://instructions.apps.allenai.org/)], 2022.5, ![](https://img.shields.io/badge/ACL2022-FAEFCA)


8. **Finetuned language models are zero-shot learners.**
   *Jason Wei, Maarten Bosma, Vincent Y. Zhao, Kelvin Guu, Adams Wei Yu, Brian Lester, Nan Du, Andrew M. Dai, Quoc V. Le.* [[pdf](https://openreview.net/pdf?id=gEZrGCozdqR)], 2021.9, ![](https://img.shields.io/badge/ICLR2022-FAEFCA)


9. **Scaling instruction-finetuned language models.**
    *Hyung Won Chung, Le Hou, Shayne Longpre, Barret Zoph, Yi Tay, William Fedus, Yunxuan Li, Xuezhi Wang, Mostafa Dehghani, Siddhartha Brahma, Albert Webson, Shixiang Shane Gu, Zhuyun Dai, Mirac Suzgun, Xinyun Chen, Aakanksha Chowdhery, Alex Castro-Ros, Marie Pellat, Kevin Robinson, Dasha Valter, Sharan Narang, Gaurav Mishra, Adams Yu, Vincent Zhao, Yanping Huang, Andrew Dai, Hongkun Yu, Slav Petrov, Ed H. Chi, Jeff Dean, Jacob Devlin, Adam Roberts, Denny Zhou, Quoc V. Le, Jason Wei* [[pdf](https://arxiv.org/pdf/2210.11416)], [[project](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints)], 2022.10, ![](https://img.shields.io/badge/arxiv-FAEFCA)

10. **Super-naturalinstructions: Generalization via declarative instructions on 1600+ nlp tasks.**
    *Yizhong Wang, Swaroop Mishra, Pegah Alipoormolabashi, Yeganeh Kordi, Amirreza Mirzaei, Atharva Naik, Arjun Ashok, Arut Selvan Dhanasekaran, Anjana Arunkumar, David Stap, Eshaan Pathak, Giannis Karamanolakis, Haizhi Gary Lai, Ishan Purohit, Ishani Mondal, Jacob Anderson, Kirby Kuznia, Krima Doshi, Kuntal Kumar Pal, Maitreya Patel, Mehrad Moradshahi, Mihir Parmar, Mirali Purohit, Neeraj Varshney, Phani Rohitha Kaza, Pulkit Verma, Ravsehaj Singh Puri, Rushang Karia, Savan Doshi, Shailaja Keyur Sampat, Siddhartha Mishra, Sujan Reddy A, Sumanta Patro, Tanay Dixit, Xudong Shen* [[pdf](https://aclanthology.org/2022.emnlp-main.340/)], [[project](https://instructions.apps.allenai.org/)], 2022.4, ![](https://img.shields.io/badge/EMNLP2022-FAEFCA)

11. **MAML-en-LLM: Model Agnostic Meta-Training of LLMs for Improved In-Context Learning.**
    *Sanchit Sinha, Yuguang Yue, Victor Soto, Mayank Kulkarni, Jianhua Lu, Aidong Zhang* [[pdf](https://dl.acm.org/doi/abs/10.1145/3637528.3671905)], 2024.5 ![](https://img.shields.io/badge/SIGKDD2024-FAEFCA)


### Prompt Tuning for ICL

This section contains the pilot works that might contributes to the prompt selection and prompt formulation strategies of ICL.

1. **On the Effect of Pretraining Corpora on In-context Learning by a Large-scale Language Model**.

   *Seongjin Shin, Sang-Woo Lee, Hwijeen Ahn, Sungdong Kim, HyoungSeok Kim, Boseop Kim, Kyunghyun Cho, Gichang Lee, Woomyoung Park, Jung-Woo Ha, Nako Sung*.  [[pdf](https://arxiv.org/abs/2204.13509)], 2022.04, ![](https://img.shields.io/badge/NAACL2022-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

   - how in-context learning performance changes as the training corpus varies, investigate the effects of the source and size of the pretraining corpus on in-context learning
2. **Chain of Thought Prompting Elicits Reasoning in Large Language Models**.

   *Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Brian Ichter, Fei Xia, Ed Chi, Quoc Le, Denny Zhou*.  [[pdf](https://arxiv.org/abs/2201.11903)], 2022.01, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)
3. **Least-to-Most Prompting Enables Complex Reasoning in Large Language Models**.

   *Denny Zhou, Nathanael Schärli, Le Hou, Jason Wei, Nathan Scales, Xuezhi Wang, Dale Schuurmans, Claire Cui, Olivier Bousquet, Quoc Le, Ed Chi*.  [[pdf](https://arxiv.org/abs/2205.10625)], 2022.05, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/section-EAD8D9)

4. **Self-Generated In-Context Learning: Leveraging Auto-regressive Language Models as a Demonstration Generator**.

   *Hyuhng Joon Kim, Hyunsoo Cho, Junyeob Kim, Taeuk Kim, Kang Min Yoo, Sang-goo Lee*.  [[pdf](https://arxiv.org/abs/2206.08082)], 2022.06, ![](https://img.shields.io/badge/NAACL_2022_Workshop-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

5. **Iteratively Prompt Pre-trained Language Models for Chain of Thought**.

   *Boshi Wang, Xiang Deng, Huan Sun*.  [[pdf](https://arxiv.org/abs/2203.08383)], [[project](https://github.com/sunlab-osu/iterprompt)], 2022.03, ![](https://img.shields.io/badge/EMNLP2022-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

6. **Automatic Chain of Thought Prompting in Large Language Models**.

   *Zhuosheng Zhang, Aston Zhang, Mu Li, Alex Smola*.  [[pdf](https://arxiv.org/abs/2210.03493)], [[project](https://github.com/amazon-research/auto-cot)], 2022.10, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

7. **Learning To Retrieve Prompts for In-Context Learning NAACL 2022 Learn an example retriever via contrastive learning**.

   *Ohad Rubin, Jonathan Herzig, Jonathan Berant*.  [[pdf](https://arxiv.org/abs/2112.08633)], [[project](https://github.com/ohadrubin/epr)], 2022.12, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

8. **Finetuned Language Models Are Zero-Shot Learners instruction tuning**.

   *Jason Wei, Maarten Bosma, Vincent Y. Zhao, Kelvin Guu, Adams Wei Yu, Brian Lester, Nan Du, Andrew M. Dai, Quoc V. Le*.  [[pdf](https://arxiv.org/abs/2109.01652)], [[project](https://github.com/google-research/flan)], 2021.09, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/prompt-EAD8D9)

   - finetuning language models on a collection of tasks described via instructions
   - substantially improves zero-shot performance on unseen tasks
  
9. **Active Example Selection for In-Context Learning**.

   *Yiming Zhang, Shi Feng, Chenhao Tan*.  [[pdf](https://arxiv.org/abs/2211.04486)], [[project](https://github.com/chicagohai/active-example-selection)], 2022.11, ![](https://img.shields.io/badge/arxiv-FAEFCA)

10. **Prompting GPT-3 To Be Reliable**![](https://img.shields.io/badge/New-EAD8D9)
    
    *Chenglei Si, Zhe Gan, Zhengyuan Yang, Shuohang Wang, Jianfeng Wang, Jordan Boyd-Graber, Lijuan Wang*.  [[pdf](https://arxiv.org/abs/2210.09150)], [[project](https://github.com/noviscl/gpt3-reliability)], 2022.10, ![](https://img.shields.io/badge/arxiv-FAEFCA)

11. **An lnformation-theoretic Approach to Prompt Engineering Without Ground Truth Labels** ![](https://img.shields.io/badge/New-EAD8D9)

    *Taylor Sorensen, Joshua Robinson, Christopher Rytting, Alexander Shaw, Kyle Rogers, Alexia Delorey, Mahmoud Khalil, Nancy Fulda, David Wingate*.  [[pdf](https://aclanthology.org/2022.acl-long.60/)], 2022.5, ![](https://img.shields.io/badge/ACL2022-FAEFCA)
      ![](https://img.shields.io/badge/prompt-EAD8D9)

12. **Self-adaptive In-context Learning** ![](https://img.shields.io/badge/New-EAD8D9)
    
    *Zhiyong Wu, Yaoxiang Wang, Jiacheng Ye, Lingpeng Kong*.  [[pdf](https://arxiv.org/abs/2212.10375)], [[project](https://github.com/shark-nlp/self-adaptive-icl)], 2022.12, ![](https://img.shields.io/badge/arxiv-FAEFCA)

13. **Demystifying Prompts in Language Models via Perplexity Estimation** ![](https://img.shields.io/badge/New-EAD8D9)
    
    *Hila Gonen, Srini Iyer, Terra Blevins, Noah A. Smith, Luke Zettlemoyer*.  [[pdf](https://arxiv.org/abs/2212.04037)], [[project](https://github.com/chicagohai/active-example-selection)], 2022.12, ![](https://img.shields.io/badge/arxiv-FAEFCA)

14. **Structured Prompting: Scaling In-Context Learning to 1,000 Examples**. ![](https://img.shields.io/badge/New-EAD8D9)
    
    *Yaru Hao, Yutao Sun, Li Dong, Zhixiong Han, Yuxian Gu, Furu Wei*. [[pdf](https://arxiv.org/abs/2212.06713)], [[project](https://github.com/microsoft/LMOps)], 2022.12. ![](https://img.shields.io/badge/arxiv-FAEFCA)

15. **Fantastically Ordered Prompts and Where to Find Them: Overcoming Few-Shot Prompt Order Sensitivity**.

   *Yao Lu, Max Bartolo, Alastair Moore, Sebastian Riedel, Pontus Stenetorp*.  [[pdf](https://arxiv.org/abs/2104.08786)], 2021.04, ![](https://img.shields.io/badge/ACL2021-FAEFCA) ![](https://img.shields.io/badge/Analysis-EAD8D9)

16. **On the Relation between Sensitivity and Accuracy in In-context Learning**.

   *Yanda Chen, Chen Zhao, Zhou Yu, Kathleen McKeown, He He*.  [[pdf](https://arxiv.org/abs/2209.07661)], 2022.09, ![](https://img.shields.io/badge/conference-FAEFCA)
    ![](https://img.shields.io/badge/Analysis-EAD8D9)

17. **Can language models learn from explanations in context?**. ![](https://img.shields.io/badge/New-EAD8D9) ![](https://img.shields.io/badge/explanations-DCE7F1)

   *Andrew K. Lampinen, Ishita Dasgupta, Stephanie C. Y. Chan, Kory Matthewson, Michael Henry Tessler, Antonia Creswell, James L. McClelland, Jane X. Wang, Felix Hill*.  [[pdf](https://arxiv.org/pdf/2204.02329.pdf)], 2022.04 ![](https://img.shields.io/badge/ArXiv-FAEFCA)

18. **Prototypical Calibration for Few-shot Learning of Language Models** ![](https://img.shields.io/badge/New-EAD8D9)
    *Zhixiong Han, Yaru Hao, Li Dong, Furu Wei*. [[pdf](https://arxiv.org/abs/2205.10183)], [[project](https://github.com/microsoft/LMOps)], 2022.05.

19. **Cross-Task Generalization via Natural Language Crowdsourcing Instructions**. ![](https://img.shields.io/badge/New-EAD8D9) ![](https://img.shields.io/badge/unseen_task_generalization-DCE7F1)

   *Swaroop Mishra, Daniel Khashabi, Chitta Baral, Hannaneh Hajishirzi*.  [[pdf](https://arxiv.org/abs/2104.08773)], [[project](https://github.com/allenai/natural-instructions)], 2022.03 ![](https://img.shields.io/badge/ACL2022-FAEFCA)
   
 20. **Large Language Models Are Implicitly Topic Models: Explaining and Finding Good Demonstrations for In-Context Learning**. ![](https://img.shields.io/badge/New-EAD8D9)
 
     *Xinyi Wang, Wanrong Zhu, William Yang Wang*.  [[pdf](https://arxiv.org/abs/2301.11916)], [[project](https://github.com/WANGXinyiLinda/concept-based-demonstration-selection)], 2023.01

### Analysis of ICL

This section contains the pilot works that might contributes to the influence factors and working mechanism analysis of ICL.

#### Influence Factors for ICL
We discuss relevant research addressing what influences ICL performance, including factors both in the pretraining stage and in the inference stage.

##### Pre-training stage 

1. **On the Effect of Pretraining Corpora on In-context Learning by a Large-scale Language Model.** ![](https://img.shields.io/badge/corpus-DCE7F1)

   *Seongjin Shin, Sang-Woo Lee, Hwijeen Ahn, Sungdong Kim, HyoungSeok Kim, Boseop Kim, Kyunghyun Cho, Gichang Lee, Woo-Myoung Park, Jung-Woo Ha, Nako Sung*.  [[pdf](https://arxiv.org/pdf/2204.13509)], 2022.08, ![](https://img.shields.io/badge/NAACL2022-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)

2. **Data Distributional Properties Drive Emergent In-Context Learning in Transformers.** ![](https://img.shields.io/badge/corpus-DCE7F1)

   *Stephanie C.Y. Chan, Adam Santoro, Andrew K. Lampinen, Jane X. Wang, Aaditya Singh, Pierre H. Richemond, Jay McClelland, Felix Hill*.  [[pdf](https://arxiv.org/pdf/2205.05055.pdf)], [[project](https://github.com/deepmind/emergent_in_context_learning)], 2022.05, ![](https://img.shields.io/badge/NeurIPS2022-FAEFCA)


3. **The learnability of in-context learning.**
   *Noam Wies, Yoav Levine, Amnon Shashua.* [[pdf](https://arxiv.org/pdf/2303.07895)], 2023.3, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)

4. **Understanding in-context learning via supportive pre-training data.**
   *Xiaochuang Han, Daniel Simig, Todor Mihaylov, Yulia Tsvetkov, Asli Celikyilmaz, Tianlu Wang.* [[pdf](https://arxiv.org/pdf/2306.15091)], 2023.6, ![](https://img.shields.io/badge/ACL2023-FAEFCA)

5. **Pretraining data mixtures enable narrow model selection capabilities in transformer models.**
   *Steve Yadlowsky, Lyric Doshi, Nilesh Tripuraneni.* [[pdf](https://arxiv.org/pdf/2311.00871)], 2023.11, ![](https://img.shields.io/badge/arxiv-FAEFCA)

6. **Pretraining task diversity and the emergence of non-bayesian in-context learning for regression.**
   *Allan Raventós, Mansheej Paul, Feng Chen, Surya Ganguli.* [[pdf](https://arxiv.org/pdf/2306.15063)], [[project](https://github.com/mansheej/icl-task-diversity)], 2023.6, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)


7. **Causallm is not optimal for in-context learning.**
   *Nan Ding, Tomer Levinboim, Jialin Wu, Sebastian Goodman, Radu Soricut.* [[pdf](https://arxiv.org/pdf/2308.06912)], 2023.8, ![](https://img.shields.io/badge/arxiv-FAEFCA)

8. **Emergent Abilities of Large Language Models.** ![](https://img.shields.io/badge/emergent-DCE7F1)

   *Jason Wei, Yi Tay, Rishi Bommasani, Colin Raffel, Barret Zoph, Sebastian Borgeaud, Dani Yogatama, Maarten Bosma, Denny Zhou, Donald Metzler, Ed H. Chi, Tatsunori Hashimoto, Oriol Vinyals, Percy Liang, Jeff Dean, William Fedus*.  [[pdf](https://arxiv.org/pdf/2206.07682)], 2022.07, ![](https://img.shields.io/badge/TMLR2022-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)

9. **Language models are few-shot learners.**
   *Tom B. Brown, Benjamin Mann, Nick Ryder, Melanie Subbiah, Jared Kaplan, Prafulla Dhariwal, Arvind Neelakantan, Pranav Shyam, Girish Sastry, Amanda Askell, Sandhini Agarwal, Ariel Herbert-Voss, Gretchen Krueger, Tom Henighan, Rewon Child, Aditya Ramesh, Daniel M. Ziegler, Jeffrey Wu, Clemens Winter, Christopher Hesse, Mark Chen, Eric Sigler, Mateusz Litwin, Scott Gray, Benjamin Chess, Jack Clark, Christopher Berner, Sam McCandlish, Alec Radford, Ilya Sutskever, Dario Amodei* [[pdf](https://arxiv.org/pdf/2005.14165)], 2020,5, ![](https://img.shields.io/badge/NeurIPS2020-FAEFCA)


##### Inference Stage 

1. **What Makes Good In-Context Examples for GPT-3?** ![img](https://img.shields.io/badge/similarity-DCE7F1)

   *Jiachang Liu, Dinghan Shen, Yizhe Zhang, Bill Dolan, Lawrence Carin, Weizhu Chen*.  [[pdf](https://arxiv.org/pdf/2101.06804)], 2022.08, ![img](https://img.shields.io/badge/DeeLIO@ACL-FAEFCA)
   ![img](https://img.shields.io/badge/Analysis-EAD8D9) ![img](https://img.shields.io/badge/feature-D8D0E1)


2. **Towards Understanding Chain-of-Thought Prompting: An Empirical Study of What Matters.** ![](https://img.shields.io/badge/understanding_cot-DCE7F1)

   *Boshi Wang, Sewon Min, Xiang Deng, Jiaming Shen, You Wu, Luke Zettlemoyer, Huan Sun*.  [[pdf](https://arxiv.org/pdf/2212.10001)], [[project](https://github.com/sunlab-osu/understanding-cot)], 2022.12, ![](https://img.shields.io/badge/ACL2023-FAEFCA)    ![](https://img.shields.io/badge/New-EAD8D9)

3. **Rethinking the Role of Scale for In-Context Learning: An Interpretability-based Case Study at 66 Billion Scale.** ![](https://img.shields.io/badge/rethinking-DCE7F1)

   *Hritik Bansal, Karthik Gopalakrishnan, Saket Dingliwal, Sravan Bodapati, Katrin Kirchhoff, Dan Roth*.  [[pdf](https://arxiv.org/pdf/2212.09095)], [[project](https://github.com/amazon-science/llm-interpret)], 2022.12, ![](https://img.shields.io/badge/ACL2023-FAEFCA)
   ![](https://img.shields.io/badge/New-EAD8D9) ![](https://img.shields.io/badge/rethinking_scale-D8D0E1)

4. **Ground-Truth Labels Matter: A Deeper Look into Input-Label Demonstrations.** ![](https://img.shields.io/badge/ground_truth-DCE7F1), [[project]()], 

   *Junyeob Kim, Hyuhng Joon Kim, Hyunsoo Cho, Hwiyeol Jo, Sang-Woo Lee, Sang-goo Lee, Kang Min Yoo, Taeuk Kim*.  [[pdf](https://arxiv.org/pdf/2205.12685)], 2022.05, ![](https://img.shields.io/badge/EMNLP2022-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)


5. **What in-context learning "learns" in-context: Disentangling task recognition and task learning.**
   *Jane Pan, Tianyu Gao, Howard Chen, Danqi Chen.* [[pdf](https://aclanthology.org/2023.findings-acl.527/)], [[project](https://github.com/princeton-nlp/WhatICLLearns)], 2023.5, ![](https://img.shields.io/badge/ACL2023-FAEFCA)


6. **Large language models can be lazy learners: Analyze shortcuts in in-context learning.**
   *Ruixiang Tang, Dehan Kong, Longtao Huang, Hui Xue* [[pdf](https://aclanthology.org/2023.findings-acl.284.pdf)], 2023.5, ![](https://img.shields.io/badge/ACL2023-FAEFCA)


7. **Larger language models do in-context learning differently.**
   *Jerry W. Wei, Jason Wei, Yi Tay, Dustin Tran, Albert Webson, Yifeng Lu, Xinyun Chen, Hanxiao Liu, Da Huang, Denny Zhou, Tengyu Ma.* [[pdf](https://arxiv.org/pdf/2303.03846)], 2023.3, ![](https://img.shields.io/badge/arxiv-FAEFCA)

8. **Diverse Demonstrations Improve In-context Compositional Generalization** ![](https://img.shields.io/badge/diverse_demonstration-DCE7F1)
   *Itay Levy, Ben Bogin, Jonathan Berant*.  [[pdf](https://arxiv.org/pdf/2212.06800)], [[project](https://github.com/itayle/diverse-demonstrations)], 2022.12, ![](https://img.shields.io/badge/ACL2023-FAEFCA)

9. **Fantastically ordered prompts and where to find them: Overcoming few-shot prompt order sensitivity.**
   *Yao Lu, Max Bartolo, Alastair Moore, Sebastian Riedel, Pontus Stenetorp.* [[pdf](https://aclanthology.org/2022.acl-long.556.pdf)], 2021.4, ![](https://img.shields.io/badge/ACL2022-FAEFCA)


10. **Active example selection for in-context learning.**
   *	Yiming Zhang, Shi Feng, Chenhao Tan.* [[pdf](https://aclanthology.org/2022.emnlp-main.622.pdf)], [[project](https://github.com/ChicagoHAI/active-example-selection)], ![](https://img.shields.io/badge/EMNLP2022-FAEFCA)


11. **Lost in the middle: How language models use long contexts.**
   *Nelson F. Liu, Kevin Lin, John Hewitt, Ashwin Paranjape, Michele Bevilacqua, Fabio Petroni, Percy Liang.* [[pdf](https://doi.org/10.48550/arXiv.2307.03172)], [[project](https://github.com/nelson-liu/lost-in-the-middle)], 2023.7, ![](https://img.shields.io/badge/ACL2024-FAEFCA)

12.  **Measuring inductive biases of in-context learning with underspecified demonstrations.**
   *Chenglei Si, Dan Friedman, Nitish Joshi, Shi Feng, Danqi Chen, He He.* [[pdf](https://doi.org/10.18653/v1/2023.acl-long.632)], [[project](https://github.com/NoviScl/AmbigPrompt)], 2023.5, ![](https://img.shields.io/badge/ACL2023-FAEFCA)


13. **In-context learning in large language models learns label relationships but is not conventional learning.**
   *Jannik Kossen, Tom Rainforth, Yarin Gal* [[pdf](https://doi.org/10.48550/arXiv.2307.12375)], 2023.7, ![](https://img.shields.io/badge/arxiv-FAEFCA)

14. **How Does In-Context Learning Help Prompt Tuning?**

      *Simeng Sun, Yang Liu, Dan Iter, Chenguang Zhu, Mohit Iyyer*.  [[pdf](https://arxiv.org/pdf/2302.11521)], 2023.02, ![](https://img.shields.io/badge/EACL2024-FAEFCA)


#### Working Mechanism of ICL
1. **In-context Learning and Induction Heads.** ![](https://img.shields.io/badge/induction_head-DCE7F1)

   *Catherine Olsson, Nelson Elhage, Neel Nanda, Nicholas Joseph, Nova DasSarma, Tom Henighan, Ben Mann, Amanda Askell, Yuntao Bai, Anna Chen, Tom Conerly, Dawn Drain, Deep Ganguli, Zac Hatfield-Dodds, Danny Hernandez, Scott Johnston, Andy Jones, Jackson Kernion, Liane Lovitt, Kamal Ndousse, Dario Amodei, Tom Brown, Jack Clark, Jared Kaplan, Sam McCandlish, Chris Olah*.  [[pdf](https://arxiv.org/pdf/2209.11895)], 2022.10, ![](https://img.shields.io/badge/arXiv-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)

2. **Birth of a transformer: A memory viewpoint.**
   *Alberto Bietti, Vivien Cabannes, Diane Bouchacourt, Hervé Jégou, Léon Bottou.* [[pdf](http://papers.nips.cc/paper_files/paper/2023/hash/0561738a239a995c8cd2ef0e50cfa4fd-Abstract-Conference.html)], 2023.6, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)


3. **Why Can GPT Learn In-Context? Language Models Secretly Perform Gradient Descent as Meta-Optimizers.** ![](https://img.shields.io/badge/meta_optimizer-DCE7F1)

   *Damai Dai, Yutao Sun, Li Dong, Yaru Hao, Zhifang Sui, Furu Wei*.  [[pdf](https://arxiv.org/pdf/2212.10559)], [[project](https://github.com/microsoft/LMOps)], 2022.12 ![](https://img.shields.io/badge/ACL2023-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)

4. **The dual form of neural networks revisited: Connecting test time predictions to training patterns via spotlights of attention.**
   *Kazuki Irie, Róbert Csordás, Jürgen Schmidhuber.* [[pdf](https://proceedings.mlr.press/v162/irie22a.html)], [[project](https://instructions.apps.allenai.org/)], 2022.2, ![](https://img.shields.io/badge/ICML2022-FAEFCA)

5. **The closeness of in-context learning and weight shifting for softmax regression.**
   *Shuai Li, Zhao Song, Yu Xia, Tong Yu, Tianyi Zhou.* [[pdf](https://doi.org/10.48550/arXiv.2304.13276)], 2023.4, ![](https://img.shields.io/badge/arxiv-FAEFCA)

6. **In context learning for attention scheme: from single softmax regression to multiple softmax regression via a tensor trick.**
   *Yeqi Gao, Zhao Song, Shenghao Xie.* [[pdf](https://doi.org/10.48550/arXiv.2307.02419)], 2023.7, ![](https://img.shields.io/badge/arxiv-FAEFCA)


7. **What and how does in-context learning learn? bayesian model averaging,parameterization, and generalization.**
   *Yufeng Zhang, Fengzhuo Zhang, Zhuoran Yang, Zhaoran Wang.* [[pdf](https://doi.org/10.48550/arXiv.2305.19420)], 2023.5, ![](https://img.shields.io/badge/arxiv-FAEFCA)

8. **An information flow perspective for understanding in-context learning.**
   *Lean Wang, Lei Li, Damai Dai, Deli Chen, Hao Zhou, Fandong Meng, Jie Zhou, Xu Sun.* [[pdf](https://doi.org/10.18653/v1/2023.emnlp-main.609)], [[project](https://github.com/lancopku/label-words-are-anchors)], 2023.5, ![](https://img.shields.io/badge/EMNLP2023-FAEFCA)


 9. **An Explanation of In-context Learning as Implicit Bayesian Inference.** ![](https://img.shields.io/badge/bayesian-DCE7F1)

   *Sang Michael Xie, Aditi Raghunathan, Percy Liang, Tengyu Ma*.  [[pdf](https://arxiv.org/pdf/2111.02080)], [[project](https://github.com/p-lambda/incontext-learning)], 2022.08, ![](https://img.shields.io/badge/ICLR2022-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)


10. **Data Distributional Properties Drive Emergent In-Context Learning in Transformers.** ![](https://img.shields.io/badge/data_distributional-DCE7F1)

   *Stephanie C. Y. Chan, Adam Santoro, Andrew K. Lampinen, Jane X. Wang, Aaditya Singh, Pierre H. Richemond, Jay McClelland, Felix Hill*.  [[pdf](https://arxiv.org/pdf/2205.05055)], [[project](https://github.com/deepmind/emergent_in_context_learning)], 2022.05, ![](https://img.shields.io/badge/NeurIPS2022-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)


11. **Transformers learn to implement preconditioned gradient descent for in-context learning.**
   *Kwangjun Ahn, Xiang Cheng, Hadi Daneshmand, Suvrit Sra.* [[pdf](https://papers.nips.cc/paper_files/paper/2023/file/8ed3d610ea4b68e7afb30ea7d01422c6-Paper-Conference.pdf)], 2023.6, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)


12.  **In-context learning through the bayesian prism.**
   *Kabir Ahuja, Madhur Panwar, Navin Goyal.* [[pdf](https://doi.org/10.48550/arXiv.2306.04891)], 2023.6, ![](https://img.shields.io/badge/arxiv-FAEFCA)

13.  **What learning algorithm is in-context learning? Investigations with linear models.** ![](https://img.shields.io/badge/learning_algorithm-DCE7F1)
    *Ekin Akyürek, Dale Schuurmans, Jacob Andreas, Tengyu Ma, Denny Zhou*.  [[pdf](https://arxiv.org/pdf/2211.15661)], 2022.11, ![](https://img.shields.io/badge/ICLR2023-FAEFCA) ![](https://img.shields.io/badge/Analysis-EAD8D9)


14. **Transformers as statisticians: Provable in-context learning with in-context algorithm selection.**
   *Yu Bai, Fan Chen, Huan Wang, Caiming Xiong, Song Mei.* [[pdf](http://papers.nips.cc/paper_files/paper/2023/hash/b2e63e36c57e153b9015fece2352a9f9-Abstract-Conference.html)], [[project](https://github.com/allenbai01/transformers-as-statisticians)], 2023.6, ![](https://img.shields.io/badge/NeurIPS2023-FAEFCA)


15. **Transformers learn higher-order optimization methods for in-context learning: A study with linear models.**
   *Deqing Fu, Tian-Qi Chen, Robin Jia, Vatsal Sharan.* [[pdf](https://doi.org/10.48550/arXiv.2310.17086)], [[project](https://github.com/DeqingFu/transformers-icl-higher-order)], 2023.10, ![](https://img.shields.io/badge/arxiv-FAEFCA)


16. **What Can Transformers Learn In-Context? A Case Study of Simple Function Classes.** ![](https://img.shields.io/badge/case_study-DCE7F1)
   *Shivam Garg, Dimitris Tsipras, Percy Liang, Gregory Valiant*.  [[pdf](https://openreview.net/pdf?id=flNZJ2eOet)], 2022.08, ![](https://img.shields.io/badge/NeurIPS2022-FAEFCA) ![](https://img.shields.io/badge/Analysis-EAD8D9)


17. **A theory of emergent in-context learning as implicit structure induction.**
   *Michael Hahn, Navin Goyal.* [[pdf](https://doi.org/10.48550/arXiv.2303.07971)], 2023.3, ![](https://img.shields.io/badge/arxiv-FAEFCA)

18. **Explaining emergent in-context learning as kernel regression.**
   *Chi Han, Ziqi Wang, Han Zhao, Heng Ji.* [[pdf](https://arxiv.org/pdf/2305.12766)], 2023.5, ![](https://img.shields.io/badge/arxiv-FAEFCA)

19. **A latent space theory for emergent abilities in large language models.**
   *Hui Jiang.* [[pdf](https://doi.org/10.48550/arXiv.2304.09960)], 2023.4, ![](https://img.shields.io/badge/arxiv-FAEFCA)

20. **Transformers as Algorithms: Generalization and Implicit Model Selection in In-context Learning.** ![](https://img.shields.io/badge/algorithm-DCE7F1)
    *Yingcong Li, M. Emrullah Ildiz, Dimitris S. Papailiopoulos, Samet Oymak*.  [[pdf](https://arxiv.org/pdf/2301.07067)], 2023.1 ![](https://img.shields.io/badge/ArXiv-FAEFCA) ![](https://img.shields.io/badge/Analysis-EAD8D9)


21. **One step of gradient descent is provably the optimal in-context learner with one layer of linear self-attention.**
   *Arvind Mahankali, Tatsunori B. Hashimoto, Tengyu Ma.* [[pdf](https://doi.org/10.48550/arXiv.2307.03576)], 2023.7, ![](https://img.shields.io/badge/arxiv-FAEFCA)

22. **What in-context learning "learns" in-context: Disentangling task recognition and task learning.**
   *Jane Pan, Tianyu Gao, Howard Chen, Danqi Chen.* [[pdf](https://doi.org/10.18653/v1/2023.findings-acl.527)], [[project](https://github.com/princeton-nlp/WhatICLLearns)], 2023.5, ![](https://img.shields.io/badge/ACL2023-FAEFCA)


23. **Transformers learn in-context by gradient descent.** ![](https://img.shields.io/badge/gd-DCE7F1)
    *von Oswald, Johannes, Eyvind Niklasson, Ettore Randazzo, João Sacramento, Alexander Mordvintsev, Andrey Zhmoginov, Max Vladymyrov*.  [[pdf](https://arxiv.org/pdf/2212.07677)], 2022.12, ![](https://img.shields.io/badge/ICML2023-FAEFCA)
   ![](https://img.shields.io/badge/Analysis-EAD8D9)

24. **Do pretrained transformers learn in-context by gradient descent?**
   *Lingfeng Shen, Aayush Mishra, Daniel Khashabi.* [[pdf](https://doi.org/10.48550/arXiv.2310.08540)], 2023.10, ![](https://img.shields.io/badge/arxiv-FAEFCA)


25. **Large language models are implicitly topic models: Explaining and finding good demonstrations for in-context learning.**
   *Xinyi Wang, Wanrong Zhu, William Yang Wang.* [[pdf](https://arxiv.org/pdf/2301.11916)], [[project](https://github.com/WANGXinyiLinda/concept-based-demonstration-selection)], 2023.1, ![](https://img.shields.io/badge/arxiv-FAEFCA)



26. **Iterative Forward Tuning Boosts In-context Learning in Language Models.** ![](https://img.shields.io/badge/DeepThinking-DCE7F1) 
   *Jiaxi Yang, Binyuan Hui, Min Yang, Binhua Li, Fei Huang, Yongbin Li*.  [[pdf](https://arxiv.org/pdf/2305.13016)], [[project](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/deep-thinking)], [[demo](https://huggingface.co/spaces/huybery/deep-thinking)], 2023.05 ![](https://img.shields.io/badge/arXiv-FAEFCA) ![](https://img.shields.io/badge/New-EAD8D9)

27. **Unveiling Induction Heads: Provable Training Dynamics and Feature Learning in Transformers**
    Siyu Chen, Heejune Sheen, Tianhao Wang, Zhuoran Yang. [[pdf](https://arxiv.org/pdf/2409.10559)], 2024.09 ![](https://img.shields.io/badge/NeurIPS2024-FAEFCA) ![](https://img.shields.io/badge/New-EAD8D9)

### Evaluation and Resources

This section contains the pilot works that might contributes to the evaluation or resources of ICL.

1. **Beyond the Imitation Game: Quantifying and extrapolating the capabilities of language models**. ![](https://img.shields.io/badge/BigBench-DCE7F1)

   *Aarohi Srivastava, Abhinav Rastogi, Abhishek Rao, Abu Awal Md Shoeb, Abubakar Abid, Adam Fisch, Adam R. Brown, Adam Santoro, Aditya Gupta, Adrià Garriga-Alonso, Agnieszka Kluska, Aitor Lewkowycz, Akshat Agarwal, Alethea Power, Alex Ray, Alex Warstadt et. al.*.  [[pdf](https://arxiv.org/abs/2206.04615)], [[project](https://github.com/google/BIG-bench)], 2022.06, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/evaluation-EAD8D9) ![](https://img.shields.io/badge/large_scale-D8D0E1)
2. **SUPER-NATURALINSTRUCTIONS: Generalization via Declarative Instructions on 1600+ NLP Task**. ![](https://img.shields.io/badge/natural_instructions-DCE7F1)

   *Yizhong Wang, Swaroop Mishra, Pegah Alipoormolabashi, Yeganeh Kordi, Amirreza Mirzaei, Anjana Arunkumar, Arjun Ashok, Arut Selvan Dhanasekaran, Atharva Naik, David Stap, Eshaan Pathak, Giannis Karamanolakis, Haizhi Gary Lai, Ishan Purohit et. al.*.  [[pdf](https://arxiv.org/abs/2204.07705)], [[project](https://github.com/allenai/natural-instructions)], 2022.04, ![](https://img.shields.io/badge/EMNLP2022-FAEFCA)
    ![](https://img.shields.io/badge/instruction_tuning-D8D0E1)
3. **Language Models are Multilingual Chain-of-Thought Reasoners**.

   *Freda Shi, Mirac Suzgun, Markus Freitag, Xuezhi Wang, Suraj Srivats, Soroush Vosoughi, Hyung Won Chung, Yi Tay, Sebastian Ruder, Denny Zhou, Dipanjan Das, Jason Wei*.  [[pdf](https://arxiv.org/abs/2210.03057)], 2022.10, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/evaluation-EAD8D9) ![](https://img.shields.io/badge/multilingual-D8D0E1)

   - evaluate the reasoning abilities of large language models in multilingual settings, introduce the Multilingual Grade School Math (MGSM) benchmark, by manually translating 250 grade-school math problems from the GSM8K dataset into ten typologically diverse languages.
4. **Instruction Induction: From Few Examples to Natural Language Task Descriptions**. ![](https://img.shields.io/badge/Instruction_Induction-DCE7F1)

   *Or Honovich, Uri Shaham, Samuel R. Bowman, Omer Levy*.  [[pdf](https://arxiv.org/abs/2205.10782)], [[project](https://github.com/orhonovich/instruction-induction)], 2022.05, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/evaluation-EAD8D9) ![](https://img.shields.io/badge/learn_task_instructions-D8D0E1)

   - how to learn task instructions from input output demonstrations
5. **Language Models Are Greedy Reasoners: A Systematic Formal Analysis of Chain-of-Thought**2022.10.3  ![](https://img.shields.io/badge/New-EAD8D9)
6. **What is Not in the Context? Evaluation of Few-shot Learners with Informative Demonstrations** 2212.01692.pdf (arxiv.org)  ![](https://img.shields.io/badge/New-EAD8D9)
7. **Unnatural Instructions: Tuning Language Models with (Almost) No Human Labor**.

   *Or Honovich, Thomas Scialom, Omer Levy, Timo Schick*. [[pdf](https://arxiv.org/pdf/2212.09689.pdf)], [[project](https://github.com/orhonovich/unnatural-instructions)], 2022.12, ![](https://img.shields.io/badge/arxiv-FAEFCA)    ![](https://img.shields.io/badge/New-EAD8D9)
8. **Self-Instruct: Aligning Language Model with Self Generated Instructions**.

   *Yizhong Wang, Yeganeh Kordi, Swaroop Mishra, Alisa Liu, Noah A. Smith, Daniel Khashabi, Hannaneh Hajishirzi*. [[pdf](https://arxiv.org/pdf/2212.10560.pdf)], [[project](https://github.com/yizhongw/self-instruct)], 2022.12, ![](https://img.shields.io/badge/arxiv-FAEFCA)    ![](https://img.shields.io/badge/New-EAD8D9)
9. **The Flan Collection: Designing Data and Methods for Effective**.

   *Shayne Longpre, Le Hou, Tu Vu, Albert Webson, Hyung Won Chung, Yi Tay, Denny Zhou, Quoc V. Le, Barret Zoph, Jason Wei, Adam Roberts*. [[pdf](https://arxiv.org/pdf/2301.13688.pdf)], [[project](https://github.com/google-research/FLAN/tree/main/flan/v2)], 2023.1, ![](https://img.shields.io/badge/arxiv-FAEFCA)    ![](https://img.shields.io/badge/New-EAD8D9)

### Application

This section contains the pilot works that expands the application of ICL.

1. **Meta-learning via Language Model In-context Tuning**.

   *Yanda Chen, Ruiqi Zhong, Sheng Zha, George Karypis, He He*.  [[pdf](https://arxiv.org/abs/2110.07814)], [[project](https://github.com/yandachen/in-context-tuning)], 2021.10, ![](https://img.shields.io/badge/ACL2022-FAEFCA)
   ![](https://img.shields.io/badge/application-EAD8D9) ![](https://img.shields.io/badge/Meta-learning-D8D0E1)

2. **Does GPT-3 Generate Empathetic Dialogues? A Novel In-Context Example Selection Method and Automatic Evaluation Metric for Empathetic Dialogue Generation**.

   *Young-Jun Lee, Chae-Gyun Lim, Ho-Jin Choi*.  [[pdf](https://aclanthology.org/2022.coling-1.56/)], 2022.10, ![](https://img.shields.io/badge/COLING2022-FAEFCA)
   ![](https://img.shields.io/badge/application-EAD8D9) ![](https://img.shields.io/badge/dialogue_generation-D8D0E1)

3. **In-context Learning Distillation: Transferring Few-shot Learning Ability of Pre-trained Language Models**. ![](https://img.shields.io/badge/ICL_Distillation-DCE7F1)

   *Yukun Huang, Yanda Chen, Zhou Yu, Kathleen McKeown*.  [[pdf](https://arxiv.org/abs/2212.10670)], 2022.12, ![](https://img.shields.io/badge/conference-FAEFCA)
   ![](https://img.shields.io/badge/challenge-EAD8D9) ![](https://img.shields.io/badge/distillation-D8D0E1)

4. **Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions**![](https://img.shields.io/badge/New-EAD8D9)

5. **Prompt-Augmented Linear Probing: Scaling Beyond the Limit of Few-shot In-Context Learner**.

   *Hyunsoo Cho, Hyuhng Joon Kim, Junyeob Kim, Sang-Woo Lee, Sang-goo Lee, Kang Min Yoo, Taeuk Kim*. [[pdf](https://arxiv.org/abs/2212.10873)], 2022.12, ![](https://img.shields.io/badge/AAAI2023-FAEFCA)
   ![](https://img.shields.io/badge/application-EAD8D9) ![](https://img.shields.io/badge/linear_probing-D8D0E1)

6. **In-Context Learning Unlocked for Diffusion Models**
   *Zhendong Wang, Yifan Jiang, Yadong Lu, Yelong Shen, Pengcheng He, Weizhu Chen, Zhangyang Wang, Mingyuan Zhou*. [[pdf]](https://arxiv.org/abs/2305.01115), [[project]](https://github.com/Zhendong-Wang/Prompt-Diffusion), 2023.5, ![](https://img.shields.io/badge/arxiv-FAEFCA)
   
7. **Molecule Representation Fusion via In-Context Learning for Retrosynthetic Plannings**
   *Songtao Liu, Zhengkai Tu, Minkai Xu, Zuobai Zhang, Lu Lin, Rex Ying, Jian Tang, Peilin Zhao, Dinghao Wu*. [[pdf]](https://arxiv.org/pdf/2209.15315.pdf), [[project]](https://github.com/SongtaoLiu0823/FusionRetro), 2023.5, ![](https://img.shields.io/badge/arxiv-FusionRetro)

This section contains the pilot works that points out the problems of ICL.

1. **The Inductive Bias of In-Context Learning: Rethinking Pretraining Example Design** ![](https://img.shields.io/badge/New-EAD8D9). ![](https://img.shields.io/badge/knn_Pretraining-DCE7F1)

   *Yoav Levine, Noam Wies, Daniel Jannai, Dan Navon, Yedid Hoshen, Amnon Shashua*.  [[pdf](https://arxiv.org/abs/2110.04541)], 2021.10, ![](https://img.shields.io/badge/ICLR2022-FAEFCA)
   ![](https://img.shields.io/badge/problem-EAD8D9) ![](https://img.shields.io/badge/knn_Pretraining-D8D0E1)

### Challenges and Future Directions

This section contains the pilot works that might contributes to the challenges and future directions of ICL.

## Blogs

[SEO is Dead, Long Live LLMO](https://jina.ai/news/seo-is-dead-long-live-llmo/)

[How does in-context learning work? A framework for understanding the differences from traditional supervised learning](http://ai.stanford.edu/blog/understanding-incontext/)

[Extrapolating to Unnatural Language Processing with GPT-3's In-context Learning: The Good, the Bad, and the Mysterious](http://ai.stanford.edu/blog/in-context-learning/)

[More Efficient In-Context Learning with GLaM](https://ai.googleblog.com/2021/12/more-efficient-in-context-learning-with.html)

## Open-source Toolkits
**OpenICL**
[[pdf](https://arxiv.org/abs/2303.02913)], [[project](https://github.com/Shark-NLP/OpenICL)], 2022.03

OpenICL provides an easy interface for in-context learning, with many state-of-the-art retrieval and inference methods built in to facilitate systematic comparison of LMs and fast research prototyping. Users can easily incorporate different retrieval and inference methods, as well as different prompt instructions into their workflow.

## Contribution

Please feel free to contribute and promote your awesome work or other related works here! 
If you recommend related works on ICL or make contributions on this repo, please provide your information (name, homepage) and we will add you to the contributor list😊.

### Contributor list 
We thank [Damai Dai](https://scholar.google.com/citations?user=8b-ysf0NWVoC&hl=zh-CN&oi=ao), [Qingxiu Dong](https://dqxiu.github.io/), [Lei Li](https://leili.site/), [Ce Zheng](https://scholar.google.com/citations?user=r7qFs7UAAAAJ&hl=zh-CN&oi=ao), [Shihao Liang](https://pooruss.github.io/-lshwebsite/), [Li Dong](http://dong.li/), [Siyin Wang](https://sinwang20.github.io/), [Po-Chuan Chen](https://jacksonchen1998.github.io/) for their repo contribution and paper recommendation.


<!-- ## Citations -->
## Reference

<!-- Please consider citing our papers in your publications if the project helps your research. BibTeX reference is as follows. -->
Some papers are discussed in the following paper:

```
@misc{dong2022survey,
      title={A Survey for In-context Learning}, 
      author={Qingxiu Dong and Lei Li and Damai Dai and Ce Zheng and Zhiyong Wu and Baobao Chang and Xu Sun and Jingjing Xu and Lei Li and Zhifang Sui},
      year={2022},
      eprint={2301.00234},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
