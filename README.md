## Submissions to PDL

For all submissions to the Population Demographics Lab (PDL) authors are required to provide a set of code which replicates the output (tables, figures, etc) of their analysis. For now the PDL is only accepting submissions which use the `R` programming language. Code for the submission must be hosted on a public facing git archive at the time of the submission (github, bitbucket, etc.), which will be copied and stored such that it meets NSF scientific reproducibility guidelines. The format of each project should resemble the directory structure seen below. 

```
project
│   README.md
│   main.R
│   ...
│
└───R
│   │   00_support_code.R
│   │   01_pre_run.R
│   │   ...
│
└───Data
    │   my_data.csv
    │   more_data.txt
    │   ...
```

The `README.md` should be a brief explanation, a paragraph or two, explaining what the code in your project does and what users should know before trying to run your code. 

The only file which should need to be run in order to replicate your analysis should be `main.R`. `main.R` should only be about 100 lines long, well commented and be the main set of code which produces your figures and tables. For most analyses 100 lines will probably not be enough space to replicate you're analysis. If this is the case, you will need to create additional `.R` files which to source which should be placed under a folder in the main project directory labeled simply `R`. In addition your analyses may also require data files which to pull from. These files should be placed in a subdirectory entitled `Data` as seen above.

Most, if not all, analyses will also require the use of additional `R` packages. For libraries which are part of either _CRAN_ or _bioconductor_ you only need to make the library calls in either the `main.R` file or in any of the `.R` files in the `R` subdirectory. For libraries which are not hosted on either _CRAN_ or _bioconductor_ we ask that you load these libraries in the `main.R` with instructions on how to install the packages.

All code submitted to the PDL will be tested on CSDE servers running Debian 5.x servers. If you have other external dependencies required to run your code please let us know on the submission forms.

An example submission is shown in this project. See `main.R` for more info.
