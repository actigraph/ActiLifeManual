Data Scoring Tab
================

--------------

Data Scoring in ActiLife allows users to analyze the details of their
dataset(s) by examining Energy Expenditure, METs, Activity Cut Points,
Activity Bouts, and Heart Rate Energy Expenditure. Figure 41 illustrates
the Data Scoring tool in action.

.. figure:: /assets/img/DataScoring.png
   :alt: 

FIGURE 41 - DATA SCORING

DATE AND TIME FILTERS
---------------------

Date and time filtering allows users to isolate the data scoring to
specific dates or times of interest. The results shown in the Data
Scoring tool only apply to the date and time filters shown in the Date
and Time Filters grid. If no filters are present, the Data Scoring
results are not limited to any dates or times, but include the entire
scope of the datasets.

Multiple filters can be added simultaneously to specifically target
certain days or times. To add a filter, click the “+” button from within
the Date and Time Filters grid as shown in Figure 42. Only checked
filters will be applied during data scoring. Multiple filters can be
checked which forces the Data Scoring tool to generate results for two
different time periods. For example, creating a Weekend Mornings filter
for Weekends from 6am-10am and then a Weekend Afternoons filter for
Weekends from 3pm-6pm would produce data scoring results for both of
those time periods only.

.. figure:: /assets/img/FilterEntry.png
   :alt: 

FIGURE 42 - DATE/TIME FILTER ENTRY

Date and time filters can be removed by clicking the “X” icon to the
right of the filter. Remove all filters by clicking the “X” at the top
of the grid. Date and Time Filters persist in ActiLife even if the
program is closed and re-opened.   ## DATA SCORING PARAMETERS AND
ALGORITHMS ##

There are five optional parameters that can be calculated from within
the Data Scoring tool: Energy Expenditure, METs, Cut Points, Bouts, and
Heart Rate Energy Expenditure (HREE). Each parameter has multiple
algorithms from which to choose. Each algorithm has been derived by
independent researchers from around the world using ActiGraph devices.
To view details about the origin of each algorithm, click the “?” icon
to the right of each scoring parameter. Check the checkbox next to each
parameter you wish to calculate for your dataset(s). Unchecked
parameters will not be calculated, displayed, or exported.

ENERGY EXPENDITURE
------------------

To calculate energy expenditure, check the box next to the “Energy
Expenditure” parameter in the Data Scoring tool. Each dataset in the
Data Scoring grid must have an associated body. Weights can be added by
clicking on the “Weight” box in the Data Scoring grid and typing in the
subject’s weight. Select “Worn on Wrist” if the device was worn on the
wrist to apply the appropriate scaling.

    Important: The “Worn On Wrist?” option scales down the activity
    counts based on an internally-developed algorithm. At this time,
    there are no validated energy expenditure algorithms for wrist-worn
    actigraphy. Validated energy expenditure can only be estimated from
    waist-worn devices.

METS
----

METs, or metabolic equivalent of task, can also be calculated from
within the Data Scoring tool. Multiple algorithms are available. When
calculating Children’s METS (Using the “Children Freedson” equation), an
age must be entered for each file. If the device was worn on the wrist,
the subject’s gender is required.

CUT POINTS
----------

Cut point data scoring option allows users to break out the proportion
of time (total epochs) within each dataset the subject spent in
different categories of activity intensity. Multiple validated cut point
sets are available by default from within ActiLife. Users can create
their own cut point set by clicking the “edit…” link to the right of the
Cut Point dropdown and clicking the “+” icon at the bottom of the list
as shown in Figure 43. Enter a Set Name for the new cut point set and
type in the maximum values for each level (click the “+” icon to create
new Cut Points). Once complete, click “Save”.

When the “Cut Points based on Vector Magnitude” box is checked, ActiLife
will look at the Vector Magnitude count levels for each epoch. When left
unchecked, the cut points apply only to the Axis 1 values for each
epoch.

Details about the default Cut Point algorithms in ActiLife can be found
by clicking the “?” icon next to the Cut Points option.

.. figure:: /assets/img/CutPointSets.png
   :alt: 

FIGURE 43 - CUSTOM AND DEFAULT CUT POINTS

BOUTS
-----

Bouts of activity can be detected within each data set in the Data
Scoring tab. Use the “Bouts” option to define a bout length, the minimum
per-epoch count level, the maximum per-epoch count level and the drop
time.

MIN LENGTH
~~~~~~~~~~

This option tells ActiLife the minimum bout length to look for.

MIN COUNTS
~~~~~~~~~~

This option tells ActiLife the minimum count value for each consecutive
epoch in the bout.

MAX COUNTS
~~~~~~~~~~

This option tells ActiLife the maximum count value for each consecutive
epoch in the bout.

DROP TIME
~~~~~~~~~

The drop time setting acts as a tolerance for bout detection and is best
explained through an example. Suppose the bout detection settings
(above) are set to Min Length = 10, Min Counts = 1953, and Max Counts =
50000. With the spike tolerance set to 0, the Bout tool will only
identify a bout of activity as 10 consecutive epochs of data with a
minimum activity count of 1953 and a maximum activity count of 50000.
Table 2 illustrates a valid bout while Table 3 illustrates an invalid
bout when Drop Time = 0. Because the value 1500 that occurs at 09:03 in
Table 3 is below the Minimum Count Level and because there is no
allowable tolerance, these epochs fail to register as a legitimate bout.
The epoch string in Table 3 would, however, qualify as a valid bout if
Drop Time were set to 1 or higher since the highlighted cell would
actually count as a valid bout epoch.  

.. raw:: html

   <table border="0">

.. raw:: html

   <thead>

.. raw:: html

   <tr>

.. raw:: html

   <th title="Field #1">

09:01:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #2">

09:02:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #3">

09:03:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #4">

09:04:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #5">

09:05:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #6">

09:06:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #7">

09:07:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #8">

09:08:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #9">

09:09:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #10">

09:10:00

.. raw:: html

   </th>

.. raw:: html

   </tr>

.. raw:: html

   </thead>

.. raw:: html

   <tbody>

.. raw:: html

   <tr>

.. raw:: html

   <td align="right">

2000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2100

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2500

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6124

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4510

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2164

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4518

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2540

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6000

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </tbody>

.. raw:: html

   </table>

TABLE 2 - EXAMPLE OF A VALID BOUT WITH DROP TIME = 0

.. raw:: html

   <table border="1">

.. raw:: html

   <thead>

.. raw:: html

   <tr>

.. raw:: html

   <th title="Field #1">

09:01:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #2">

09:02:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #3">

09:03:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #4">

09:04:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #5">

09:05:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #6">

09:06:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #7">

09:07:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #8">

09:08:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #9">

09:09:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #10">

09:10:00

.. raw:: html

   </th>

.. raw:: html

   </tr>

.. raw:: html

   </thead>

.. raw:: html

   <tbody>

.. raw:: html

   <tr>

.. raw:: html

   <td align="right">

2000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2100

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

1500

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6124

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4510

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2164

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4518

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2540

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6000

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </tbody>

.. raw:: html

   </table>

TABLE 3 - EXAMPLE OF AN INVALID BOUT WITH DROP TIME = 0

With a Drop Time = 2, the epoch string in Table 4 would be considered a
valid bout since there are exactly 2 epochs that are outside of the
min/max epoch levels (they count as valid epochs). If the epoch value at
06:10 were outside of the min/max range, that epoch would mark the end
of the bout (it would be 10 epochs long). The epoch string in Table 5
would not qualify as a valid bout under these conditions.

.. raw:: html

   <table border="1">

.. raw:: html

   <thead>

.. raw:: html

   <tr>

.. raw:: html

   <th title="Field #1">

06:00:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #2">

06:01:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #3">

06:02:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #4">

06:03:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #5">

06:04:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #6">

06:05:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #7">

06:06:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #8">

06:07:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #9">

06:08:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #10">

06:09:00

.. raw:: html

   </th>

.. raw:: html

   </tr>

.. raw:: html

   </thead>

.. raw:: html

   <tbody>

.. raw:: html

   <tr>

.. raw:: html

   <td align="right">

2000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2100

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2500

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

1274

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4510

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2164

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

862

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2540

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6000

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </tbody>

.. raw:: html

   </table>

TABLE 4 - EXAMPLE OF A VALID BOUT WITH DROP TIME = 2

.. raw:: html

   <table border="1">

.. raw:: html

   <thead>

.. raw:: html

   <tr>

.. raw:: html

   <th title="Field #1">

09:01:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #2">

09:02:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #3">

09:03:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #4">

09:04:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #5">

09:05:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #6">

09:06:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #7">

09:07:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #8">

09:08:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #9">

09:09:00

.. raw:: html

   </th>

.. raw:: html

   <th title="Field #10">

09:10:00

.. raw:: html

   </th>

.. raw:: html

   </tr>

.. raw:: html

   </thead>

.. raw:: html

   <tbody>

.. raw:: html

   <tr>

.. raw:: html

   <td align="right">

2000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2100

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

1500

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4000

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

1824

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

4510

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2164

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

1619

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

2540

.. raw:: html

   </td>

.. raw:: html

   <td align="right">

6000

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </tbody>

.. raw:: html

   </table>

TABLE 5 - EXAMPLE OF AN INVALID BOUT WITH DROP TIME = 2 Once a bout is
detected, the bout does not end until the drop time tolerance is
exceeded. Suppose the epoch string in Table 4 continued as follows:
06:10 – 4305; 06:11 – 3390; 06:12 – 5530; 06:13 – 9930; 06:14 – 100. The
epoch at 06:14 would mark the end of the bout which would be 14 minutes
long.

BOUT EXAMPLE
~~~~~~~~~~~~

-  Minimum Bout Length: 10 minutes
-  Minimum Count Level to be considered a Bout: 1953
-  Maximum Count Level to be considered a Bout: 5724
-  Tolerance/Drop Time (in minutes): 2
-  Dataset collected in one-minute epoch lengths
-  A string of epoch values from the dataset
-  1805, 2048, 3159, 4651, 4216, 4673, 5531, 1846, 2615, 2648, 3894,
   4869, 5201, 5756, 6165
-  This string contains one bout:
-  2048, 3159, 4651, 4216, 4673, 5531, 1846, 2615, 2648, 3894, 4869,
   5201
-  The value 1846 is considered the first “drop” time
-  The value 5756 is considered the second drop time
-  The value 6165 is considered the third and final drop time. ActiLife
   regresses the dataset once 6165 is detected to find the last “good”
   value. This defines the end of the dataset.

The “Use Vector Magnitude” option within the bout parameter settings
forces ActiLife to use the Vector Magnitude combination of all three
axes for each epoch when making bout level determinations. With this
option unchecked, ActiLife only uses Axis 1.

HEART RATE EE
-------------

The Heart Rate EE option calculates the following variables from any
datasets that are loaded in the Data Scoring tab.

**ADL Heart Rate**: Average Daily Living Heart Rate. This is the average
base (resting) heart rate of all ADL qualified epochs in the dataset. In
order to qualify as ADL heart rate, an epoch must contain heart rate
data below 79 beats per minute and one-minute activity data above 100
counts per epoch.

**Avg Active Heart Rate**: The average active heart rate in a given
dataset. In order to qualify as active heart rate, epoch activity must
exceed 1951 counts per minute epoch and heart rate must exceed 80 beats
per minute.

**HR Delta**: The difference between the Average Active Heart Rate and
the Average Daily Living Heart Rate for a given dataset

**Avg Active Caloric Expenditure**: The average minute-by-minute caloric
expenditure (kcal) for all epochs that match the “Active Heart Rate”
qualifier used to calculate Average Active Heart Rate. Calories are
calculated using the Freedson Equation (1997).

**Calibration Ratio**: Average Active Caloric Expenditure / HR Delta.
This value is used to determine calories-per-BPM, or calories that
should be associated with the subject’s BPM rate (Active Heart Rate)
when activity counts are not reliable.

The HREE algorithm should not be used as a standard for measuring
activity energy expenditure and is only an estimate of overall energy
expenditure when ambulatory movement is not reliable. For example, HREE
may be used when a user is riding a bicycle or lifting weights.

USE VALIDATED DATA IF AVAILABLE
-------------------------------

The “Use Validated Data if Available” checkbox option (shown in Figure
44) tells ActiLife whether to use only the wear time as calculated by
the Wear Time Validation tool (checked) or whether to use all epochs
within the file (unchecked) to perform the Data Scoring.

.. figure:: /assets/img/UseValidatedData.png
   :alt: 

FIGURE 44 - USE VALIDATED DATA IF AVAILABLE

DATA SCORING COLUMNS
--------------------

There are 75 columns of possible optional calculations that can be made
within the Data Scoring tool. Select the “Edit Columns” option to view
the selected columns and to enable/disable columns. Enabling more
columns will extend the time required for ActiLife to perform the
calculations and the batch data export (if used).

.. figure:: /assets/img/DataScoringColumns.png
   :alt: 

FIGURE 45 - DATA SCORING COLUMNS

The following parameters can be extracted from user datasets in the Data
Scoring tab.

1.   **Subject** - Name of the subject
2.   **Filename** - Filename of the subject
3.   **Epoch** - Epoch length in seconds
4.   **Weight** - The weight of the subject in lbs.
5.   **Age** - The age of the subject in years
6.   **Gender** - The gender of the subject
7.   **Date** - Date in local format
8.   **Hour** - Hour in local format
9.   **Day of Week** - Day of the week name in local format
10.  **Day of Week Num** - Day of the week number: 1=Monday, 2=Tuesday,
     etc.
11.  **kcals** - kcals during this hour
12.  **METs** - MET rate for a period of time
13.  **Bouts** - Number of Bouts starting in a period of time
14.  **Total Time in Bouts** - Time of bouts during a period of time
15.  **Avg Time per Bout** - Average length of time (in minutes) of
     bouts during a period of time
16.  **Total Counts in Bouts** - Total counts in bouts during a period
     of time
17.  **Bout Start** - The date and time of the start of a bout
18.  **Bout End** - The date and time of the end of a bout
19.  **Time in Bout** - The time of a bout in minutes
20.  **ADL Heart Rate** - Average Non-Sedentary HR between 41 and 79
21.  **Average Active Heart Rate** - Average HR during active activity
     (above light)
22.  **Heart Rate Delta** - The difference between Average Active Heart
     Rate and ADL Heart Rate
23.  **Average Active Caloric Expenditure** - Average amount of calories
     burned above light activity
24.  **Calibration Ratio** - Ratio of Average Active Caloric Expenditure
     divided by Heart Rate Delta
25.  **Light** - Length of time in Light in minutes
26.  **Moderate** - Length of time in Moderate in minutes
27.  **Vigorous** - Length of time in Vigorous in minutes
28.  **Very Vigorous** - Length of time in Very Vigorous in minutes
29.  **Axis 1 Counts Scored** - Sum of counts for Axis 1 (Y-Axis) during
     scored time
30.  **Axis 2 Counts Scored** - Sum of counts for Axis 2 (X-Axis) during
     scored time
31.  **Axis 3 Counts Scored** - Sum of counts for Axis 3 (Z-Axis) during
     scored time
32.  **Axis 1 Counts Non-Scored** - Sum of counts for Axis 1 (Y-Axis)
     during non-scored time
33.  **Axis 2 Counts Non-Scored** - Sum of counts for Axis 2 (X-Axis)
     during non-scored time
34.  **Axis 3 Counts Non-Scored** - Sum of counts for Axis 3 (Z-Axis)
     during non-scored time
35.  **Axis 1 Counts Total** - Sum of counts for Axis 1 (Y-Axis) during
     scored and non-scored time
36.  **Axis 2 Counts Total** - Sum of counts for Axis 2 (X-Axis) during
     scored and non-scored time
37.  **Axis 3 Counts Total** - Sum of counts for Axis 3 (Z-Axis) during
     scored and non-scored time
38.  **Axis 1 Average Counts Scored** - Average of counts for Axis 1
     (Y-Axis) during scored time
39.  **Axis 2 Average Counts Scored** - Average of counts for Axis 2
     (X-Axis) during scored time
40.  **Axis 3 Average Counts Scored** - Average of counts for Axis 3
     (Z-Axis) during scored time
41.  **Axis 1 Average Counts Non-Scored** - Average of counts for Axis 1
     (Y-Axis) during non-scored time
42.  **Axis 2 Average Counts Non-Scored** - Average of counts for Axis 2
     (X-Axis) during non-scored time
43.  **Axis 3 Average Counts Non-Scored** - Average of counts for Axis 3
     (Z-Axis) during non-scored time
44.  **Axis 1 Average Counts Total** - Average of counts for Axis 1
     (Y-Axis) during scored and non-scored time
45.  **Axis 2 Average Counts Total** - Average of counts for Axis 2
     (X-Axis) during scored and non-scored time
46.  **Axis 3 Average Counts Total** - Average of counts for Axis 3
     (Z-Axis) during scored and non-scored time
47.  **Axis 1 Max Counts Scored** - Maximum count value for Axis 1
     (Y-Axis) during scored time
48.  **Axis 2 Max Counts Scored** - Maximum count value for Axis 2
     (X-Axis) during scored time
49.  **Axis 3 Max Counts Scored** - Maximum count value for Axis 3
     (Z-Axis) during scored time
50.  **Axis 1 Max Counts Non-Scored** - Maximum count value for Axis 1
     (Y-Axis) during non-scored time
51.  **Axis 2 Max Counts Non-Scored** - Maximum count value for Axis 2
     (X-Axis) during non-scored time
52.  **Axis 3 Max Counts Non-Scored** - Maximum count value for Axis 3
     (Z-Axis) during non-scored time
53.  **Axis 1 Max Counts Total** - Maximum count value for Axis 1
     (Y-Axis) during scored and non-scored time
54.  **Axis 2 Max Counts Total** - Maximum count value for Axis 2
     (X-Axis) during scored and non-scored time
55.  **Axis 3 Max Counts Total** - Maximum count value for Axis 3
     (Z-Axis) during scored and non-scored time
56.  **Axis 1 CPM Scored** - Counts Per Minute for Axis 1 (Y-Axis)
     during scored time
57.  **Axis 2 CPM Scored** - Counts Per Minute for Axis 2 (X-Axis)
     during scored time
58.  **Axis 3 CPM Scored** - Counts Per Minute for Axis 3 (Z-Axis)
     during scored time
59.  **Axis 1 CPM Non-Scored** - Counts Per Minute for Axis 1 (Y-Axis)
     during non-scored time
60.  **Axis 2 CPM Non-Scored** - Counts Per Minute for Axis 2 (X-Axis)
     during non-scored time
61.  **Axis 3 CPM Non-Scored** - Counts Per Minute for Axis 3 (Z-Axis)
     during non-scored time
62.  **Axis 1 CPM Total** - Counts Per Minute for Axis 1 (Y-Axis) during
     scored and non-scored time
63.  **Axis 2 CPM Total** - Counts Per Minute for Axis 2 (X-Axis) during
     scored and non-scored time
64.  **Axis 3 CPM Total** - Counts Per Minute for Axis 3 (Z-Axis) during
     scored and non-scored time
65.  **Vector Magnitude Counts Scored** - Vector Magnitude of all 3 Axis
     during scored time
66.  **Vector Magnitude Counts Non-Scored** - Vector Magnitude of all 3
     Axis during non-scored time
67.  **Vector Magnitude Counts Total** - Vector Magnitude of all 3 Axis
     during scored and non-scored time
68.  **Vector Magnitude Average Counts Scored** - Average Vector
     Magnitude of all 3 Axis during scored time
69.  **Vector Magnitude Average Counts Non-Scored** - Average Vector
     Magnitude of all 3 Axis during non-scored time
70.  **Vector Magnitude Average Counts Total** - Average Vector
     Magnitude of all 3 Axis during scored and non-scored time
71.  **Vector Magnitude Max Counts Scored** - Maximum Vector Magnitude
     of all 3 Axis during scored time
72.  **Vector Magnitude Max Counts Non-Scored** - Maximum Vector
     Magnitude of all 3 Axis during non-scored time
73.  **Vector Magnitude Max Counts Total** - Maximum Vector Magnitude of
     all 3 Axis during scored and non-scored time
74.  **Vector Magnitude CPM Scored** - Vector Magnitude Counts Per
     Minute during scored time
75.  **Vector Magnitude CPM Non-Scored** - Vector Magnitude Counts Per
     Minute during non-scored time
76.  **Vector Magnitude CPM Total** - Vector Magnitude Counts Per Minute
     during scored and non-scored time
77.  **Steps Counts Scored** - Sum of Step Counts during scored time
78.  **Steps Counts Non-Scored** - Sum of Step Counts during non-scored
     time
79.  **Steps Counts Total** - Sum of Step Counts during scored and
     non-scored time
80.  **Steps Average Counts Scored** - Average Step Counts during scored
     time
81.  **Steps Average Counts Non-Scored** - Average Step Counts during
     non-scored time
82.  **Steps Average Counts Total** - Average Step Counts during scored
     and non-scored time
83.  **Steps Max Counts Scored** - Maximum Step Counts during scored
     time
84.  **Steps Max Counts Non-Scored** - Maximum Step Counts during
     non-scored time
85.  **Steps Max Counts Total** - Maximum Step Counts during scored and
     non-scored time
86.  **Steps Per Minute Scored** - Steps Per Minute during scored time
87.  **Steps Per Minute Non-Scored** - Steps Per Minute during
     non-scored time
88.  **Steps Per Minute Total** - Steps Per Minute during scored and
     non-scored time
89.  **Lux Average Counts Scored** - Average Lux Value during scored
     time
90.  **Lux Average Counts Non-Scored** - Average Lux Value during
     non-scored time
91.  **Lux Average Counts Total** - Average Lux Value during scored and
     non-scored time
92.  **Lux Max Counts Scored** - Maximum Lux Value during scored time
93.  **Lux Max Counts Non-Scored** - Maximum Lux Value during non-scored
     time
94.  **Lux Max Counts Total** - Maximum Lux Value during scored and
     non-scored time
95.  **Number of Epochs Scored** - Number of epochs during scored time
96.  **Number of Epochs Non-Scored** - Number of epochs during
     non-scored time
97.  **Number of Epochs Total** - Number of epochs during scored and
     non-scored time
98.  **Time Scored** - Length of scored time
99.  **Time Non-Scored** - Length of non-scored time
100. **Time Total** - Length of scored and non-scored time
101. **Calendar Days Scored** - Number of Calendar Days during scored
     time
102. **Calendar Days Non-Scored** - Number of Calendar Days during
     non-scored time
103. **Calendar Days Total** - Number of Calendar Days during scored and
     non-scored time
104. **Wear Time Start** - The start of a wear time
105. **Wear Time End** - The end of a wear time

BATCH EXPORTING
---------------

Results from the Data Scoring tool can be batch exported to a Microsoft
Excel ® spreadsheet. The resulting export will contain a full list of
all subjects with corresponding Data Scoring results broken down by
hours, days, and Summary. Bout details and Wear Time Validation can also
be exported along with a separate sheet showing which algorithms were
used to produce the results and a “Definitions” sheet which defines all
of the exported parameters.

To begin the export, click the “Export” button after performing a
calculation in the Data Scoring tab. Check the “Create Batch View…”
option as shown in Figure 46. Select any of the desired export options
and click “Export…”

.. figure:: /assets/img/DataScoringExportOptions.png
   :alt: 

FIGURE 46 - DATA SCORING EXPORT OPTIONS

Depending on the number of variables and files, the export process could
take anywhere from 10 seconds to 2 hours.
