[comment]: <> (Hi. If you are seeing this message, please open this file with markdown preview or jupyter notebook. You can do this by right clicking on the readme file and picking 'open with'.)
![course-card](images/module_anchor_image.png)
# University of Maine Cloud Training Tutorials for RNA-seq and Network Analysis

## Overview

Included here are several tutorials in the form of 'Jupyter notebooks'.

The purpose of these tutorials is to help users familiarize themselves with the cloud computing in the specific context of running bioinformatics workflows. Here is a link to a [YouTube video](https://youtube.com) that gives you an overview of the tutorials.

These tutorials do this by going step-by-step through specific workflows for bulk RNA-Seq, small RNA-Seq and single cell RNA-Seq (scRNA-Seq). These workflows cover the start to finish of basic bioinformatics analysis; starting from downloading raw sequence data, and extending to differential gene expression analysis, and producing common plots in R.

## Table of Contents

[Requirements](#requirements)  
[Getting Started](#getting-started)  
[Workflows](#workflows)  
[Data](#data)  
[Support Forum Thanks](#support-forum-thanks)  
[Funding](#funding)  
   

## Requirements

These tutorials were designed to be used on cloud computing platforms, with the aim of requiring nothing but the files within this GitHub repository.

With this in mind, our tutorials use Jupyter Notebook files, which Google Cloud Platform, Amazon Web Service, and Microsoft Azure all provide support for. Therefore, requirements should only require creation of a virtual machine on one of these providers, and the downloading of this github's files to that machine.

For more information on creating a virtual machine and downloading our GitHub repo to that machine, we have a getting started section below. Currently this section only includes information on how to do this using Google Cloud Platform.

## Getting Started

This repository contains several notebook files which serve as bioinformatics workflow tutorials.

The below steps guide you through setting up a virtual machine on Google Cloud Platform, downloading our tutorial files, and running those files. 

Accordingly, before starting, make sure you have a google account and have access to a Google Cloud Platform Project.

Once you have these, you can begin by first navigating to https://console.cloud.google.com/ and logging in with your credentials. Then, in the top left of the screen, navigate to 'select a project', and choose the project you belong to.

This tutorial will cost you just less than $x.xx assuming a n1-standard-8 machine, and assuming you delete the virtual machine and the storage bucket after you finish the tutorial. You can save some time by using an n2 machine, but it will cost a little bit more (thought not that much). 

### Creating a user managed notebook 

Follow the steps highlighted [here](https://github.com/STRIDES/NIHCloudLabGCP/blob/main/docs/vertexai.md) to create a new user-managed notebook in AWS SageMaker. Follow steps 1-8 and be especially careful to enable idle shutdown as highlighted in step 7. For this module you should select Debian 10 and R 4.2 in the Environment tab in step 5. In step 6 in the Machine type tab, select n1-standard-4 from the dropdown box.

To clone this repository, use the Git command `git clone https://github.com/King-Laboratory/scRNASeq-miRNASeq-and-TF-Network-Analysis.git` in the dropdown menu option in Jupyter notebook. Please make sure you only enter the link for the repository that you want to clone. There are other bioinformatics related learning modules available in the [NIGMS Repository](https://github.com/NIGMS). This should download our repo, and the tutorial files inside, into a folder called 'RNA-Seq-Differential-Expression-Analysis'. Double click this folder now. Inside you will find all our tutorial files, which you can double click and run.

### Stopping Your Virtual Machine

When you are finished running code, you can turn off your virtual machine to prevent unneeded billing or resource use by checking your notebook and pushing the **Stop** button.

## Workflows

Our tutorials are broken down into 'workflows'. Each notebook file covers a specific workflow, which contains written and visual commentary, as well as the actual step-by-step code for running that workflow analysis. 

These notebooks were designed to be run using a virtual machine on a cloud computing provider. For more information on how to do this; navigate to the [Getting Started](#getting-started) section. Feel free to explore and run the workflows in any order you like. 

![RNA-Seq workflow](images/Cloud_Modules.png)

### Species-Specific Bulk RNA-Seq Workflows

#### Tutorial 1: A short introduction to downloading and mapping sequences to a transcriptome using Trimmomatic and RSEM.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_mouse.ipynb) - Mouse workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1B_alignment_full_dataset_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_full_dataset_mouse.ipynb) - Mouse workflow using the full dataset including downloading reads from SRA.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_1_alignment_zebrafish.ipynb) - Zebrafish workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1B_alignment_full_dataset_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_1_alignment_full_dataset_zebrafish.ipynb) - Zebrafish workflow using the full dataset including downloading reads from SRA.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_c_elegans.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_c_elegans.ipynb) - *C. elegans* workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1B_alignment_full_dataset_c_elegans.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_full_dataset_c_elegans.ipynb) - *C. elegans* workflow using the full dataset including downloading reads from SRA.

#### Tutorial 2: Analysis of read counts using R/DESeq2.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_mouse.ipynb) - Mouse workflow starting with read counts.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_2_DEG_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_zebrafish.ipynb) - Zebrafish workflow workflow starting with read counts.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_2_DEG_c_elegans.ipynb](Bulk_RNA-Seq_C_elegans/Tutorial_2_DEG_c_elegans.ipynb) - *C. elegans* workflow workflow starting with read counts.

#### Tutorial 2B: Analysis of mouse transcription factor networks using NetAct.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2B_NetAct_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2B_NetAct_mouse.ipynb) - Mouse workflow starting with read counts.

### Species-Specific Small RNA-Seq Workflows

#### Tutorial 3: Analysis of small RNA-Seq reads using miRGeneDB annotation of microRNAs with R/DESeq2.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_Mouse/Tutorial_3_miRNA_mouse.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_Mouse/Tutorial_3_miRNA_mouse.ipynb) - Mouse workflow starting with read counts.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_Zebrafish/Tutorial_3_miRNA_zebrafish.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_Zebrafish/Tutorial_3_miRNA_zebrafish.ipynb) - Zebrafish workflow workflow starting with read counts.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_C_elegans/Tutorial_3_miRNA_c_elegans.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_C_elegans/Tutorial_3_miRNA_c_elegans.ipynb) - *C. elegans* workflow workflow starting with read counts.

### Single Cell RNA-Seq Workflows

#### Tutorial 4: Single Cell RNA-Seq Workflows using R/seurat.

[Single_Cell_RNA-Seq_Tutorials/Single_Cell_RNA-Seq_Mouse/Tutorial_4_scRNA-Seq_mouse.ipynb](Single_Cell_RNA-Seq_Tutorials/Single_Cell_RNA-Seq_Mouse/Tutorial_4_scRNA-Seq_mouse.ipynb) - Mouse workflow starting with read counts.

## Data

These tutorials use example sequence data procured from the Sequence Read Archive. 

## Support Forum Thanks

Support forum thanks. For almost any programming project, contributions to online databases and support forums are an invaluable resource that are heavily leaned upon. Thank goodness for those people who take the time to answer silly questions.

## Funding

Funded by NIH grant number T32 GM132006 the Maine INBRE Program (NIH/NIGMS P20 GM103423).

## **License for Data**

Text and materials are licensed under a Creative Commons CC-BY-NC-SA license. The license allows you to copy, remix and redistribute any of our publicly available materials, under the condition that you attribute the work (details in the license) and do not make profits from it. More information is available [here](https://tilburgsciencehub.com/about).

![Creative commons license](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

