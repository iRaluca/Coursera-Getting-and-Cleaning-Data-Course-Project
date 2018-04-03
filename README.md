## Coursera - [Getting and Cleaning Data](https://www.coursera.org/learn/data-cleaning) - Course Project

### Overview
The goal of this analysis is to prepare tidy data sets that can be used for later analysis. 

The original source (raw data) represents data collected from the accelerometers from the Samsung Galaxy S smartphone. More information can be found [here](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).

### In the repository can be found the following files:
* the result of the analysis (first and second tidy data set)
* the processing script "run_analysis.R"
* a code book that describes the variables, the data, any transformations or work that performed to clean up the data called CodeBook.md
* this README.md file that provide an overview of all the files from the repository and how they are connected.

### The steps that need to be performed in order to obtain the result of the analysis:
* fork this repository 
* clone it to your local working directory
* source the file "run_analysis.R": Example: source("run_analysis.R")
* call the function: run_analysis() - this function will also print all the main steps that are performed in this analysis
* to read more about the processing steps performed, please read: CodeBook.md file from this repository.

### Important notes:
    * System information:
        - Operating system: Windows
        - Platform: x86_64-w64-mingw32
    * R version:
        - 3.3.2 (2016-10-31)
    * Required libraries: 
        - dplyr
        - tidyr
