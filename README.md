# Lake Powell Inflow Comparisons
Comparisons of Lake Powell inflow Projections and scenarios

The code LakePowellForecastHistory.ipynb contains 6 blocks of code:
1.	 reads in all the needed python packages
2.	Pulls from the latest USBR 24 month study release and creates or updates the files from the regulated inflow: 
  a. 	inflow_24_months_wide.xlsx
  b.	inflow_24_months_wide.csv
3.	Pulls from the latest USBR 24 month study release and creates or updates the files from the unregulated inflow ESP traces:
  a.	inflow_24_months_wide_with_esp.xlsx
  b.	inflow_24_months_wide_with_esp.csv 
4.	Creates a forecast history comparison of all 24-month study releases starting in Jan 2025, using the regulated inflow.
5.	Compares the most recent release of the unregulated ESP 10th and 50th percentile projections to selected scenarios from the 5yearsMinimumSumHydrologyResults.xlsx, which are pulled from 
https://github.com/Anabelle374/Quantifying-Data-for-Extreme-Low-Inflow-and-Extreme-Low-Storage-Scenarios-for-Lake-Mead/tree/0d0031910fc2cafc3527fb576759873df44afe1a/HydrologyScenarios/AnnualDifferenceInFlow

6.	Lists the unique ensembles and how many scenarios in each that have an average natural flow less than 7.5 MAF.
