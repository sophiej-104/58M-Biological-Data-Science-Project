===============================================================
58M-Biological-Data-Science-Project
===============================================================

#Assessing Macrophage Activation and Response to Bacterial Infection *in vitro*

The aim of this project is to reproduce an investigation into macrophage activation and response to bacterial infection from previous use of the Summit software system during the Stage II module Laboratory and Professional Skills for the Bioscientist - Bioscience Techniques, Immunology strand. 

---------------------------------------------------------------
Packages Required
---------------------------------------------------------------

* tidyverse (Version 1.3.0)
* ggplot2 (Version 3.3.2)
* flowCore (Version 2.2.0)
* ggcyto (Version 1.18.0)
* ggpubr (Version 0.4.0)

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

#Installing ggpubr
install.packages("ggpubr")