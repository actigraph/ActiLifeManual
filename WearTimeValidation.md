# Wear Time Validation Tab #

----------

The Wear Time Validation (WTV) tool in ActiLife allows users to easily flag invalid data (or data collected when a device was not worn) for exclusion from further analysis.  WTV also provides a summary of the wear-time and non-wear time results from the datasets.  The Data Screening Criteria allow users to define non-wear periods.  Data flagged as non-wear is not removed from the *.agd file - it is simply flagged (within the file) as "wear time" or "non-wear time".

The default Wear Time Validation algorithm uses the floating window technique.  This algorithm does not define wear or non-wear time from calendar hours, but rather looks at contiguous time and discerns how many total hours (and/or minutes) of non-wear time are in the file without regard for breaks in the calendar day/hour.  Conversely, the deprecated “Daily Algorithm” looks at calendar hours (e.g., 9:00am – 10:00am) and days (March 2 – March 3) to determine whether or not that hour (or day) is valid or not.  The floating window algorithm allows users to the same thing by using the “Flag Entire Day as Invalid…” option in the Optional Screening Parameters section.

The defaults defined for Wear Time screening (60 minutes of consecutive zeros with a 2 minute spike tolerance) were loosely derived from the research note Identification of accelerometer non-wear time and sedentary behavior, published in the Research Quarterly for Exercise and Sport, submitted to the journal on June 1, 2010.  Permission to share this article publically has been requested by ActiGraph to the managing editor of Research Quarterly for Exercise and Sport.

![](/assets/img/WearTimeValidation.png)

FIGURE 38 - WEAR TIME VALIDATION

## DEFINE A NON-WEAR PERIOD ##

This section provides options for defining the non-wear period.  ActiLife will use this information to scan the data for non-wear bouts.

*Begin non-wear bout after ____ minutes/epochs of consecutive zeros* - After scanning the data and detecting the selected number of consecutive zeros, ActiLife will begin flagging data as "non-wear time".  The leading zeros detected during this process will be flagged retroactively (after they have been initially scanned).  Data will be flagged as "non-wear time" until the Spike Tolerance is exceeded.

*Use Vector Magnitude* - When checked, ActiLife scans the vector magnitude of three-axis data (when available) to detect wear or non-wear time.  When unchecked, ActiLife scans only Axis 1 (the vertical axis - see users' manual for details) to detect wear/non-wear times.

*Use an activity threshold of _____ counts per minute/epoch* - Instead of looking for zeros to qualify non-wear time, this option allows the user to set a non-zero activity threshold requirement for wear-time.  Data below this value will be qualified as "zero".

*Spike Tolerance ____ minutes/epochs* - This option allows the user to set a "spurious count" tolerance.  ActiLife will continue scoring a non-wear bout as non-wear until it detects more than the Spike Tolerance number of minutes/epochs above zero (or above the activity threshold, if that option is enabled).
 
## OPTIONAL SCREENING PARAMETERS ##

*Ignore wear periods less than _____ minutes/epochs* - Because of the WTV algorithms used, some wear periods may be very short (shorter than the spike tolerance).  Use this option to set the minimum length of an acceptable wear period.

*Flag entire day as invalid if wear time less than _____ minutes/epochs* - Use this setting to flag an entire 24 hour day as invalid if there are less than the selected amount of valid (wear-time) minutes or epochs in the day.

*Change Wear Time Validation Algorithm* - This shortcut opens the Wear Time Validation options settings (also accessible from the Edit->Options menu) and allows the user to choose between the Floating Window and Daily WTV algorithm.

Once these settings are adjusted, press the “Run Selected” button to run the Wear Time Validation algorithm on the selected files.  Clicking the “Save Settings as Default” button will save the settings; ActiLife will remember them and use them each time the Wear Time Validation tool is opened.

## VIEWING DETAILS OF WEAR TIME VALIDATION RESULTS ##

Summary-level results of the Wear Time Validation process are available in the main grid immediately after the process has completed.  The following parameters are available:

* Wear Periods – The number of wear bouts detected by the algorithm for the entire data set
* Non-Wear Periods - The number of non-wear bouts detected by the algorithm for the entire data set.
* Wear Length – Total time the device was worn.
* Non-Wear Length – Total time the device was not worn.
* Avg Length Wear Period – Average length of the wear periods (or bouts).
* Avg Length Non-Wear Period - Average length of the non-wear periods (or bouts).
* Wear % - Percentage of wear-time for the entire data set
* Non-Wear % - Percentage of non-wear-time for the entire data set
* Avg Wear Time per Total Days (All Days) – Total wear time divided by the total number of days in the dataset.
* Avg Wear Time per Days with Wear Time – Total wear time divided by the total number of days in the dataset that have >0 wear time.
* Avg Non-Wear Time per Total Days - Total non-wear time divided by the total number of days in the dataset that have >0 wear time.
* Avg Non-Wear Time per Days with Wear Time - Total non-wear time divided by the total number of days in the dataset that have >0 wear time.

After the wear-time has been calculated, details of each wear and non-wear bout can be viewed by clicking the “Details” button to the right of each dataset file name as shown in Figure 39.

![](/assets/img/WtvDetailsButton.png)

FIGURE 39 – DETAILS VIEW SHOWS EPOCH-BY-EPOCH VALIDATION

Details about which days are considered “valid” can be seen in the details view.  An example is shown in Figure 40.  The Days section details out the number of Wear Time and Non-Wear-Time (in minutes) per calendar day.  The percentages of wear and non-wear for each day are also available here.  The VM column represents the total “Total Vector Magnitude Counts” for that day (see Appendix B – Vector Magnitude for more details).  This number can be used to gauge relative activity from day-to-day.

The Wear Time and Non-Wear Time Periods section details the wear and non-wear bouts as detected by the Wear Time Validation tool.  The “Use?” column indicates whether or not that particular bout will be considered or excluded when calculating output scores in the Data Scoring tool.  Non-wear periods are never used and wear periods are always used by default.  This can be changed by checking or un-checking the bout of interest.  Clicking “Save and Close” will store those changes in the *.agd file.

Clicking the “More” button next to a wear or non-wear bout will reveal the epoch level breakdown for that particular bout on the right hand side.  All data in this view can be copied/pasted by selecting the columns/rows of interest, pressing “Ctrl+C” on the keyboard to copy, then pressing “Ctrl+V” to paste the data into a spreadsheet or text editor.  Use the individual “export” links to export a wear or non-wear period into a *.csv file.

![](/assets/img/WtvDetails.png)

FIGURE 40 – DETAIL BREAKDOWN OF WEAR AND NON-WEAR TIME FOR A DATASET

## EXPORT REPORT ##

The “Export Report” option exports the information in the Wear Time Validation grid to a comma separated value file for sharing and manipulation.  Detailed data can be exported to CSV format from the “Details” view of each dataset.

## SCORE SELECTED ##
This option pushes the selected files into the Data Scoring tab.  This is typically the next step after Wear-Time Validation.  This button speeds up the process by eliminating the need to manually search for the files from the Data Scoring file importer.
