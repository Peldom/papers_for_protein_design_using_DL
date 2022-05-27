# List of papers about Proteins Design using Deep Learning

## About this repository

Inspired by Kevin Kaichuang Yang's [Machine-learning-for-proteins](https://github.com/yangkky/Machine-learning-for-proteins). In terms of the fast changing of **protein design in DL**, my colleagues and I started making this dynamic repository as a record of papers in this field for the newcomers like us.  
My notes of these papers are shared in a **[Zhihu Column](https://www.zhihu.com/column/c_1475864742820929537)** (simplified Chinese).  
Mini protein, metalloprotein, antibody, peptide & molecule designs are included.  
Heading [[2]](#2-model-based-design) follows a **"generator-predictor-optimizer paradigm"**, Heading [[3]](#3-function-to-scaffold)&[[4]](#4scaffold-to-sequence) follow ["Inside-out" paradigm](https://www.nature.com/articles/nature19946)(*function-scaffold-sequence*) from [Baker lab](https://www.bakerlab.org/), Heading [[5]](#5function-to-sequence)&[[7]](#7molecular-design-models) follow other ML/DL strategies.  
[Contributions](https://github.com/Peldom/papers_for_protein_design_using_DL/blob/main/CONTRIBUTING.md) are welcome!

## Menu

- [List of papers about Proteins Design using Deep Learning](#list-of-papers-about-proteins-design-using-deep-learning)
  - [About this repository](#about-this-repository)
  - [Menu](#menu)
  - [0. Benchmarks and datasets](#0-benchmarks-and-datasets)
    - [0.1 Function to sequence](#01-function-to-sequence)
    - [0.2 Structure to sequence](#02-structure-to-sequence)
    - [0.3 Others](#03-others)
      - [0.3.1 Sequence Database](#031-sequence-database)
      - [0.3.2 Structure Database](#032-structure-database)
      - [0.3.3 Protein Structure Datasets](#033-protein-structure-datasets)
  - [1. Reviews](#1-reviews)
  - [2. Model-based design](#2-model-based-design)
    - [2.1 trRosetta-based](#21-trrosetta-based)
    - [2.2 AlphaFold2-based](#22-alphafold2-based)
    - [2.3 DMPfold2-based](#23-dmpfold2-based)
    - [2.4 RoseTTAFold-based](#24-rosettafold-based)
    - [2.5 CM-Align](#25-cm-align)
    - [2.6 MSA-transformer-based](#26-msa-transformer-based)
    - [2.7 DeepAb-based](#27-deepab-based)
  - [3. Function to Scaffold](#3-function-to-scaffold)
    - [3.1 GAN-based](#31-gan-based)
    - [3.2 VAE-based](#32-vae-based)
    - [3.3 DAE-based](#33-dae-based)
    - [3.4 MLP-based](#34-mlp-based)
  - [4.Scaffold to Sequence](#4scaffold-to-sequence)
    - [4.1 MLP-based](#41-mlp-based)
    - [4.2 VAE-based](#42-vae-based)
    - [4.3 LSTM-based](#43-lstm-based)
    - [4.4 CNN-based](#44-cnn-based)
    - [4.5 GNN-based](#45-gnn-based)
    - [4.6 GAN-based](#46-gan-based)
    - [4.7 Transformer-based](#47-transformer-based)
    - [4.8 ResNet-based](#48-resnet-based)
  - [5.Function to Sequence](#5function-to-sequence)
    - [5.1 CNN-based](#51-cnn-based)
    - [5.2 VAE-based](#52-vae-based)
    - [5.3 GAN-based](#53-gan-based)
    - [5.4 Transformer-based](#54-transformer-based)
    - [5.5 ResNet-based](#55-resnet-based)
    - [5.6 Bayesian-based](#56-bayesian-based)
    - [5.7 RL-based](#57-rl-based)
    - [5.8 Flow-based](#58-flow-based)
    - [5.9 RNN-based](#59-rnn-based)
    - [5.10 LSTM-based](#510-lstm-based)
  - [6. Function to Structure](#6-function-to-structure)
    - [6.1 LSTM-based](#61-lstm-based)
  - [7. Other tasks](#7-other-tasks)
    - [7.1 Effects of mutation & Fitness Landscape](#71-effects-of-mutation--fitness-landscape)
    - [7.2 Protein Language Models (PTM) and representation learning](#72-protein-language-models-ptm-and-representation-learning)
    - [7.3 Molecular Design Models](#73-molecular-design-models)
      - [7.3.1 Gradient optimization](#731-gradient-optimization)
      - [7.3.2 Optimized sampling](#732-optimized-sampling)

## 0. Benchmarks and datasets

### 0.1 Function to sequence

**FLIP: Benchmark tasks in fitness landscape inference for proteins**  
Christian Dallago, Jody Mou, Kadina E Johnston, Bruce Wittmann, Nick Bhattacharya, Samuel Goldman, Ali Madani, Kevin K Yang  
[NeurIPS 2021 Datasets and Benchmarks Track](https://openreview.net/forum?id=p2dMLEwL8tF) || [website](https://benchmark.protein.properties/)   

### 0.2 Structure to sequence

**AlphaDesign: A graph protein design method and benchmark on AlphaFoldDB**  
Zhangyang Gao, Cheng Tan, Stan Z. Li  
[arxiv (2022)](https://arxiv.org/abs/2202.01079)

### 0.3 Others

#### 0.3.1 Sequence Database

[UniProt](https://www.uniprot.org/downloads)  

#### 0.3.2 Structure Database

1. [PDB](https://www.rcsb.org/)
2. [AlphaFoldDB](https://alphafold.ebi.ac.uk/)
3. [PDBbind](http://www.pdbbind.org.cn/download.php)

#### 0.3.3 Protein Structure Datasets

**SidechainNet: An All-Atom Protein Structure Dataset for Machine Learning**
Jonathan E. King, David Ryan Koes  
[arxiv](https://arxiv.org/abs/2010.08162) || [github::sidechainnet](https://github.com/jonathanking/sidechainnet)  

[TDC](https://tdcommons.ai/overview/) maintains a resource list that currently contains 22 tasks (and its datasets) related to small molecules and macromolecules, including PPI, DDI and so on. [MoleculeNet](https://github.com/GLambard/Molecules_Dataset_Collection) published a small molecule related benchmark four years ago.

> In terms of datasets and benchmarks, protein design is far less mature than drug discovery ([paperwithcode drug discovery benchmarks](https://paperswithcode.com/task/drug-discovery)). (Maybe should add the evaluation of protein design for deep learning method (especially deep generative model))  
> Difficulties and opportunities always coexist. Happy to see the work of [Christian Dallago, Jody Mou, Kadina E. Johnston, Bruce J. Wittmann, Nicholas Bhattacharya, Samuel Goldman, Ali Madani, Kevin K. Yang](https://www.biorxiv.org/content/10.1101/2021.11.09.467890v1) and [Zhangyang Gao, Cheng Tan, Stan Z. Li](https://arxiv.org/abs/2202.01079). How grateful.

## 1. Reviews

**Deep learning in protein structural modeling and design**  
Wenhao Gao, Sai Pooja Mahajan, Jeremias Sulam, and Jeffrey J. Gray  
[Patterns 1.9](https://www.sciencedirect.com/science/article/pii/S2666389920301902) || 2020  

**Protein sequence design with deep generative models**  
Zachary Wu, Kadina E. Johnston, Frances H. Arnold, Kevin K. Yang  
[Current Opinion in Chemical Biology](https://www.sciencedirect.com/science/article/pii/S136759312100051X) || [note](https://zhuanlan.zhihu.com/p/466616309) || 2021  

**Structure-based protein design with deep learning**  
Ovchinnikov, Sergey, and Po-Ssu Huang.  
[Current opinion in chemical biology](https://www.sciencedirect.com/science/article/pii/S1367593121001125) || [note](https://zhuanlan.zhihu.com/p/467001175) || 2021  

**Protein design via deep learning**  
Wenze Ding, Kenta Nakai, Haipeng Gong  
[Briefings in Bioinformatics](https://academic.oup.com/bib/advance-article/doi/10.1093/bib/bbac102/6554124) || 25 March 2022

**Deep generative modeling for protein design**  
Strokach, Alexey, and Philip M. Kim.  
[Current Opinion in Structural Biology](https://www.sciencedirect.com/science/article/pii/S0959440X21001573) || 2022  

**Deep generative models for peptide design**  
Wan, Fangping, Daphne Kontogiorgos-Heintz, and Cesar de la Fuente-Nunez  
[Digital Discovery (2022)](https://pubs.rsc.org/en/content/articlehtml/2022/dd/d1dd00024a)

## 2. Model-based design

> Invert trained models with optimize algorithms through iterations for sequence design. Inverted structure prediction models are known as **Hallucination**.

### 2.1 trRosetta-based

**Design of proteins presenting discontinuous functional sites using deep learning**  
Doug Tischer, Sidney Lisanza, Jue Wang, Runze Dong,  View ORCID ProfileIvan Anishchenko, Lukas F. Milles, Sergey Ovchinnikov, David Baker  
[bioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.11.29.402743v1.abstract)  

**Fast differentiable DNA and protein sequence optimization for molecular design**  
Linder, Johannes, and Georg Seelig.  
[arXiv preprint arXiv:2005.11275 (2020)](https://arxiv.org/abs/2005.11275)

**De novo protein design by deep network hallucination**  
Ivan Anishchenko, Samuel J. Pellock, Tamuka M. Chidyausiku, Theresa A. Ramelot, Sergey Ovchinnikov, Jingzhou Hao, Khushboo Bafna, Christoffer Norn, Alex Kang, Asim K. Bera, Frank DiMaio, Lauren Carter, Cameron M. Chow, Gaetano T. Montelione & David Baker  
[Nature (2021)](https://doi.org/10.1038/s41586-021-04184-w)  || [code](https://github.com/gjoni/trDesign) || [trRosetta](https://yanglab.nankai.edu.cn/trRosetta/download/) || 

**Protein sequence design by conformational landscape optimization**  
Norn, Christoffer, et al.  
[Proceedings of the National Academy of Sciences 118.11 (2021)](https://www.pnas.org/content/118/11/e2017228118) || [code](https://github.com/gjoni/trDesign)

### 2.2 AlphaFold2-based

**Solubility-aware protein binding peptide design using AlphaFold**  
Takatsugu Kosugi, Masahito Ohue  
[bioRxiv 2022.05.14.491955](https://doi.org/10.1101/2022.05.14.491955) || [Supplemental Materials](https://www.biorxiv.org/content/biorxiv/early/2022/05/15/2022.05.14.491955/DC1/embed/media-1.pdf?download=true)

**End-to-end learning of multiple sequence alignments with differentiable Smith-Waterman**  
Petti, Samantha, Bhattacharya, Nicholas, Rao, Roshan, Dauparas, Justas, Thomas, Neil, Zhou, Juannan, Rush, Alexander M, Koo, Peter K, Ovchinnikov, Sergey  
[bioRxiv (2021)](http://repository.cshl.edu/id/eprint/40409/) || [ColabDesign](https://github.com/sokrypton/ColabDesign), [SMURF](https://github.com/spetti/SMURF), [AF2 back propagation](https://github.com/sokrypton/af_backprop) || [My notes1](https://zhuanlan.zhihu.com/p/468219547), [notes2](https://zhuanlan.zhihu.com/p/472037977)  

**AlphaDesign: A de novo protein design framework based on AlphaFold**  
Jendrusch, Michael, Jan O. Korbel, and S. Kashif Sadiq.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.10.11.463937.abstract)  

**Using AlphaFold for Rapid and Accurate Fixed Backbone Protein Design**  
Moffat, Lewis, Joe G. Greener, and David T. Jones.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.08.24.457549v1)  

### 2.3 DMPfold2-based

**Design in the DARK: Learning Deep Generative Models for De Novo Protein Design**  
Moffat, Lewis, Shaun M. Kandathil, and David T. Jones.  
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.01.27.478087v1.abstract) || [DMPfold2](https://github.com/psipred/DMPfold2)

### 2.4 RoseTTAFold-based

**Deep learning methods for designing proteins scaffolding functional sites**  
Wang J, Lisanza S, Juergens D, Tischer D, Anishchenko I, Baek M, Watson JL, Chun JH, Milles LF, Dauparas J, Expòsit M, Yang W, Saragovi A, Ovchinnikov S, Baker D  
[bioRxiv(2021)](https://europepmc.org/article/ppr/ppr419387) || [RFDesign](https://github.com/RosettaCommons/RFDesign) || [my notes](https://zhuanlan.zhihu.com/p/477854488)

### 2.5 CM-Align

**AutoFoldFinder: An Automated Adaptive Optimization Toolkit for De Novo Protein Fold Design**  
Shuhao Zhang, Youjun Xu, Jianfeng Pei, Luhua Lai  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_AutoFoldFinder.pdf)  

### 2.6 MSA-transformer-based

**Protein language models trained on multiple sequence alignments learn phylogenetic relationships**  
Lupo, Umberto, Damiano Sgarbossa, and Anne-Florence Bitbol.  
[arXiv preprint arXiv:2203.15465 (2022)](https://arxiv.org/abs/2203.15465)

### 2.7 DeepAb-based

**Towards deep learning models for target-specific antibody design**  
Mahajan, Sai Pooja, et al.  
[Biophysical Journal 121.3 (2022)](https://www.cell.com/biophysj/pdf/S0006-3495(21)03758-9.pdf) || [DeepAb](https://github.com/RosettaCommons/DeepAb)

## 3. Function to Scaffold

> These models design backbone/scaffold/template.

### 3.1 GAN-based

**Conditioning by adaptive sampling for robust design**  
Brookes, David, Hahnbeom Park, and Jennifer Listgarten.  
[International conference on machine learning. PMLR, 2019](http://proceedings.mlr.press/v97/brookes19a/brookes19a.pdf)  || without code  

**Fully differentiable full-atom protein backbone generation**  
Anand Namrata, Raphael Eguchi, and Po-Ssu Huang.  
[OpenReview ICLR 2019 workshop DeepGenStruct](https://openreview.net/forum?id=SJxnVL8YOV) || without code  

**RamaNet: Computational de novo helical protein backbone design using a long short-term memory generative neural network**  
Sabban, Sari, and Mikhail Markovsky.  
[F1000Research 9 (2020)](http://f1000researchdata.s3.amazonaws.com/manuscripts/29106/f45e92eb-5d68-4da0-b918-91ded85d2e7d_22907_-_sari_sabban_v2.pdf) || [code](https://sarisabban.github.io/RamaNet/) || pyRosetta || tensorflow || maximizaing the fluorescence of a protein  

**HelixGAN: A bidirectional Generative Adversarial Network with search in latent space for generation under constraints**  
Xuezhi Xie, Philip M. Kim  
[Machine Learning for Structural Biology Workshop, NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_HelixGAN:_A_bidirectional_Generative.pdf) || without code  

### 3.2 VAE-based

**IG-VAE: generative modeling of immunoglobulin proteins by direct 3D coordinate generation**  
Raphael R. Eguchi, Christian A. Choe, Po-Ssu Huang  
[Biorxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.08.07.242347v2) || without code ||  

**Deep sharpening of topological features for de novo protein design**  
Harteveld, Zander, et al.  
[ICLR2022 Machine Learning for Drug Discovery. 2022](https://openreview.net/forum?id=DwN81YIXGQP)

### 3.3 DAE-based

**Function-guided protein design by deep manifold sampling**  
Vladimir Gligorijevic, Stephen Ra, Daniel Berenberg, Richard Bonneau, Kyunghyun Cho  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Function-guided_protein_design_by.pdf) || without code

### 3.4 MLP-based

**A backbone-centred energy function of neural networks for protein design**  
Huang, B., Xu, Y., Hu, X. et al  
[Nature (2022)](https://doi.org/10.1038/s41586-021-04383-5)

## 4.Scaffold to Sequence

> Identify amino sequence from given backbone/scaffold/template constrains: torsion angles(φ & ψ), backbone angles(θ and τ), backbone dihedrals (φ, ψ & ω), backbone atoms (Cα, N, C, & O), Cα − Cα distance, unit direction vectors of Cα−Cα, Cα−N & Cα−C, etc. Referred from [here](https://arxiv.org/abs/2202.01079).

### 4.1 MLP-based

**3D representations of amino acids—applications to protein sequence comparison and classification**  
Li, Jie, and Patrice Koehl.  
[Computational and structural biotechnology journal 11.18 (2014)](https://www.sciencedirect.com/science/article/pii/S2001037014000270) || 2014  

**Direct prediction of profiles of sequences compatible with a protein structure by neural networks with fragment‐based local and energy‐based nonlocal profiles**  
Li, Zhixiu, et al.  
[Proteins: Structure, Function, and Bioinformatics 82.10 (2014)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.24620) || code unavailable

**SPIN2: Predicting sequence profiles from protein structures using deep neural networks**  
O'Connell, James, et al.  
[Proteins: Structure, Function, and Bioinformatics 86.6 (2018)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25489) || code unavailable

**Computational protein design with deep learning neural networks**  
Wang, Jingxue, et al.  
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-24760-x.pdf) || code unavailable

### 4.2 VAE-based

**Design of metalloproteins and novel protein folds using variational autoencoders**  
Greener, Joe G., Lewis Moffat, and David T. Jones.  
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-34533-1)

### 4.3 LSTM-based

**To improve protein sequence profile prediction through image captioning on pairwise residue distance map**  
Chen, Sheng, et al.  
[Journal of chemical information and modeling 60.1 (2019)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00438) || [SPROF](https://github.com/biomed-AI/SPROF)

**Deep learning of Protein Sequence Design of Protein-protein Interactions**  
Syrlybaeva, Raulia, and Eva-Maria Strauch.  
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.01.28.478262v1) || [code](https://github.com/strauchlab/iNNterfaceDesign)


### 4.4 CNN-based

**A structure-based deep learning framework for protein engineering**  
Shroff, Raghav, et al.  
[bioRxiv (2019)](https://www.biorxiv.org/content/10.1101/833905v1.abstract)

**ProDCoNN: Protein design using a convolutional neural network**  
Zhang, Yuan, et al.  
[Proteins: Structure, Function, and Bioinformatics 88.7 (2020)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25868) || code unavailable

**Protein sequence design with a learned potential**  
Namrata Anand, Raphael Eguchi, Irimpan I. Mathews, Carla P. Perez, Alexander Derry, Russ B. Altman & Po-Ssu Huang  
[Nacture Communications (2022)](https://www.nature.com/articles/s41467-022-28313-9) || [code](https://github.com/ProteinDesignLab/protein_seq_des)  

### 4.5 GNN-based

**Learning from protein structure with geometric vector perceptrons**  
Jing, Bowen, et al.  
[arXiv preprint arXiv:2009.01411 (2020)](https://arxiv.org/abs/2009.01411) || [GVP](https://github.com/drorlab/gvp-pytorch)

**Fast and flexible protein design using deep graph neural networks.**  
Alexey Strokach, David Becerra, Carles Corbi-Verge, Albert Perez-Riba, Philip M. Kim  
[Cell Systems (2020)](https://www.sciencedirect.com/science/article/pii/S2405471220303276) || [code::ProteinSolver](https://gitlab.com/ostrokach/proteinsolver)  

**TERMinator: A Neural Framework for Structure-Based Protein Design using Tertiary Repeating Motifs**  
Li, Alex J., et al.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_TERMinator:_A_Neural_Framework.pdf) / [arXiv (2022)](https://arxiv.org/pdf/2204.13048.pdf) 

**Iterative refinement graph neural network for antibody sequence-structure co-design**  
Jin, Wengong, et al.  
[arXiv preprint arXiv:2110.04624 (2021)](https://arxiv.org/abs/2110.04624) || [RefineGNN](https://github.com/wengong-jin/RefineGNN)

**Exploration of novel αβ-protein folds through de novo design**  
Minami, Shintaro, et al.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.08.06.455475v1.abstract) || [GCNdesgin](https://github.com/ShintaroMinami/GCNdesign)

**XENet: Using a new graph convolution to accelerate the timeline for protein design on quantum computers**  
Maguire, Jack B., et al.  
[PLoS computational biology 17.9 (2021)](https://pdfs.semanticscholar.org/23bc/58424378d15fda91e9d427fb553728c38b8a.pdf)

**AlphaDesign: A graph protein design method and benchmark on AlphaFoldDB**  
Gao, Zhangyang, Cheng Tan, and Stan Li.  
[arXiv preprint arXiv:2202.01079 (2022)](https://arxiv.org/abs/2202.01079) || [code](https://github.com/jonathanking/sidechainnet)

**Generative De Novo Protein Design with Global Context**  
Cheng Tan, Zhangyao Gao, Jun Xia and Stan Z. Li  
[arXiv](https://arxiv.org/abs/2204.10673) || Apr 2022

### 4.6 GAN-based

**De novo protein design for novel folds using guided conditional Wasserstein generative adversarial networks**  
Mostafa Karimi, Shaowen Zhu, Yue Cao, Yang Shen  
[Journal of chemical information and modeling 60.12 (2020)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.0c00593) || [gcWGAN](https://github.com/Shen-Lab/gcWGAN)

### 4.7 Transformer-based

**Generative models for graph-based protein design**  
[John Ingraham](https://openreview.net/profile?email=ingraham%40csail.mit.edu), Vikas K Garg, Dr.Regina Barzilay, Tommi Jaakkola  
[NeurIPS 2019](https://openreview.net/forum?id=ByMEAHrgLB) || [GraphTrans](https://github.com/jingraham/neurips19-graph-protein-design)  

**Fold2Seq: A Joint Sequence (1D)-Fold (3D) Embedding-based Generative Model for Protein Design**  
Cao, Yue, et al.  
[International Conference on Machine Learning. PMLR, 2021](https://arxiv.org/pdf/2106.13058)

**Rotamer-Free Protein Sequence Design Based on Deep Learning and Self-Consistency**  
Liu, Yufeng, et al.  
[Nature portfolio (2022)](https://www.researchsquare.com/article/rs-1209166/v1)

**A Deep SE(3)-Equivariant Model for Learning Inverse Protein Folding**  
Mmatthew McPartlon, Ben Lai, Jinbo Xu  
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.15.488492v1)

**Learning inverse folding from millions of predicted structures**  
Chloe Hsu, Robert Verkuil, Jason Liu, Zeming Lin, Brian Hie, Tom Sercu, Adam Lerer, Alexander Rives  
[bioRxiv (2022)](https://doi.org/10.1101/2022.04.10.487779) || [esm](https://github.com/facebookresearch/esm)  

### 4.8 ResNet-based

**DenseCPD: improving the accuracy of neural-network-based computational protein sequence design with DenseNet**  
Qi, Yifei, and John ZH Zhang.  
[Journal of chemical information and modeling 60.3 (2020)](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.0c00043) || code unavailable

## 5.Function to Sequence

> These models generate sequences from expected function.

### 5.1 CNN-based

**Protein design and variant prediction using autoregressive generative models**  
Shin, Jung-Eun, et al.  
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-22732-w.pdf) || [code::SeqDesign](https://github.com/debbiemarkslab/SeqDesign) || mutation effect prediction || sequence generation || April 2021  

### 5.2 VAE-based

**Variational auto-encoding of protein sequences**  
Sinai, Sam, et al.  
[arXiv preprint arXiv:1712.03346 (2017)](https://arxiv.org/abs/1712.03346)

**Pepcvae: Semi-supervised targeted design of antimicrobial peptide sequences**  
Das, Payel, et al.  
[arXiv preprint arXiv:1810.07743 (2018)](https://arxiv.org/abs/1810.07743)

**Deep generative models for T cell receptor protein sequences**  
Davidsen, Kristian, et al.  
[Elife 8 (2019)](https://elifesciences.org/articles/46935)

**How to hallucinate functional proteins**  
Costello, Zak, and Hector Garcia Martin.  
[arXiv preprint arXiv:1903.00458 (2019)](https://arxiv.org/abs/1903.00458)

**Variational autoencoder for generation of antimicrobial peptides**  
Dean, Scott N., and Scott A. Walper.  
[ACS omega 5.33 (2020)](https://pubs.acs.org/doi/abs/10.1021/acsomega.0c00442)

**Generating functional protein variants with variational autoencoders**  
Hawkins-Hooker, Alex, et al.  
[PLoS computational biology 17.2 (2021)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008736)

**Accelerated antimicrobial discovery via deep generative models and molecular dynamics simulations**  
Das, Payel, et al.  
[Nature Biomedical Engineering 5.6 (2021)](https://www.nature.com/articles/s41551-021-00689-x)

**Deep generative models create new and diverse protein structures**  
Zeming, Tom, Yann and Alexander.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Deep_generative_models_create.pdf)

**Therapeutic enzyme engineering using a generative neural network**  
Giessel, Andrew, et al.  
[Scientific Reports 12.1 (2022)](https://www.nature.com/articles/s41598-022-05195-x)

**GM-Pep: A High Efficiency Strategy to De Novo Design Functional Peptide Sequences**  
Chen, Qushuo, et al.  
[Journal of Chemical Information and Modeling (2022)](https://pubs.acs.org/doi/10.1021/acs.jcim.2c00089) || [code](https://github.com/TimothyChen225/GM-Pep)

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

**GANDALF: Peptide Generation for Drug Design using Sequential and Structural Generative Adversarial Networks**  
Rossetto, Allison, and Wenjin Zhou.  
[Proceedings of the 11th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2020](https://dl.acm.org/doi/abs/10.1145/3388440.3412487)

**Generating ampicillin-level antimicrobial peptides with activity-aware generative adversarial networks**  
Tucs, Andrejs, et al.  
[ACS omega 5.36 (2020)](https://pubs.acs.org/doi/abs/10.1021/acsomega.0c02088)

**Conditional Generative Modeling for De Novo Protein Design with Hierarchical Functions**  
Kucera, Tim, Matteo Togninalli, and Laetitia Meng-Papaxanthos  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.11.10.467885v1.abstract)  

**Expanding functional protein sequence spaces using generative adversarial networks**  
Repecka, Donatas, et al.  
[Nature Machine Intelligence 3.4 (2021)](https://www.nature.com/articles/s42256-021-00310-5)

**HelixGAN: A bidirectional Generative Adversarial Network with search in latent space for generation under constraints**  
Xie, Xuezhi, and Philip M. Kim.  
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_HelixGAN:_A_bidirectional_Generative.pdf)

**A Generative Approach toward Precision Antimicrobial Peptide Design.**  
Ferrell, Jonathon B., et al.  
[BioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2020.10.02.324087.abstract)

**AMPGAN v2: Machine Learning-Guided Design of Antimicrobial Peptides**  
Van Oort, Colin M., et al.  
[Journal of chemical information and modeling 61.5 (2021)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.0c01441)

**DeepImmuno: deep learning-empowered prediction and generation of immunogenic peptides for T-cell immunity**  
Li, Guangyuan, et al.  
[Briefings in bioinformatics 22.6 (2021)](https://academic.oup.com/bib/article-abstract/22/6/bbab160/6261914)

**PandoraGAN: Generating antiviral peptides using Generative Adversarial Network**  
Surana, Shraddha, et al.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.02.15.431193.abstract)

### 5.4 Transformer-based

**Progen: Language modeling for protein generation**  
Madani, Ali, et al.  
[arXiv preprint arXiv:2004.03497 (2020)](https://arxiv.org/abs/2004.03497)

**Signal peptides generated by attention-based neural networks**  
Wu, Zachary, et al.  
[ACS Synthetic Biology 9.8 (2020)](https://pubs.acs.org/doi/full/10.1021/acssynbio.0c00219)

**Generative Language Modeling for Antibody Design**  
Shuai, Richard W., Jeffrey A. Ruffolo, and Jeffrey J. Gray.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.12.13.472419v1)

**Deep neural language modeling enables functional protein generation across families**  
Madani, Ali, et al.  
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.07.18.452833.abstract)  

**BioPhi: A platform for antibody design, humanization, and humanness evaluation based on natural antibody repertoires and deep learning**  
Prihoda, David, et al.  
[mAbs. Vol. 14. No. 1. Taylor & Francis, 2022](tandfonline.com/doi/full/10.1080/19420862.2021.2020203)

**Guided Generative Protein Design using Regularized Transformers**  
Castro, Egbert, et al.  
[arXiv preprint arXiv:2201.09948 (2022)](https://arxiv.org/abs/2201.09948)

**A deep unsupervised language model for protein design**  
Noelia Ferruz,  View ProfileSteffen Schmidt,  View ProfileBirte Höcker  
[bioRxiv](https://www.biorxiv.org/content/10.1101/2022.03.09.483666v1.full) || [model::huggingface](https://huggingface.co/nferruz/ProtGPT2) [datasets::hugingface](https://huggingface.co/datasets/nferruz/UR50_2021_04) || March 12 2022

**Few Shot Protein Generation**  
Ram, Soumya, and Tristan Bepler.  
[arXiv preprint arXiv:2204.01168 (2022)](https://arxiv.org/abs/2204.01168)

### 5.5 ResNet-based

**Accelerating protein design using autoregressive generative models**  
Riesselman, Adam, et al.  
[BioRxiv (2019)](https://web.archive.org/web/20190928104354id_/https://www.biorxiv.org/content/biorxiv/early/2019/09/05/757252.full.pdf)

### 5.6 Bayesian-based

**AntBO: Towards Real-World Automated Antibody Design with Combinatorial Bayesian Optimisation**  
Khan, Asif, et al.  
[arXiv preprint(2022)](https://arxiv.org/abs/2201.12570)

**Discovering de novo peptide substrates for enzymes using machine learning**  
Tallorin, Lorillee, et al.  
[Nature communications 9.1 (2018)](https://www.nature.com/articles/s41467-018-07717-6) || [code](https://github.com/peter-i-frazier/pool)

### 5.7 RL-based

**Model-based reinforcement learning for biological sequence design**  
Angermueller, Christof, et al.  
[International conference on learning representations. 2019](https://openreview.net/forum?id=HklxbgBKvr&fileGuid=3xgr169o12oUrbxS)  

### 5.8 Flow-based

**Biological Sequence Design with GFlowNets**  
Jain, Moksh, et al.  
[arXiv preprint arXiv:2203.04115 (2022)](https://arxiv.org/abs/2203.04115)

### 5.9 RNN-based

**Deep learning to design nuclear-targeting abiotic miniproteins**  
Schissel, Carly K., et al.  
[Nature Chemistry 13.10 (2021)](https://www.nature.com/articles/s41557-021-00766-3) || [code](https://github.com/learningmatter-mit/peptimizer)

**Recurrent neural network model for constructive peptide design**  
Müller, Alex T., Jan A. Hiss, and Gisbert Schneider.  
[Journal of chemical information and modeling 58.2 (2018)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.7b00414)

**Machine learning designs non-hemolytic antimicrobial peptides**  
Capecchi, Alice, et al.  
[Chemical Science 12.26 (2021)](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc01713f)

**Using molecular dynamics simulations to prioritize and understand AI-generated cell penetrating peptides**  
Tran, Duy Phuoc, et al.  
[Scientific reports 11.1 (2021)](https://www.nature.com/articles/s41598-021-90245-z)

### 5.10 LSTM-based

**Computational antimicrobial peptide design and evaluation against multidrug-resistant clinical isolates of bacteria**  
Nagarajan, Deepesh, et al  
[Journal of Biological Chemistry 293.10 (2018)](https://www.jbc.org/article/S0021-9258(20)40390-4/fulltext)

**Deep learning enables the design of functional de novo antimicrobial proteins**  
Caceres-Delpiano, Javier, et al.  
[bioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.08.26.266940v1.full)

**ECNet is an evolutionary context-integrated deep learning framework for protein engineering**  
Luo, Yunan, et al.  
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-25976-8)

**Deep learning for novel antimicrobial peptide design**  
Wang, Christina, Sam Garlick, and Mire Zloh.  
[Biomolecules 11.3 (2021)](https://www.mdpi.com/2218-273X/11/3/471)

**Deep learning to design nuclear-targeting abiotic miniproteins**  
Schissel, Carly K., et al.  
[Nature Chemistry 13.10 (2021)](https://www.nature.com/articles/s41557-021-00766-3)  

## 6. Function to Structure

> These models generate structures(including side chains) from expected function.

### 6.1 LSTM-based

**One-sided design of protein-protein interaction motifs using deep learning**  
Syrlybaeva, Raulia, and Eva-Maria Strauch.  
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.03.30.486144v2) || [code](https://github.com/strauchlab/iNNterfaceDesign)

## 7. Other tasks

### 7.1 Effects of mutation & Fitness Landscape

**Deep generative models of genetic variation capture the effects of mutations**  
Adam J. Riesselman, John B. Ingraham & Debora S. Marks  
[Nature Methods](https://www.nature.com/articles/s41592-018-0138-4) || [code::DeepSequence](https://github.com/debbiemarkslab/DeepSequence) || Oct 2018

**Deciphering protein evolution and fitness landscapes with latent space models**  
Xinqiang Ding, Zhengting Zou & Charles L. Brooks III  
[Nature Communications](https://www.nature.com/articles/s41467-019-13633-0) || [code::PEVAE](https://github.com/xqding/PEVAE_Paper) || Dec 2019

**The generative capacity of probabilistic protein sequence models**
Francisco McGee, Sandro Hauri, Quentin Novinger, Slobodan Vucetic, Ronald M. Levy, Vincenzo Carnevale & Allan Haldane  
[Nature Communications](https://www.nature.com/articles/s41467-021-26529-9) || [code::generation_capacity_metrics](https://github.com/alagauche/generative_capacity_metrics) || [code::sVAE](https://github.com/ahaldane/MSA_VAE) || Nov 2021  

**Epistatic Net allows the sparse spectral regularization of deep neural networks for inferring fitness functions**  
Amirali Aghazadeh, Hunter Nisonoff, Orhan Ocal, David H. Brookes, Yijie Huang, O. Ozan Koyluoglu, Jennifer Listgarten & Kannan Ramchandran  
[Nature Communications](https://www.nature.com/articles/s41467-021-25371-3) || [code](https://github.com/amirmohan/epistatic-net) || Sep 2021  

**Proximal Exploration for Model-guided Protein Sequence Design**  
Zhizhou Ren, Jiahan Li, Fan Ding, Yuan Zhou, Jianzhu Ma, Jian Peng  
[BioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.12.487986v1)

**Efficient evolution of human antibodies from general protein language models and sequence information alone**  
Hie, Brian L., et al.  
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.10.487811v1) || [code](https://github.com/brianhie/efficient-evolution)

### 7.2 Protein Language Models (PTM) and representation learning

**Protein Structure Representation Learning by Geometric Pretraining**  
Zuobai Zhang, Minghao Xu, Arian Jamasb, Vijil Chenthamarakshan, Aurelie Lozano, Payel Das, Jian Tang  
[arXiv](https://arxiv.org/abs/2203.06125) || Jan 2022

### 7.3 Molecular Design Models

> Unlike **function-scaffold-sequence** paradigm in protein design, major molecular design models based on paradigm form DL from 3 kinds of level: **atom-based**, **fragment-based**, **reaction-based**, and they can be categorized as [Gradient optimization](#61-gradient-optimization) or [Optimized sampling](#62-optimized-sampling)(gradient-free). [Click here for detail review](https://www.sciencedirect.com/science/article/pii/S1359644621002531)  
> In consideration of learning more various of generative models for design, these recommended latest models from **Molecular Design** might be helpful and even be able to be transplanted to protein design.

#### 7.3.1 Gradient optimization

**Inverse design of 3d molecular structures with conditional generative neural networks**  
Gebauer, Niklas WA, et al.  
[arXiv preprint arXiv:2109.04824 (2021)](https://arxiv.org/abs/2109.04824) || [code](https://github.com/atomistic-machine-learning/cG-SchNet) || Sept 21

**Differentiable scaffolding tree for molecular optimization**  
Fu, T., Gao, W., Xiao, C., Yasonik, J., Coley, C. W., & Sun, J.  
[arXiv preprint arXiv:2109.10469](https://arxiv.org/abs/2109.10469) || [code](https://github.com/futianfan/DST) || Sept 21

#### 7.3.2 Optimized sampling

**De novo drug design framework based on mathematical programming method and deep learning model**  
Yujing Zhao, Qilei Liu*, Xinyuan Wu, Lei Zhang, Jian Du*, Qingwei Meng.  
[AIChE Journal. 2022, e17748](https://doi.org/10.1002/aic.17748)

**Structure-based de novo drug design using 3D deep generative models**  
Li, Yibo, Jianfeng Pei, and Luhua Lai.  
[Chemical science 12.41 (2021)](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc04444c)

**A 3D Generative Model for Structure-Based Drug Design**  
Luo, Shitong, et al.  
[Advances in Neural Information Processing Systems 34 (2021)](https://proceedings.neurips.cc/paper/2021/hash/314450613369e0ee72d0da7f6fee773c-Abstract.html)

**CELLS: Cost-Effective Evolution in Latent Space for Goal-Directed Molecular Generation**  
Chen, Zhiyuan, et al.  
[arXiv preprint arXiv:2112.00905 (2021)](https://arxiv.org/abs/2112.00905)  

**Generating 3D Molecules for Target Protein Binding**  
Meng Liu, Youzhi Luo, Kanji Uchino, Koji Maruhashi, Shuiwang Ji  
[arxiv (2022)](https://arxiv.org/abs/2204.09410) || [GraphBP](https://github.com/divelab/graphbp)

**Optimizing molecules using efficient queries from property evaluations**  
Hoffman, Samuel C., et al.  
[Nature Machine Intelligence 4.1 (2022)](https://www.nature.com/articles/s42256-021-00422-y)

**Deep Evolutionary Learning for Molecular Design**  
K. Grantham, M. Mukaidaisi, H. K. Ooi, M. S. Ghaemi, A. Tchagang and Y. Li  
[IEEE Computational Intelligence Magazine, vol. 17, no. 2, pp. 14-28, May 2022](https://ieeexplore.ieee.org/document/9756593)

<!-- ### 7.4  -->
