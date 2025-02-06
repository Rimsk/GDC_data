# GDC_data
GDC Download Pipeline Using R

This repository provides an R-based pipeline for downloading genomic data from the Genomic Data Commons (GDC), part of the National Cancer Institute (NCI). The pipeline allows users to efficiently retrieve, process, and store datasets from GDC, including whole-genome sequencing data, gene expression data, and other bioinformatics files.

Features

Automated download of raw and processed genomic data from the GDC portal.
Support for various data types such as gene expression, somatic mutations, clinical data, and more.
Integration with GDC's API to facilitate easy data retrieval.
Capabilities for downloading and organizing data into a local directory structure.
Data filtering options to refine the selection of data for downloading.
Option to handle large-scale downloads, resume interrupted downloads, and manage download queues.
Prerequisites

R (>= 4.0)
The following R packages are required:
httr
jsonlite
curl
data.table
R.utils
You can install these packages using the following R command:

install.packages(c("httr", "jsonlite", "curl", "data.table", "R.utils"))
Installation

To use this pipeline, you can clone the repository to your local machine using Git:

git clone https://github.com/your-username/gdc-download-pipeline.git
Alternatively, you can download the ZIP file directly from the repository page.

Usage

Set up the pipeline configuration: Before starting the download, you need to configure the config.R file, where you can specify the following:
GDC data portal API endpoint (defaults to GDC API endpoint)
Types of data to download (e.g., gene expression, mutations, clinical)
Filters to apply for specific datasets (e.g., specific project, disease type, sample type)
