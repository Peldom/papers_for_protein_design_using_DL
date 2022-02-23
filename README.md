# List of papers about Proteins Design using Deep Learning

## About this repository

Inspired by Kevin Kaichuang Yang's [Machine-learning-for-proteins](https://github.com/yangkky/Machine-learning-for-proteins). In terms of the fast changing of **protein design in DL**, I started making this dynamic repository as a record of papers in this field for newcomers like me.
My notes of these papers are shared in a **[Zhihu Column](https://www.zhihu.com/column/c_1475864742820929537)**(simplified Chinese).  

## Menu

- [List of papers about Proteins Design using Deep Learning](#list-of-papers-about-proteins-design-using-deep-learning)
  - [About this repository](#about-this-repository)
  - [Menu](#menu)
  - [1. Reviews](#1-reviews)
  - [2. Hallucination](#2-hallucination)
    - [2.1 trRosetta-based](#21-trrosetta-based)
    - [2.2 AlphaFold2-based](#22-alphafold2-based)
  - [3. Function to Scaffold](#3-function-to-scaffold)
    - [3.1 GAN-based](#31-gan-based)
    - [3.2 VAE-based](#32-vae-based)
    - [3.3 DAE-based](#33-dae-based)
    - [3.4 MLP-based](#34-mlp-based)
  - [4.Scaffold to Sequence](#4scaffold-to-sequence)
    - [4.1 MLP-based](#41-mlp-based)
    - [4.2 VAE-based](#42-vae-based)
    - [4.3 Bi-LSTM+2D-ResNet](#43-bi-lstm2d-resnet)
    - [4.4 CNN-based](#44-cnn-based)
    - [4.5 GNN-based](#45-gnn-based)
    - [4.6 GAN-based](#46-gan-based)
    - [4.7 Transformer-based](#47-transformer-based)
    - [4.8 ResNet-based](#48-resnet-based)
  - [5.Function to Sequence](#5function-to-sequence)
    - [5.1 CM-Align](#51-cm-align)
    - [5.2 VAE-based](#52-vae-based)
    - [5.3 GAN-based](#53-gan-based)
    - [5.4 NLP-based](#54-nlp-based)
    - [5.5 ResNet-based](#55-resnet-based)
    - [5.6 Bayesian-based](#56-bayesian-based)
    - [5.7 Pretrained-based](#57-pretrained-based)
    - [5.8 RL-based](#58-rl-based)
  - [6.Molecular Design Models](#6molecular-design-models)
    - [6.1 Gradient optimization](#61-gradient-optimization)
    - [6.2 Combinatorial optimized sampling](#62-combinatorial-optimized-sampling)
  - [7. Other tasks](#7-other-tasks)
    - [7.1 Fitness functions / Landscape exploring using latent space](#71-fitness-functions--landscape-exploring-using-latent-space)

## 1. Reviews

**Deep learning in protein structural modeling and design**  
Wenhao Gao, Sai Pooja Mahajan, Jeremias Sulam, and Jeffrey J. Gray  
[Patterns 1.9](https://www.sciencedirect.com/science/article/pii/S2666389920301902)  || 2020

**Deep generative modeling for protein design**  
Strokach, Alexey, and Philip M. Kim.  
[Current Opinion in Structural Biology](https://www.sciencedirect.com/science/article/pii/S0959440X21001573) || 2022  

**Protein sequence design with deep generative models**  
Zachary Wu, Kadina E. Johnston, Frances H. Arnold, Kevin K. Yang  
[Current Opinion in Chemical Biology](https://www.sciencedirect.com/science/article/pii/S136759312100051X) || [note](https://zhuanlan.zhihu.com/p/466616309) || 2021  

**Structure-based protein design with deep learning**  
Ovchinnikov, Sergey, and Po-Ssu Huang.  
[Current opinion in chemical biology](https://www.sciencedirect.com/science/article/pii/S1367593121001125) || [note](https://zhuanlan.zhihu.com/p/467001175) || 2021  

## 2. Hallucination

> Hallucination is inverting prediction model for design.

### 2.1 trRosetta-based

 **Design of proteins presenting discontinuous functional sites using deep learning**  
Doug Tischer, Sidney Lisanza, Jue Wang, Runze Dong,  View ORCID ProfileIvan Anishchenko, Lukas F. Milles, Sergey Ovchinnikov, David Baker  
[bioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.11.29.402743v1.abstract)  

**De novo protein design by deep network hallucination**  
Ivan Anishchenko, Samuel J. Pellock, Tamuka M. Chidyausiku, Theresa A. Ramelot, Sergey Ovchinnikov, Jingzhou Hao, Khushboo Bafna, Christoffer Norn, Alex Kang, Asim K. Bera, Frank DiMaio, Lauren Carter, Cameron M. Chow, Gaetano T. Montelione & David Baker  
[Nature (2021)](https://doi.org/10.1038/s41586-021-04184-w)  || [code](https://github.com/gjoni/trDesign) || [trRosetta](https://yanglab.nankai.edu.cn/trRosetta/download/) || 

**Protein sequence design by conformational landscape optimization**  
Norn, Christoffer, et al.  
[Proceedings of the National Academy of Sciences 118.11 (2021)](https://www.pnas.org/content/118/11/e2017228118) || [code](https://github.com/gjoni/trDesign)   

**Fast differentiable DNA and protein sequence optimization for molecular design**  
Linder, Johannes, and Georg Seelig.  
[arXiv preprint arXiv:2005.11275 (2020)](https://arxiv.org/abs/2005.11275)

### 2.2 AlphaFold2-based

**End-to-end learning of multiple sequence alignments with differentiable Smith-Waterman**  
Petti, Samantha, Bhattacharya, Nicholas, Rao, Roshan, Dauparas, Justas, Thomas, Neil, Zhou, Juannan, Rush, Alexander M, Koo, Peter K, Ovchinnikov, Sergey  
[bioRxiv (2021)](http://repository.cshl.edu/id/eprint/40409/) || [Notes of mine](https://zhuanlan.zhihu.com/p/468219547)  

**Deep learning methods for designing proteins scaffolding functional sites**  
Wang J, Lisanza S, Juergens D, Tischer D, Anishchenko I, Baek M, Watson JL, Chun JH, Milles LF, Dauparas J, Expòsit M, Yang W, Saragovi A, Ovchinnikov S, Baker D  
[bioRxiv(2021)](https://europepmc.org/article/ppr/ppr419387)  

**AlphaDesign: A de novo protein design framework based on AlphaFold**  
Jendrusch, Michael, Jan O. Korbel, and S. Kashif Sadiq.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.10.11.463937.abstract) ||  

**Using AlphaFold for Rapid and Accurate Fixed Backbone Protein Design**  
Moffat, Lewis, Joe G. Greener, and David T. Jones.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.08.24.457549v1)  

## 3. Function to Scaffold

> These models design backbone/scaffold/template.

### 3.1 GAN-based

**Conditioning by adaptive sampling for robust design**  
Brookes, David, Hahnbeom Park, and Jennifer Listgarten.  
[International conference on machine learning. PMLR, 2019](http://proceedings.mlr.press/v97/brookes19a/brookes19a.pdf)  || without code  

**RamaNet: Computational de novo helical protein backbone design using a long short-term memory generative neural network**  
Sabban, Sari, and Mikhail Markovsky.  
[F1000Research 9 (2020)](http://f1000researchdata.s3.amazonaws.com/manuscripts/29106/f45e92eb-5d68-4da0-b918-91ded85d2e7d_22907_-_sari_sabban_v2.pdf) || [code](https://sarisabban.github.io/RamaNet/) || pyRosetta || tensorflow || maximizaing the fluorescence of a protein  

**Fully differentiable full-atom protein backbone generation**  
Anand Namrata, Raphael Eguchi, and Po-Ssu Huang.  
[OpenReview ICLR 2019 workshop DeepGenStruct](https://openreview.net/forum?id=SJxnVL8YOV) || without code  

### 3.2 VAE-based

**IG-VAE: generative modeling of immunoglobulin proteins by direct 3D coordinate generation**  
Raphael R. Eguchi, Christian A. Choe, Po-Ssu Huang  
[Biorxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.08.07.242347v2) || without code ||  

### 3.3 DAE-based

**Function-guided protein design by deep manifold sampling**  
Vladimir Gligorijevic, Stephen Ra, Daniel Berenberg, Richard Bonneau, Kyunghyun Cho  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Function-guided_protein_design_by.pdf) || without code

### 3.4 MLP-based

**A backbone-centred energy function of neural networks for protein design**  
Huang, B., Xu, Y., Hu, X. et al  
[Nature (2022)](https://doi.org/10.1038/s41586-021-04383-5)

## 4.Scaffold to Sequence

> Identify amino sequence from given backbone/scaffold/template.

### 4.1 MLP-based

**3D representations of amino acids—applications to protein sequence comparison and classification**  
Li, Jie, and Patrice Koehl.  
[Computational and structural biotechnology journal 11.18 (2014)](https://www.sciencedirect.com/science/article/pii/S2001037014000270) || 2014  

**SPIN2: Predicting sequence profiles from protein structures using deep neural networks**  
O'Connell, James, et al.  
[Proteins: Structure, Function, and Bioinformatics 86.6 (2018)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25489)

**Computational protein design with deep learning neural networks**  
Wang, Jingxue, et al.  
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-24760-x.pdf)  

### 4.2 VAE-based

**Design of metalloproteins and novel protein folds using variational autoencoders**  
Greener, Joe G., Lewis Moffat, and David T. Jones.  
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-34533-1)

### 4.3 Bi-LSTM+2D-ResNet

**To improve protein sequence profile prediction through image captioning on pairwise residue distance map**  
Chen, Sheng, et al.  
[Journal of chemical information and modeling 60.1 (2019)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00438)

### 4.4 CNN-based

**ProDCoNN: Protein design using a convolutional neural network**  
Zhang, Yuan, et al.  
[Proteins: Structure, Function, and Bioinformatics 88.7 (2020)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25868)

**A structure-based deep learning framework for protein engineering**  
Shroff, Raghav, et al.  
[bioRxiv (2019)](https://www.biorxiv.org/content/10.1101/833905v1.abstract)

**Protein sequence design with a learned potential**  
Anand-Achim, Namrata, et al.  
[Biorxiv (2021)](https://www.biorxiv.org/content/10.1101/2020.01.06.895466v3.full.pdf)

### 4.5 GNN-based

**Fast and flexible protein design using deep graph neural networks.**  
Strokach, Alexey, et al.  
[Cell Systems 11.4 (2020)](https://www.sciencedirect.com/science/article/pii/S2405471220303276)  

**TERMinator: A Neural Framework for Structure-Based Protein Design using Tertiary Repeating Motifs**  
Li, Alex J., et al.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_TERMinator:_A_Neural_Framework.pdf)  

### 4.6 GAN-based

**De novo protein design for novel folds using guided conditional Wasserstein generative adversarial networks**  
Mostafa Karimi, Shaowen Zhu, Yue Cao, Yang Shen  
[Journal of chemical information and modeling 60.12 (2020)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.0c00593) || [code](https://github.com/Shen-Lab/gcWGAN) || gcWGAN

### 4.7 Transformer-based

**Generative models for graph-based protein design**  
[John Ingraham](https://openreview.net/profile?email=ingraham%40csail.mit.edu), Vikas K Garg, Dr.Regina Barzilay, Tommi Jaakkola  
[NeurIPS 2019](https://openreview.net/forum?id=ByMEAHrgLB) || [code](https://github.com/jingraham/neurips19-graph-protein-design)  

**Rotamer-Free Protein Sequence Design Based on Deep Learning and Self-Consistency**  
Liu, Yufeng, et al.  
[Nature portfolio (2022)](https://www.researchsquare.com/article/rs-1209166/v1)

### 4.8 ResNet-based

**DenseCPD: improving the accuracy of neural-network-based computational protein sequence design with DenseNet**  
Qi, Yifei, and John ZH Zhang.  
[Journal of chemical information and modeling 60.3 (2020)](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.0c00043)  

## 5.Function to Sequence

> These models generate sequences from expected function.

### 5.1 CM-Align

**AutoFoldFinder: An Automated Adaptive Optimization Toolkit for De Novo Protein Fold Design**  
Shuhao Zhang, Youjun Xu, Jianfeng Pei, Luhua Lai  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_AutoFoldFinder.pdf)  

### 5.2 VAE-based

**Variational auto-encoding of protein sequences**  
Sinai, Sam, et al.  
[arXiv preprint arXiv:1712.03346 (2017)](https://arxiv.org/abs/1712.03346)

**Deep generative models for T cell receptor protein sequences**  
Davidsen, Kristian, et al.  
[Elife 8 (2019)](https://elifesciences.org/articles/46935)

**How to hallucinate functional proteins**  
Costello, Zak, and Hector Garcia Martin.  
[arXiv preprint arXiv:1903.00458 (2019)](https://arxiv.org/abs/1903.00458)

**Conditioning by adaptive sampling for robust design**  
Brookes, David, Hahnbeom Park, and Jennifer Listgarten.  
[International conference on machine learning. PMLR, 2019](http://proceedings.mlr.press/v97/brookes19a.html)

**Generating functional protein variants with variational autoencoders**  
Hawkins-Hooker, Alex, et al.  
[PLoS computational biology 17.2 (2021)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008736)

**Therapeutic enzyme engineering using a generative neural network**  
Giessel, Andrew, et al.  
[Scientific Reports 12.1 (2022)](https://www.nature.com/articles/s41598-022-05195-x)

**Function-guided protein design by deep manifold sampling**  
Gligorijevic, Vladimir, et al.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.12.22.473759v1)

**Deep generative models create new and diverse protein structures**  
Zeming, Tom, Yann and Alexander.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Deep_generative_models_create.pdf)

### 5.3 GAN-based

**Generative modeling for protein structures**  
Anand, Namrata, and Possu Huang.  
[NeurIPS 2018](https://proceedings.neurips.cc/paper/2018/file/afa299a4d1d8c52e75dd8a24c3ce534f-Paper.pdf)

**Generating protein sequences from antibiotic resistance genes data using Generative Adversarial Networks**  
Chhibbar, Prabal, and Arpit Joshi.  
[arXiv preprint arXiv:1904.13240 (2019)](https://arxiv.org/abs/1904.13240)

**ProGAN: Protein solubility generative adversarial nets for data augmentation in DNN framework**  
Han, Xi, et al.  
[Computers & Chemical Engineering 131 (2019)](https://www.sciencedirect.com/science/article/abs/pii/S0098135419304922)

**Conditional Generative Modeling for De Novo Protein Design with Hierarchical Functions**  
Kucera, Tim, Matteo Togninalli, and Laetitia Meng-Papaxanthos  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.11.10.467885v1.abstract)  

**Expanding functional protein sequence spaces using generative adversarial networks**  
Repecka, Donatas, et al.  
[Nature Machine Intelligence 3.4 (2021)](https://www.nature.com/articles/s42256-021-00310-5)

**HelixGAN: A bidirectional Generative Adversarial Network with search in latent space for generation under constraints**  
Xie, Xuezhi, and Philip M. Kim.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_HelixGAN:_A_bidirectional_Generative.pdf)

### 5.4 NLP-based

**Recurrent neural network model for constructive peptide design**  
Müller, Alex T., Jan A. Hiss, and Gisbert Schneider.  
[Journal of chemical information and modeling 58.2 (2018)](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.7b00414)  

**Pepcvae: Semi-supervised targeted design of antimicrobial peptide sequences**  
Das, Payel, et al.  
[arXiv preprint arXiv:1810.07743 (2018)](https://arxiv.org/abs/1810.07743)

**Deep learning to design nuclear-targeting abiotic miniproteins**  
Schissel, Carly K., et al.  
[Nature Chemistry 13.10 (2021)](https://www.nature.com/articles/s41557-021-00766-3)  

**Protein design and variant prediction using autoregressive generative models**  
Shin, Jung-Eun, et al.  
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-22732-w.pdf) || [code::SeqDesign](https://github.com/debbiemarkslab/SeqDesign) || mutation effect prediction || sequence generation || April 2021  

**ECNet is an evolutionary context-integrated deep learning framework for protein engineering**  
Luo, Yunan, et al.  
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-25976-8)

**Guided Generative Protein Design using Regularized Transformers**  
Castro, Egbert, et al.  
[arXiv preprint arXiv:2201.09948 (2022)](https://arxiv.org/abs/2201.09948)

**Generative Language Modeling for Antibody Design**  
Shuai, Richard W., Jeffrey A. Ruffolo, and Jeffrey J. Gray.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.12.13.472419v1)

**Deep neural language modeling enables functional protein generation across families**  
Madani, Ali, et al.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.07.18.452833.abstract)  

**BioPhi: A platform for antibody design, humanization, and humanness evaluation based on natural antibody repertoires and deep learning**  
Prihoda, David, et al.  
[mAbs. Vol. 14. No. 1. Taylor & Francis, 2022](tandfonline.com/doi/full/10.1080/19420862.2021.2020203)

### 5.5 ResNet-based

**Accelerating protein design using autoregressive generative models**  
Riesselman, Adam, et al.  
[BioRxiv (2019)](https://web.archive.org/web/20190928104354id_/https://www.biorxiv.org/content/biorxiv/early/2019/09/05/757252.full.pdf)

### 5.6 Bayesian-based

**AntBO: Towards Real-World Automated Antibody Design with Combinatorial Bayesian Optimisation**  
Khan, Asif, et al.  
[arXiv preprint(2022)](https://arxiv.org/abs/2201.12570)

### 5.7 Pretrained-based

**Progen: Language modeling for protein generation**  
Madani, Ali, et al.  
[arXiv preprint arXiv:2004.03497 (2020)](https://arxiv.org/abs/2004.03497)

### 5.8 RL-based

**Model-based reinforcement learning for biological sequence design**  
Angermueller, Christof, et al.  
[International conference on learning representations. 2019](https://openreview.net/forum?id=HklxbgBKvr&fileGuid=3xgr169o12oUrbxS)  

## 6.Molecular Design Models

> In consideration of learning more various of generative models for design, these recommended models from **Molecular Design** might be helpful.

### 6.1 Gradient optimization

**Inverse design of 3d molecular structures with conditional generative neural networks**  
Gebauer, Niklas WA, et al.  
[arXiv preprint arXiv:2109.04824 (2021)](https://arxiv.org/abs/2109.04824) || [code](https://github.com/atomistic-machine-learning/cG-SchNet) || Sept 21

**Differentiable scaffolding tree for molecular optimization**  
Fu, T., Gao, W., Xiao, C., Yasonik, J., Coley, C. W., & Sun, J.  
[arXiv preprint arXiv:2109.10469](https://arxiv.org/abs/2109.10469) || [code](https://github.com/futianfan/DST) || Sept 21

### 6.2 Combinatorial optimized sampling

**Structure-based de novo drug design using 3D deep generative models**  
Li, Yibo, Jianfeng Pei, and Luhua Lai.  
[Chemical science 12.41 (2021)](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc04444c)

**A 3D Generative Model for Structure-Based Drug Design**  
Luo, Shitong, et al.  
[Advances in Neural Information Processing Systems 34 (2021)](https://proceedings.neurips.cc/paper/2021/hash/314450613369e0ee72d0da7f6fee773c-Abstract.html)

**CELLS: Cost-Effective Evolution in Latent Space for Goal-Directed Molecular Generation**  
Chen, Zhiyuan, et al.  
[arXiv preprint arXiv:2112.00905 (2021)](https://arxiv.org/abs/2112.00905)  

## 7. Other tasks

### 7.1 Fitness functions / Landscape exploring using latent space

**Deciphering protein evolution and fitness landscapes with latent space models**  
Xinqiang Ding, Zhengting Zou & Charles L. Brooks III  
[Nature Communications](https://www.nature.com/articles/s41467-019-13633-0) || [code](https://github.com/xqding/PEVAE_Paper) || Dec 2019

**The generative capacity of probabilistic protein sequence models**
Francisco McGee, Sandro Hauri, Quentin Novinger, Slobodan Vucetic, Ronald M. Levy, Vincenzo Carnevale & Allan Haldane  
[Nature Communications](https://www.nature.com/articles/s41467-021-26529-9) || [code::generation_capacity_metrics](https://github.com/alagauche/generative_capacity_metrics) || [code::sVAE](https://github.com/ahaldane/MSA_VAE) || Nov 2021  

**Deep generative models of genetic variation capture the effects of mutations**  
Adam J. Riesselman, John B. Ingraham & Debora S. Marks  
[Nature Methods](https://www.nature.com/articles/s41592-018-0138-4) || [code](https://github.com/debbiemarkslab/DeepSequence) || Oct 2018

**Epistatic Net allows the sparse spectral regularization of deep neural networks for inferring fitness functions**  
Amirali Aghazadeh, Hunter Nisonoff, Orhan Ocal, David H. Brookes, Yijie Huang, O. Ozan Koyluoglu, Jennifer Listgarten & Kannan Ramchandran  
[Nature Communications](https://www.nature.com/articles/s41467-021-25371-3) || [code](https://github.com/amirmohan/epistatic-net) || Sep 2021  
