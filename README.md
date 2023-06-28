# COPD-Microbiome-Shift-Analysis
<img width="812" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/ef7643ec-7762-463c-a389-09d1efb31ee2">


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

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/11e90999-8401-44ee-809c-48ed4a6fa261)

**Stacked barplot of genera with more than 0,1% relative abundance distribution in Zymo mock sample subsets across pipelines, with a bar representing the theoretical composition of the Zymo mock sample. Relative abundances of <0.1% allocated to ‘other’.**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/29be0267-6eca-447d-923a-11187e8da383)

**Stacked barplot of genera with more than 0,1% relative abundance distribution in sputum sample subsets across pipelines. Relative abundances of <0.1% allocated to ‘other’.**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/12709a24-b782-4b9c-80d5-34b42b680975)

**Temporal abundance heatmap of detected genera in sputum samples from 1 patient collected at 4 different moments**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/42c10d1e-2787-442a-b723-304a3a108a98)

**Flowchart**

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/7999909e-337b-47f2-9560-73929772dbb3)

## Tables
**Theoretical Composition ZymoBIOMICS™ Microbial Community DNA Standard based on Genomic DNA**

<img width="209" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/2856f6d3-2f0f-4c51-b278-ebfb616d8a9d">

**Sputum samples collected for Microbiome analysis**

<img width="140" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/46ca91f7-ef83-46bb-b50a-db356484e777">

**Cultured bacteria in sputum samples**

<img width="302" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/426760d2-a3fc-41ad-9345-82d66bb8e64b">

**Basic quality measurements sequenced Sputum and Zymo mock samples with selection of top 10% and 90%  reads based on quality**

<img width="362" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/db74db63-c33b-4156-b5ed-db54f9fa910a">

**Basic quality measurements sequenced Sputum samples from 1 patient**

<img width="268" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/4389f24a-3d09-4a7b-8871-3e9fa3fb2afb">

**Computational performances of the three command-line pipelines, * indicates a difficult installation process, ** indicates an average installation process and *** indicates an easy installation process**

<img width="269" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/694d90f3-e7bb-49e1-b748-27c0f611cd4d">

## Data availability
The article can be viewed [here.](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/blob/main/Scientific%20paper%20COPD%20JGBR%20versie%202%20(draft).docx)
