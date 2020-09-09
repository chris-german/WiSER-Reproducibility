# Data

## Abstract

We apply WiSER to three datasets: the Women’s Health Study Accelerometry Study (WHS via dbGaP), The Action to Control Cardiovascular Disease (ACCORD via BioLINCC), and S&P 500/ President Trump’s Twitter Data (publicly available). WHS data contains accelerometer data on over 15,000 women over 7 days. ACCORD data contains data from a multi-center trial in patients with type II diabetes. The S&P 500/Trump Twitter data is data downloaded from publicly available web APIs.  


## Availability


- [x] Data **are** publicly available.

### Publicly available data

- [x] Data are available online at:
    - S&P 500/Trump Twitter: S&P500 data are publicly available to download via Stock APIs, unemployment rate was obtained from the Federal Reserve Economic Data (FRED) database at https://fred.stlouisfed.org/series/UNRATE, and Trump's tweets are downloaded from http://www.trumptwitterarchive.com/.

- [x] Data are publicly available by request, following the process described here:

    * WHS: From dbGaP, the protocols and requirements for requesting data are available at: https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001964.v1.p1dbGaP

    * ACCORD: From BioLINCC, the protocols and requirements for requesting data are available at:  https://biolincc.nhlbi.nih.gov/studies/accord/ 


## Description

### File format(s)

- [x] CSV or other plain text.

### Data dictionary
- [x] Available at the following URL: 
    - WHS: From dbGaP, the protocols and requirements for requesting data are available at: https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001964.v1.p1dbGaP
    - ACCORD: From BioLINCC, the protocols and requirements for requesting data are available at:  https://biolincc.nhlbi.nih.gov/studies/accord/ 

# Part 2: Code

## Abstract

Code to download data (when applicable), clean data, and reproduce results are provided in the form of Jupyter Notebooks in the github respository for this project. The subfolders contain code/related content for each analysis found in the paper. 

## Description

### Code format(s)


- [x] Package
    - [ ] R
    - [ ] Python
    - [ ] MATLAB toolbox
    - [x] Other: WiSER.jl at https://github.com/OpenMendel/WiSER.jl 
- [x] Reproducible report 
    - [x] R Markdown
    - [x] Jupyter notebook

### Supporting software requirements

#### Version of primary software used

WiSER.jl version v0.0.2.

#### Libraries and dependencies used by the code

R packages: ggplot2, facetgrid
Julia Packages: WiSER (and its dependencies found at https://github.com/OpenMendel/WiSER.jl/blob/master/Project.toml), KNITRO, StatsBase, DataFrames, CSV, MarketData, TimeZones, CodecZlib, Roots, SpecialFunctions, DelimitedFiles, GLM




### Parallelization used

- [x] No parallel code used


### License

- [x] MIT License (default)


### Additional information (optional)

Parallelization of code was not used, but is easily possible in WiSER, shown in its github documentation. 

# Part 3: Reproducibility workflow


## Scope

The jupyter notebooks and code provided can be used to reproduce all results (including tables and figures) in Sections 5 and 6, and their accompanying supplementary material sections (S.5-S.8). 

## Workflow

### Format(s)

- [x] Self-contained R Markdown file, Jupyter notebook, or other literate programming approach

### Instructions

Each subfolder in the github repository links to certain sections of the paper (Simulations, Women's Health Study, ACCORD, Twitter/Stock data). These each contain jupyter notebook that go step-by-step through the workflow of the paper, starting from cleaning the data to analyzing the data. Once you have access to the data, you can run these notebooks with the data and it will produce the results seen in the paper. 

### Expected run-time

Approximate time needed to reproduce the analyses on a standard desktop machine:
- [x] > 8 hours

### Additional information (optional)

The simulations take the bulk of the time. The real data analyses, including cleaning the data, should take under an hour on a standard desktop machine. 

