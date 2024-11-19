# DGE
Differential Gene Expression Analysis in Deseq2

# Prerequisites
R 4.4.1  -  Confirmed useable on local 11/19/2024

Required organization is 3 directories under the same parent directory with the following names. CASE SENSITIVE. These directories have already been made in this github.

Parent directory
-DGE
--DGE.rmd (the file that you should run which contains all of its package installers and the R code)

-DGE_outputs
-- where you will find the outputs of the DGE.rmd including the volcano plot

-files
--Tomoki_Kall_annotated_kallisto_output.csv
--Kall_annotated_kallisto_output.csv

You should change the files to your desired inputs.


# Usage

To specify the 2 cell types from the Truong lab data you are interested in DGEing, specify them by changing the values in the line code commented with '# Replace with your cell identities!'

# Notes

This pipeline was made for the internal bulkRNAseq Kallisto pseudoaligned data. Data from all Kallisto pseudoalignments of interest from SRA are in Kall_annotated_kallisto_output.csv with SRA IDs appended in a column titled SRA. Cell_identity was entered by the user who added that data to our database and should be uniform for all samples considered equivalent. Tomoki_Kall_annotated_kallisto_output.csv contains Dr. Tomoki Yanagi's bulkRNAseq runs for all of his cells and has the same structure as the Kall_annotated_kallisto_output.csv with the run IDs being in the SRA column. If your data has a different format, you will need to update this script accordingly.

Below are the columns in our csvs

target_id	length	eff_length	est_counts	tpm	external_gene_name	cell_identity	SRA
