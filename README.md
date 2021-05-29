![cover image](https://hvoltbb.github.io/pics/cover_pic2.png)
# Tracking the effects of climate change on marine life - Case study 1
[3/19/21 update: article submitted. Text for each section will be available when finalized]

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

### Example
The example files can be found [here](src/example). That folder contains an [R script](src/example/example.R) and a [TMB script](src/example/example.cpp). To run this example, one other [R script](src/preprocess.R), and two header files [1](src/growth.h) and [2](src/growth_imp.h) are needed.

Download the [source directory](src) first, and then make `example` you working directory. Then, you can source the [R script](src/example/example.R) to fit a von Bertalanffy curve to see if it works correctly on your machine. A verification value has been provided in the comment section at the bottom of the script. Most likely, your R console will complain about missing libraries the first time you run it. Install them.

This code has been tested on both Windows and Linux systems. There are no system requirements to run the example.

### Full source code
It is recommended to go through the example above first to make sure you understand the core of the code, if you are not already familiar with TMB modelling. The controlling statements in the full source code can be too much for the first read. But once you understand the structure of the program, the code should be fairly simple to understand.

The source files contain R scripts [1](src/v3.R) and [2](src/preprocess.R), two header files [1](src/growth.h) and [2](src/growth_imp.h), and a [TMB script](src/v5.cpp).

The code has been annotated and sectioned according to RStudio style. It is recommended to use RStudio to view the code.

This code has been tested on both Windows and Linux systems with 8+ GB of RAM. 

Warning: it is recommended to run the full program on a system with 8+ GB of RAM. Some of the large models require a substantial amount of memory to execute. Your system may freeze if you are low on available memory. Your R may crash if the TMB program is given a wrong set of inputs. You have been warned. Do save your work first. 

Bug reports, feature requests and colabs are welcome. 
