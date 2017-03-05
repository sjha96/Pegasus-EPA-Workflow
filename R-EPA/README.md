# R-EPA Workflow

Generating a Workflow
---------------------
Run the generate_dax.sh script.

Running a Workflow
-------------------
Run the plan_dax.sh script.

Workflow Description
-------------------
Source: https://www3.epa.gov/caddis/da_software_rscript12.html

All the base R scripts and data sets are obtained from the EPA website above.
The R scripts were modified to generate input and output files instead of local 
objects that the scripts initially relied on. Only setupvar.R, weighted.average.R 
and cumulative.percentiles.R scripts were used in this example. The oregon data sets 
were not used in this example but are provided as inputs anyway for completion's sake.

This example demonstrates the usage of a split workflow. The setupvar.R script is first 
run to parse the input files into csv format that the other scripts will import and use.
Once these csv files are generated, they are used as inputs to weighted.average.R and
cumulative.percentiles.R scripts. The scripts run their own analysis and generate their
respective csv files and jpg files in the case of cumulative percentiles script. 
There should be a total of 5 output files at the end of the workflow: 3 jpg files and
2 csv files.
