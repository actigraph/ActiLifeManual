Sleep Analysis Tab
==================

--------------

Sleep analysis can be performed on any dataset to determine sleep
efficiency and other sleep statistics that may indicate sleep problems.
Any combinations of the various initialization modes are allowed for a
given dataset file (activity, dual-axis, steps and heart rate). ActiLife
will attempt to re-integrate data collected at epoch intervals less than
60 seconds as all scoring is performed using 60 second epoch cycles.

To begin scoring a dataset, click the “Select Dataset” option from the
top of the Sleep Scoring tool and browse to an .agd file that contains
data collected during sleep episodes. Graphs of each day in the dataset
will appear in the “Sleep Scoring” view.

.. figure:: /assets/img/SleepScoring.png
   :alt: 

FIGURE 47 – SLEEP SCORING

Areas on the graphs can be magnified by dragging the mouse pointer over
the area of interest as shown in Figure 48. To return to the normal
view, click the small circle in the bottom left-hand corner of the
graph.

|image0| |image1|

FIGURE 48 – GRAPHING

MANUALLY ENTERING SLEEP TIMES
-----------------------------

Sleep times (time in or out of bed) can be manually entered into the
Sleep Analysis tool using two different techniques. To key-in sleep
times, select the “Add Bed Time” button on the right of the Sleep
Scoring tool. Enter the subject’s exact time in bed and time out of bed
and click “ok.” The selected time slot will be highlighted in
translucent red on the graph.

Sleep times can also be added directly on the graph itself by clicking
anywhere on the graph and using the arrow keys to navigate to the sleep
episode start time. Once a suitable start time is located, right-click
anywhere on the graph and choose “Add New In Bed Time Here” This will
mark the start of the sleep episode. Repeat this process and choose
“Accept Out Of Bed Time” to mark the end of the sleep episode. Figure 49
illustrates this process.

|image2| |image3|

FIGURE 49 – MARKING SLEEP EPISODES GRAPHICALLY

AUTOMATICALLY ENTERING SLEEP TIMES
----------------------------------

ActiSleep+ users can automatically estimate bed times (Time in Bed [TOB]
and Time Out of Bed [TOB]) in ActiLife by pressing the “Auto Score”
button. ActiLife will estimate bed times for the current data set and
apply the selected algorithm to those bed times.

.. figure:: /assets/img/AutoSleepScore.png
   :alt: 

FIGURE 50 - AUTO SCORE SLEEP TIMES

The Auto Score feature will not ignore non-wear times (as estimated by
the Wear Time Validation tool), but the algorithm is designed to ignore
gaps in the sleep data as shown in Figure 51.

.. figure:: /assets/img/AutoSleepScoreIgnored.png
   :alt: 

FIGURE 51 - AUTO SCORE IGNORES PERIODS WHEN DEVICE WAS REMOVED

EDITING AUTO SCORED TIMES
-------------------------

The bed times estimated by the Auto Score feature can be easily adjusted
by right-clicking on the sleep period of interest, choosing “Adjust Out
Bed Time” (or “Adjust In Bed Time”), using the left or right arrow keys
on the keyboard to adjust the time, then right-clicking anywhere on the
graph and selecting “Finished Entering Bed Times”. This is illustrated
in Figure 52.

.. figure:: /assets/img/AdjustingBedTimes.png
   :alt: 

FIGURE 52 - ADJUSTING BED TIMES

    Important: The Auto Score can only be used with data collected from
    ActiSleep+ devices. The feature can be enabled for data collected
    from other ActiGraph devices for a small fee. Contact
    support@theactigraph.com for more information.

REMOVING SLEEP TIMES
--------------------

Sleep periods can be removed by right-clicking on them on the graph and
choosing “Delete Current Sleep Period.” To delete all of the sleep
periods for a particular day or for the entire dataset, choose the
proper corresponding option (“Delete All Sleep Periods in this Day” or
“Delete All Sleep Periods for the Dataset”). Sleep periods can also be
removed by selecting the sleep period in the list to the right and
clicking the “Remove” button below the list.

ACTIVITY AND LUX SCALE
----------------------

The “Activity Scale” and “Lux Scale” settings below the sleep graphs
adjust the maximum scale shown for Activity and Lux counts on the sleep
graphs. Changing the value scales all of the graphs simultaneously.

CHANGING GRAPH COLORS
---------------------

Graph colors for activity, lux, the sleep score period, and the score
indicator can be changed easily by clicking the color palette beside the
corresponding item and choosing a different color as shown in Figure 53.
Note that the “Period Color” is translucent and may appear slightly
lighter than its selected color.

.. figure:: /assets/img/ColorPallete.png
   :alt: 

FIGURE 53 – COLOR PALETTE FOR SLEEP SCORING GRAPH

LUX
---

Lux, or ambient light, is measured by ActiGraph’s ActiSleep+ monitor,
the ActiTrainer and the GT3X+ devices. Ambient light may affect subject
sleeping habits and thus is a useful tool in analyzing circadian rhythms
and sleeping patterns. If lux data was recorded by the ActiGraph device,
it will appear in yellow on the sleep graphs as shown below in Figure
54. The lux data can be hidden by deselecting the “Show LUX data” option
at the bottom of the screen. Details regarding the significance of the
lux values are revealed by hovering the mouse pointer over the “Lux
Info” link at the bottom of the screen as shown in Figure 55. Note that
these levels are only estimates and are not meant for exact
interpretation of the light detected by the device.

.. figure:: /assets/img/SleepLuxOverlay.png
   :alt: 

FIGURE 54 – LUX DATA OVERLAY ON SLEEP GRAPHS

.. figure:: /assets/img/LuxThresholds.png
   :alt: 

FIGURE 55 – LUX THRESHOLDS

SLEEP SCORING ALGORITHMS
------------------------

The Sleep Analysis tool comes standard with two validated algorithms
(Sadeh or Cole-Kripke ) to determine minute-by-minute asleep/awake
status. These algorithms are selectable by the user and can be changed
instantly for comparison purposes. The algorithms are described below.
Select the desired algorithm by choosing it from the “Algorithm”
drop-down menu at the top right-hand corner of the Sleep Analysis tool.
More information is available about the origin of the algorithms by
clicking “Sleep Algorithm Information” link below the algorithm dropdown
menu.   ### COLE-KRIPKE ALGORITHM ###

The Cole-Kripke algorithm is considered appropriate for use with adult
populations because it was developed using subjects ranging from 35 to
65 years of age. Roger J. Cole and Daniel F. Kripke adapted a scoring
method developed by J. B. Webster with an experimental wrist actigraph
for the AMI actigraph in 1992. It was developed using 10, 30 and 60
epochs, with the highest level of accuracy resulting from data collected
at 10 second epoch periods.

The algorithm was adapted to the ActiGraph ActiSleep monitor by
performing a side by side test using the AMI device and the ActiSleep
monitor worn together. The data were scaled then put through the
algorithms until the ActiSleep monitor sleep score matched that from the
AMI device.

SADEH ALGORITHM SUMMARY
~~~~~~~~~~~~~~~~~~~~~~~

The Sadeh algorithm was developed by Dr. Avi Sadeh from Tel-Aviv
University in Israel and is considered appropriate for younger
populations because it was developed using subjects ranging from 10 to
25 years of age. He used the same device that Cole-Kripke used to
develop their algorithm, and ActiGraph therefore adapted it in the same
way by scaling our data until it matched up with the scoring results of
the AMI device. In general terms, this algorithm determines a subject’s
sleep state by examining the ActiGraph activity over an 11 minute
sliding window. For any given window, a “Sleep Score” (whether the
person is asleep or not) can be determined by applying this formula.
After selecting a sleep time (Time In Bed (TIB) and Time Out of Bed
(TOB)) each minute of sleep data is analyzed this way.

CUSTOM SLEEP ALGORITHMS
~~~~~~~~~~~~~~~~~~~~~~~

ActiSleep+ customers can create their own custom sleep scoring algorithm
that uses the same “sliding window” concept as the Sadeh and Cole-Kripke
algorithms. To get started, choose “Create New” from the Algorithm
dropdown menu.

.. figure:: /assets/img/CustomSleepAlgorithm.png
   :alt: 

FIGURE 56 - CUSTOM SLEEP ALGORITHM

*The Custom Sleep Scoring Parameters* form shown in will load.

.. figure:: /assets/img/CustomSleepAlgorithmForm.png
   :alt: 

FIGURE 57 - CUSTOM SLEEP SCORING DESIGN FORM

This tool will allow users to customize the following settings.

ALGORITHM NAME
~~~~~~~~~~~~~~

The Algorithm Name is the name that will appear in the drop-down menu
after the algorithm design is complete.

EPOCH WINDOW
~~~~~~~~~~~~

The sliding window technique works as follows: All epochs in a given
dataset are scanned. Each epoch of data receives a sleep or a wake score
based on its count level as well as the count levels of other epochs
before and after itself. This “window” of epochs and surrounding epochs
then “slides” to the next epoch (and surrounding epochs) and the process
repeats.

The Epoch Window defines the sliding window and the weighting which is
given to the current and surrounding epochs in order to determine
whether to score the current epoch as sleep or wake. To increase the
size of the window, adjust the “Epochs to use before current” and
“Epochs to use after current” options; the graphic will increase or
decrease in width automatically.

.. figure:: /assets/img/CustomSleepAlgorithmWindow.png
   :alt: 

FIGURE 58 - CUSTOM SLEEP SCORE EPOCH WINDOW

Adjust the numbers below the surrounding epochs to change the weighting.
Change the Wake Threshold in the Count Parameters section to adjust the
comparison level. The Sleep/Wake formula at the bottom of the Custom
Sleep Algorithm tool shows the formula used to determine whether the
current epoch (epoch-0) is scored as wake or sleep. In the formula show
in Figure 59, the current epoch will be scored as wake if the formula is
greater than or equal to 10.

.. figure:: /assets/img/CustomSleepAlgorithmFormula.png
   :alt: 

FIGURE 59 - SLEEP/WAKE FORMULA

COUNT PARAMETERS
~~~~~~~~~~~~~~~~

*Wake Threshold* – This is the value which the sliding window is
compared to in order to determine sleep or wake status for epoch-0

*Data to Use*: Users have the option of using Axis 1, Axis 2, or Axis 3
data to calculate the custom sleep score. Alternatively, the Vector
Magnitude (VM) of all 3 axes can be used.

*Set Maximum Value of Count* – Use this option to put a limit on the
maximum weight a particular epoch can have on the sleep/wake formula.
For instance, if (epoch-2)\*0.05 = 500 (see Figure 59), setting the
Maximum Value of Count to 300 would actually limit that epoch’s
contribution to 300 (rather than 500).

*Epoch Length Required* – This option allows users to specify a required
epoch length for datasets using the new customized formula. Datasets
that do not meet this requirement cannot be used – ActiLife will
automatically attempt to reintegrate lesser epoch sized datasets up to
the required epoch length.

PORTABILITY OF THE CUSTOM SLEEP ALGORITHM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once the custom algorithm has been written, it can be shared with other
ActiLife users. Simply run the custom algorithm against an *.agd dataset
to produce the Sleep Score Information for that dataset. That *.agd will
then contain the custom sleep score algorithm. Whenever the \*.agd file
is shared with other users, this algorithm will automatically appear in
their algorithm dropdown menu in the Sleep Analysis tool.

    Important: The Custom Sleep Algorithm tool can only be used with
    data collected from ActiSleep+ devices. The feature can be enabled
    for data collected from other ActiGraph devices for a small fee.
    Contact support@theactigraph.com for more information.

SLEEP SCORE INFORMATION
-----------------------

Both algorithms will yield the following information within ActiLife’s
Sleep Scoring tool for each sleep period. Sleep period scores can be
seen by clicking on the sleep period of interest on the right-hand side
of the screen (see Figure 47 for an illustration).

**Sleep Onset** - The first minute that the algorithm scores “asleep.”

**Total Sleep Time (TST)** – The total number of minutes scored as
“asleep.”

**Wake after Sleep Onset (WASO)** – The total amount of time a subject
is awake during a sleep period, minus the sleep latency.

**Awakenings** - The number of different awakening episodes as scored by
the algorithm. This is sometimes referred to as Frequency of Awakenings
(shown as the number of awakenings per night).

**Avg Awakening** – The average length, in minutes, of all awakening
episodes.

**Total Counts** – The total actigraphy counts summed together for the
entire sleep period.

**Efficiency** – Number of sleep minutes divided by the total number of
minutes the subject was in bed (i.e., the difference between the In-Bed
and Out Bed time).

ACTOGRAM VIEW
-------------

The ActoGram view option provides ActiSleep + users with the ability to
quickly discern circadian patterns in sleep behavior by scaling and
compressing the sleep graphs. Enable the ActoGram view by choosing the
radio button corresponding to this view at the bottom of the Sleep
Scoring tool. Figure 60 illustrates an ActoGram view.

Several options exist for editing the ActoGram view.

**Show 6 Hour Ticks** – This option will toggle the periodic 6 hour hash
marks on the ActoGram graph.

**Show Hourly Ticks** – This option will toggle the periodic hourly hash
marks on the ActoGram graph.

**Graphs Per Page** – Use this option to compress or expand the ActoGram
view vertically.

**Lux** – This check box toggles the ambient light data on the ActoGram
view (in yellow)

.. figure:: /assets/img/Actogram.png
   :alt: 

FIGURE 60 – ACTOGRAM VIEW

SAVING THE ACTOGRAM
~~~~~~~~~~~~~~~~~~~

The ActoGram can be saved as a sharable image by clicking “Save
ActoGram” at the bottom of the graph. This option will give the user the
option to export the ActoGram to a .jpg image for sharing.

    Important: The ActoGram view can only be used with data collected
    from ActiSleep+ devices. The feature can be enabled for data
    collected from other ActiGraph devices for a small fee. Contact
    support@theactigraph.com for more information.

SHOW SLEEP EPOCHS
-----------------

Clicking the “Show Sleep Epochs” button will load a matrix of each epoch
in the dataset with details about whether the epoch was scored as a
“Sleep Epoch” (indicated by an “S”) or a “Wake Epoch” (indicated by a
“W”). This list can be exported to CSV by clicking “Save” at the bottom
of the form or by copying and pasting the values. In addition, the
entire list can be copied to the clipboard by clicking the corresponding
button – the list can then be pasted into any text editor.

SAVE SLEEP REPORT
~~~~~~~~~~~~~~~~~

Sleep scores produced in the Sleep Scoring tab can be exported to either
a CSV or PDF file by clicking the “Save Sleep Report” option at the
bottom right-hand side of the screen. Select the desired output from the
options dialog that appears. Browse to the export location, type a file
name, and click “Save” to begin the export.

.. figure:: /assets/img/SleepReport.png
   :alt: 

FIGURE 61 – SAVE SLEEP REPORT DIALOG

.. |image0| image:: /assets/img/GraphingPreZoom.png
.. |image1| image:: /assets/img/GraphingPostZoom.png
.. |image2| image:: /assets/img/MarkingSleepPeriodsGraphically1.png
.. |image3| image:: /assets/img/MarkingSleepPeriodsGraphically2.png
