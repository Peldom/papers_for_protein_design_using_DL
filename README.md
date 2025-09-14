# List of papers about Protein Design using Deep Learning

> This repository is inspired by the remarkable work of [Kevin Kaichuang Yang](https://github.com/yangkky) and their outstanding project [Machine-learning-for-proteins](https://github.com/yangkky/Machine-learning-for-proteins). We have established this repository to provide a specialized and focused platform for the field of **Deep Learning for Protein Design**, a rapidly advancing domain in computational biology.
>
> [Contributions](https://github.com/Peldom/papers_for_protein_design_using_DL/blob/main/CONTRIBUTING.md) and [suggestions](https://github.com/Peldom/papers_for_protein_design_using_DL/issues) are warmly welcome!
> Community Values, Guiding Principles, and Commitments for the Responsible Development of AI for Protein Design: [details](https://responsiblebiodesign.ai/)

<!-- >
>1. Mini protein, binders, metalloprotein, antibody, peptide & molecule designs are included  
>2. More de novo protein design paper list at [Wangchentong](https://github.com/Wangchentong)'s GitHub repo: [paper_for_denovo_protein_design](https://github.com/Wangchentong/paper_for_denovo_protein_design)  
>3. Our notes of these papers are shared in a **[Zhihu Column](https://www.zhihu.com/column/c_1475864742820929537)** (simplified Chinese/English), more suggested notes at [RosettAI](https://www.zhihu.com/column/rosettastudy)   -->

*Papers last week, updated on 2025.09.14:*
+   Generative latent diffusion language modeling yields anti-infective synthetic peptides
    + [[Cell Biomaterials (2025)](https://www.cell.com/cell-biomaterials/fulltext/S3050-5623(25)]00174-6) • [[code](https://github.com/programmablebio/amp-diffusion)]
+   De novo design of phosphorylation-induced protein switches for synthetic signaling in cells
    + [[bioRxiv 2025.09.10.675034](https://www.biorxiv.org/content/10.1101/2025.09.10.675034v1)]
+   LSMTCR: A Scalable Multi-Architecture Model for Epitope-Specific T Cell Receptor de novo Design
    + [[arXiv:2509.07627](https://arxiv.org/abs/2509.07627)]
+   PepCCD: A Contrastive Conditioned Diffusion Framework for Target-Specific Peptide Generation
    + [[bioRxiv 2025.09.01.673427](https://www.biorxiv.org/content/10.1101/2025.09.01.673427v1)] • [[Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/09/04/2025.09.01.673427/DC1/embed/media-1.pdf)]
+   AI-driven protein design
    + [[Nat Rev Bioeng (2025)](https://www.nature.com/articles/s44222-025-00349-8)]




---

<p align="center">
  <br>
  <!-- <img src="dl_pd.png" alt="deep learning for protein design" width="500"> -->
  <img src="cover.jpg" alt="deep learning for protein design">
</p>
<!-- ## Menu -->
<!-- > Heading [[2]](#2-model-based-design) follows a **"generator-predictor-optimizer" paradigm**, Heading [[3]](#3-function-to-scaffold), [[4]](#4scaffold-to-sequence)&[[6]](#6-function-to-structure) follow ["Inside-out" paradigm](https://www.nature.com/articles/nature19946)(*function-scaffold-sequence*) from [RosettaCommons](https://www.rosettacommons.org/), Heading [[5]](#5function-to-sequence)&[[7]](#7-other-tasks) follow other ML/DL strategies   -->
<p align='center'>
  <strong><a href='#0-benchmarks-and-datasets'>0) Benchmarks and datasets </a></strong>
  <br>
  <a href="#01-sequence-datasets-benchmarks">Sequence dataset/benchmarks</a> •
  <a href="#02-structure-datasets-benchmarks">Structure datasets/benchmarks</a> •
  <a href="#03-databases">Public database</a> •
  <a href="#04-similar-list">Similar list</a> •
  <a href="#05-guides">Guides</a>
  <br>
  <strong><a href="#1-reviews">1) Reviews and surveys</a></strong>
  <br>
  <a href="#11-de-novo-protein-design">De novo design</a> •
  <a href="#12-antibody-design">Antibody design</a> •
  <a href="#13-peptide-design">Peptide design</a> •
  <a href="#14-binder-design">Binder design</a> •
  <a href="#15-enzyme-design">Enzyme design</a>
  <br>
  <strong><a href="#2-model-based-design">2) Model-based design</a></strong>
  <br>
  <a href="#21-structure-prediction-model-based">Structure Prediction Model-based</a> •
  <a href="#22-cm-align">CM-Align</a> •
  <a href="#23-msa-transformer-based">MSA transformer-based</a> •
  <a href="#24-LLM-based">LLM-based</a> •
  <a href="#25-sampling-algorithms">Sampling-algorithms</a>
  <br>
  <strong><a href="#3-function-to-scaffold" class="large-link">3) Function to Scaffold</a></strong>
  <br>
  <a href="#31-gan-based">GAN-based</a> •
  <a href="#32-autoencoder-based">AutoEncoder-based</a> •
  <a href="#33-mlp-based">MLP-based</a> •
  <a href="#34-diffusion-based">Diffusion-based</a> •
  <a href="#35-rl-based">RL-based</a> •
  <a href="#36-flow-based">Flow-based</a> •
  <a href="#37-score-based">Score-based</a>
  <br>
  <strong><a href="#4scaffold-to-sequence">4) Scaffold to Sequence</a></strong>
  <br>
  <a href="#40-review">Review</a> •
  <a href="#41-mlp-based">MLP-based</a> •
  <a href="#42-vae-based">VAE-based</a> •
  <a href="#43-lstm-based">LSTM-based</a> •
  <a href="#44-cnn-based">CNN-based</a> •
  <a href="#45-gnn-based">GNN-based</a> •
  <a href="#46-gan-based">GAN-based</a> •
  <a href="#47-transformer-based">Transformer-based</a> •
  <a href="#48-resnet-based">ResNet-based</a> •
  <a href="#49-diffusion-based">Diffusion-based</a> •
  <a href="#410-bayesian-based">Bayesian method</a> •
  <a href="#411-flow-based">Flow-based</a> •
  <a href="#412-rl-based">RL-based</a> •
  <a href="#413-train-method">Train method</a>
  <br>
  <strong><a href="#5function-to-sequence">5) Function to Sequence</a></strong>
  <br>
  <a href="#51-cnn-based">CNN-based</a> •
  <a href="#52-vae-based">VAE-based</a> •
  <a href="#53-gan-based">GAN-based</a> •
  <a href="#54-transformer-based">Transformer-based</a> •
  <a href="#55-bayesian-based">Bayesian method</a> •
  <a href="#56-rl-based">Reinforcement Learning</a> •
  <a href="#57-flow-based">Flow-based</a> •
  <a href="#58-rnn-based">RNN-based</a> •
  <a href="#59-lstm-based">LSTM-based</a> •
  <a href="#510-autoregressive-models">Autoregressive</a> •
  <a href="#511-boltzmann-machine-based">Boltzmann machine</a> •
  <a href="#512-diffusion-based">Diffusion-based</a> •
  <a href="#513-gnn-based">GNN-based</a> •
  <a href="#514-score-based">Score-based</a>
  <br>
  <strong><a href="#6-function-to-structure">6) Function to Structure</a></strong>
  <br>
  <a href="#60-review">Review</a> •
  <a href="#61-lstm-based">LSTM-based</a> •
  <a href="#62-diffusion-based">Diffusion-based</a> •
  <a href="#63-rosettafold-based">RoseTTAFold-based</a> •
  <a href="#64-cnn-based">CNN-based</a> •
  <a href="#65-gnn-based">GNN-based</a> •
  <a href="#66-transformer-based">Transformer-based</a> •
  <a href="#67-mlp-based">MLP-based</a> •
  <a href="#68-flow-based">Flow-based</a> •
  <a href="#69-alphafold-based">AlphaFold-based</a>
  <br>
  <strong><a href="#7-other-tasks">7) Other</a></strong>
  <br>
  <a href="#71-effects-of-mutation--fitness-landscape">Effects of mutations & Fitness Landscape</a>  •
  <a href="#72-protein-language-models-plm-and-representation-learning">Protein Language Model & Representation Learning</a>  •
  <a href="#73-molecular-design-models">Molecular Design Model</a> •
  <a href="#74-unclassified">Unclassified</a>
</p>

---

## 0. Benchmarks and datasets

### 0.1 Sequence Datasets, Benchmarks

**FLIP: Benchmark tasks in fitness landscape inference for proteins**
Christian Dallago, Jody Mou, Kadina E Johnston, Bruce Wittmann, Nick Bhattacharya, Samuel Goldman, Ali Madani, Kevin K Yang
[NeurIPS 2021 Datasets and Benchmarks Track](https://openreview.net/forum?id=p2dMLEwL8tF)/[bioRxiv 2021](https://www.biorxiv.org/content/10.1101/2021.11.09.467890v2) • [website](https://benchmark.protein.properties/) • [code](https://github.com/J-SNACKKB/FLIP) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/01/19/2021.11.09.467890/DC1/embed/media-1.pdf)

**A Benchmark Framework for Evaluating Structure-to-Sequence Models for Protein Design**
Jeffrey Chan, Seyone Chithrananda, David Brookes, Sam Sinai
Paper unavailable at [Machine Learning in Structural Biology Workshop 2022](https://nips.cc/Conferences/2022/ScheduleMultitrack?event=50005)

**PDBench: Evaluating Computational Methods for Protein-Sequence Design**
Leonardo V Castorina, Rokas Petrenas, Kartic Subr, Christopher W Wood
[Bioinformatics, 2023;, btad027](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btad027/6986968) • [code](https://github.com/wells-wood-research/PDBench)

**Benchmarking deep generative models for diverse antibody sequence design**
Igor Melnyk, Payel Das, Vijil Chenthamarakshan, Aurelie Lozano
[arXiv:2111.06801](https://arxiv.org/abs/2111.06801)

**The Protein Engineering Tournament: An Open Science Benchmark for Protein Modeling and Design**
Chase Armer, Hassan Kane, Dana Cortade, Dave Estell, Adil Yusuf, Radhakrishna Sanka, Henning Redestig, TJ Brunette, Pete Kelly, Erika DeBenedictis
[arXiv:2309.09955](https://arxiv.org/abs/2309.09955v2)

**Computational Scoring and Experimental Evaluation of Enzymes Generated by Neural Networks**
Sean R.Johnson, Xiaozhi Fu, Sandra Viknander, Clara Goldin, Sarah Monaco, Aleksej Zelezniak, Kevin K. Yang
[bioRxiv (2023)](https://www.biorxiv.org/content/10.1101/2023.03.04.531015v2) • [code](https://github.com/seanrjohnson/protein_scoring)

**FLOP: Tasks for Fitness Landscapes Of Protein Wildtypes**
Peter Mørch Groth, Richard Michael, Jesper Salomon, Pengfei Tian, Wouter Boomsma
[bioRxiv 2023.06.21.545880](https://www.biorxiv.org/content/10.1101/2023.06.21.545880v2) • [code](https://github.com/petergroth/FLOP)

**ProteinGym: Large-Scale Benchmarks for Protein Design and Fitness Prediction**
Pascal Notin, Aaron W Kollasch, Daniel Ritter, Lood van Niekerk, Steffanie Paul, Hansen Spinner, Nathan Rollins, Ada Shaw, Ruben Weitzman, Jonathan Frazer, Mafalda Dias, Dinko Franceschi, Rose Orenbuch, Yarin Gal, Debora S Marks
[bioRxiv 2023.12.07.570727](https://biorxiv.org/content/10.1101/2023.12.07.570727v1) • [code](https://github.com/OATML-Markslab/ProteinGym)

**Results of the Protein Engineering Tournament: An Open Science Benchmark for Protein Modeling and Design**
Chase Armer, Hassan Kane, Dana L. Cortade, Henning Redestig, David A. Estell, Adil Yusuf, Nathan Rollins, Hansen Spinner, Debora Marks, TJ Brunette, Peter J. Kelly, Erika DeBenedictis
[bioRxiv 2024.08.12.606135](https://www.biorxiv.org/content/10.1101/2024.08.12.606135v1)/[Proteins: Structure, Function, and Bioinformatics (2025)](https://onlinelibrary.wiley.com/doi/10.1002/prot.70008) • [code](https://github.com/the-protein-engineering-tournament/pet-pilot-2023) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/08/12/2024.08.12.606135/DC1/embed/media-1.pdf)

**Generative AI Models for the Protein Scaffold Filling Problem**
Letu Qingge, Kushal Badal, Richard Annan, Jordan Sturtz, Xiaowen Liu, and Binhai Zhu
[Journal of Computational Biology](https://www.liebertpub.com/doi/10.1089/cmb.2024.0510)

**Benchmarking Inverse Folding Models for Antibody CDR Sequence Design**
Per Junior Greisen, Yifan Li, Yuxiang Lang, Chenrui Xu, Yi Zhou, Ziwei Pang
[bioRxiv 2024.12.16.628614](https://www.biorxiv.org/content/10.1101/2024.12.16.628614v1)

**Self-supervised machine learning methods for protein design improve sampling but not the identification of high-fitness variants**
Moritz Ertelt, Rocco Moretti, Jens Meiler, and Clara T. Schoeder
[Science Advances 11.7 (2025)](https://www.science.org/doi/10.1126/sciadv.adr7338) • [code](https://github.com/meilerlab/probabilities_design)

**Crowdsourced Protein Design: Lessons From the Adaptyv EGFR Binder Competition**
Tudor-Stefan Cotet, Igor Krawczuk, Filippo Stocco, Noelia Ferruz, Anthony Gitter, Yoichi Kurumida, Lucas de Almeida Machado, Francesco Paesani, Cianna N. Calia, Chance A. Challacombe, Nikhil Haas, Ahmad Qamar, Bruno E. Correia, Martin Pacesa, Lennart Nickel, Kartic Subr, Leonardo V. Castorina, Maxwell J. Campbell, Constance Ferragu, Patrick Kidger, Logan Hallee, Christopher W. Wood, Michael J. Stam, Tadas Kluonis, Suleyman Mert Unal, Elian Belot, Alexander Naka, Adaptyv Competition Organizers
[bioRxiv 2025.04.17.648362](https://www.biorxiv.org/content/10.1101/2025.04.17.648362v2) • [github](https://github.com/adaptyvbio/egfr2024_post_competition)

**Experimental Evaluation of AI-Driven Protein Design Risks Using Safe Biological Proxies**  
Svetlana P. Ikonomova, Bruce J. Wittmann, Fernanda Piorino, David J. Ross, Samuel W. Schaffter, Olga Vasilyeva, Eric Horvitz, James Diggans, Elizabeth A. Strychalski, Sheng Lin-Gibson, Geoffrey J. Taghon  
[bioRxiv 2025.05.15.654077](https://www.biorxiv.org/content/10.1101/2025.05.15.654077v1) • [code](https://github.com/usnistgov/AIPD_TEVV/)

**Benchmark for Antibody Binding Affinity Maturation and Design**  
Xinyan Zhao, Yi-Ching Tang, Akshita Singh, Victor J Cantu, KwanHo An, Junseok Lee, Adam E Stogsdill, Ashwin Kumar Ramesh, Zhiqiang An, Xiaoqian Jiang, Yejin Kim  
[arXiv:2506.04235](https://arxiv.org/abs/2506.04235) • [dataset](https://huggingface.co/datasets/AbBibench/Antibody_Binding_Benchmark_Dataset) • [code](https://github.com/MSBMI-SAFE/AbBiBench)

**The Dayhoff Atlas: scaling sequence diversity for improved protein generation**  
Kevin K. Yang, Sarah Alamdari, Alex J. Lee, Kaeli Kaymak-Loveless, Samir Char, Garyk Brixi, Carles Domingo-Enrich, Chentong Wang, Suyue Lyu, Nicolo Fusi, Neil Tenenholtz, Ava P. Amini  
[bioRxiv 2025.07.21.665991](https://www.biorxiv.org/content/10.1101/2025.07.21.665991v1) • [code](https://github.com/microsoft/dayhoff) • [dataset](https://huggingface.co/collections/microsoft/dayhoff-atlas-6866d679465a2685b06ee969)

### 0.2 Structure Datasets, Benchmarks

**AlphaDesign: A graph protein design method and benchmark on AlphaFoldDB**
Zhangyang Gao, Cheng Tan, Stan Z. Li
[arxiv (2022)](https://arxiv.org/abs/2202.01079)

**SidechainNet: An All-Atom Protein Structure Dataset for Machine Learning**
Jonathan E. King, David Ryan Koes
[arxiv](https://arxiv.org/abs/2010.08162) • [github::sidechainnet](https://github.com/jonathanking/sidechainnet)

[TDC](https://tdcommons.ai/overview/) maintains a resource list that currently contains 22 tasks (and its datasets) related to small molecules and macromolecules, including PPI, DDI and so on. [MoleculeNet](https://github.com/GLambard/Molecules_Dataset_Collection) published a small molecule related benchmark four years ago.

> In terms of datasets and benchmarks, protein design is far less mature than drug discovery ([paperwithcode drug discovery benchmarks](https://paperswithcode.com/task/drug-discovery)). (Maybe should add the evaluation of protein design for deep learning method (especially deep generative model))
> Difficulties and opportunities always coexist. Happy to see the work of [Christian Dallago, Jody Mou, Kadina E. Johnston, Bruce J. Wittmann, Nicholas Bhattacharya, Samuel Goldman, Ali Madani, Kevin K. Yang](https://www.biorxiv.org/content/10.1101/2021.11.09.467890v1) and [Zhangyang Gao, Cheng Tan, Stan Z. Li](https://arxiv.org/abs/2202.01079).

**Sampling of structure and sequence space of small protein folds**
Thomas W. Linsky, Kyle Noble, Autumn R. Tobin, Rachel Crow, Lauren Carter, Jeffrey L. Urbauer, David Baker & Eva-Maria Strauch
[Nat Commun 13, 7151 (2022)](https://www.nature.com/articles/s41467-022-34937-8) • [code](https://github.com/strauchlab/scaffold_design) • [Supplementary](https://static-content.springer.com/esm/art%3A10.1038%2Fs41467-022-34937-8/MediaObjects/41467_2022_34937_MOESM1_ESM.pdf)

**OpenProteinSet: Training data for structural biology at scale**
Gustaf Ahdritz, Nazim Bouatta, Sachin Kadyan, Lukas Jarosch, Daniel Berenberg, Ian Fisk, Andrew M. Watkins, Stephen Ra, Richard Bonneau, Mohammed AlQuraishi
[arXiv:2308.05326](https://arxiv.org/abs/2308.05326) • [OpenFold](https://github.com/aqlaboratory/openfold)

**ProteinInvBench: Benchmarking Protein Design on Diverse Tasks, Models, and Metrics**
Zhangyang Gao, Cheng Tan, Yijie Zhang, Xingran Chen, Stan Z. Li
[GitHub](https://github.com/A4Bio/ProteinInvBench)

**PDB-Struct: A Comprehensive Benchmark for Structure-based Protein Design**
Chuanrui Wang, Bozitao Zhong, Zuobai Zhang, Narendra Chaudhary, Sanchit Misra, Jian Tang
[arXiv preprint arXiv:2312.00080 (2023)](https://arxiv.org/abs/2312.00080) • [code](https://github.com/WANG-CR/PDB-Struct)

**Scaffold-Lab: Critical Evaluation and Ranking of Protein Backbone Generation Methods in A Unified Framework**
Zhuoqi Zheng, Bo Zhang, Bozitao Zhong, Kexin Liu, Jinyu Yu, Zhengxin Li, JunJie Zhu, Ting Wei, Hai-Feng Chen
[bioRxiv 2024.02.10.579743](https://www.biorxiv.org/content/10.1101/2024.02.10.579743v1) • [code](https://github.com/Immortals-33/Scaffold-Lab) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/02/12/2024.02.10.579743/DC1/embed/media-1.pdf)

**Antibody DomainBed: Out-of-Distribution Generalization in Therapeutic Protein Design**
Nataša Tagasovska, Ji Won Park, Matthieu Kirchmeyer, Nathan C. Frey, Andrew Martin Watkins, Aya Abdelsalam Ismail, Arian Rokkum Jamasb, Edith Lee, Tyler Bryson, Stephen Ra, Kyunghyun Cho
[arXiv:2407.21028](https://arxiv.org/abs/2407.21028) • [code](https://github.com/prescient-design/antibody-domainbed) • [dataset](https://www.dropbox.com/scl/fo/e670i9adp29yv2knfu6wd/h?rlkey=uax6phjjfumkk8xoxrbwcit1h&e=1&dl=0)

**Large protein databases reveal structural complementarity and functional locality**
Paweł Szczerbiak, Lukasz Szydlowski, Witold Wydmański, P. Douglas Renfrew, Julia Koehler Leman, Tomasz Kosciolek
[bioRxiv 2024.08.14.607935](https://www.biorxiv.org/content/10.1101/2024.08.14.607935v1) • [code](https://github.com/Tomasz-Lab/protein-structure-landscape) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/08/14/2024.08.14.607935/DC1/embed/media-1.pdf) • [website](https://protein-structure-landscape.sano.science/)

**The Protein Design Archive (PDA): insights from 40 years of protein design**
Marta Chronowska, Michael J. Stam, Derek N. Woolfson, Luigi F. Di Constanzo, Christopher W. Wood
[bioRxiv 2024.09.05.611465](https://www.biorxiv.org/content/10.1101/2024.09.05.611465v1)/[Nat Biotechnol (2025)](https://www.nature.com/articles/s41587-025-02607-x) • [code](https://github.com/wells-wood-research/chronowska-stam-wood-2024-protein-design-archive) • [Supplementary](hhttps://www.biorxiv.org/content/biorxiv/early/2024/09/07/2024.09.05.611465/DC1/embed/media-1.docx) • [website](https://pragmaticproteindesign.bio.ed.ac.uk/pda/)

**ProteinBench: A Holistic Evaluation of Protein Foundation Models**
Fei Ye, Zaixiang Zheng, Dongyu Xue, Yuning Shen, Lihao Wang, Yiming Ma, Yan Wang, Xinyou Wang, Xiangxin Zhou, Quanquan Gu
[arXiv:2409.06744](https://arxiv.org/abs/2409.06744) • [code](https://proteinbench.github.io/)

**Benchmarking Generative Models for Antibody Design & Exploring Log-Likelihood for Sequence Ranking**
Talip Uçar, Cedric Malherbe, Ferran Gonzalez
[bioRxiv 2024.10.07.617023](https://www.biorxiv.org/content/10.1101/2024.10.07.617023v3) • [code](https://github.com/AstraZeneca/DiffAbXL)

**Towards Robust Evaluation of Protein Generative Models: A Systematic Analysis of Metrics**
Pavel Strashnov, Andrey Shevtsov, Viacheslav Meshchaninov, Maria Ivanova, Fedor Nikolaev, Olga Kardymon, Dmitry Vetrov
[bioRxiv 2024.10.25.620213](https://www.biorxiv.org/content/10.1101/2024.10.25.620213v1)

**MotifBench: A standardized protein design benchmark for motif-scaffolding problems**
Zhuoqi Zheng, Bo Zhang, Kieran Didi, Kevin K. Yang, Jason Yim, Joseph L. Watson, Hai-Feng Chen, Brian L. Trippe
[arXiv:2502.12479](https://arxiv.org/abs/2502.12479) • [code](https://github.com/blt2114/MotifBench)

**Systematic comparison of Generative AI-Protein Models reveals fundamental differences between structural and sequence-based approaches**
Alexander J Barnett, KC Rajendra, Pratikshya Pandey, Pamodha Somasiri, Kirsten A Fairfax, Sandy Hung, Alex W Hewitt
[bioRxiv 2025.03.23.644844](https://www.biorxiv.org/content/10.1101/2025.03.23.644844v1) • [code](https://github.com/hewittlab/Systematic-comparison-of-Generative-AI-Protein-Models) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/03/24/2025.03.23.644844/DC1/embed/media-1.docx)

**Conformation-specific Design: a New Benchmark and Algorithm with Application to Engineer a Constitutively Active Map Kinase**  
Jacob A. Stern, Siba Alharbi, Anandsukeerthi Sandholu, Stefan T. Arold, Dennis Della Corte  
[bioRxiv 2025.04.23.650138](https://www.biorxiv.org/content/10.1101/2025.04.23.650138v1) • [code](https://github.com/dellacortelab/cs_design) • [dataset](https://github.com/dellacortelab/motif_div)

**PRIDE-New-Benchmark-Dataset-For-Protein-Structural-Design**  
Hanqun CAO, dchenhe  
[github](https://github.com/chq1155/PRIDE_Benchmark_ProteinDesign)

**Protein FID: Improved Evaluation of Protein Structure Generative Models**  
Felix Faltings, Hannes Stark, Tommi Jaakkola, Regina Barzilay  
[arXiv:2505.08041](https://arxiv.org/abs/2505.08041)

**PDFBench: A Benchmark for De novo Protein Design from Function**  
Jiahao Kuang, Nuowei Liu, Changzhi Sun, Tao Ji, Yuanbin Wu  
[arXiv:2505.20346](https://arxiv.org/abs/2505.20346) • [website](https://pdfbench.github.io/) • [code](https://github.com/pdfbench/PDFBench)

**An improved model for prediction of de novo designed proteins with diverse geometries**  
Benjamin Orr, Stephanie E Crilly, Deniz Akpinaroglu, Eleanor Zhu, Michael J. Keiser, Tanja Kortemme  
[bioRxiv 2025.06.02.657515](https://www.biorxiv.org/content/10.1101/2025.06.02.657515v1)

**Protein-SE(3): Benchmarking SE(3)-based Generative Models for Protein Structure Design**  
Lang Yu, Zhangyang Gao, Cheng Tan, Qin Chen, Jie Zhou, Liang He
[arXiv:2507.20243](https://arxiv.org/abs/2507.20243v1)

**Evaluating zero-shot prediction of protein design success by AlphaFold, ESMFold, and ProteinMPNN**  
Mario Garcia, Gabriel Jacob Rocklin, Sugyan Dixit  
[bioRxiv 2025.07.29.667290](https://www.biorxiv.org/content/10.1101/2025.07.29.667290v1)

**Predicting Experimental Success in De Novo Binder Design: A Meta-Analysis of 3,766 Experimentally Characterised Binders**  
Max Daniel Overath, Andreas Rygaard, Christian Peder Jacobsen, Valentas Brasas, Oliver Morell, Pietro Sormanni, Timothy Patrick Jenkins  
[bioRxiv 2025.08.14.670059](https://www.biorxiv.org/content/10.1101/2025.08.14.670059v1) • [dataset](https://zenodo.org/records/15722219)

### 0.3 Databases

> A list of suggested protein databases, more lists at [CNCB](https://ngdc.cncb.ac.cn/databasecommons/).

#### 0.3.1 Sequence Database

1. [UniProt](https://www.uniprot.org/downloads)
2. [DisProt](https://disprot.org)
3. [MobiDB](https://mobidb.bio.unipd.it/)
4. [Peptipedia](https://app.peptipedia.cl/)

#### 0.3.2 Structure Database

| Database                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PDB](https://www.rcsb.org/)                                   | The Protein Data Bank (PDB) is a database of 3D structural data of large biological molecules, such as proteins and nucleic acids. These data are gathered using experimental methods such as X-ray crystallography, NMR spectroscopy, or cryo-electron microscopy                                                                                                                                                                                                                                                                |
| [AlphaFoldDB](https://alphafold.ebi.ac.uk/)                    | AlphaFoldDB is a database of protein structure predictions produced by DeepMind's AlphaFold system. It provides highly accurate predictions of protein 3D structures                                                                                                                                                                                                                                                                                                                                                              |
| [PDBbind](http://www.pdbbind.org.cn/download.php)              | PDBbind is a comprehensive collection of the binding data of all types of biomolecular complexes in the PDB database. It is primarily used for the development and validation of computational methods for predicting molecular interactions                                                                                                                                                                                                                                                                                      |
| [AB-Bind](https://github.com/sarahsirin/AB-Bind-Database)      | AB-Bind is a database for antibody binding affinity data. It offers a curated set of experimental binding data and corresponding antibody-protein complex structures                                                                                                                                                                                                                                                                                                                                                              |
| [AntigenDB](http://crdd.osdd.net/raghava/antigendb/)           | AntigenDB is a manually curated database of experimentally verified antigens that includes detailed information about the antigen, the source organism, and the associated antibodies                                                                                                                                                                                                                                                                                                                                             |
| [CAMEO](https://www.cameo3d.org/)                              | CAMEO (Continuous Automated Model EvaluatiOn) is a project for the automated evaluation of methods predicting macromolecular structure. It continuously assesses the performance of automated protein structure prediction servers                                                                                                                                                                                                                                                                                                |
| [CAPRI](https://www.ebi.ac.uk/msd-srv/capri/)                  | The Critical Assessment of PRediction of Interactions (CAPRI) is a community-wide experiment to evaluate protein-protein interaction prediction methods                                                                                                                                                                                                                                                                                                                                                                           |
| [PIFACE](http://prism.ccbb.ku.edu.tr/piface)                   | PIFACE is a web server for the prediction of protein-protein interactions. It identifies potential interaction interfaces on protein surfaces                                                                                                                                                                                                                                                                                                                                                                                     |
| [SAbDab](http://opig.stats.ox.ac.uk/webapps/newsabdab/sabdab/) | The Structural Antibody Database (SAbDab) is an automatically updated resource for the structural information of antibodies from the PDB. It allows for easy access to curated, annotated, and classified antibody structures                                                                                                                                                                                                                                                                                                     |
| [SKEMPI v2.0](https://life.bsc.es/pid/skempi2)                 | SKEMPI 2.0 is a database of experimental measurements of the change in binding free energy caused by mutations in protein-protein complexes                                                                                                                                                                                                                                                                                                                                                                                       |
| [ProtCAD](http://dunbrack2.fccc.edu/protcad/)                  | ProtCAD is a suite of tools for the design and engineering of novel protein structures, sequences, and functions. It allows users to build and manipulate complex protein structures, generate and evaluate sequence libraries, and simulate mutational effects. ProtCAD is a suite of tools for the design and engineering of novel protein structures, sequences, and functions. It allows users to build and manipulate complex protein structures, generate and evaluate sequence libraries, and simulate mutational effects. |

### 0.4 Similar List

> Some similar GitHub lists that include papers about protein design using deep learning:

1. [design_tools](https://github.com/hefeda/design_tools/blob/main/README.md)
2. [awesome-AI-based-protein-design](https://github.com/opendilab/awesome-AI-based-protein-design)
3. [ProteinStructureWithDL](https://github.com/Yang-J-LIN/ProteinStructureWithDL)
4. [List of available bioinformatic tools and services](https://neurosnap.ai/services)

### 0.5 Guides

Guides/Tutorials for beginners on GitHub:

1. [how_to_create_a_protein](https://github.com/universvm/how_to_create_a_protein)
2. [protein-design-tutorials](https://github.com/ProteinDesignLab/protein-design-tutorials)

Collection of Protein Design Labs:

- [ProteinDesignLabs](https://github.com/Zuricho/ProteinDesignLabs)

## 1. Reviews

### 1.1 De novo protein design

**Protein design: from computer models to artificial intelligence**
Antonella Paladino, Filippo Marchetti, Silvia Rinaldi, Giorgio Colombo
[Wiley Interdisciplinary Reviews: Computational Molecular Science 7.5 (2017): e1318](https://wires.onlinelibrary.wiley.com/doi/10.1002/wcms.1318)

**Advances in protein structure prediction and design**
Brian Kuhlman, Philip Bradley
[Nat Rev Mol Cell Biol 20, 681-697 (2019)](https://www.nature.com/articles/s41580-019-0163-x)

**Deep learning in protein structural modeling and design**
Wenhao Gao, Sai Pooja Mahajan, Jeremias Sulam, and Jeffrey J. Gray
[Patterns 1.9](https://www.sciencedirect.com/science/article/pii/S2666389920301902) • 2020

**100th anniversary of macromolecular science viewpoint: Data-driven protein design**
Ferguson, Andrew L., and Rama Ranganathan
[ACS Macro Letters 10.3 (2021)](https://pubs.acs.org/doi/abs/10.1021/acsmacrolett.0c00885)

**Artificial intelligence in early drug discovery enabling precision medicine**
Fabio Bonioloa, Emilio Dorigattia, Alexander J. Ohnmachta, Dieter Saurb, Benjamin Schuberta, and Michael P. Menden
[Expert Opinion on Drug Discovery 16.9 (2021)](https://www.tandfonline.com/doi/full/10.1080/17460441.2021.1918096)

**Protein design with deep learning**
Defresne, Marianne, Sophie Barbe, and Thomas Schiex
[International Journal of Molecular Sciences 22.21 (2021)](https://www.mdpi.com/1422-0067/22/21/11741)

**Protein sequence design with deep generative models**
Zachary Wu, Kadina E. Johnston, Frances H. Arnold, Kevin K. Yang
[Current Opinion in Chemical Biology 65](https://www.sciencedirect.com/science/article/pii/S136759312100051X) • [note](https://zhuanlan.zhihu.com/p/466616309) • 2021

**Structure-based protein design with deep learning**
Ovchinnikov, Sergey, and Po-Ssu Huang
[Current opinion in chemical biology 65](https://www.sciencedirect.com/science/article/pii/S1367593121001125) • [note](https://zhuanlan.zhihu.com/p/467001175) • 2021

**Deep learning techniques have significantly impacted protein structure prediction and protein design**
Pearce, Robin, and Yang Zhang
[Current opinion in structural biology 68 (2021)](https://www.sciencedirect.com/science/article/pii/S0959440X21000142)

**Recent advances in de novo protein design: Principles, methods, and applications**
Pan, Xingjie, and Tanja Kortemme
[Journal of Biological Chemistry 296 (2021)](https://www.sciencedirect.com/science/article/pii/S0021925821003367)

**Protein design via deep learning**
Wenze Ding, Kenta Nakai, Haipeng Gong
[Briefings in Bioinformatics](https://academic.oup.com/bib/advance-article/doi/10.1093/bib/bbac102/6554124) • 25 March 2022

**Deep generative modeling for protein design**
Strokach, Alexey, and Philip M. Kim
[Current Opinion in Structural Biology](https://www.sciencedirect.com/science/article/pii/S0959440X21001573) • 2022

**Dawn of a new era for membrane protein design**
Sowlati-Hashjin, Shahin, Aanshi Gandhi, and Michael Garton
[BioDesign Research (2022)](https://spj.science.org/doi/10.34133/2022/9791435)

**Deep learning approaches for conformational flexibility and switching properties in protein design**
Rudden, Lucas SP, Mahdi Hijazi, and Patrick Barth
[Frontiers in Molecular Biosciences](https://www.frontiersin.org/articles/10.3389/fmolb.2022.928534/full)

**Computational protein design with evolutionary-based and physics-inspired modeling: current and future synergies**
Cyril Malbranke, David Bikard, Simona Cocco, Rémi Monasson, Jérôme Tubiana
[arXiv:2208.13616v2](https://arxiv.org/abs/2208.13616v2)

**From sequence to function through structure: deep learning for protein design**
Noelia Ferruz, Michael Heinzinger, Mehmet Akdel, Alexander Goncearenco, Luca Naef, Christian Dallago
[bioRxiv 2022.08.31.505981](https://www.biorxiv.org/content/10.1101/2022.08.31.505981v1)/[Computational and Structural Biotechnology Journal Volume 21, 2023](https://www.sciencedirect.com/science/article/pii/S2001037022005086) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/09/03/2022.08.31.505981/DC1/embed/media-1.pdf) • [accompanying list](https://github.com/hefeda/design_tools/blob/main/README.md)

**Computational protein design with data-driven approaches: Recent developments and perspectives**
Haiyan Liu, Quan Chen
[WIREs Comput Mol Sci. 2022. e1646](https://wires.onlinelibrary.wiley.com/doi/10.1002/wcms.1646)

**Understanding by design: Implementing deep learning from protein structure prediction to protein design**
Gao, Yuanxu, Jiangshan Zhan, and Albert CH Yu
[MedComm-Future Medicine 1.2 (2022): e22](https://onlinelibrary.wiley.com/doi/full/10.1002/mef2.22)

**Diffusion Models in Bioinformatics: A New Wave of Deep Learning Revolution in Action**
Zhiye Guo, Jian Liu, Yanli Wang, Mengrui Chen, Duolin Wang, Dong Xu, Jianlin Cheng
[arXiv:2302.10907](https://arxiv.org/abs/2302.10907)

**Machine learning for evolutionary-based and physicsinspired protein design: Current and future synergies**
Cyril Malbranke, David Bikard, Simona Cocco, Rémi Monasson, Jérôme Tubiana
[Current Opinion in Structural Biology](https://www.sciencedirect.com/science/article/pii/S0959440X23000453)

**De novo design of polyhedral protein assemblies: before and after the AI revolution**
Bhoomika Basu Mallik, Jenna Stanislaw, Tharindu Madhusankha Alawathurage, and Alena Khmelinskaia
[ChemBioChem 2023, e202300117](http://dx.doi.org/10.1002/cbic.202300117)

**Research progress of artificial intelligence in protein design**
CHEN Zhihang, JI Menglin, QI Yifei
[Synthetic Biology Journal (2023)](https://synbioj.cip.com.cn/article/2023/2096-8280/2023-008.shtml)

**A Survey on Graph Diffusion Models: Generative AI in Science for Molecule, Protein and Material**
Mengchun Zhang, Maryam Qamar, Taegoo Kang, Yuna Jung, Chenshuang Zhang, Sung-Ho Bae, Chaoning Zhang
[https://arxiv.org/abs/2304.01565](https://arxiv.org/pdf/2304.01565.pdf)

**Exploring the Protein Sequence Space with Global Generative Models**
Sergio Romero-Romero, Sebastian Lindner, Noelia Ferruz
[arXiv:2305.01941](https://arxiv.org/abs/2305.01941)

**The Era of Machine Learning for Protein Design, Summarized in Four Key Methods**
LucianoSphere
[Towards Data Science](https://towardsdatascience.com/the-era-of-machine-learning-for-protein-design-summarized-in-four-key-methods-d6f1dac5de96)

**Is novelty predictable?**
Clara Fannjiang, Jennifer Listgarten
[arXiv:2306.00872](https://arxiv.org/abs/2306.00872)

**Computational protein design - where it goes?**
Xu Binbin, Chen Yingjun and Xue Weiwei
[Current Medicinal Chemistry 2023](https://www.eurekaselect.com/article/132267)

**How can the protein design community best support biologists who want to harness AI tools for protein structure prediction and design?**
Birte Höcker, Peilong Lu, Anum Glasgow, Debora S. Marks
Pranam Chatterjee, Joanna S.G. Slusky, Ora Schueler-Furman, Possu Huang
[Cell Systems 14.8 (2023)](https://www.cell.com/cell-systems/fulltext/S2405-4712(23)00212-0)

**De novo 設計ナノポアの創製**
新津藍
[生物工学会誌 101.8 (2023)](https://www.jstage.jst.go.jp/article/seibutsukogaku/101/8/101_101.8_431/_article/-char/ja/)

**Generative artificial intelligence for de novo protein design**
Adam Winnifrith, Carlos Outeiral, Brian Hie
[arXiv:2310.09685](https://arxiv.org/abs/2310.09685)

**Intelligent Protein Design and Molecular Characterization Techniques: A Comprehensive Review**
Jingjing Wang, Chang Chen, Ge Yao, Junjie Ding, Liangliang Wang and Hui Jiang
[Molecules 28.23 (2023)](https://www.mdpi.com/1420-3049/28/23/7865)

**Generative models for protein sequence modeling: recent advances and future directions**
Mehrsa Mardikoraem, Zirui Wang, Nathaniel Pascual, Daniel Woldring
[Briefings in Bioinformatics](https://academic.oup.com/bib/article/24/6/bbad358/7325909)

**A new age in protein design empowered by deep learning**
Hamed Khakzad, Ilia Igashov, Arne Schneuing, Casper Goverde, Michael Bronstein, Bruno Correia
[Cell Systems, Volume 14, Issue 11](https://www.cell.com/cell-systems/fulltext/S2405-4712(23)00298-3)

**Deep learning for protein structure prediction and design—progress and applications**
Jürgen Jänes and Pedro Beltrao
[Mol Syst Biol(2024)](https://www.embopress.org/doi/full/10.1038/s44320-024-00016-x)

**De novo protein design—From new structures to programmable functions**
Tanja Kortemme
[Cell 187.3 (2024)](https://www.cell.com/cell/fulltext/S0092-8674(23)01402-2)

**Generative models for protein structures and sequences**
Chloe Hsu, Clara Fannjiang & Jennifer Listgarten
[Nat Biotechnol 42, 196–199 (2024)](https://www.nature.com/articles/s41587-023-02115-w)

**What does it take for an ‘AlphaFold Moment’ in functional protein engineering and design?**
Roberto A. Chica & Noelia Ferruz
[Nat Biotechnol 42, 173–174 (2024)](https://www.nature.com/articles/s41587-023-02120-z)

**Protein design: the experts speak**
Anne Doerr
[Nat Biotechnol 42, 175–178 (2024)](https://www.nature.com/articles/s41587-023-02111-0)

**Machine learning for functional protein design**
Pascal Notin, Nathan Rollins, Yarin Gal, Chris Sander & Debora Marks
[Nat Biotechnol 42, 216–228 (2024)](https://www.nature.com/articles/s41587-024-02127-0)

**Sparks of function by de novo protein design**
Alexander E. Chu, Tianyu Lu & Po-Ssu Huang
[Nat Biotechnol 42, 203–215 (2024)](https://www.nature.com/articles/s41587-024-02133-2) • [poster](https://drive.google.com/file/d/1sG3OlEWvhHcWAdtf7RTcCawAapDmyeEx/view)

**A Survey of Generative AI for De Novo Drug Design: New Frontiers in Molecule and Protein Generation**
Xiangru Tang, Howard Dai, Elizabeth Knight, Fang Wu, Yunyang Li, Tianxiao Li, Mark Gerstein
[arXiv:2402.08703](https://arxiv.org/abs/2402.08703)

**Security challenges by AI-assisted protein design**
Philip Hunter
[EMBO Rep(2024)](https://www.embopress.org/doi/full/10.1038/s44319-024-00124-7)

**Opportunities and challenges in design and optimization of protein function**
Dina Listov, Casper A. Goverde, Bruno E. Correia & Sarel Jacob Fleishman
[Nat Rev Mol Cell Biol (2024)](https://www.nature.com/articles/s41580-024-00718-y)

**The State-of-the-Art Overview to Application of Deep Learning in Accurate Protein Design and Structure Prediction**
Saber Saharkhiz, Mehrnaz Mostafavi, Amin Birashk, Shiva Karimian, Shayan Khalilollah, Sohrab Jaferian, Yalda Yazdani, Iraj Alipourfard, Yun Suk Huh, Marzieh Ramezani Farani & Reza Akhavan-Sigari
[Top Curr Chem (Z) 382, 23 (2024)](https://link.springer.com/article/10.1007/s41061-024-00469-6)

**Computational methods for protein design**
Noelia Ferruz, Amelie Stein
[Protein Engineering, Design and Selection, Volume 37, 2024](https://academic.oup.com/peds/article/doi/10.1093/protein/gzae011/7710436)

**Structure-based protein and small molecule generation using EGNN and diffusion models: A comprehensive review**
Farzan Soleymani, Eric Paquet, Herna Lydia Viktor, Wojtek Michalowski
[Computational and Structural Biotechnology Journal (2024)](https://www.sciencedirect.com/science/article/pii/S2001037024002228)

**Machine learning in biological physics: From biomolecular prediction to design**
Jonathan Martin, Marcos Lequerica Mateos, José N. Onuchic, and Faruck Morcos
[Proceedings of the National Academy of Sciences 121.27 (2024)](https://www.pnas.org/doi/10.1073/pnas.2311807121)

**AI has dreamt up a blizzard of new proteins. Do any of them actually work?**
Ewen Callaway
[Nature 634.8034 (2024)](https://www.nature.com/articles/d41586-024-03335-z)

**Five protein-design questions that still challenge AI**
Sara Reardon
[Nature 635.8037 (2024)](https://www.nature.com/articles/d41586-024-03595-9)

**De novo protein design in the age of artificial intelligence**
Nan Liu, Xiaocheng Jin, Chongzhou Yang, Ziyang Wang, Xiaoping Min, Shengxiang Ge
[Sheng Wu Gong Cheng Xue Bao](https://doi.org/10.13345/j.cjb.240087)

**Generative Models in Protein Engineering: A Comprehensive Survey**
Chen Xinhui, Yiwen Yuan, Joseph Liu, Chak Tou Leong, Xiaoye Zhu, Jiaqi Chen
[Neurips 2024 Workshop](https://openreview.net/forum?id=Xc7l84S0Ao)

**A Survey of Deep Learning Methods in Protein Bioinformatics and its Impact on Protein Design**
Weihang Dai
[arXiv:2501.01477](https://arxiv.org/abs/2501.01477)

**The Promise of Protein Design: A Q&A with Nobel Laureate David Baker**
David Baker and Fay Lin
[GEN Biotechnology (2025)](https://www.liebertpub.com/doi/abs/10.1089/genbio.2025.0004?journalCode=genbio)

**Protein design and structure solution for drug discovery**
Petra Bombicz
[Crystallography Reviews (2024)](https://www.tandfonline.com/doi/full/10.1080/0889311X.2024.2461923)

**A Model-Centric Review of Deep Learning for Protein Design**
Gregory W. Kyro, Tianyin Qiu, Victor S. Batista
[arXiv:2502.19173](https://arxiv.org/abs/2502.19173)

**Computational protein design**
Katherine I. Albanese, Sophie Barbe, Shunsuke Tagami, Derek N. Woolfson & Thomas Schiex
[Nature Reviews Methods Primers 5.1 (2025)](https://www.nature.com/articles/s43586-025-00383-1)

**Exploring the Blueprint of Life: The Innovation in Antibody and Protein Design**
Yang, Zhiwei, and Gerald H. Lushington
[Combinatorial chemistry &amp; high throughput screening](https://www.eurekaselect.com/article/146786)

**Advanced Deep Learning Methods for Protein Structure Prediction and Design**
Yichao Zhang, Ningyuan Deng, Xinyuan Song, Ziqian Bi, Tianyang Wang, Zheyu Yao, Keyu Chen, Ming Li, Qian Niu, Junyu Liu, Benji Peng, Sen Zhang, Ming Liu, Li Zhang, Xuanhe Pan, Jinlang Wang, Pohsun Feng, Yizhu Wen, Lawrence KQ Yan, Hongming Tseng, Yan Zhong, Yunze Wang, Ziyuan Qin, Bowen Jing, Junjie Yang, Jun Zhou, Chia Xin Liang, Junhao Song
[arXiv:2503.13522](https://arxiv.org/abs/2503.13522)

**Deep Learning-Driven Protein Structure Prediction and Design: Key Model Developments by Nobel Laureates and Multi-Domain Applications**
Wanqing Yang, Yanwei Wang, Yang Wang
[arXiv:2504.01490](https://arxiv.org/abs/2504.01490)

**Intelligent mining, engineering, and de novo design of proteins**
LIU Cui, SHI Zhenkun, MA Hongwu, LIAO Xiaoping
[Sheng wu gong cheng xue bao= Chinese journal of biotechnology 41.3 (2025)](https://cjb.ijournals.cn/html/cjbcn/2025/3/07240629.htm)

**Protein-based Materials: Applications, Modification and Molecular Design**  
Alitenai Tunuhe, Ze Zheng, Xinran Rao, Hongbo Yu, Fuying Ma, Yaxian Zhou, Shangxian Xie  
[BioDesign Research (2025)](https://www.sciencedirect.com/science/article/pii/S2693125725000056)

**Artificial intelligence is transforming the study of proteins: Structures and beyond**  
Haiyan Liu, Quan Chen, and Yufeng Liu  
[hLife (2025)](https://www.sciencedirect.com/science/article/pii/S2949928325000021)

**Artificial intelligence methods for protein folding and design**  
Zhidian Zhang, Chenxi Ou, Yehlin Cho, Yo Akiyama, Sergey Ovchinnikov  
[Current Opinion in Structural Biology 93 (2025)](https://www.sciencedirect.com/science/article/abs/pii/S0959440X25000843)

**AI4Protein: transforming the future of protein design**  
Dequan Wang, Zheling Tan, Jin Gao, Shaoting Zhang, Jiaqi Shen & Yuming Lu  
[Science China Life Sciences (2025)](https://link.springer.com/article/10.1007/s11427-024-2906-3)

**Comment on the Use of AI-based Protein Design for Autoimmune Encephalitis: Exciting Possibilities and Practical Considerations**  
Zengwei Kou  
[Multiple Sclerosis and Related Disorders (2025)](https://www.msard-journal.com/article/S2211-0348(25)00335-9/fulltext)

**Computational Protein Design: Advancing Biotechnology through In Silico Engineering**  
Ranjit Ranbhor, Ruthvik Venkatesan, Amay Sanjay Redkar, Vibin Ramakrishnan  
[Progress in Biophysics and Molecular Biology (2025)](https://www.sciencedirect.com/science/article/pii/S0079610725000380)

**Advances of computational protein design: Principles, strategies and applications in nutrition and health**  
Ziling Zhao, Qiyang Qu, Fuwei Sun, Jiachen Zang, Bowen Zheng, Tuo Zhang, 
Guanghua Zhao, Chenyan Lv, Zhongjiang Wang  
[Biotechnology Advances (2025)](https://www.sciencedirect.com/science/article/pii/S0734975025001429)

**Artificial intelligence in de novo protein design**  
Yao, Jiawei, and Xiaogang Wang  
[Medicine in Novel Technology and Devices (2025)](https://www.sciencedirect.com/science/article/pii/S2590093525000177)

**AI-driven protein design**  
Huan Yee Koh, Yizhen Zheng, Madeleine Yang, Rohit Arora, Geoffrey I. Webb, Shirui Pan, Li Li & George M. Church  
[Nat Rev Bioeng (2025)](https://www.nature.com/articles/s44222-025-00349-8)

### 1.2 Antibody design

**A review of deep learning methods for antibodies**
Jordan Graves, Jacob Byerly, Eduardo Priego, Naren Makkapati , S. Vince Parish, Brenda Medellin and Monica Berrondo
[Antibodies 9.2 (2020)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7344881/pdf/antibodies-09-00012.pdf)

**Progress and challenges for the machine learning-based design of fit-for-purpose monoclonal antibodies**
Rahmad Akbar, Habib Bashour, Puneet Rawat, Philippe A. Robert, Eva Smorodina, Tudor-Stefan Cotet, Karine Flem-Karlsen, Robert Frank, Brij Bhushan Mehta, Mai Ha Vu, Talip Zengin, Jose Gutierrez-Marcos, Fridtjof Lund-Johansen,  Jan Terje Andersen, and Victor Greif
[Mabs. Vol. 14. No. 1. Taylor &amp; Francis, 2022](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8928824/)

**Advances in computational structure-based antibody design**
Hummer, Alissa M., Brennan Abanades, and Charlotte M. Deane
[Current Opinion in Structural Biology 74 (2022)](https://www.sciencedirect.com/science/article/pii/S0959440X22000586)

**Computational and artificial intelligence-based methods for antibody development**
Jisun Kim, Matthew McFee, Qiao Fang, Osama Abdin, Philip M. Kim
[Trends in Pharmacological Sciences (2023)](https://www.sciencedirect.com/science/article/pii/S0165614722002796)

**Leveraging deep learning to improve vaccine design**
Andrew P. Hederman, Margaret E. Ackerman
[Trends in immunology (2023)](https://www.cell.com/trends/immunology/fulltext/S1471-4906(23)00046-7)

**In Silico Approaches to Deliver Better Antibodies by Design: The Past, the Present and the Future**
Andreas Evers, Shipra Malhotra, Vanita D. Sood
[arXiv:2305.07488](https://arxiv.org/abs/2305.07488)

**AI Models for Protein Design are Driving Antibody Engineering**
Michael Chungyoun, Jeffrey J. Gray
[Current Opinion in Biomedical Engineering (2023): 100473](https://www.sciencedirect.com/science/article/abs/pii/S2468451123000296)

**Computational Methods in Immunology and Vaccinology: Design and Development of Antibodies and Immunogens**
Federica Guarra and Giorgio Colombo
[Journal of Chemical Theory and Computation (2023)](https://pubs.acs.org/doi/10.1021/acs.jctc.3c00513)

**Simplifying complex antibody engineering using machine learning**
Makowski, Emily K., Hsin-Ting Chen, and Peter M. Tessier
[Cell Systems 14.8 (2023)](https://www.cell.com/cell-systems/fulltext/S2405-4712(23)00118-7)/[2022 AIChE Annual Meeting. AIChE, 2022.](https://aiche.confex.com/aiche/2022/meetingapp.cgi/Paper/650993)

**AI driven B-cell Immunotherapy Design**
Bruna Moreira da Silva, David B. Ascher, Nicholas Geard, Douglas E. V. Pires
[arXiv:2309.01122](https://arxiv.org/abs/2309.01122)

**Best practices for machine learning in antibody discovery and development**
Leonard Wossnig, Norbert Furtmann, Andrew Buchanan, Sandeep Kumar, Victor Greiff
[arXiv:2312.08470](https://arxiv.org/abs/2312.08470)/[Drug Discovery Today (2024)](https://www.sciencedirect.com/science/article/pii/S1359644624001508)

**Next generation of multispecific antibody engineering**
Daniel Keri, Matt Walker, Isha Singh, Kyle Nishikawa, Fernando Garces
[Antibody Therapeutics (2023): tbad027](https://academic.oup.com/abt/article/7/1/37/7463325)

**A primer on ML in antibody engineering**
[ABHISHAIKE MAHAJAN](https://substack.com/@abhishaikemahajan)
[Substack](https://www.abhishaike.com/p/a-primer-on-ai-in-antibody-engineering) • blog

**Antibody design using deep learning: from sequence and structure design to affinity maturation**
Sara Joubbi, Alessio Micheli, Paolo Milazzo, Giuseppe Maccari, Giorgio Ciano, Dario Cardamone, Duccio Medini
[Briefings in Bioinformatics, Volume 25, Issue 4, July 2024, bbae307](https://academic.oup.com/bib/article/25/4/bbae307/7705535)

**AI-accelerated therapeutic antibody development: practical insights**
Luca Santuari, Marianne Bachmann Salvy, Ioannis Xenarios, Bulak Arpat
[Frontiers in Drug Discovery 4 (2024)](https://www.frontiersin.org/journals/drug-discovery/articles/10.3389/fddsv.2024.1447867/full)

**AI-driven antibody design with generative diffusion models: current insights and future directions**
Xin-heng He, Jun-rui Li, James Xu, Hong Shan, Shi-yi Shen, Si-han Gao & H. Eric Xu
[Acta Pharmacologica Sinica (2024)](https://www.nature.com/articles/s41401-024-01380-y)

**Applying computational protein design to therapeutic antibody discovery -- current state and perspectives**
Weronika Bielska, Igor Jaszczyszyn, Pawel Dudzic, Bartosz Janusz, Dawid Chomicz, Sonia Wrobel, Victor Greiff, Ryan Feehan, Jared Adolf-Bryfogle, Konrad Krawczyk
[arXiv:2503.00913](https://arxiv.org/abs/2503.00913)/[Frontiers in Immunology 16 (2025)](https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2025.1571371/full)

**Artificial intelligence-driven computational methods for antibody design and optimization**  
Luiz Felipe Vecchietti, Bryan Nathanael Wijaya, Azamat Armanuly,Begench Hangeldiyev, Hyunkyu Jung, Sooyeon Lee, Meeyoung Cha & Ho Min Kim  
[mAbs, 2025](https://www.tandfonline.com/doi/full/10.1080/19420862.2025.2528902)

**Artificial intelligence in antibody design and development: harnessing the power of computational approaches**  
Soudabeh Kavousipour, Mahdi Barazesh, Shiva Mohammadi  
[Medical & Biological Engineering & Computing (2025)](https://link.springer.com/article/10.1007/s11517-025-03429-4)

### 1.3 Peptide design

**Deep generative models for peptide design**
Wan, Fangping, Daphne Kontogiorgos-Heintz, and Cesar de la Fuente-Nunez
[Digital Discovery (2022)](https://pubs.rsc.org/en/content/articlehtml/2022/dd/d1dd00024a)

**Design of protein segments and peptides for binding to protein targets**
Gupta, Suchetana, Noora Azadvari, and Parisa Hosseinzadeh
[BioDesign Research 2022 (2022)](https://spj.science.org/doi/10.34133/2022/9783197)

**Revolutionizing peptide-based drug discovery: Advances in the post-AlphaFold era**
Liwei Chang, Arup Mondal, Bhumika Singh, Yisel Martínez-Noa, Alberto Perez
[Wiley Interdisciplinary Reviews: Computational Molecular Science](https://wires.onlinelibrary.wiley.com/doi/epdf/10.1002/wcms.1693)

**Peptide-based drug discovery through artificial intelligence: towards an autonomous design of therapeutic peptides**
Montserrat Goles, Anamaría Daza, Gabriel Cabas-Mora, Lindybeth Sarmiento-Varón, Julieta Sepúlveda-Yañez, Hoda Anvari-Kazemabad, Mehdi D Davari, Roberto Uribe-Paredes, Álvaro Olivera-Nappa, Marcelo A Navarrete, David Medina-Ortiz
[Briefings in Bioinformatics 25.4 (2024)](https://academic.oup.com/bib/article/25/4/bbae275/7690345)

**Accelerating antimicrobial peptide design: Leveraging deep learning for rapid discovery**
Ahmad M. Al-Omari ,Yazan H. Akkam,Ala’a Zyout,Shayma’a Younis,Shefa M. Tawalbeh,Khaled Al-Sawalmeh,Amjed Al Fahoum ,Jonathan Arnold
[PloS one 19.12 (2024): e0315477](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0315477)

**Trends in the Research and Development of Peptide Drug Conjugates: Artificial Intelligence Aided Design**
Dong-E Zhang, Dong-E Zhang, Tong He, Tong He, Tianyi Shi, Tianyi Shi, Kun Huang, Kun Huang, Anlin Peng, Anlin Peng
[Frontiers in Pharmacology 16](https://www.frontiersin.org/journals/pharmacology/articles/10.3389/fphar.2025.1553853/full)

### 1.4 Binder design

**Improving de novo Protein Binder Design with Deep Learning**
Nathaniel Bennett, Brian Coventry, Inna Goreshnik, Buwei Huang, Aza Allen, Dionne Vafeados, Ying Po Peng, Justas Dauparas, Minkyung Baek, Lance Stewart, Frank DiMaio, Steven De Munck, Savvas Savvides, David Baker
[bioRxiv 2022.06.15.495993](https://www.biorxiv.org/content/10.1101/2022.06.15.495993v1)/[Nat Commun 14, 2625 (2023)](https://www.nature.com/articles/s41467-023-38328-5) • [code](https://github.com/nrbennet/dl_binder_design) • [news](https://phys.org/news/2023-08-deep-protein.html)

**Data and AI-driven synthetic binding protein discovery**
Yanlin Li, Zixin Duan, Zhenwen Li, Weiwei Xue
[Trends in Pharmacological Sciences (2025)](https://www.cell.com/trends/pharmacological-sciences/abstract/S0165-6147(24)00268-2)

**Code to complex: AI-driven de novo binder design**  
Daniel R. Fox, Cyntia Taveneau, Janik Clement, Rhys Grinter, Gavin J. Knott  
[Structure (2025)](https://www.cell.com/structure/fulltext/S0969-2126(25)00311-9)

### 1.5 Enzyme design

**A review of enzyme design in catalytic stability by artificial intelligence**
Yongfan Ming, Wenkang Wang, Rui Yin, Min Zeng, Li Tang, Shizhe Tang, Min Li
[Briefings in Bioinformatics, 2023](https://academic.oup.com/bib/advance-article-abstract/doi/10.1093/bib/bbad065/7086816)

**Application of "foldability" in the intelligent of enzymes engineering and design: take AlphaFold2 for example**
MENG Qiaozhen, GUO Fei
[Synthetic Biology Journal (2023)](https://synbioj.cip.com.cn/article/2023/2096-8280/2023-011.shtml)

**AlphaFold2 and Deep Learning for Elucidating Enzyme Conformational Flexibility and Its Application for Design**
Casadevall, Guillem, Cristina Duran, and Sí­lvia Osuna
[JACS Au (2023)](https://pubs.acs.org/doi/10.1021/jacsau.3c00188)

**Accelerating Biocatalysis Discovery with Machine Learning: A Paradigm Shift in Enzyme Engineering, Discovery, and Design**
Braun Markus, Gruber Christian C, Krassnigg Andreas, Kummer Arkadij, Lutz Stefan, Oberdorfer Gustav, Siirola Elina, and Snajdrova Radka
[ACS Catal. 2023](https://pubs.acs.org/doi/10.1021/acscatal.3c03417)

**Building Enzymes through Design and Evolution**
Hossack, Euan J., Florence J. Hardy, and Anthony P. Green
[ACS Catalysis 13.19 (2023)](https://pubs.acs.org/doi/10.1021/acscatal.3c02746)

**Advances in generative modeling methods and datasets to design novel enzymes for renewable chemicals and fuels**
Rana A Barghout, Zhiqing Xu, Siddharth Betala, Radhakrishnan Mahadevan
[Current Opinion in Biotechnology, Volume 84, 2023](https://www.sciencedirect.com/science/article/abs/pii/S0958166923001179)

**Opportunites and Challenges for Machine Learning-Assisted Enzyme Engineering**
Jason Yang, Francesca-Zhoufan Li, Frances H. Arnold
[ACS Central Science (2024)](https://pubs.acs.org/doi/10.1021/acscentsci.3c01275)

**Navigating the landscape of enzyme design: from molecular simulations to machine learning**
Jiahui Zhoua, Meilan Huang
[Chemical Society Reviews (2024)](https://pubs.rsc.org/en/Content/ArticleLanding/2024/CS/D4CS00196F)

**Structure Prediction and Computational Protein Design for Efficient Biocatalysts and Bioactive Proteins**
Rebecca Buller, Jiri Damborsky, Donald Hilvert, Uwe Bornscheuer
[Angewandte Chemie (International ed. in English)](https://onlinelibrary.wiley.com/doi/10.1002/anie.202421686)

## 2. Model-based design

> Invert trained models with optimize algorithms through iterations for sequence design. Inverted structure prediction models are known as **Hallucination**.

### 2.1 Structure Prediction Model-based

### 2.1.1 trRosetta-based

**Design of proteins presenting discontinuous functional sites using deep learning**
Doug Tischer, Sidney Lisanza, Jue Wang, Runze Dong,  View ORCID ProfileIvan Anishchenko, Lukas F. Milles, Sergey Ovchinnikov, David Baker
[bioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.11.29.402743v1)

**Fast differentiable DNA and protein sequence optimization for molecular design**
Linder, Johannes, and Georg Seelig
[arXiv preprint arXiv:2005.11275 (2020)](https://arxiv.org/abs/2005.11275)

**De novo protein design by deep network hallucination**
Ivan Anishchenko, Samuel J. Pellock, Tamuka M. Chidyausiku, Theresa A. Ramelot, Sergey Ovchinnikov, Jingzhou Hao, Khushboo Bafna, Christoffer Norn, Alex Kang, Asim K. Bera, Frank DiMaio, Lauren Carter, Cameron M. Chow, Gaetano T. Montelione & David Baker
[Nature (2021)](https://doi.org/10.1038/s41586-021-04184-w)  • [code](https://github.com/gjoni/trDesign) • [trRosetta](https://yanglab.nankai.edu.cn/trRosetta/download/)

**Protein sequence design by conformational landscape optimization**
Christoffer Norn, Basile I. M. Wicky, David Juergens, and Sergey Ovchinnikov
[Proceedings of the National Academy of Sciences 118.11 (2021)](https://www.pnas.org/content/118/11/e2017228118) • [code](https://github.com/gjoni/trDesign)

**De novo design of small beta barrel proteins**
David E. Kim, Davin R. Jensen, David Feldman, Doug Tischer  and Ayesha Saleem, Cameron M. Chow, Xinting Li, Lauren Carter, Lukas Milles, Hannah Nguyen, Alex Kang, Asim K. Bera, Francis C. Peterson, Brian F. Volkman, Sergey Ovchinnikov, David Baker
[PNAS(2023),e2207974120](https://www.pnas.org/doi/10.1073/pnas.2207974120) • [code](https://github.com/sokrypton/TrDesign_partialhal)

**Exploring "dark matter" protein folds using deep learning**
Zander Harteveld, Alexandra Van Hall-Beauvais, Irina Morozova, Joshua Southern, Casper Alexander Goverde, Sandrine Georgeon, Stephane Rosset, Andreas Loukas, Pierre Vandergheynst, Michael Bronstein, Bruno Correia
[bioRxiv 2023.08.30.555621](https://www.biorxiv.org/content/10.1101/2023.08.30.555621v1)/[Cell Systems](https://www.cell.com/cell-systems/fulltext/S2405-4712(24)00270-9) • [Suppplymentary](https://www.biorxiv.org/content/biorxiv/early/2023/09/01/2023.08.30.555621/DC1/embed/media-1.pdf) • [code](https://github.com/zanderharteveld/genesis)

**Carving out a Glycoside Hydrolase Active Site for Incorporation into a New Protein Scaffold Using Deep Network Hallucination**
Anders Lønstrup Hansen, Frederik Friis Theisen, Ramon Crehuet, Enrique Marcos, Nushin Aghajari, and Martin Willemoës
[ACS Synth. Biol. 2024](https://pubs.acs.org/doi/10.1021/acssynbio.3c00674)

**Implicit modeling of the conformational landscape and sequence allows scoring and generation of stable proteins**
Yehlin Cho, Justas Dauparas, Kotaro Tsuboyama, Gabriel Rocklin, Sergey Ovchinnikov
[bioRxiv 2024.12.20.629706](https://www.biorxiv.org/content/10.1101/2024.12.20.629706v1) • [code](https://github.com/yehlincho/Joint_Model_Stability) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/22/2024.12.20.629706/DC1/embed/media-1.pdf)

#### 2.1.2 AlphaFold2-based

**End-to-end learning of multiple sequence alignments with differentiable Smith-Waterman**
Petti, Samantha, Bhattacharya, Nicholas, Rao, Roshan, Dauparas, Justas, Thomas, Neil, Zhou, Juannan, Rush, Alexander M, Koo, Peter K, Ovchinnikov, Sergey
[bioRxiv (2021)](http://repository.cshl.edu/id/eprint/40409/)/[Bioinformatics, 2022;, btac724](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btac724/6820925) • [ColabDesign](https://github.com/sokrypton/ColabDesign), [SMURF](https://github.com/spetti/SMURF), [AF2 back propagation](https://github.com/sokrypton/af_backprop) • [our notes1](https://zhuanlan.zhihu.com/p/468219547), [notes2](https://zhuanlan.zhihu.com/p/472037977) • [lecture1](https://www.youtube.com/watch?v=2HmXwlKWMVs), [lecture2](https://www.youtube.com/watch?v=BJdRvODiDnk) • [Discord](https://discord.com/invite/FpYPneYB)

**AlphaDesign: A de novo protein design framework based on AlphaFold**
Jendrusch, Michael, Jan O. Korbel, and S. Kashif Sadiq
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.10.11.463937v1)/[Molecular Systems Biology (2025)](https://www.embopress.org/doi/full/10.1038/s44320-025-00119-z)

**Using AlphaFold for Rapid and Accurate Fixed Backbone Protein Design**
Moffat, Lewis, Joe G. Greener, and David T. Jones
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.08.24.457549v1)

**State-of-the-art estimation of protein model accuracy using AlphaFold**
James P. Roney, Sergey Ovchinnikov
[bioRxiv 2022.03.11.484043](https://www.biorxiv.org/content/10.1101/2022.03.11.484043v3)/[Physical Review Letters 129.23 (2022)](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.129.238101) • [code](https://github.com/jproney/AF2Rank)

**Solubility-aware protein binding peptide design using AlphaFold**
Takatsugu Kosugi, Masahito Ohue
[bioRxiv 2022.05.14.491955](https://doi.org/10.1101/2022.05.14.491955)/[Biomedicines 10.7 (2022)](https://www.mdpi.com/2227-9059/10/7/1626) • [Supplemental Materials](https://www.biorxiv.org/content/biorxiv/early/2022/05/15/2022.05.14.491955/DC1/embed/media-1.pdf) • [code](https://github.com/ohuelab/Solubility_AfDesign)

**Hallucinating protein assemblies**
Basile I M Wicky, Lukas F Milles, Alexis Courbet, Robert J Ragotte, Justas Dauparas, Elias Kinfu, Sam Tipps, Ryan D Kibler, Minkyung Baek, Frank DiMaio, Xinting Li, Lauren Carter, Alex Kang, Hannah Nguyen, Asim K Bera, David Baker
[bioRxiv 2022.06.09.493773](https://www.biorxiv.org/content/10.1101/2022.06.09.493773v1)/[Science (2022)](https://www.science.org/doi/10.1126/science.add1964) • [related slides](https://docs.google.com/presentation/d/1_tvzLKks83sYOKemfFeImCPnWtCQ-CHqmKK_3IQI1so/) • [our notes](https://zhuanlan.zhihu.com/p/527152827) • [news](https://www.nature.com/articles/d41586-022-02947-7)

**EvoBind: in silico directed evolution of peptide binders with AlphaFold**
Patrick Bryant, Arne Elofsson
[bioRxiv 2022.07.23.501214](https://www.biorxiv.org/content/10.1101/2022.07.23.501214v1) • [code](https://github.com/patrickbryant1/EvoBind)

**Hallucination of closed repeat proteins containing central pockets**
Linna An, Derrick R Hicks, Dmitri Zorine, Justas Dauparas, Basile I. M. Wicky, Lukas F Milles, Alexis Courbet, Asim K. Bera, Hannah Nguyen, Alex Kang, Lauren Carter, David Baker
[bioRxiv 2022.09.01.506251](https://www.biorxiv.org/content/10.1101/2022.09.01.506251v1)/[Nat Struct Mol Biol 30, 1755-1760 (2023)](https://www.nature.com/articles/s41594-023-01112-6) • [Supplementary data](https://static-content.springer.com/esm/art%3A10.1038%2Fs41594-023-01112-6/MediaObjects/41594_2023_1112_MOESM1_ESM.pdf)

**Predicting the structure of large protein complexes using AlphaFold and Monte Carlo tree search**
Patrick Bryant, Gabriele Pozzati, Wensi Zhu, Aditi Shenoy, Petras Kundrotas & Arne Elofsson
[Nature communications 13.1 (2022)](https://www.nature.com/articles/s41467-022-33729-4) • [gitlba](https://gitlab.com/patrickbryant1/molpc), [github](https://github.com/patrickbryant1/MoLPC) • [Supplementary data1](https://doi.org/10.5281/zenodo.6367019), [Supplementary data2](https://doi.org/10.17044/scilifelab.19375172)

**De novo protein design by inversion of the AlphaFold structure prediction network**
Casper Goverde, Benedict Wolf, Hamed Khakzad, Stephane Rosset, Bruno E Correia
[bioRxiv 2022.12.13.520346](https://www.biorxiv.org/content/10.1101/2022.12.13.520346v1) • [code](https://github.com/bene837/af_gradmcmc) • [lecture1](https://www.youtube.com/watch?v=aUMGuogMZCA) • [lecture2](https://www.youtube.com/watch?v=4S4J7gbhAa0)

**Code of OpenComplex**
Jingcheng, Yu and Zhaoming, Chen and Zhaoqun, Li and Mingliang, Zeng and Wenjun, Lin and He, Huang and Qiwei, Ye
[code](https://github.com/baaihealth/OpenComplex)

**Efficient and scalable de novo protein design using a relaxed sequence space**
Christopher Josef Frank, Ali Khoshouei, Yosta de Stigter, Dominik Schiewitz, Shihao Feng, Sergey Ovchinnikov, Hendrik Dietz
[bioRxiv 2023.02.24.529906](https://www.biorxiv.org/content/10.1101/2023.02.24.529906v1) • [code](https://github.com/sokrypton/ColabDesign/blob/main/af/examples/af_relax_design.ipynb)

**Cyclic peptide structure prediction and design using AlphaFold**
Stephen A. Rettie, Katelyn V. Campbell, Asim K. Bera, Alex Kang, Simon Kozlov, Joshmyn De La Cruz, Victor Adebomi, Guangfeng Zhou, Frank DiMaio, Sergey Ovchinnikov, Gaurav Bhardwaj
[bioRxiv](https://www.biorxiv.org/content/10.1101/2023.02.25.529956v1)/[Nat Commun 16, 4730 (2025)](https://www.nature.com/articles/s41467-025-59940-7) • [Code](https://github.com/sokrypton/ColabDesign/blob/main/af/examples/af_cyc_design.ipynb) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/02/26/2023.02.25.529956/DC1/embed/media-1.xlsx)

**De novo design of luciferases using deep learning**
Andy Hsien-Wei Yeh, Christoffer Norn, Yakov Kipnis, Doug Tischer, Samuel J. Pellock, Declan Evans, Pengchen Ma, Gyu Rie Lee, Jason Z. Zhang, Ivan Anishchenko, Brian Coventry, Longxing Cao, Justas Dauparas, Samer Halabiya, Michelle DeWitt, Lauren Carter, K. N. Houk & David Baker
[Nature](https://www.nature.com/articles/s41586-023-05696-3) • [Code](https://files.ipd.uw.edu/pub/luxSit/scaffold_generation.tar.gz) • [Supplementary Materials](https://static-content.springer.com/esm/art%3A10.1038%2Fs41586-023-05696-3/MediaObjects/41586_2023_5696_MOESM1_ESM.pdf)

**In silico evolution of protein binders with deep learning models for structure prediction and sequence design**
Odessa J Goudy, Amrita Nallathambi, Tomoaki Kinjo, Nicholas Randolph, Brian Kuhlman
[bioRxiv 2023.05.03.539278](https://www.biorxiv.org/content/10.1101/2023.05.03.539278v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/05/03/2023.05.03.539278/DC1/embed/media-1.pdf) • [code](https://github.com/KuhlmanLab/evopro)

**Computational design of soluble analogues of integral membrane protein structures**
Casper Alexander Goverde, Martin Pacesa, Lars Jeremy Dornfeld, Sandrine Georgeon, Stephane Rosset, Justas Dauparas, Christian Shellhaas, Simon Kozlov, David Baker, Sergey Ovchinnikov, Bruno Correia
[bioRxiv 2023.05.09.540044](https://www.biorxiv.org/content/10.1101/2023.05.09.540044v2)/[Nature (2024)](https://www.nature.com/articles/s41586-024-07601-y) • [code](https://github.com/bene837/af2seq) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/05/09/2023.05.09.540044/DC1/embed/media-1.pdf)

**Antibody Complementarity-Determining Region Sequence Design using AlphaFold2 and Binding Affinity Prediction Model**
Takafumi Ueki, Masahito Ohue
[bioRxiv 2023.06.02.543382](https://www.biorxiv.org/content/10.1101/2023.06.02.543382v1)

**Context-Dependent Design of Induced-fit Enzymes using Deep Learning Generates Well Expressed, Thermally Stable and Active Enzymes**
Lior Zimmerman, Noga Alon, Itay Levin, Anna Koganitsky, Nufar Shpigel, Chen Brestel, Gideon David Lapidoth
[bioRxiv 2023.07.27.550799](https://www.biorxiv.org/content/10.1101/2023.07.27.550799v2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/07/31/2023.07.27.550799/DC1/embed/media-1.xlsx)

**Highly accurate and robust protein sequence design with CarbonDesign**/**Accurate and robust protein sequence design with CarbonDesign**
Milong Ren, Chungong Yu, Dongbo Bu, Haicang Zhang
[bioRxiv 2023.08.07.552204](https://www.biorxiv.org/content/10.1101/2023.08.07.552204v1)/[Nat Mach Intell 6, 536–547 (2024)](https://www.nature.com/articles/s42256-024-00838-2) • [code](https://github.com/zhanghaicang/carbonmatrix_public)

**Design of Cyclic Peptides Targeting Protein-Protein Interactions using AlphaFold**
Takatsugu Kosugi, Masahito Ohue
[bioRxiv 2023.08.20.554056](https://www.biorxiv.org/content/10.1101/2023.08.20.554056v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/08/21/2023.08.20.554056/DC1/embed/media-1.pdf) • [code](https://github.com/YoshitakaMo/localcolabfold/)

**MetaPPI: In Silico Screen for Novel CRBN-based Substrates**
neoxbio
[website](https://www.neoxbio.com/platform-technology.html) • [news](https://mp.weixin.qq.com/s/Kb4EQ0YvYDvoLZ_cnAlUPw) • masif-based • commercial

**AlphaFold Distillation for Protein Design**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=3pgJNIx3gc) • [code](https://anonymous.4open.science/r/AFDistill-28C3)

**High-throughput computational discovery of inhibitory protein fragments with AlphaFold**
Andrew Savinov, Sebastian Swanson, Amy E. Keating, Gene-Wei Li
[bioRxiv 2023.12.19.572389](https://www.biorxiv.org/content/10.1101/2023.12.19.572389v1) • [code](https://github.com/swanss/FragFold)

**An integrative approach to protein sequence design through multiobjective optimization**
Lu Hong, Tanja Kortemme
[bioRxiv 2024.03.01.582670](https://www.biorxiv.org/content/10.1101/2024.03.01.582670v1)/[PLOS Computational Biology 20(7)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1011953) • [code](https://github.com/luhong88/int_seq_des) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/03/04/2024.03.01.582670/DC1/embed/media-1.pdf)

**Protein Design Using Structure-Prediction Networks: AlphaFold and RoseTTAFold as Protein Structure Foundation Models**
Jue Wang, Joseph L. Watson and Sidney L. Lisanza
[Cold Spring Harbor Perspectives in Biology(2024)](https://cshperspectives.cshlp.org/content/early/2024/03/01/cshperspect.a041472.short)

**Context-dependent design of induced-fit enzymes using deep learning generates well-expressed, thermally stable and active enzymes**
Lior Zimmerman, Noga Alon, Itay Levin, and Gideon D. Lapidoth
[Proceedings of the National Academy of Sciences 121.11(2024)](https://www.pnas.org/doi/10.1073/pnas.2313809121)

**Design of Repeat Alpha-Beta Proteins with Capping Helices**
Dmitri Zorine, David Baker
[bioRxiv 2024.06.15.590358](https://www.biorxiv.org/content/10.1101/2024.06.15.590358v1) • [code](https://github.com/dmitropher/af2_multistate_hallucination)

**Design of linear and cyclic peptide binders of different lengths only from a protein target sequence**
Qiuzhen Li, Efstathios Nikolaos Vlachos, Patrick Bryant
[bioRxiv 2024.06.20.599739](https://www.biorxiv.org/content/10.1101/2024.06.20.599739v1) • [code](https://zenodo.org/records/11543503) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/06/22/2024.06.20.599739/DC1/embed/media-1.pdf)

**BindCraft: one-shot design of functional protein binders**
Martin Pacesa, Lennart Nickel, Joseph Schmidt, Ekaterina Pyatova, Christian Schellhaas, Lucas Kissling, Ana Alcaraz-Serna, Yehlin Cho, Kourosh H. Ghamary, Laura Vinue, Brahm J. Yachnin, Andrew M. Wollacott, Stephen Buckley, Sandrine Georgeon, Casper A. Goverde, Georgios N. Hatzopoulos, Pierre Gonczy, Yannick D. Muller, Gerald Schwank, Sergey Ovchinnikov, Bruno E. Correia
[bioRxiv 2024.09.30.615802](https://www.biorxiv.org/content/10.1101/2024.09.30.615802v1)/[Nature (2025)](https://www.nature.com/articles/s41586-025-09429-6) • [code](https://github.com/martinpacesa/BindCraft)

**Design of linear and cyclic peptide binders of different lengths from protein sequence information**
Qiuzhen Li, Efstathios Nikolaos Vlachos, Patrick Bryant
[bioRxiv 2024.06.20.599739](https://www.biorxiv.org/content/10.1101/2024.06.20.599739v2) • [code](https://zenodo.org/records/13913345)

**Scalable protein design using optimization in a relaxed sequence space**
Christopher Frank, Ali Khoshouei , Lara Fub , Dominik Schiwietz , Dominik Putz, Lara Weber, Zhixuan Zhao, Motoyuki Hattori, Shihao Feng, Yosta de Stigter, Sergey Ovchinnikov, Hendrik Dietz
[Science386,439-445(2024)](https://www.science.org/doi/10.1126/science.adq1741) • [code](https://github.com/sokrypton/ColabDesign)

**Alphafold2 refinement improves designability of large de novo proteins**
Christopher Josef Frank, Dominik Schiwietz, Lara Fuss, Sergey Ovchinnikov, Hendrik Dietz
[bioRxiv 2024.11.21.624687](https://www.biorxiv.org/content/10.1101/2024.11.21.624687v1) • [colab](https://colab.research.google.com/drive/14ULdrjOmH-XMtGDrikzjDF1FLegZg3-a?usp=sharing)

**Low-N OpenFold fine-tuning improves peptide design without additional structures**
Theodore Sternlieb, Jakub Otwinowski, Sam Sinai, Jeffrey Chan
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/Low-N_OpenFold_fine-tuning_improves_peptide_design_without_additional_structures.pdf)

**HighPlay: Cyclic Peptide Sequence Design Based on Reinforcement Learning and Protein Structure Prediction**
Huitian Lin, Cheng Zhu, Tianfeng Shang, Ning Zhu, Kang Lin, Xiang Shao, Xudong Wang, Hongliang Duan
[bioRxiv 2025.03.17.643626](http://biorxiv.org/content/10.1101/2025.03.17.643626v1)

**Designing Novel Solenoid Proteins with In Silico Evolution**
Daniella Pretorius, Georgi Ivanov Nikov, Kono Washio, Steve-William Florent, Henry Taunt, Sergey Ovchinnikov, James William Murray
[bioRxiv 2025.04.23.646631](https://www.biorxiv.org/content/10.1101/2025.04.23.646631v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/04/24/2025.04.23.646631/DC1/embed/media-1.pdf)

**Single-Shot Design of a Cyclic Peptide Inhibitor of HIV-1 Membrane Fusion with EvoBind**  
Diandra Daumiller, Federica Giammarino, Qiuzhen Li, Anders Sönnerborg, Rafael Ceña Diez, Patrick Bryant  
[bioRxiv 2025.04.30.651413](https://www.biorxiv.org/content/10.1101/2025.04.30.651413v1)

**BindEnergyCraft: Casting Protein Structure Predictors as Energy-Based Models for Binder Design**  
Divya Nori, Anisha Parsan, Caroline Uhler, Wengong Jin  
[arXiv:2505.21241](https://arxiv.org/abs/2505.21241)

**Blind De Novo Design of Dual Cyclic Peptide Agonists Targeting GCGR and GLP1R**  
Qiuzhen Li, Elisee Wiita, Thomas Helleday, Patrick Bryant  
[bioRxiv 2025.06.06.658268](https://www.biorxiv.org/content/10.1101/2025.06.06.658268v1) • [code](https://zenodo.org/records/13933365)

**AlphaFold distillation for inverse protein design**  
Igor Melnyk, Aurélie Lozano, Payel Das & Vijil Chenthamarakshan  
[Sci Rep 15, 21743 (2025)](https://www.nature.com/articles/s41598-025-00436-1) • [code](https://github.com/IBM/AFDistill)

**Fold-Conditioned De Novo Binder Design via AlphaFold2-Multimer Hallucination**  
Khondamir. R. Rustamov, Artyom Y. Baev  
[bioRxiv 2025.07.02.662497](https://www.biorxiv.org/content/10.1101/2025.07.02.662497v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/07/05/2025.07.02.662497/DC1/embed/media-1.docx) • [code](https://github.com/KhondamirRustamov/FoldCraft)

**Design of linear and cyclic peptide binders from protein sequence  information**  
Qiuzhen Li, Efstathios Nikolaos Vlachos & Patrick Bryant  
[Commun Chem 8, 211 (2025)](https://www.nature.com/articles/s42004-025-01601-3)

**Generative Design of High-Affinity Peptides Using BindCraft**  
Mike Filius, Thanasis Patsos, Hugo Minee, Gianluca Turco, Jingming Liu, Monika Gnatzy, Ramon S.M. Rooth, Andy C. H. Liu, Rosa D.T. Ta, Isa H. A. Rijk, Safiya Ziani, Femke J. Boxman, Sebastian J. Pomplun  
[bioRxiv 2025.07.23.666285](https://www.biorxiv.org/content/10.1101/2025.07.23.666285v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/07/25/2025.07.23.666285/DC1/embed/media-1.pdf)

**Computational Design of Soluble CCR8 Analogues with Preserved Antibody Binding**  
Trang Nguyen, Songming Liu, Yifan Li, Longfei Cong, Roger Shek, Tek Hyang Lee, Li Yi, Per Greisen  
[bioRxiv 2025.08.18.670068](https://www.biorxiv.org/content/10.1101/2025.08.18.670068v1)

**De novo design of a peptide modulator to reverse sodium channel dysfunction linked to cardiac arrhythmias and epilepsy**  
Ryan Mahling, Bence Hegyi, Erin R. Cullen, Timothy M. Cho, Aaron R. Rodriques, Lucile Fossier, Marc Yehya, Lin Yang, Bi-Xing Chen, Alexander N. Katchman, Nourdine Chakouri, Ruiping Ji, Elaine Y. Wan, Jared Kushner, Steven O. Marx, Sergey Ovchinnikov, Christopher D. Makinson, Donald M. Bers, Manu Ben-Johny  
[Cell (2025)](https://www.cell.com/cell/fulltext/S0092-8674(25)00860-8)

#### 2.1.3 DMPfold2-based

**Design in the DARK: Learning Deep Generative Models for De Novo Protein Design**
Moffat, Lewis, Shaun M. Kandathil, and David T. Jones
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.01.27.478087v1) • [DMPfold2](https://github.com/psipred/DMPfold2)

#### 2.1.4 DeepAb-based

**Towards deep learning models for target-specific antibody design**
Sai Pooja Mahajan, Jeffrey Ruffolo, Rahel Frick, Jeffrey J. Gray
[Biophysical Journal 121.3 (2022)](https://www.cell.com/biophysj/pdf/S0006-3495(21)03758-9.pdf) • [DeepAb](https://github.com/RosettaCommons/DeepAb) • [lecture](https://www.youtube.com/watch?v=LIo-1jPfrns)

**Hallucinating structure-conditioned antibody libraries for target-specific binders**
Sai Pooja Mahajan, Jeffrey A Ruffolo, Rahel Frick, Jeffrey J. Gray
[bioRxiv 2022.06.06.494991](https://www.biorxiv.org/content/10.1101/2022.06.06.494991v1)/[Front. Immunol. 13:999034](https://www.frontiersin.org/articles/10.3389/fimmu.2022.999034/full) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/06/06/2022.06.06.494991/DC1/embed/media-1.pdf) • [code](https://github.com/RosettaCommons/FvHallucinator)

#### 2.1.5 TRFold2-based

[News of TRDesign](https://mp.weixin.qq.com/s/OQzKawtL9RdK9HzYsfu80g)
[TIANRANG XLab](https://xlab.tianrang.com/)
paper unavailable • [slides](https://pan.baidu.com/share/init?surl=4AOW_D9dwlvC7VGGZA2tmQ&pwd=ffui) • [website](https://xcreator.tianrang.com/auth/login) • commercial • [news](https://mp.weixin.qq.com/s/45Gz7GWOGxHl0i6LXxTUpw)

#### 2.1.6 Boltz-based

**Boltzdesign1: Inverting All-Atom Structure Prediction Model for Generalized Biomolecular Binder Design**
Yehlin Cho, Martin Pacesa, Zhidian Zhang, Bruno E. Correia, Sergey Ovchinnikov
[bioRxiv 2025.04.06.647261](https://www.biorxiv.org/content/10.1101/2025.04.06.647261v1) • [code](https://github.com/yehlincho/BoltzDesign1)

#### 2.1.7 RareFold-based

**RareFold: Structure prediction and design of proteins with noncanonical amino acids**  
Qiuzhen Li, Diandra Daumiller, Patrick Bryant  
[bioRxiv 2025.05.19.654846](https://www.biorxiv.org/content/10.1101/2025.05.19.654846v1) • [code](https://github.com/patrickbryant1/RareFold)

#### 2.1.8 HelixFold-based

**HelixDesign-Binder: A Scalable Production-Grade Platform for Binder Design Built on HelixFold3**  
Jie Gao, Jun Li, Jing Hu, Shanzhuo Zhang, Kunrui Zhu, Yueyang Huang, Xiaonan Zhang, Xiaomin Fang  
[arXiv:2505.21873](https://arxiv.org/abs/2505.21873) • ESM-IF-based

**HelixDesign-Antibody: A Scalable Production-Grade Platform for Antibody Design Built on HelixFold3**  
Jie Gao, Jing Hu, Shanzhuo Zhang, Kunrui Zhu, Sheng Qian, Yueyang Huang, Xiaonan Zhang, Xiaomin Fang  
[arXiv:2507.02345](https://arxiv.org/abs/2507.02345) • [website](https://paddlehelix.baidu.com/)

### 2.2 CM-Align

**AutoFoldFinder: An Automated Adaptive Optimization Toolkit for De Novo Protein Fold Design**
Shuhao Zhang, Youjun Xu, Jianfeng Pei, Luhua Lai
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_AutoFoldFinder.pdf)

### 2.3 MSA-transformer-based

**Protein language models trained on multiple sequence alignments learn phylogenetic relationships**
Damiano Sgarbossa, Umberto Lupo, Anne-Florence Bitbol
[arXiv preprint arXiv:2203.15465 (2022)](https://arxiv.org/abs/2203.15465)/[bioRxiv 2022.04.14.488405](https://www.biorxiv.org/content/10.1101/2022.04.14.488405v1)

**EvoOpt: an MSA-guided, fully unsupervised sequence optimization pipeline for protein design**
Hideki Yamaguchi, Yutaka Saito
[NeurIPS 2022](https://www.mlsb.io/papers_2022/EvoOpt_an_MSA_guided_fully_unsupervised_sequence_optimization_pipeline_for_protein_design.pdf)

**Generative power of a protein language model trained on multiple sequence alignments**
Sgarbossa, Damiano, Umberto Lupo, and Anne-Florence Bitbol
[Elife 12 (2023): e79854](https://elifesciences.org/articles/79854) • [code](https://github.com/Bitbol-Lab/Iterative_masking)

### 2.4 LLM-based

#### 2.4.1 GPT-based

**Multi-segment preserving sampling for deep manifold sampler**
Daniel Berenberg, Jae Hyeon Lee, Simon Kelow, Ji Won Park, Andrew Watkins, Vladimir Gligorijević, Richard Bonneau, Stephen Ra, Kyunghyun Cho
[arXiv preprint arXiv:2205.04259 (2022)](https://arxiv.org/abs/2205.04259)

**Preference optimization of protein language models as a multi-objective binder design paradigm**
Pouria Mistani, Venkatesh Mysore
[arXiv:2403.04187](https://arxiv.org/abs/2403.04187)

**HMAMP: Hypervolume-Driven Multi-Objective Antimicrobial Peptides Design**
Li Wang, Yiping Li, Xiangzheng Fu, Xiucai Ye, Junfeng Shi, Gary G. Yen, Xiangxiang Zeng
[arXiv:2405.00753](https://arxiv.org/abs/2405.00753)

#### 2.4.2 ESM-based

**Generating novel protein sequences using Gibbs sampling of masked language models**
Sean R. Johnson, Sarah Monaco, Kenneth Massie, Zaid Syed
[bioRxiv 2021.01.26.428322](https://www.biorxiv.org/content/10.1101/2021.01.26.428322v1) • [code](https://github.com/seanrjohnson/protein_gibbs_sampler)

**A high-level programming language for generative protein design**
Brian Hie, Salvatore Candido, Zeming Lin, Ori Kabeli, Roshan Rao, Nikita Smetanin, Tom Sercu, Alexander Rives
[bioRxiv 2022.12.21.521526](https://www.biorxiv.org/content/10.1101/2022.12.21.521526v1)

**Language models generalize beyond natural proteins**
Robert Verkuil, Ori Kabeli, Yilun Du, Basile IM Wicky, Lukas F Milles, Justas Dauparas, David Baker, Sergey Ovchinnikov, Tom Sercu, Alexander Rives
[bioRxiv 2022.12.21.521521](https://www.biorxiv.org/content/10.1101/2022.12.21.521521v1)

**ESMFold Hallucinates Native-Like Protein Sequences**
Jeliazko R Jeliazkov, Diego del Alamo, Joel D Karpiak
[bioRxiv 2023.05.23.541774](https://www.biorxiv.org/content/10.1101/2023.05.23.541774v1)

**Protein Language Model Supervised Precise and Efficient Protein Backbone Design Method**
Bo Zhang, Kexin Liu, Zhuoqi Zheng, Yunfeiyang Liu, Junxi Mu, Ting Wei, Hai-Feng Chen
[bioRxiv 2023.10.26.564121](https://www.biorxiv.org/content/10.1101/2023.10.26.564121v1)/[preprint](https://www.researchsquare.com/article/rs-5450034/v1) • [code](https://github.com/sirius777coder/GPDL) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/10/30/2023.10.26.564121/DC1/embed/media-1.pdf)

**Unexplored regions of the protein sequence-structure map revealed at scale by a library of foldtuned language models**
Arjuna M. Subramanian, Matt Thomson
[bioRxiv 2023.12.22.573145](https://www.biorxiv.org/content/10.1101/2023.12.22.573145v1)

**Computational scoring and experimental evaluation of enzymes generated by neural networks**
Sean R. Johnson, Xiaozhi Fu, Sandra Viknander, Clara Goldin, Sarah Monaco, Aleksej Zelezniak & Kevin K. Yang
[Nature Biotechnology (2024)](https://www.nature.com/articles/s41587-024-02214-2) • [code](https://github.com/seanrjohnson/protein_scoring)

**Exploring Latent Space for Generating Peptide Analogs Using Protein Language Models**
Po-Yu Liang, Xueting Huang, Tibo Duran, Andrew J. Wiemer, Jun Bai
[arXiv:2408.08341](https://arxiv.org/abs/2408.08341) • [code](https://github.com/LabJunBMI/Latent-Space-Peptide-Analogues-Generation)

**Designing diverse and high-performance proteins with a large language model in the loop**
Carlos A. Gomez-Uribe, Japheth Gado, Meiirbek Islamov
[bioRxiv 2024.10.25.620340](https://www.biorxiv.org/content/10.1101/2024.10.25.620340v1)

**Key-cutting machine: A novel optimization framework for tailored protein and peptide design**
Yan C. Leyva, Marcelo D. T. Torres, Carlos A. Oliva, Cesar de la Fuente-Nunez, Carlos A. Brizuela
[bioRxiv 2025.01.05.631393](https://www.biorxiv.org/content/10.1101/2025.01.05.631393v1) • [code](https://github.com/cbrizuel/KCM)

**Improving functional protein generation via foundation model-derived latent space likelihood optimization**
Changge Guan, Fangping Wan, Marcelo D. T. Torres, Cesar de la Fuente-Nunez
[bioRxiv 2025.01.07.631724](https://www.biorxiv.org/content/10.1101/2025.01.07.631724v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/01/08/2025.01.07.631724/DC1/embed/media-1.docx)

**DPAC: Prediction and Design of Protein-DNA Interactions via Sequence-Based Contrastive Learning**  
Leo Tianlai Chen, Rishab Pulugurta, Pranay Vure, Pranam Chatterjee  
[bioRxiv 2025.05.14.654102](https://www.biorxiv.org/content/10.1101/2025.05.14.654102v1) • [code](https://github.com/programmablebio/dpac)

**BAGEL: Protein Engineering via Exploration of an Energy Landscape**  
Jakub Lála, Ayham Al-Saffar, Stefano Angiolleti-Uberti  
[bioRxiv 2025.07.05.663138](https://www.biorxiv.org/content/10.1101/2025.07.05.663138v1) • [code](https://github.com/softnanolab/bagel)

#### 2.4.3 Antiberta-based

**DyAb: sequence-based antibody design and property prediction in a low-data regime**
Joshua Yao-Yu Lin, Jennifer L. Hofmann, Andrew Leaver-Fay, Wei-Ching Liang, Stefania Vasilaki, Edith Lee, Pedro O. Pinheiro, Natasa Tagasovska, James R. Kiefer, Yan Wu, Franziska Seeger, Richard Bonneau, Vladimir Gligorijevic, Andrew Watkins, Kyunghyun Cho, Nathan C. Frey
[bioRxiv 2025.01.28.635353](https://www.biorxiv.org/content/10.1101/2025.01.28.635353v1) • [code](github.com/prescient-design/lobster) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/02/02/2025.01.28.635353/DC1/embed/media-1.pdf)

### 2.5 Sampling-algorithms

**AdaLead: A simple and robust adaptive greedy search algorithm for sequence design**
Sam Sinai, Richard Wang, Alexander Whatley, Stewart Slocum, Elina Locane, Eric D. Kelsic
[arXiv preprint arXiv:2010.02141 (2020)](https://arxiv.org/abs/2010.02141) • [code](https://github.com/samsinai/FLEXS)

**Autofocused oracles for model-based design**
Fannjiang, Clara, and Jennifer Listgarten
[Advances in Neural Information Processing Systems 33 (2020)](https://proceedings.neurips.cc/paper/2020/file/972cda1e62b72640cb7ac702714a115f-Paper.pdf)

**An Efficient MCMC Approach to Energy Function Optimization in Protein Structure Prediction**
Lakshmi A. Ghantasala, Risi Jaiswal, Supriyo Datta
[arXiv:2211.03193](https://arxiv.org/abs/2211.03193)

**Plug & Play Directed Evolution of Proteins with Gradient-based Discrete MCMC**
Patrick Emami, Aidan Perreault, Jeffrey Law, David Biagioni, Peter St. Joh
[NeurIPS 2022](https://www.mlsb.io/papers_2022/Plug_Play_Directed_Evolution_of_Proteins_with_Gradient_based_Discrete_MCMC.pdf)/[arXiv:2212.09925](https://arxiv.org/abs/2212.09925)

**Importance Weighted Expectation-Maximization for Protein Sequence Design**
Zhenqiao Song, Lei Li
[arXiv:2305.00386](https://arxiv.org/abs/2305.00386) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/05/09/2023.05.09.539914/DC1/embed/media-1.pdf)

**Simultaneous enhancement of multiple functional properties using evolution-informed protein design**
Benjamin Fram, Ian Truebridge, Yang Su, Adam J. Riesselman, John B. Ingraham, Alessandro Passera, Eve Napier, Nicole N. Thadani, Samuel Lim, Kristen Roberts, Gurleen Kaur, Michael Stiffler, Debora S. Marks, Christopher D. Bahl, Amir R. Khan, Chris Sander, Nicholas P. Gauthier
[bioRxiv (2023): 2023-05](https://www.biorxiv.org/content/10.1101/2023.05.09.539914v1)

**Optimizing protein fitness using Gibbs sampling with Graph-based Smoothing**
Andrew Kirjner, Jason Yim, Raman Samusevich, Tommi Jaakkola, Regina Barzilay, Ila Fiete
[arXiv:2307.00494](https://arxiv.org/abs/2307.00494) • [code](https://github.com/kirjner/GGS)

**Sampling Protein Language Models for Functional Protein Design**  
Jeremie Theddy Darmawan, Yarin Gal, Pascal Notin  
[ICLR 2025 Workshop LMRL](https://openreview.net/forum?id=eRALDwvk9O)

**Reliable algorithm selection for machine learning-guided design**
Clara Fannjiang, Ji Won Park
[arXiv:2503.20767](https://arxiv.org/abs/2503.20767)

**Why risk matters for protein binder design**
Tudor-Stefan Cotet, Igor Krawczuk
[arXiv:2504.00146](https://arxiv.org/abs/2504.00146)

**Guide your favorite protein sequence generative model**  
Junhao Xiong, Hunter Nisonoff, Ishan Gaur, Jennifer Listgarten  
[arXiv:2505.04823](https://arxiv.org/abs/2505.04823)

**Computational nanobody design using graph neural networks and Metropolis Monte Carlo sampling**  
Lei Wang, Xiaoming He, Gaoxing Guo, Xinzhou Qian, Qiang Huang  
[bioRxiv 2025.06.08.658414](https://www.biorxiv.org/content/10.1101/2025.06.08.658414v1) • [code](https://github.com/Fudan-HQLab/AiPPA)

## 3. Function to Scaffold

> These models design backbone/scaffold/template in Cartesian coordinates, contact maps, distance maps and φ & ψ angles. Including conditional/unconditional generative models.

### 3.1 GAN-based

**Generative modeling for protein structures**
Anand, Namrata, and Possu Huang
[NeurIPS 2018](https://proceedings.neurips.cc/paper/2018/file/afa299a4d1d8c52e75dd8a24c3ce534f-Paper.pdf)

**Fully differentiable full-atom protein backbone generation**
Anand Namrata, Raphael Eguchi, and Po-Ssu Huang
[OpenReview ICLR 2019 workshop DeepGenStruct](https://openreview.net/forum?id=SJxnVL8YOV) • without code

**RamaNet: Computational de novo helical protein backbone design using a long short-term memory generative neural network**
Sabban, Sari, and Mikhail Markovsky
[F1000Research 9 (2020)](http://f1000researchdata.s3.amazonaws.com/manuscripts/29106/f45e92eb-5d68-4da0-b918-91ded85d2e7d_22907_-_sari_sabban_v2.pdf) • [code](https://sarisabban.github.io/RamaNet/) • pyRosetta • tensorflow • maximizaing the fluorescence of a protein

**A Generative Model for Creating Path Delineated Helical Proteins**
Nicholas B. Woodall, Ryan Kibler, Basile Wicky, Brian Coventry
[bioRxiv 2023.05.24.542095](https://www.biorxiv.org/content/10.1101/2023.05.24.542095v1) • [code](https://github.com/NickWoodall/HelixGen)

### 3.2 AutoEncoder-based

**Conditioning by adaptive sampling for robust design**
Brookes, David, Hahnbeom Park, and Jennifer Listgarten
[International conference on machine learning. PMLR, 2019](http://proceedings.mlr.press/v97/brookes19a/brookes19a.pdf)  • without code

**IG-VAE: generative modeling of immunoglobulin proteins by direct 3D coordinate generation**
Raphael R. Eguchi, Christian A. Choe, Po-Ssu Huang
[Biorxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.08.07.242347v2) • without code

**Generating tertiary protein structures via an interpretative variational autoencoder**
Xiaojie Guo, Yuanqi Du, Sivani Tadepalli, Liang Zhao, Amarda Shehu
[arXiv preprint arXiv:2004.07119 (2020)](https://arxiv.org/abs/2004.07119) • code not available

**Function-guided protein design by deep manifold sampling**
Vladimir Gligorijevic, Stephen Ra, Daniel Berenberg, Richard Bonneau, Kyunghyun Cho
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Function-guided_protein_design_by.pdf) • without code

**Deep sharpening of topological features for de novo protein design**
Zander Harteveld, Joshua Southern, Michaël Defferrard, Andreas Loukas, Pierre Vandergheynst, Micheal Bronstein, Bruno Correia
[ICLR2022 Machine Learning for Drug Discovery. 2022](https://openreview.net/forum?id=DwN81YIXGQP) • code not available

**End-to-End deep structure generative model for protein design**
Boqiao Lai, matthew McPartlon, Jinbo Xu
[bioRxiv 2022.07.09.499440](https://www.biorxiv.org/content/10.1101/2022.07.09.499440v1)

**Deep Generative Design of Epitope-Specific Binding Proteins by Latent Conformation Optimization**
Raphael R Eguchi, Christian A Choe, Udit Parekh, Irene S Khalek, Michael D Ward, Neha Vithani, Gregory R Bowman, Joseph G Jardine, Possu Huang
[bioRxiv 2022.12.22.521698](https://www.biorxiv.org/content/10.1101/2022.12.22.521698v1)

**Leveraging Deep Generative Model For Computational Protein Design And Optimization**
Boqiao Lai
[arXiv:2408.17241](https://arxiv.org/abs/2408.17241) • PhD thesis

**CyclicCAE: A Conformational Autoencoder for Efficient Heterochiral Macrocyclic Backbone Sampling**
Andrew C. Powers, P. Douglas Renfrew, Parisa Hosseinzadeh, Vikram Khipple Mulligan
[bioRxiv 2025.02.21.639569](https://www.biorxiv.org/content/10.1101/2025.02.21.639569v1)

### 3.3 MLP-based

**A backbone-centred energy function of neural networks for protein design**
Bin Huang, Yang Xu, Xiuhong Hu, Yongrui Liu, Shanhui Liao, Jiahai Zhang, Chengdong Huang, Jingjun Hong, Quan Chen & Haiyan Liu
[Nature (2022)](https://doi.org/10.1038/s41586-021-04383-5) • [code](https://zenodo.org/record/4533424#.YwP3UPFBwqs)

**De novo Design of Cavity-Containing Proteins with a Backbone-Centered Neural Network Energy Function**
Yang Xu, Xiuhong Hu, Chenchen Wang, Yongrui Liu, Quan Chen
Haiyan Liu
[Structure (2024)](https://www.cell.com/structure/fulltext/S0969-2126(24)00007-8)

### 3.4 Diffusion-based

**Diffusion probabilistic modeling of protein backbones in 3D for the motif-scaffolding problem**
Brian L. Trippe, Jason Yim, Doug Tischer, Tamara Broderick, David Baker, Regina Barzilay, Tommi Jaakkola
[arXiv:2206.04119](https://arxiv.org/abs/2206.04119v2)/[NeurIPS 2022](https://www.mlsb.io/papers_2022/Diffusion_probabilistic_modeling_of_protein_backbones_in_3D_for_the_motif_scaffolding_problem.pdf)/[ICLR 2023](https://openreview.net/forum?id=6TxBxqNME1Y) • [poster](https://nips.cc/media/PosterPDFs/NeurIPS%202022/d3d9446802a44259755d38e6d163e820.png?t=1667835607.0141048) • [Supplementary](https://openreview.net/attachment?id=6TxBxqNME1Y&name=supplementary_material) • [code](https://github.com/blt2114/ProtDiff_SMCDiff)

**ProteinSGM: Score-based generative modeling for de novo protein design**
Jin Sub Lee, Philip M Kim
[bioRxiv 2022.07.13.499967](https://www.biorxiv.org/content/10.1101/2022.07.13.499967v2)/[Nat Comput Sci (2023)](https://www.nature.com/articles/s43588-023-00440-3) • [code](https://gitlab.com/mjslee0921/proteinsgm)

**Protein structure generation via folding diffusion**
Kevin E. Wu, Kevin K. Yang, Rianne van den Berg, James Y. Zou, Alex X. Lu, Ava P. Amini
[arXiv:2209.15611](https://arxiv.org/abs/2209.15611v2)/[Nat Commun 15, 1059 (2024)](https://www.nature.com/articles/s41467-024-45051-2) • [code](https://github.com/microsoft/foldingdiff)

**Generating Novel, Designable, and Diverse Protein Structures by Equivariantly Diffusing Oriented Residue Clouds**
Yeqing Lin, Mohammed AlQuraishi
[arXiv:2301.12485v3](https://arxiv.org/abs/2301.12485v3) • [code](https://github.com/aqlaboratory/genie) • [news](https://www.dw.com/en/generative-ai-inventing-proteins-is-changing-medicine/a-66356415)

**SE(3) diffusion model with application to protein backbone generation**
Jason Yim, Brian L. Trippe, Valentin De Bortoli, Emile Mathieu, Arnaud Doucet, Regina Barzilay, Tommi Jaakkola
[arXiv:2302.02277](https://arxiv.org/abs/2302.02277v2)/[ICLR 2023](https://openreview.net/forum?id=6TxBxqNME1Y) • [code](https://github.com/jasonkyuyim/se3_diffusion) • [Supplementary](https://openreview.net/attachment?id=6TxBxqNME1Y&name=supplementary_material)

**A Latent Diffusion Model for Protein Structure Generation**
Cong Fu, Keqiang Yan, Limei Wang, Wing Yee Au, Michael McThrow, Tao Komikado, Koji Maruhashi, Kanji Uchino, Xiaoning Qian, Shuiwang Ji
[arXiv:2305.04120](https://arxiv.org/abs/2305.04120)

**Practical and Asymptotically Exact Conditional Sampling in Diffusion Models**
Luhuan Wu, Brian L. Trippe, Christian A. Naesseth, David M. Blei, John P. Cunningham
[arXiv:2306.17775](https://arxiv.org/abs/2306.17775) • [code](https://github.com/blt2114/twisted_diffusion_sampler)

**Dynamics-Informed Protein Design with Structure Conditioning**
Simon V. Mathis, Urszula Julia Komorowska, Mateja Jamnik, Pietro Lió
[WCBICML2023](https://icml-compbio.github.io/2023/papers/WCBICML2023_paper121.pdf)/[ICLR 2024](https://openreview.net/forum?id=jZPqf2G9Sw)

**ForceGen: End-to-end de novo protein generation based on nonlinear mechanical unfolding responses using a protein language diffusion model**
Bo Ni and David L. Kaplan and M. Buehler
[arXiv:2310.10605](https://arxiv.org/abs/2310.10605)/[Science Advances 10.6 (2024)](https://www.science.org/doi/10.1126/sciadv.adl4000) • [Supplementary](https://www.dropbox.com/scl/fi/33tnpd6u2xwermlvj22y9/SI_3_unfolding_movies_from_dataset.zip?rlkey=qno7rcitcdree8t9cj8wzg9sf&dl=0) • [code](https://github.com/lamm-mit/ProteinMechanicsDiffusionDesign)

**DiffSDS: A geometric sequence diffusion model for protein backbone inpainting**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=2xYO9oxh0y)/[arXiv:2301.09642](https://arxiv.org/abs/2301.09642)

**A framework for conditional diffusion modelling with applications in motif scaffolding for protein design**
Kieran Didi, Francisco Vargas, Simon V Mathis, Vincent Dutordoir, Emile Mathieu, Urszula J Komorowska, Pietro Lio
[arXiv:2312.09236](https://arxiv.org/abs/2312.09236)

**Improving diffusion-based protein backbone generation with global-geometry-aware latent encoding**
Yuyang Zhang, Yuhang Liu, Zinnia Ma, Min Li, Chunfu Xu & Haipeng Gong  
[bioRxiv 2023.12.13.571602](https://www.biorxiv.org/content/10.1101/2023.12.13.571602v1)/[Nat Mach Intell (2025)](https://www.nature.com/articles/s42256-025-01059-x)• [code](https://github.com/meneshail/TopoDiff)

**Improved motif-scaffolding with SE(3) flow matching**
Jason Yim, Andrew Campbell, Emile Mathieu, Andrew Y. K. Foong, Michael Gastegger, José Jiménez-Luna, Sarah Lewis, Victor Garcia Satorras, Bastiaan S. Veeling, Frank Noé, Regina Barzilay, Tommi S. Jaakkola
[arXiv:2401.04082](https://arxiv.org/abs/2401.04082)/[TMLR](https://openreview.net/forum?id=fa1ne8xDGn) • [code1](https://github.com/microsoft/frame-flow),[code2](https://github.com/microsoft/protein-frame-flow)

**DiffTopo: Fold exploration using coarse grained protein topology representations**
Yangyang Miao, Bruno Correia
[bioRxiv 2024.02.01.578456](https://www.biorxiv.org/content/10.1101/2024.02.01.578456v1)/ICLR 2024

**Diffusion models in protein structure and docking**
Jason Yim, Hannes Stärk, Gabriele Corso, Bowen Jing, Regina Barzilay, Tommi S. Jaakkola
[Wiley Interdisciplinary Reviews: Computational Molecular Science 14.2 (2024)](https://wires.onlinelibrary.wiley.com/doi/10.1002/wcms.1711) • review

**De novo antibody design with SE(3) diffusion**
Daniel Cutting, Frédéric A. Dreyer, David Errington, Constantin Schneider, Charlotte M. Deane
[arXiv:2405.07622](https://arxiv.org/abs/2405.07622)

**Out of Many, One: Designing and Scaffolding Proteins at the Scale of the Structural Universe with Genie 2**
Yeqing Lin, Minji Lee, Zhao Zhang, Mohammed AlQuraishi
[arXiv:2405.15489](https://arxiv.org/abs/2405.15489) • [code](https://github.com/aqlaboratory/genie2) • [news](https://www.marktechpost.com/2024/05/29/genie-2-transforming-protein-design-with-advanced-multi-motif-scaffolding-and-enhanced-structural-diversity/)

**DSG2-mini**
[DiffuseBio](https://www.linkedin.com/company/diffuse-bio/)
[technical appendix](https://diffuse.bio/updates.html#appendix) • [website](https://app.diffuse.bio/) • commercial

**Floating Anchor Diffusion Model for Multi-motif Scaffolding**
Ke Liu, Weian Mao, Shuaike Shen, Xiaoran Jiao, Zheng Sun, Hao Chen, Chunhua Shen
[ICML 2024](https://proceedings.mlr.press/v235/liu24av.html)/[arXiv:2406.03141](https://arxiv.org/abs/2406.03141) • [code](https://github.com/aim-uofa/FADiff) • [poster](https://icml.cc/virtual/2024/poster/34654)

**De novo Design of A Fusion Protein Tool for GPCR Research**
Kaixuan Gao, Xin Zhang, Jia Nie, Hengyu Meng, Weishe Zhang, Boxue Tian, Xiangyu Liu
[bioRxiv 2024.09.14.613090](https://www.biorxiv.org/content/10.1101/2024.09.14.613090v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/09/15/2024.09.14.613090/DC1/embed/media-1.pdf) • RFdiffusion-based

**Text2Protein: A Generative Model for Designated Protein Design on Given Description**
Ramtin Hosseini, Siyang Zhang, Pengtao Xie
[PREPRINT (Version 1) available at Research Square](https://doi.org/10.21203/rs.3.rs-4868665/v1) • [code](https://github.com/szhan227/text2protein)

**Diffusion Posterior Sampling via Sequential Monte Carlo for Zero-Shot Scaffolding of Protein Motifs**
Young, James Matthew Uygongco, and Omer Deniz Akyildiz
[Imperial CollegeofScience, Technology and Medicine, 2024](https://matsagad.com/files/papers/MRes_Project.pdf) • [code](https://github.com/matsagad/mres-project) • Master thesis • Genie-based

**Protein A-like Peptide Design Based on Diffusion and ESM2 Models**
Long Zhao, Qiang He, Huijia Song, Huijia Song,Tianqian Zhou, An Luo, Zhenguo Wen,Teng Wang, and Xiaozhu Lin
[Molecules 29.20 (2024)](https://www.mdpi.com/1420-3049/29/20/4965) • [code](https://github.com/tomlongcool/diffusion4Protein)

**FoldMark: Protecting Protein Generative Models with Watermarking**
Zaixi Zhang, Ruofan Jin, Kaidi Fu, Le Cong, Marinka Zitnik, Mengdi Wang
[arXiv:2410.20354](https://arxiv.org/abs/2410.20354) • [code](https://github.com/zaixizhang/FoldMark)

**ProteinWeaver: A Divide-and-Assembly Approach for Protein Backbone Design**
Yiming Ma, Fei Ye, Yi Zhou, Zaixiang Zheng, Dongyu Xue, Quanquan Gu
[arXiv:2411.16686](https://arxiv.org/abs/2411.16686)

**On Diffusion Posterior Sampling via Sequential Monte Carlo for Zero-Shot Scaffolding of Protein Motifs**
James Matthew Young, O. Deniz Akyildiz
[arXiv:2412.05788](https://arxiv.org/abs/2412.05788) • [code](https://github.com/matsagad/mres-project)

**From thermodynamics to protein design: Diffusion models for biomolecule generation towards autonomous protein engineering**
Wen-ran Li, Xavier F. Cadet, David Medina-Ortiz, Mehdi D. Davari, Ramanathan Sowdhamini, Cedric Damour, Yu Li, Alain Miranville, Frederic Cadet
[arXiv:2501.02680](https://arxiv.org/abs/2501.02680) • review

**RFdiffusion Exhibits Low Success Rate in De Novo Design of Functional Protein Binders for Biochemical Detection**
Bruce Jiang, Xiaoxiao Li, Amber Guo, Moris Wei, Jonny Wu
[bioRxiv 2025.02.07.636769](https://www.biorxiv.org/content/10.1101/2025.02.07.636769v1)

**From Atoms to Fragments: A Coarse Representation for Efficient and Functional Protein Design**
Leonardo V Castorina, Christopher W Wood, Kartic Subr
[bioRxiv 2025.03.19.644162](https://www.biorxiv.org/content/10.1101/2025.03.19.644162v2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/03/20/2025.03.19.644162/DC1/embed/media-1.pdf) • RFdiffusion-based

**Hierarchical Protein Backbone Generation with Latent and Structure Diffusion**
Jason Yim, Marouane Jaakik, Ge Liu, Jacob Gershon, Karsten Kreis, David Baker, Regina Barzilay, Tommi Jaakkola
[ICLR 2025](https://openreview.net/forum?id=J19jKa3wFj)

**The Dance of Atoms-De Novo Protein Design with Diffusion Model**
Yujie Qin, Ming He, Changyong Yu, Ming Ni, Xian Liu, Xiaochen Bo
[arXiv:2504.16479](https://arxiv.org/abs/2504.16479) • review

**ProT-GFDM: A Generative Fractional Diffusion Model for Protein Generation**  
Xiao Liang, Wentao Ma, Eric Paquet, Herna Lydia Viktor, Wojtek Michalowski
[arXiv:2504.21092](https://arxiv.org/abs/2504.21092)

**De novo design of phosphorylation-induced protein switches for synthetic signaling in cells**  
Stephen Buckley, Yangyang Miao, Mubarak Idris, Pao-Wan Lee, Leo Scheller, Roland Riek, Sebastian J. Maerkl, Luciano A. Abriata, Bruno E. Correia  
[bioRxiv 2025.09.10.675034](https://www.biorxiv.org/content/10.1101/2025.09.10.675034v1)

### 3.5 RL-based

**Top-down design of protein nanomaterials with reinforcement learning**
Isaac D Lutz, Shunzhi Wang, Christoffer Norn, Andrew J Borst, Yan Ting Zhao, Annie Dosey, Longxing Cao, Zhe Li, Minkyung Baek, Neil P King, Hannele Ruohola-Baker, David Baker
[bioRxiv 2022.09.25.509419](https://www.biorxiv.org/content/10.1101/2022.09.25.509419v1)/[Science380, 266-273(2023)](https://www.science.org/doi/10.1126/science.adf6591) • [code](https://github.com/idlutz/protein-backbone-MCTS),[code2](https://files.ipd.uw.edu/pub/2023_RL_capsid_design/sequence_design_pipeline.tar)

**Model-based reinforcement learning for protein backbone design**
Frederic Renard, Cyprien Courtot, Alfredo Reichlin, Oliver Bent
[arXiv:2405.01983](https://arxiv.org/abs/2405.01983)

**Target-based de novo design of cyclic peptide binders**
Fanhao Wang, Tiantian Zhang, Jintao Zhu, Xiaoling Zhang, Changsheng Zhang, Luhua Lai
[bioRxiv 2025.01.18.633746](https://www.biorxiv.org/content/10.1101/2025.01.18.633746v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/01/19/2025.01.18.633746/DC1/embed/media-1.pdf)

### 3.6 Flow-based

**SE(3)-Stochastic Flow Matching for Protein Backbone Generation**
Avishek Joey Bose, Tara Akhound-Sadegh, Kilian Fatras, Guillaume Huguet, Jarrid Rector-Brooks, Cheng-Hao Liu, Andrei Cristian Nica, Maksym Korablyov, Michael Bronstein, Alexander Tong
[arXiv:2310.02391](https://arxiv.org/abs/2310.02391)/[ICLR 2024](https://openreview.net/forum?id=kJFIH23hXb)

**Fast protein backbone generation with SE(3) flow matching**
Jason Yim, Andrew Campbell, Andrew Y. K. Foong, Michael Gastegger, José Jiménez-Luna, Sarah Lewis, Victor Garcia Satorras, Bastiaan S. Veeling, Regina Barzilay, Tommi Jaakkola, Frank Noé
[arXiv:2310.05297](https://arxiv.org/abs/2310.05297) • [code](https://github.com/microsoft/frame-flow)

**Sequence-Augmented SE(3)-Flow Matching For Conditional Protein Backbone Generation**
Guillaume Huguet, James Vuckovic, Kilian Fatras, Eric Thibodeau-Laufer, Pablo Lemos, Riashat Islam, Cheng-Hao Liu, Jarrid Rector-Brooks, Tara Akhound-Sadegh, Michael Bronstein, Alexander Tong, Avishek Joey Bose
[arXiv:2405.20313](https://arxiv.org/abs/2405.20313)/[NeurIPS 2024](https://openreview.net/forum?id=paYwtPBpyZ) • [website](https://www.dreamfold.ai/blog/foldflow-2) • [lecture](https://www.youtube.com/watch?v=xgA8T9h8mm0)

**Design of Ligand-Binding Proteins with Atomic Flow Matching**
Junqi Liu, Shaoning Li, Chence Shi, Zhi Yang, Jian Tang
[arXiv:2409.12080](https://arxiv.org/abs/2409.12080)

**ReQFlow: Rectified Quaternion Flow for Efficient and High-Quality Protein Backbone Generation**  
Angxiao Yue, Zichong Wang, Hongteng Xu  
[arXiv:2502.14637](https://arxiv.org/abs/2502.14637) • [code](https://github.com/AngxiaoYue/ReQFlow)

**Proteina: Scaling Flow-based Protein Structure Generative Models**
Tomas Geffner, Kieran Didi, Zuobai Zhang, Danny Reidenbach, Zhonglin Cao, Jason Yim, Mario Geiger, Christian Dallago, Emine Kucukbenli, Arash Vahdat, Karsten Kreis
[ICLR 2025 Oral](https://openreview.net/forum?id=TVQLu34bdw) • [code](https://github.com/NVIDIA-Digital-Bio/proteina/) • [website](https://research.nvidia.com/labs/genair/proteina/) • [lecture](https://www.youtube.com/watch?v=Y2dRj9_ZEHw)

**ProtComposer: Compositional Protein Structure Generation with 3D Ellipsoids**
Hannes Stark, Bowen Jing, Tomas Geffner, Jason Yim, Tommi Jaakkola, Arash Vahdat, Karsten Kreis
[ICLR 2025 Oral](https://openreview.net/forum?id=0ctvBgKFgc) • [code](https://github.com/NVlabs/protcomposer) • [lecture](https://www.youtube.com/watch?v=2G0d-RePc7c)

**Robust and Reliable de novo Protein Design: A Flow-Matching-Based Protein Generative Model Achieves Remarkably High Success Rates**  
Junyu Yan, Zibo Cui, Wenqing Yan, Yuhang Chen, Mengchen Pu, Shuai Li, Sheng Ye  
[bioRxiv 2025.04.29.651154](https://www.biorxiv.org/content/10.1101/2025.04.29.651154v1) • [code](https://github.com/JoreyYan/Originflow)

**Flexibility-conditioned protein structure design with flow matching**  
Vsevolod Viliuga, Leif Seute, Nicolas Wolf, Simon Wagner, Arne Elofsson, Jan Stühmer, Frauke Gräter  
[ICML 2025](https://openreview.net/forum?id=890gHX7ieS)

**Challenges and Guidelines in Deep Generative Protein Design: Four Case Studies**  
Tianyuan Zheng, Alessandro Rondina, Gos Micklem, Pietro Lio
[FM4LS 2025](https://openreview.net/forum?id=FcfpwlFDUZ)

### 3.7 Score-based

**Score-Based Generative Models for Designing Binding Peptide Backbones**
John D Boom, Matthew Greenig, Pietro Sormanni, Pietro Liò
[arXiv:2310.07051](https://arxiv.org/abs/2310.07051) • [code](https://github.com/mgreenig/loopgen)

**Building Confidence in Deep Generative Protein Design**
Tianyuan Zheng, Alessandro Rondina, Pietro Liò
[arXiv:2411.18568](https://arxiv.org/abs/2411.18568) • [code](https://github.com/ECburx/PROTEVAL)

## 4.Scaffold to Sequence

> Identify amino sequence from given backbone/scaffold/template constrains: torsion angles(φ & ψ), backbone angles(θ and τ), backbone dihedrals (φ, ψ & ω), backbone atoms (Cα, N, C, & O), Cα − Cα distance, unit direction vectors of Cα−Cα, Cα−N & Cα−C, etc(aka. inverse folding). Referred from [here](https://arxiv.org/abs/2202.01079). Energy-based models are also inculded for task of rotamer conformation(χ angles or atom coordinates) recovery.

### 4.0 Review

**Protein sequence design on given backbones with deep learning**
Yufeng Liu, Haiyan Liu
[Protein Engineering, Design and Selection, 2023](https://academic.oup.com/peds/advance-article-abstract/doi/10.1093/protein/gzad024/7503843)

**Multi-indicator comparative evaluation for deep Learning-Based protein sequence design methods**
Jinyu Yu, Junxi Mu, Ting Wei, Hai-Feng Chen
[Bioinformatics, 2024;, btae037](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btae037/7585533)

**Generative AI for Controllable Protein Sequence Design: A Survey**
Yiheng Zhu, Zitai Kong, Jialu Wu, Weize Liu, Yuqiang Han, Mingze Yin, Hongxia Xu, Chang-Yu Hsieh, Tingjun Hou
[arXiv:2402.10516](https://arxiv.org/abs/2402.10516)

**Backbone Conditional Protein Sequence Design**  
Justas Dauparas  
[Cold Spring Harbor Perspectives in Biology (2025)](https://cshperspectives.cshlp.org/content/early/2025/05/03/cshperspect.a041517)

**Zero-shot protein stability prediction by inverse folding models: a free energy interpretation**  
Jes Frellsen, Maher M. Kassem, Tone Bengtsen, Lars Olsen, Kresten Lindorff-Larsen, Jesper Ferkinghoff-Borg, Wouter Boomsma  
[arXiv:2506.05596](https://arxiv.org/abs/2506.05596)

### 4.1 MLP-based

**3D representations of amino acids-applications to protein sequence comparison and classification**
Li, Jie, and Patrice Koehl
[Computational and structural biotechnology journal 11.18 (2014)](https://www.sciencedirect.com/science/article/pii/S2001037014000270) • 2014

**Direct prediction of profiles of sequences compatible with a protein structure by neural networks with fragment-based local and energy-based nonlocal profiles**
Zhixiu Li, Yuedong Yang, Eshel Faraggi, Jian Zhan, Yaoqi Zhou
[Proteins: Structure, Function, and Bioinformatics 82.10 (2014)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.24620) • code unavailable

**SPIN2: Predicting sequence profiles from protein structures using deep neural networks**
James O'Connell, Zhixiu Li, Jack Hanson, Rhys Heffernan, James Lyons, Kuldip Paliwal, Abdollah Dehzangi, Yuedong Yang, Yaoqi Zhou
[Proteins: Structure, Function, and Bioinformatics 86.6 (2018)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25489) • code unavailable

**Computational protein design with deep learning neural networks**
Jingxue Wang, Huali Cao, John Z. H. Zhang & Yifei Qi
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-24760-x.pdf) • code unavailable

**Ligand-aware protein sequence design using protein self contacts**
Jody Mou, Benjamin Fry, Chun-Chen Yao, Nicholas Polizzi
[NeurIPS 2022](https://www.dropbox.com/s/98ri2f9gverljcw/Ligand-aware_protein_sequence_design_using_protein_self_contacts.pdf?dl=0)

**SeqPredNN: a neural network that generates protein sequences that fold into specified tertiary structures**
Lategan, F. Adriaan, Caroline Schreiber, and Hugh G. Patterton
[BMC bioinformatics 24.1 (2023)](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-023-05498-4) • [code](https://github.com/falategan/SeqPredNN)

### 4.2 VAE-based

**Design of metalloproteins and novel protein folds using variational autoencoders**
Greener, Joe G., Lewis Moffat, and David T. Jones
[Scientific reports 8.1 (2018)](https://www.nature.com/articles/s41598-018-34533-1)

**AlphaFold Database Debiasing for Robust Inverse Folding**  
Cheng Tan, Zhenxiao Cao, Zhangyang Gao, Siyuan Li, Yufei Huang, Stan Z. Li  
[arXiv:2506.08365](https://arxiv.org/abs/2506.08365)

**DivPro: diverse protein sequence design with direct structure recovery guidance**  
Xinyi Zhou, Guibao Shen, Yingcong Chen, Guangyong Chen, Pheng Ann Heng  
[Bioinformatics (2025)](https://academic.oup.com/bioinformatics/article/41/Supplement_1/i382/8199395) • [code](https://github.com/veghen/DivPro)

### 4.3 LSTM-based

**To improve protein sequence profile prediction through image captioning on pairwise residue distance map**
Sheng Chen, Zhe Sun, Lihua Lin, Zifeng Liu, Xun Liu, Yutian Chong, Yutong Lu, Huiying Zhao, and Yuedong Yang
[Journal of chemical information and modeling 60.1 (2019)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00438) • [SPROF](https://github.com/biomed-AI/SPROF)

**Deep learning of Protein Sequence Design of Protein-protein Interactions**
Syrlybaeva, Raulia, and Eva-Maria Strauch
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.01.28.478262v1)/[Bioinformatics, 2022;, btac733](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btac733/6827796) • [Supplementary](https://www.biorxiv.org/content/10.1101/2022.01.28.478262v1.supplementary-material) • [code](https://github.com/strauchlab/iNNterfaceDesign)

### 4.4 CNN-based

**A structure-based deep learning framework for protein engineering**
Raghav Shroff, Austin W. Cole, Barrett R. Morrow, Daniel J. Diaz, Isaac Donnell, Jimmy Gollihar, Andrew D. Ellington, Ross Thyer
[bioRxiv (2019)](https://www.biorxiv.org/content/10.1101/833905v1)

**ProDCoNN: Protein design using a convolutional neural network**
Yuan Zhang, Yang Chen, Chenran Wang, Chun-Chao Lo, Xiuwen Liu, Wei Wu, Jinfeng Zhang
[Proteins: Structure, Function, and Bioinformatics 88.7 (2020)](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25868) • code unavailable

**Protein sequence design with a learned potential**
Namrata Anand, Raphael Eguchi, Irimpan I. Mathews, Carla P. Perez, Alexander Derry, Russ B. Altman & Po-Ssu Huang
[Nacture Communications (2022)](https://www.nature.com/articles/s41467-022-28313-9) • [code](https://github.com/ProteinDesignLab/protein_seq_des)

**TIMED-Design: Flexible and Accessible Protein Sequence Design with Convolutional Neural Networks**
Leonardo V Castorina, Suleyman Mert Ünal, Kartic Subr, Christopher W Wood
[Protein Engineering, Design and Selection, 2024](https://academic.oup.com/peds/advance-article/doi/10.1093/protein/gzae002/7591701)) • [code](https://github.com/wells-wood-research/timed-design) • [website](https://pragmaticproteindesign.bio.ed.ac.uk/timed/)

**Biosensor and machine learning-aided engineering of an amaryllidaceae enzyme**
Simon d’Oelsnitz, Daniel J. Diaz, Wantae Kim, Daniel J. Acosta, Tyler L. Dangerfield, Mason W. Schechter, Matthew B. Minus, James R. Howard, Hannah Do, James M. Loy, Hal S. Alper, Y. Jessie Zhang & Andrew D. Ellington
[Nature Communications 15.1 (2024)](https://www.nature.com/articles/s41467-024-46356-y) • [code1](https://github.com/danny305/MutComputeX), [code2](https://github.com/simonsnitz/plotting)

**OPUS-Design: Designing Protein Sequence from Backbone Structure with 3DCNN and Protein Language Model**
Gang Xu, Yulu Yang, Yiqiu Zhang, Qinghua Wang, Jianpeng Ma
[bioRxiv 2024.08.20.608889](https://www.biorxiv.org/content/10.1101/2024.08.20.608889v2) • [code](https://github.com/OPUS-MaLab/opus_design)

**ProBID-Net: A Deep Learning Model for Protein-Protein Binding Interface Design**
Zhihang Chen, Menglin Ji, Jie Qiana, Zhe Zhang, Xiangying Zhang, Haotian Gao, Haojie Wang, Renxiao Wang, Yifei Qi
[Chemical Science (2024)](https://pubs.rsc.org/en/Content/ArticleLanding/2024/SC/D4SC02233E) • [code](https://github.com/ComputArtCMCG/ProBID-NET)

### 4.5 GNN-based

**Learning from protein structure with geometric vector perceptrons**
Bowen Jing, Stephan Eismann, Patricia Suriana, Raphael J.L. Townshend, Ron Dror
[arXiv preprint arXiv:2009.01411 (2020)](https://arxiv.org/abs/2009.01411)/[ICLR(2021)](https://openreview.net/forum?id=1YLJDvSx6J4) • [GVP](https://github.com/drorlab/gvp-pytorch)

**Fast and flexible protein design using deep graph neural networks**
Alexey Strokach, David Becerra, Carles Corbi-Verge, Albert Perez-Riba, Philip M. Kim
[Cell Systems (2020)](https://www.sciencedirect.com/science/article/pii/S2405471220303276) • [code::ProteinSolver](https://gitlab.com/ostrokach/proteinsolver)

**Mimetic Neural Networks: A unified framework for Protein Design and Folding**
Moshe Eliasof, Tue Boesen, Eldad Haber, Chen Keasar, Eran Treister
[arXiv:2102.03881](https://arxiv.org/abs/2102.03881)/[Front. Bioinform. 2:715006](https://www.frontiersin.org/articles/10.3389/fbinf.2022.715006/full)

**TERMinator: A Neural Framework for Structure-Based Protein Design using Tertiary Repeating Motifs**
Alex J. Li, Vikram Sundar, Gevorg Grigoryan, Amy E. Keating
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_TERMinator:_A_Neural_Framework.pdf) / [arXiv (2022)](https://arxiv.org/pdf/2204.13048.pdf)

**A neural network model for prediction of amino-acid probability from a protein backbone structure**
Shintaro Minami, Koya Sakuma, Naoya Kobayashi
Unpublished yet (June 2021)• [GCNdesgin](https://github.com/ShintaroMinami/GCNdesign)

**XENet: Using a new graph convolution to accelerate the timeline for protein design on quantum computers**
Jack B Maguire, Daniele Grattarola, Vikram Khipple Mulligan, Eugene Klyshko, Hans Melo
[PLoS computational biology 17.9 (2021)](https://pdfs.semanticscholar.org/23bc/58424378d15fda91e9d427fb553728c38b8a.pdf)

**AlphaDesign: A graph protein design method and benchmark on AlphaFoldDB**
Gao, Zhangyang, Cheng Tan, and Stan Li
[arXiv preprint arXiv:2202.01079 (2022)](https://arxiv.org/abs/2202.01079) • [code](https://github.com/jonathanking/sidechainnet)

**Generative De Novo Protein Design with Global Context**
Cheng Tan, Zhangyao Gao, Jun Xia and Stan Z. Li
[arXiv](https://arxiv.org/abs/2204.10673) • Apr 2022 • [code](https://github.com/chengtan9907/gca-generative-protein-design)

**Masked inverse folding with sequence transfer for protein representation learning**
Kevin K Yang, Hugh Yeh, Niccolò Zanichelli
[bioRxiv 2022.05.25.493516](https://www.biorxiv.org/content/10.1101/2022.05.25.493516v1)/[Protein Engineering, Design and Selection 36 (2023)](https://academic.oup.com/peds/article/doi/10.1093/protein/gzad015/7330543) • [code](https://github.com/microsoft/protein-sequence-models) • [model](https://doi.org/10.1234/mifst)

**Robust deep learning based protein sequence design using ProteinMPNN**
Justas Dauparas, Ivan Anishchenko, Nathaniel Bennett, Hua Bai, Robert J. Ragotte, Lukas F. Milles, Basile I. M. Wicky, Alexis Courbet, Robbert J. de Haas, Neville Bethel, Philip J. Y. Leung, Timothy F. Huddy, Sam Pellock, Doug Tischer, Frederick Chan, Brian Koepnick, Hannah Nguyen, Alex Kang, Banumathi Sankaran, Asim Bera, Neil P. King, David Baker
[bioRxiv 2022.06.03.494563](https://www.biorxiv.org/content/10.1101/2022.06.03.494563v1.article-metrics)/[Science (2022)](https://www.science.org/doi/10.1126/science.add2187) • [code](https://github.com/dauparas/ProteinMPNN) • [hugging face](https://huggingface.co/spaces/simonduerr/ProteinMPNN) • [lecture](https://www.youtube.com/watch?v=aVQQuoToTJA) • [colab(in_jax)](https://colab.research.google.com/github/sokrypton/ColabDesign/blob/v1.1.0/mpnn/examples/proteinmpnn_in_jax.ipynb) • [ProteinMPNN+ESMFold](https://huggingface.co/spaces/simonduerr/ProteinMPNNESM/blob/main/README.md)

**Antibody-Antigen Docking and Design via Hierarchical Equivariant Refinement**
Jin, Wengong, Regina Barzilay, and Tommi Jaakkola
[arXiv preprint arXiv:2207.06616 (2022)](https://arxiv.org/abs/2207.06616)/[International Conference on Machine Learning. PMLR, 2022](https://icml.cc/virtual/2022/poster/16625) • [code](https://github.com/wengong-jin/abdockgen) • [poster](https://icml.cc/media/PosterPDFs/ICML%202022/b7f520a55897b35e6eb462bbf80915c6.png)

**Neural Network-Derived Potts Models for Structure-Based Protein Design using Backbone Atomic Coordinates and Tertiary Motifs**
Alex J. Li, Mindren Lu, Israel Desta, Vikram Sundar, Gevorg Grigoryan, and Amy E. Keating
[bioRxiv 2022.08.02.501736](https://www.biorxiv.org/content/10.1101/2022.08.02.501736v1.full.pdf)/[Protein Science, 32(2)](https://onlinelibrary.wiley.com/doi/10.1002/pro.4554)

**SE(3) Equivalent Graph Attention Network as an Energy-Based Model for Protein Side Chain Conformation**
Deqin Liu, Sheng Chen, Shuangjia Zheng, Sen Zhang, Yuedong Yang
[bioRxiv 2022.09.05.506704](https://www.biorxiv.org/content/10.1101/2022.09.05.506704v1) • [code](https://github.com/biomed-AI/GraphEBM)

**PiFold: Toward effective and efficient protein inverse folding**
Zhangyang Gao, Cheng Tan, Stan Z. Li
[arXiv:2209.12643v2](https://arxiv.org/abs/2209.12643v3)/[ICLR 2023](https://openreview.net/pdf?id=oMsN9TYwJ0j) • [github](https://github.com/A4Bio/PiFold)

**Protein Sequence Design by Entropy-based Iterative Refinement**
Xinyi Zhou, Guangyong Chen, Junjie Ye, Ercheng Wang, Jun Zhang, Cong Mao, Zhanwei Li, Jianye Hao, Xingxu Huang, Jin Tang, Pheng Ann Heng
[bioRxiv 2023.02.04.527099](https://www.biorxiv.org/content/10.1101/2023.02.04.527099v1)

**Lightweight Contrastive Protein Structure-Sequence Transformation**
Jiangbin Zheng, Ge Wang, Yufei Huang, Bozhen Hu, Siyuan Li, Cheng Tan, Xinwen Fan, Stan Z. Li
[arXiv:2303.11783](https://arxiv.org/abs/2303.11783)

**Modeling Protein Structure Using Geometric Vector Field Networks**
Weian Mao, Muzhi Zhu, Hao Chen, Chunhua Shen
[bioRxiv 2023.05.07.539736](https://www.biorxiv.org/content/10.1101/2023.05.07.539736v1)

**Knowledge-Design: Pushing the Limit of Protein Deign via Knowledge Refinement**
Zhangyang Gao, Cheng Tan, Stan Z. Li
[arXiv:2305.15151](https://arxiv.org/abs/2305.15151)/[ICLR](https://openreview.net/forum?id=mpqMVWgqjn) • [code](https://github.com/A4Bio/ProteinInvBench)

**SPIN-CGNN: Improved fixed backbone protein design with contact map-based graph construction and contact graph neural network**
Xing Zhang, Hongmei Yin, Fei Ling, Jian Zhan, Yaoqi Zhou
[bioRxiv 2023.07.07.548080](https://www.biorxiv.org/content/10.1101/2023.07.07.548080v1)/[PLOS Computational Biology](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1011330) • [code](https://github.com/EricZhangSCUT/SPIN-CGNN)

**ZetaDesign: an end-to-end deep learning method for protein sequence design and side-chain packing**
Junyu Yan and others
[Briefings in Bioinformatics, 2023](https://academic.oup.com/bib/advance-article-abstract/doi/10.1093/bib/bbad257/7222295) • [code](https://github.com/JoreyYan/zetadesign)

**Contextual protein encodings from equivariant graph transformers**
Sai Pooja Mahajan, Jeffrey A. Ruffolo, Jeffrey J. Gray
[bioRxiv 2023.07.15.549154](https://www.biorxiv.org/content/10.1101/2023.07.15.549154v1) • [code](https://github.com/GrayLab/MaskedProteinEnT)

**Robust Design of Effective Allosteric Activators for Rsp5 E3 Ligase Using the Machine Learning Tool ProteinMPNN**
Hsi-Wen Kao, Wei-Lin Lu, Meng-Ru Ho, Yu-Fong Lin, Yun-Jung Hsieh, Tzu-Ping Ko, Shang-Te Danny Hsu, and Kuen-Phon Wu
[ACS Synthetic Biology (2023)](https://pubs.acs.org/doi/10.1021/acssynbio.3c00042) • [Supplementary](https://pubs.acs.org/doi/suppl/10.1021/acssynbio.3c00042/suppl_file/sb3c00042_si_001.pdf)

**Rapid and automated design of two-component protein nanomaterials using ProteinMPNN**
Robbert J. de Haas, Natalie Brunette, Alex Goodson, Justas Dauparas, Sue Y. Yi, Erin C. Yang, Quinton Dowling, Hannah Nguyen, Alex Kang, Asim K. Bera, Banumathi Sankaran, Renko de Vries, David Baker, Neil P. King
[bioRxiv 2023.08.04.551935](https://www.biorxiv.org/content/10.1101/2023.08.04.551935v1)/[Proceedings of the National Academy of Sciences 121.(13)](https://www.pnas.org/doi/10.1073/pnas.2314646121) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/08/04/2023.08.04.551935/DC1/embed/media-1.pdf) • [data](https://zenodo.org/records/8278877)

**Rationally seeded computational protein design**
Katherine I. Albanese, Rokas Petrenas, Fabio Pirro, Elise A. Naudin, Ufuk Borucu, William M. Dawson, D. Arne Scott, Graham J. Leggett, Orion D. Weiner, Thomas A. A. Oliver, Derek N. Woolfson
[bioRxiv 2023.08.25.554789](https://www.biorxiv.orxg/content/10.1101/2023.08.25.554789v1) • [code](https://github.com/polizzilab/design_tools)

**Computational design of sequence-specific DNA-binding proteins**
Cameron J Glasscock, Robert Pecoraro, Ryan McHugh, Lindsey A. Doyle, Wei Chen, Olivier Boivin, Beau Lonnquist, Emily Na, Yuliya Politanska, Hugh K Haddox, David Cox, Christoffer Norn, Brian Coventry, Inna Goreshnik, Dionne Vafeados, Gyu Rie Lee, Raluca Gordan, Barry L Stoddard, Frank DiMaio, David Baker
[bioRxiv 2023.09.20.558720](https://www.biorxiv.org/content/10.1101/2023.09.20.558720v1)/[Nat Struct Mol Biol (2025)](https://www.nature.com/articles/s41594-025-01669-4) • [code](https://github.com/cjg263/dbp_design)  • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/09/21/2023.09.20.558720/DC1/embed/media-1.docx)

**Improving protein expression, stability, and function with ProteinMPNN**
Kiera H. Sumida, Reyes Núñez Franco, Indrek Kalvet, Samuel J. Pellock, Basile I. M. Wicky, Lukas F. Milles, Justas Dauparas, Jue Wang, Yakov Kipnis, Noel Jameson, Alex Kang, Joshmyn De La Cruz, Banumathi Sankaran, Asim K Bera, Gonzalo Jimenez Oses, David Baker
[bioRxiv 2023.10.03.560713](https://www.biorxiv.org/content/10.1101/2023.10.03.560713v1)/[J. Am. Chem. Soc. 2024](https://pubs.acs.org/doi/full/10.1021/jacs.3c10941) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/10/03/2023.10.03.560713/DC1/embed/media-1.pdf)

**A Suite of Designed Protein Cages Using Machine Learning Algorithms and Protein Fragment-Based Protocols**
Kyle Meador, Roger Castells-Graells, Roman Aguirre, Michael R. Sawaya, Mark A. Arbing, Trent Sherman, Chethaka Senarathne, Todd O. Yeates
[bioRxiv 2023.10.09.561468](https://www.biorxiv.org/content/10.1101/2023.10.09.561468v1) • [code](https://github.com/kylemeador/symdesign) • [colab](https://bit.ly/symdesign-colab)

**PROTEIN DESIGNER BASED ON SEQUENCE PROFILE USING ULTRAFAST SHAPE RECOGNITION**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=s4mPCrSNUZ)

**Inverse folding for antibody sequence design using deep learning**
Frédéric A. Dreyer, Daniel Cutting, Constantin Schneider, Henry Kenlay, Charlotte M. Deane
[arXiv:2310.19513](https://arxiv.org/abs/2310.19513)

**De novo design of allosterically switchable protein assemblies**
Arvind Pillai, Abbas Idris, Annika Philomin, Connor Weidle, Rebecca Skotheim, Philip J. Y. Leung, Adam Broerman, Cullen Demakis, Andrew J. Borst, Florian Praetorius, David Baker
[bioRxiv 2023.11.01.565167](https://www.biorxiv.org/content/10.1101/2023.11.01.565167v1)/[Nature (2024)](https://www.nature.com/articles/s41586-024-07813-2) • [code](https://github.com/arvind-pillai/switchable_rings) • [data](https://www.biorxiv.org/content/biorxiv/early/2023/11/02/2023.11.01.565167/DC1/embed/media-1.zip)

**ProRefiner: an entropy-based refining strategy for inverse protein folding with global graph attention**
Xinyi Zhou, Guangyong Chen, Junjie Ye, Ercheng Wang, Jun Zhang, Cong Mao, Zhanwei Li, Jianye Hao, Xingxu Huang, Jin Tang, Pheng Ann Heng
[Nature Communications](https://www.nature.com/articles/s41467-023-43166-6) • [Supplementary](https://static-content.springer.com/esm/art%3A10.1038%2Fs41467-023-43166-6/MediaObjects/41467_2023_43166_MOESM1_ESM.pdf) • [code](https://zenodo.org/records/10030882)

**Engineered immunogens to elicit antibodies against conserved coronavirus epitopes**
A. Brenda Kapingidza, Daniel J. Marston, Caitlin Harris, Daniel Wrapp, Kaitlyn Winters, Dieter Mielke, Lu Xiaozhi, Qi Yin, Andrew Foulger, Rob Parks, Maggie Barr, Amanda Newman, Alexandra Schäfer, Amanda Eaton, Justine Mae Flores, Austin Harner, Nicholas J. Catanzaro Jr., Michael L. Mallory, Melissa D. Mattocks, Christopher Beverly, Brianna Rhodes, Katayoun Mansouri, Elizabeth Van Itallie, Pranay Vure, Brooke Dunn, Taylor Keyes, Sherry Stanfield-Oakley, Christopher W. Woods, Elizabeth A. Petzold, Emmanuel B. Walter, Kevin Wiehe, Robert J. Edwards, David C. Montefiori, Guido Ferrari, Ralph Baric, Derek W. Cain, Kevin O. Saunders, Barton F. Haynes & Mihai L. Azoitei
[Nat Commun 14, 7897 (2023)](https://www.nature.com/articles/s41467-023-43638-9) • [code](https://github.com/AzoiteiLab/S2-scaffold-scripts)

**DNDesign: Enhancing Physical Understanding of Protein Inverse Folding Model via Denoising**
Youhan Lee, Jaehoon Kim
[bioRxiv 2023.12.05.570298](https://www.biorxiv.org/content/10.1101/2023.12.05.570298v1)

**In vitro validated antibody design against multiple therapeutic antigens using generative inverse folding**
Amir Shanehsazzadeh, Julian Alverio, George Kasun, Simon Levine, Jibran A Khan, Chelsea Chung, Nicolas Diaz, Breanna K Luton, Ysis Tarter, Cailen McCloskey, Katherine B Bateman, Hayley Carter, Dalton Chapman, Rebecca Consbruck, Alec Jaeger, Christa Kohnert, Gaelin Kopec-Belliveau, John M Sutton, Zheyuan Guo, Gustavo Canales, Kai Ejan, Emily Marsh, Alyssa Ruelos, Rylee Ripley, Brooke Stoddard, Rodante Caguiat, Kyra Chapman, Matthew Saunders, Jared Sharp, Douglas Ganini da Silva, Audree Feltner, Jake Ripley, Megan E Bryant, Danni Castillo, Joshua Meier, Christian M Stegmann, Katherine Moran, Christine Lemke, Shaheed Abdulhaqq, Lillian R Klug, Sharrol Bachas
[bioRxiv 2023.12.08.570889](https://www.biorxiv.org/content/10.1101/2023.12.08.570889v1)

**SPDesign: protein sequence designer based on structural sequence profile using ultrafast shape recognition**
Hui Wang, Dong Liu, Kailong Zhao, Yajun Wang, Guijun Zhang
[bioRxiv 2023.12.14.571651](https://www.biorxiv.org/content/10.1101/2023.12.14.571651v1)/[Briefings in Bioinformatics 25.3 (2024): bbae146](https://academic.oup.com/bib/article/25/3/bbae146/7642672) • [website](http://zhanglab-bioinf.com/SPDesign/)

**De novo design of diverse small molecule binders and sensors using Shape Complementary Pseudocycles**
Linna An, Meerit Said, Long Tran, Sagardip Majumder, Inna Goreshnik, Gyu Rie Lee, David Juergens, Justas Dauparas, Ivan Anishchenko, Brian Coventry, Asim K Bera, Alex Kang, Paul M Levine, Valentina Alvarez, Arvindd Pillai, Christoffer Norn, David Feldman, Dmitri Zorine, Derrick R Hicks, Xinting Li, Mariana Garcia Sanchez, Dionne K Vafeados, Patrick J Salveson, Anastassia A Vorobieva, David Baker
[bioRxiv 2023.12.20.572602](https://www.biorxiv.org/content/10.1101/2023.12.20.572602v1)/[Science385,276-282(2024)](https://www.science.org/doi/10.1126/science.adn3780) • [code1](https://github.com/LAnAlchemist/Pseudocycle_small_molecule_binder), [code2](https://github.com/iamlongtran/pseudocycle_paper), [code3](https://github.com/feldman4/ngs_app)

**Atomic context-conditioned protein sequence design using LigandMPNN**
Justas Dauparas, Gyu Rie Lee, Robert Pecoraro, Linna An, Ivan Anishchenko, Cameron Glasscock, D. Baker
[bioRxiv 2023.12.22.573103](https://www.biorxiv.org/content/10.1101/2023.12.22.573103v1)/[Nat Methods (2025)](https://www.nature.com/articles/s41592-025-02626-1) • [code](https://github.com/dauparas/LigandMPNN)

**Structure-conditioned masked language models for protein sequence design generalize beyond the native sequence space**
Deniz Akpinaroglu, Kosuke Seki, Amy Guo, Eleanor Zhu, Mark J. S. Kelly, Tanja Kortemme
[bioRxiv 2023.12.15.571823](https://www.biorxiv.org/content/10.1101/2023.12.15.571823v1) • [code](https://github.com/dakpinaroglu/Frame2seq)

**ProteinMPNN Recovers Complex Sequence Properties of Transmembrane β-Barrels**
Marissa D Dolorfino, Anastassia A Vorobieva
[bioRxiv 2024.01.16.575764](https://www.biorxiv.org/content/10.1101/2024.01.16.575764v1) • [code](https://github.com/marissadolorfino2024/ProteinMPNN-TMB-Design.git)

**DIProT: A deep learning based interactive toolkit for efficient and effective Protein design**
He, Jieling, Wenxu Wu, and Xiaowo Wang
[Synthetic and Systems Biotechnology (2024)](https://www.sciencedirect.com/science/article/pii/S2405805X24000115)

**Blueprinting extendable nanomaterials with standardized protein blocks**
Timothy F. Huddy, Yang Hsia, Ryan D. Kibler, Jinwei Xu, Neville Bethel, Deepesh Nagarajan, Rachel Redler, Philip J. Y. Leung, Connor Weidle, Alexis Courbet, Erin C. Yang, Asim K. Bera, Nicolas Coudray, S. John Calise, Fatima A. Davila-Hernandez, Hannah L. Han, Kenneth D. Carr, Zhe Li, Ryan McHugh, Gabriella Reggiano, Alex Kang, Banumathi Sankaran, Miles S. Dickinson, Brian Coventry, T. J. Brunette, Yulai Liu, Justas Dauparas, Andrew J. Borst, Damian Ekiert, Justin M. Kollman, Gira Bhabha & David Baker
[Nature (2024)](https://www.nature.com/articles/s41586-024-07188-4) • [RosettaScripts](https://github.com/tfhuddy/2023-manuscript-materials)

**All-atom protein sequence design based on geometric deep learning**
Jiale Liu, Zheng Guo, Changsheng Zhang, Luhua Lai
[bioRxiv 2024.03.18.585651](https://www.biorxiv.org/content/10.1101/2024.03.18.585651v1)/[Angew. Chem. Int. Ed. 2024](https://onlinelibrary.wiley.com/doi/abs/10.1002/anie.202411461) • [code](https://github.com/PKUliujl/GesSeqBuilder)

**Graphormer supervised de novo protein design method and function validation**
Junxi Mu, Zhengxin Li, Bo Zhang, Qi Zhang, Jamshed Iqbal,   Abdul Wadood, Ting Wei, Yan Feng, Hai-Feng Chen
[Briefings in Bioinformatics 25.3 (2024): bbae135](https://academic.oup.com/bib/article/25/3/bbae135/7638270) • [code](https://github.com/decodermu/GPD)

**The Damietta Server: a comprehensive protein design toolkit**
Iwan Grin, Kateryna Maksymenko, Tobias Wörtwein, Mohammad ElGamacy
[Nucleic Acids Research, 2024;, gkae297](https://academic.oup.com/nar/advance-article/doi/10.1093/nar/gkae297/7658041) • [website](https://damietta.de/) • ProteinMPNN-based • [news](https://cbirt.net/protein-design-made-easy-with-damietta-server-a-comprehensive-toolkit/), [news2](https://www.innovations-report.com/life-sciences/toolkit-makes-protein-design-faster-and-more-accessible/)

**Exploring the Potential of Structure-Based Deep Learning Approaches for T cell Receptor Design**
Helder V. Ribeiro-Filho, Gabriel E. Jara, João V. S. Guerra, Melyssa Cheung, Nathaniel R. Felbinger, José G. C. Pereira, Brian G. Pierce, Paulo S. Lopes-de-Oliveira
[bioRxiv 2024.04.19.590222](https://www.biorxiv.org/content/10.1101/2024.04.19.590222v1) • [code](https://github.com/LBC-LNBio/ESMIFDesign), [code2](https://github.com/piercelab/tcrmodel2/)

**SurfPro: Functional Protein Design Based on Continuous Surface**
Zhenqiao Song, Tinglin Huang, Lei Li, Wengong Jin
[arXiv:2405.06693](https://arxiv.org/abs/2405.06693) • ProteinMPNN-based

**Computational Design of Myoglobin-based Carbene Transferases for Monoterpene Derivatization**
Yiyang Sun, Yinian Tang, Jing Zhou, Bingchen Guo, Feiyan Yuan, Bo Yao, Yang Yu, Chun Li
[Biochemical and Biophysical Research Communications (2024)](https://www.sciencedirect.com/science/article/pii/S0006291X2400696X) • [code](https://github.com/yangyu1-github/MbDesignMPNN) • LigandMPNN-based

**UniIF: Unified Molecule Inverse Folding**
Zhangyang Gao, Jue Wang, Cheng Tan, Lirong Wu, Yufei Huang, Siyuan Li, Zhirui Ye, Stan Z. Li
[arXiv:2405.18968](https://arxiv.org/abs/2405.18968)

**Integrating MHC Class I visibility targets into the ProteinMPNN protein design process**
Hans-Christof Gasser, Diego A. Oyarzún, Javier Antonio Alfaro, Ajitha Rajan
[bioRxiv 2024.06.04.597365](https://www.biorxiv.org/content/10.1101/2024.06.04.597365v1)

**A Top-Down Design Approach for Generating a Peptide PROTAC Drug Targeting Androgen Receptor for Androgenetic Alopecia Therapy**
Bohan Ma, Donghua Liu, Zhe Wang, Dize Zhang, Yanlin Jian, Kun Zhang, Tianyang Zhou, Yibo Gao, Yizeng Fan, Jian Ma, Yang Gao, Yule Chen, Si Chen, Jing Liu, Xiang Li, and Lei Li
[Journal of Medicinal Chemistry (2024)](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c00828)

**Improving Inverse Folding models at Protein Stability Prediction without additional Training or Data**
Oliver Dutton, Sandro Bottaro, Michele Invernizzi, Istvan Redl, Albert Chung, Carlo Fisicaro, Fabio Airoldi, Stefano Ruschetta, Louie Henderson, Benjamin MJ Owens, Patrik Foerch, Kamil Tamiola
[bioRxiv 2024.06.15.599145](https://www.biorxiv.org/content/10.1101/2024.06.15.599145v1) • ProteinMPNN/ESMIF-based

**Kernel-Based Evaluation of Conditional Biological Sequence Models**
Pierre Glaser, Steffanie Paul, Alissa M Hummer, Charlotte Deane, Debora Susan Marks, Alan Nawzad Amin
[Proceedings of the 41st International Conference on Machine Learning, PMLR 235:15678-15705, 2024](https://proceedings.mlr.press/v235/glaser24a.html) • ProteinMPNN-based

**Design of intrinsically disordered region binding proteins**  
Kejia Wu, Hanlun Jiang, Derrick R. Hicks, Caixuan Liu, Edin Muratspahić, Theresa A. Ramelot, Yuexuan Liu, Kerrie McNally, Sebastian Kenny, Andrei Mihut, Amit Gaur, Brian Coventry, Wei Chen, Asim K. Bera, Alex Kang, Stacey Gerben, Mila Ya-Lan Lamb, Analisa Murray, Xinting Li, Madison A. Kennedy, Wei Yang, Zihao Song, Gudrun Schober, Stuart M. Brierley, John O’Neill, Michael H. Gelb, Gaetano T. Montelione, Emmanuel Derivery, David Baker  
[bioRxiv 2024.07.15.603480](https://www.biorxiv.org/content/10.1101/2024.07.15.603480v3)/[Science389,eadr8063(2025)](https://www.science.org/doi/10.1126/science.adr8063)

**CodonMPNN for Organism Specific and Codon Optimal Inverse Folding**
Hannes Stark, Umesh Padia, Julia Balla, Cameron Diao, George Church
[arXiv:2409.17265](https://arxiv.org/abs/2409.17265) • ProteinMPNN-based • [code](https://github.com/HannesStark/CodonMPNN)

**Exploring the potential of structure-based deep learning approaches for T cell receptor design**
Helder V. Ribeiro-Filho, Gabriel E. Jara, João V. S. Guerra, Melyssa Cheung,Nathaniel R. Felbinger, José G. C. Pereira, Brian G. Pierce, Paulo S. Lopes-de-Oliveira
[PLoS Comput Biol 20(9)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1012489) • ProteinMPNN-based • ESM-based

**ProteusAI: An Open-Source and User-Friendly Platform for Machine Learning-Guided Protein Design and Engineering**
Jonathan Funk, Laura Machado, Samuel A. Bradley, Marta Napiorkowska, Rodrigo Gallegos-Dextre, Liubov Pashkova, Niklas G. Madsen, Henry Webel, Patrick Victor Phaneuf, Timothy P. Jenkins, Carlos G. Acevedo-Rocha Sr
[bioRxiv 2024.10.01.616114](https://www.biorxiv.org/content/10.1101/2024.10.01.616114v1) • ProteinMPNN-based • ESM-based

**Improving Inverse Folding for Peptide Design with Diversity-regularized Direct Preference Optimization**
Ryan Park, Darren J. Hsu, C. Brian Roland, Maria Korshunova, Chen Tessler, Shie Mannor, Olivia Viessmann, Bruno Trentini
[arXiv:2410.19471](https://arxiv.org/abs/2410.19471)

**Computational design of developable therapeutic antibodies: efficient traversal of binder landscapes and rescue of escape mutations**
Frédéric A. Dreyer, Constantin Schneider, Aleksandr Kovaltsuk, Daniel Cutting, Matthew J. Byrne, Daniel A. Nissley, Newton Wahome, Henry Kenlay, Claire Marks, David Errington, Richard J. Gildea, David Damerell, Pedro Tizei, Wilawan Bunjobpol, John F. Darby, Ieva Drulyte, Daniel L. Hurdiss, Sachin Surade, Douglas E. V. Pires, Charlotte M. Deane
[bioRxiv 2024.10.03.616038](https://www.biorxiv.org/content/10.1101/2024.10.03.616038v1) • [code](https://github.com/Exscientia/ab-characterisation) • AbMPNN-based

**State-specific Peptide Design Targeting G Protein-coupled Receptors**
Yang Xue, Jun Li, Hong Wang, Jianguo Hu, Zhi Zheng, Jingzhou He, Huanzhang Gong, Xiangqun Li, Xiaonan Zhang, Xiaomin Fang
[bioRxiv 2024.11.27.625792](https://www.biorxiv.org/content/10.1101/2024.11.27.625792v2) • ProteinMPNN-based

**Computer-guided design of Z domain peptides with improved inhibition of VEGF**
Carsten Geist, Abibe Useini, Aleksandr Kazimir, Richy Kümpfel, Jens Meiler, Christina Lamers, Stefan Kalkhof, Georg Künze
[bioRxiv 2024.11.29.626075](https://www.biorxiv.org/content/10.1101/2024.11.29.626075v1) [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/11/30/2024.11.29.626075/DC1/embed/media-1.pdf) • ProteinMPNN-based

**HyperMPNN – A general strategy to design thermostable proteins learned from hyperthermophiles**
Moritz Ertelt, Phillip Schlegel, Max Beining, Leonard Kaysser, Jens Meiler, Clara T. Schoeder
[bioRxiv 2024.11.26.625397](https://www.biorxiv.org/content/10.1101/2024.11.26.625397v1) • [code](https://github.com/meilerlab/HyperMPNN) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/01/2024.11.26.625397/DC1/embed/media-1.pdf)

**IgDesign: In vitro validated antibody design against multiple therapeutic antigens using inverse folding**
Amir Shanehsazzadeh, Julian Alverio, George Kasun, Simon Levine, Ido Calman, Jibran A. Khan, Chelsea Chung, Nicolas Diaz, Breanna K. Luton, Ysis Tarter, Cailen McCloskey, Katherine B. Bateman, Hayley Carter, Dalton Chapman, Rebecca Consbruck, Alec Jaeger, Christa Kohnert, Gaelin Kopec-Belliveau, John M. Sutton, Zheyuan Guo, Gustavo Canales, Kai Ejan, Emily Marsh, Alyssa Ruelos, Rylee Ripley, Brooke Stoddard, Rodante Caguiat, Kyra Chapman, Matthew Saunders, Jared Sharp, Douglas Ganini da Silva, Audree Feltner, Jake Ripley, Megan E. Bryant, Danni Castillo, Joshua Meier, Christian M. Stegmann, Katherine Moran, Christine Lemke, Shaheed Abdulhaqq, Lillian R. Klug, Sharrol Bachas
[bioRxiv 2023.12.08.570889](https://www.biorxiv.org/content/10.1101/2023.12.08.570889v1) • [code](https://github.com/AbSciBio/igdesign)

**Learning to engineer protein flexibility**
Petr Kouba, Joan Planas-Iglesias, Jiri Damborsky, Jiri Sedlar, Stanislav Mazurenko, Josef Sivic
[arXiv:2412.18275](https://arxiv.org/abs/2412.18275) • [code](https://github.com/KoubaPetr/Flexpert)

**AI.zymes – A modular platform for evolutionary enzyme design**
Lucas P. Merlicek, Jannik Neumann, Abbie Lear, Vivian Degiorgi, Moor de Waal, Tudor-Stefan Cotet, Adrian J. Mulholland, H. Adrian Bunzel
[bioRxiv 2025.01.18.633707](https://www.biorxiv.org/content/10.1101/2025.01.18.633707v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/01/22/2025.01.18.633707/DC1/embed/media-1.pdf)

**AI-assisted protein design to rapidly convert antibody sequences to intrabodies targeting diverse peptides and histone modifications**
Gabriel Galindo, Daiki Maejima, Jacob DeRoo, Scott R. Burlingham, Gretchen Fixen, Tatsuya Morisaki, Hallie P. Febvre, Ryan Hasbrook, Ning Zhao, Soham Ghosh, E. Handly Mayton, Christopher D. Snow, Brian J. Geiss, Yasuyuki Ohkawa, Yuko Sato, Hiroshi Kimura, Timothy J. Stasevich
[bioRxiv 2025.02.06.636921](https://www.biorxiv.org/content/10.1101/2025.02.06.636921v2) • [code](https://github.com/jbderoo/scFv_Pmpnn_AF2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/02/09/2025.02.06.636921/DC1/embed/media-1.pdf) • ProteinMPNN-based

**Sidechain conditioning and modeling for full-atom protein sequence design with FAMPNN**
Richard W. Shuai, Talal Widatalla, Po-Ssu Huang, Brian L. Hie
[bioRxiv 2025.02.13.637498](https://www.biorxiv.org/content/10.1101/2025.02.13.637498v1) • [code](https://github.com/richardshuai/fampnn)

**Fast and Accurate Antibody Sequence Design via Structure Retrieval**
Xingyi Zhang, Kun Xie, Ningqiao Huang, Wei Liu, Peilin Zhao, Sibo Wang, Kangfei Zhao, Biaobin Jiang
[arXiv:2502.19395](https://arxiv.org/abs/2502.19395)

**Enhancing Functional Protein Design Using Heuristic Optimization and Deep Learning for Anti‐Inflammatory and Gene Therapy Applications**
Patat, Ayşenur Soytürk, and Özkan Ufuk Nalbantoğlu
[Proteins: Structure, Function, and Bioinformatics (2025)](https://onlinelibrary.wiley.com/doi/10.1002/prot.26810) • [code](https://github.com/aysenursoyturk/HMHO)

**ProDualNet: Dual-Target Protein Sequence Design Method Based on Protein Language Model and Structure Model**
Liu Cheng, Ting Wei, Xiaochen Cui, Haifeng Chen, Zhangsheng Yu
[bioRxiv 2025.02.28.640919](https://www.biorxiv.org/content/10.1101/2025.02.28.640919v1)/[Briefings in Bioinformatics, July 2025, bbaf391](https://academic.oup.com/bib/article/26/4/bbaf391/8241296) • [code](https://github.com/chengliu97/ProDualNet)

**CHIEF: An Attention-based Ensemble Learning Framework for Functional Protein Design**
Zilong Geng, Yuze Wang, Tingting Liu, Ao Tan, Shuo Wu, Xiaoling Guo, Ruogu Li, Xumin Hou, Kun Sun, LianPin Wu, Qinghua Cui, Lintai Da, Zhiyuan Ma, Honglin Li, Bing Zhang
[bioRxiv 2025.03.07.641005](https://www.biorxiv.org/content/10.1101/2025.03.07.641005v2) • ProteinMPNN-based • ESM-IF-based • Frame2seq-based • PiFold-based

**Tuning ProteinMPNN to reduce protein visibility via MHC Class I through direct preference optimization**
Hans-Christof Gasser, Diego A Oyarzún, Javier Alfaro, Ajitha Rajan
[Protein Engineering, Design and Selection (2025)](https://academic.oup.com/peds/advance-article/doi/10.1093/protein/gzaf003/8082933) • [code](https://github.com/hcgasser/CAPE_MPNN) • ProteinMPNN-based

**AI-Driven Efficient De Novo design of GLP-1RAs with Extended Half-Life and Enhanced Efficacy**
Ting Wei, Xiaochen Cui, Jiahui Lin, Zhuoqi Zheng, Taiying Cui, Liu Cheng, Xiaoqian Lin, Junjie Zhu, Xuyang Ran, Xiaohun Hong, Zhangsheng Yu, Haifeng Chen
[bioRxiv 2025.03.26.645438](https://www.biorxiv.org/content/10.1101/2025.03.26.645438v1) • ProteinMPNN-based

**A novel decoding strategy for ProteinMPNN to design with less MHC Class I immune-visibility**
Hans-Christof Gasser, Ajitha Rajan, Javier A. Alfaro
[bioRxiv 2025.04.14.648837](https://www.biorxiv.org/content/10.1101/2025.04.14.648837v1) • ProteinMPNN-based

**Zero-shot design of drug-binding proteins via neural selection-expansion**  
Benjamin Fry, Kaia Slaw, Nicholas F. Polizzi  
[bioRxiv 2025.04.22.649862](https://www.biorxiv.org/content/10.1101/2025.04.22.649862v1) • [code](https://github.com/polizzilab/LASErMPNN)

**Conformation-specific Design: a New Benchmark and Algorithm with Application to Engineer a Constitutively Active Map Kinase**  
Jacob A. Stern, Siba Alharbi, Anandsukeerthi Sandholu, Stefan T. Arold, Dennis Della Corte  
[bioRxiv 2025.04.23.650138](https://www.biorxiv.org/content/10.1101/2025.04.23.650138v1) • [code](https://github.com/dellacortelab/cs_design) • [dataset](https://github.com/dellacortelab/motif_div)

**Deep learning guided design of dynamic proteins**
Amy B. Guo, Deniz Akpinaroglu, Mark J.S. Kelly, Tanja Kortemme
[bioRxiv 2024.07.17.603962](https://www.biorxiv.org/content/10.1101/2024.07.17.603962v1)/[Science388,eadr7094(2025)](https://www.science.org/doi/10.1126/science.adr7094) • [code](https://github.com/amyguo1997/dynamic_protein_design) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/07/19/2024.07.17.603962/DC1/embed/media-1.docx)

**AI. zymes–A modular platform for evolutionary enzyme design**  
Lucas P. Merlicek, Jannik Neumann, Abbie Lear, Vivian Degiorgi, Moor M. de Waal, Tudor-Stefan Cotet, Adrian J. Mulholland, Adrian Bunzel  
[Angewandte Chemie International Edition (2025)](https://onlinelibrary.wiley.com/doi/10.1002/anie.202507031) • [code](https://github.com/bunzela/AIzymes) • ProteinMPNN-based

**Design of overlapping genes using deep generative models of protein sequences**  
Gun Woo Byeon, Marc Expòsit, David Baker, Georg Seelig  
[bioRxiv 2025.05.06.652464](https://www.biorxiv.org/content/10.1101/2025.05.06.652464v1) • [code](https://github.com/gwbyeon/OLG-design) • ProteinMPNN-based

**De novo design of porphyrin-containing proteins as efficient and stereoselective catalysts**  
Kaipeng Hou, Wei Huang, Miao Qi, Thomas H. Tugwell, Turki M. Alturaifi, Yuda Chen, Xingjie Zhang, Lei Lu, Samuel I. Mann, Peng Liu, Yang Yang, and William F. DeGrado  
[Science 388.6747 (2025)](https://www.science.org/doi/full/10.1126/science.adt7268) • LigandMPNN-based

**Adapting ProteinMPNN for antibody design without retraining**  
Diego del Alamo, Rahel Frick, Daphne Truan, Joel D Karpiak  
[bioRxiv 2025.05.09.653228](https://www.biorxiv.org/content/10.1101/2025.05.09.653228v1)

**HighMPNN: A Graph Neural Network Approach for Structure-Constrained Cyclic Peptide Sequence Design**  
Wen Xu, Chengyun Zhang ,Tianfeng Shang ,Qingyi Mao ,Hongliang Duan  
[ChemRxiv. 2025](https://chemrxiv.org/engage/chemrxiv/article-details/6826dcef927d1c2e661210c2)

**Computational design of dynamic biosensors for emerging synthetic opioids**  
Alison C. Leonard, Chase Lenert-Mondou, Rachel Chayer, Samuel Swift, Zachary T. Baumer, Ryan Delaney, Anika J. Friedman, Nicholas R. Robertson, Norman Seder, Jordan Wells, Lindsey M. Whitmore, Sean R. Cutler, Michael R. Shirts, Ian Wheeldon, Timothy A. Whitehead  
[bioRxiv 2025.05.15.654300](https://www.biorxiv.org/content/10.1101/2025.05.15.654300v1) • LigandMPNN-based

**Designing Cyclic Peptides via Harmonic SDE with Atom-Bond Modeling**  
Xiangxin Zhou, Mingyu Li, Yi Xiao, Jiahan Li, Dongyu Xue, Zaixiang Zheng, Jianzhu Ma, Quanquan Gu  
[arXiv:2505.21452](https://arxiv.org/abs/2505.21452)

**De novo design of high-affinity miniprotein binders targeting Francisella tularensis virulence factor**  
Gizem Gokce-Alpkilic, Buwei Huang, Andi Liu, Lieselotte S.M. Kreuk, Yaxi Wang, Victor Adebomi, Yensi Flores Bueso, Asim K. Bera, Alex Kang, Stacey R. Gerben, Stephen Rettie, Dionne K. Vafeados, Nicole Roullier, Inna Goreshnik, Xinting Li, David Baker, Joshua J. Woodward, Joseph D. Mougous, Gaurav Bhardwaj  
[bioRxiv 2025.07.02.662053](https://www.biorxiv.org/content/10.1101/2025.07.02.662053v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/07/05/2025.07.02.662053/DC1/embed/media-1.pdf) • [code](https://www.biorxiv.org/content/biorxiv/early/2025/07/05/2025.07.02.662053/DC2/embed/media-2.zip) • ProteinMPNN-based

**A Computational Workflow for Structure-Guided Design of Potent and Selective Kinase Peptide Substrates**  
Abeeb A. Yekeen, Cynthia J. Meyer, Melissa McCoy, Bruce Posner, Kenneth D. Westover  
[bioRxiv 2025.07.04.663216](https://www.biorxiv.org/content/10.1101/2025.07.04.663216v1) • ProteinMPNN-based

**Fully functional AAV viral vectors with highly altered structural cores and subunit interfaces using ProteinMPNN**  
Ziyu Jiang, Sirimar Laosinwattana, Paul A. Dalby  
[bioRxiv 2025.07.24.666527](https://www.biorxiv.org/content/10.1101/2025.07.24.666527v1)

**Computational design of bifaceted protein nanomaterials**  
Sanela Rankovic, Kenneth D. Carr, Justin Decarreau, Rebecca Skotheim, Ryan D. Kibler, Sebastian Ols, Sangmin Lee, Jung-Ho Chun, Marti R. Tooley, Justas Dauparas, Helen E. Eisenach, Matthias Glögl, Connor Weidle, Andrew J. Borst, David Baker & Neil P. King  
[Nat. Mater. (2025)](https://www.nature.com/articles/s41563-025-02295-7)

**Multi-state Protein Design with DynamicMPNN**  
Alex Abrudan, Sebastian Pujalte Ojeda, Chaitanya K. Joshi, Matthew Greenig, Felipe Engelberger, Alena Khmelinskaia, Jens Meiler, Michele Vendruscolo, Tuomas P. J. Knowles  
[arXiv:2507.21938](https://arxiv.org/abs/2507.21938) • [code](https://github.com/Alex-Abrudan/DynamicMPNN)

**De Novo Design of High-Performance Cortisol Luminescent Biosensors**
Julie Yi-Hsuan Chen, Xue Peng, Chenggang Xi, Gyu Rie Lee, David Baker, Andy Hsien-Wei Yeh  
[J. Am. Chem. Soc](https://pubs.acs.org/doi/abs/10.1021/jacs.5c05004)

**Accelerating protein design by scaling experimental characterization**  
Jason Qian, Lukas F. Milles, Basile I. M. Wicky, Amir Motmaen, Xinting Li, Ryan D. Kibler, Lance Stewart, David Baker  
[bioRxiv 2025.08.05.668824](https://www.biorxiv.org/content/10.1101/2025.08.05.668824v1) • [code](https://github.com/bwicky/SAPP_DMX)

**AI-Driven De Novo Design of Ultra Long-Acting GLP-1 Receptor Agonists**  
Ting Wei, Jiating Ma, Xiaochen Cui, Jiahui Lin, Zhuoqi Zheng, Liu Cheng, Taiying Cui, Xiaoqian Lin, Junjie Zhu, Xuyang Ran, Xiaokun Hong, Luke Johnston, Zhangsheng Yu, Haifeng Chen  
[Advanced science (Weinheim, Baden-Wurttemberg, Germany)](https://advanced.onlinelibrary.wiley.com/doi/10.1002/advs.202507044) • ProteinMPNN-based

**From sequence to scaffold: computational design of protein nanoparticle vaccines from AlphaFold2-predicted building blocks**  
Cyrus M. Haas, Naveen Jasti, Annie Dosey, Joel D. Allen, Rebecca Gillespie, Jackson McGowan, Elizabeth M. Leaf, Max Crispin, Cole A. DeForest, Masaru Kanekiyo, Neil P. King  
[bioRxiv 2025.08.20.671178](https://www.biorxiv.org/content/10.1101/2025.08.20.671178v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/08/20/2025.08.20.671178/DC1/embed/media-1.pdf)

**De novo design of light-responsive protein–protein interactions enables reversible formation of protein assemblies**  
Bowen Yu, Jiao Liu, Zhanyuan Cui, Chu Wang, Peipei Chen, Chentong Wang, Yanzhe Zhang, Xingxing Zhu, Ze Zhang, Shichao Li, Jinheng Pan, Mingqi Xie, Huaizong Shen & Longxing Cao  
[Nat. Chem. (2025)](https://www.nature.com/articles/s41557-025-01929-2) • [code](https://github.com/LongxingLab/NCAA_Light_Assembly)

### 4.6 GAN-based

**De novo protein design for novel folds using guided conditional Wasserstein generative adversarial networks**
Mostafa Karimi, Shaowen Zhu, Yue Cao, Yang Shen
[Journal of chemical information and modeling 60.12 (2020)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.0c00593) • [gcWGAN](https://github.com/Shen-Lab/gcWGAN)

**HelixGAN: A bidirectional Generative Adversarial Network with search in latent space for generation under constraints**
Xuezhi Xie, Philip M. Kim
[Machine Learning for Structural Biology Workshop, NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_HelixGAN:_A_bidirectional_Generative.pdf)/[Bioinformatics, 2023;, btad036](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btad036/6991169) • [code](https://github.com/xxiexuezhi/helix_gan)

### 4.7 Transformer-based

**Generative models for graph-based protein design**
[John Ingraham](https://openreview.net/profile?email=ingraham%40csail.mit.edu), Vikas K Garg, Dr.Regina Barzilay, Tommi Jaakkola
[NeurIPS 2019](https://openreview.net/forum?id=ByMEAHrgLB) • [GraphTrans](https://github.com/jingraham/neurips19-graph-protein-design)

**Fold2Seq: A Joint Sequence (1D)-Fold (3D) Embedding-based Generative Model for Protein Design**
Yue Cao, Payel Das, Vijil Chenthamarakshan, Pin-Yu Chen, Igor Melnyk, Yang Shen
[International Conference on Machine Learning. PMLR, 2021](https://arxiv.org/pdf/2106.13058)

**Rotamer-Free Protein Sequence Design Based on Deep Learning and Self-Consistency**
Yufeng Liu, Lu Zhang, Weilun Wang, Min Zhu, Chenchen Wang, Fudong Li, Jiahai Zhang, Houqiang Li, Quan Chen& Haiyan Liu
[Nature portfolio (2022)](https://www.researchsquare.com/article/rs-1209166/v1)/[Nature computational science(2022)](https://www.nature.com/articles/s43588-022-00273-6) • [Supplementary](https://static-content.springer.com/esm/art%3A10.1038%2Fs43588-022-00273-6/MediaObjects/43588_2022_273_MOESM1_ESM.pdf) • [Comment](https://www.nature.com/articles/s43588-022-00274-5) • [code](https://codeocean.com/capsule/6949436/tree/v1)

**A Deep SE(3)-Equivariant Model for Learning Inverse Protein Folding**
Mmatthew McPartlon, Ben Lai, Jinbo Xu
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.15.488492v1)

**Learning inverse folding from millions of predicted structures**
Chloe Hsu, Robert Verkuil, Jason Liu, Zeming Lin, Brian Hie, Tom Sercu, Adam Lerer, Alexander Rives
[bioRxiv (2022)](https://doi.org/10.1101/2022.04.10.487779) • [esm](https://github.com/facebookresearch/esm)

**Breaking boundaries in protein design with a new AI model that understands interactions with any kind of molecule**
LucianoSphere
[Towards Data Science](https://towardsdatascience.com/breaking-boundaries-in-protein-design-with-a-new-ai-model-that-understands-interactions-with-any-388fd747ee40)

**Accurate and efficient protein sequence design through learning concise local environment of residues**
Bin Huang, Tingwen Fan, Kaiyue Wang, Haicang Zhang, Chungong Yu, Shuyu Nie, Yangshuo Qi, Wei-Mou Zheng, Jian Han, Zheng Fan, Shiwei Sun, Sheng Ye, Huaiyi Yang, Dongbo Bu
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.06.25.497605v4)/[Bioinformatics 39.3 (2023)](https://academic.oup.com/bioinformatics/article/39/3/btad122/7077134) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/06/30/2022.06.25.497605/DC1/embed/media-1.pdf) • [website](http://81.70.37.223) • [code](https://github.com/bigict/ProDESIGN-LE)

**PeTriBERT : Augmenting BERT with tridimensional encoding for inverse protein folding and design**
Baldwin Dumortier, Antoine Liutkus, Clément Carré, Gabriel Krouk
[bioRxiv 2022.08.10.503344](https://www.biorxiv.org/content/10.1101/2022.08.10.503344v1)

**Evolutionary-scale prediction of atomic level protein structure with a language model**
Zeming Lin, Halil Akin, Roshan Rao, Brian Hie, Zhongkai Zhu, Wenting Lu, Nikita Smetanin, Robert Verkuil, Ori Kabeli, Yaniv Shmueli, Allan dos Santos Costa, Maryam Fazel-Zarandi, Tom Sercu, Salvatore Candido, Alexander Rives
[bioRxiv 2022.07.20.500902](https://www.biorxiv.org/content/10.1101/2022.07.20.500902v2) • [blog](https://ai.facebook.com/blog/protein-folding-esmfold-metagenomics/) • [github](https://github.com/facebookresearch/esm)

**Structure-informed Language Models Are Protein Designers**
Zaixiang Zheng, Yifan Deng, Dongyu Xue, Yi Zhou, Fei YE, Quanquan Gu
[arXiv:2302.01649](https://arxiv.org/abs/2302.01649) • [code::ByProt](https://github.com/BytedProtein/ByProt)

**Incorporating Pre-training Paradigm for Antibody Sequence-Structure Co-design**
Kaiyuan Gao, Lijun Wu, Jinhua Zhu, Tianbo Peng, Yingce Xia, Liang He, Shufang Xie, Tao Qin, Haiguang Liu, Kun He, Tie-Yan Liu
[arXiv:2211.08406](https://arxiv.org/abs/2211.08406) • [code](https://github.com/KyGao/ABGNN)

**A Text-guided Protein Design Framework**
Shengchao Liu, Yutao Zhu, Jiarui Lu, Zhao Xu, Weili Nie, Anthony Gitter, Chaowei Xiao, Jian Tang, Hongyu Guo, Anima Anandkumar
[arXiv:2302.04611](https://arxiv.org/abs/2302.04611)/[Nat Mach Intell (2025)](https://www.nature.com/articles/s42256-025-01011-z) • [code](https://github.com/chao1224/ProteinDT)

**An end-to-end deep learning method for protein side-chain packing and inverse folding**
McPartlon, Matthew, and Jinbo Xu
[Proceedings of the National Academy of Sciences 120.23 (2023)](https://www.pnas.org/doi/10.1073/pnas.2216438120) • [code](https://github.com/MattMcPartlon/AttnPacker) • [Supplementary](https://www.pnas.org/doi/suppl/10.1073/pnas.2216438120/suppl_file/pnas.2216438120.sapp.pdf)

**Context-aware geometric deep learning for protein sequence design**
Lucien Krapp, Fernado Meireles, Luciano Abriata, Matteo Dal Peraro
[bioRxiv 2023.06.19.545381](https://www.biorxiv.org/content/10.1101/2023.06.19.545381v1)/[Nature Communications, 2024](https://www.nature.com/articles/s41467-024-50571-y) • [code](https://github.com/LBM-EPFL/CARBonARa) • [News](https://actu.epfl.ch/news/a-new-ai-approach-to-protein-design/)

**De Novo Generation and Prioritization of Target-Binding Peptide Motifs from Sequence Alone**
Suhaas Bhat, Kalyan Palepu, Vivian Yudistyra, Lauren Hong, Venkata Srikar Kavirayuni, Tianlai Chen, Lin Zhao, Tian Wang, Sophia Vincoff, Pranam Chatterjee
[bioRxiv 2023.06.26.546591](https://www.biorxiv.org/content/10.1101/2023.06.26.546591v1) • [code](https://github.com/programmablebio/pepprclip) • [colab](https://drive.google.com/drive/u/0/folders/1A4kQXjsG5j3OrO0XQtzBWWZu9Zm7c0ak) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/06/28/2023.06.26.546591/DC1/embed/media-1.pdf)

**ProstT5: Bilingual Language Model for Protein Sequence and Structure Michael Heinzinger**
Konstantin Weissenow, Joaquin Gomez Sanchez, Adrian Henkel, Martin Steinegger, Burkhard Rost
[bioRxiv 2023.07.23.550085](https://www.biorxiv.org/content/10.1101/2023.07.23.550085v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/07/25/2023.07.23.550085/DC1/embed/media-1.pdf) • [code](https://github.com/mheinzinger/ProstT5)

**De novo Protein Sequence Design Based on Deep Learning and Validation on CalB Hydrolase**
Junxi Mu, ZhengXin Li, Bo Zhang, Qi Zhang, Jamshed Iqbal, Abdul Wadood, Ting Wei, Yan Feng, Haifeng Chen
[bioRxiv 2023.08.01.551444](https://www.biorxiv.org/content/10.1101/2023.08.01.551444v1) • [code](https://github.com/weitinging/GPD)

**Invariant point message passing for protein side chain packing and design**
Nicholas Z Randolph, Brian Kuhlman
[bioRxiv 2023.08.03.551328](https://www.biorxiv.org/content/10.1101/2023.08.03.551328v1) • [code](https://github.com/Kuhlman-Lab/PIPPack)

**Atom-by-atom protein generation and beyond with language models**
Daniel Flam-Shepherd, Kevin Zhu, Alán Aspuru-Guzik
[arXiv:2308.09482](https://arxiv.org/abs/2308.09482)

**SaProt: Protein Language Modeling with Structure-aware Vocabulary**
Jin Su, Chenchen Han, Yuyang Zhou, Junjie Shan, Xibin Zhou, Fajie Yuan
[bioRxiv 2023.10.01.560349](https://www.biorxiv.org/content/10.1101/2023.10.01.560349v5) • [code](https://github.com/westlake-repl/SaProt)

**SaprotHub: Making Protein Modeling Accessible to All Biologists**
Jin Su, Zhikai Li, Chenchen Han, Yuyang Zhou, Yan He, Junjie Shan, Xibin Zhou, Xing Chang, Shiyu Jiang, Dacheng Ma, The OPMC, Martin Steinegger, Sergey Ovchinnikov,  Fajie Yuan
[bioRxiv 2024.05.24.595648](https://www.biorxiv.org/content/10.1101/2024.05.24.595648)  •  [code](https://github.com/westlake-repl/SaprotHub) • [colab](https://colab.research.google.com/github/westlake-repl/SaprotHub/blob/main/colab/SaprotHub_v2.ipynb)

**AntiFold: Improved antibody structure design using inverse folding**
Magnus Høie, Alissa Hummer, Tobias Olsen, Morten Nielsen, Charlotte Deane
[GenBio@NeurIPS2023 Spotlight](https://openreview.net/forum?id=bxZMKHtlL6)/[Bioinformatics Advances (2025)](https://academic.oup.com/bioinformaticsadvances/advance-article/doi/10.1093/bioadv/vbae202/8090019) • [code](https://opig.stats.ox.ac.uk/data/downloads/AntiFold/), [github](https://github.com/oxpig/AntiFold) • [colab](https://colab.research.google.com/drive/1TTfgjoZx3mzF5u4e9b4Un9Y7b_rqXc_4), [website](https://opig.stats.ox.ac.uk/webapps/antifold/)

**MMDesign: Multi-Modality Transfer Learning for Generative Protein Design**
Jiangbin Zheng, Siyuan Li, Yufei Huang, Zhangyang Gao, Cheng Tan, Bozhen Hu, Jun Xia, Ge Wang, Stan Z. Li
[arXiv preprint arXiv:2312.06297 (2023)](https://arxiv.org/abs/2312.06297)

**ShapeProt: Top-down Protein Design with 3D Protein Shape Generative Model**
Lee, Youhan, and Jaehoon Kim
[bioRxiv (2023): 2023-12](https://www.biorxiv.org/content/10.1101/2023.12.03.567710v3)

**X-LoRA: Mixture of Low-Rank Adapter Experts, a Flexible Framework for Large Language Models with Applications in Protein Mechanics and Design**
Eric L. Buehler, Markus J. Buehler
[arXiv:2402.07148](https://arxiv.org/abs/2402.07148) • [code](https://github.com/EricLBuehler/xlora) • [Model &amp; weights](https://huggingface.co/lamm-mit/x-lora)

**AntiFold: Improved antibody structure-based design using inverse folding**
Magnus Haraldson Høie, Alissa Hummer, Tobias H. Olsen, Broncio Aguilar-Sanjuan, Morten Nielsen, Charlotte M. Deane
[arXiv:2405.03370](https://arxiv.org/abs/2405.03370) • [code](https://github.com/oxpig/AntiFold) • [website](https://opig.stats.ox.ac.uk/webapps/antifold/) • ESM-IF-based

**Protein Design with StructureGPT: a Deep Learning Model for Protein Structure-to-Sequence Translation**
Nicanor Zalba Sr., Pablo Ursua-Medrano Sr., Humberto Bustince Sr
[bioRxiv 2024.06.03.597105](https://www.biorxiv.org/content/10.1101/2024.06.03.597105v1) • [code](https://github.com/StructureGPT) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/06/07/2024.06.03.597105/DC1/embed/media-1.pdf)

**Adapting protein language models for structure-conditioned design**
Jeffrey A Ruffolo, Aadyot Bhatnagar, Joel Beazer, Stephen Nayfach, Jordan Russ, Emily Hill, Riffat Hussain, Joseph Gallagher, Ali Madani
[bioRxiv 2024.08.03.606485](https://www.biorxiv.org/content/10.1101/2024.08.03.606485v1) • [code](https://github.com/Profluent-AI/proseLM-public) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/08/03/2024.08.03.606485/DC1/embed/media-1.zip) • [news](https://www.genengnews.com/topics/artificial-intelligence/giving-structure-to-language-profluents-ai-models-move-toward-precise-and-steerable-protein-design/) • [lecture](https://www.youtube.com/watch?v=MkwM3t80XpQ)

**EMOCPD: Efficient Attention-based Models for Computational Protein Design Using Amino Acid Microenvironment**
Xiaoqi Ling, Cheng Cai, Demin Kong, Zhisheng Wei, Jing Wu, Lei Wang, Zhaohong Deng
[arXiv:2410.21069](https://arxiv.org/abs/2410.21069)/[Journal of Chemical Information and Modeling (2024)](https://pubs.acs.org/doi/10.1021/acs.jcim.5c00378) • [data](https://github.com/lingxqqqqq/DataSet)

**Mixture of Experts Enable Efficient and Effective Protein Understanding and Design**
Ning Sun, Shuxian Zou, Tianhua Tao, Sazan Mahbub, Dian Li, Yonghao Zhuang, Hongyi Wang, Xingyi Cheng, Le Song, Eric P. Xing
[bioRxiv 2024.11.29.625425](https://www.biorxiv.org/content/10.1101/2024.11.29.625425v1) • [code](https://github.com/genbio-ai/AIDO/)

**Finetuning ESM3 with Contrastive Preference Optimization for Antigen-Specific Antibody Design**
Anirudh Venkatraman, Gopinath Balaji, Veeresh Kande
[UIUC Fall 2024 CS582 MLCB](https://openreview.net/forum?id=wDpvm3TrhE) • [code](https://github.com/anirudhvenk/antibody-dpo)

**Protein CREATE enables closed-loop design of de novo synthetic protein binders**
Alec Lourenço, Arjuna Subramanian, Ryan Spencer, Michael Anaya, Jiapei Miao, William Fu, Eric Chow, Matt Thomson
[bioRxiv 2024.12.20.629847](https://www.biorxiv.org/content/10.1101/2024.12.20.629847v1) • ESM-IF-based

**DS-ProGen: A Dual-Structure Deep Language Model for Functional Protein Design**  
Yanting Li, Jiyue Jiang, Zikang Wang, Ziqian Lin, Dongchen He, Yuheng Shan, Yanruisheng Shao, Jiayi Li, Xiangyu Shi, Jiuming Wang, Yanyu Chen, Yimin Fan, Han Li, Yu Li  
[arXiv:2505.12511](https://arxiv.org/abs/2505.12511)

### 4.8 ResNet-based

**DenseCPD: improving the accuracy of neural-network-based computational protein sequence design with DenseNet**
Qi, Yifei, and John ZH Zhang
[Journal of chemical information and modeling 60.3 (2020)](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.0c00043) • code unavailable

**DeepUSPS: Deep Learning‐Empowered Unconstrained‐Structural Protein Sequence Design**  
Zhichong Ma, Jiawen Yang  
[Proteins: Structure, Function, and Bioinformatics (2025)](https://onlinelibrary.wiley.com/doi/10.1002/prot.26847) • [code](https://github.com/mazhichong/MZC) • [data](https://zenodo.org/records/10811470)

### 4.9 Diffusion-based

**De novo protein backbone generation based on diffusion with structured priors and adversarial training**
Yufeng Liu, Linghui Chen, Haiyan Liu
[bioRxiv 2022.12.17.520847](https://www.biorxiv.org/content/10.1101/2022.12.17.520847v1)/[Nat Methods (2024)](https://www.nature.com/articles/s41592-024-02437-w) • [code](https://github.com/liuyf020419/SCUBA-D)

**Generative design of de novo proteins based on secondary-structure constraints using an attention-based diffusion model**
Bo Ni, David L. Kaplan, Markus J. Buehler
[Chem,(2023)](https://www.cell.com/chem/fulltext/S2451-9294(23)00139-0) • [code](https://github.com/lamm-mit/ProteinDiffusionGenerator) • [news](https://news.mit.edu/2023/ai-system-can-generate-novel-proteins-structural-design-0420)

**Graph Denoising Diffusion for Inverse Protein Folding**
Kai Yi, Bingxin Zhou, Yiqing Shen, Pietro Liò, Yu Guang Wang
[arXiv:2306.16819](https://arxiv.org/abs/2306.16819)/[NeurIPS 2023](https://openreview.net/forum?id=u4YXKKG5dX) • [code](https://github.com/ykiiiiii/GraDe_IF)

**Conditional Protein Denoising Diffusion Generates Programmable Endonucleases**
Bingxin Zhou, Lirong Zheng, Banghao Wu, Kai Yi, Bozitao Zhong, Pietro Lio, Liang Hong
[bioRxiv 2023.08.10.552783](https://www.biorxiv.org/content/10.1101/2023.08.10.552783v1)

**Diffusion in a quantized vector space generates non-idealized protein structures and predicts conformational distributions**
Liu Haiyan, Liu Yufeng, Chen Linghui
[bioRxiv 2023.11.18.567666](https://www.biorxiv.org/content/10.1101/2023.11.18.567666v1)

**Fast non-autoregressive inverse folding with discrete diffusion**
John J. Yang, Jason Yim, Regina Barzilay, Tommi Jaakkola
[arXiv:2312.02447](https://arxiv.org/abs/2312.02447) • [code](https://github.com/johnyang101/pmpnndiff)

**Diffusion Language Models Are Versatile Protein Learners**
Xinyou Wang, Zaixiang Zheng, Fei Ye, Dongyu Xue, Shujian Huang, Quanquan Gu
[arXiv:2402.18567](https://arxiv.org/abs/2402.18567)

**LéxFusion**
Levinthal
paper not available • [news](https://mp.weixin.qq.com/s/Iex0YndimhLDM0mASp1MtA) • commercial

**A conditional protein diffusion model generates artificial programmable endonuclease sequences with enhanced activity**
Bingxin Zhou, Lirong Zheng, Banghao Wu, Kai Yi, Bozitao Zhong, Yang Tan, Qian Liu, Pietro Liò, Liang Hong
[bioRxiv 2023.08.10.552783](https://www.biorxiv.org/content/10.1101/2023.08.10.552783v2)/[Cell Discovery 10.1 (2024)](https://www.nature.com/articles/s41421-024-00728-2) • [code](https://github.com/bzho3923/CPDiffusion)

**LaGDif: Latent Graph Diffusion Model for Efficient Protein Inverse Folding with Self-Ensemble**
Taoyu Wu, Yu Guang Wang, Yiqing Shen
[arXiv:2411.01737](https://arxiv.org/abs/2411.01737) • [code](https://github.com/TaoyuW/LaGDif)

**Bridge-IF: Learning Inverse Protein Folding with Markov Bridges**
Yiheng Zhu, Jialu Wu, Qiuyi Li, Jiahuan Yan, Mingze Yin, Wei Wu, Mingyang Li, Jieping Ye, Zheng Wang, Jian Wu
[arXiv:2411.02120](https://arxiv.org/abs/2411.02120) • [code](https://github.com/violet-sto/Bridge-IF)

**Mask prior-guided denoising diffusion improves inverse protein folding**
Peizhen Bai, Filip Miljković, Xianyuan Liu, Leonardo De Maria, Rebecca Croasdale-Wood, Owen Rackham, Haiping Lu
[arXiv:2412.07815](https://arxiv.org/abs/2412.07815)/[Nature Machine Intelligence (2025)](https://www.nature.com/articles/s42256-025-01042-6) • [code](https://github.com/peizhenbai/MapDiff)

**Agentic End-to-End De Novo Protein Design for Tailored Dynamics Using a Language Diffusion Model**
Bo Ni, Markus J. Buehler
[arXiv preprint arXiv:2502.10173 (2025)](https://arxiv.org/pdf/2502.10173) • [code](https://github.com/lamm-mit/ModeShapeDiffusionDesign), [model](https://huggingface.co/lamm-mit/VibeGen)

**All-Atom Protein Sequence Design using Discrete Diffusion Models**  
Amelia Villegas-Morcillo, Gijs J. Admiraal, Marcel J.T. Reinders, Jana M. Weber  
[bioRxiv 2025.06.13.659451](https://www.biorxiv.org/content/10.1101/2025.06.13.659451v1) • [code](https://github.com/Intelligent-molecular-systems/All-Atom-Protein-Sequence-Generation)

### 4.10 Bayesian-based

**Inverse Protein Folding Using Deep Bayesian Optimization**
Natalie Maus, Yimeng Zeng, Daniel Allen Anderson, Phillip Maffettone, Aaron Solomon, Peyton Greenside, Osbert Bastani, Jacob R. Gardner
[arXiv:2305.18089](https://arxiv.org/abs/2305.18089) • [code](https://github.com/nataliemaus/bo-if)

**Design of Protein Sequences with Precisely Tuned Kinetic Properties**
Z. Faidon Brotzakis, Michele Vendruscolo, Georgios Skretas
[bioRxiv 2025.02.13.638027](https://www.biorxiv.org/content/10.1101/2025.02.13.638027v1)

**IgCraft: A versatile sequence generation framework for antibody discovery and engineering**
Matthew Greenig, Haowen Zhao, Vladimir Radenkovic, Aubin Ramon, Pietro Sormanni
[arXiv:2503.19821](https://arxiv.org/abs/2503.19821) • [code](https://github.com/mgreenig/IgCraft)

### 4.11 Flow-based

**Harmonic Self-Conditioned Flow Matching for Multi-Ligand Docking and Binding Site Design**
Hannes Stärk, Bowen Jing, Regina Barzilay, Tommi Jaakkola
[arXiv:2310.05764](https://arxiv.org/abs/2310.05764) • [code](https://github.com/HannesStark/FlowSite)

### 4.12 RL-based

**Fine-Tuning Discrete Diffusion Models via Reward Optimization with Applications to DNA and Protein Design**
Chenyu Wang, Masatoshi Uehara, Yichun He, Amy Wang, Tommaso Biancalani, Avantika Lal, Tommi Jaakkola, Sergey Levine, Hanchen Wang, Aviv Regev
[arXiv:2410.13643](https://arxiv.org/abs/2410.13643) • [code](https://github.com/ChenyuWang-Monica/DRAKES)

**Reinforcement learning on structure-conditioned categorical diffusion for protein inverse folding**
Yasha Ektefaie, Olivia Viessmann, Siddharth Narayanan, Drew Dresser, J. Mark Kim, Armen Mkrtchyan
[arXiv:2410.17173](https://arxiv.org/abs/2410.17173) • [code](https://github.com/flagshippioneering/pi-rldif)

**ProtInvTree: Deliberate Protein Inverse Folding with Reward-guided Tree Search**  
Mengdi Liu, Xiaoxue Cheng, Zhangyang Gao, Hong Chang, Cheng Tan, Shiguang Shan, Xilin Chen  
[arXiv:2506.00925](https://arxiv.org/abs/2506.00925)

**ProteinZero: Self-Improving Protein Generation via Online Reinforcement Learning**  
Ziwen Wang, Jiajun Fan, Ruihan Guo, Thao Nguyen, Heng Ji, Ge Liu  
[arXiv:2506.07459](https://arxiv.org/abs/2506.07459)

### 4.13 Train-method

**Protein Inverse Folding From Structure Feedback**  
Junde Xu, Zijun Gao, Xinyi Zhou, Jie Hu, Xingyi Cheng, Le Song, Guangyong Chen, Pheng-Ann Heng, Jiezhong Qiu  
[arXiv:2506.03028](https://arxiv.org/abs/2506.03028v1)

**Improving Protein Sequence Design through Designability Preference Optimization**  
Fanglei Xue, Andrew Kubaney, Zhichun Guo, Joseph K. Min, Ge Liu, Yi Yang, David Baker
[arXiv:2506.00297](https://arxiv.org/abs/2506.00297) • LigandMPNN-based

**EnerBridge-DPO: Energy-Guided Protein Inverse Folding with Markov Bridges and Direct Preference Optimization**  
Dingyi Rong, Haotian Lu, Wenzhuo Zheng, Fan Zhang, Shuangjia Zheng, Ning Liu  
[arXiv:2506.09496](https://arxiv.org/abs/2506.09496) • [code](https://github.com/DeepGraphLearning/EnerBridge-DPO)

**Attribution assignment for deep-generative sequence models enables interpretability analysis using positive-only data**  
Robert Frank, Michael Widrich, Rahmad Akbar, Günter Klambauer, Geir Kjetil Sandve, Philippe A. Robert, Victor Greiff  
[arXiv:2506.23182](https://arxiv.org/abs/2506.23182)

## 5.Function to Sequence

> These models generate sequences from expected function.

### 5.1 CNN-based

**Antibody complementarity determining region design using high-capacity machine learning**
Ge Liu, Haoyang Zeng, Jonas Mueller, Brandon Carter,   Ziheng Wang, Jonas Schilz, Geraldine Horny, Michael E Birnbaum, Stefan Ewert, David K Gifford
[Bioinformatics 36.7 (2020): 2126-2133](https://academic.oup.com/bioinformatics/article/36/7/2126/5645171) • [code](https://github.com/gifford-lab/antibody-2019)

**Protein design and variant prediction using autoregressive generative models**
Jung-Eun Shin, Adam J. Riesselman, Aaron W. Kollasch, Conor McMahon, Elana Simon, Chris Sander, Aashish Manglik, Andrew C. Kruse & Debora S. Marks
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-22732-w.pdf) • [code::SeqDesign](https://github.com/debbiemarkslab/SeqDesign) • mutation effect prediction • sequence generation • April 2021

**Optimization of therapeutic antibodies by predicting antigen specificity from antibody sequence via deep learning**
Derek M. Mason, Simon Friedensohn, Cédric R. Weber, Christian Jordi, Bastian Wagner, Simon M. Meng, Roy A. Ehling, Lucia Bonati, Jan Dahinden, Pablo Gainza, Bruno E. Correia & Sai T. Reddy
[Nature Biomedical Engineering 5.6 (2021)](https://www.nature.com/articles/s41551-021-00699-9) • [code](https://github.com/dahjan/DMS_opt)

**Accelerated Engineering of ELP‐based Materials through Hybrid Biomimetic‐De Novo Predictive Molecular Design**
Timo Laakko, Antti Korkealaakso, Burcu Firatligil Yildirir, Piotr Batys, Ville Liljeström, Ari Hokkanen, Nonappa, Merja Penttilä, Anssi Laukkanen, Ali Miserez, Caj Södergård, Pezhman Mohammadi
[Advanced Materials (2024)](https://onlinelibrary.wiley.com/doi/10.1002/adma.202312299)

### 5.2 VAE-based

**Machine learning-aided design and screening of an emergent protein function in synthetic cells**
Shunshi Kohyama, Béla P. Frohn, Leon Babl & Petra Schwille
[Nature Communications 15, 2010 (2024)](https://doi.org/10.1038/s41467-024-46203-0) • [code](https://github.com/BelaFrohn/synMinE)

**Variational auto-encoding of protein sequences**
Sam Sinai, Eric Kelsic, George M. Church, Martin A. Nowak
[arXiv preprint arXiv:1712.03346 (2017)](https://arxiv.org/abs/1712.03346)

**Design by adaptive sampling**
Brookes, David H., and Jennifer Listgarten
[arXiv preprint arXiv:1810.03714 (2018)](https://arxiv.org/abs/1810.03714)

**Pepcvae: Semi-supervised targeted design of antimicrobial peptide sequences**
Payel Das, Kahini Wadhawan, Oscar Chang, Tom Sercu, Cicero Dos Santos, Matthew Riemer, Vijil Chenthamarakshan, Inkit Padhi, Aleksandra Mojsilovic
[arXiv preprint arXiv:1810.07743 (2018)](https://arxiv.org/abs/1810.07743)

**Deep generative models for T cell receptor protein sequences**
Kristian Davidsen, Branden J Olson, William S DeWitt III, Jean Feng, Elias Harkins, Philip Bradley, Frederick A Matsen IV
[Elife 8 (2019)](https://elifesciences.org/articles/46935)

**How to hallucinate functional proteins**
Costello, Zak, and Hector Garcia Martin
[arXiv preprint arXiv:1903.00458 (2019)](https://arxiv.org/abs/1903.00458)

**Convergent selection in antibody repertoires is revealed by deep learning**
Simon Friedensohn, Daniel Neumeier, Tarik A Khan, Lucia Csepregi, Cristina Parola, Arthur R Gorter de Vries, Lena Erlach, Derek M Mason, Sai T Reddy
[BioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.02.25.965673v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2020/02/26/2020.02.25.965673/DC1/embed/media-1.pdf) • code available after publication

**Variational autoencoder for generation of antimicrobial peptides**
Dean, Scott N., and Scott A. Walper
[ACS omega 5.33 (2020)](https://pubs.acs.org/doi/abs/10.1021/acsomega.0c00442)

**Generating functional protein variants with variational autoencoders**
Alex Hawkins-Hooker, Florence Depardieu, Sebastien Baur, Guillaume Couairon, Arthur Chen, David Bikard
[PLoS computational biology 17.2 (2021)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008736)

**Accelerated antimicrobial discovery via deep generative models and molecular dynamics simulations**
Payel Das, Tom Sercu, Kahini Wadhawan, Inkit Padhi, Sebastian Gehrmann, Flaviu Cipcigan, Vijil Chenthamarakshan, Hendrik Strobelt, Cicero dos Santos, Pin-Yu Chen, Yi Yan Yang, Jeremy P. K. Tan, James Hedrick, Jason Crain & Aleksandra Mojsilovic
[Nature Biomedical Engineering 5.6 (2021)](https://www.nature.com/articles/s41551-021-00689-x)

**Deep generative models create new and diverse protein structures**
Zeming, Tom, Yann and Alexander
[NeurIPS 2021](https://www.mlsb.io/papers_2021/MLSB2021_Deep_generative_models_create.pdf)

**PepVAE: variational autoencoder framework for antimicrobial peptide generation and activity prediction**
Scott N. Dean, Jerome Anthony E. Alvarez, Dan Zabetakis, Scott A. Walper, and Anthony P. Malanoski
[Frontiers in microbiology 12 (2021)](https://www.frontiersin.org/articles/10.3389/fmicb.2021.725727/full) • [code](https://github.com/zswitten/Antimicrobial-Peptides) • [Supplementary](https://www.frontiersin.org/articles/10.3389/fmicb.2021.725727/full#supplementary-material)

**HydrAMP: a deep generative model for antimicrobial peptide discovery**
Paulina Szymczak, Marcin Możejko, Tomasz Grzegorzek, Marta Bauer, Damian Neubauer, Michał Michalski, Jacek Sroka, Piotr Setny, Wojciech Kamysz, Ewa Szczurek
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.01.27.478054v2) • [code](https://github.com/szczurek-lab/hydramp)

**Therapeutic enzyme engineering using a generative neural network**
Andrew Giessel, Athanasios Dousis, Kanchana Ravichandran, Kevin Smith, Sreyoshi Sur, Iain McFadyen, Wei Zheng & Stuart Licht
[Scientific Reports 12.1 (2022)](https://www.nature.com/articles/s41598-022-05195-x)

**GM-Pep: A High Efficiency Strategy to De Novo Design Functional Peptide Sequences**
Qushuo Chen, Changyan Yang, Yihao Xie, Yuqiang Wang, Xiaoxu Li, Kairong Wang, Jinqi Huang, and Wenjin Yan
[Journal of Chemical Information and Modeling (2022)](https://pubs.acs.org/doi/10.1021/acs.jcim.2c00089) • [code](https://github.com/TimothyChen225/GM-Pep)

**Mean Dimension of Generative Models for Protein Sequences**
Christoph Feinauer, Emanuele Borgonovo
[bioRxiv 2022.12.12.520028](https://www.biorxiv.org/content/10.1101/2022.12.12.520028v1) • [code](https://github.com/christophfeinauer/ProteinMeanDimension)

**Prediction of designer-recombinases for DNA editing with generative deep learning**
Lukas Theo Schmitt, Maciej Paszkowski-Rogacz, Florian Jug & Frank Buchholz
[Nat Commun 13, 7966 (2022)](https://www.nature.com/articles/s41467-022-35614-6) • [code](https://github.com/ltschmitt/RecGen) • [Supplementary](https://static-content.springer.com/esm/art%3A10.1038%2Fs41467-022-35614-6/MediaObjects/41467_2022_35614_MOESM1_ESM.pdf)

**ProT-VAE: Protein Transformer Variational AutoEncoder for Functional Protein Design**
Emre Sevgen, Joshua Moller, Adrian Lange, John Parker, Sean Quigley, Jeff Mayer, Poonam Srivastava, Sitaram Gayatri, David Hosfield, Maria Korshunova, Micha Livne, Michelle Gill, Rama Ranganathan, Anthony B Costa, Andrew L Ferguson
[bioRxiv 2023.01.23.525232](https://www.biorxiv.org/content/10.1101/2023.01.23.525232v1)

**Target specific peptide design using latent space approximate trajectory collector**
Tong Lin, Sijie Chen, Ruchira Basu, Dehu Pei, Xiaolin Cheng, Levent Burak Kara
[arXiv:2302.01435](https://arxiv.org/abs/2302.01435)

**Deep-learning generative models enable design of synthetic orthologs of a signaling protein**
Xinran Lian, Niksa Praljak, Andrew L. Ferguson, Rama Ranganathan
[Biophysical Journal 122.3 (2023): 311a](https://www.cell.com/biophysj/fulltext/S0006-3495(22)02664-9)

**Designing a protein with emergent function by combined in silico, in vitro and in vivo screening**
Shunshi Kohyama, Bela Paul Frohn, Leon Babl, Petra Schwille
[bioRxiv 2023.02.16.528840](https://www.biorxiv.org/content/10.1101/2023.02.16.528840v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/02/19/2023.02.16.528840/DC1/embed/media-1.pdf)

**ProteinVAE: Variational AutoEncoder for Translational Protein Design**
Suyue Lyu, Shahin Sowlati-Hashjin, Michael Garton
[bioRxiv 2023.03.04.531110](https://www.biorxiv.org/content/10.1101/2023.03.04.531110v1)/[Nat Mach Intell (2024)](https://www.nature.com/articles/s42256-023-00787-2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/03/05/2023.03.04.531110/DC1/embed/media-1.pdf) • [code](https://huggingface.co/Rostlab/prot_bert)

**ProtWave-VAE: Integrating autoregressive sampling with latent-based inference for data-driven protein design**
Niksa Praljak, Xinran Lian, Rama Ranganathan, Andrew Ferguson
[bioRxiv 2023.04.23.537971](https://www.biorxiv.org/content/10.1101/2023.04.23.537971v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/04/23/2023.04.23.537971/DC1/embed/media-1.pdf) • [code](https://github.com/PraljakReps/ProtWaveVAE)

**Designing meaningful continuous representations of T cell receptor sequences with deep generative models**
Allen Y. Leary, Darius Scott, Namita T. Gupta, Janelle C. Waite, Dimitris Skokos, Gurinder S. Atwal, Peter G. Hawkins
[bioRxiv 2023.06.17.545423](https://www.biorxiv.org/content/10.1101/2023.06.17.545423v1) • [code](https://github.com/peterghawkins-regn/tcrvalid)

**Utility of language model and physics-based approaches in modifying MHC Class-I immune-visibility for the design of vaccines and therapeutics**
Hans-Christof Gasser, Diego Oyarzun, Ajitha Rajan, Javier Alfaro
[bioRxiv 2023.07.10.548300](https://www.biorxiv.org/content/10.1101/2023.07.10.548300v1)

**Cell-free biosynthesis combined with deep learning accelerates de novo-development of antimicrobial peptides**
Amir Pandi, David Adam, Amir Zare, Van Tuan Trinh, Stefan L. Schaefer, Marie Burt, Björn Klabunde, Elizaveta Bobkova, Manish Kushwaha, Yeganeh Foroughijabbari, Peter Braun, Christoph Spahn, Christian Preußer, Elke Pogge von Strandmann, Helge B. Bode, Heiner von Buttlar, Wilhelm Bertrams, Anna Lena Jung, Frank Abendroth, Bernd Schmeck, Gerhard Hummer, Olalla Vázquez & Tobias J. Erb
[Nature Communications 14.1 (2023)](https://www.nature.com/articles/s41467-023-42434-9) • [code](https://github.com/amirpandi/Deep_AMP)

**Design of target specific peptide inhibitors using generative deep learning and molecular dynamics simulations**
Sijie Chen, Tong Lin, Ruchira Basu, Jeremy Ritchey, Shen Wang, Yichuan Luo, Xingcan Li, Dehua Pei, Levent Burak Kara & Xiaolin Cheng
[Nat Commun 15, 1611 (2024)](https://www.nature.com/articles/s41467-024-45766-2) • [code](https://doi.org/10.5281/zenodo.10587692)

**Deep-learning-based design of synthetic orthologs of SH3 signaling domains**
Xinran Lian, Nikša Praljak, Subu K. Subramanian, Sarah Wasinger, Rama Ranganathan, Andrew L. Ferguson
[Cell Systems (2024)](https://www.cell.com/cell-systems/abstract/S2405-4712(24)00204-7)

**CMADiff: Cross-Modal Aligned Diffusion for Controllable Protein Generation**  
Changjian Zhou, Yuexi Qiu, Tongtong Ling, Jiafeng Li, Shuanghe Liu, Xiangjing Wang, Jia Song, Wensheng Xiang  
[arXiv:2503.21450](https://arxiv.org/abs/2503.21450) • [code](https://github.com/HPC-NEAU/PhysChemDiff)

**Efficient Design of Affilin® Protein Binders for HER3**
Anna Maria Díaz-Rovira, Jonathan Lotze, Gregor Hoffmann, Chiara Pallara, Alexis Molina, Ina Coburger, Manja Gloser-Bräunig, Maren Meysing, Madlen Zwarg, Lucía Díaz, Victor Guallar, Eva Bosse-Doenecke, Sergi Roda
[bioRxiv 2025.04.02.646551](https://www.biorxiv.org/content/10.1101/2025.04.02.646551v1) • [code](https://github.com/annadiarov/ProtVAE) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/04/02/2025.04.02.646551/DC1/embed/media-1.pdf)

### 5.3 GAN-based

**Feedback GAN for DNA optimizes protein functions**
Gupta, Anvita, and James Zou
[Nature Machine Intelligence 1.2 (2019)](https://www.nature.com/articles/s42256-019-0017-4) • [code](https://github.com/av1659/fbgan)

**Generating protein sequences from antibiotic resistance genes data using Generative Adversarial Networks**
Chhibbar, Prabal, and Arpit Joshi
[arXiv preprint arXiv:1904.13240 (2019)](https://arxiv.org/abs/1904.13240)

**ProGAN: Protein solubility generative adversarial nets for data augmentation in DNN framework**
Xi Han, Liheng Zhang, Kang Zhou, Xiaonan Wang
[Computers &amp; Chemical Engineering 131 (2019)](https://www.sciencedirect.com/science/article/abs/pii/S0098135419304922)

**GANDALF: Peptide Generation for Drug Design using Sequential and Structural Generative Adversarial Networks**
Rossetto, Allison, and Wenjin Zhou
[Proceedings of the 11th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2020](https://dl.acm.org/doi/abs/10.1145/3388440.3412487)

**Designing feature-controlled humanoid antibody discovery libraries using generative adversarial networks**
Tileli Amimeur, Jeremy M. Shaver, Randal R. Ketchem, J. Alex Taylor, Rutilio H. Clark, Josh Smith, Danielle Van Citters, Christine C. Siska, Pauline Smidt, Megan Sprague, Bruce A. Kerwin, Dean Pettit
[BioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.04.12.024844v2)

**Generating ampicillin-level antimicrobial peptides with activity-aware generative adversarial networks**
Andrejs Tucs, Duy Phuoc Tran, Akiko Yumoto, Yoshihiro Ito, Takanori Uzawa, and Koji Tsuda
[ACS omega 5.36 (2020)](https://pubs.acs.org/doi/10.1021/acsomega.0c02088) • [code](https://github.com/tsudalab/PepGAN)

**Conditional Generative Modeling for De Novo Protein Design with Hierarchical Functions**
Kucera, Tim, Matteo Togninalli, and Laetitia Meng-Papaxanthos
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.11.10.467885v1)/[Bioinformatics 38.13 (2022)](https://academic.oup.com/bioinformatics/article/38/13/3454/6593486) • [code](https://github.com/timkucera/proteogan)

**Expanding functional protein sequence spaces using generative adversarial networks**
Donatas Repecka, Vykintas Jauniskis, Laurynas Karpus, Elzbieta Rembeza, Irmantas Rokaitis, Jan Zrimec, Simona Poviloniene, Audrius Laurynenas, Sandra Viknander, Wissam Abuajwa, Otto Savolainen, Rolandas Meskys, Martin K. M. Engqvist & Aleksej Zelezniak
[Nature Machine Intelligence 3.4 (2021)](https://www.nature.com/articles/s42256-021-00310-5) • [code](https://github.com/Biomatter-Designs/ProteinGAN)

**A Generative Approach toward Precision Antimicrobial Peptide Design.**
Jonathon B. Ferrell, Jacob M. Remington, Colin M. Van Oort, Mona Sharafi, Reem Aboushousha, Yvonne Janssen-Heininger, Severin T. Schneebeli, Matthew J. Wargo, Safwan Wshah, Jianing Li
[BioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2020.10.02.324087v2) • [code](https://gitlab.com/vail-uvm/amp-gan/-/tree/test_samples/)

**AMPGAN v2: Machine Learning-Guided Design of Antimicrobial Peptides**
Colin M. Van Oort, Jonathon B. Ferrell, Jacob M. Remington, Safwan Wshah, and Jianing Li
[Journal of chemical information and modeling 61.5 (2021)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.0c01441)

**DeepImmuno: deep learning-empowered prediction and generation of immunogenic peptides for T-cell immunity**
Guangyuan Li, Balaji Iyer, V B Surya Prasath, Yizhao Ni, Nathan Salomonis
[Briefings in bioinformatics 22.6 (2021)](https://academic.oup.com/bib/article-abstract/22/6/bbab160/6261914) • [code](https://github.com/frankligy/DeepImmuno) • [web](https://deepimmuno.research.cchmc.org/)

**PandoraGAN: Generating antiviral peptides using Generative Adversarial Network**
Shraddha Surana, Pooja Arora, Divye Singh, Deepti Sahasrabuddhe, Jayaraman Valadi
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.02.15.431193v2)

**Feedback-AVPGAN: Feedback-guided generative adversarial network for generating antiviral peptides**
Kano Hasegawa, Yoshitaka Moriwaki, Tohru Terada, Cao Wei, and Kentaro Shimizu
[Journal of Bioinformatics and Computational Biology (2022)](https://www.worldscientific.com/doi/10.1142/S0219720022500263) • [code](https://github.com/KanoHase/AVP-Generator)

**Designing antimicrobial peptides using deep learning and molecular dynamic simulations**
Qiushi Cao, Cheng Ge, Xuejie Wang, Peta J Harvey, Zixuan Zhang, Yuan Ma, Xianghong Wang, Xinying Jia, Mehdi Mobli, David J Craik, Tao Jiang, Jinbo Yang, Zhiqiang Wei, Yan Wang, Shan Chang, Rilei Yu
[Briefings in Bioinformatics (2023)](https://academic.oup.com/bib/article-abstract/24/2/bbad058/7066348)

**Generative β-Hairpin Design Using a Residue-Based Physicochemical Property Landscape**
Vardhan Satalkar and Gemechis D. Degaga and Wei Li and Yui Tik Pang and Andrew C. McShan and James C. Gumbart and Julie C. Mitchell and Matthew P. Torres
[Biophysical Journal(2024)](https://www.sciencedirect.com/science/article/pii/S0006349524000705) • [code](https://github.com/juliecmitchell/beGAN)

**De Novo Antimicrobial Peptide Design with Feedback Generative Adversarial Networks**
Michaela Areti Zervou, Effrosyni Doutsi, Yannis Pantazis, Panagiotis Tsakalides
[International Journal of Molecular Sciences 25.10 (2024)](https://www.mdpi.com/1422-0067/25/10/5506) • [code](https://github.com/aretiz/de_novo_design_GAN)

**Binary Discriminator Facilitates GPT-based Protein Design**
Zishuo Zeng, Rufang Xu, Jin Guo, Xiaozhou Luo
[bioRxiv 2023.11.20.567789](https://www.biorxiv.org/content/10.1101/2023.11.20.567789v3) • [code](https://github.com/zishuozeng/GPT_protein_design) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/12/21/2023.11.20.567789/DC1/embed/media-1.xlsx)

### 5.4 Transformer-based

> Including protein large language models(pLLM) and autoregressive language models.

**Progen: Language modeling for protein generation** / **Large language models generate functional protein sequences across diverse families**
Ali Madani, Bryan McCann, Nikhil Naik, Nitish Shirish Keskar, Namrata Anand, Raphael R. Eguchi, Po-Ssu Huang, Richard Socher
[arXiv preprint arXiv:2004.03497 (2020)](https://arxiv.org/abs/2004.03497)/[Nat Biotechnol (2023)](https://www.nature.com/articles/s41587-022-01618-2) • [ProGen](https://github.com/salesforce/progen), [CTRL](https://github.com/salesforce/ctrl)

**Signal peptides generated by attention-based neural networks**
Zachary Wu, Kevin K. Yang, Michael J. Liszka, Alycia Lee, Alina Batzilla, David Wernick, David P. Weiner, and Frances H. Arnold
[ACS Synthetic Biology 9.8 (2020)](https://pubs.acs.org/doi/full/10.1021/acssynbio.0c00219)

**ProtTrans: towards cracking the language of Life's code through self-supervised deep learning and high performance computing**
Ahmed Elnaggar, Michael Heinzinger, Christian Dallago, Ghalia Rehawi, Yu Wang, Llion Jones, Tom Gibbs, Tamas Feher, Christoph Angerer, Martin Steinegger,Debsindhu Bhowmik, and Burkhard Rost
[arXiv preprint arXiv:2007.06225 (2020)](https://ieeexplore.ieee.org/document/9477085) • [code](https://github.com/agemagician/ProtTrans)

**Generative Language Modeling for Antibody Design**
Shuai, Richard W., Jeffrey A. Ruffolo, and Jeffrey J. Gray
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.12.13.472419v2)/[Cell Systems](https://www.cell.com/cell-systems/pdf/S2405-4712(23)00271-5.pdf) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/12/20/2021.12.13.472419/DC1/embed/media-1.pdf) • [code](https://github.com/Graylab/IgLM)

**Deep neural language modeling enables functional protein generation across families**
Ali Madani, Ben Krause, Eric R. Greene, Subu Subramanian, Benjamin P. Mohr, James M. Holton, Jose Luis Olmos Jr., Caiming Xiong, Zachary Z. Sun, Richard Socher, James S. Fraser, Nikhil Naik
[bioRxiv (2021)](https://www.biorxiv.org/content/10.1101/2021.07.18.452833v1)

**Protein sequence sampling and prediction from structural data**
Gabriel A. Orellana, Javier Caceres-Delpiano, Roberto Ibañez, Michael P. Dunne, Leonardo Alvarez
[bioRxiv 2021.09.06.459171](https://www.biorxiv.org/content/10.1101/2021.09.06.459171v3)

**Transformer-based protein generation with regularized latent space optimization**
Egbert Castro, Abhinav Godavarthi, Julian Rubinfien, Kevin Givechian, Dhananjay Bhaskar & Smita Krishnaswamy
[Nat Mach Intell (2022)](https://www.nature.com/articles/s42256-022-00532-1)/[arXiv:2201.09948](https://arxiv.org/abs/2201.09948) • [code](https://github.com/KrishnaswamyLab/ReLSO-Guided-Generative-Protein-Design-using-Regularized-Transformers)

**BioPhi: A platform for antibody design, humanization, and humanness evaluation based on natural antibody repertoires and deep learning**
David Prihoda, Jad Maamary, Andrew Waight, Veronica Juan, Laurence Fayadat-Dilman, Daniel Svozil, Danny A. Bitton
[mAbs. Vol. 14. No. 1. Taylor &amp; Francis, 2022](https://www.tandfonline.com/doi/full/10.1080/19420862.2021.2020203)

**Guided Generative Protein Design using Regularized Transformers**
Egbert Castro, Abhinav Godavarthi, Julian Rubinfien, Kevin B. Givechian, Dhananjay Bhaskar, Smita Krishnaswamy
[arXiv preprint arXiv:2201.09948 (2022)](https://arxiv.org/abs/2201.09948)

**Towards Controllable Protein design with Conditional Transformers**
Noelia Ferruz, Birte Höcker
[arXiv preprint arXiv:2201.07338 (2022)](https://arxiv.org/abs/2201.07338)/[Nature Machine Intelligence (2022)](https://www.nature.com/articles/s42256-022-00499-z) • review of [Heading 5.4](#54-transformer-based)

**ProteinBERT: a universal deep-learning model of protein sequence and function**  
Nadav Brandes, Dan Ofer, Yam Peleg, Nadav Rappoport, Michal Linial  
[Bioinformatics, March 2022](https://academic.oup.com/bioinformatics/article/38/8/2102/6502274) • [code](https://github.com/nadavbra/protein_bert)

**ProtGPT2 is a deep unsupervised language model for protein design**
Noelia Ferruz,  View ProfileSteffen Schmidt,  View ProfileBirte Höcker
[bioRxiv](https://www.biorxiv.org/content/10.1101/2022.03.09.483666v1.full)/[Nature Communications](https://www.nature.com/articles/s41467-022-32007-7) • [model::huggingface](https://huggingface.co/nferruz/ProtGPT2) [datasets::hugingface](https://huggingface.co/datasets/nferruz/UR50_2021_04) • [lecture](https://www.youtube.com/watch?v=BA5C0kLcErM) • [research highlights](https://www.nature.com/articles/s41587-022-01518-5) • [news](https://cen.acs.org/physical-chemistry/protein-folding/Generative-AI-dreaming-new-proteins/101/i12#)

**Few Shot Protein Generation**
Ram, Soumya, and Tristan Bepler
[arXiv preprint arXiv:2204.01168 (2022)](https://arxiv.org/abs/2204.01168)

**RITA: a Study on Scaling Up Generative Protein Sequence Models**
Daniel Hesslow, Niccoló Zanichelli, Pascal Notin, Iacopo Poli, Debora Marks
[arXiv preprint arXiv:2205.05789 (2022)](https://arxiv.org/abs/2205.05789) • [code](https://huggingface.co/lightonai/RITA_xl)

**ProGen2: Exploring the Boundaries of Protein Language Models**
Erik Nijkamp, Jeffrey Ruffolo, Eli N. Weinstein, Nikhil Naik, Ali Madani
[arXiv:2206.13517](https://arxiv.org/abs/2206.13517) • [code](https://github.com/salesforce/progen) • [guide](https://github.com/ZeeSid/BioLM_Tutes/tree/main)

**AbLang: an antibody language model for completing antibody sequences**
Tobias H Olsen, Iain H Moal, Charlotte M Deane
[Bioinformatics Advances, Volume 2, Issue 1, 2022, vbac046](https://academic.oup.com/bioinformaticsadvances/article/2/1/vbac046/6609807)

**Reprogramming Pretrained Language Models for Antibody Sequence Infilling**
Igor Melnyk, Vijil Chenthamarakshan, Pin-Yu Chen, Payel Das, Amit Dhurandhar, Inkit Padhi, Devleena Das
[arXiv:2210.07144](https://arxiv.org/abs/2210.07144) • [code](https://github.com/IBM/ReprogBERT)

**AbBERT: Learning Antibody Humanness via Masked Language Modeling**
Denis Vashchenko, Sam Nguyen, Andre Goncalves, Felipe Leno da Silva, Brenden Petersen, Thomas Desautels, Daniel Faissol
[bioRxiv 2022.08.02.502236](https://doi.org/10.1101/2022.08.02.502236)

**Accelerating Antibody Design with Active Learning**
Seung-woo Seo, Min Woo Kwak, Eunji Kang, Chaeun Kim, Eunyoung Park, Tae Hyun Kang, Jinhan Kim
[bioRxiv 2022.09.12.507690](https://www.biorxiv.org/content/10.1101/2022.09.12.507690v1)

**Reprogramming Large Pretrained Language Models for Antibody Sequence Infilling**
Igor Melnyk, Vijil Chenthamarakshan, Pin-Yu Chen, Payel Das, Amit Dhurandhar, Inkit Padhi, Devleena Das
[ICLR 2023](https://openreview.net/forum?id=axFCgjTKP45)/[arXiv:2210.07144](https://arxiv.org/abs/2210.07144)

**Machine Learning Optimization of Candidate Antibodies Yields Highly Diverse Sub-nanomolar Affinity Antibody Libraries**
Lin Li, Esther Gupta, John Spaeth, Leslie Shing, Rafael Jaimes, Rajmonda Sulo Caceres, Tristan Bepler, Matthew E. Walsh
[bioRxiv 2022.10.07.502662](https://www.biorxiv.org/content/10.1101/2022.10.07.502662v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/10/07/2022.10.07.502662/DC1/embed/media-1.pdf) • code will be available

**ZymCTRL: a conditional language model for the contollable generation of artificial enzymes**
Noelia Ferruz
[NeurIPS 2022](https://www.mlsb.io/papers_2022/ZymCTRL_a_conditional_language_model_for_the_controllable_generation_of_artificial_enzymes.pdf)/[bioRxiv 2024.05.03.592223](https://www.biorxiv.org/content/10.1101/2024.05.03.592223v1) • [hugging face](https://huggingface.co/nferruz/ZymCTRL) • [poster](https://nips.cc/media/PosterPDFs/NeurIPS%202022/59047.png?t=1669864213.082831)

**Generative Antibody Design for Complementary Chain Pairing Sequences through Encoder-Decoder Language Model**
Chu, Simon, and Kathy Wei
[NeurIPS 2023 Generative AI and Biology (GenBio) Workshop. 2023](https://openreview.net/forum?id=QrH4bhWhwY)/[arXiv:2301.02748](https://arxiv.org/abs/2301.02748)

**Unlocking de novo antibody design with generative artificial intelligence**
Amir Shanehsazzadeh, Matt McPartlon, George Kasun, Andrea K. Steiger, John M. Sutton, Edriss Yassine, Cailen McCloskey, Robel Haile, Richard Shuai, Julian Alverio, Goran Rakocevic, Simon Levine, Jovan Cejovic, Jahir M. Gutierrez, Alex Morehead, Oleksii Dubrovskyi, Chelsea Chung, Breanna K. Luton, Nicolas Diaz, Christa Kohnert, Rebecca Consbruck, Hayley Carter, Chase LaCombe, Itti Bist, Phetsamay Vilaychack, Zahra Anderson, Lichen Xiu, Paul Bringas, Kimberly Alarcon, Bailey Knight, Macey Radach, Katherine Bateman, Gaelin Kopec-Belliveau, Dalton Chapman, Joshua Bennett, Abigail B. Ventura, Gustavo M. Canales, Muttappa Gowda, Kerianne A. Jackson, Rodante Caguiat, Amber Brown, Douglas Ganini da Silva, Zheyuan Guo, Shaheed Abdulhaqq, Lillian R. Klug, Miles Gander, Engin Yapici, Joshua Meier, Sharrol Bachas
[bioRxiv (2023): 2023-01](https://www.biorxiv.org/content/10.1101/2023.01.08.523187v4) • [data](https://github.com/AbSciBio/unlocking-de-novo-antibody-design) • [news](https://www.genengnews.com/topics/drug-discovery/antibodies/absci-eyes-ind-for-platforms-first-de-novo-antibody-within-two-years/) • [blog](https://www.science.org/content/blog-post/computing-our-way-antibodies) • commercial

**A universal deep-learning model for zinc finger design enables transcription factor reprogramming**
David M. Ichikawa, Osama Abdin, Nader Alerasool, Manjunatha Kogenaru, April L. Mueller, Han Wen, David O. Giganti, Gregory W. Goldberg, Samantha Adams, Jeffrey M. Spencer, Rozita Razavi, Satra Nim, Hong Zheng, Courtney Gionco, Finnegan T. Clark, Alexey Strokach, Timothy R. Hughes, Timothee Lionnet, Mikko Taipale, Philip M. Kim & Marcus B. Noyes
[Nat Biotechnol (2023)](https://www.nature.com/articles/s41587-022-01624-4)

**XuperNovo®/ProteinGPT**
XtalPi
[news](https://mp.weixin.qq.com/s?__biz=MzI4MzUwNjI5OQ==&mid=2247499137&sn=d8c9e006cdb131dcf5639db6824bb0e3&chksm=eb8b1e95dcfc97835268d9e66636e63a4c6eb2f6fde780a4d45180872ea8d79bbd1d29363aff) • [news2](https://mp.weixin.qq.com/s/h_mpZXnQQ_o8vSWzXl3wcQ) • [website](https://www.xtalpi.com/en/macromolecular-drug-discovery) • commercial

**Evaluating Prompt Tuning for Conditional Protein Sequence Generation**
Andrea Nathansen, Kevin Klein, Bernhard Y. Renard, Melania Nowicka, Jakub M. Bartoszewicz
[bioRxiv 2023.02.28.530492](https://www.biorxiv.org/content/10.1101/2023.02.28.530492v1) • [code](https://gitlab.com/dacs-hpi/protein-prompt-tuning)

**AB-Gen: Antibody Library Design with Generative Pre-trained Transformer and Deep Reinforcement Learning**
Xiaopeng Xu, Tiantian Xu, Juexiao Zhou, Xingyu Liao, Ruochi Zhang, Yu Wang, Lu Zhang, Xin Gao
[bioRxiv 2023.03.17.533102](https://www.biorxiv.org/content/10.1101/2023.03.17.533102v1) • [code](https://github.com/charlesxu90/ab-gen) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/03/21/2023.03.17.533102/DC1/embed/media-1.docx) • [data](https://zenodo.org/record/7657016)

**Unsupervised cross-domain translation via deep learning and adversarial attention neural networks and application to music-inspired protein designs**
Buehler, Markus J
[Patterns 4.3 (2023)](https://www.cell.com/patterns/fulltext/S2666-3899(23)00023-5) • [code](https://github.com/lamm-mit/AttentionCrossTranslation)

**ProtFIM: Fill-in-Middle Protein Sequence Design via Protein Language Models**
Lee, Youhan, and Hasun Yu
[arXiv preprint arXiv:2303.16452 (2023)](https://arxiv.org/pdf/2303.16452.pdf)/[ICLR 2023](https://openreview.net/forum?id=9XAZBUfnefS)

**REXzyme: A Translation Machine for the Generation of New-to-Nature Enzymes**
Sebastian Lindner, Michael Heinzinger, Noelia Ferruz
paper coming soon • [hugging face](https://huggingface.co/AI4PD/REXzyme)

**A generalized protein design ML model enables generation of functional de novo proteins**
Timothy P. Riley, Pourya Kalantari, Ismail Naderi, Kooshiar Azimian, Kathy Y. Wei, Oleg Matusovsky, Mohammad S. Parsa
[bioRxiv 2025.03.21.644400](https://www.biorxiv.org/content/10.1101/2025.03.21.644400v1) • [news](https://medium.com/310-ai/mpm4-ai-text2protein-breakthrough-tackles-the-molecule-programming-challenge-870045a8c1ad) • [repo](https://310.ai/mpm/repo) • commercial

**De Novo Design of Peptide Binders to Conformationally Diverse Targets with Contrastive Language Modeling**
Suhaas Bhat, Kalyan Palepu, Lauren Hong, Joey Mao, Tianzheng Ye, Rema Iyer, Lin Zhao, Tianlai Chen, Sophia Vincoff, Rio Watson, Tian Wang, Divya Srijay, Venkata Srikar Kavirayuni, Kseniia Kholina, Shrey Goel, Pranay Vure, Aniruddha H Desphande, Scott Soderling, Matthew DeLisa, Pranam Chatterjee
[bioRxiv 2023.06.26.546591](https://www.biorxiv.org/content/10.1101/2023.06.26.546591v2) • [code](https://zenodo.org/doi/10.5281/zenodo.10971077) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/07/22/2023.06.26.546591/DC1/embed/media-1.pdf)

**xTrimoPGLM: Unified 100B-Scale Pre-trained Transformer for Deciphering the Language of Protein**
Bo Chen, Xingyi Cheng, Li-ao Gengyang, Shen Li, Xin Zeng, Boyan Wang, Gong Jing, Chiming Liu, Aohan Zeng, Yuxiao Dong, Jie Tang, Le Song
[bioRxiv 2023.07.05.547496](https://www.biorxiv.org/content/10.1101/2023.07.05.547496v1)/[Nat Methods (2025)](https://www.nature.com/articles/s41592-025-02636-z) • [news](https://mp.weixin.qq.com/s/XQn8je49z23UYby8pR7fkA) • [website](https://www.biomap.com/aigp-light-beta/form) • [code](https://github.com/biomap-research/xTrimoPGLM) • [model](https://huggingface.co/biomap-research) • commercial

**TULIP - a Transformer based Unsupervised Language model for Interacting Peptides and T-cell receptors that generalizes to unseen epitopes**
Barthelemy Meynard-Piganeau, Christoph Feinauer, Martin Weigt, Aleksandra M Walczak, Thierry Mora
[bioRxiv 2023.07.19.549669](https://www.biorxiv.org/content/10.1101/2023.07.19.549669v1) • [code](https://github.com/barthelemymp/TULIP-TCR/)

**Efficient and accurate sequence generation with small-scale protein language models**
Yaiza Serrano, Sergi Roda, Victor Guallar, Alexis Molina
[bioRxiv 2023.08.04.551626](https://www.biorxiv.org/content/10.1101/2023.08.04.551626v1)

**IMPROVING ANTIBODY AFFINITY USING LABORATORY DATA WITH LANGUAGE MODEL GUIDED DESIGN**
Ben Krause, Subu Subramanian, Tom Yuan, Marisa Yang, Aaron Sato, Nikhil Naik
[bioRxiv 2023.09.13.557505](https://www.biorxiv.org/content/10.1101/2023.09.13.557505v1)

**NL2ProGPT: Taming Large Language Model for Conversational Protein Design**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=sFJr7okOBi)

**PepMLM: Target Sequence-Conditioned Generation of Peptide Binders via Masked Language Modeling**
Tianlai Chen, Sarah Pertsemlidis, Rio Watson, Venkata Srikar Kavirayuni, Ashley Hsu, Pranay Vure, Rishab Pulugurta, Sophia Vincoff, Lauren Hong, Tian Wang, Vivian Yudistyra, Elena Haarer, Lin Zhao, Pranam Chatterjee
[arXiv:2310.03842](https://arxiv.org/abs/2310.03842) • [code](https://github.com/programmablebio/pepmlm)

**De novo generation of antibody CDRH3 with a pre-trained generative large language model**
HaoHuai He, Bing He, Lei Guan, Yu Zhao, Guanxing Chen, Qingge Zhu, Calvin Yu-Chian Chen, Ting Li, Jianhua Yao
[bioRxiv 2023.10.17.562827](https://www.biorxiv.org/content/10.1101/2023.10.17.562827v1)/[Nature Communications 15.1 (2024)](https://www.nature.com/articles/s41467-024-50903-y) • [code](https://github.com/TencentAILabHealthcare/PALM) • [data](https://doi.org/10.5281/zenodo.7794583)

**SaLT&PepPr is an interface-predicting language model for designing peptide-guided protein degraders**
Garyk Brixi, Tianzheng Ye, Lauren Hong, Tian Wang, Connor Monticello, Natalia Lopez-Barbosa, Sophia Vincoff, Vivian Yudistyra, Lin Zhao, Elena Haarer, Tianlai Chen, Sarah Pertsemlidis, Kalyan Palepu, Suhaas Bhat, Jayani Christopher, Xinning Li, Tong Liu, Sue Zhang, Lillian Petersen, Matthew P. DeLisa & Pranam Chatterjee
[Commun Biol 6, 1081 (2023)](https://www.nature.com/articles/s42003-023-05464-z) • [code](https://github.com/programmablebio/saltnpeppr)

**ProteinNPT: Improving Protein Property Prediction and Design with Non-Parametric Transformers**
Pascal Notin, Ruben Weitzman, Debora S Marks, Yarin Gal
[bioRxiv 2023.12.06.570473](https://www.biorxiv.org/content/10.1101/2023.12.06.570473v1) • [code](https://github.com/OATML-Markslab/ProteinNPT)

**The promises of large language models for protein design and modeling**
Giorgio Valentini, Dario Malchiodi, Jessica Gliozzo, Marco Mesiti, Mauricio Soto-Gomez, Alberto Cabri, Justin Reese, Elena Casiraghi, and Peter N. Robinson
[Frontiers in Bioinformatics 3 (2023)](https://www.frontiersin.org/articles/10.3389/fbinf.2023.1304099/full)

**Conversational Drug Editing Using Retrieval and Domain Feedback**
Shengchao Liu, Jiongxiao Wang, Yijin Yang, Chengpeng Wang, Ling Liu, Hongyu Guo, Chaowei Xiao
[ICLR (2024)](https://openreview.net/forum?id=yRrPfKyJQ2) • [code](https://github.com/chao1224/ChatDrug) • [website](https://chao1224.github.io/ChatDrug)

**ProtAgents: Protein discovery via large language model multi-agent collaborations combining physics and machine learning**
Alireza Ghafarollahi, Markus J. Buehler
[arXiv:2402.04268](https://arxiv.org/abs/2402.04268) • [code](https://github.com/lamm-mit/ProtAgents)

**Designing proteins with language models**
Ruffolo, J.A., Madani, A
[Nat Biotechnol 42, 200–202 (2024)](https://www.nature.com/articles/s41587-024-02123-4) • review

**ProLLaMA: A Protein Large Language Model for Multi-Task Protein Language Processing**
Liuzhenghao Lv, Zongying Lin, Hao Li, Yuyang Liu, Jiaxi Cui, Calvin Yu-Chian Chen, Li Yuan, Yonghong Tian
[arXiv:2402.16445](https://arxiv.org/abs/2402.16445) • [code](https://arxiv.org/pdf/2402.16445.pdf)

**Combining machine learning with structure-based protein design to predict and engineer post-translational modifications of proteins**
Moritz Ertelt, Vikram Khipple Mulligan, Jack B. Maguire, Sergey Lyskov, Rocco Moretti, Torben Schiffner, Jens Meiler, Clara T. Schoeder
[PLOS Computational Biology 20(3): e1011939](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1011939) • [code](https://github.com/meilerlab/PTMPrediction)

**Combining Rosetta Sequence Design with Protein Language Model Predictions Using Evolutionary Scale Modeling (ESM) as Restraint**
Moritz Ertelt, Jens Meiler, and Clara T. Schoeder
[ACS Synth. Biol. 2024](https://pubs.acs.org/doi/10.1021/acssynbio.3c00753) • [code](https://github.com/meilerlab/PLM_restraint)

**Design of Antigen-Specific Antibody CDRH3 Sequences Using AI and Germline-Based Templates**
Toma M. Marinov, Alexandra A. Abu-Shmais, Alexis K. Janke, Ivelin S. Georgiev
[bioRxiv 2024.03.22.586241](https://www.biorxiv.org/content/10.1101/2024.03.22.586241v1.full)

**Design of highly functional genome editors by modeling the universe of CRISPR-Cas sequences**
Jeffrey A. Ruffolo, Stephen Nayfach, Joseph Gallagher, Aadyot Bhatnagar, Joel Beazer, Riffat Hussain, Jordan Russ, Jennifer Yip, Emily Hill, Martin Pacesa, Alexander J. Meeske, Peter Cameron, Ali Madani
[bioRxiv 2024.04.22.590591](https://www.biorxiv.org/content/10.1101/2024.04.22.590591v1) • [code](https://github.com/Profluent-AI/OpenCRISPR)

**Functional Protein Design with Local Domain Alignment**
Chaohao Yuan, Songyou Li, Geyan Ye, Yikun Zhang, Long-Kai Huang, Wenbing Huang, Wei Liu, Jianhua Yao, Yu Rong
[arXiv:2404.16866](https://arxiv.org/abs/2404.16866)

**The Continuous Language of Protein Structure**
Lukas Billera, Anton Oresten, Aron Stålmarck, Kenta Sato, Mateusz Kaduk, Ben Murrell
[bioRxiv 2024.05.11.593685](https://www.biorxiv.org/content/10.1101/2024.05.11.593685v1) • [code](https://github.com/MurrellGroup/InvariantPointAttention.jl)

**Generative Enzyme Design Guided by Functionally Important Sites and Small-Molecule Substrates**
Zhenqiao Song, Yunlong Zhao, Wenxian Shi, Wengong Jin, Yang Yang, Lei Li
[arXiv:2405.08205](https://arxiv.org/abs/2405.08205)/[ICML 2024](https://openreview.net/pdf/b349f5504ef1e6143231064979e2e96feaf5a6a9.pdf) • [code](https://github.com/LeiLiLab/EnzyGen)

**A generative foundation model for antibody sequence understanding**
Justin Barton, Aretas Gaspariunas, David A Yadin, Jorge Dias, Francesca L Nice, Danielle H Minns, Olivia Snudden, Chelsea Povall, Sara Valle Tomas, Harry Dobson, James HR Farmery, Jinwoo Leem, Jacob D Galson
[bioRxiv 2024.05.22.594943](https://www.biorxiv.org/content/10.1101/2024.05.22.594943v1) • [huggingface](https://huggingface.co/alchemab)

**Decoupled Sequence and Structure Generation for Realistic Antibody Design**
Nayoung Kim, Minsu Kim, Sungsoo Ahn, Jinkyoo Park
[arXiv:2402.05982](https://arxiv.org/abs/2402.05982)/[Under review for TMLR](https://openreview.net/forum?id=CTkABQvnkm) • [code](https://github.com/lkny123/ASSD_public)

**Addressing the antibody germline bias and its effect on language models for improved antibody design**
Tobias H. Olsen, Iain H. Moal, Charlotte M. Deane
[bioRxiv 2024.02.02.578678](https://www.biorxiv.org/content/10.1101/2024.02.02.578678v1)/[Bioinformatics (2024): btae618](https://academic.oup.com/bioinformatics/article/40/11/btae618/7845256) • [code](https://github.com/oxpig/AbLang2)

**MoFormer: Multi-objective Antimicrobial Peptide Generation Based on Conditional Transformer Joint Multi-modal Fusion Descriptor**
Li Wang, Xiangzheng Fu, Jiahao Yang, Xinyi Zhang, Xiucai Ye, Yiping Liu, Tetsuya Sakurai, Xiangxiang Zeng
[arXiv:2406.00735](https://arxiv.org/abs/2406.02610)

**HELM-GPT: de novo macrocyclic peptide design using generative pre-trained transformer**
Xiaopeng Xu, Chencheng Xu, Wenjia He, Lesong Wei, Haoyang Li, Juexiao Zhou, Ruochi Zhang, Yu Wang, Yuanpeng Xiong, Xin Gao
[Bioinformatics (2024): btae364](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btae364/7691994) • [code](https://github.com/charlesxu90/helm-gpt)

**Unifying Sequences, Structures, and Descriptions for Any-to-Any Protein Generation with the Large Multimodal Model HelixProtX**
Zhiyuan Chen, Tianhao Chen, Chenggang Xie, Yang Xue, Xiaonan Zhang, Jingbo Zhou, Xiaomin Fang
[arXiv:2407.09274](https://arxiv.org/abs/2407.09274) • [code](https://github.com/PaddlePaddle/PaddleHelix/tree/dev/apps/helixprotx)

**A foundation model approach to guide antimicrobial peptide design in the era of artificial intelligence driven scientific discovery**
Jike Wang, Jianwen Feng, Yu Kang, Peichen Pan, Jingxuan Ge, Yan Wang, Mingyang Wang, Zhenxing Wu, Xingcai Zhang, Jiameng Yu, Xujun Zhang, Tianyue Wang, Lirong Wen, Guangning Yan, Yafeng Deng, Hui Shi, Chang-Yu Hsieh, Zhihui Jiang, Tingjun Hou
[arXiv:2407.12296](https://arxiv.org/abs/2407.12296) • [code](https://github.com/jkwang93/AMP-Designer)

**Conditional Sequence-Structure Integration: A Novel Approach for Precision Antibody Engineering and Affinity Optimization**
Benyamin Jamialahmadi, Mahmood Chamankhah, Mohammad Kohandel, Ali Ghodsi
[bioRxiv 2024.07.16.603820](https://www.biorxiv.org/content/10.1101/2024.07.16.603820v1) • [blog](https://simplescience.ai/en/2024-08-28-advancements-in-antibody-design-with-aida-method--an1v4d)

**moPPIt: De Novo Generation of Motif-Specific Binders with Protein Language Models**
Tong Chen, Yinuo Zhang, Pranam Chatterjee
[bioRxiv 2024.07.31.606098](https://www.biorxiv.org/content/10.1101/2024.07.31.606098v1) • [code](https://huggingface.co/ChatterjeeLab/moPPIt)

**Toward De Novo Protein Design from Natural Language**
Fengyuan Dai, Yuliang Fan, Jin Su, Chentong Wang, Chenchen Han, Xibin Zhou, Jianming Liu, Hui Qian, Shunzhi Wang, Anping Zeng, Yajie Wang, Fajie Yuan
[bioRxiv 2024.08.01.606258](https://www.biorxiv.org/content/10.1101/2024.08.01.606258v5) • [code](https://github.com/westlake-repl/Denovo-Pinal) •[demo](http://www.denovo-pinal.com/)

**Design Proteins Using Large Language Models: Enhancements and Comparative Analyses**
Kamyar Zeinalipour, Neda Jamshidi, Monica Bianchini, Marco Maggini, Marco Gori
[arXiv:2408.06396](https://arxiv.org/abs/2408.06396) • [code](https://github.com/KamyarZeinalipour/protein-design-LLMs)

**Miniaturizing, Modifying, and Augmenting Nature's Proteins with Raygun**
Kapil Devkota, Daichi Shonai, Joey Mao, Scott H Soderling, Rohit Singh
[bioRxiv 2024.08.13.607858](https://www.biorxiv.org/content/10.1101/2024.08.13.607858v1) • [code](https://github.com/rohitsinghlab/raygun)

**TourSynbio: A Multi-Modal Large Model and Agent Framework to Bridge Text and Protein Sequences for Protein Engineering**
Yiqing Shen, Zan Chen, Michail Mamalakis, Yungeng Liu, Tianbin Li, Yanzhou Su, Junjun He, Pietro Liò, Yu Guang Wang
[arXiv:2408.15299](https://arxiv.org/abs/2408.15299) • [code](https://github.com/tsynbio/TourSynbio) • [model](https://huggingface.co/tsynbio/Toursynbio) • [website](http://prdtst.tsynbio.com:51443/) • [news](https://mp.weixin.qq.com/s/IROlGdP04uLUUipNAd7YOg) • commercial

**AbGPT: De Novo Antibody Design via Generative Language Modeling**
Desmond Kuan, Amir Barati Farimani
[arXiv:2409.06090](https://arxiv.org/abs/2409.06090v1) • [code](https://github.com/deskk/AbGPT)

**PepINVENT: Generative peptide design beyond the natural amino acids**
Gökçe Geylan, Jon Paul Janet, Alessandro Tibo, Jiazhen He, Atanas Patronov, Mikhail Kabeshov, Florian David, Werngard Czechtizky, Ola Engkvist, Leonardo De Maria
[arXiv:2409.14040](https://arxiv.org/abs/2409.14040)

**Conditional Enzyme Generation Using Protein Language Models with Adapters**
Jason Yang, Aadyot Bhatnagar, Jeffrey A. Ruffolo, Ali Madani
[arXiv:2410.03634](https://arxiv.org/abs/2410.03634) • [code](https://github.com/Profluent-Internships/ProCALM)

**Re-examining Metrics for Success in Machine Learning, from Fairness and Interpretability to Protein Design**
Frances Ding
[Diss. University of California, Berkeley, 2024](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2024/EECS-2024-156.html) • Phd thesis

**Computational design of target-specific linear peptide binders with TransformerBeta**
Haowen Zhao, Francesco A. Aprile, Barbara Bravi
[arXiv:2410.16302](https://arxiv.org/abs/2410.16302) • [code](https://github.com/HZ3519/TransformerBeta_project)

**Structure Language Models for Protein Conformation Generation**
Jiarui Lu, Xiaoyin Chen, Stephen Zhewen Lu, Chence Shi, Hongyu Guo, Yoshua Bengio, Jian Tang
[arXiv:2410.18403](https://arxiv.org/abs/2410.18403) • [code](https://github.com/lujiarui/esmdiff)

**Peptide-GPT: Generative Design of Peptides using Generative Pre-trained Transformers and Bio-informatic Supervision**
Aayush Shah, Chakradhar Guntuboina, Amir Barati Farimani
[arXiv:2410.19222](https://arxiv.org/abs/2410.19222) • [code](https://github.com/aayush-shah14/PeptideGPT)

**An adaptive autoregressive diffusion approach to design active humanized antibody and nanobody**
Jian Ma, Fandi Wu, Tingyang Xu, Shaoyong Xu, Wei Liu, Divin Yan, Qifeng Bai, Jianhua Yao
[bioRxiv 2024.10.22.619416](https://www.biorxiv.org/content/10.1101/2024.10.22.619416v1) • [code](https://github.com/TencentAI4S/HuDiff)

**Concept Bottleneck Language Models For protein design**
Aya Abdelsalam Ismail, Tuomas Oikarinen, Amy Wang, Julius Adebayo, Samuel Stanton, Taylor Joren, Joseph Kleinhenz, Allen Goodman, Héctor Corrada Bravo, Kyunghyun Cho, Nathan C. Frey
[arXiv:2411.06090](https://arxiv.org/abs/2411.06090)

**De novo design of triosephosphate isomerases using generative language models**
Sergio Romero-Romero, Alexander E. Braun, Timo Kossendey, Noelia Ferruz, Steffen Schmidt, Birte Höcker
[bioRxiv 2024.11.10.622869](https://www.biorxiv.org/content/10.1101/2024.11.10.622869v1)

**Natural Language Prompts Guide the Design of Novel Functional Protein Sequences**
Nikša Praljak, Hugh Yeh, Miranda Moore, Michael Socolich, Rama Ranganathan, Andrew L. Ferguson
[bioRxiv 2024.11.11.622734](https://www.biorxiv.org/content/10.1101/2024.11.11.622734v1)

**Multi-purpose controllable protein generation via prompted language models**
Zeyuan Wang, Binbin Chen, Keyan Ding, Jiawen Cao, Ming Qin, Yadan Niu, Xiang Zhuang, Xiaotong Li, Kehua Feng, Tong Xu, Ningyu Zhang, Haoran Yu, Qiang Zhang, Huajun Chen
[bioRxiv 2024.11.17.624051](https://www.biorxiv.org/content/10.1101/2024.11.17.624051v1)

**Antiviral Peptide-Generative Pre-Trained Transformer (AVP-GPT): A Deep Learning-Powered Model for Antiviral Peptide Design with High-Throughput Discovery and Exceptional Potency**
Huajian Zhao, Gengshen Song
[Viruses 16.11 (2024)](https://www.mdpi.com/1999-4915/16/11/1673)

**Pan-protein Design Learning Enables Task-adaptive Generalization for Low-resource Enzyme Design**
Jiangbin Zheng, Ge Wang, Han Zhang, Stan Z. Li
[arXiv:2411.17795](https://arxiv.org/abs/2411.17795)

**ProtDAT: A Unified Framework for Protein Sequence Design from Any Protein Text Description**
Xiao-Yu Guo, Yi-Fan Li, Yuan Liu, Xiaoyong Pan, Hong-Bin Shen
[arXiv:2412.04069](https://arxiv.org/abs/2412.04069) • [code](https://github.com/GXY0116/ProtDAT)

**Annotation-guided Protein Design with Multi-Level Domain Alignment**
Chaohao Yuan, Songyou Li, Geyan Ye, Yikun Zhang, Long-Kai Huang, Wenbing Huang, Wei Liu, Jianhua Yao, Yu Rong
[arXiv:2404.16866](https://arxiv.org/abs/2404.16866)

**Open-Source Protein Language Models for Function Prediction and Protein Design**
Shivasankaran Vanaja Pandi, Bharath Ramsundar
[arXiv:2412.13519](https://arxiv.org/abs/2412.13519)

**Discovery and language model-guided design of hyperactive transposase**
Marc Güell, Dimitrije Ivančić, Alejandro Agudelo, Jonathan Lindstrom-Vautri, Jessica Jaraba-Wallace, Maria Gallo, Alejandro Ragel, Irene Higueras, Federico Billeci, Marta Sanvicente, Paolo Petazzi, Noelia Ferruz, Avencia Sánchez-Mejías, Ravi Das
[preprint](https://www.researchsquare.com/article/rs-5536951/v1) • [code](https://github.com/Integra-tx/Piggybac_bioprospecting_pipeline) • Progen2-based

**Generation of antigen-specific paired heavy-light chain antibody sequences using large language models**
Perry T. Wasdin, Nicole V. Johnson, Alexis K. Janke, Sofia Held, Toma M. Marinov, Gwen Jordaan, Léna Vandenabeele, Fani Pantouli, Rebecca A. Gillespie, Matthew J. Vukovich, Clinton M. Holt, Jeongryeol Kim, Grant Hansman, Jennifer Logue, Helen Y. Chu, Sarah F. Andrews, Masaru Kanekiyo, Giuseppe A. Sautto, Ted M. Ross, Daniel J. Sheward, Jason S. McLellan, Alexandra A. Abu-Shmais, Ivelin S. Georgiev
[bioRxiv 2024.12.20.629482](https://www.biorxiv.org/content/10.1101/2024.12.20.629482v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/22/2024.12.20.629482/DC1/embed/media-1.pdf)

**Controllable Protein Sequence Generation with LLM Preference Optimization**
Xiangyu Liu, Yi Liu, Silei Chen, Wei Hu
[arXiv:2501.15007](https://arxiv.org/abs/2501.15007) • [code](https://github.com/nju-websoft/CtrlProt)

**Discovery of antimicrobial peptides with notable antibacterial potency by an LLM-based foundation model**
Jike Wang, Jianwen Feng, Yu Kang, Peichen Pan, Jingxuan Ge, Yan Wang, Mingyang Wang, Zhenxing Wu, Xingcai Zhang, Jiameng Yu, Xujun Zhang, Tianyue Wang, Lirong Wen, Guangning Yan, Yafeng Deng, Hui Shi, Chang-Yu Hsieh, Zhihui Jiang, and Tingjun Hou
[Sci. Adv.11,eads8932(2025)](https://www.science.org/doi/10.1126/sciadv.ads8932) • [code](https://github.com/jkwang93/AMP-Designer)

**CasGen: A Regularized Generative Model for CRISPR Cas Protein Design with Classification and Margin-Based Optimization**
Bharani Nammi, Vindi M. Jayasinghe-Arachchige, Sita Sirisha Madugula, Maria Artiles, Charlene Norgan Radler, Tyler Pham, Jin Liu, Shouyi Wang
[bioRxiv 2025.02.28.640911](https://www.biorxiv.org/content/10.1101/2025.02.28.640911v1) • [code](https://github.com/shouyisxty/CasGen)

**Language models for protein design**
Jin Sub Lee, Osama Abdin, and Philip M. Kim
[Current Opinion in Structural Biology 92 (2025)](https://www.sciencedirect.com/science/article/abs/pii/S0959440X25000454) • review

**De Novo Design of Antigen-Specific Antibodies Using Structural Constraint-Based Generative Language Model**  
Yuran Jia, Bing He, Tianxu Lv, YangXiao, Tianyi Zhao, Jianhua Yao  
[OpenReview](https://openreview.net/forum?id=8F2JrQC2DJ)

**SOAPI: Siamese-guided generation of Off-Target-Avoiding Protein Interactions**  
Sophia Vincoff, Oscar Davis, Alexander Tong, Joey Bose, Pranam Chatterjee  
[OpenReview](https://openreview.net/forum?id=mUp7mfNfXz)

**Prot42: a Novel Family of Protein Language Models for Target-aware Protein Binder Generation**
Mohammad Amaan Sayeed, Engin Tekin, Maryam Nadeem, Nancy A. ElNaker, Aahan Singh, Natalia Vassilieva, Boulbaba Ben Amor
[arXiv:2504.04453](https://arxiv.org/abs/2504.04453) • [model](https://huggingface.co/inceptionai)

**Customizing Spider Silk: Generative Models with Mechanical Property Conditioning for Protein Engineering**
Neeru Dubey, Elin Karlsson, Miguel Angel Redondo, Johan Reimegård, Anna Rising, Hedvig Kjellström
[arXiv:2504.08437](https://arxiv.org/abs/2504.08437) • ProtGPT2-based

**A multimodal foundation model for controllable protein generation and representation learning**  
Timothy Fei Truong Jr, Tristan Bepler  
[blog](https://www.openprotein.ai/a-multimodal-foundation-model-for-controllable-protein-generation-and-representation-learning) • commercial

**Elucidating the Design Space of Multimodal Protein Language Models**
Cheng-Yen Hsieh, Xinyou Wang, Daiheng Zhang, Dongyu Xue, Fei Ye, Shujian Huang, Zaixiang Zheng, Quanquan Gu
[arXiv:2504.11454](https://arxiv.org/abs/2504.11454)

**Scaling unlocks broader generation and deeper functional understanding of proteins**
Aadyot Bhatnagar, Sarthak Jain, Joel Beazer, Samuel C Curran, Alexander M Hoffnagle, Kyle Ching, Michael Martyn, Stephen Nayfach, Jeffrey A Ruffolo, Ali Madani
[bioRxiv 2025.04.15.649055](https://www.biorxiv.org/content/10.1101/2025.04.15.649055v1) • [code](https://github.com/Profluent-AI/progen3)

**Sparks: Multi-Agent Artificial Intelligence Model Discovers Protein Design Principles**  
Alireza Ghafarollahi, Markus J. Buehler  
[arXiv:2504.19017](https://arxiv.org/abs/2504.19017) • [code](https://github.com/lamm-mit/Sparks/)

**Protein Design with Dynamic Protein Vocabulary**  
Nuowei Liu, Jiahao Kuang, Yanting Liu, Changzhi Sun, Tao Ji, Yuanbin Wu, Man Lan  
[arXiv:2505.18966](https://arxiv.org/abs/2505.18966) • [code](https://github.com/sornkL/ProDVa)

**ProtMamba: a homology-aware but alignment-free protein state space model**  
Damiano Sgarbossa, Cyril Malbranke, Anne-Florence Bitbol  
[bioRxiv 2024.05.24.595730](https://www.biorxiv.org/content/10.1101/2024.05.24.595730v4) • [code](https://github.com/Bitbol-Lab/ProtMamba)

**Natural Language Guided Ligand-Binding Protein Design**  
Zhenqiao Song, Ramith Hettiarachchi, Chuan Li, Jianwen Xie, Lei Li  
[arXiv:2506.09332](https://www.arxiv.org/abs/2506.09332)

**Toward the Explainability of Protein Language Models for Sequence Design**  
Andrea Hunklinger, Noelia Ferruz  
[arXiv:2506.19532](https://arxiv.org/abs/2506.19532)

**Metalorian: De Novo Generation of Heavy Metal-Binding Peptides with Classifier-Guided Diffusion Sampling**  
Yinuo Zhang, Divya Srijay, Zachary Quinn, Pranam Chatterjee  
[bioRxiv 2025.07.10.664242](https://www.biorxiv.org/content/10.1101/2025.07.10.664242v1) • ESM2-based

**ProteinReasoner: A Multi-Modal Protein Language Model with Chain-of-Thought Reasoning for Efficient Protein Design**  
Chaozhong Liu, Linlin Chao, Shaomin Ji, Hao Wang, Taorui Jiang, Zhangyang Gao, Yucheng Guo, Ming Yang, Xiaoming Zhang  
[bioRxiv 2025.07.21.665832](https://www.biorxiv.org/content/10.1101/2025.07.21.665832v1)

**The Dayhoff Atlas: scaling sequence diversity for improved protein generation**  
Kevin K. Yang, Sarah Alamdari, Alex J. Lee, Kaeli Kaymak-Loveless, Samir Char, Garyk Brixi, Carles Domingo-Enrich, Chentong Wang, Suyue Lyu, Nicolo Fusi, Neil Tenenholtz, Ava P. Amini  
[bioRxiv 2025.07.21.665991](https://www.biorxiv.org/content/10.1101/2025.07.21.665991v1) • [code](https://github.com/microsoft/dayhoff) • [dataset](https://huggingface.co/collections/microsoft/dayhoff-atlas-6866d679465a2685b06ee969)

**The Virtual Lab of AI agents designs new SARS-CoV-2 nanobodies**  
Kyle Swanson, Wesley Wu, Nash L. Bulaong, John E. Pak & James Zou  
[Nature (2025)](https://www.nature.com/articles/s41586-025-09442-9)

**Enhancing Safe and Controllable Protein Generation via Knowledge Preference Optimization**  
Yuhao Wang, Keyan Ding, Kehua Feng, Zeyuan Wang, Ming Qin, Xiaotong Li, Qiang Zhang, Huajun Chen  
[arXiv:2507.10923](https://arxiv.org/abs/2507.10923) • [code](https://github.com/HICAI-ZJU/KPO)

**Target sequence-conditioned design of peptide binders using masked language modeling**  
Leo Tianlai Chen, Zachary Quinn, Madeleine Dumas, Christina Peng, Lauren Hong, Moises Lopez-Gonzalez, Alexander Mestre, Rio Watson, Sophia Vincoff, Lin Zhao, Jianli Wu, Audrey Stavrand, Mayumi Schaepers-Cheu, Tian Zi Wang, Divya Srijay, Connor Monticello, Pranay Vure, Rishab Pulugurta, Sarah Pertsemlidis, Kseniia Kholina, Shrey Goel, Matthew P. DeLisa, Jen-Tsan Ashley Chi, Ray Truant, Hector C. Aguilar & Pranam Chatterjee  
[Nat Biotechnol (2025)](https://www.nature.com/articles/s41587-025-02761-2) • [code](https://github.com/programmablebio/pepmlm) • [model](https://huggingface.co/ChatterjeeLab/PepMLM-650M)

**ICEPIC: A Toolkit to Discover Ice Binding Proteins from Sequence**  
Jimmy Zhang, Subbulakshmi Suresh, Shmuel Gleizer, Sophia Ewens, Aarya Venkat, Valentin Zulkower, Thomas Biernacki, Daniel Wen, Catherine Li, Mohammed Eslami, Susan Buckhout-White  
[bioRxiv 2025.08.08.669420](https://www.biorxiv.org/content/10.1101/2025.08.08.669420v2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/08/14/2025.08.08.669420/DC1/embed/media-1.pdf) • [code](https://github.com/netrias/ICEPIC)

**Improved multimodal protein language model-driven universal biomolecules-binding protein design with EiRA**  
Wenwu Zeng, Haitao Zou, Xiaoyu Li, Xiaoqi Wang, Shaoliang Peng  
[bioRxiv 2025.09.02.673615](https://www.biorxiv.org/content/10.1101/2025.09.02.673615v1) • [code](https://github.com/pengsl-lab/EiRA)

**LSMTCR: A Scalable Multi-Architecture Model for Epitope-Specific T Cell Receptor de novo Design**  
Ruihao Zhang, Xiao Liu  
[arXiv:2509.07627](https://arxiv.org/abs/2509.07627)

### 5.5 Bayesian-based

**Optimistic Games for Combinatorial Bayesian Optimization with Applications to Protein Design**
Melis Ilayda Bal, Pier Giuseppe Sessa, Mojmir Mutny, Andreas Krause
[NeurIPS 2023 Workshop on Adaptive Experimental Design and Active Learning in the Real World, 2023](https://openreview.net/forum?id=ScOvmGz4xH)/[arXiv:2409.18582](https://arxiv.org/abs/2409.18582)

**Discovering de novo peptide substrates for enzymes using machine learning**
Lorillee Tallorin, JiaLei Wang, Woojoo E. Kim, Swagat Sahu, Nicolas M. Kosa, Pu Yang, Matthew Thompson, Michael K. Gilson, Peter I. Frazier, Michael D. Burkart & Nathan C. Gianneschi
[Nature communications 9.1 (2018)](https://www.nature.com/articles/s41467-018-07717-6) • [code](https://github.com/peter-i-frazier/pool)

**Biological Sequences Design using Batched Bayesian Optimization**
David Belanger, Suhani Vora, Zelda Mariet, Ramya Deshpande, David Dohan, Christof Angermueller, Kevin Murphy, Olivier Chapelle, Lucy Colwell
[Machine Learning and the Physical Sciences Workshop (NeurIPS 2019)](https://ml4physicalsciences.github.io/2019/files/NeurIPS_ML4PS_2019_141.pdf)

**Lattice protein design using Bayesian learning**
Takahashi, Tomoei, George Chikenji, and Kei Tokita
[arXiv:2003.06601](https://arxiv.org/abs/2003.06601)/[Physical Review E 104.1 (2021): 014404](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.104.014404)

**Now What Sequence? Pre-trained Ensembles for Bayesian Optimization of Protein Sequences**
Ziyue Yang, Katarina A Milas, Andrew D White
[bioRxiv 2022.08.05.502972](https://www.biorxiv.org/content/10.1101/2022.08.05.502972v2) • [code](https://github.com/ur-whitelab/wazy) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/08/06/2022.08.05.502972/DC1/embed/media-1.pdf) • [Colab](https://colab.research.google.com/github/ur-whitelab/wazy/blob/master/colab/WazyAlphaFold2.ipynb)

**AntBO: Towards Real-World Automated Antibody Design with Combinatorial Bayesian Optimisation**
Asif Khan, Alexander I. Cowen-Rivers, Antoine Grosnit, Derrick-Goh-Xin Deik, Philippe A. Robert, Victor Greiff, Eva Smorodina, Puneet Rawat, Kamil Dreczkowski, Rahmad Akbar, Rasul Tutunov, Dany Bou-Ammar, Jun Wang, Amos Storkey, Haitham Bou-Ammar
[arXiv preprint (2022)](https://arxiv.org/abs/2201.12570)/[Cell Reports Methods (2023): 100374](https://www.sciencedirect.com/science/article/pii/S2667237522002764)

**Accelerating Bayesian Optimization for Biological Sequence Design with Denoising Autoencoders**
Samuel Stanton, Wesley Maddox, Nate Gruver, Phillip Maffettone, Emily Delaney, Peyton Greenside, Andrew Gordon Wilson
[ICML 2022](https://arxiv.org/abs/2203.12742) • [code](https://github.com/samuelstanton/lambo)

**Statistical Mechanics of Protein Design**
Takahashi, Tomoei, George Chikenji, and Kei Tokita
[arXiv preprint arXiv:2205.03696 (2022)](https://arxiv.org/abs/2205.03696)

**PropertyDAG: Multi-objective Bayesian optimization of partially ordered, mixed-variable properties for biological sequence design**
Ji Won Park, Samuel Stanton, Saeed Saremi, Andrew Watkins, Henri Dwyer, Vladimir Gligorijevic, Richard Bonneau, Stephen Ra, Kyunghyun Cho
[arXiv:2210.04096](https://arxiv.org/abs/2210.04096)

**A probabilistic view of protein stability, conformational specificity, and design**
Jacob A. Stern, Tyler J. Free, Kimberlee L. Stern, Spencer Gardiner, Nicholas A. Dalley, Bradley C. Bundy, Joshua L. Price, David Wingate, Dennis Della Corte
[bioRxiv 2022.12.28.521825](https://www.biorxiv.org/content/10.1101/2022.12.28.521825v1)/[Scientific Reports 13.1 (2023)](https://www.nature.com/articles/s41598-023-42032-1) • [code](https://github.com/dellacortelab/bayes_design) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/12/30/2022.12.28.521825/DC1/embed/media-1.pdf)

**Design of antimicrobial peptides containing non-proteinogenic amino acids using multi-objective Bayesian optimisation**
Murakami Y, Ishida S, Demizu Y, Terayama K
[ChemRxiv. Cambridge: Cambridge Open Engage; 2023](https://chemrxiv.org/engage/chemrxiv/article-details/645f192ef2112b41e97720f3) • [code](https://github.com/ycu-iil/MODAN)

**Vaxformer: Antigenicity-controlled Transformer for Vaccine Design Against SARS-CoV-2**
Aryo Pradipta Gema, Michał Kobiela, Achille Fraisse, Ajitha Rajan, Diego A. Oyarzún, Javier Antonio Alfaro
[arXiv:2305.11194](https://arxiv.org/abs/2305.11194) • [code](https://github.com/aryopg/vaxformer)

**Sample-efficient Antibody Design through Protein Language Model for Risk-aware Batch Bayesian Optimization**
Yanzheng Wang, Boyue Wang, Tianyu Shi, Jie Fu, Yi Zhou, Zhizhuo Zhang
[bioRxiv 2023.11.06.565922](https://www.biorxiv.org/content/10.1101/2023.11.06.565922v1)

**Integrating Protein Structure Prediction and Bayesian Optimization for Peptide Design**
Negin Manshour, Fei He, Duolin Wang, Dong Xu
[NeurIPS 2023 Generative AI and Biology (GenBio) Workshop. 2023](https://openreview.net/forum?id=CsjGuWD7hk)

**Bayesian Optimisation for Protein Sequence Design: Gaussian Processes with Zero-Shot Protein Language Model Prior Mean**
Carolin Benjamins, Shikha Surana, Oliver Bent, Marius Lindauer, Paul Duckworth
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/Bayesian_Optimisation_for_Protein_Sequence_Design:_Gaussian_Processes_with_Zero-Shot_Protein_Language_Model_Prior_Mean.pdf)

**Steering Protein Family Design through Profile Bayesian Flow**
Jingjing Gong, Yu Pei, Siyu Long, Yuxuan Song, Zhe Zhang, Wenhao Huang, Ziyao Cao, Shuyi Zhang, Hao Zhou, Wei-Ying Ma
[arXiv:2502.07671](https://arxiv.org/abs/2502.07671)

**AMix-1: A Pathway to Test-Time Scalable Protein Foundation Model**  
Changze Lv, Jiang Zhou, Siyu Long, Lihao Wang, Jiangtao Feng, Dongyu Xue, Yu Pei, Hao Wang, Zherui Zhang, Yuchen Cai, Zhiqiang Gao, Ziyuan Ma, Jiakai Hu, Chaochen Gao, Jingjing Gong, Yuxuan Song, Shuyi Zhang, Xiaoqing Zheng, Deyi Xiong, Lei Bai, Wanli Ouyang, Ya-Qin Zhang, Wei-Ying Ma, Bowen Zhou, Hao Zhou  
[arXiv:2507.08920](https://arxiv.org/abs/2507.08920) • [code](https://gensi-thuair.github.io/AMix-1/)

### 5.6 RL-based

**Model-based reinforcement learning for biological sequence design**
Christof Angermueller, David Dohan, David Belanger, Ramya Deshpande, Kevin Murphy, Lucy Colwell
[International conference on learning representations. 2019](https://openreview.net/forum?id=HklxbgBKvr&fileGuid=3xgr169o12oUrbxS)

**Structured Q-learning For Antibody Design**
Alexander I. Cowen-Rivers, Philip John Gorinski, Aivar Sootla, Asif Khan, Liu Furui, Jun Wang, Jan Peters, Haitham Bou Ammar
[arXiv preprint arXiv:2209.04698 (2022)](https://arxiv.org/abs/2209.04698)

**Protein Sequence Design in a Latent Space via Model-based Reinforcement Learning**
Minji Lee, Luiz Felipe Vecchietti, Hyunkyu Jung, Hyunjoo Ro, Ho Min Kim, Meeyoung Cha
[ICLR 2023](https://openreview.net/forum?id=OhjGzRE5N6o)/[NeurIPS 2022](https://www.mlsb.io/papers_2022/Protein_Sequence_Design_in_a_Latent_Space_via_Model_based_Reinforcement_Learning.pdf) • [Supplementary](https://openreview.net/attachment?id=OhjGzRE5N6o&name=supplementary_material)

**Designing Biological Sequences via Meta-Reinforcement Learning and Bayesian Optimization**
Leo Feng, Padideh Nouri, Aneri Muni, Yoshua Bengio, Pierre-Luc Bacon
[arXiv:2209.06259](https://arxiv.org/abs/2209.06259)/[NeurIPS 2022](https://www.mlsb.io/papers_2022/Designing_Biological_Sequences_via_Meta_Reinforcement_Learning_and_Bayesian_Optimization.pdf) • [poster](https://nips.cc/media/PosterPDFs/NeurIPS%202022/58993.png?t=1669588933.2017226)

**Self-play reinforcement learning guides protein engineering**
Yi Wang, Hui Tang, Lichao Huang, Lulu Pan, Lixiang Yang, Huanming Yang, Feng Mu & Meng Yang
[Nature Machine Intelligence (2023)](https://www.nature.com/articles/s42256-023-00691-9) • [code](https://github.com/melobio/EvoPlay)

**Curiosity Driven Protein Sequence Generation via Reinforcement Learning**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=tPjVRmHqCg)

**Stable Online and Offline Reinforcement Learning for Antibody CDRH3 Design**
Yannick Vogt, Mehdi Naouar, Maria Kalweit, Christoph Cornelius Miething, Justus Duyster, Roland Mertelsmann, Gabriel Kalweit, Joschka Boedecker
[arXiv:2401.05341](https://arxiv.org/abs/2401.05341)

**Peptide Vaccine Design by Evolutionary Multi-Objective Optimization**
Dan-Xuan Liu, Yi-Heng Xu, Chao Qian
[arXiv:2406.05743](https://arxiv.org/abs/2406.05743)

**Reinforcement Learning for Sequence Design Leveraging Protein Language Models**
Jithendaraa Subramanian, Shivakanth Sujit, Niloy Irtisam, Umong Sain, Derek Nowrouzezahrai, Samira Ebrahimi Kahou, Riashat Islam
[arXiv:2407.03154](https://arxiv.org/abs/2407.03154)

**BetterBodies: Reinforcement Learning guided Diffusion for Antibody Sequence Design**
Yannick Vogt, Mehdi Naouar, Maria Kalweit, Christoph Cornelius Miething, Justus Duyster, Joschka Boedecker, Gabriel Kalweit
[arXiv:2409.16298](https://arxiv.org/abs/2409.16298)

**Reinforcement learning-driven exploration of peptide space: accelerating generation of drug-like peptides**
Qian Wang, Xiaotong Hu, Zhiqiang Wei, Hao Lu, Hao Liu
[Briefings in Bioinformatics 25.5 (2024): bbae444](https://academic.oup.com/bib/article/25/5/bbae444/7754450) • [code](https://github.com/p1acemker/MomdTDSRL)

**Guiding Generative Protein Language Models with Reinforcement Learning**
Filippo Stocco, Maria Artigues-Lleixa, Andrea Hunklinger, Talal Widatalla, Marc Guell, Noelia Ferruz
[arXiv:2412.12979](https://arxiv.org/abs/2412.12979) • [code](https://github.com/AI4PDLab/DPO_pLM)

**DOTA: Developability-Optimized Antibody Generation**
Thao Nguyen, Jiateng Liu, Anna Hart
[UIUC Fall 2024 CS582 MLCB](https://openreview.net/forum?id=H4430Z0HfD)

**PepTune: De Novo Generation of Therapeutic Peptides with Multi-Objective-Guided Discrete Diffusion**
Sophia Tang, Yinuo Zhang, Pranam Chatterjee
[arXiv:2412.17780](https://arxiv.org/abs/2412.17780)

**PepINVENT: generative peptide design beyond natural amino acids**  
Gökçe Geylan, Jon Paul Janet, Alessandro Tibo, Jiazhen He, Atanas Patronov, Mikhail Kabeshov, Werngard Czechtizky, Florian David, Ola Engkvist and Leonardo De Maria  
[Chemical Science (2025)](https://pubs.rsc.org/en/content/articlelanding/2025/sc/d4sc07642g) • [code](https://github.com/MolecularAI/PepINVENT/)

### 5.7 Flow-based

**Biological Sequence Design with GFlowNets**
Moksh Jain, Emmanuel Bengio, Alex-Hernandez Garcia, Jarrid Rector-Brooks, Bonaventure F. P. Dossou, Chanakya Ekbote, Jie Fu, Tianyu Zhang, Micheal Kilgour, Dinghuai Zhang, Lena Simine, Payel Das, Yoshua Bengio
[arXiv preprint arXiv:2203.04115 (2022)](https://arxiv.org/abs/2203.04115) • [lecture](https://www.youtube.com/watch?v=YRbFDThaAmo)

**ProtFlow: Fast Protein Sequence Design via Flow Matching on Compressed Protein Language Model Embeddings**
Zitai Kong, Yiheng Zhu, Yinlong Xu, Hanjing Zhou, Mingzhe Yin, Jialu Wu, Hongxia Xu, Chang-Yu Hsieh, Tingjun Hou, Jian Wu
[arXiv:2504.10983](https://arxiv.org/abs/2504.10983)

**Multi-Objective-Guided Discrete Flow Matching for Controllable Biological Sequence Design**  
Tong Chen, Yinuo Zhang, Sophia Tang, Pranam Chatterjee  
[arXiv:2505.07086](https://arxiv.org/abs/2505.07086v2) • [model](https://huggingface.co/ChatterjeeLab/MOG-DFM)

### 5.8 RNN-based

**Deep learning to design nuclear-targeting abiotic miniproteins**
Carly K. Schissel, Somesh Mohapatra, Justin M. Wolfe, Colin M. Fadzen, Kamela Bellovoda, Chia-Ling Wu, Jenna A. Wood, Annika B. Malmberg, Andrei Loas, Rafael Gómez-Bombarelli & Bradley L. Pentelute
[Nature Chemistry 13.10 (2021)](https://www.nature.com/articles/s41557-021-00766-3) • [code](https://github.com/learningmatter-mit/peptimizer)

**Recurrent neural network model for constructive peptide design**
Müller, Alex T., Jan A. Hiss, and Gisbert Schneider
[Journal of chemical information and modeling 58.2 (2018)](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.7b00414)

**Machine learning designs non-hemolytic antimicrobial peptides**
Alice Capecchi, Xingguang Cai, Hippolyte Personne, Thilo Köhler, Christian van Delden, and Jean-Louis Reymond
[Chemical Science 12.26 (2021)](https://pubs.rsc.org/en/content/articlehtml/2021/sc/d1sc01713f)

**Using molecular dynamics simulations to prioritize and understand AI-generated cell penetrating peptides**
Duy Phuoc Tran, Seiichi Tada, Akiko Yumoto, Akio Kitao, Yoshihiro Ito, Takanori Uzawa & Koji Tsuda
[Scientific reports 11.1 (2021)](https://www.nature.com/articles/s41598-021-90245-z)

**De novo antioxidant peptide design via machine learning and DFT studies**
Parsa Hesamzadeh, Abdolvahab Seif, Kazem Mahmoudzadeh, Mokhtar Ganjali Koli, Amrollah Mostafazadeh, Kosar Nayeri, Zohreh Mirjafary & Hamid Saeidian
[Scientific Reports 14.1 (2024)](https://www.nature.com/articles/s41598-024-57247-z) • [code](https://github.com/mephisto121/DeepGenAntiOxidantPeptide)

### 5.9 LSTM-based

**Computational antimicrobial peptide design and evaluation against multidrug-resistant clinical isolates of bacteria**
Deepesh Nagarajan, Tushar Nagarajan, Natasha Roy, Omkar Kulkarni, Sathyabaarathi Ravichandran, Madhulika Mishra
Dipshikha Chakravortty, Nagasuma Chandra
[Journal of Biological Chemistry 293.10 (2018)](https://www.jbc.org/article/S0021-9258(20)40390-4/fulltext)

**Deep learning enables the design of functional de novo antimicrobial proteins**
Javier Caceres-Delpiano, Roberto Ibañez, Patricio Alegre, Cynthia Sanhueza, Romualdo Paz-Fiblas, Simon Correa, Pedro Retamal, Juan Cristóbal Jiménez, Leonardo Álvarez
[bioRxiv (2020)](https://www.biorxiv.org/content/10.1101/2020.08.26.266940v1.full)

**ECNet is an evolutionary context-integrated deep learning framework for protein engineering**
Yunan Luo, Guangde Jiang, Tianhao Yu, Yang Liu, Lam Vo, Hantian Ding, Yufeng Su, Wesley Wei Qian, Huimin Zhao & Jian Peng
[Nature communications 12.1 (2021)](https://www.nature.com/articles/s41467-021-25976-8)

**Deep learning for novel antimicrobial peptide design**
Wang, Christina, Sam Garlick, and Mire Zloh
[Biomolecules 11.3 (2021)](https://www.mdpi.com/2218-273X/11/3/471)

**Antibody design using LSTM based deep generative model from phage display library for affinity maturation**
Koichiro Saka, Taro Kakuzaki, Shoichi Metsugi, Daiki Kashiwagi, Kenji Yoshida, Manabu Wada, Hiroyuki Tsunoda & Reiji Teramoto
[Scientific reports 11.1 (2021)](https://www.nature.com/articles/s41598-021-85274-7)

**In silico proof of principle of machine learning-based antibody design at unconstrained scale**
Akbar, Rahmad, et al
[Mabs. Vol. 14. No. 1. Taylor &amp; Francis, 2022](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8986205/pdf/KMAB_14_2031482.pdf) • [code](https://github.com/csi-greifflab/manuscript_insilico_antibody_generation)

**Large-scale design and refinement of stable proteins using sequence-only models**
Jedediah M. Singer , Scott Novotney, Devin Strickland, Hugh K. Haddox, Nicholas Leiby, Gabriel J. Rocklin, Cameron M. Chow, Anindya Roy, Asim K. Bera, Francis C. Motta, Longxing Cao, Eva-Maria Strauch, Tamuka M. Chidyausiku, Alex Ford, Ethan Ho, Alexander Zaitzeff, Craig O. Mackenzie, Hamed Eramian, Frank DiMaio, Gevorg Grigoryan, Matthew Vaughn, Lance J. Stewart, David Baker, Eric Klavins
[PloS one 17.3 (2022)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0265020) • [code](https://zenodo.org/record/4906529)

**Deep-learning based bioactive therapeutic peptides generation and screening**
Haiping Zhang, Konda Mani Saravanan, Yanjie Wei, Yang Jiao, Yang Yang, Yi Pan, Xuli Wu, John Z.H. Zhang
[bioRxiv 2022.11.14.516530](https://www.biorxiv.org/content/10.1101/2022.11.14.516530v1) • [code](https://github.com/haiping1010/New_peptide_iteration) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/11/16/2022.11.14.516530/DC1/embed/media-1.pdf)

**Deep-learning based bioactive peptides generation and screening against Xanthine oxidase**
Haiping Zhang, Konda Mani Saravanan, John Z.H. Zhang, Xuli Wu
[bioRxiv 2023.01.11.523536](https://www.biorxiv.org/content/10.1101/2023.01.11.523536v1)

**Deep Learning-Based Bioactive Therapeutic Peptide Generation and Screening**
Haiping Zhang, Konda Mani Saravanan, Yanjie Wei, Yang Jiao, Yang Yang, Yi Pan, Xuli Wu, and John Z. H. Zhang
[Journal of Chemical Information and Modeling 63.3 (2023)](https://pubs.acs.org/doi/10.1021/acs.jcim.2c01485) • [code](https://github.com/haiping1010/New_peptide_iteration/tree/master/iteration_main_protease_Antiviral_pep)

**Bio-xLSTM: Generative modeling, representation and in-context learning of biological and chemical sequences**
Niklas Schmidinger, Lisa Schneckenreiter, Philipp Seidl, Johannes Schimunek, Pieter-Jan Hoedt, Johannes Brandstetter, Andreas Mayr, Sohvi Luukkonen, Sepp Hochreiter, Günter Klambauer
[arXiv:2411.04165](https://arxiv.org/abs/2411.04165)

### 5.10 Autoregressive-models

**Efficient generative modeling of protein sequences using simple autoregressive models**
Jeanne Trinquier, Guido Uguzzoni, Andrea Pagnani, Francesco Zamponi & Martin Weigt
[Nature communications 12.1 (2021): 1-11](https://www.nature.com/articles/s41467-021-25756-4) • [code](https://github.com/pagnani/ArDCA.jl)

**Conformal prediction for the design problem**
Clara Fannjiang, Stephen Bates, Anastasios N. Angelopoulos, Jennifer Listgarten, Michael I. Jordan
[arXiv:2202.03613v4](https://arxiv.org/abs/2202.03613) • [code](https://github.com/clarafy/conformal-for-design)

**Enhancing privacy in biosecurity with watermarked protein design**  
Yanshuo Chen, Zhengmian Hu, Yihan Wu, Ruibo Chen, Yongrui Jin, Marcus Zhan, Chengjin Xie, Wei Chen, Heng Huang
[Bioinformatics, 2025;, btaf141](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btaf141/8124073) • [code](https://github.com/poseidonchan/ProteinWatermark)

**Controllable Protein Design via Autoregressive Direct Coupling Analysis Conditioned on Principal Components**  
Francesco Caredda, Andrea Pagnani, Paolo De Los Rios, Lisa Gennai  
[bioRxiv 2025.08.18.669886](https://www.biorxiv.org/content/10.1101/2025.08.18.669886v1) • [code](https://github.com/francescocaredda/FeatureDCA.jl)

### 5.11 Boltzmann-machine-based

**How pairwise coevolutionary models capture the collective residue variability in proteins?**
Figliuzzi, Matteo, Pierre Barrat-Charlaix, and Martin Weigt
[Molecular biology and evolution 35.4 (2018): 1018-1027](https://academic.oup.com/mbe/article/35/4/1018/4815777) • [code](https://github.com/matteofigliuzzi/bmDCA)

**A Pareto-optimal compositional energy-based model for sampling and optimization of protein sequences**
Nataša Tagasovska, Nathan C. Frey, Andreas Loukas, Isidro Hötzel, Julien Lafrance-Vanasse, Ryan Lewis Kelly, Yan Wu, Arvind Rajpal, Richard Bonneau, Kyunghyun Cho, Stephen Ra, Vladimir Gligorijević
[arXiv:2210.10838](https://arxiv.org/abs/2210.10838) • [slides](https://drive.google.com/file/d/1spTU-iZ4EEq8ZICRHBw8CstpYQXCxMy8/view)

**Computational design of novel Cas9 PAM-interacting domains using evolution-based modelling and structural quality assessment**
Cyril Malbranke, William Rostain, Florence Depardieu, Simona Cocco, Remi Monasson, David Bikard
[bioRxiv 2023.03.20.533501](https://www.biorxiv.org/content/10.1101/2023.03.20.533501v1) • [code](https://github.com/CyrilMa/DesignCas9WithCLD) • [Supplementary](https://www.biorxiv.org/content/10.1101/2023.03.20.533501v1.supplementary-material)

**Protein Discovery with Discrete Walk-Jump Sampling**
Nathan C. Frey, Daniel Berenberg, Karina Zadorozhny, Joseph Kleinhenz, Julien Lafrance-Vanasse, Isidro Hotzel, Yan Wu, Stephen Ra, Richard Bonneau, Kyunghyun Cho, Andreas Loukas, Vladimir Gligorijevic, Saeed Saremi
[arXiv:2306.12360](https://arxiv.org/abs/2306.12360)/[ICLR 2024](https://openreview.net/forum?id=zMPHKOmQNb) • [code](https://github.com/Genentech/walk-jump) • [lecture](https://www.youtube.com/watch?v=r28m5Vk77Wk)

### 5.12 Diffusion-based

**denoising-diffusion-protein-sequence**
Zhangzhi Peng
Paper unavailable • [github](https://github.com/pengzhangzhi/protein-sequence-diffusion-model)

**Protein Design with Guided Discrete Diffusion**
Nate Gruver, Samuel Stanton, Nathan C. Frey, Tim G. J. Rudner, Isidro Hotzel, Julien Lafrance-Vanasse, Arvind Rajpal, Kyunghyun Cho, Andrew Gordon Wilson
[arXiv:2305.20009](https://arxiv.org/abs/2305.20009)/[Advances in neural information processing systems, 2024](https://openreview.net/forum?id=MfiK69Ga6p) • [code](https://github.com/ngruver/NOS) • [lecture](https://www.youtube.com/watch?v=Hm8Z0SIyLqw)

**PRO-LDM: Protein Sequence Generation with Conditional Latent Diffusion Models**
Zixuan Jiang, Sitao Zhang, Rundong Huang, Shaoxun Mo, Letao Zhu, Peiheng Li, Ziyi Zhang, Xi Chen, Yunfei Long, Renjing Xu, Rui Qing
[bioRxiv 2023.08.22.554145](https://www.biorxiv.org/content/10.1101/2023.08.22.554145v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/08/23/2023.08.22.554145/DC1/embed/media-1.pdf)

**Protein generation with evolutionary diffusion: sequence is all you need**
Sarah Alamdari, Nitya Thakkar, Rianne van den Berg, Alex Xijie Lu, Nicolo Fusi, Ava Pardis Amini, Kevin K Yang
[bioRxiv 2023.09.11.556673](https://www.biorxiv.org/content/10.1101/2023.09.11.556673v1) • [code](https://github.com/microsoft/evodiff) • [data](https://zenodo.org/record/8045076) • [lecture](https://www.youtube.com/watch?v=e1e-_SkyNjw), [lecture2](https://www.youtube.com/watch?v=iV_7mgxe4OI)

**AntiBARTy Diffusion for Property Guided Antibody Design**
Jordan Venderley
[arXiv:2309.13129](https://arxiv.org/abs/2309.13129)

**PD-1 Targeted Antibody Discovery Using AI Protein Diffusion**
Colby T. Ford
[bioRxiv 2024.01.18.576323](https://www.biorxiv.org/content/10.1101/2024.01.18.576323v2) • [code](https://github.com/tuplexyz/PD-1_Fab_Diffusion)

**ProT-Diff: A Modularized and Efficient Approach to De Novo Generation of Antimicrobial Peptide Sequences through Integration of Protein Language Model and Diffusion Model**
Xue-Fei Wang, Jing-Ya Tang, Han Liang, Jing Sun, Sonam Dorje, Bo Peng, Xu-Wo Ji, Zhe Li, Xian-En Zhang, Dian-Bing Wang
[bioRxiv 2024.02.22.581480](https://www.biorxiv.org/content/10.1101/2024.02.22.581480v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/02/23/2024.02.22.581480/DC1/embed/media-1.docx)

**TaxDiff: Taxonomic-Guided Diffusion Model for Protein Sequence Generation**
Lin Zongying, Li Hao, Lv Liuzhenghao, Lin Bin, Zhang Junwu, Chen Calvin Yu-Chian, Yuan Li, Tian Yonghong
[arXiv:2402.17156](https://arxiv.org/abs/2402.17156) • [code](https://github.com/Linzy19/TaxDiff)

**Diffusion on language model embeddings for protein sequence generation**
Viacheslav Meshchaninov, Pavel Strashnov, Andrey Shevtsov, Fedor Nikolaev, Nikita Ivanisenko, Olga Kardymon, Dmitry Vetrov
[arXiv:2403.03726](https://arxiv.org/abs/2403.03726)

**AMP-Diffusion: Integrating Latent Diffusion with Protein Language Models for Antimicrobial Peptide Generation**
Tianlai Chen, Pranay Vure, Rishab Pulugurta, Pranam Chatterjee
[bioRxiv 2024.03.03.583201](https://www.biorxiv.org/content/10.1101/2024.03.03.583201v1)

**Atomically accurate de novo design of single-domain antibodies**
Nathaniel R. Bennett, Joseph L. Watson, Robert J. Ragotte, Andrew J. Borst, DeJenae L. See, Connor Weidle, Riti Biswas, Ellen L. Shrock, Philip J. Y. Leung, Buwei Huang, Inna Goreshnik, Russell Ault, Kenneth D. Carr, Benedikt Singer, Cameron Criswell, Dionne Vafeados, Mariana Garcia Sanchez, Ho Min Kim, Susana Vazquez Torres, Sidney Chan, David Baker
[bioRxiv 2024.03.14.585103](https://www.biorxiv.org/content/10.1101/2024.03.14.585103v1)/[Nat Chem Biol (2025)](https://www.nature.com/articles/s41589-025-01929-w) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/03/18/2024.03.14.585103/DC1/embed/media-1.pdf)

**Complex-based Ligand-Binding Proteins Redesign by Equivariant Diffusion-based Generative Models**
Viet Thanh Duy Nguyen, Nhan Nguyen, Truong Son Hy
[bioRxiv 2024.04.17.589997](https://www.biorxiv.org/content/10.1101/2024.04.17.589997v1) • [code](https://github.com/HySonLab/Protein_Redesign)

**Cytochrome P450 Enzyme Design by Constraining Catalytic Pocket in Diffusion model**
Qian Wang, Xiaonan Liu, Hejian Zhang, Huanyu Chu, Chao Shi, Lei Zhang, Jie Bai, Pi Liu, Jing Li, Xiaoxi Zhu, Yuwan Liu, Zhangxin Chen, Rong Huang, Hong Chang, Tian Liu, Zhenzhan Chang , Jian Cheng , and Huifeng Jiang
[Research (2024)](https://spj.science.org/doi/10.34133/research.0413) • [code](https://github.com/JiangLab2020/P450Diffusion)

**Context-Guided Diffusion for Out-of-Distribution Molecular and Protein Design**
Leo Klarner, Tim G. J. Rudner, Garrett M. Morris, Charlotte M. Deane, Yee Whye Teh
[arXiv:2407.11942](https://arxiv.org/abs/2407.11942) • [code](https://github.com/leojklarner/context-guided-diffusion)

**Secondary Structure-Guided Novel Protein Sequence Generation with Latent Graph Diffusion**
Yutong Hu, Yang Tan, Andi Han, Lirong Zheng, Liang Hong, Bingxin Zhou
[arXiv:2407.07443](https://arxiv.org/abs/2407.07443) • [code](https://github.com/riacd/CPDiffusion-SS)

**AI-generated small binder improves prime editing**
Ju-Chan Park, Heesoo Uhm, Yong-Woo Kim, Ye Eun Oh, Sangsu Bae
[bioRxiv 2024.09.11.612443](https://www.biorxiv.org/content/10.1101/2024.09.11.612443v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/09/14/2024.09.11.612443/DC1/embed/media-1.pdf)

**MeMDLM: De Novo Membrane Protein Design with Masked Discrete Diffusion Protein Language Models**
Shrey Goel, Vishrut Thoutam, Edgar Mariano Marroquin, Aaron Gokaslan, Arash Firouzbakht, Sophia Vincoff, Volodymyr Kuleshov, Huong T. Kratochvil, Pranam Chatterjee
[arXiv:2410.16735](https://arxiv.org/abs/2410.16735)/[ICLR 2025 Workshop LMRL](https://openreview.net/forum?id=ZnEx3GbU9C)

**Retrieval Augmented Diffusion Model for Structure-informed Antibody Design and Optimization**
Zichen Wang, Yaokun Ji, Jianing Tian, Shuangjia Zheng
[arXiv:2410.15040](https://arxiv.org/abs/2410.15040)

**ProtDiff: Function-Conditioned Masked Diffusion Models for Robust Directed Protein Generation**
Vishrut Thoutam, Yair Schiff, Sergey Ovchinnikov, Pranam Chatterjee
[Neurips 2024 Workshop Foundation Models for Science: Progress, Opportunities, and Challenges](https://openreview.net/forum?id=POrk2Cc7Ux)

**Diffusion on language model encodings for protein sequence generation**
Viacheslav Meshchaninov, Pavel Strashnov, Andrey Shevtsov, Fedor Nikolaev, Nikita Ivanisenko, Olga Kardymon, Dmitry Vetrov
[ICLR 2025](https://openreview.net/forum?id=LoXJlAW3gU)

**Reward-Guided Iterative Refinement in Diffusion Models at Test-Time with Applications to Protein and DNA Design**
Masatoshi Uehara, Xingyu Su, Yulai Zhao, Xiner Li, Aviv Regev, Shuiwang Ji, Sergey Levine, Tommaso Biancalani
[arXiv:2502.14944](https://arxiv.org/abs/2502.14944) • [code](https://github.com/masa-ue/ProDifEvo-Refinement)

**De Novo Design of Large Polypeptides Using a Lightweight Diffusion Model Integrating LSTM and Attention Mechanism Under Per-Residue Secondary Structure Constraints**
Sisheng Liao,Gang Xu,Li Jin and Jianpeng Ma
[Molecules 30.5 (2025)](https://www.mdpi.com/1420-3049/30/5/1116) • [code](https://github.com/daedaluser/PPD)

**AI-Based Antibody Design Targeting Recent H5N1 Avian Influenza Strains**  
Nicholas Santolla, Colby T. Ford  
[bioRxiv 2025.04.24.650061](https://www.biorxiv.org/content/10.1101/2025.04.24.650061v1) • [code](https://github.com/Santollan/Frankies) • EvoDiff-based

**CFP-Gen: Combinatorial Functional Protein Generation via Diffusion Language Models**  
Junbo Yin, Chao Zha, Wenjia He, Chencheng Xu, Xin Gao  
[arXiv:2505.22869](https://arxiv.org/abs/2505.22869)

**AMPGen: an evolutionary information-reserved and diffusion-driven generative model for de novo design of antimicrobial peptides**  
Shuwen Jin, Zihan Zeng, Xiyan Xiong, Baicheng Huang, Li Tang, Hongsheng Wang, Xiao Ma, Xiaochun Tang, Guoqing Shao, Xingxu Huang & Feng Lin  
[Communications Biology 8.1 (2025)](https://www.nature.com/articles/s42003-025-08282-7) • [code](https://doi.org/10.5281/zenodo.15454482.7433980)

**Diffusion Sequence Models for Enhanced Protein Representation and Generation**  
Logan Hallee, Nikolaos Rafailidis, David B. Bichara, Jason P. Gleghorn  
[arXiv:2506.08293](https://arxiv.org/abs/2506.08293) • [code](https://github.com/Gleghorn-Lab/DSM)

**Uncertainty-Aware Discrete Diffusion Improves Protein Design**  
Sazan Mahbub, Christoph Feinauer, Caleb N. Ellington, Le Song, Eric P. Xing  
[bioRxiv 2025.06.30.662407](https://www.biorxiv.org/content/10.1101/2025.06.30.662407v1)

**Guided Generation for Developable Antibodies**  
Siqi Zhao, Joshua Moller, Porfi Quintero-Cadena, Lood van Niekerk  
[arXiv:2507.02670](https://arxiv.org/abs/2507.02670) • ESM-2-based

**PRO‐LDM: A Conditional Latent Diffusion Model for Protein Sequence Design and Functional Optimization**  
Sitao Zhang, Zixuan Jiang, Rundong Huang, Wenting Huang, Siyuan Peng, Shaoxun Mo, Letao Zhu, Peiheng Li, Ziyi Zhang, Emily Pan, Xi Chen, Yunfei Long, Qi Liang, Jin Tang, Renjing Xu, Rui Qing  
[Advanced Science (2025)](https://advanced.onlinelibrary.wiley.com/doi/10.1002/advs.202502723) • ESM-2-based

**Protein A-like peptide generation based on generalized diffusion model**  
Tianqian Zhou, Shibo Zhang, Huijia Song, Qiang He, Chun Fang & Xiaozhu Lin  
[J Comput Aided Mol Des 39, 76 (2025)](https://link.springer.com/article/10.1007/s10822-025-00653-w) • [code](https://github.com/PotatoGan/ProteinGeneration-GeneralizedDiffusion)

**PepCCD: A Contrastive Conditioned Diffusion Framework for Target-Specific Peptide Generation**  
Jun Zhang, Yangyang Zhou, Tiantian Zhu, Zexuan Zhu  
[bioRxiv 2025.09.01.673427](https://www.biorxiv.org/content/10.1101/2025.09.01.673427v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/09/04/2025.09.01.673427/DC1/embed/media-1.pdf)

**Generative latent diffusion language modeling yields anti-infective synthetic peptides**  
Marcelo D.T. Torres, Leo Tianlai Chen, Fangping Wan, Pranam Chatterjee, Cesar de la Fuente-Nunez  
[Cell Biomaterials (2025)](https://www.cell.com/cell-biomaterials/fulltext/S3050-5623(25)00174-6) • [code](https://github.com/programmablebio/amp-diffusion)

### 5.13 GNN-based

**Generative Pretrained Autoregressive Transformer Graph Neural Network applied to the Analysis and Discovery of Novel Proteins**
Markus J. Buehler
[arXiv:2305.04934](https://arxiv.org/abs/2305.04934) • [code](https://github.com/lamm-mit/MateriomicTransformer)

### 5.14 Score-based

**Microdroplet screening rapidly profiles a biocatalyst to enable its AI-assisted engineering**
Maximilian Gantz, Simon V. Mathis, Friederike E. H. Nintzel, Paul J. Zurek, Tanja Knaus, Elie Patel, Daniel Boros, Friedrich-Maximilian Weberling, Matthew R. A. Kenneth, Oskar J. Klein, Elliot J. Medcalf, Jacob Moss, Michael Herger, Tomasz S. Kaminski, Francesco G. Mutti, Pietro Lio, Florian Hollfelder
[bioRxiv (2024.04.08)](https://www.biorxiv.org/content/10.1101/2024.04.08.588565v1.full.pdf)

**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**
Minsu Kim, Federico Berto, Sungsoo Ahn, Jinkyoo Park
[arXiv:2306.03111](https://arxiv.org/abs/2306.03111)  • [code](https://github.com/kaist-silab/bootgen)

## 6. Function to Structure

> These models generate protein structures(including side chains) from expected function or recover a part of protein structures(aka. **inpainting**)

### 6.0 Review

**Towards deep learning sequence-structure co-generation for protein design**
Chentong Wang, Sarah Alamdari, Carles Domingo-Enrich, Ava Amini, Kevin K. Yang
[arXiv:2410.01773](https://arxiv.org/abs/2410.01773)/[Current Opinion in Structural Biology (2025)](https://www.sciencedirect.com/science/article/pii/S0959440X25000363)

### 6.1 LSTM-based

**One-sided design of protein-protein interaction motifs using deep learning**
Syrlybaeva, Raulia, and Eva-Maria Strauch
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.03.30.486144v2) • [code](https://github.com/strauchlab/iNNterfaceDesign) • [our notes](https://zhuanlan.zhihu.com/p/521613546) • [lecture](https://www.youtube.com/watch?v=bSWkXy56rt8)

### 6.2 Diffusion-based

**Protein Structure and Sequence Generation with Equivariant Denoising Diffusion Probabilistic Models**
Namrata Anand, Tudor Achim
[GitHub (2022)](https://nanand2.github.io/proteins/)/[arXiv (2022)](https://arxiv.org/abs/2205.15019) • [our notes](https://zhuanlan.zhihu.com/p/520488133) • [lecture](https://www.youtube.com/watch?v=i8fGzddGbU8)

**Antigen-Specific Antibody Design and Optimization with Diffusion-Based Generative Models for Protein Structures**
Shitong Luo, Yufeng Su, Xingang Peng, Sheng Wang, Jian Peng, Jianzhu Ma
[bioRxiv 2022.07.10.499510](https://www.biorxiv.org/content/10.1101/2022.07.10.499510v5)/[ICML (2023)](https://icml-compbio.github.io/2023/papers/WCBICML2023_paper143.pdf) • [code](https://github.com/luost26/diffab) • [hugging face](https://huggingface.co/spaces/luost26/DiffAb)

**Illuminating protein space with a programmable generative model**
John Ingraham, Max Baranov, Zak Costello, Vincent Frappier, Ahmed Ismail, Shan Tie, Wujie Wang, Vincent Xue, Fritz Obermeyer, Andrew Beam, Gevorg Grigoryan
[Generate Biomedicines Preprint](https://cdn.generatebiomedicines.com/assets/ingraham2022.pdf)/[bioRxiv 2022.12.01.518682](https://www.biorxiv.org/content/10.1101/2022.12.01.518682v1)/[Nature (2023)](https://www.nature.com/articles/s41586-023-06728-8) • [website](https://generatebiomedicines.com/chroma) • [news](https://www.nature.com/articles/s41587-023-01705-y) • [code](https://github.com/generatebio/chroma) • [colab](https://colab.research.google.com/github/generatebio/chroma/blob/main/notebooks/ChromaTutorial.ipynb) • commercial

**Physics-Inspired Protein Encoder Pre-Training via Siamese Sequence-Structure Diffusion Trajectory Prediction**
Zuobai Zhang, Minghao Xu, Aurélie Lozano, Vijil Chenthamarakshan, Payel Das, Jian Tang
[arXiv:2301.12068](https://arxiv.org/abs/2301.12068) • [code](https://github.com/DeepGraphLearning/SiamDiff)

**TRDiffusion**
[TIANRANG XLab](https://xlab.tianrang.com/)
[news](https://mp.weixin.qq.com/s/9rJ6IoJbf6cvz3UqE-rpIg) • [website](https://xlab.tianrang.com/xCREATOR) • commercial

**An all-atom protein generative model**
Alexander E Chu, Lucy Cheng, Gina El Nesr, Minkai Xu, Po-Ssu Huang
[bioRxiv 2023.05.24.542194](https://www.biorxiv.org/content/10.1101/2023.05.24.542194v1)/[Proceedings of the National Academy of Sciences 121.27 (2024)](https://www.pnas.org/doi/full/10.1073/pnas.2311500121) • [code](https://github.com/alexechu/protpardelle)

**DiffPack: A Torsional Diffusion Model for Autoregressive Protein Side-Chain Packing**
Yangtian Zhan, Zuobai Zhang, Bozitao Zhong, Sanchit Misra, Jian Tang
[arxiv 2023.06.01](https://arxiv.org/abs/2306.01794) • [code](https://github.com/DeepGraphLearning/DiffPack)

**AbDiffuser: Full-Atom Generation of In-Vitro Functioning Antibodies**
Karolis Martinkus, Jan Ludwiczak, Kyunghyun Cho, Wei-Ching Lian, Julien Lafrance-Vanasse, Isidro Hotzel, Arvind Rajpal, Yan Wu, Richard Bonneau, Vladimir Gligorijevic, Andreas Loukas
[arXiv:2308.05027](https://arxiv.org/abs/2308.05027) • [lecture](https://www.youtube.com/watch?v=95w0Ht3m0JY)

**Generative Diffusion Models for Antibody Design, Docking, and Optimization**
Zhangzhi Peng, Chenchen Han, Xiaohan Wang, Dapeng Li, Fajiie Yuan
[bioRxiv 2023.09.25.559190](https://www.biorxiv.org/content/10.1101/2023.09.25.559190v1) • [code](https://github.com/pengzhangzhi/ab_opt) • [website](https://pengzhangzhi.github.io/ab_opt_homepage/)

**Bridging Sequence and Structure: Latent Diffusion for Conditional Protein Generation**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=DP4NkPZOpD)

**Guiding diffusion models for antibody sequence and structure co-design with developability properties**
Amelia Villegas-Morcillo, Jana M. Weber, Marcel J.T. Reinders
[bioRxiv 2023.11.22.568230](https://www.biorxiv.org/content/10.1101/2023.11.22.568230v1)/[NeurIPS 2023 Generative AI and Biology Workshop](https://openreview.net/forum?id=bPcgbKDCUQ) • [code](https://github.com/amelvim/antibody-diffusion-properties)

**A Multi-Modal Contrastive Diffusion Model for Therapeutic Peptide Generation**
Yongkang Wang, Xuan Liu, Feng Huang, Zhankun Xiong, Wen Zhang
[arXiv:2312.15665](https://arxiv.org/abs/2312.15665) • [code](https://github.com/wyky481l/MMCD)

**Towards Joint Sequence-Structure Generation of Nucleic Acid and Protein Complexes with SE(3)-Discrete Diffusion**
Alex Morehead, Jeffrey Ruffolo, Aadyot Bhatnagar, Ali Madani
[arXiv:2401.06151](https://arxiv.org/abs/2401.06151) • [code](https://github.com/Profluent-Internships/MMDiff)

**Proteus: exploring protein structure generation for enhanced designability and efficiency**
Chentong Wang, Yannan Qu, Zhangzhi Peng, Yukai Wang, Hongli Zhu, Dachuan Chen, Longxing Cao
[bioRxiv 2024.02.10.579791](https://www.biorxiv.org/content/10.1101/2024.02.10.579791v3) • [code](https://github.com/Wangchentong/Proteus)

**Full-Atom Peptide Design with Geometric Latent Diffusion**
Xiangzhe Kong, Wenbing Huang, Yang Liu
[arXiv:2402.13555](https://arxiv.org/abs/2402.13555)

**A Hybrid Diffusion Model for Stable, Affinity-Driven, Receptor-Aware Peptide Generation**
R Vishva Saravanan, Soham Choudhuri, Bhaswar Ghosh
[bioRxiv 2024.03.14.584934](https://www.biorxiv.org/content/10.1101/2024.03.14.584934v1) • [code](https://github.com/BhaswarGhoshLab/HYDRA) • [dataset](http://huanglab.phys.hust.edu.cn/pepbdb/)

**Antigen-Specific Antibody Design via Direct Energy-based Preference Optimization**
Xiangxin Zhou, Dongyu Xue, Ruizhe Chen, Zaixiang Zheng, Liang Wang, Quanquan Gu
[arXiv:2403.16576](https://arxiv.org/abs/2403.16576)

**HelixDiff, a Score-Based Diffusion Model for Generating All-Atom α-Helical Structures**
Xuezhi Xie, Pedro A Valiente, Jisun Kim, and Philip M Kim
[ACS Central Science (2024)](https://pubs.acs.org/doi/full/10.1021/acscentsci.3c01488) • [code](https://github.com/xxiexuezhi/HelixDiff)

**Combining transformer and 3DCNN models to achieve co-design of structures and sequences of antibodies in a diffusional manner**
Yue Hu, Feng Tao, Jun Wen Lan, Jing Zhang
[bioRxiv 2024.04.25.587828](https://www.biorxiv.org/content/10.1101/2024.04.25.587828v1) • [code](https://github.com/YueHuLab/AlphaPanda)

**Target-Specific De Novo Peptide Binder Design with DiffPepBuilder**
Fanhao Wang, Yuzhe Wang, Laiyi Feng, Changsheng Zhang, Luhua Lai
[arXiv:2405.00128](https://arxiv.org/abs/2405.00128)/[J. Chem. Inf. Model. 2024](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.4c00975) • [code](https://github.com/YuzheWangPKU/DiffPepBuilder)

**Improving Antibody Design with Force-Guided Sampling in Diffusion Models**
Paulina Kulytė, Francisco Vargas, Simon Valentin Mathis, Yu Guang Wang, José Miguel Hernández-Lobato, Pietro Liò
[arXiv:2406.05832](https://arxiv.org/abs/2406.05832)

**Antibody Design Using a Score-based Diffusion Model Guided by Evolutionary, Physical and Geometric Constraints**
Tian Zhu, Milong Ren, Haicang Zhang
[ICML 2024](https://openreview.net/forum?id=1YsQI04KaN) • [code](https://github.com/zhanghaicang/carbonmatrix_public)

**Antibody-SGM, a Score-Based Generative Model for Antibody Heavy-Chain Design**
Xuezhi Xie, Pedro A. Valiente, Jin Sub Lee, Jisun Kim, Philip M. Kim
[Journal of Chemical Information and Modeling (2024)](https://pubs.acs.org/doi/10.1021/acs.jcim.4c00711) • [code](https://github.com/xxiexuezhi/ABSGM)

**Hybrid Diffusion Model for Stable, Affinity-Driven, Receptor-Aware Peptide Generation**
Vishva Saravanan R, Soham Choudhuri, Bhaswar Ghosh
[J. Chem. Inf. Model. 2024](https://pubs.acs.org/doi/10.1021/acs.jcim.4c01020) • [code](https://github.com/ComputationalBiologyLab-IIITH/HYDRA)

**De novo design of high-affinity protein binders with AlphaProteo**
Vinicius Zambaldi, David La, Alexander E. Chu, Harshnira Patani, Amy E. Danson, Tristan O. C., Kwan, Thomas Frerix, Rosalia G. Schneider, David Saxton, Ashok Thillaisundaram, Zachary Wu, Isabel Moraes, Oskar Lange, Eliseo Papa, Gabriella Stanton, Victor Martin, Sukhdeep Singh, Lai H. Wong, Russ Bates, Simon A. Kohl, Josh Abramson, Andrew W. Senior, Yilmaz Alguel, Mary Y. Wu, Irene M. Aspalter, Katie Bentley, David L.V. Bauer, Peter Cherepanov, Demis Hassabis, Pushmeet Kohli, Rob Fergus, and Jue Wang
[DeepMind Preprint](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/alphaproteo-generates-novel-proteins-for-biology-and-health-research/Protein_Design_White_Paper_2024.pdf)/[arXiv:2409.08022](https://arxiv.org/abs/2409.08022) • [blog](https://deepmind.google/discover/blog/alphaproteo-generates-novel-proteins-for-biology-and-health-research/)

**DPLM-2: A Multimodal Diffusion Protein Language Model**
Xinyou Wang, Zaixiang Zheng, Fei Ye, Dongyu Xue, Shujian Huang, Quanquan Gu
[arXiv:2410.13782](https://arxiv.org/abs/2410.13782) • [code](https://github.com/bytedance/dplm) • [website](https://bytedance.github.io/dplm/dplm-2)

**E(3)-invaraint diffusion model for pocket-aware peptide generation**
Po-Yu Liang, Jun Bai
[arXiv:2410.21335](https://arxiv.org/abs/2410.21335) • [code](https://github.com/LabJunBMI/E3-invaraint-diffusion-model-for-pocket-aware-peptide-generation)

**Generating All-Atom Protein Structure from Sequence-Only Training Data** / **All-Atom Protein Generation with Latent Diffusion**
Amy X. Lu, Wilson Yan, Sarah A. Robinson, Kevin K. Yang, Vladimir  Gligorijevic, Kyunghyun Cho, Richard Bonneau, Pieter Abbeel, Nathan Frey
[bioRxiv 2024.12.02.626353](https://www.biorxiv.org/content/10.1101/2024.12.02.626353v2)/[OpenReview](https://openreview.net/forum?id=5zNRgNMxIS) • [code](https://github.com/amyxlu/plaid) • [blog](https://www.matricedigitale.it/tech/intelligenza-artificiale/plaid-intelligenza-artificiale-proteine-3d/)

**Efficient protein structure generation with sparse denoising models**
Michael Jendrusch, Jan O. Korbel
[bioRxiv 2025.01.31.635780](https://www.biorxiv.org/content/10.1101/2025.01.31.635780v1) • [code](https://doi.org/10.5281/zenodo.14711580), [github](https://github.com/mjendrusch/salad)

**Neo-1**
[VANTAI](https://www.vant.ai/team)
paper not available • [website](https://www.vant.ai/neo-1) • commercial

**UniMoMo: Unified Generative Modeling of 3D Molecules for De Novo Binder Design**
Xiangzhe Kong, Zishen Zhang, Ziting Zhang, Rui Jiao, Jianzhu Ma, Kai Liu, Wenbing Huang, Yang Liu
[arXiv:2503.19300](https://arxiv.org/abs/2503.19300v1)

**PPDiff: Diffusing in Hybrid Sequence-Structure Space for Protein-Protein Complex Design**  
Zhenqiao Song, Tiaoxiao Li, Lei Li, Martin Renqiang Min  
[arXiv:2506.11420](https://arxiv.org/abs/2506.11420)

**Antibody Design and Optimization with Multi-scale Equivariant Graph Diffusion Models for Accurate Complex Antigen Binding**  
Jiameng Chen, Xiantao Cai, Jia Wu, Wenbin Hu  
[arXiv:2506.20957](https://arxiv.org/abs/2506.20957v1) • [code](https://github.com/Patrick221215/AbMEGD)

**Demystify Protein Generation with Hierarchical Conditional Diffusion Models**  
Zinan Ling, Yi Shi, Da Yan, Yang Zhou, Bo Hui  
[arXiv:2507.18603](https://arxiv.org/abs/2507.18603)

**PXDesign: Fast, Modular, and Accurate De Novo Design of Protein Binders**  
Milong Ren, Jinyuan Sun, Jiaqi Guan, Cong Liu, Chengyue Gong, Yuzhe Wang, Lan Wang, Qixu Cai, Xinshi Chen, Wenzhi Xiao  
[technical report](https://protenix.github.io/pxdesign/technical_report.pdf)/[bioRxiv 2025.08.15.670450](https://www.biorxiv.org/content/10.1101/2025.08.15.670450v1) • [code](https://github.com/bytedance/PXDesignBench) • [server](https://protenix-server.com/) • [data]([supplements/670450_file03.zip])

**Deep learning-based joint sequence-structure de novo membrane protein design**  
Lucas Rudden, Remo Battig, Vinnie Andrews, Julie Nguyen, Martin Stoll, Lorenzo Scutteri, Michal Winnicki, Melissa J Call, Matthew E Call, Damien Thevenin, Patrick Barth  
[bioRxiv 2025.08.15.670493](https://www.biorxiv.org/content/10.1101/2025.08.15.670493v1)

**Conditional Protein Structure Generation with Protpardelle-1C**  
Tianyu Lu, Richard Shuai, Petr Kouba, Zhaoyang Li, Yilin Chen, Akio Shirali, Jinho Kim, Po-Ssu Huang  
[bioRxiv 2025.08.18.670959](https://www.biorxiv.org/content/10.1101/2025.08.18.670959v2) • [code](https://github.com/ProteinDesignLab/protpardelle-1c/tree/main)

**Generating functional and multistate proteins with a multimodal diffusion transformer**  
Bowen Jing, Anna Sappington, Mihir Bafna, Ravi Shah, Adrina Tang, Rohith Krishna, Adam Klivans, Daniel J Diaz, Bonnie Berger  
[bioRxiv 2025.09.03.672144](https://www.biorxiv.org/content/10.1101/2025.09.03.672144v2) • [code](https://github.com/bjing2016/ProDiT)

### 6.3 RoseTTAFold-based

**Deep learning methods for designing proteins scaffolding functional sites** / **Scaffolding protein functional sites using deep learning**
Jue Wang, Sidney Lisanza, David Juergens, Doug Tischer, Ivan Anishchenko, Minkyung Baek, Joseph L. Watson, Jung Ho Chun, Lukas F. Milles, Justas Dauparas, Marc Expòsit, Wei Yang, Amijai Saragovi, Sergey Ovchinnikov, David Baker
[bioRxiv(2021)](https://europepmc.org/article/ppr/ppr419387)/[Science(2022)](https://www.science.org/doi/10.1126/science.abn2100) • [RFDesign](https://github.com/RosettaCommons/RFDesign) • [our notes](https://zhuanlan.zhihu.com/p/477854488) • [lecture](https://www.youtube.com/watch?v=-EJ8SXTBin0) • [RoseTTAFold](https://github.com/RosettaCommons/RoseTTAFold) • [Supplementary](https://www.science.org/doi/suppl/10.1126/science.abn2100/suppl_file/science.abn2100_sm.pdf), [Other Supplementary](https://www.science.org/doi/suppl/10.1126/science.abn2100/suppl_file/science.abn2100_data_s1_and_s2.zip)

**Broadly applicable and accurate protein design by integrating structure prediction networks and diffusion generative models** / **De novo design of protein structure and function with RFdiffusion**
Joseph L. Watson, David Juergens, Nathaniel R. Bennett, Brian L. Trippe, Jason Yim, Helen E. Eisenach, Woody Ahern, Andrew J. Borst, Robert J. Ragotte, Lukas F. Milles, Basile I. M. Wicky, Nikita Hanikel, Samuel J. Pellock, Alexis Courbet, William Sheffler, Jue Wang, Preetham Venkatesh, Isaac Sappington, Susana Vázquez Torres, Anna Lauko, Valentin De Bortoli, Emile Mathieu, Regina Barzilay, Tommi S. Jaakkola, Frank DiMaio, Minkyung Baek, David Baker
[Bakerlab Preprint](https://www.bakerlab.org/wp-content/uploads/2022/11/Diffusion_preprint_12012022.pdf)/[bioRxiv 2022.12.09.519842](https://www.biorxiv.org/content/10.1101/2022.12.09.519842v2)/[Nature (2023)](https://www.nature.com/articles/s41586-023-06415-8) • [news](https://www.bakerlab.org/2022/11/30/diffusion-model-for-protein-design/), [news2](https://www.ipd.uw.edu/2023/03/rf-diffusion-now-free-and-open-source/), [news3](https://www.nature.com/articles/d41586-023-02227-y) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/12/10/2022.12.09.519842/DC1/embed/media-1.pdf) • [lecture](https://www.youtube.com/watch?v=wIHwHDt2NoI), [lecture2](https://www.youtube.com/watch?v=828WPIIOwaA) • [RFdiffusion:code](https://github.com/RosettaCommons/RFdiffusion), [Colab](https://colab.research.google.com/github/sokrypton/ColabDesign/blob/v1.1.1/rf/examples/diffusion.ipynb) • [blog](https://www.science.org/content/blog-post/protein-design-ai-way)

**De novo design of high-affinity protein binders to bioactive helical peptides**
Susana Vázquez Torres, Philip J. Y. Leung, Isaac D. Lutz, Preetham Venkatesh, Joseph L Watson, Fabian Hink, Huu-Hien Huynh, Andy Hsien-Wei Yeh, David Juergens, Nathaniel R. Bennett, Andrew N. Hoofnagle, Eric Huang, Michael J. MacCoss, Marc Expòsit, Gyu Rie Lee, Elif Nihal Korkmaz, Jeff Nivala, Lance Stewart, Joseph M. Rodgers, David Baker
[bioRxiv 2022.12.10.519862](https://www.biorxiv.org/content/10.1101/2022.12.10.519862v1)/[Nature (2023)](https://www.nature.com/articles/s41586-023-06953-1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/12/10/2022.12.10.519862/DC1/embed/media-1.pdf)

**Joint Generation of Protein Sequence and Structure with RoseTTAFold Sequence Space Diffusion**
Sidney Lyayuga Lisanza, Jacob Merle Gershon, Sam Wayne Kenmore Tipps, Lucas Arnoldt, Samuel Hendel, Jeremiah Nelson Sims, Xinting Li, David Baker
[bioRxiv 2023.05.08.539766](https://www.biorxiv.org/content/10.1101/2023.05.08.539766v1)/[Nat Biotechnol (2024)](https://www.nature.com/articles/s41587-024-02395-w) • [code](https://github.com/RosettaCommons/protein_generator#proteingenerator-generate-sequence-structure-pairs-with-rosettafold) • [hugging face](https://huggingface.co/spaces/merle/PROTEIN_GENERATOR) • [lecture](https://www.youtube.com/watch?v=bS71K2U0amA)

**The structural landscape of the immunoglobulin fold by large-scale de novo design**
Jorge Roel-Touris, Lourdes Carcelen, Enrique Marcos
[bioRxiv 2023.10.03.560637](https://www.biorxiv.org/content/10.1101/2023.10.03.560637v1)/[Protein Science (2024)](https://onlinelibrary.wiley.com/doi/10.1002/pro.4936) • [Supplementary](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1002%2Fpro.4936&file=pro4936-sup-0001-supinfo.docx) • [code](https://github.com/JorgeRoel/betasandwich) • [data](https://zenodo.org/record/8380285)

**Generalized Biomolecular Modeling and Design with RoseTTAFold All-Atom**
Rohith Krishna, Jue Wang, Woody Ahern, Pascal Sturmfels, Preetham Venkatesh, Indrek Kalvet, Gyu Rie Lee, Felix S Morey-Burrows, Ivan Anishchenko, Ian R Humphreys, Ryan McHugh, Dionne Vafeados, Xinting Li, George A Sutherland, Andrew Hitchcock, C Neil Hunter, Minkyung Baek, Frank DiMaio, David Baker
[bioRxiv 2023.10.09.561603](https://www.biorxiv.org/content/10.1101/2023.10.09.561603v1)/[Science](https://www.science.org/doi/10.1126/science.adl2528) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/10/09/2023.10.09.561603/DC1/embed/media-1.pdf) • [code](https://github.com/baker-laboratory/RoseTTAFold-All-Atom)

**Amalga: Designable Protein Backbone Generation with Folding and Inverse Folding Guidance**
Shugao Chen, Ziyao Li, Xiangxiang Zeng, Guolin Ke
[bioRxiv 2023.11.07.565939](https://www.biorxiv.org/content/10.1101/2023.11.07.565939v1)

**Replicating enzymatic activity by positioning active sites with synthetic protein scaffolds**  
Yujing Ding, Shanshan Zhang, Henry Hess, Xian Kong, Yifei Zhang  
[bioRxiv 2024.01.31.577620](https://www.biorxiv.org/content/10.1101/2024.01.31.577620v1)/[Advanced Science (2025)](https://advanced.onlinelibrary.wiley.com/doi/10.1002/advs.202500859) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/01/31/2024.01.31.577620/DC1/embed/media-1.pdf) • RFjoint/ProteinMPNN-based

**Accurate single domain scaffolding of three non-overlapping protein epitopes using deep learning**
Karla M Castro, Joseph L Watson, Jue Wang, Joshua Southern, Reyhaneh Ayardulabi, Sandrine Georgeon, Stephane Rosset, David Baker, Bruno E Correia
[bioRxiv 2024.05.07.592871](https://www.biorxiv.org/content/10.1101/2024.05.07.592871v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/05/10/2024.05.07.592871/DC1/embed/media-1.pdf)

**Diversifying de novo TIM barrels by hallucination**
Beck, Julian, Sooruban Shanmugaratnam, and Birte Höcker
[Protein Science 33.6 (2024)](https://onlinelibrary.wiley.com/doi/10.1002/pro.5001)

**De novo designed proteins neutralize lethal snake venom toxins**
Susana Vázquez Torres, Melisa Benard Valle, Stephen P. Mackessy, Stefanie K. Menzies, Nicholas R. Casewell, Shirin Ahmadi, Nick J. Burlet, Edin Muratspahić, Isaac Sappington, Max D.Overath, Esperanza Rivera-de-Torre, Jann Ledergerber, Andreas H. Laustsen, Kim Boddum, Asim K.Bera, Alex Kang,Evans Brackenbrough, Iara A. Cardoso, Edouard P. Crittenden, Rebecca J.Edge, Justin Decarreau, Robert J. Ragotte, Arvind S. Pillai, Mohamad Abedi, Hannah L. Han,Stacey R. Gerben, Analisa Murray, Rebecca Skotheim, Lynda Stuart, Lance Stewart, Thomas J.A. Fryer, Timothy P. Jenkins, David Baker
[PREPRINT (Version 1) available at Research Square](https://www.researchsquare.com/article/rs-4402792/v1)/[Nature (2025)](https://www.nature.com/articles/s41586-024-08393-x)

**Controlling semiconductor growth with structured de novo protein interfaces**
Amijai Saragovi, Harley Pyles, Paul Kwon, Nikita Hanikel, Fátima A. Dávila-Hernández, Asim K. Bera, Alex Kang, Evans Brackenbrough, Dionne K. Vafeados, Aza Allen, Lance Stewart, David Baker
[bioRxiv 2024.06.24.600095](https://www.biorxiv.org/content/10.1101/2024.06.24.600095v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/06/25/2024.06.24.600095/DC1/embed/media-1.pdf)

**Diffusing protein binders to intrinsically disordered proteins**
Caixuan Liu, Kejia Wu, Hojun Choi, Hannah Han, Xueli Zhang, Joseph L Watson, Sara Shijo, Asim K Bera, Alex Kang, Evans Brackenbrough, Brian Coventry, Derrick R Hick, Andrew N Hoofnagle, Ping Zhu, Xingting Li, Justin Decarreau, Stacey R Gerben, Wei Yang, Xinru Wang, Mila Lamp, Analisa Murray, Magnus Bauer, David Baker
[bioRxiv 2024.07.16.603789](https://www.biorxiv.org/content/10.1101/2024.07.16.603789v1)/[Nature (2025)](https://www.nature.com/articles/s41586-025-09248-9) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/07/16/2024.07.16.603789/DC1/embed/media-1.mov)

**Parametrically guided design of beta barrels and transmembrane nanopores using deep learning**
David E. Kim, Joseph L. Watson, David Juergens, Sagardip Majumder, Stacey R. Gerben, Alex Kang, Asim K. Bera, Xinting Li, David Baker
[bioRxiv 2024.07.22.604663](https://www.biorxiv.org/content/10.1101/2024.07.22.604663v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/07/23/2024.07.22.604663/DC1/embed/media-1.pdf) • [code1](https://github.com/davidekim/parametric_barrels), [code2](https://github.com/sagardipm/denovoPores)

**Computational design of highly active de novo enzymes**
Markus Braun, Adrian Tripp, Morakot Chakatok, Sigrid Kaltenbrunner, Massimo G. Totaro, David Stoll, Aleksandar Bijelic, Wael Elaily, Shlomo Yakir Yakir Hoch, Matteo Aleotti, Melanie Hall, Gustav Oberdorfer
[bioRxiv 2024.08.02.606416](https://www.biorxiv.org/content/10.1101/2024.08.02.606416v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/08/03/2024.08.02.606416/DC1/embed/media-1.pdf)

**Computational design of serine hydrolases**
Anna Lauko, Samuel J Pellock, Ivan Anischanka, Kiera H Sumida, David Juergens, Woody Ahern, Alex Shida, Andrew Hunt, Indrek Kalvet, Christoffer Norn, Ian R Humphreys, Cooper S Jamieson, Alex Kang, Evans Brackenbrough, Banumathi Sankaran, K N Houk, David Baker
[bioRxiv 2024.08.29.610411](https://www.biorxiv.org/content/10.1101/2024.08.29.610411v1)/[Science0,eadu2454](https://www.science.org/doi/10.1126/science.adu2454) • [news](https://www.asimov.press/p/ai-enzymes)

**De novo design of Ras isoform selective binders**
Jason Zhaoxing Zhang, Xinting Li, Caixuan Liu, Hanlun Jiang, Kejia Wu, David Baker
[bioRxiv 2024.08.29.610300](https://www.biorxiv.org/content/10.1101/2024.08.29.610300v1)

**Improved protein binder design using beta-pairing targeted RFdiffusion**
Isaac Sappington, Martin Toul, David S. Lee, Stephanie A. Robinson, Inna Goreshnik, Clara McCurdy, Tung Ching Chan, Nic Buchholz, Buwei Huang, Dionne Vafeados, Mariana Garcia-Sanchez, Nicole Roullier, Matthias Glögl, Chris Kim, Joseph L. Watson, Susana Vázquez Torres, Koen H. G. Verschueren, Kenneth Verstraete, Cynthia S. Hinck, Melisa Benard-Valle, Brian Coventry, Jeremiah Nelson Sims, Green Ahn, Xinru Wang, Andrew P. Hinck, Timothy P. Jenkins, Hannele Ruohola-Baker, Steven M. Banik, Savvas N. Savvides, David Baker
[bioRxiv 2024.10.11.617496](https://www.biorxiv.org/content/10.1101/2024.10.11.617496v1)/[preprint](https://assets-eu.researchsquare.com/files/rs-5473963/v1_covered_81143f0e-3579-4f09-86c3-c0e316288e3a.pdf) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/10/12/2024.10.11.617496/DC1/embed/media-1.pdf)

**Afpdb–an efficient structure manipulation package for AI protein design**
Yingyao Zhou, Jiayi Cox, Bin Zhou, Steven Zhu, Yang Zhong, Glen Spraggon
[Bioinformatics (2024): btae654](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btae654/7876263) • [code](https://github.com/data2code/afpdb) • [website](https://pypi.org/project/afpdb)

**GRACE: Generative Redesign in Artificial Computational Enzymology**
Ruei-En, HuChi-Hua, Yu I-Son Ng
[ACS Synthetic Biology (2024)](https://pubs.acs.org/doi/10.1021/acssynbio.4c00624) • [code](https://github.com/Ryan-Hu-Hu-Hu/GRACE)

**Computational Design of Metallohydrolases**
Donghyo Kim, Seth M. Woodbury, Woody Ahern, Indrek Kalvet, Nikita Hanikel, Saman Salike, Samuel J. Pellock, Anna Lauko, Donald Hilvert, David Baker
[bioRxiv 2024.11.13.623507](https://www.biorxiv.org/content/10.1101/2024.11.13.623507v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/11/14/2024.11.13.623507/DC1/embed/media-1.pdf)

**Design of facilitated dissociation enables control over cytokine signaling duration**
Adam J. Broerman, Christoph Pollmann, Mauriz A. Lichtenstein, Mark D. Jackson, Maxx H. Tessmer, Won Hee Ryu, Mohamad H. Abedi, Danny D. Sahtoe, Aza Allen, Alex Kang, Joshmyn De La Cruz, Evans Brackenbrough, Banumathi Sankaran, Asim K. Bera, Daniel M. Zuckerman, Stefan Stoll, Florian Praetorius, Jacob Piehler, David Baker
[bioRxiv 2024.11.15.623900](https://www.biorxiv.org/content/10.1101/2024.11.15.623900v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/11/16/2024.11.15.623900/DC1/embed/media-1.pdf)

**Accurate de novo design of high-affinity protein binding macrocycles using deep learning**
Stephen A. Rettie, David Juergens, Victor Adebomi, Yensi Flores Bueso, Qinqin Zhao, Alexandria N. Leveille, Andi Liu, Asim K. Bera, Joana A. Wilms, Alina Üffing, Alex Kang, Evans Brackenbrough, Mila Lamb, Stacey R. Gerben, Analisa Murray, Paul M. Levine, Maika Schneider, Vibha Vasireddy, Sergey Ovchinnikov, Oliver H. Weiergräber, Dieter Willbold, Joshua A. Kritzer, Joseph D. Mougous, David Baker, Frank DiMaio, Gaurav Bhardwaj
[bioRxiv 2024.11.18.622547](https://www.biorxiv.org/content/10.1101/2024.11.18.622547v1)/[Nat Chem Biol (2025)](https://www.nature.com/articles/s41589-025-01929-w) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/11/18/2024.11.18.622547/DC1/embed/media-1.zip) • [code](https://zenodo.org/records/15264344)

**Engineering de novo binder CAR-T cell therapies with generative AI**
Markus Mergen, Daniela Abele, Naile Koleci, Alba Schmahl Fernandez, Maya Sugden, Noah Holzleitner, Andreas Carr, Leonie Rieger, Valentina Leone, Maximilian Reichert, Karl-Ludwig Laugwitz, Florian Bassermann, Dirk H. Busch, Julian Grünewald, Andrea Schmidts
[bioRxiv 2024.11.25.625151](https://www.biorxiv.org/content/10.1101/2024.11.25.625151v1) • RFDiffusion/ProteinMPNN-based

**CycleDesigner: Leveraging RFdiffusion and HighFold to Design Cyclic Peptide Binders for Specific Targets**
Chenhao Zhang, Zhenyu Xu, Kang Lin, Chengyun Zhang, Wen Xu, Hongliang Duan
[bioRxiv 2024.11.27.625581](https://www.biorxiv.org/content/10.1101/2024.11.27.625581v1) • RFDiffusion/ProteinMPNN-based

**De novo designed pMHC binders facilitate T cell induced killing of cancer cells**
Kristoffer Haurum Johansen, Darian Stephan Wolff, Beatrice Scapolo, Monica L. Fernández Quintero, Charlotte Risager Christensen, Johannes R. Loeffler, Esperanza Rivera-de-Torre, Max D. Overath, Kamilla Kjærgaard Munk, Oliver Morell, Marie Christine Viuff, Alberte T. Damm Englund, Mathilde Due, Stefano Forli, Emma Qingjie Andersen, Jordan Sylvester Fernandes, Suthimon Thumtecho, Andrew B. Ward, Maria Ormhøj, Sine Reker Hadrup, Timothy P. Jenkins
[bioRxiv 2024.11.27.624796](https://www.biorxiv.org/content/10.1101/2024.11.27.624796v1)/[Science389,380-385(2025)](https://www.science.org/doi/10.1126/science.adv0422) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/03/2024.11.27.624796/DC1/embed/media-1.pdf)

**Design of high specificity binders for peptide-MHC-I complexes**  
Bingxu Liu, Nathan F. Greenwood, Julia E. Bonzanini, Amir Motmaen, Jazmin Sharp, Chunyu Wang, Gian Marco Visani, Dionne K. Vafeados, Nicole Roullier, Armita Nourmohammad, K. Christopher Garcia, David Baker  
[bioRxiv 2024.11.28.625793](https://www.biorxiv.org/content/10.1101/2024.11.28.625793v1)/[Science389,386-391(2025)](https://www.science.org/doi/10.1126/science.adv0185)

**Target-conditioned diffusion generates potent TNFR superfamily antagonists and agonists**
Matthias Glögl, Aditya Krishnakumar, Robert J. Ragotte, Inna Goreshnik, Brian Coventry, Asim K. Bera, Alex Kang, Emily Joyce, Green Ahn, Buwei Huang, Wei Yang, Wei Chen, Mariana Garcia Sanchez, Brian Koepnick, David Baker
[Science 386.6726 (2024)](https://www.science.org/doi/10.1126/science.adp1779)

**Design of a Water-Soluble CD20 Antigen with Computational Epitope Scaffolding**
Zhiyuan Yao, Brian Kuhlman
[bioRxiv 2024.12.05.627087](https://www.biorxiv.org/content/10.1101/2024.12.05.627087v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/06/2024.12.05.627087/DC1/embed/media-1.pdf) • [code](https://www.biorxiv.org/content/biorxiv/early/2024/12/06/2024.12.05.627087/DC2/embed/media-2.zip) • RFDiffusion-based

**Inhibiting heme-piracy by pathogenic Escherichia coli using de novo-designed proteins**
Daniel R Fox, Kazem Asadollahi, Imogen G Samuels, Bradley Spicer, Ashleigh Kropp, Chris Lupton, Kevin Lim, Chunxiao Wang, Hariprasad Venugopal, Marija Dramicanin, Gavin J Knott, Rhys Grinter
[bioRxiv 2024.12.05.626953](https://www.biorxiv.org/content/10.1101/2024.12.05.626953v1)/[Nat Commun 16, 6066 (2025)](https://www.nature.com/articles/s41467-025-60612-9) • RFDiffusion/ProteinMPNN-based

**De novo design of potent CRISPR-Cas13 inhibitors**
Cyntia Taveneau, Her Xiang Chai, Jovita D'Silva, Rebecca S Bamert, Brooke K Hayes, Roland W Calvert, Daniel J Curwen, Fabian Munder, Lisandra L Martin, Jeremy J Barr, Rhys Grinter, Gavin J Knott
[bioRxiv 2024.12.05.626932](https://www.biorxiv.org/content/10.1101/2024.12.05.626932v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/06/2024.12.05.626932/DC1/embed/media-1.pdf) • RFDiffusion/ProteinMPNN-based

**Development of a De Novo Protein Binder that Inhibits the Alpha Kinase eEF2K**
Kody A Klupt, Ethan Belrose, Zongchao Jia
[bioRxiv 2024.12.10.627789](https://www.biorxiv.org/content/10.1101/2024.12.10.627789v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/11/2024.12.10.627789/DC1/embed/media-1.pdf) • RFDiffusion/ProteinMPNN-based

**Generating and evaluating diverse sequences for protein backbones**
Yo Akiyama, Sergey Ovchinnikov
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/Generating_and_evaluating_diverse_sequences_for_protein_backbones.pdf) • RFDiffusion/ProteinMPNN-based

**De novo design and structure of a peptide-centric TCR mimic binding module**
Karsten D. Householder, Xinyu Xiang, Kevin M. Jude, Arthur Deng, Matthias Obenaus, Steven C. Wilson, Xiaojing Chen, Nan Wang, K. Christopher Garcia
[bioRxiv 2024.12.16.628822](https://www.biorxiv.org/content/10.1101/2024.12.16.628822v1)/[Science389,375-379(2025)](https://www.science.org/doi/10.1126/science.adv3813) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/20/2024.12.16.628822/DC1/embed/media-1.pdf) • RFDiffusion/ProteinMPNN-based

**Bottom-up design of calcium channels from defined selectivity filter geometry**
Yulai Liu, Connor Weidle, Ljubica Mihaljevic, Joseph L. Watson, Zhe Li, Le Tracy Yu, Sagardip Majumder, Andrew J. Borst, Kenneth D. Carr, Ryan D. Kibler, Tamer M. Gamal El-Din, William A. Catterall, David Baker
[bioRxiv 2024.12.19.629320](https://www.biorxiv.org/content/10.1101/2024.12.19.629320v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/12/20/2024.12.19.629320/DC1/embed/media-1.pdf) • RFDiffusion/ProteinMPNN-based

**Solubilization of Membrane Proteins using designed protein WRAPS**
Ljubica Mihaljević, David E. Kim, Helen E. Eisenach, Pooja D. Bandawane, Andrew J. Borst, Alexis Courbet, Everton Bettin, Qiushi Liu, Connor Weidle, Sagardip Majumder, Xinting Li, Mila Lamb, Analisa Nicole Azcárraga Murray, Rashmi Ravichandran, Elizabeth C. Williams, Shuyuan Hu, Lynda Stuart, Linda Grillová, Nicholas R. Thomson, Pengxiang Chang, Melissa J. Caimano, Kelly L. Hawley, Neil P. King, David Baker
[bioRxiv 2025.02.04.636539](https://www.biorxiv.org/content/10.1101/2025.02.04.636539v1) • RFDiffusion/ProteinMPNN-based

**Inhibition of ice recrystallization with designed twistless helical repeat proteins**
Robbert J. de Haas, Harley Pyles, Timothy F. Huddy, Jannick van Ossenbruggen, Chuanbao Zheng, Daniëlle van den Broek, Ann Carr, Asim K. Bera, Alex Kang, Evans Brackenbrough, Emily Joyce, Banumathi Sankaran, David Baker, Ilja K. Voets, Renko de Vries
[bioRxiv 2025.03.09.642278](https://www.biorxiv.org/content/10.1101/2025.03.09.642278v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/03/13/2025.03.09.642278/DC1/embed/media-1.pdf) • [code](https://doi.org/10.5281/zenodo.13763849) • RFDiffusion/ProteinMPNN-based

**RoseTTAFold diffusion-guided short peptide design: a case study of binders against Keap1/Nrf2**
Francesco Morena, Chiara Cencinia, Carla Emiliani, Sabata Martinoa
[Computational and Structural Biotechnology Journal (2025)](https://www.csbj.org/article/S2001-0370(25)00061-3/fulltext) • RFDiffusion/ProteinMPNN-based

**De novo design of miniprotein agonists and antagonists targeting G protein-coupled receptors**
Edin Muratspahić, David Feldman, David E. Kim, Xiangli Qu, Ana-Maria Bratovianu, Paula Rivera-Sánchez, Federica Dimitri, Jason Cao, Brian P. Cary, Matthew J. Belousoff, Peter Keov, Qingchao Chen, Yue Ren, Justyn Fine, Isaac Sappington, Thomas Schlichthaerle, Jason Z. Zhang, Arvind Pillai, Ljubica Mihaljević, Magnus Bauer, Susana Vázquez Torres, Amir Motmaen, Gyu Rie Lee, Long Tran, Xinru Wang, Inna Goreshnik, Dionne K. Vafeados, Justin E. Svendsen, Parisa Hosseinzadeh, Nicolai Lindegaard, Matthäus Brandt, Yann Waltenspühl, Kristine Deibler, Luke Oostdyk, William Cao, Lakshmi Anantharaman, Lance Stewart, Lauren Halloran, Jamie B. Spangler, Patrick M. Sexton, Bryan L. Roth, Brian E. Krumm, Denise Wootten, Christopher G. Tate, Christoffer Norn, David Baker
[bioRxiv 2025.03.23.644666](https://www.biorxiv.org/content/10.1101/2025.03.23.644666v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/03/23/2025.03.23.644666/DC1/embed/media-1.pdf)

**Atom level enzyme active site scaffolding using RFdiffusion2**
Woody Ahern, Jason Yim, Doug Tischer, Saman Salike, Seth Woodbury, Donghyo Kim, Indrek Kalvet, Yakov Kipnis, Brian Coventry, Han Altae-Tran, Magnus Bauer, Regina Barzilay, Tommi Jaakkola, Rohith Krishna, David A Baker
[bioRxiv 2025.04.09.648075](https://www.biorxiv.org/content/10.1101/2025.04.09.648075v2) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/04/10/2025.04.09.648075.1/DC1/embed/media-1.pdf) • [lecture](https://www.youtube.com/watch?v=bd6bFXRmEGA&pp=ygUMcmZkaWZmdXNpb24y) • [code](https://github.com/RosettaCommons/RFdiffusion2)

**Generative protein design meets synthetic porphyrin assembly**
Hiroaki Inaba, Hiroki Onoda, Takayuki Uchihashi, Atsunori Oshima and Osami Shoji
[ChemRxiv. 2025](https://chemrxiv.org/engage/chemrxiv/article-details/67f4f96381d2151a0284768f) • RFDiffusion/ProteinMPNN-based

**Development of AI-designed protein binders for detection and targeting of cancer cell surface proteins**  
Bianca Broske, Sophie C. Binder, Benjamin A. McEnroe, Tim N. Kempchen, Caroline I. Fandrey, Julia M. Messmer, Elisabeth Tan, Peter Konopka, Dominic Ferber, Michelle C. R. Yong, Marie Kleinert, Alexander Hoch, Katja Blumenstock, Jan M. P. Tödtmann, Johannes Oldenburg, Heiko Rühl, Alexander Semaan, Marieta I. Toma, Kristina Markova, Sebastian Kobold, Tim Rollenske, Matthias Geyer, Stephan Menzel, Tobias Bald, Jonathan L. Schmid-Burgk, Gregor Hagelueken, Michael Hölzel  
[bioRxiv 2025.05.11.652819](https://www.biorxiv.org/content/10.1101/2025.05.11.652819v1) • [code](https://github.com/HoelzelLab/IEO_AI_Binder_cancer_surface_2025) • RFDiffusion/ProteinMPNN-based

**Poxvirus targeted by RFdiffusion peptide-binders**  
J. Coll  
[bioRxiv 2025.05.14.654163](https://www.biorxiv.org/content/10.1101/2025.05.14.654163v1) • RFDiffusion/ProteinMPNN-based

**AI assisted design of ligands for Lipocalin-2**  
Jacopo Sgrignani, Sara Buscarini, Patrizia Locatelli, Concetta Guerra, Alberto Furlan, Yingyi Chen, Giada Zoppi, Andrea Cavalli  
[bioRxiv 2025.05.18.654718](https://www.biorxiv.org/content/10.1101/2025.05.18.654718v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/05/19/2025.05.18.654718/DC1/embed/media-1.docx) • RFDiffusion/ProteinMPNN-based

**De novo luciferases enable multiplexed bioluminescence imaging**  
Julie Yi-Hsuan Chen, Qing Shi, Xue Peng, Jean de Dieu Habimana, James Wang, William Sobolewski, Andy Hsien-Wei Yeh  
[Chem 11.3 (2025)](https://www.cell.com/chem/fulltext/S2451-9294(24)00539-4) • RFjoint/ProteinMPNN-based

**Bioinformatics classification of the MgtE Mg2+ channel and de novo protein design for the stabilization of its novel subclass**  
Zhixuan Zhao, Kimiho Omae, Wataru Iwasaki, Ziyi Zhang, Fazhi Pan, Eun-Jin Lee, Motoyuki Hattori  
[bioRxiv 2025.05.26.656215](https://www.biorxiv.org/content/10.1101/2025.05.26.656215v1) • [code](https://github.com/0mae/mgte_short) • RFDiffusion/ProteinMPNN-based

**De Novo Structure-Based Design of TEM-171 β-Lactamase Protein Inhibitors Using Integrated Deep Learning and Multi-Scale Simulations to Combat Bacterial Resistance**  
Krishiv Potluri  
[bioRxiv 2025.06.23.661177](https://www.biorxiv.org/content/10.1101/2025.06.23.661177v1) • [code](https://github.com/kishpish/tem171-inhibitor-pipeline) • RFDiffusion/ProteinMPNN-based

**Generation of structure-guided pMHC-I libraries using Diffusion Models**  
Sergio Mares, Ariel Espinoza Weinberger, Nilah M. Ioannidis  
[arXiv:2507.08902](https://arxiv.org/abs/2507.08902v1) • [code](https://github.com/sermare/struct-mhc-dev) • RFDiffusion/ProteinMPNN-based

**De novo design of a fusion protein tool for GPCR research**  
Kaixuan Gao, Xin Zhang, Jia Nie, Hengyu Meng, Weishe Zhang, Boxue Tian, and Xiangyu Liu  
[Proceedings of the National Academy of Sciences 122.29 (2025)](https://www.pnas.org/doi/10.1073/pnas.2422360122)

**CycleDesigner: Leveraging CycRFdiffusion and HighFold to Design Cyclic Peptide Binders for Specific Targets**  
Chenhao ZhangZhenyu XuKang LinNing ZhuChengyun ZhangWen XuJingjing GuoAn SuChengxi LiHongliang Duan  
[J. Chem. Inf. Model. 2025](https://pubs.acs.org/doi/10.1021/acs.jcim.5c00227)

**AI-generated MLH1 small binder improves prime editing efficiency**  
Ju-Chan Park, Heesoo Uhm, Yong-Woo Kim, Ye Eun Oh, Jang Hyeon Lee, Jiyun Yang, Kyoungmi Kim, Sangsu Bae  
[Cell (2025)](https://www.cell.com/cell/fulltext/S0092-8674(25)00799-8) • [code](https://github.com/baelab/PE-SB)

**De novo design of light-regulated dynamic proteins using deep learning**  
PATRICK BARTH, Lorenzo Scutteri, Luciano Abriata, Shuhao Zhang, Aysima Hacisuleyman, Kelvin Lau, Florence Pojer, Sahand Jamal Rahi  
[bioRxiv 2025.08.12.669910](https://www.biorxiv.org/content/10.1101/2025.08.12.669910v1) • RFDiffusion/ProteinMPNN-based

**De Novo Design of Miniprotein Inhibitors of Bacterial Adhesins**  
Adam M. Chazin-Gray, Tuscan R. Thompson, Edward D. B. Lopatto, Pearl Magala, Patrick W. Erickson, Andrew C. Hunt, Anna Manchenko, Pavel Aprikian, Veronika Tchesnokova, Irina Basova, Denise A. Sanick, Kevin O. Tamadonfar, Morgan R. Timm, Jerome S. Pinkner, Karen W. Dodson, Alex Kang, Emily Joyce, Asim K. Bera, Aaron J. Schmitz, Ali H. Ellebedy, Kelli L. Hvorecny, Mark J. Cartwright, Andyna Vernet, Sarai Bardales, Desmond White, Rachel E. Klevit, Evgeni V. Sokurenko, Scott J. Hultgren, David Baker  
[bioRxiv 2025.08.18.670751](https://www.biorxiv.org/content/10.1101/2025.08.18.670751v1) • RFDiffusion/ProteinMPNN-based

**Computationally Designed Nanobinders as Affinity Ligands in Diagnostic and Therapeutic Applications**
Jueun Jeon, Q. John Liu, Hyunkyung Woo, Isabel Barth, Yoonjeong Choi, L. Jessica Sang, Hakho Lee  
[J. Am. Chem. Soc.(2025)](https://pubs.acs.org/doi/10.1021/jacs.5c11289)  • RFDiffusion/ProteinMPNN-based

### 6.4 CNN-based

**De Novo Design of Site-specific Protein Binders Using Surface Fingerprints**
Pablo Gainza, Sarah Wehrle, Alexandra Van Hall-Beauvais, Anthony Marchand, Andreas Scheck, Zander Harteveld, Stephen Buckley, Dongchun Ni, Shuguang Tan, Freyr Sverrisson, Casper Goverde, Priscilla Turelli, Charlène Raclot, Alexandra Teslenko, Martin Pacesa, Stéphane Rosset, Sandrine Georgeon, Jane Marsden, Aaron Petruzzella, Kefang Liu, Zepeng Xu, Yan Chai, Pu Han, George F. Gao, Elisa Oricchio, Beat Fierz, Didier Trono, Henning Stahlberg, Michael Bronstein, Bruno E. Correia
[Protein Science 30.CONF (2021)](https://infoscience.epfl.ch/record/290120)/[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.06.16.496402v2)/[Nature (2023)](https://www.nature.com/articles/s41586-023-05993-x) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2022/06/17/2022.06.16.496402/DC1/embed/media-1.pdf) • [masif_seed](https://github.com/LPDI-EPFL/masif_seed) • [masif](https://github.com/LPDI-EPFL/masif) • [lecture](https://www.youtube.com/watch?v=4S4J7gbhAa0)

**Targeting protein-ligand neosurfaces using a generalizable deep learning approach**
Anthony Marchand, Stephen Buckley, Arne Schneuing, Martin Pacesa, Pablo Gainza, Evgenia Elizarova, Rebecca Manuela Neeser, Pao-Wan Lee, Luc Reymond, Maddalena Elia, Leo Scheller, Sandrine Georgeon, Joseph Schmidt, Philippe Schwaller, Sebastian Josef Maerkl, Michael Bronstein, Bruno Emmanuel Correia
[bioRxiv 2024.03.25.585721](https://www.biorxiv.org/content/10.1101/2024.03.25.585721v1)/[Nature (2025)](https://www.nature.com/articles/s41586-024-08435-4) • [Supplementary](https://static-content.springer.com/esm/art%3A10.1038%2Fs41586-024-08435-4/MediaObjects/41586_2024_8435_MOESM1_ESM.pdf) • [code](https://github.com/LPDI-EPFL/masif-neosurf) • [lecture](https://www.youtube.com/watch?v=setIzkcEAVs)

**Mapping targetable sites on the human surfaceome for the design of novel binders**
Petra E. M. Balbi, Ahmed Sadek, Anthony Marchand, Ta-Yi Yu, Jovan Damjanovic, Sandrine Georgeon, Joseph Schmidt, Simone Fulle, Che Yang, Hamed Khakzad, Bruno E. Correia
[bioRxiv 2024.12.16.628626](https://www.biorxiv.org/content/10.1101/2024.12.16.628626v1)• [code](https://github.com/hamedkhakzad/SURFACE-Bind)

**Design of pseudosymmetric protein hetero-oligomers**
Ryan D. Kibler, Sangmin Lee, Madison A. Kennedy, Basile I. M. Wicky, Stella M. Lai, Marius M. Kostelic, Ann Carr, Xinting Li, Cameron M. Chow, Tina K. Nguyen, Lauren Carter, Vicki H. Wysocki, Barry L. Stoddard & David Baker
[Nat Commun 15, 10684 (2024)](https://www.nature.com/articles/s41467-024-54913-8) • [code](https://github.com/rdkibler/Stepwise-design-of-pseudosymmetric-protein-hetero-oligomers)

### 6.5 GNN-based

**Iterative refinement graph neural network for antibody sequence-structure co-design**
Wengong Jin, Jeremy Wohlwend, Regina Barzilay, Tommi Jaakkola
[arXiv preprint arXiv:2110.04624 (2021)](https://arxiv.org/abs/2110.04624) • [RefineGNN](https://github.com/wengong-jin/RefineGNN) • [lecture1](https://www.youtube.com/watch?v=uDTccbg_Ai4), [lecture2](https://www.youtube.com/watch?v=px5iC79jtfc)

**Antibody Complementarity Determining Regions (CDRs) design using Constrained Energy Model**
Fu, Tianfan, and Jimeng Sun
[Proceedings of the 28th ACM SIGKDD Conference on Knowledge Discovery and Data Mining. 2022](https://dl.acm.org/doi/abs/10.1145/3534678.3539285) • [code](https://github.com/futianfan/energy_model4antibody_design)

**Conditional Antibody Design as 3D Equivariant Graph Translation**
Xiangzhe Kong, Wenbing Huang, Yang Liu
[ICLR 2023](https://openreview.net/forum?id=LFHFQbjxIiP)/[arXiv:2208.06073](https://arxiv.org/abs/2208.06073)

**End-to-End Full-Atom Antibody Design**
Xiangzhe Kong, Wenbing Huang, Yang Liu
[arXiv:2302.00203](https://arxiv.org/abs/2302.00203) • [code](https://github.com/THUNLP-MT/dyMEAN)

**AbODE: Ab Initio Antibody Design using Conjoined ODEs**
Yogesh Verma, Markus Heinonen, Vikas Garg
[arXiv:2306.01005](https://arxiv.org/abs/2306.01005)

**Joint Design of Protein Sequence and Structure based on Motifs**
Zhenqiao Song, Yunlong Zhao, Yufei Song, Wenxian Shi, Yang Yang, Lei Li
[arXiv:2310.02546](https://arxiv.org/abs/2310.02546)

**De novo protein design using geometric vector field networks**
Weian Mao, Muzhi Zhu, Zheng Sun, Shuaike Shen, Lin Yuanbo Wu, Hao Chen, Chunhua Shen
[arXiv:2310.11802](https://arxiv.org/abs/2310.11802)/[ICLR 2024](https://openreview.net/forum?id=9UIGyJJpay)

**A Survey of Geometric Graph Neural Networks: Data Structures, Models and Applications**
Jiaqi Han, Jiacheng Cen, Liming Wu, Zongzhao Li, Xiangzhe Kong, Rui Jiao, Ziyang Yu, Tingyang Xu, Fandi Wu, Zihe Wang, Hongteng Xu, Zhewei Wei, Yang Liu, Yu Rong, Wenbing Huang
[arXiv:2403.00485](https://arxiv.org/abs/2403.00485) • review

**GeoAB: Towards Realistic Antibody Design and Reliable Affinity Maturation**
Haitao LIN, Lirong Wu, Huang Yufei, Yunfan Liu, Odin Zhang, Yuanqing Zhou, Rui Sun, Stan Z Li
[bioRxiv 2024.05.15.594274](https://www.biorxiv.org/content/10.1101/2024.05.15.594274v1)/[ICML 2024](https://openreview.net/forum?id=6pHP51F55x) • [code](https://github.com/Edapinenut/GeoAB)

**Topological Neural Networks go Persistent, Equivariant, and Continuous**
Yogesh Verma, Amauri H Souza, Vikas Garg
[arXiv:2406.03164](https://arxiv.org/abs/2406.03164) • [code](https://github.com/Aalto-QuML/TopNets)

**Relation-Aware Equivariant Graph Networks for Epitope-Unknown Antibody Design and Specificity Optimization**
Lirong Wu, Haitao Lin, Yufei Huang, Zhangyang Gao, Cheng Tan, Yunfan Liu, Tailin Wu, Stan Z. Li
[arXiv:2501.00013](https://arxiv.org/abs/2501.00013) • [code](https://github.com/LirongWu/RAAD)

**Towards More Accurate Full-Atom Antibody Co-Design**
Jiayang Wu, Xingyi Zhang, Xiangyu Dong, Kun Xie, Ziqi Liu, Wensheng Gan, Sibo Wang, Le Song
[arXiv:2502.19391](https://arxiv.org/abs/2502.19391)/[OpenReiview](https://openreview.net/forum?id=1VLdFJFWhL)

**NanoDesigner: Resolving the complex–CDR interdependency with iterative refinement**
Melissa Maria Rios Zertuche, Şenay Kafkas, Dominik Renn, Magnus Rueping, Robert Hoehndorf
[bioRxiv 2025.02.25.640028](https://www.biorxiv.org/content/10.1101/2025.02.25.640028v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/03/01/2025.02.25.640028/DC1/embed/media-1.pdf) • [code](https://github.com/bio-ontology-research-group/NanoDesigner) • dyMEAN-based

### 6.6 Transformer-based

**Protein Sequence and Structure Co-Design with Equivariant Translation**
Chence Shi, Chuanrui Wang, Jiarui Lu, Bozitao Zhong, Jian Tang
[arXiv:2210.08761](https://arxiv.org/abs/2210.08761)/[ICLR 2023](https://openreview.net/forum?id=pRCMXcfdihq) • [Supplementary](https://openreview.net/attachment?id=pRCMXcfdihq&name=supplementary_material) • [code](https://github.com/shichence/ProtSeed)

**Deep Learning for Flexible and Site-Specific Protein Docking and Design**
Matt McPartlon, Jinbo Xu
[bioRxiv 2023.04.01.535079](https://www.biorxiv.org/content/10.1101/2023.04.01.535079v1) • [code](https://github.com/drorlab/DIPS)

**Full-Atom Protein Pocket Design via Iterative Refinement**
Zaixi Zhang, Zepu Lu, Zhongkai Hao, Marinka Zitnik, Qi Liu
[arXiv:2310.02553](https://arxiv.org/abs/2310.02553) • [code](https://github.com/zaixizhang/FAIR)

**Functional Geometry Guided Protein Sequence and Backbone Structure Co-Design**
Anonymous
[ICLR 2024](https://openreview.net/forum?id=Dr4qD9bzZd)

**Fast and accurate modeling and design of antibody-antigen complex using tFold**
Fandi Wu, Yu Zhao, Jiaxiang Wu, Biaobin Jiang, Bing He, Longkai Huang, Chenchen Qin, Fan Yang, Ningqiao Huang, Yang Xiao, Rubo Wang, Huaxian Jia, Yu Rong, Yuyi Liu, Houtim Lai, Tingyang Xu, Wei Liu, Peilin Zhao, Jianhua Yao
[bioRxiv 2024.02.05.578892](https://www.biorxiv.org/content/10.1101/2024.02.05.578892v1) • [website](https://drug.ai.tencent.com/cn)

**PocketGen: Generating Full-Atom Ligand-Binding Protein Pockets**
Zhang Zaixi, Wanxiang Shen, Qi Liu, Marinka Zitnik
[bioRxiv 2024.02.25.581968](https://www.biorxiv.org/content/10.1101/2024.02.25.581968v1)/[Nature Machine Intelligence, 2024](https://www.nature.com/articles/s42256-024-00920-9) • [code](https://github.com/zaixizhang/PocketGen) • [website](https://zitniklab.hms.harvard.edu/projects/PocketGen/)

**Simulating 500 million years of evolution with a language model**
Thomas Hayes,  Roshan Rao,  Halil Akin,  Nicholas James Sofroniew,  Deniz Oktay,  Zeming Lin, Robert Verkuil, Vincent Quy Tran, Jonathan Deaton, Marius Wiggert, Rohil Badkundri, Irhum Shafkat, Jun Gong, Alexander Derry, Raul Santiago Molina, Neil Thomas, Yousuf Khan, Chetan Mishra, Carolyn Kim, Liam J. Bartie, Patrick D. Hsu, Tom Sercu, Salvatore Candido, Alexander Rives
[preprint](https://evolutionaryscale-public.s3.us-east-2.amazonaws.com/research/esm3.pdf)/[bioRxiv 2024.07.01.600583](https://www.biorxiv.org/content/10.1101/2024.07.01.600583v1)/[Science (2025): eads0018](https://www.science.org/doi/10.1126/science.ads0018) • [website](https://www.evolutionaryscale.ai/blog/esm3-release) • [code](https://github.com/evolutionaryscale/esm) • [colab](https://colab.research.google.com/github/evolutionaryscale/esm/blob/main/examples/generate.ipynb) • [news](https://www.nature.com/articles/d41586-024-02214-x)

**Towards Protein Sequence & Structure Co-Design with Multi-Modal Language Models**  
Stephen Zhewen Lu, Stephen_Zhewen_Lu, Jiarui Lu, Hongyu Guo, Jian Tang  
[ICLR 2025 Workshop LMRL](https://openreview.net/forum?id=QLszcahdXR) • ESM3-based

### 6.7 MLP-based

**Protein Complex Invariant Embedding with Cross-Gate MLP is A One-Shot Antibody Designer**
Cheng Tan, Zhangyang Gao, Stan Z. Li
[arXiv:2305.09480](https://arxiv.org/abs/2305.09480)

**Hotspot-Driven Peptide Design via Multi-Fragment Autoregressive Extension**
Jiahan Li, Tong Chen, Shitong Luo, Chaoran Cheng, Jiaqi Guan, Ruihan Guo, Sheng Wang, Ge Liu, Jian Peng, Jianzhu Ma
[arXiv:2411.18463](https://arxiv.org/abs/2411.18463)

### 6.8 Flow-based

**Generative Flows on Discrete State-Spaces: Enabling Multimodal Flows with Applications to Protein Co-Design**
Andrew Campbell, Jason Yim, Regina Barzilay, Tom Rainforth, Tommi Jaakkola
[arXiv:2402.04997](https://arxiv.org/abs/2402.04997) • [code](https://github.com/andrew-cr/discrete_flow_models) • [lecture](https://www.youtube.com/watch?v=yzc29vhM2Aw)

**PPFlow: Target-Aware Peptide Design with Torsional Flow Matching**
Haitao Lin, Odin Zhang, Huifeng Zhao, Dejun Jiang, Lirong Wu, Zicheng Liu, Yufei Huang, Stan Z. Li
[bioRxiv 2024.03.07.583831](https://www.biorxiv.org/content/10.1101/2024.03.07.583831v1)/[arXiv:2405.06642](https://arxiv.org/abs/2405.06642) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2024/03/08/2024.03.07.583831/DC1/embed/media-1.zip) • [code](https://github.com/EDAPINENUT/ppflow)

**Full-Atom Peptide Design based on Multi-modal Flow Matching**
Jiahan Li, Chaoran Cheng, Zuofan Wu, Ruihan Guo, Shitong Luo, Zhizhou Ren, Jian Peng, Jianzhu Ma
[arXiv:2406.00735](https://arxiv.org/abs/2406.00735) • [code](https://github.com/Ced3-han/PepFlowww)

**AntibodyFlow: Normalizing Flow Model for Designing Antibody Complementarity-Determining Regions**
Bohao Xu, Yanbo Wang, Wenyu Chen, Shimin Shan
[arXiv:2406.13162](https://arxiv.org/abs/2406.13162)

**Generalized Protein Pocket Generation with Prior-Informed Flow Matching**
Zaixi Zhang, Marinka Zitnik, Qi Liu
[arXiv:2409.19520](https://arxiv.org/abs/2409.19520)

**D-Flow: Multi-modality Flow Matching for D-peptide Design**
Fang Wu, Tinson Xu, Shuting Jin, Xiangru Tang, Zerui Xu, James Zou, Brian Hie
[arXiv:2411.10618](https://arxiv.org/abs/2411.10618) • [code](https://github.com/smiles724/PeptideDesign)

**FlowDesign: Improved Design of Antibody CDRs Through Flow Matching and Better Prior Distributions**
Jun Wu, Xiangzhe Kong, Ningguan Sun, Jing Wei, Sisi Shan, Fuli Feng, Feng Wu, Jian Peng, Linqi Zhang, Yang Liu, Jianzhu Ma
[bioRxiv 2024.11.07.622422](https://www.biorxiv.org/content/10.1101/2024.11.07.622422v2)/[Cell Systems (2025)](https://www.cell.com/cell-systems/abstract/S2405-4712(25)00103-6) • [code](https://github.com/nohandsomewujun/FlowDesign)

**Reaction-conditioned De Novo Enzyme Design with GENzyme**
Chenqing Hua, Jiarui Lu, Yong Liu, Odin Zhang, Jian Tang, Rex Ying, Wengong Jin, Guy Wolf, Doina Precup, Shuangjia Zheng
[arXiv:2411.16694](https://arxiv.org/abs/2411.16694) • [code](https://github.com/WillHua127/GENzyme)

**ProteinZen: combining latent and SE(3) flow matching for all-atom protein generation**
Alex Li, Tanja Kortemme
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/ProteinZen:_combining_latent_and_SE(3)_flow_matching_for_all-atom_protein_generation.pdf)

**HelixFlow, SE(3)–equivariant Full-atom Design of Peptides With Flow-matching Models**
Xuezhi Xie, Pedro A Valiente, Jisun Kim, Jin Sub Lee, Philip Kim
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/HelixFlow,_SE(3)–equivariant_Full-atom_Design_of_Peptides_With_Flow-matching_Models.pdf)

**IgFlow: Flow Matching for De Novo Antibody Design**
Sanjay Nagaraj, Amir Shanehsazzadeh, Hyun Park, Jonathan King, Simon Levine
[Machine Learning for Structural Biology Workshop, NeurIPS 2024](https://www.mlsb.io/papers_2024/IgFlow:_Flow_Matching_for_De_Novo_Antibody_Design.pdf)

**Surface-based Peptide Design with Multi-modal Flow Matching**  
Fang Wu, Shuting Jin, xiangxiang Zeng, Jure Leskovec, Jinbo Xu  
[ICLR 2025](https://openreview.net/forum?id=MeCPwqrm19)

**Non-Linear Flow Matching for Full-Atom Peptide Design**
Dengdeng Huang, Shikui Tu
[arXiv:2502.15855](https://arxiv.org/abs/2502.15855)

**dyAb: Flow Matching for Flexible Antibody Design with AlphaFold-driven Pre-binding Antigen**
Cheng Tan, Yijie Zhang, Zhangyang Gao, Yufei Huang, Haitao Lin, Lirong Wu, Fandi Wu, Mathieu Blanchette, Stan. Z. Li
[arXiv:2503.01910](https://arxiv.org/abs/2503.01910) • [code](https://github.com/A4Bio/dyAb)

**GeoFlow-V2: A Unified Atomic Diffusion Model for Protein Structure Prediction and De Novo Design**
BioGeometry Team
[preprint](https://open-res.biogeom.com/geoflow-v2/technical-report.pdf) • [website](https://prot.design/) • commercial

**All-atom inverse protein folding through discrete flow matching**  
Kai Yi, Kiarash Jamali, Sjors HW Scheres  
[ICML 2025 poster](https://openreview.net/forum?id=8tQdwSCJmA)

**Co-Design protein sequence and structure in discrete space via generative flow**  
Sen Yang, Lingli Ju, Cheng Peng, JiangLin Zhou, Yamin Cai, Dawei Feng  
[Bioinformatics, 2025](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btaf248/8123382) • [code](https://github.com/LtECoD/CoFlow) • [model](https://zenodo.org/records/14842367)

**La-Proteina: Atomistic Protein Generation via Partially Latent Flow Matching**  
Tomas Geffner, Kieran Didi, Zhonglin Cao, Danny Reidenbach, Zuobai Zhang, Christian Dallago, Emine Kucukbenli, Karsten Kreis, Arash Vahdat  
[arXiv:2507.09466](https://arxiv.org/abs/2507.09466) • [webstie](https://research.nvidia.com/labs/genair/la-proteina/)

**Design of peptides with non-canonical amino acids using flow matching**  
Jin Sub Lee, Philip M Kim  
[bioRxiv 2025.07.31.667780](https://www.biorxiv.org/content/10.1101/2025.07.31.667780v1)

**Investigating the impacts of sidechains on de-novo protein design**  
Cooper Svajda, Joshua Yuan  
[bioRxiv 2025.08.08.669410](https://www.biorxiv.org/content/10.1101/2025.08.08.669410v1)

### 6.9 AlphaFold-based

**CarbonNovo: Joint Design of Protein Structure and Sequence Using a Unified Energy-based Model**
Ren, Milong, Tian Zhu, and Haicang Zhang
[ICML 2024](https://openreview.net/forum?id=FSxTEvuFa7) • [code](https://github.com/zhanghaicang/carbonmatrix_public)

**P(all-atom) Is Unlocking New Path For Protein Design**
Wei Qu, Jiawei Guan, Rui Ma, Ke Zhai, Weikun Wu, Haobo Wang
[bioRxiv 2024.08.16.608235](https://www.biorxiv.org/content/10.1101/2024.08.16.608235v1) • [code](https://github.com/levinthal/Pallatom) • [news](https://mp.weixin.qq.com/s/j86-ncoYMM2gfbvTJX6I7w)

**EnzymeFlow: Generating Reaction-specific Enzyme Catalytic Pockets through Flow-Matching and Co-Evolutionary Dynamics**
Chenqing Hua
paper not available • [code](https://github.com/WillHua127/EnzymeFlow)

**IgGM: A Generative Model for Functional Antibody and Nanobody Design**
Rubo Wang, Fandi Wu, Xingyu Gao, Jiaxiang Wu, Peilin Zhao, Jianhua Yao
[bioRxiv 2024.09.19.613838](https://www.biorxiv.org/content/10.1101/2024.09.19.613838v1) • [code](https://github.com/TencentAI4S/IgGM)

**An All-Atom Generative Model for Designing Protein Complexes**
Ruizhe Chen, Dongyu Xue, Xiangxin Zhou, Zaixiang Zheng, Xiangxiang Zeng, Quanquan Gu
[arXiv:2504.13075](https://arxiv.org/abs/2504.13075) • [code](https://github.com/bytedance/apm)

**Repurposing AlphaFold3-like Protein Folding Models for Antibody Sequence and Structure Co-design**  
Nianzu Yang, Nianzu_Yang, Jian Ma, Songlin Jiang, Huaijin Wu, Shuangjia Zheng, Wengong Jin, Junchi Yan  
[OpenReview](https://openreview.net/forum?id=Ja2le9YnqN)

## 7. Other tasks

### 7.1 Effects of mutation & Fitness Landscape

**Deep generative models of genetic variation capture the effects of mutations**
Adam J. Riesselman, John B. Ingraham & Debora S. Marks
[Nature Methods](https://www.nature.com/articles/s41592-018-0138-4) • [code::DeepSequence](https://github.com/debbiemarkslab/DeepSequence) • Oct 2018

**Deciphering protein evolution and fitness landscapes with latent space models**
Xinqiang Ding, Zhengting Zou & Charles L. Brooks III
[Nature Communications](https://www.nature.com/articles/s41467-019-13633-0) • [code::PEVAE](https://github.com/xqding/PEVAE_Paper) • Dec 2019

**Is transfer learning necessary for protein landscape prediction?**
Shanehsazzadeh, Amir, David Belanger, and David Dohan
[arXiv preprint arXiv:2011.03443 (2020)](https://arxiv.org/abs/2011.03443)

**Epistatic Net allows the sparse spectral regularization of deep neural networks for inferring fitness functions**
Amirali Aghazadeh, Hunter Nisonoff, Orhan Ocal, David H. Brookes, Yijie Huang, O. Ozan Koyluoglu, Jennifer Listgarten & Kannan Ramchandran
[Nature Communications](https://www.nature.com/articles/s41467-021-25371-3) • [code](https://github.com/amirmohan/epistatic-net) • Sep 2021

**The generative capacity of probabilistic protein sequence models**
Francisco McGee, Sandro Hauri, Quentin Novinger, Slobodan Vucetic, Ronald M. Levy, Vincenzo Carnevale & Allan Haldane
[Nature Communications](https://www.nature.com/articles/s41467-021-26529-9) • [code::generation_capacity_metrics](https://github.com/alagauche/generative_capacity_metrics) • [code::sVAE](https://github.com/ahaldane/MSA_VAE) • Nov 2021

**Learning the local landscape of protein structures with convolutional neural networks**
Anastasiya V. Kulikova, Daniel J. Diaz, James M. Loy, Andrew D. Ellington & Claus O. Wilke
[Journal of Biological Physics 47.4 (2021)](https://link.springer.com/article/10.1007/s10867-021-09593-6)

**Neural networks to learn protein sequence-function relationships from deep mutational scanning data**
Sam Gelman, Sarah A. Fahlberg, Pete Heinzelman, Philip A. Romero & Anthony Gitter
[Proceedings of the National Academy of Sciences](https://doi.org/10.1073/pnas.2104878118) • [code](https://github.com/gitter-lab/nn4dms) • Nov 2021

**Learning Protein Fitness Models from Evolutionary and Assay-labeled Data**
Chloe Hsu, Hunter Nisonoff, Clara Fannjiang, Jennifer Listgarten
[Nature Biotechnology (2022)](https://www.nature.com/articles/s41587-021-01146-5) • [Supplementary Information](https://static-content.springer.com/esm/art%3A10.1038%2Fs41587-021-01146-5/MediaObjects/41587_2021_1146_MOESM1_ESM.pdf) • [code](https://github.com/chloechsu/combining-evolutionary-and-assay-labelled-data)

**Proximal Exploration for Model-guided Protein Sequence Design**
Zhizhou Ren, Jiahan Li, Fan Ding, Yuan Zhou, Jianzhu Ma, Jian Peng
[BioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.12.487986v1) • [code](https://github.com/HeliXonProtein/proximal-exploration) • commercial

**Efficient evolution of human antibodies from general protein language models and sequence information alone**
Brian L. Hie, Duo Xu, Varun R. Shanker, Theodora U.J. Bruun, Payton A. Weidenbacher, Shaogeng Tang, Peter S. Kim
[bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.10.487811v1) • [code](https://github.com/brianhie/efficient-evolution)

**Tranception: protein fitness prediction with autoregressive transformers and inference-time retrieval**
Notin, P., Dias, M., Frazer, J., Marchena-Hurtado, J., Gomez, A., Marks, D.S., Gal, Y
[ICML (2022)](https://arxiv.org/abs/2205.13760)/[arXiv:2205.13760](https://arxiv.org/abs/2205.13760) • [code](https://github.com/OATML-Markslab/Tranception) • [hugging face](https://huggingface.co/ICML2022/Tranception)

**Protein engineering via Bayesian optimization-guided evolutionary algorithm and robotic experiments**
Ruyun Hu, Lihao Fu, Yongcan Chen, Junyu Chen, Yu Qiao, Tong Si
[bioRxiv 2022.08.11.503535](https://www.biorxiv.org/content/10.1101/2022.08.11.503535v1)

**Antibody optimization enabled by artificial intelligence predictions of binding affinity and naturalness**
Sharrol Bachas, Goran Rakocevic, David Spencer, Anand V. Sastry, Robel Haile, John M. Sutton, George Kasun, Andrew Stachyra, Jahir M. Gutierrez, Edriss Yassine, Borka Medjo, Vincent Blay, Christa Kohnert, Jennifer T. Stanton, Alexander Brown, Nebojsa Tijanic, Cailen McCloskey, Rebecca Viazzo, Rebecca Consbruck, Hayley Carter, Simon Levine, Shaheed Abdulhaqq, Jacob Shaul, Abigail B. Ventura, Randal S. Olson, Engin Yapici, Joshua Meier, Sean McClain, Matthew Weinstock, Gregory Hannum, Ariel Schwartz, Miles Gander, Roberto Spreafico
[bioRxiv 2022.08.16.504181](https://www.biorxiv.org/content/10.1101/2022.08.16.504181v1) • [poster](https://nips.cc/media/PosterPDFs/NeurIPS%202022/58999.png?t=1668022673.3853557)

**Construction of a Deep Neural Network Energy Function for Protein Physics**
Yang, Huan, Zhaoping Xiong, and Francesco Zonta
[Journal of Chemical Theory and Computation (2022)](https://pubs.acs.org/doi/10.1021/acs.jctc.2c00069)

**Inferring protein fitness landscapes from laboratory evolution experiments**
Sameer D’Costa, Emily C. Hinds, Chase R. Freschlin, Hyebin Song, Philip A. Romero
[bioRxiv 2022.09.01.506224](https://www.biorxiv.org/content/10.1101/2022.09.01.506224v1) • [Supplementary](https://www.biorxiv.org/content/10.1101/2022.09.01.506224v1.supplementary-material)

**BayeStab: Predicting Effects of Mutations on Protein Stability with Uncertainty Quantification**
Shuyu Wang, Hongzhou Tang, Yuliang Zhao, Lei Zuo
[Protein Science (2022)](https://onlinelibrary.wiley.com/doi/abs/10.1002/pro.4467) • [code](https://github.com/HongzhouTang/BayeStab) • [website](http://www.bayestab.com)

**Tuned Fitness Landscapes for Benchmarking Model-Guided Protein Design**
Neil Thomas, Atish Agarwala, David Belanger, Yun S. Song, Lucy Colwell
[bioRxiv 2022.10.28.514293](https://www.biorxiv.org/content/10.1101/2022.10.28.514293v1) • [code](https://github.com/google-research/slip)

**Protein design using structure-based residue preferences**
David Ding, Ada Y Shaw, Sam Sinai, Nathan J Rollins, Noam Prywes, David Savage, Michael T Laub, Debora S Marks
[bioRxiv 2022.10.31.514613](https://www.biorxiv.org/content/10.1101/2022.10.31.514613v2) • [code](https://github.com/ddingding/CoVES)

**Accurate Mutation Effect Prediction using RoseTTAFold**
Sanaa Mansoor, Minkyung Baek, David Juergens, Joseph L Watson, David Baker
[bioRxiv 2022.11.04.515218](https://www.biorxiv.org/content/10.1101/2022.11.04.515218v1)

**Learning the shape of protein micro-environments with a holographic convolutional neural network**
Michael N. Pun, Andrew Ivanov, Quinn Bellamy, Zachary Montague, Colin LaMont, Philip Bradley, Jakub Otwinowski, Armita Nourmohammad
[bioRxiv (2022)](https://arxiv.org/abs/2211.02936) • [code](https://github.com/StatPhysBio/protein_holography)

**Infer global, predict local: quantity-quality trade-off in protein fitness predictions from sequence data**
Lorenzo Posani, Francesca Rizzato, Rémi Monasson, Simona Cocco
[bioRxiv 2022.12.12.520004](https://www.biorxiv.org/content/10.1101/2022.12.12.520004v1)

**Validation of de novo designed water-soluble and transmembrane proteins by in silico folding and melting**
Alvaro Martin, Carolin Berner, Sergey Ovchinnikov, Anastassia Andreevna Vorobieva
[bioRxiv 2023.06.06.543955](https://www.biorxiv.org/content/10.1101/2023.06.06.543955v1) • [colab](https://colab.research.google.com/github/vorobieva/ColabFold/blob/main/beta/ESMFold_melting.ipynb)

**PoET: A generative model of protein families as sequences-of-sequences**
Timothy F. Truong Jr, Tristan Bepler
[arXiv:2306.06156](https://arxiv.org/abs/2306.06156) • [code](https://github.com/OpenProteinAI/PoET)

**Rapid protein stability prediction using deep learning representations**
Lasse M BlaabjergMaher M KassemLydia L GoodNicolas JonssonMatteo CagiadaKristoffer E JohanssonWouter BoomsmaAmelie SteinKresten Lindorff-Larsen
[eLife 12:e82593](https://elifesciences.org/articles/82593) • [code](https://github.com/KULL-Centre/_2022_ML-ddG-Blaabjerg/)

**A general Temperature-Guided Language model to engineer enhanced Stability and Activity in Proteins**
Pan Tan, Mingchen Li, Yuanxi Yu, Fan Jiang, Lirong Zheng, Banghao Wu, Xinyu Sun, Liqi Kang, Jie Song, Liang Zhang, Yi Xiong, Wanli Ouyang, Zhiqiang Hu, Guisheng Fan, Yufeng Pei, Liang Hong
[arXiv:2307.12682](https://arxiv.org/abs/2307.12682)

**Transfer learning to leverage larger datasets for improved prediction of protein stability changes**
Henry Dieckhaus, Michael Brocidiacono, Nicholas Randolph, Brian Kuhlman
[bioRxiv 2023.07.27.550881](https://www.biorxiv.org/content/10.1101/2023.07.27.550881v1) • [code](https://github.com/Kuhlman-Lab/ThermoMPNN) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/07/30/2023.07.27.550881/DC1/embed/media-1.docx)

**Structure-based self-supervised learning enables ultrafast prediction of stability changes upon mutation at the protein universe scale**
Jinyuan Sun, Tong Zhu, Yinglu Cui, Bian Wu
[bioRxiv 2023.08.09.552725](https://www.biorxiv.org/content/10.1101/2023.08.09.552725v1) • [code](https://github.com/Wublab/Pythia)

**Boosting AND/OR-Based Computational Protein Design: Dynamic Heuristics and Generalizable UFO**
Bobak Pezeshki, Radu Marinescu, Alexander Ihler, Rina Dechter
[arXiv:2309.00408](https://arxiv.org/abs/2309.00408)

**Zero-shot Mutation Effect Prediction on Protein Stability and Function using RoseTTAFold**
Sanaa Mansoor, Minkyung Baek, David Juergens, Joseph L. Watson, David Baker
[Protein Science](https://onlinelibrary.wiley.com/doi/10.1002/pro.4780) • [dissertation](https://www.proquest.com/openview/dba5569e5efd0dc60fc7bedccb6afee3/)

**Accurate proteome-wide missense variant effect prediction with AlphaMissense**
Jun Cheng, Guido Novati, Joshua Pan, Clare Bycroft, Akvile Žemgulyte, Taylor Applebaum, Alexander Pritzel, Lai Hong Wong, Michal Zielinski, Tobias Sargeant, Rosalia G. Schneider, Andrew W. Senior, John Jumper, Demis Hassabis, Pushmeet Kohli, Žiga Avsec
[Science0,eadg7492DOI:10.1126/science.adg7492](https://www.science.org/doi/10.1126/science.adg7492) • [code](https://github.com/deepmind/alphamissense) • [data](https://console.cloud.google.com/storage/browser/dm_alphamissense)

**Enzyme structure correlates with variant effect predictability**
Floris Julian van der Flier, Dave Estell, Sina Pricelius, Lydia Dankmeyer, Sander van Stigt Thans, Harm Mulder, Rei Otsuka, Frits Goedegebuur, Laurens Lammerts, Diego Staphorst, Aalt D.J. van Dijk, Dick de Ridder, Henning Redestig
[bioRxiv 2023.09.25.559319](https://www.biorxiv.org/content/10.1101/2023.09.25.559319v2)/[Computational and Structural Biotechnology Journal (2024)](https://doi.org/10.1016/j.csbj.2024.09.007) • [code](https://github.com/florisvdf/mutation-predictability)

**Fast, accurate ranking of engineered proteins by target binding propensity using structure modeling**
Xiaozhe Ding, Xinhong Chen, Erin E. Sullivan, Timothy F. Shay, Viviana Gradinaru
[bioRxiv 2023.01.11.523680](https://www.biorxiv.org/content/10.1101/2023.01.11.523680v2)/[Molecular Therapy (2024)](https://www.cell.com/molecular-therapy-family/molecular-therapy/fulltext/S1525-0016(24)00219-3) • [code](https://github.com/GradinaruLab/APPRAISE) • [colab](https://colab.research.google.com/github/GradinaruLab/APPRAISE/blob/main/Colab_APPRAISE.ipynb)

**Neural network extrapolation to distant regions of the protein fitness landscape**
Sarah A Fahlberg, Chase R Freschlin, Pete Heinzelman, Philip A Romero
[bioRxiv 2023.11.08.566287](https://www.biorxiv.org/content/10.1101/2023.11.08.566287v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/11/09/2023.11.08.566287/DC1/embed/media-1.pdf)

**Accelerating protein engineering with fitness landscape modeling and reinforcement learning**
Haoran Sun, Liang He, Pan Deng, Guoqing Liu, Haiguang Liu, Chuan Cao, Fusong Ju, Lijun Wu, Tao Qin, Tie-Yan Liu
[bioRxiv 2023.11.16.565910](https://www.biorxiv.org/content/10.1101/2023.11.16.565910v1)

**Protein Design by Directed Evolution Guided by Large Language Models**
Trong Thanh Tran, Truong Son Hy
[bioRxiv 2023.11.29.568945](https://www.biorxiv.org/content/10.1101/2023.11.28.568945v1) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2023/11/29/2023.11.28.568945/DC1/embed/media-1.pdf) • [code](https://github.com/HySonLab/Directed_Evolution)

**High-throughput ML-guided design of diverse single-domain antibodies against SARS-CoV-2**
Christof Angermueller, Zelda Marie, Benjamin Jester, Emily Engelhart, Ryan Emerson, Babak Alipanahi, Zachary Ryan McCaw, Jim Roberts, Randolph M Lopez, David Younger, Lucy Colwell
[bioRxiv 2023.12.01.569227](https://www.biorxiv.org/content/10.1101/2023.12.01.569227v1)

**Efficiently Predicting Protein Stability Changes Upon Single-point Mutation with Large Language Models**
Yijie Zhang, Zhangyang Gao, Cheng Tan, Stan Z.Li
[arXiv preprint arXiv:2312.04019 (2023)](https://arxiv.org/abs/2312.04019)

**DSMBind: SE(3) denoising score matching for unsupervised binding energy prediction and nanobody design**
Wengong Jin, Xun Chen, Amrita Vetticaden, Siranush Sarzikova, Raktima Raychowdhury, Caroline Uhler, Nir Hacohen
[bioRxiv 2023.12.10.570461](https://www.biorxiv.org/content/10.1101/2023.12.10.570461v1) • [Supplementary1](https://www.biorxiv.org/content/biorxiv/early/2023/12/10/2023.12.10.570461/DC1/embed/media-1.xlsx) • [Supplementary2](https://www.biorxiv.org/content/biorxiv/early/2023/12/10/2023.12.10.570461/DC2/embed/media-2.pdf)

**Inverse folding of protein complexes with a structure-informed language model enables unsupervised antibody evolution**
Varun R. Shanker, Theodora U.J. Bruun, Brian L. Hie, Peter S. Kim
[bioRxiv 2023.12.19.572475](https://www.biorxiv.org/content/10.1101/2023.12.19.572475v2)

**EvolMPNN: Predicting Mutational Effect on Homologous Proteins by Evolution Encoding**
Zhiqiang Zhong, Davide Mottin
[arXiv:2402.13418](https://arxiv.org/abs/2402.13418)

**Generating mutants of monotone affinity towards stronger protein complexes through adversarial learning**
Tian Lan, Shuquan Su, Pengyao Ping, Gyorgy Hutvagner, Tao Liu, Yi Pan & Jinyan Li
[Nat Mach Intell 6, 315–325 (2024)](https://www.nature.com/articles/s42256-024-00803-z) • [code](https://github.com/tianlt/Deepdirect)

**Biophysics-based protein language models for protein engineering**
Sam Gelman, Bryce Johnson, Chase Freschlin, Sameer D'Costa, Anthony Gitter & Philip A. Romero
[bioRxiv 2024.03.15.585128](https://doi.org/10.1101/2024.03.15.585128) • [code](https://github.com/gitter-lab/metl)

**Latent-based Directed Evolution accelerated by Gradient Ascent for Protein Sequence Design** / **LatentDE: latent-based directed evolution for protein sequence design**
Nhat Khang Ngo, Thanh V. T. Tran, Viet Thanh Duy Nguyen, Truong Son Hy
[bioRxiv 2024.04.13.589381](https://www.biorxiv.org/content/10.1101/2024.04.13.589381v1)/[NeurIPS 2024](https://openreview.net/pdf?id=4YkbQGVWGF)/[Machine Learning: Science and Technology (2025)](https://iopscience.iop.org/article/10.1088/2632-2153/adc2e2) • [code](https://github.com/HySonLab/LatentDE)

**AAVDiff: Experimental Validation of Enhanced Viability and Diversity in Recombinant Adeno-Associated Virus (AAV) Capsids through Diffusion Generation**
Lijun Liu, Jiali Yang, Jianfei Song, Xinglin Yang, Lele Niu, Zeqi Cai, Hui Shi, Tingjun Hou, Chang-yu Hsieh, Weiran Shen, Yafeng Deng
[arXiv:2404.10573](https://arxiv.org/abs/2404.10573)

**Protein engineering with lightweight graph denoising neural networks**
Bingxin Zhou, Lirong Zheng, Banghao Wu, Yang Tan, Outongyi Lv, Kai Yi, Guisheng Fan, and Liang Hong
[Journal of Chemical Information and Modeling (2024)](https://pubs.acs.org/doi/10.1021/acs.jcim.4c00036) • [code](https://github.com/bzho3923/ProtLGN)

**VespaG: Expert-guided protein Language Models enable accurate and blazingly fast fitness prediction**
Celine Marquet, Julius Schlensok, Marina Abakarova, Burkhard Rost, Elodie Laine
[bioRxiv 2024.04.24.590982](https://www.biorxiv.org/content/10.1101/2024.04.24.590982v1) • [code](https://github.com/JSchlensok/VespaG)

**Interface design of SARS-CoV-2 symmetrical nsp7 dimer and machine learning-guided nsp7 sequence prediction reveals physicochemical properties and hotspots for nsp7 stability, adaptation, and therapeutic design**
Amar Jeet Yadav, Shivank Kumar, Shweata Maurya, Khushboo Bhagat, and Aditya K. Padhi
[Physical Chemistry Chemical Physics (2024)](https://pubs.rsc.org/en/content/articlelanding/2024/cp/d4cp01014k)

**Aligning protein generative models with experimental fitness via Direct Preference Optimization**
Talal Widatalla, Rafael Rafailov, Brian Hie
[bioRxiv 2024.05.20.595026](https://www.biorxiv.org/content/10.1101/2024.05.20.595026v1) • [code](https://github.com/evo-design/protein-dpo)

**ProBASS – a language model with sequence and structural features for predicting the effect of mutations on binding affinity**
Sagara N.S. Gurusinghe, Yibing Wu, William DeGrado, Julia M. Shifman
[bioRxiv 2024.06.21.600041](https://www.biorxiv.org/content/10.1101/2024.06.21.600041v1) • [code](https://github.com/sagagugit/ProBASS)

**Unsupervised evolution of protein and antibody complexes with a structure-informed language model**
Varun R. Shanker, Theodora U. J. Bruun, Brian L. Hie, Peter S. Kim
[Science385,46-53(2024)](https://www.science.org/doi/10.1126/science.adk8946) • [code](https://github.com/varun-shanker/structural-evolution)

**Enhancing efficiency of protein language models with minimal wet-lab data through few-shot learning**
Ziyi Zhou, Liang Zhang, Yuanxi Yu, Banghao Wu, Mingchen Li, Liang Hong & Pan Tan
[Nat Commun 15, 5566 (2024)](https://www.nature.com/articles/s41467-024-49798-6) • [code](https://github.com/OATML-Markslab/Tranception)

**Rapid protein evolution by few-shot learning with a protein language model**
Kaiyi Jiang, Zhaoqing Yan, Matteo Di Bernardo, Samantha R. Sgrizzi, Lukas Villiger, Alisan Kayabolen, Byungji Kim, Josephine K. Carscadden, Masahiro Hiraizumi, Hiroshi Nishimasu, Jonathan S. Gootenberg, Omar O. Abudayyeh
[bioRxiv 2024.07.17.604015](https://www.biorxiv.org/content/10.1101/2024.07.17.604015v1) • [code1](https://github.com/mat10d/EvolvePro),[code2](https://github.com/idmjky/EvolvePro)

**Zero-shot prediction of mutation effects with multimodal deep representation learning guides protein engineering**
Peng Cheng, Cong Mao, Jin Tang, Sen Yang, Yu Cheng, Wuke Wang, Qiuxi Gu, Wei Han, Hao Chen, Sihan Li, Yaofeng Chen, Jianglin Zhou, Wuju Li, Aimin Pan, Suwen Zhao, Xingxu Huang, Shiqiang Zhu, Jun Zhang, Wenjie Shu & Shengqi Wang
[Cell Research (2024)](https://www.nature.com/articles/s41422-024-00989-2) • [code](https://github.com/wenjiegroup/ProMEP)

**Machine learning-guided co-optimization of fitness and diversity facilitates combinatorial library design in enzyme engineering**
Kerr Ding, Michael Chin, Yunlong Zhao, Wei Huang, Binh Khanh Mai, Huanan Wang, Peng Liu, Yang Yang & Yunan Luo
[Nature Communications 15.1 (2024)](https://www.nature.com/articles/s41467-024-50698-y) • [code](https://github.com/luo-group/MODIFY), [model](https://doi.org/10.5281/zenodo.12715542)

**Dirichlet latent modelling enables effective learning and sampling of the functional protein design space**
Evgenii Lobzaev, Giovanni Stracquadanio
[Nat Commun 15, 9309 (2024)](https://www.nature.com/articles/s41467-024-53622-6) • [code](https://licensing.edinburgh-innovations.ed.ac.uk/product/proton)

**MProt-DPO: Breaking the ExaFLOPS Barrier for Multimodal Protein Design Workflows with Direct Preference Optimization**
Gautham Dharuman, Kyle Hippe, Alexander Brace, Sam Foreman, Väinö Hatanpää, Varuni K. Sastry, Huihuo Zheng, Logan Ward, Servesh Muralidharan, Archit Vasan, Bharat Kale, Carla M. Mann, Heng Ma, Yun-Hsuan Cheng, Yuliana Zamora, Shengchao Liu, Chaowei Xiao, Murali Emani, Tom Gibbs, Mahidhar Tatineni, Deepak Canchi, Jerome Mitchell, Koichi Yamada, Maria Garzaran, Michael E. Papka, Ian Foster, Rick Stevens, Anima Anandkumar, Venkatram Vishwanath, Arvind Ramanathan
[International Conference for High Performance Computing, Networking, Storage and Analysis SC. IEEE Computer Society, 2024](https://www.computer.org/csdl/proceedings-article/sc/2024/529100a074/21HUV88n1F6)

**Scoring-Assisted Generative Exploration for Proteins (SAGE-Prot): A Framework for Multi-Objective Protein Optimization via Iterative Sequence Generation and Evaluation**  
Hocheol Lim, Geon-Ho Lee, Kyoung Tai No  
[arXiv:2505.01277](https://arxiv.org/abs/2505.01277) • [code](https://github.com/hclim0213/SAGE-Prot)

**Artificial Intelligence And First Principle Methods In Protein Redesign: A Marriage Of Convenience?**  
Damiano Cianferoni, David Vizarraga, Ana María Fernández-Escamilla, Ignacio Fita, Rahma Hamdani, Raul Reche, Javier Delgado, Luis Serrano  
[bioRxiv 2025.05.12.653318](https://www.biorxiv.org/content/10.1101/2025.05.12.653318v1)/[Protein Science](https://onlinelibrary.wiley.com/doi/10.1002/pro.70210) • [Supplementary](https://www.biorxiv.org/content/biorxiv/early/2025/05/15/2025.05.12.653318/DC1/embed/media-1.pdf)

**Likelihood-based Fine-tuning of Protein Language Models for Few-shot Fitness Prediction and Design**  
Alex Hawkins-Hooker, Shikha Surana, Jack Simons, Jakub Kmec, Oliver Bent, Paul Duckworth  
[bioRxiv 2024.05.28.596156](https://www.biorxiv.org/content/10.1101/2024.05.28.596156v3)

**ProSpero: Active Learning for Robust Protein Design Beyond Wild-Type Neighborhoods**  
Michal Kmicikiewicz, Vincent Fortuin, Ewa Szczurek  
[arXiv:2505.22494](https://arxiv.org/abs/2505.22494v1)

**Heuristic Multi-site Optimization for Protein Sequence Design using Masked Protein Language Models**  
Lijuan Wang, Yuze Wang, Chen Qiu, Liwei Xiao, Xianliang Liu, Junjie Chen  
[bioRxiv 2025.07.31.668012](https://www.biorxiv.org/content/10.1101/2025.07.31.668012v1)

### 7.2 Protein Language Models (pLM) and representation learning

> More detailed protein representation learning list:
> [Lirong Wu](https://github.com/LirongWu)'s [awesome-protein-representation-learning](https://github.com/LirongWu/awesome-protein-representation-learning)

**Unified rational protein engineering with sequence-based deep representation learning**
Ethan C. Alley, Grigory Khimulya, Surojit Biswas, Mohammed AlQuraishi & George M. Church
[Nature methods 16.12 (2019)](https://www.nature.com/articles/s41592-019-0598-1)

**Protein Structure Representation Learning by Geometric Pretraining**
Zuobai Zhang, Minghao Xu, Arian Jamasb, Vijil Chenthamarakshan, Aurelie Lozano, Payel Das, Jian Tang
[arXiv](https://arxiv.org/abs/2203.06125) • Jan 2022

**Evolutionary velocity with protein language models**
Brian L. Hie, Kevin K. Yang, and Peter S. Kim
[bioRxiv](https://www.biorxiv.org/content/10.1101/2021.06.07.447389v1.full.pdf)

**Advancing protein language models with linguistics: a roadmap for improved interpretability**
Mai Ha Vu, Rahmad Akbar, Philippe A. Robert, Bartlomiej Swiatczak, Victor Greiff, Geir Kjetil Sandve, Dag Trygve Truslew Haug
[arXiv:2207.00982](https://arxiv.org/abs/2207.00982)

**Deciphering the language of antibodies using self-supervised learning**
Jinwoo Leem, Laura S. Mitchell, James H.R. Farmery, Justin Barton, Jacob D. Galson
[Patterns (2022): 100513](https://www.sciencedirect.com/science/article/pii/S2666389922001052) • [code](https://github.com/alchemab/antiberta)

**On Pre-training Language Model for Antibody**
Anonymous(Paper under double-blind review)
[ICLR 2023](https://openreview.net/forum?id=zaq4LV55xHl) • [Supplementary](https://openreview.net/attachment?id=zaq4LV55xHl&name=supplementary_material)

**Antibody Representation Learning for Drug Discovery**
Lin Li, Esther Gupta, John Spaeth, Leslie Shing, Tristan Bepler, Rajmonda Sulo Caceres
[arXiv:2210.02881](https://arxiv.org/abs/2210.02881)

**Learning Complete Protein Representation by Deep Coupling of Sequence and Structure**
Bozhen Hu, Cheng Tan, Jun Xia, Jiangbin Zheng, Yufei Huang, Lirong Wu, Yue Liu, Yongjie Xu, Stan Z. Li
[bioRxiv 2023.07.05.547769](https://www.biorxiv.org/content/10.1101/2023.07.05.547769v1)

**Leveraging Ancestral Sequence Reconstruction for Protein Representation Learning**
D. S. Matthews, M. A. Spence, A. C. Mater, J. Nichols, S. B. Pulsford, M. Sandhu, J. A. Kaczmarski, C. M. Miton, N. Tokuriki, C. J. Jackson
[bioRxiv 2023.12.20.572683](https://www.biorxiv.org/content/10.1101/2023.12.20.572683v1) • [code](https://github.com/RSCJacksonLab/local-ancestral-sequence-embeddings)

**Protein language models are biased by unequal sequence sampling across the tree of life**
Frances Ding, Jacob Steinhardt
[bioRxiv 2024.03.07.584001](https://www.biorxiv.org/content/10.1101/2024.03.07.584001v1)

**InstructPLM: Aligning Protein Language Models to Follow Protein Structure Instructions**
Jiezhong Qiu, Junde Xu, Jie Hu, Hanqun Cao, Liya Hou, Zijun Gao, Xinyi Zhou, Anni Li, Xiujuan Li, Bin Cui, Fei Yang, Shuang Peng, Ning Sun, Fangyu Wang, Aimin Pan, Jie Tang, Jieping Ye, Junyang Lin, Jin Tang, Xingxu Huang, Pheng Ann Heng, Guangyong Chen
[bioRxiv 2024.04.17.589642](https://www.biorxiv.org/content/10.1101/2024.04.17.589642v1)

### 7.3 Molecular Design Models

> Unlike **function-scaffold-sequence** paradigm in protein design, major molecular design models based on paradigm form DL from 3 kinds of level: **atom-based**, **fragment-based**, **reaction-based**, and they can be categorized as [Gradient optimization](#731-gradient-optimization) or [Optimized sampling](#732-optimized-sampling)(gradient-free). [Click here for detail review](https://www.sciencedirect.com/science/article/pii/S1359644621002531)In consideration of learning more various of generative models for design, these recommended latest models from **Molecular Design** might be helpful and even be able to be transplanted to protein design.
> More paper list at :
>
> 1. [CondaPereira](https://github.com/CondaPereira)'s GitHub repo: [Essay_For_Molecular_Generation](https://github.com/CondaPereira/Essay_For_Molecular_Generation).
> 2. [AspirinCode](https://github.com/AspirinCode)'s :[papers-for-molecular-design-using-DL](https://github.com/AspirinCode/papers-for-molecular-design-using-DL),[awesome-AI4MolConformation-MD](https://github.com/AspirinCode/awesome-AI4MolConformation-MD)
> 3. [Alex Morehead](https://github.com/amorehead)'s :[awesome-molecular-generation](https://github.com/amorehead/awesome-molecular-generation)

#### 7.3.1 Gradient optimization

**Differentiable scaffolding tree for molecular optimization**
Fu, T., Gao, W., Xiao, C., Yasonik, J., Coley, C. W., & Sun, J
[arXiv preprint arXiv:2109.10469](https://arxiv.org/abs/2109.10469) • [code](https://github.com/futianfan/DST) • Sept 21

**Equivariant Energy-Guided SDE for Inverse Molecular Design**
Fan Bao, Min Zhao, Zhongkai Hao, Peiyao Li, Chongxuan Li, Jun Zhu
[arXiv:2209.15408](https://arxiv.org/abs/2209.15408)

**Equivariant Shape-Conditioned Generation of 3D Molecules for Ligand-Based Drug Design**
Keir Adams, Connor W. Coley
[arXiv:2210.04893](https://arxiv.org/abs/2210.04893) • [code](https://github.com/keiradams/SQUID)

**Structure-based Drug Design with Equivariant Diffusion Models**
Arne Schneuing, Yuanqi Du, Charles Harris, Arian Jamasb, Ilia Igashov, Weitao Du, Tom Blundell, Pietro Lió, Carla Gomes, Max Welling, Michael Bronstein, Bruno Correia
[NeurIPS 2022](https://www.mlsb.io/papers_2022/Structure_based_Drug_Design_with_Equivariant_Diffusion_Models.pdf)/[arXiv:2210.13695](https://arxiv.org/abs/2210.13695) • [code](https://github.com/arneschneuing/DiffSBDD)

#### 7.3.2 Optimized sampling

**Generating 3D Molecules for Target Protein Binding**
Meng Liu, Youzhi Luo, Kanji Uchino, Koji Maruhashi, Shuiwang Ji
[International Conference on Machine Learning 39 (2022)](https://proceedings.mlr.press/v162/liu22m.html) • [GraphBP](https://github.com/divelab/graphbp)

**Pocket2Mol: Efficient Molecular Sampling Based on 3D Protein Pockets**
Peng, Xingang, et al
[International Conference on Machine Learning 39 (2022)](https://proceedings.mlr.press/v162/peng22b.html) • [code](https://github.com/pengxingang/Pocket2Mol)

**Reinforced Genetic Algorithm for Structure-based Drug Design**
Fu, Tianfan, et al
[arXiv preprint arXiv:2211.16508 (2022)](https://arxiv.org/abs/2211.16508)/[ICML22](https://openreview.net/forum?id=_Sfd-icezCa) • [code](https://github.com/futianfan/reinforced-genetic-algorithm) • [website](https://deepai.org/publication/reinforced-genetic-algorithm-for-structure-based-drug-design)

**Molecule Generation For Target Protein Binding with Structural Motifs**
Zhang, Zaixi, et al
[International Conference on Learning Representations 11 (2023)](https://openreview.net/forum?id=Rq13idF0F73) • [code](https://github.com/zaixizhang/FLAG)

**3D Equivariant Diffusion for Target-Aware Molecule Generation and Affinity Prediction**
Guan, Jiaqi, et al
[International Conference on Learning Representations 11 (2023)](https://openreview.net/forum?id=kJqXEPXMsE0) • [code](https://github.com/guanjq/targetdiff)

### 7.4 Unclassified

**De novo design of epitope-specific antibodies against soluble and multipass membrane proteins with high specificity, developability,and function**
[Nabla Bio](https://www.nabla.bio/)
[preprint](https://nabla-public.s3.us-east-1.amazonaws.com/2024_Nabla_JAM_de_novo_antibodies.pdf) • [blog](https://www.nabla.bio/news/denovo) • [news](https://www.science.org/content/article/ai-conjures-potential-new-antibody-drugs-matter-months) • commercial

**Chai-2: Zero-Shot Antibody Discovery in a 24-well Plate**  
Chai Discovery Team  
[technical report](https://chaiassets.com/chai-2/paper/technical_report.pdf) • [news](https://www.chaidiscovery.com/news/introducing-chai-2) • commercial

**Latent-X: An Atom-level Frontier Model for De Novo Protein Binder Design**  
Latent Labs Team  
[technical report](https://www.latentlabs.com/wp-content/uploads/2025/07/Latent-X-Technical-Report.pdf) • [website](https://www.latentlabs.com/latent-x/) • commercial
