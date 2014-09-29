==================
ActiLife Menu Items
==================

File Menu
---------

The file menu in ActiLife contains options related to file manipulation,
AGD file analysis, and template loading and editing.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/FileMenu.png
   :alt: 

Import/Export
-------------

As discussed previously, users can import and export file formats to 
various formats to meet nearly any need. For details about the various
file formats, see details in Appendix A – File Types in
ActiLife6. The table below explains the Import/Export
options that are shown in Figure 10.

* Epoch to Epoch
	- Imported files in this category contain epoch level data (e.g., 1s, 5s, 10s, 30s, 60s epochs).
	- Exported files also contain epoch level data in the new file format.
	- CSV->AGD conversion will convert both regular CSV files and Data Table CSV files.
	- Use these options to simply switch file types (file extensions).
* Raw to Epoch
	- Imported files in this category contain raw, 30Hz data or contain binary compressed data (*.gt3x format).  Note, 12Hz import files are not allowed.  See Uncompressing *.gt3x Files for details.
	- *.DAT files are file types used in ActiLife version 4.
	- Exported files in this category contain epoch level data (e.g., 1s, 5s, 10s, 30s, 60s epochs).
	- Exported files are first filtered then accumulated
	- Supported export file formats include .CSV, .AGD, .DAT
* Raw to Raw
	- Used to export binary*.gt3x files directly to *.csv format
	- Both import and export file formats contain raw data at whatever frequency was used to produce the *.gt3x file
* Re-Integrate
	- This feature is used to reintegrate epoch level post-filtered/post-accumulated *.agd files into larger epoch “buckets.”  
	- E.g., reintegrating a 10s epoch file into a 60s epoch file.
	- Files cannot be reintegrated into smaller epoch lengths (e.g., 15s -> 10s)

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/ImportExportMenu.png
   :alt: 

Figure 10 – ActiLife Import and Export Menu

Converting to a Data Table vs. Standard .CSV
--------------------------------------------

A data table *.csv file contains separate columns with corresponding
headers for each data type collected by the device and also includes the
Vector Magnitude sum of each axis if data is collected for all three
axes. A standard *.csv file produced during conversion simply exports
the data into \*.csv format. Column headers are not included unless that
option is by checking “Add Column Headers to CSV” in the options menu.

Matlab® Export Option
--------------------

Users can export native *.AGD files to *.MAT format for easy importing
into MathWorks Matlab® mathematical software platform.

Re-Integrating
--------------

The “Re-Integrate AGD File” option allows users to integrate AGD files
to larger epoch periods (e.g., 1 second epoch data collection
reintegrated to 60 second epoch periods for Sleep Analysis or Data
Scoring). After selecting the file to be reintegrated, selected the
desired epoch length as shown and click “OK.” The new file will be saved
in the same directory as the existing file with an appended file name
indicating the new epoch length.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/Reintegrate.png
   :alt: 

Figure 11 – Re-Integration Option

AGD File Viewer
---------------

The AGD File Viewer can be accessed from the File menu, by clicking
“finished downloading” from the Devices grid after a download, or by
double-clicking on an \*.agd file from within Windows Explorer.

Using the AGD viewer, users can instantly view the data they’ve just
downloaded. With ActiLife 6.1 and later, the AGD viewer provides a
graphical summary view of both activity cut points (according to the
stored cut points in ActiLife) or daily activity counts which allow
users to make quick observations about the subject’s compliance level
(see Figure 12Figure 12).

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/AgdViewer.png
   :alt: 

Figure 12 - AGD File Viewer

Click “Edit” near the “Subject Biometric Information” section to edit
the stored biometric variables associated with the \*.agd file. Click
“Save” to instantly update the file with these changes.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/AgdViewerEdit.png
   :alt: 

Figure 13 - Edit Subject Bio Data in AGD Viewer

Clicking “Show Data” in the AGD viewer will display hour-long previews
of the data in a grid format. The hourly view can be changed by clicking
the desired date/hour or by clicking “Next Hour->” to proceed
sequentially through the hourly view. Data can be copied from the grid
by selecting the data and pressing “Ctrl+C.” Data can then be pasted by
pressing “Ctrl+V” in MS Excel® or any text editor.

Data can be exported to any format directly from the AGD file viewer by
clicking on “Export Data To...” above the data graph. This is equivalent
to selecting “Export” from the File menu.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/AgdViewerEpochs.png
   :alt: 

Figure 14 – Agd File Viewer Epochs

Load Template
-------------

The ‘Load Template’ option allows users to browse and locate an ActiLife
template file (\*.agt) which forces ActiLife to pre-defined
initialization and/or download parameters to ensure consistency among
all sites. For details on using the template editor, see Building and
Using a Template. Once a template is loaded, details about the template
including the template name and ‘last modified’ date will appear in the
upper right-hand corner of the ActiLife tool as shown in Figure 15.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/TemplateInUse.png
   :alt: 

Figure 15 – Template in Use Information

Remove Template
---------------

The ‘Remove Template’ option simply disables any active template that
ActiLife is using. The current template information as shown in Figure
15 will disappear after using this option. For more information about
the template feature, see Building and Using a Template.

Template Editor
---------------

The template editor loads the template editor form which can be used to
create new or modify existing templates for use with all versions of
ActiLife. For more information, see Building and Using a Template.

	.. note:: The template editor is not available in ActiLife LITE.

Edit Menu
---------

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/EditMenu.png
   :alt: 

Figure 16 – Edit Menu

The “Copy” and “Select All” options in the Edit menu allow users to
select and copy elements in the selected grid so that they may be pasted
into a text or spreadsheet editor. These apply to any tab within
ActiLife. The “Options…” menu item allows ActiLife users to set system
options that control how ActiLife functions. To change any option, make
the change then click ‘Apply’ in the Options panel. Click ‘OK’ to close
the panel.

General Options
===============

Update Options
--------------

| Checking “Check for Program Updates” enables ActiLife’s auto-update
feature and allows ActiLife to check for program updates via the
Internet when the program starts up. If an Internet connection is
unavailable, ActiLife automatically skips this step.
| > Important: It is strongly recommended that this option remain
checked. Doing so ensures that the user has the latest version of
ActiLife. Older versions of ActiLife may have bugs or issues which could
affect data collection and/or device interaction. ActiGraph makes every
effort to ensure that data collection and download are unaffected during
program updates

Each time a device is initialized, ActiLife checks the firmware version
on the device. If it is not the latest version available from ActiGraph,
it is automatically loaded onto the device prior to re-initialization.
Because all data on a device is deleted prior to flashing firmware,
firmware updates are only performed just prior to re-initialization
during which time the device is fully erased. The “Update Firmware on
Initialization” option allows the user to disable this feature. However,
in order to guarantee that all devices remain up to date, this feature
is permanently checked and enabled and cannot be unchecked. In order to
disable this feature, contact ActiGraph support at
support@theactigraph.com.

	.. note:: It should be noted that ActiLife automatically downloads the latest
version of firmware (for all ActiGraph devices) each time the program
loads. In this way, ActiLife makes every effort to keep users updated
with the latest firmware for their devices. The latest firmware files
can be found in the C:<user name>directory.

	.. note:: ActiLife ships with the latest versions of firmware available in an
effort to ensure that our offline customers remain updated.

Units of Measurement
--------------------

Use these options to select the desired units of measurement throughout
the ActiLife software (in all grids and in all exports). If “English” is
selected, users have the option to display subject height information in
inches or Ft/Inches.

Timespan Display
----------------

The Timespan Display settings set the default view for the ‘Current Data
Recorded’ display in the Devices grid. Selecting the default (Days Hours
Minutes Seconds) breaks the display of time parameters in ActiLife’s
grids into four parts (days, hours, minutes, and seconds). Checking
“Show text for ‘D’ ‘H’ ‘M’ and/or ‘S’” annotates the time with letters
corresponding to hours, minutes or seconds (e.g., 820m versus 820 –
useful for copy/pasting into a text or spreadsheet editor that may not
use the h/m/s notation).

Directories
-----------

Use this option to set the default directories for data downloads,
firmware storage, and CSV file creation

Downloading
===========

Download Naming Convention
--------------------------

These options set the default naming convention for downloaded files.
During the download process, users have the option to change this
option.

Create File Options
===================

Create DAT and CSV with AGD Download
------------------------------------

Use these options to create a *.dat or *.csv file at the time of
download. Important: These options only work whenever an AGD file is
created. Hence, when downloading a GT3X+ device, *.dat and *.csv files
will not be created when these options are checked unless the “Create
AGD File” is checked during the download process (see Downloading GT3X+
Devices for details on creating an AGD file on download).

Add Column Headers to CSV
-------------------------

Checking this option will add column header labels to the columns in CSV
(like “Axis 1,” “Axis 2,”, “Axis 3,” “Steps,” etc.) files when those
files are created via export.

Compress GT3X Files
--------------------

This option will apply maximum file compression to *.gt3x files when
they are downloaded from GT3X+ devices. This compression can greatly
reduce the file size of the *.gt3x zip files, but can double the
post-processing time (i.e., the time it takes to create an *.agd file
from a *.gt3x file). For details on post-processing, see Uncompressing
\*.gt3x Files.

Create Sub-Folders When Exporting "Raw to Epoch"
------------------------------------------------

Check this option to create sub-folders for *.agd, *.dat, and/or \*.csv
files created when exporting from “Raw to Epoch” files from the
Import/Export menu.

Create AGD During Download of GT3X+ or ActiSleep+
-------------------------------------------------

When checked, this option tells ActiLife to automatically create an
*.agd file immediately after downloading *.gt3x files from ActiSleep+,
GT3X+ or wGT3X+ devices. For more information on these file types, see
Appendix A – File Types in ActiLife.

Scan of GT3X File
-----------------------

When downloading GT3X+, ActiSleep+, or wGT3X+ data, this option allows
users to be notified of large gaps (null data or 0s) in the data which
may indicate either a problem with the device itself or non-compliance
with the device end-user. Setting this option to a certain percentage
will prompt the user if there are more than that percentage of the data
contains 0s. For example, setting to 10% will cause notifications to
appear when 10% or more of the data on the device contains null data
(0s). Set this option to 100% to disable notifications.

Wear Time Validation
--------------------

Wear Time Validation options are used to set the default values for the
dataset filters in the Wear Time Validation tool. The user also has the
option to switch between the Floating Window or Daily Wear Time
Validation algorithms.

	.. note:: The daily algorithm has been deprecated and should be avoided.

Data Scoring
------------

The Data Scoring options are used to set default values for the
algorithms available in the Data Scoring tool in ActiLife. Whenever the
Data Scoring tab is opened, the default values set in this options
dialog will be used; however, they can be changed directly from within
the Data Scoring tool.

Note that clicking the “?” icons to the right of each algorithm option
will open the ActiGraph support website and reveal the origin of each of
the algorithms. Reference abstracts are available from the support site.

Bouts - Use Vector Magnitude
----------------------------

When this option is checked, the vector magnitude of 3-axis devices will
be used to calculate bout levels.

Sleep Scoring
-------------

The Sleep Scoring option allows the user to set the default Sleep
Scoring Formula for the Sleep Scoring Tool. See Sleep Scoring Algorithms
for more information.

Checking the “Create Clinical Report on Download” will cause ActiLife to
automatically create a clinical PDF report immediately after download.
See Clinical Report for details.

Colors
------

The Colors option allows the user to set the default colors for all
graphing items in ActiLife. The “Multiple Colors” checkbox in the
Progress Bar section will cause ActiLife to use multi-colored progress
bars in the Devices tab when interacting with multiple devices.

Communication Menu
==================

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/CommunicationMenu.png
   :alt: 

Figure 17 – Communication Menu

Show Download Folder
--------------------

The Show Download Folder simply opens ActiLife’s default download
folder. This option is useful for locating files downloaded from devices
in the Devices tab.

Show CSV Folder
---------------

The Show CSV Folder opens the default CSV conversion/download folder

Update Firmware From File
-------------------------

Within the “Advanced” menu, the Update Firmware from File option allows
users to manually upgrade (or downgrade) device firmware. From the
Devices tab, select the devices that need to be upgraded then select the
Update Firmware from File option. A dialog box will allow the user to
select a firmware file for each of the connected devices types. After
the file has been selected, click “OK to update the firmware.

	.. note:: Manually upgrading or downgrading firmware is not
    recommended. Doing so could render your ActiGraph device unusable
    and could void the product’s warranty. Contact ActiGraph support
    prior to manually changing the firmware. Under normal circumstances,
    ActiLife will automatically update the devices firmware.

Tools Menu
==========

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/ToolsMenu.png
   :alt: 

Figure 18 - Tools Menu

The Tools menu contains options for printing a sleep diary, creating a
clinical report, correlating GPS data with data from ActiGraph devices
and merging multiple AGD files together.

Print Sleep Diary
-----------------

Many times, it is useful to provide patients with a sleep log for making
subjective logs of time-in-bed (TIB) and time-out-of-bed (TOB) times so
that sleep analyses can be properly performed. The “Print Sleep Diary”
option in the Tools menu allows users to export a printable sleep diary
for patients to use while they are wearing a device. Click the option
and select a location to store the log diary (PDF format). A screenshot
of the log diary is shown in Figure 19.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/SleepLog.png
   :alt: 

Figure 19 - Sleep Log (Diary)

Clinical Report
---------------

ActiLife can create a clinical report which contains the following
information: - Subject and Device Information (Name, Weight, Device
Serial Number, Start/End Time) - Wear Time Information - Energy
Expenditure - Cut Points - Sleep Graphs - Sleep Period Breakdown and
Summary

The clinical report can be used to quickly generate a report on an
individual in a clinical environment without running through all of the
tools in ActiLife.   ## GENERATING A CLINICAL REPORT ## When downloading
data from an ActiSleep or ActiSleep+ device, users can generate a
Clinical Report by simply checking the box “Create Clinical Report on
Download…” as shown in Figure 20.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/ClinicalReportOnDownload.png
   :alt: 

Figure 20 - Clinical Report on Download

The report can also be generated after a data download through the tools
menu. Select the \*.agd file that was generated from an ActiSleep or
ActiSleep+ device and click “Open”.

Clinical Report Default Values
------------------------------

The Clinical Report generator uses the default values stored in the Wear
Time Validation tool to calculate wear and non-wear time. Similarly, the
tool also uses the default algorithms selected in Data Scoring (on last
program close) to calculate Energy Expenditure. To change the
algorithms, open ActiLife, navigate to the Data Scoring tab, switch to a
new energy expenditure algorithm and close the program. If sleep times
have already been entered via the Sleep Analysis tool, the Clinical
Report tool will use those times to calculate the sleep score and graph
information in the report. If not, the Auto Score feature will be
utilized.

	.. note:: The Clinical Report tool is only available for data collected
    using the ActiSleep or ActiSleep+ devices. This feature can be
    enabled for non-ActiSleep devices for a small fee. Contact ActiGraph
    support at support@theactigraph.com for more information.

Correlate GPS Data
------------------

More info coming soon.

Merge AGD
---------

More info coming soon.

Help Menu
---------

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/HelpMenu.png
   :alt: 

Figure 21 - Help Menu

Online Support
--------------

Click this option to access our online support system

View Welcome Tour
-----------------

This option launches the ActiLife introduction dialog that outlines
what’s new in the current release.

Activation Details
------------------

Click this option to view the ActiLife product key, the edition type,
and the maintenance expiration date.

Deactivate
----------

ActiLife licenses are node locked to the machine on which the software
is installed. Users are allotted a specific number of activations on
various machines. In order to prevent losing an activation, ActiLife
should be deactivated before it is uninstalled and removed from its host
computer. To deactivate ActiLife and reclaim the activation, select the
Deactivate option and click “Deactivate ActiLife.”

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/Deactivate.png
   :alt: 

Figure 22 - Deactivate Dialog

Check For Updates
-----------------

Clicking this option will force ActiLife to check for any maintenance
updates. This action is done automatically each time ActiLife is loaded,
but may be manually done via this method.

About ActiLife
--------------

The About ActiLife option displays information about the ActiLife
program including the software version number (also available in the
main dialog frame), copyright information, and a link to ActiGraph’s
corporate website.
