# Data

## Abstract

We apply WiSER to three datasets in order to investigate factors related to intra-individual variability: the Women’s Health Study Accelerometry Study (WHS available via dbGaP), The Action to Control Cardiovascular Disease (ACCORD available via BioLINCC), and S&P 500/ President Trump’s Twitter Data (publicly available). WHS data contains accelerometer data on over 15,000 women over 7 days. ACCORD data contains data from a multi-center trial in patients with type II diabetes. The S&P 500/Trump Twitter data is data downloaded from publicly available web APIs that contain Trump's Tweets and Daily historic stock data from the stocks in S&P 500. 


## Availability


- [x] Data **are** publicly available.

### Publicly available data

- [x] Data are available online at:
    - S&P 500/Trump Twitter: S&P500 data are publicly available to download via Stock APIs, unemployment rate was obtained from the Federal Reserve Economic Data (FRED) database at https://fred.stlouisfed.org/series/UNRATE, and Trump's tweets are downloaded from http://www.trumptwitterarchive.com/. The workflow for downloading this data is given, but we also supply the data in the GitHub repository for this analysis in the `trump_twitter_stock_analysis` subfolder.

- [x] Data are publicly available by request, following the process described here:

    * WHS: From dbGaP, the protocols and requirements for requesting data are available at: https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001964.v1.p1

    * ACCORD: From BioLINCC, the protocols and requirements for requesting data are available at:  https://biolincc.nhlbi.nih.gov/studies/accord/ 


## Description

### File format(s)

- [x] CSV or other plain text.

### Data dictionary
- [x] Available at the following URL: 
    * WHS: From variable descriptions are located at: https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/dataset.cgi?study_id=phs001964.v1.p1&phv=427400&phd=8090&pha=&pht=9960&phvf=&phdf=&phaf=&phtf=&dssp=1&consent=&temp=1

    * ACCORD: the Data Dictionary for the ACCORD data is available from BioLINCC at:  https://biolincc.nhlbi.nih.gov/studies/accord/ under the "Study Documents" section. 

# Part 2: Code

## Abstract

Code to download data (when applicable), clean data, and reproduce results are provided in the form of Jupyter Notebooks in the GitHub respository for this project. The subfolders contain code/related content for each analysis found in the paper. 

## Description

### Code format(s)


- [x] Package
    - [ ] R
    - [ ] Python
    - [ ] MATLAB toolbox
    - [x] Other: WiSER.jl at https://GitHub.com/OpenMendel/WiSER.jl 
- [x] Reproducible report 
    - [x] R Markdown
    - [x] Jupyter notebook

### Supporting software requirements

#### Version of primary software used

WiSER.jl version v0.0.2.

#### Libraries and dependencies used by the code

- R packages (used for plotting): data.table, facetscales, ggplot2, gridExtra, scales
- Julia Packages: WiSER (and its dependencies found at https://GitHub.com/OpenMendel/WiSER.jl/blob/master/Project.toml), CodecZlib, CSV, DataFrames, DelimitedFiles, GLM, KNITRO [academic license], MarketData, RCall, Roots, SpecialFunctions, StatsBase, TimeZones, DelimitedFiles.


### Parallelization used

- [x] No parallel code used


### License

- [x] MIT License (default)


### Additional information (optional)

Parallelization of code was not used, but is easily possible in WiSER, shown in its GitHub documentation. 

Julia allows for easy reproducibility, by including a `Manifest.toml` and `Project.toml` pair in each subfolder. The user can simply run `] activate .` in Julia at that directory and the correct environment with Julia package dependencies used will run.

# Part 3: Reproducibility workflow


## Scope

The Jupyter notebooks and code provided can be used to reproduce all results (including tables and figures) in Sections 5 and 6, and their accompanying supplementary material sections (S.5-S.8). 

## Workflow

### Format(s)

- [x] Self-contained R Markdown file, Jupyter notebook, or other literate programming approach

### Instructions

Each subfolder in the GitHub repository links to certain sections of the paper (Simulations, Women's Health Study, ACCORD, Twitter/Stock data). These each contain Jupyter notebooks with extensions `.ipynb` that go step-by-step through the workflow of the analyses presented in the paper, starting from downloading the data (when applicable), to cleaning the data, to analyzing the data. Once you have access to the data sets that require researcher requests, you can run these notebooks with the data and it will produce the results seen in the paper. For easy readability, `.html` files of the rendered notebooks are also included, which can be opened to view the notebook contents without launching Jupyter. 

**Note**: In order to run Julia in a Jupyter notebook, you must install Julia and the IJulia package. After downloading and launching Julia, IJulia can be installed and Jupyter notebook can be launched by running the following code in Julia:

```
using Pkg
Pkg.add("IJulia")
Pkg.build("IJulia")
using IJulia
notebook()
```

### Expected run-time

Approximate time needed to reproduce the analyses on a standard desktop machine:
- [x] > 8 hours

### Additional information (optional)

The simulations take the bulk of the time. The real data analyses, including cleaning the data, should take under an hour on a standard desktop machine. 

