![cover image](https://hvoltbb.github.io/pics/cover_pic2.png)
# Tracking the effects of climate change on marine life - Case study 1
[3/19/21 update: article submitted. Text for each section will appear when finalized]

[5/27/21 update: major revision]
## Quick View
**Background**: 

**Problem statement**: 

**Contributions**: 

## Full Story

### Issues
1.
2.
### Data
[Tagging database](https://www.fisheries.noaa.gov/inport/item/25121)

[NAO indices](https://www.cpc.ncep.noaa.gov/products/precip/CWlink/pna/nao.shtml)

Disclaimer: Neither of the datasets are owned/maintained by me. Please go to the original source to obtain your own copy of the file. Questions solely related to the dataset should be directed to the data maintainers found in the links above. However, if the links provided above are not working, let me know. The format of the current version of the data files might be different from my copy, and you may need to change some lines in the [preprocessing code](src/preprocess.R) to take that into account. My own copy of the data files will be conditionally provided through PM (latency: hours) or through an automatic email server by clicking [here](mailto:eidotog@gmail.com?subject=XxCLIMATE01xX&body=Do%20not%20modify%20the%20subject%20line.%20Not%20monitored.) (latency: secs; offline on 6-1-2021, all outstanding requests will be fullfilled once online). You may want to check your spam folder for my reply because replying an email in milliseconds isn't humanly possible and it will be flagged as spam the majority of the times.

### Example
The example files can be found [here](src/example). That folder contains an [R script](src/example/example.R) and a [TMB script](src/example/example.cpp). To run this example, one other [R script](src/preprocess.R), and two header files [1](src/growth.h) and [2](src/growth_imp.h) are needed.

Download the [source directory](src) first, and then make `example` you working directory. Then, you can source the [R script](src/example/example.R) to fit a von Bertalanffy curve to see if it works correctly on your machine. A verification value has been provided in the comment section at the bottom of the script. Most likely, your R console will complain about missing libraries the first time you run it. Install them.

This code has been tested on both Windows and Linux systems. There are no system requirements to run the example.

### Full source code
It is recommended to go through the example above first to make sure you understand the core of the code, if you are not already familiar with TMB modelling. The control statements in the full source code can be too much for the first read. But once you understand the structure of the program, the code should be fairly simple to understand.

The source files contain R scripts [1](src/v3.R) and [2](src/preprocess.R), two header files [1](src/growth.h) and [2](src/growth_imp.h), and a [TMB script](src/v5.cpp).

The R code has been annotated and sectioned according to RStudio style. It is recommended to use RStudio to view the code.

This code has been tested on both Windows and Linux systems with 8+ GB of RAM. 

Warning: it is recommended to run the full program on a system with 8+ GB of RAM. Some of the large models require a substantial amount of memory to execute. Your system may freeze if you are low on available memory. Your R may crash if the TMB program is given a wrong set of inputs. You have been warned. Do save your work first. 

Bug reports, feature requests, and colabs are welcome. 
