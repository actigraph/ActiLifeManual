Periodic Leg Movement (PLM) Analysis Tab
========================================

--------------

The Periodic Leg Movement (PLM) tool allows users to detect and score
periodic leg movements in patients with PLM disorder or restless leg
syndrome. Note: The PLM tool is only compatible with data collected from
the legacy ActiSleep or the new ActiSleep+ monitor devices. This
analysis serves as a cost effective alternative to polysomnography (PSG)
analysis.

    Note: ActiGraph is working with leading sleep institutions to obtain
    research-backed validation on the PLM Analysis tool. However, at
    this time, the PLM analysis uses existing research to make estimates
    on the presence of PLM in patients.

INITIALIZING DEVICES FOR PLM ANALYSIS
-------------------------------------

To use the tool, initialize an ActiSleep monitor through the devices tab
to start collecting data at the desired time. (Info about ActiSleep
battery life) ActiSleep+ devices only have one option for initialization
(30Hz). Legacy ActiSleep devices should be initialized to collect data
at 1s epochs. During initialization, ActiLife gives users the option to
print a sleep diary. The sleep diary can be used by patients who choose
to wear the devices for several nights in their own homes or for doctors
who are logging multiple patients' sleep behaviors. Patients should be
instructed to use the sleep diary to keep track of the time in bed (TIB)
and time out of bed (TOB) for purposes of analysis.

Attach the ActiSleep monitor to the top interior of the patient’s left
and right feet around the ball of the foot as shown in the image below.
This can be accomplished with bandage wrapping or with straps available
from ActiGraph. Patients should wear the device during the entire
duration of their total time in bed.

.. figure:: /img/PlmWearLocation.png
   :alt: 

FIGURE 62 - WEAR LOCATION FOR PLM ANALYSIS

DOWNLOADING DEVICES
-------------------

After patients have worn the devices for the desired number of sleep
periods, collect the devices and download them using the Devices tab.
Legacy ActiSleep monitors will produce an *.agd file on download. This
file can be used for scoring PLM in the PLM tab. ActiSleep+ devices will
create a *.gt3x file on download. This file contains the raw
acceleration data collected by the devices and needs to be
post-processed (i.e., converted to \*.agd format) prior to PLM scoring.
This can be accomplished by choosing “Create AGD File” from the download
dialog as shown in the figure below. Select 1s epoch and 3 axes. The
other options are optional, but “Low Frequency Extension” should not be
selected.

.. figure:: /img/PlmDownloadSettings.png
   :alt: 

FIGURE 63 - DOWNLOAD SETTINGS FOR PLM ANALYSIS

After download, an AGD file will be created in the download folder which
is also selected at the time of download.

SCORING THE PLM DATA
--------------------

To score periodic leg movements, open the PLM tab and select the left
and right leg *.agd files. Click the “Add Sleep Periods” button and
select the entry method. * Add Period Using Bed Times – Use this option
to manually enter in times as recorded by the doctor or patient on the
sleep diary. \* Import from Separate AGD File – Use this option to
import sleep times from another AGD file that already contains the same
sleep times. \* Enter Period Graphically – Coming soon.

Select which axis or axes to use to score the PLM data. The Vector
Magnitude option combines all three axes using the vector magnitude
formula. See Appendix B – Vector Magnitude for more information.

Select the thresholds for detecting legitimate “movement”.

    Note: these thresholds only set the level at which PLM activity
    occurs. ActiLife’s built-in algorithm determines whether or not the
    movement qualifies as PLM.

-  Onset Threshold – The threshold (in counts-per-epoch) at which PLM
   movement detection starts
-  Decay Threshold – The threshold (in counts-per-epoch) at which PLM
   movement detection ends.

Onset and decay thresholds are available to introduce hysteresis into
the movement detection.

INTERPRETING THE PERIODIC LIMB MOVEMENT OUTPUT
----------------------------------------------

After scoring files for Periodic Leg Movement, click on the different
sleep periods to view the graph and PLM stats for each sleep period.

GRAPHS
~~~~~~

Clicking on a sleep period will load a PLM score graph. The green
background represents the total time in bed (sleep period) as logged by
the user. The graph will automatically show data 1 hour before the time
in bed and 1 hour after the time out of bed. The blue horizontal line
represents the onset threshold and the red horizontal line represents
the decay threshold. The bar graph below the main activity graph gives
users a quick reference to PLM bouts (bouts of activity that meet the
qualifications of Periodic Leg Movement). Both graphs can be zoomed in
or out simultaneously by dragging the mouse over the area of interest.
To zoom back out, click the small circle in the lower left-hand corner
of the graph until the desired zoom level is achieved.

STATS
~~~~~

-  PLMI (per hour) - PLMI stands for Periodic Leg Movement Indices. This
   value represents the number of qualifying periodic leg movements per
   hour, averaged over the entire sleep period.
-  Minutes of PLM Kicks - The total number of minutes of "kicks" or
   activity spikes that exceed the onset threshold AND the total minutes
   of consecutive "kicks" thereafter that exceed the decay threshold.
-  Number of PLM Kicks - The number of "kicks" or activity spikes that
   exceed the onset threshold AND the number of consecutive "kicks" that
   exceed the decay threshold.
-  Number of PLM Bouts - A count of the number of bouts of PLM that
   occurred during the selected sleep period.
-  Average PLM Bout Length (min) - The average length, in minutes, of
   all of the PLM bouts for the selected sleep period.
-  Minutes of PLM Bouts - The total time, in minutes, of PLM bouts. This
   time is different from the PLM kicks because kicks do not necessarily
   qualify as valid PLM.
-  Avg PLMS Intensity - The average intensity of the PLM during Sleep of
   all of the PLM bouts. Essentially, this is the duty cycle of all PLM
   bouts. Avg PLMS Intensity = total minutes of valid PLM / total PLM
   bout length

For more information regarding the source of our PLM calculations, see
our online FAQ, "How were the Periodic Leg Movement algorithms
derived?".
