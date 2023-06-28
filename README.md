# COPD-Microbiome-Shift-Analysis
<img width="812" alt="Schermafbeelding 2023-06-26 094816" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/f9d588e3-00bc-44ef-9e92-4a86a8ca9d5a">



This is the repository for a bioinformatics project about identifying the optimal pipeline for identifying a potential microbiome shift in COPD patients after ceasing azithromycin treatment.

## Summary
**Introduction** 

Chronic obstructive pulmonary disease (COPD) is a prevalent respiratory condition characterized by airflow obstruction and inflammation, often leading to acute exacerbations. While azithromycin shows promise in reducing exacerbations, concerns regarding antibiotic resistance and side effects arise with prolonged use. Understanding the impact of discontinuing azithromycin treatment on exacerbations and patient well-being requires assessing changes in the COPD-associated microbiome. We aimed to identify an optimal pipeline for analyzing 16S rRNA gene sequencing data by comparing five pipelines: [NanoCLUST](https://github.com/genomicsITER/NanoCLUST), [NanoRTax](https://github.com/genomicsITER/NanoRTax), [BugSeq](https://bugseq.com/), [Emu](https://gitlab.com/treangenlab/emu), and [Kraken2](https://github.com/DerrickWood/kraken2/tree/master)/[Bracken](https://github.com/jenniferlu717/Bracken). 

**Methods**

We evaluated the accuracy of the five taxonomic classifiers using a Zymo mock sample with known bacterial DNA composition and a sputum sample spiked with *Allobacillus* and *Imtechella*. NanoCLUST demonstrated robust performance for taxonomic classification on a genus level. Subsequently, we utilized NanoCLUST to analyze sputum samples from a single patient collected at months 0, 3, 6, and 9. Rstudio facilitated data visualization through heatmaps and barplots, enabling comparison of microbiome compositions across patient groups. 

**Results**

Among the pipelines evaluated, NanoCLUST stood out as the only one that consistently detected the same number of genera in both the sputum subsets and the Zymo mock subsets. The sputum sample was spiked with microbial cells from the *Imtechella* and *Allobacillus* genera. NanoCLUST detected all genera except *Lactobacillus*, but the pipeline identified *Limosilactobacillus* in the subsets which is a genus splitted from *Lactobacillus*. NanoCLUST accurately identified *Imtechella* with relative abundances of 2.4% and 2.1% in the 10% and 90% subsets, respectively. It also detected *Allobacillus* with relative abundances of 33.2% and 37.2% in the corresponding subsets.

Over a 9-month monitoring period, sputum samples were collected from a patient every 3 months and analyzed using NanoCLUST for relative abundance analysis of genera in 16s rRNA gene reads. The results showed changes in the relative abundance of different genera, including a decline in Haemophilus and fluctuations in Streptococcus. The percentages of Veillonella and Gemella reads varied, while Granulicatella showed a consistent increase. Unique genera were found in each sample, and NanoCLUST's taxonomic classification aligned with the culturing results. The findings were visualized with a heatmap.

**Conclusion**

This study provides insights into COPD-associated microbiome changes and highlights NanoCLUST as a reliable pipeline for taxonomic analysis of 16S rRNA gene sequencing data. The visualization approach enhances interpretation and comparison of microbiome data in COPD research, advancing our understanding of the effects of discontinuing azithromycin treatment in COPD patients. 

## Figures

**Barplot of amount of unique genera detected by each pipeline in each of the four subsets**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/5ea405b2-db16-4146-a88b-efae8b4bad2c)

**Stacked barplot of genera with more than 0,1% relative abundance distribution in Zymo mock sample subsets across pipelines, with a bar representing the theoretical composition of the Zymo mock sample. Relative abundances of <0.1% allocated to ‘other’.**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/8f255c07-70d4-40bd-ab45-89c1d29ea3ba)


**Stacked barplot of genera with more than 0,1% relative abundance distribution in sputum sample subsets across pipelines. Relative abundances of <0.1% allocated to ‘other’.**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/523da54f-1312-4d9e-a72a-5fda038de022)


**Temporal abundance heatmap of detected genera in sputum samples from 1 patient collected at 4 different moments**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/5677dcba-f037-46f5-8c69-1e545adf4e28)


**Flowchart**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/afc6b1d9-a542-4ff1-830a-69c0b7274f60)


## Tables
**Theoretical Composition ZymoBIOMICS™ Microbial Community DNA Standard based on Genomic DNA**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/046fd52c-603f-439c-a3ff-f64bf2c0530d)


**Sputum samples collected for Microbiome analysis**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/2bdc6f8b-719b-4888-99a5-d40af599de06)

**Cultured bacteria in sputum samples**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/7e286872-50d7-48ca-8a2b-a938dfac0d52)


**Basic quality measurements sequenced Sputum and Zymo mock samples with selection of top 10% and 90%  reads based on quality**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/10b630ca-087e-421b-b983-dfa5efb710a5)


**Basic quality measurements sequenced Sputum samples from 1 patient**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/a8a6287a-1734-4247-a6c8-86773be41d8a)


**Computational performances of the three command-line pipelines, * indicates a difficult installation process, ** indicates an average installation process and *** indicates an easy installation process**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/5ff5b5f6-f02b-44ce-9e67-aad01e962a31)


## Data availability
The article can be viewed [here.](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/blob/main/Scientific%20paper%20COPD%20JGBR%20versie%202.pdf)
