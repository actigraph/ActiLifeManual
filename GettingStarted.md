# GETTING STARTED #


## DOWNLOADING AND INSTALLING ##
Download ActiLife 6 from [http://www.theactigraph.com/actilife](http://www.theactigraph.com/actilife "ActiLife") to a known location.  Double-click the icon to start the installer.  After running the ActiLife6 installer, follow the installation instructions in the on-screen prompts.  

![](/assets/img/ActiLifeSetupIcon.png)
ACTILIFE6 SETUP ICON

> IMPORTANT: Please be sure to remove any ActiGraph devices that you have connected to your computer during installation.  Failure to do so could result in a faulty installation of your ActiLife software.
> 
> NOTE: Older versions of ActiLife (4 and 5) will be removed whenever ActiLife 6 is installed

After installing ActiLife, an icon similar to the one shown here will appear on your desktop.  Double click the icon to start ActiLife 6.

![](/assets/img/ActiLifeDesktopShortcut.png) 
FIGURE 2 – ACTILIFE 6 PROGRAM DESKTOP SHORTCUT

## LICENSING ##
ActiLife software is a licensed program and requires users to obtain a product key before the software can be activated.  If you have not purchased an ActiLife license, you may do so by visiting the ActiGraph store at [www.theactigraph.com/store](www.theactigraph.com/store).  If you have misplaced your product key, contact ActiGraph sales support at [support@theactigraph.com](support@theactigraph.com) in order to proceed.   Once ActiLife 6 has been purchased or upgraded from a previous version, users are entitled to free updates for 12 months.  After that period, an optional maintenance plan may be purchased.  **It is highly recommended that users purchase the maintenance plan in order to guarantee access to the newest updates, features, and bug fixes.**
 
## ACTIVATION OVER THE INTERNET ##
The first time the program is launched, users will be presented with a screen similar to that shown in Figure 3.  If you have already received a product key for your ActiLife Pro or ActiLife Lite software, type that product key in the box provided.  If the license formatting is correct, a green check mark will appear to the right of the license box.  Click “Activate”.  ActiLife will connect to ActiGraph’s license server to confirm that the product key is correct and that it has indeed been purchased or upgraded.  After activation, a screen similar to the one shown in Figure 4 will be displayed.  This screen summarizes the product type and the number of activations used and available, as well as the name and contact information of the person to whom the license is registered.  **Name, Email, and Organization fields must be populated in order to continue**.  This activation process is required for each computer on which ActiLife is running.

![](/assets/img/Activation.png) 

FIGURE 3 – ACTILIFE ACTIVATION SCREEN
 
![](/assets/img/RegistrationConfirmation.png) 

FIGURE 4 – ACTILIFE REGISTRATION CONFIRMATION

## ACTIVATION WITHOUT AN INTERNET CONNECTION ##
For users without an internet connection, ActiLife can be activated by contacting our technical support staff either via email ([support@theactigraph.com](support@theactigraph.com)) or by phone (1-877-497-6996 option 1).  Similar to the Internet activation, enter the ActiLife product key in the first box that appears after launching the program.  After clicking “Continue,” a screen similar to Figure 5 will appear.  Provide the 24-character product key to ActiGraph customer service representative.  After validating the product key, the representative will provide a confirmation code.  Type or copy/paste the confirmation code into the box provided.  Click ‘Next’ to activate ActiLife.

![](/assets/img/OfflineActivation.png) 

FIGURE 5 – NON-INTERNET ACTIVATION

## ACTILIFE NEW FEATURE OVERVIEW ##
Each release (update) of ActiLife provides users with a new feature overview.  This screen (or similar) will appear immediately after loading ActiLife 6 for the first time.  Note that this screen will change with each release to quickly illustrate the new features.

![](/assets/img/WelcomeScreen.png) 

FIGURE 6 – ACTILIFE WELCOME SCREEN

To view this welcome screen again at any time, select the ‘Help’ tab in the menu bar and then select ‘ActiLife Tour’ as shown in Figure 7.

![](/assets/img/RunWelcomeTour.png) 
 
FIGURE 7 – RUN TOUR FROM HELP MENU

## ACTILIFE DEFAULT UNITS SELECTION ##
On first load, ActiLife gives users the option to choose which default units of measurement, time display format, and download directory they wish to use (see Figure 8).  These settings can be changed at any time from the Options menu.

![](/assets/img/DefaultUnits.png) 
 
FIGURE 8 - DEFAULT UNITS SETTINGS ON FIRST LOAD

## ACTILIFE DATA FORMATS ##
ActiLife stores and uses data from native *.agd files which are produced during the download or export process for all devices.  These files are in SQLite Format, which is essentially a small database.  ActiLife can import data from any legacy file formats by selecting “File->Import/Export” and selecting the appropriate action from the menu (see the ActiLife Main Menu discussion section in this manual).  Multiple files can be imported simultaneously.

# ACTILIFE MAIN MENU #

## FILE MENU ##
The file menu in ActiLife contains options related to file manipulation, AGD file analysis, and template loading and editing.

![](/assets/img/FileMenu.png)

FIGURE 9 – ACTILIFE FILE MENU

## IMPORT/EXPORT ##
As discussed previously, users can import and export file formats to various formats to meet nearly any need.  For details about the various file formats, see details in [Appendix A – File Types in ActiLife6](/appendix/AppendixA.md "Appendix A").  The table below explains the Import/Export options that are shown in Figure 10.


<table>
  <tr>
    <th>Import/Export Option</th>
    <th>Explanation</th>
  </tr>
  <tr>
    <td>Epoch to Epoch</td>
    <td>
		• Imported files in this category contain epoch level data (e.g., 1s, 5s, 10s, 30s, 60s epochs).<br>
		• Exported files also contain epoch level data in the new file format.<br>
		• CSV->AGD conversion will convert both regular CSV files and Data Table CSV files.<br>
		• Use these options to simply switch file types (file extensions).
	</td>
  </tr>
  <tr>
    <td>Raw to Epoch</td>
    <td>
		• Imported files in this category contain raw, 30Hz data or contain binary compressed data (*.gt3x format).  Note: 12Hz import files are not allowed.  See Uncompressing *.gt3x Files for details.<br>
		• *.DAT files are file types used in ActiLife version 4.<br>
		• Exported files in this category contain epoch level data (e.g., 1s, 5s, 10s, 30s, 60s epochs).<br>
		• Exported files are first filtered then accumulated.<br>
		• Supported export file formats include .CSV, .AGD, .DAT<br>
	</td>
  </tr>
  <tr>
    <td>Raw to Raw</td>
    <td>
		• Used to export binary*.gt3x files directly to *.csv format<br>
		• Both import and export file formats contain raw data at whatever frequency was used to produce the *.gt3x file<br>
	</td>
  </tr>
  <tr>
    <td>Re-Integrate</td>
    <td>
		• This feature is used to reintegrate epoch level post-filtered/post-accumulated *.agd files into larger epoch “buckets.”  <br>
		• E.g., reintegrating a 10s epoch file into a 60s epoch file.<br>
		• Files cannot be reintegrated into smaller epoch lengths (e.g., 15s -> 10s)<br>
	</td>
  </tr>
</table>

![](/assets/img/ImportExportMenu.png)

FIGURE 10 – ACTILIFE IMPORT/EXPORT MENU OPTION

## CONVERTING TO A DATA TABLE VS. STANDARD .CSV ##
A data table *.csv file contains separate columns with corresponding headers for each data type collected by the device and also includes the Vector Magnitude sum of each axis if data is collected for all three axes.  A standard *.csv file produced during conversion simply exports the data into *.csv format.  Column headers are not included unless that option is by checking “Add Column Headers to CSV” in the options menu.

## MATLAB EXPORT OPTION ##
Users can export native *.AGD files to *.MAT format for easy importing into MathWorks Matlab® mathematical software platform.

## RE-INTEGRATING ##
The “Re-Integrate AGD File” option allows users to integrate AGD files to larger epoch periods (e.g., 1 second epoch data collection reintegrated to 60 second epoch periods for Sleep Analysis or Data Scoring).  After selecting the file to be reintegrated, selected the desired epoch length as shown and click “OK.”  The new file will be saved in the same directory as the existing file with an appended file name indicating the new epoch length.

![](/assets/img/Reintegrate.png)

FIGURE 11 – RE-INTEGRATION OPTION


## AGD FILE VIEWER ##
The AGD File Viewer can be accessed from the File menu, by clicking “finished downloading” from the Devices grid after a download, or by double-clicking on an *.agd file from within Windows Explorer.

Using the AGD viewer, users can instantly view the data they’ve just downloaded.  With ActiLife 6.1 and later, the AGD viewer provides a graphical summary view of both activity cut points (according to the stored cut points in ActiLife) or daily activity counts which allow users to make quick observations about the subject’s compliance level (see Figure 12Figure 12). 

![](/assets/img/AgdViewer.png)
 
FIGURE 12 - AGD FILE VIEWER (SHOWING CUT POINTS OR DAILY COUNTS)

Click “Edit” near the “Subject Biometric Information” section to edit the stored biometric variables associated with the *.agd file.   Click “Save” to instantly update the file with these changes.
 
![](/assets/img/AgdViewerEdit.png)

FIGURE 13 - EDIT SUBJECT BIOMETRICS FROM AGD VIEWER

Clicking “Show Data” in the AGD viewer will display hour-long previews of the data in a grid format.  The hourly view can be changed by clicking the desired date/hour or by clicking “Next Hour->” to proceed sequentially through the hourly view.  Data can be copied from the grid by selecting the data and pressing “Ctrl+C.”  Data can then be pasted by pressing “Ctrl+V” in MS Excel® or any text editor.

Data can be exported to any format directly from the AGD file viewer by clicking on “Export Data To...” above the data graph.  This is equivalent to selecting “Export” from the File menu.
 
![](/assets/img/AgdViewerEpochs.png)

FIGURE 14 – AGD FILE VIEWER

## LOAD TEMPLATE ##
The ‘Load Template’ option allows users to browse and locate an ActiLife template file (*.agt) which forces ActiLife to pre-defined initialization and/or download parameters to ensure consistency among all sites.  For details on using the template editor, see Building and Using a Template.  Once a template is loaded, details about the template including the template name and ‘last modified’ date will appear in the upper right-hand corner of the ActiLife tool as shown in Figure 15.
 
![](/assets/img/TemplateInUse.png)

FIGURE 15 – TEMPLATE-IN-USE INFORMATION

## REMOVE TEMPLATE ##
The ‘Remove Template’ option simply disables any active template that ActiLife is using.  The current template information as shown in Figure 15 will disappear after using this option.  For more information about the template feature, see Building and Using a Template.

## TEMPLATE EDITOR ##
The template editor loads the template editor form which can be used to create new or modify existing templates for use with all versions of ActiLife.  For more information, see Building and Using a Template.

> Note. The template editor is not available in ActiLife LITE.

## EDIT MENU ##

![](/assets/img/EditMenu.png) 

FIGURE 16 – EDIT MENU

The “Copy” and “Select All” options in the Edit menu allow users to select and copy elements in the selected grid so that they may be pasted into a text or spreadsheet editor.  These apply to any tab within ActiLife.  The “Options…” menu item allows ActiLife users to set system options that control how ActiLife functions. To change any option, make the change then click ‘Apply’ in the Options panel.  Click ‘OK’ to close the panel.

# GENERAL OPTIONS #

## UPDATE OPTIONS ##
Checking “Check for Program Updates” enables ActiLife’s auto-update feature and allows ActiLife to check for program updates via the Internet when the program starts up.  If an Internet connection is unavailable, ActiLife automatically skips this step.  
> Important: It is strongly recommended that this option remain checked.  Doing so ensures that the user has the latest version of ActiLife.  Older versions of ActiLife may have bugs or issues which could affect data collection and/or device interaction.  ActiGraph makes every effort to ensure that data collection and download are unaffected during program updates

Each time a device is initialized, ActiLife checks the firmware version on the device.  If it is not the latest version available from ActiGraph, it is automatically loaded onto the device prior to re-initialization.  Because all data on a device is deleted prior to flashing firmware, firmware updates are only performed just prior to re-initialization during which time the device is fully erased.  The “Update Firmware on Initialization” option allows the user to disable this feature.  However, in order to guarantee that all devices remain up to date, this feature is permanently checked and enabled and cannot be unchecked.  In order to disable this feature, contact ActiGraph support at support@theactigraph.com.  

It should be noted that ActiLife automatically downloads the latest version of firmware (for all ActiGraph devices) each time the program loads.  In this way, ActiLife makes every effort to keep users updated with the latest firmware for their devices.  The latest firmware files can be found in the C:\Users\<user name>\Documents\ActiGraph\ActiLife\FirmwareFiles directory.  
ActiLife ships with the latest versions of firmware available in an effort to ensure that our offline customers remain updated.

## UNITS OF MEASUREMENT ##
Use these options to select the desired units of measurement throughout the ActiLife software (in all grids and in all exports).  If “English” is selected, users have the option to display subject height information in inches or Ft/Inches.

## TIMESPAN DISPLAY ##
The Timespan Display settings set the default view for the ‘Current Data Recorded’ display in the Devices grid.  Selecting the default (Days Hours Minutes Seconds) breaks the display of time parameters in ActiLife’s grids into four parts (days, hours, minutes, and seconds).  Checking “Show text for ‘D’ ‘H’ ‘M’ and/or ‘S’” annotates the time with letters corresponding to hours, minutes or seconds (e.g., 820m versus 820 – useful for copy/pasting into a text or spreadsheet editor that may not use the h/m/s notation).

## DIRECTORIES ##
Use this option to set the default directories for data downloads, firmware storage, and CSV file creation

# DOWNLOADING #
## DOWNLOAD NAMING CONVENTION ##
These options set the default naming convention for downloaded files.  During the download process, users have the option to change this option.

# CREATE FILE OPTIONS #

## CREATE DAT AND CSV WITH AGD DOWNLOAD ##
Use these options to create a *.dat or *.csv file at the time of download.  Important: These options only work whenever an AGD file is created.  Hence, when downloading a GT3X+ device, *.dat and *.csv files will not be created when these options are checked unless the “Create AGD File” is checked during the download process (see Downloading GT3X+ Devices for details on creating an AGD file on download).

## ADD COLUMN HEADERS TO CSV ##
Checking this option will add column header labels to the columns in CSV (like “Axis 1,” “Axis 2,”, “Axis 3,” “Steps,” etc.) files when those files are created via export.

## COMPRESS GT3X+ FILES ##
This option will apply maximum file compression to *.gt3x files when they are downloaded from GT3X+ devices.  This compression can greatly reduce the file size of the *.gt3x zip files, but can double the post-processing time (i.e., the time it takes to create an *.agd file from a *.gt3x file).  For details on post-processing, see Uncompressing *.gt3x Files.

## CREATE SUB-FOLDERS WHEN EXPORTING "RAW TO EPOCH" ##
Check this option to create sub-folders for *.agd, *.dat, and/or *.csv files created when exporting from “Raw to Epoch” files from the Import/Export menu.

## CREATE AGD DURING DOWNLOAD OF GT3X+ OR ACTISLEEP+ ##
When checked, this option tells ActiLife to automatically create an *.agd file immediately after downloading *.gt3x files from ActiSleep+, GT3X+ or wGT3X+ devices.  For more information on these file types, see Appendix A – File Types in ActiLife.

## SCAN OF GT3X+ DOWNLOADS ##
When downloading GT3X+, ActiSleep+, or wGT3X+ data, this option allows users to be notified of large gaps (null data or 0s) in the data which may indicate either a problem with the device itself or non-compliance with the device end-user.  Setting this option to a certain percentage will prompt the user if there are more than that percentage of the data contains 0s.  For example, setting to 10% will cause notifications to appear when 10% or more of the data on the device contains null data (0s).  Set this option to 100% to disable notifications.

## WEAR TIME VALIDATION ##
Wear Time Validation options are used to set the default values for the dataset filters in the Wear Time Validation tool.  The user also has the option to switch between the Floating Window or Daily Wear Time Validation algorithms.  

> Note: The daily algorithm has been deprecated and should be avoided.

## DATA SCORING ##
The Data Scoring options are used to set default values for the algorithms available in the Data Scoring tool in ActiLife.  Whenever the Data Scoring tab is opened, the default values set in this options dialog will be used; however, they can be changed directly from within the Data Scoring tool.

Note that clicking the “?” icons to the right of each algorithm option will open the ActiGraph support website and reveal the origin of each of the algorithms.  Reference abstracts are available from the support site.

## BOUTS – USE VECTOR MAGNITUDE ##
When this option is checked, the vector magnitude of 3-axis devices will be used to calculate bout levels.

## SLEEP SCORING ##
The Sleep Scoring option allows the user to set the default Sleep Scoring Formula for the Sleep Scoring Tool.  See Sleep Scoring Algorithms for more information.

Checking the “Create Clinical Report on Download” will cause ActiLife to automatically create a clinical PDF report immediately after download.  See Clinical Report for details.

## COLORS ##
The Colors option allows the user to set the default colors for all graphing items in ActiLife.  The “Multiple Colors” checkbox in the Progress Bar section will cause ActiLife to use multi-colored progress bars in the Devices tab when interacting with multiple devices.

# COMMUNICATION MENU #

![](/assets/img/CommunicationMenu.png) 

FIGURE 17 – COMMUNICATION MENU

## SHOW DOWNLOAD FOLDER ##
The Show Download Folder simply opens ActiLife’s default download folder.  This option is useful for locating files downloaded from devices in the Devices tab.

## SHOW CSV FOLDER ##
The Show CSV Folder opens the default CSV conversion/download folder

## UPDATE FIRMWARE FROM FILE ##
Within the “Advanced” menu, the Update Firmware from File option allows users to manually upgrade (or downgrade) device firmware.  From the Devices tab, select the devices that need to be upgraded then select the Update Firmware from File option.  A dialog box will allow the user to select a firmware file for each of the connected devices types.  After the file has been selected, click “OK to update the firmware.

> Important: Manually upgrading or downgrading firmware is not recommended.  Doing so could render your ActiGraph device unusable and could void the product’s warranty.  Contact ActiGraph support prior to manually changing the firmware.  Under normal circumstances, ActiLife will automatically update the devices firmware.

# TOOLS MENU #

![](/assets/img/ToolsMenu.png) 

FIGURE 18 - TOOLS MENU

The Tools menu contains options for printing a sleep diary, creating a clinical report, correlating GPS data with data from ActiGraph devices and merging multiple AGD files together.

## PRINT SLEEP DIARY ##
Many times, it is useful to provide patients with a sleep log for making subjective logs of time-in-bed (TIB) and time-out-of-bed (TOB) times so that sleep analyses can be properly performed.  The “Print Sleep Diary” option in the Tools menu allows users to export a printable sleep diary for patients to use while they are wearing a device.  Click the option and select a location to store the log diary (PDF format).  A screenshot of the log diary is shown in Figure 19.

![](/assets/img/SleepLog.png)

FIGURE 19 - SLEEP LOG (DIARY)

## CLINICAL REPORT ##
ActiLife can create a clinical report which contains the following information:
- Subject and Device Information (Name, Weight, Device Serial Number, Start/End Time)
- Wear Time Information
- Energy Expenditure
- Cut Points
- Sleep Graphs
- Sleep Period Breakdown and Summary

The clinical report can be used to quickly generate a report on an individual in a clinical environment without running through all of the tools in ActiLife.
 
## GENERATING A CLINICAL REPORT ##
When downloading data from an ActiSleep or ActiSleep+ device, users can generate a Clinical Report by simply checking the box “Create Clinical Report on Download…” as shown in Figure 20.  

![](/assets/img/ClinicalReportOnDownload.png)

FIGURE 20 - CLINICAL REPORT ON DOWNLOAD

The report can also be generated after a data download through the tools menu.  Select the *.agd file that was generated from an ActiSleep or ActiSleep+ device and click “Open”.

## CLINICAL REPORT DEFAULT VALUES ##

The Clinical Report generator uses the default values stored in the Wear Time Validation tool to calculate wear and non-wear time.  Similarly, the tool also uses the default algorithms selected in Data Scoring (on last program close) to calculate Energy Expenditure.  To change the algorithms, open ActiLife, navigate to the Data Scoring tab, switch to a new energy expenditure algorithm and close the program.  If sleep times have already been entered via the Sleep Analysis tool, the Clinical Report tool will use those times to calculate the sleep score and graph information in the report.  If not, the Auto Score feature will be utilized.

> Note: The Clinical Report tool is only available for data collected using the ActiSleep or ActiSleep+ devices.  This feature can be enabled for non-ActiSleep devices for a small fee.  Contact ActiGraph support at support@theactigraph.com for more information.

## CORRELATE GPS DATA ##
More info coming soon.

## MERGE AGD ##
More info coming soon.

## HELP MENU ##

![](/assets/img/HelpMenu.png)

FIGURE 21 - HELP MENU

## ONLINE SUPPORT ##
Click this option to access our online support system

## VIEW WELCOME TOUR ##
This option launches the ActiLife introduction dialog that outlines what’s new in the current release.

## ACTIVATION DETAILS ##
Click this option to view the ActiLife product key, the edition type, and the maintenance expiration date.

## DEACTIVATE ##
ActiLife licenses are node locked to the machine on which the software is installed.  Users are allotted a specific number of activations on various machines.  In order to prevent losing an activation, ActiLife should be deactivated before it is uninstalled and removed from its host computer.  To deactivate ActiLife and reclaim the activation, select the Deactivate option and click “Deactivate ActiLife.”

![](/assets/img/Deactivate.png)

FIGURE 22 - DEACTIVATE DIALOG

## CHECK FOR UPDATES ##
Clicking this option will force ActiLife to check for any maintenance updates.  This action is done automatically each time ActiLife is loaded, but may be manually done via this method.

## ABOUT ACTILIFE ##
The About ActiLife option displays information about the ActiLife program including the software version number (also available in the main dialog frame), copyright information, and a link to ActiGraph’s corporate website.
