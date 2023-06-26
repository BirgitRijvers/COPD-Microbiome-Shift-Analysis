# COPD-Microbiome-Shift-Analysis
<img width="812" alt="image" src="https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/ef7643ec-7762-463c-a389-09d1efb31ee2">


This is the repository for a bioinformatics project about identifying the optimal pipeline for identifying a potential microbiome shift in COPD patients after ceasing azithromycin treatment.


**Introduction** 
Chronic obstructive pulmonary disease (COPD) is a prevalent respiratory condition characterized by airflow obstruction and inflammation, often leading to acute exacerbations. While azithromycin shows promise in reducing exacerbations, concerns regarding antibiotic resistance and side effects arise with prolonged use. Understanding the impact of discontinuing azithromycin treatment on exacerbations and patient well-being requires assessing changes in the COPD-associated microbiome. We aimed to identify an optimal pipeline for analyzing 16S rRNA gene sequencing data by comparing five pipelines: NanoCLUST, NanoRTax, BugSeq, Emu, and Kraken2/Bracken. 

**Methods**
We evaluated their accuracy using a Zymo mock sample with known bacterial DNA composition and a sputum sample spiked with Allobacillus and Imtechella. NanoCLUST demonstrated robust performance for taxonomic classification on a genus level. Subsequently, we utilized NanoCLUST to analyze sputum samples from a single patient collected at months 0, 3, 6, and 9. Rstudio facilitated data visualization through heatmaps, enabling comparison of microbiome compositions across patient groups. 

**Results**
Among the pipelines evaluated, NanoCLUST stood out as the only one that consistently detected the same number of genera in both the sputum subsets and the Zymo mock subsets. The sputum sample was spiked with microbial cells from the Imtechella and Allobacillus genera. NanoCLUST detected all genera except Lactobacillus, but the pipeline identified Limosilactobacillus in the subsets which is a genus splitted from Lactobacillus. NanoCLUST accurately identified Imtechella with relative abundances of 2.4% and 2.1% in the 10% and 90% subsets, respectively. It also detected Allobacillus with relative abundances of 33.2% and 37.2% in the corresponding subsets. Over a period of 9 months a sputum sample was taken from a patient once every 3 months and sequenced, the relative abundance of genera in the 16s rRNA gene reads was analyzed with NanoCLUST. 

**Conclusion**
This study provides insights into COPD-associated microbiome changes and highlights NanoCLUST as a reliable pipeline for taxonomic analysis of 16S rRNA gene sequencing data. The visualization approach enhances interpretation and comparison of microbiome data in COPD research, advancing our understanding of the effects of discontinuing azithromycin treatment in COPD patients. 

## Flowchart

![image](https://github.com/BirgitRijvers/COPD-Microbiome-Shift-Analysis/assets/126883391/7999909e-337b-47f2-9560-73929772dbb3)

## Data availability
The article can be viewed here. 
