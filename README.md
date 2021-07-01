![cover image](https://hvoltbb.github.io/pics/blueshark.jpg)
# Tracking the effects of climate change on marine life - Case study 1
[3/19/21 update: article submitted. Text for each section will appear when finalized]

[5/27/21 update: major revision]

[6/17/21 update: minor revision]

[6/19/21 update: accepted]

## Quick View
**Background**: Substantial progress has been made in identifying large-scale climate effect on somatic growth through the use of ageing-based methods in aquatic environments, yet their annual/seasonal temporal resolution seems too coarse for such a fast process. 

**Problem statement**: Temporal resolution is a missing dimension in our understanding of climate effects on growth.

**Contributions**: An alternative source of high temporal resolution growth increments embedded within a multi-decadal traditional tag-recapture database was analysed to identify climate signals in the somatic growth of blue sharks Prionace glauca in the North Atlantic. Results indicate the growth response of P. glauca to the NAO occurred at a daily scale with a time-lag. Non-parametric modelling reveals an optimal response curve around the historical average of the NAO, and a significant negative response for large positive NAO anomalies. The temporal resolution of this study is unprecedented among current ageing-based studies with a comparable temporal coverage. Integrating high temporal resolution into long-term climate effect studies can open new avenues for research on identifying climate effect on growth and provide detailed clues to its mechanisms of action.

## Full Story

### Issues
1. Limitations of the hard-part bio-chronology approach to reliably achieve a higher temporal resolution 

2. An annual/seasonal resolution seems overly coarse, and may mask important climate signals due to excessive averaging.

Not being able to adopt a sufficiently high temporal resolution greatly constrains the power to track animal growth under climate change.

### Data
[Tagging database](https://www.fisheries.noaa.gov/inport/item/25121)

[NAO indices](https://www.cpc.ncep.noaa.gov/products/precip/CWlink/pna/nao.shtml)

Disclaimer: Neither of the datasets are owned/maintained by me. Please go to the original source to obtain your own copy of the file. Questions solely related to the dataset should be directed to the data maintainers found in the links above. However, if the links provided above are not working, let me know. The format of the current version of the data files might be different from my copy, and you may need to change some lines in the [preprocessing code](src/preprocess.R) to take that into account. 

My own copy of the data files will be conditionally provided through PM (latency: hours) or through an automatic email server by clicking [here](mailto:eidotog@gmail.com?subject=XxCLIMATE01xX&body=Do%20not%20modify%20the%20subject%20line.%20Not%20monitored.) (latency: secs). You may want to check your spam folder for the reply because replying an email in milliseconds isn't humanly possible and it will be flagged as spam the majority of the times. Note that I don't monitor these data requests. Once a request is fullfilled, the message will be permanantly removed from the server. No personal information will be collected by me.

### Example
The example files can be found [here](src/example). That folder contains an [R script](src/example/example.R) and a [TMB script](src/example/example.cpp). To run this example, one other [R script](src/preprocess.R), and two header files [1](src/growth.h) and [2](src/growth_imp.h) are needed.

Download the [source directory](src) first, and then make `example` you working directory. Then, you can source the [R script](src/example/example.R) to fit a von Bertalanffy curve to see if it works correctly on your machine. A verification value has been provided in the comment section at the bottom of the script. Getting exactly the same number as provided indicates success. Most likely, your R console will complain about missing libraries the first time you run it. Install them.

This code has been tested on both Windows and Linux systems. There are no system requirements to run the example.

### Full source code
It is recommended to go through the example above first to make sure you understand the core of the code, if you are not already familiar with TMB modelling. The control statements in the full source code can be too much for the first read. But once you understand the structure of the program, the code should be fairly simple to understand.

The source files contain R scripts [1](src/v3.R) and [2](src/preprocess.R), two header files [1](src/growth.h) and [2](src/growth_imp.h), and a [TMB script](src/v5.cpp).

The R code has been annotated and sectioned according to RStudio style. It is recommended to use RStudio to view the code.

This code has been tested on both Windows and Linux systems with 8+ GB of RAM. 

Warning: it is recommended to run the full program on a system with 8+ GB of RAM. Some of the large models require a substantial amount of memory to execute. Your system may freeze if you are low on available memory. Your R may crash if the TMB program is given a wrong set of inputs. You have been warned. Do save your work first.

Bug reports, feature requests, and colabs are welcome. 
