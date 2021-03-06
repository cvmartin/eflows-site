## What is `eflows`?

`eflows` is an open-source framework for managing energy-related data and apply functions over it. It is written in R and C++.

As an R package, it can be used either interactively in an R programming environment, or embedded in an R script into a larger automated infrastructure. 

The functions and algorithms are integral part of the framework. These can be used to:

- **Describe**: To predict how an energy system will behave without steering it (no "smart management" involved). The main functions are `simulate()` and `distribute()`.

- **Timeshift**: To steer the energy system, so the demand is realized when is more convenient. Timeshifting involves either delaying the energy consumption (`foreshift()`) or storing it beforehand (`backshift()`).

![Foreshift and backshift](../../app/www/images/general/fore-backshift.png)

`eflows` can be used as the core of an Energy Management System (EMS). That said, having a functional EMS requires extra software components customized to interact with the EMS hardware: 

- A component to gather real-time data from devices and other data sources (like weather forecasts). This may involve heavy use of predictive models, that are absent from `eflows`.

- A component to relay instructions to the devices so they are steered following the results obtained with `eflows`.

## Getting started

Working with `eflows` requires an installation of [R](https://www.r-project.org/). In addition, [R studio](https://www.rstudio.com/) is highly recommended for visualizing the results as graphs.

The package is not available in CRAN, but it can be installed from github using the R console: ` devtools::install_github('cvmartin/eflows')`. The companion package `eflows.viz` is used for visualizations, and it is installed in the same way: `devtools::install_github('cvmartin/eflows.viz')`. 

