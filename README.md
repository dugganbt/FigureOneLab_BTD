# FigureOneLab_BTD
A bioinformatic analysis case study, following the Figure One Lab guide by Dean Lee. **__Disclaimer__**: This repository is an exercise in performing a bioinformatic analysis and is not intended as a reference. Please refer to the listed publications for peer reviewed literature. 

## Background
This project follows a guided bioinformatic analysis based on public data and the Figure One Lab guide by Dean Lee. The project addresses the use of antibody two antibody therapies:
1. Trastuzumab for treatment of HER2-positive breast and gastric cancers, targets HER2
2. Bevacizumab for treatment of colorectal, lung, glioblastoma, breast, liver and kidney cancer, targets VEGF.

## Breaking down the Key Scientific Question (KSQ)
KSQ from the case-study: 
>"Using available scRNA-seq data from cancer cell lines, how would you explore the use of the following FDA-approved antibody therapies in additional cancers?" 

To paraphrase: _we want to evaluate the potential use of Trastuzumab and Bevacizumab for additional cancer treatments beyond their approved regimens using publicly available scRNA-seq data from cell lines._

### _Subcomponent 1._ Methodology used: How is scRNA-seq data used to assess cancer therapy? Advantages and limitations?
Single-cell RNA sequencing (scRNA-seq) probes gene expression on the level of individual cells, allowing us to obtain a snapshot of the dynamic operations of a cell within the context of it's tissue on the mRNA level. This data, amongst other modalities such as chromatin accessibility, proteins and location, can be leveraged to study cellular responses to therapeutics at high-resolution [1]. 

Within the context of disease research, scRNA-seq allows us to identify patterns associated with certain disease phenotypes. For cancer specifically, scRNA-seq can help better understand key processes in tumor initiation, drug response, resistance, and metastases [2]. For example, scRNA-seq has been applied to identify cellular programs common to "cold" tumors that limit the infiltration of T lymphocytes into the tumor environment, evading the immune response and rendering immune therapy such as immune checkpoint inhibition less effective. This cellular program could be used to predict clinical responses to immunotherapy in melanoma patients, explore potential treatment options, and was expanded to other cancer types [3, 4].

However, interrogation of cellular programs at the mRNA level represents just one layer of a more complex system which can be expanded by studying further modalities such as chromatin accessibility, protein expression and spatial context. It is important to also consider the correct approacht to address the research question, as each scRNA-seq method comes with it's advantages and drawbacks [1,5]. 



### _Subcomponent 2._ Model used: What aspects of the diseases do the cell lines recapitulate, and what limitations do they bring? What further studies would need to support this data?
Immortalized cancer cell lines find prominent use within pharmaceutical research due to their ease-of-use, high level of characterization and availability of a multitude of clones, at relatively low-cost. Nevertheless, the use of cell lines should consider their potential drawbacks and applicability within the desired context. Given that cell lines are frequently cultured in simplified settings such as in 2D flasks using standardized media lacking tumor-specific microenvironment components, it is important to verify that findings used in cell line research is translatable to the clinic. Studies addressing this question have been reviewed [6], and systematic benchmarking has been performed to guide the choice of relevant cell lines for a desired context-of-use [7]. 

### _Subcomponent 3._ Drugs and targets: What are the mechanisms of action for the conventional use-cases of the drugs, and how could this be expanded to additional cancers?

#### Bevacizumab (Avastin)
Bevacizumab is a monoclonal antibody conventionally used to treat angiogenic solid cancers such as metastatic colorecal cancer, metastatic breast cancer, ovarian cancer, non-small-cell lung cancer, and glioblastoma multiforme [8]. Specifically, it binds soluble Vasculare Endothelial Growth Factor A (VEGF-A), which is primarly expressed during embryogenesis, during wound healing or during the female reproductive cycle to promote growth of new blood vessels from existing vasculature. Some angiogenic cancers express high levels of VEGF-A to increase their oxygen and nutrient supply to support their increasing metabolic demands as they expand [8]. 

More recently, VEGF-A has been associated with non-angiogenic mechanisms of cancer progression such as increasing cancer cell proliferation, stem cell ness, and suppressing immune cells. As a consequence, Bevacizumab has also found application in enhancement of cancer immunotherapy efficacy [8]. 


#### Trastuzumab (Herceptin)
Trastuzumab is also a monoclonal antibody and is specificallly used for the treatment of HER-2 positive breast and gastric cancers [9, 10]. It acts by binding HER-2, a tyrosine kinase receptor overexpressed on HER-2 positive breast cancer cells thereby inhibiting HER-2 signalling pathway that promotes disease progression, as well as by recruiting immune cells by antibody-dependent cell-mediated cytotoxicity [9]. 

Trastuzumab, or viariations and combinations of it's targeting mechanism, have been expanded onto other solid cancer types with varying success. Additionally, resistance mechanisms such as HER-2 alterations that limit drug binding or constitutive expression of downstream pathways have posed a challenge for treatments [10]. 

_To be continued_


### References
[1] Heumos, L., Schaar, A.C., Lance, C. et al. Best practices for single-cell analysis across modalities. Nat Rev Genet (2023). https://doi.org/10.1038/s41576-023-00586-w

[2] Orit Rozenblatt-Rosen, Aviv Regev et al. The Human Tumor Atlas Network: Charting Tumor Transitions across Space and Time at Single-Cell Resolution. Cell, 181, 2, 4 (2020). https://doi.org/10.1016/j.cell.2020.03.053

[3] Livnat Jerby-Arnon, Parin Shah et al. A Cancer Cell Program Promotes T Cell Exclusion and Resistance to Checkpoint Blockade. Cell, 175, 4, 11 (2018). https://doi.org/10.1016/j.cell.2018.09.006

[4] Jerby-Arnon, L., Regev, A. DIALOGUE maps multicellular programs in tissue from single-cell or spatial transcriptomics data. Nat Biotechnol 40, 1467–1477 (2022). https://doi.org/10.1038/s41587-022-01288-0

[5] Matilde I. Conte, Azahara Fuentes-Trillo et al. Opportunities and tradeoffs in single-cell transcriptomic technologies. Trends in Genetics, 40, 1, 1 (2024). https://doi.org/10.1016/j.tig.2023.10.003.

[6] Lucia Trastulla, Javad Noorbakhsh et al. Computational estimation of quality and clinical relevance of cancer cell lines. Molecular Systems Biology, 18, 7, 7 2022

[7] Jin, H., Zhang, C., Zwahlen, M. et al. Systematic transcriptional analysis of human cell lines for gene expression landscape and tumor representation. Nat Commun 14, 5417 (2023). https://doi.org/10.1038/s41467-023-41132-w.

[8] Josep Garcia, Herbert I. Hurwitz et al. Cancer Treatment Reviews, 86, 6 (2020). Anti-tumour Treatment Bevacizumab (Avastin®) in cancer treatment: A review of 15 years of clinical experience and future outlook. https://doi.org/10.1016/j.ctrv.2020.102017.

[9] Swain, S.M., Shastry, M. & Hamilton, E. Targeting HER2-positive breast cancer: advances and future directions. Nat Rev Drug Discov 22, 101–126 (2023). https://doi.org/10.1038/s41573-022-00579-0

[10] Yoon, J., Oh, DY. HER2-targeted therapies beyond breast cancer — an update. Nat Rev Clin Oncol 21, 675–700 (2024). https://doi.org/10.1038/s41571-024-00924-9
