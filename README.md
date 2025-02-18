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

git clone https://github.com/Rimsk/gdc-download-pipeline.git
Alternatively, you can download the ZIP file directly from the repository page.

Usage

Set up the pipeline configuration: Before starting the download, you need to configure the config.R file, where you can specify the following:
GDC data portal API endpoint (defaults to GDC API endpoint)
Types of data to download (e.g., gene expression, mutations, clinical)
Filters to apply for specific datasets (e.g., specific project, disease type, sample type)


Run the download pipeline: Execute the gdc_download.R script in R. You can provide input parameters such as the project IDs, data types, and destination folder.
Example:

source("gdc_download.R")
download_gdc_data(
  project_id = "TCGA-BRCA",
  data_types = c("Gene Expression", "Somatic Mutations"),
  output_dir = "./gdc_data"
)
This command will download the data for the TCGA-BRCA project, including gene expression and somatic mutation data, and store it in the ./gdc_data directory.
Monitor the download: The script provides progress output to the console and handles any errors during the download process. If a download is interrupted, it will resume automatically when run again.
Data processing: After the download is complete, you can further process the data using additional R scripts provided in the repository, depending on your analysis goals.
Example Workflow

Clone the repository.
Install the necessary dependencies.
Modify config.R to specify the datasets you want to download.
Run gdc_download.R to start downloading data from the GDC.
Process the downloaded files as needed for your analysis.
Directory Structure

The pipeline organizes downloaded data into a structured directory format. Below is an example of how the directory structure might look after downloading data:

/gdc_data/
    /TCGA-BRCA/
        /Gene_Expression/
            file1.txt
            file2.txt
        /Somatic_Mutations/
            mutation1.maf
            mutation2.maf
        /Clinical/
            clinical_data.tsv
Contributing

Contributions to this pipeline are welcome! Please fork the repository and submit pull requests for any improvements or fixes.

When contributing, please ensure that your changes maintain compatibility with the existing pipeline, and provide proper documentation for any new features or bug fixes.

License

This project is licensed under the MIT License - see the LICENSE file for details.


