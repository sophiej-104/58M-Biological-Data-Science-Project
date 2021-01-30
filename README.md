---------------------------------------------------------------
58M-Biological-Data-Science-Project
---------------------------------------------------------------

# Assessing Macrophage Activation and Response to Bacterial Infection *in vitro*

The aim of this project is to reproduce an investigation into macrophage activation and response to bacterial infection from previous use of the Summit software system during the Stage II module Laboratory and Professional Skills for the Bioscientist - Bioscience Techniques, Immunology strand. 

---------------------------------------------------------------
Packages Required
---------------------------------------------------------------

* tidyverse (Version 1.3.0)
* ggplot2 (Version 3.3.2)
* flowCore (Version 2.2.0)
* ggcyto (Version 1.18.0)
* patchwork (Version 1.1.1)

The code here can be copied and run directly in R to install the packages

#Installing the tidyverse

install.packages("tidyverse")

#Installing ggplot2

install.packages("ggplot2")

#Installing the flowCore package (information can be found at: http://www.bioconductor.org/packages/release/bioc/html/flowCore.html)
#Please note this works for R version "4.0", for earlier versions of R please see the webpage provided for more information

if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("flowCore")

#Installing ggcyto (also a part of the Bioconductor project: https://www.bioconductor.org/packages/release/bioc/html/ggcyto.html)
#Please note this works for R version "4.0", for ealier versions of R please see the webpage provided for more information

if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("ggcyto")

#Installing patchwork

install.packages("patchwork")

#To install the wordcount addin used: 

devtools::install_github("benmarwick/wordcountaddin", type = "source", dependencies = TRUE)

--------------------------------------------------------------
Set Up
--------------------------------------------------------------

The .fcs files containing the flow cytometry data along with the .csv file containing the data to calculate molecular weights should be contained in the data-raw folder. The image for the western blot is contained in the folder labelled images. 

To aid understanding of the column names in the .fcs files there is an additional .xlsx file within the data-raw folder called panel(1).xlsx

--------------------------------------------------------------
Additional Instructions
--------------------------------------------------------------

If using the script to process alternative data to that provided, the data will need to be checked to contain spillover data in order to carry out the compensation steps. This is done using the spillover() function from the flowCore package (this step is already included in the code chunk). If the spillover data is contained under a different key word to that for this current data set adjustments to the code chunks can be made. If the data being used returns NULL for every key word (no spillover data), manual compensation may need to be carried out instead. 