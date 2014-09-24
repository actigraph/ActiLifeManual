# DEVICE INITIALIZATION AND DOWNLOAD #

Once ActiLife is properly installed and licensed, users will be presented with the “Devices” screen similar to the one shown in Figure 23.  ActiLife is capable of initializing or downloading multiple devices simultaneously.  Devices can be connected either before or after ActiLife is launched. 

![](/assets/img/OpeningScreen.png)

FIGURE 23 – OPENING SCREEN
 
> Important: Attempting to communicate with multiple GT1M and GT3X devices has been known to be problematic.  Users may see an error similar to the one shown…  To remedy the problem, ensure that the USB hub in use is a powered hub (ActiGraph recommends the 7-port ConnectLand sold on the theactigraph.com store).  Sometimes a retry will fix the issue, but not always.  Read more about the problem on our FAQ page [here](https://help.theactigraph.com/forums/20630327-actilife6-software).

As shown in Figure 24, device status information will appear in the “Devices” tab as devices are connected to the computer. Device status information is provided in the Devices grid.

![](/assets/img/DeviceTool.png)

FIGURE 24 - ACTILIFE DEVICES TOOL

### DEVICE ###
The “Device” column describes the type of ActiGraph device(s) connected to the PC.  Mixing devices is allowed.

### SERIAL # ###
The “Serial #” column displays the serial number of the device connected.

### STATUS ###
The “Status” column displays the current status of the attached device.  The status could be “Ready,” “Idle,” “Initializing,” “Finished Initializing,” “Updating,” “Downloading,” “Finished Downloading,” or “Finished Creating Clinical Report.”

### PROGRESS ###
The “Progress” column contains the progress bar indicating the progress toward completion of the status indicated in the “Status” column.

### FIRMWARE ###
The “Firmware” column displays the current firmware version on the device.  Firmware is automatically updated during initialization.  See Update Options for more details.

### BATTERY VOLTAGE ###
This column displays the device battery voltage and charge percentage.  For more information, see device owners manual.

### TOTAL MEMORY ###
The Total Memory column displays the total memory available on the device.  MB = Megabyte (or 1048576 bytes).

### CURRENT DATA RECORDED ###
This column displays the current number of days, hours, minutes, and seconds of recorded data on the device.  To adjust how this appears, see Timespan Display.

### EPOCH/SAMPLE RATE ###
For non-GT3X+ devices, this column represents the accumulation epoch length.  For GT3X+ devices and non-GT3X+ devices in raw data collection mode, this column represents the sample/store rate.

### SUBJECT NAME ###
This column displays the subject name currently stored on the device.

### START DATE & TIME ###
This column displays the start date and time programmed on the device.

### STOP DATE & TIME ###
This column displays the stop date and time programmed on the device.  This option can be set during initialization and is used to align the file lengths for multiple devices during large longitudinal studies.

### FILTER ###
The “Filter” column displays the on-board accelerometer filter setting for initialized devices (Normal or Low-Frequency-Extension).  See Setting Device Parameters for details.  This column is not applicable for GT3X+ devices as no on-board filtering is performed.

### AXIS ENABLED ###
The “Axis Enabled” column indicates which axes are being sampled and stored.  1 –vertical axis only (Axis 1); 2 – vertical and horizontal (Axes 1 and 2); 3 – vertical, horizontal, and lateral (Axes 1, 2, and 3).

### MODES ###
The “Modes” column displays icons representing the data channels that the device is set to log (if initialized).  The icons and their meanings are interpreted in Table 1.

<table>
  <tr>
    <th>Mode/Channel Icon</th>
    <th>Interpretation</th>
  </tr>
  <tr>
    <td><img src=assets/img/LedIcon.png></a></td>
    <td>
		Flash LED Mode Enabled (LED flashes periodically to indicate device is active).  See Recharging and LED Decoding for more details.
	</td>
  </tr>
  <tr>
    <td><img src=assets/img/StepIcon.png></a></td>
    <td>
		Step counting enabled. Indicates that the device is recording step counts per epoch.  See Steps for more details.
	</td>
  </tr>
  <tr>
    <td><img src=assets/img/InclinometerIcon.png></a></td>
    <td>
		Flash LED Mode Enabled (LED flashes periodically to indicate device is active).  See Recharging and LED Decoding for more details.
	</td>
  </tr>
  <tr>
    <td><img src=assets/img/LuxIcon.png></a></td>
    <td>
		Flash LED Mode Enabled (LED flashes periodically to indicate device is active).  See Recharging and LED Decoding for more details.
	</td>
  </tr>
</table>
TABLE 1 – MODE/CHANNEL ICON DEFINITIONS

### MORE INFO ###
The button in the “More Info” column is for debug purposes by ActiGraph support and should not be required to operate the device(s).

The data in the Devices grid can be copied and pasted into any text editor by clicking on a cell, pressing and holding the Shift key and clicking on another cell to select a group of cells then pressing “Ctrl+C” to copy the data to the PC clipboard.  This can be useful for studies in which device data must be logged.

> IMPORTANT: Device drivers must load the first time a device is connected to a USB port.  Devices may take a few seconds to load during device driver enumeration.  GT3X+ and ActiSleep+ devices may cause Windows to display the AutoRun prompt (asking the user to choose a default action upon opening.  The ActiGraph software development team is working on eliminating this action.

## INITIALIZING DEVICES ##
Select a check box corresponding to the devices to be initialized (or select all devices”) and click “Initialize.”  A dialog similar to Figure 25 will appear.

![](/assets/img/InitDialog.png)

FIGURE 25 - INITIALIZATION DIALOG FOR GT3X+ VS GT3X

### SETTING DEVICE PARAMETERS ###
The ‘Initialize Device(s)’ screen contains a separate tab for each type of ActiGraph device connected to the PC and appears after clicking the “Initialize” button at the top of the “Devices” screen.  Tabs across the top represent the types of devices to be initialized.  If multiple devices of each type are selected, the tab group applies to all devices of that type.

Select the tab for the type of device you wish to configure and set the specific data collection parameters.  Filter information can also be set at the time of initialization.  For more details about the low frequency extension, see Low Frequency Extension.  All ActiGraph devices of the same type that are initialized simultaneously will be initialized with the same data collection parameters.

Start Date and Time and Stop Date and Time apply to all devices and cannot be unique for each device group.  Stop time is optional.

The “Max Recording Time” for each device is shown in the Initialization screen.  This number will change depending upon the number of axes selected, the epoch length, and the number of active channels (see Available Channels (Modes) for details of the meaning of each setting).  Most devices’ “Max Recording Time” will far exceed the battery life of the device.

The icon in the top right corner of the initialization screen indicates which axes are selected.  As the “# of Axis” dropdown box is increased, so too are the number of logged axes.  
GT3X+ devices collect data from all channels regardless of initialization settings.  The only settings available for the GT3X+ are the raw Sample Rate and the “Flash LED” options as shown in Figure 25.

After data collection parameters have been set up for each model, select the ‘Enter Subject Info…’ button.

### SUBJECT INFO ###

The Subject Name screen allows users to enter a unique subject name for the attached devices.  This data will be stored on the device and will be available at download and can help with file naming when data is downloaded from the device.  To add or change a name, highlight the subject name cell.  Note that GT3X+ devices (devices with serial numbers beginning with ‘NEO’) will store more information.

![](/assets/img/SubjectName.png)
 
FIGURE 26 – SUBJECT NAME ENTRY FORM

If desired, the “Use Serial Number” button will populate the Subject Name column with the serial number of the device.  Similarly, the “Use Device Info” button will automatically populate the Subject Name column with the Subject Name currently stored on the device.  The “Clear” button will erase the fields for easier editing.

> Important: If any devices have a voltage less than 4.1 volts, we recommend leaving them connected, allowing them to charge fully if time allows. Updated voltage can be viewed by selecting the ‘Refresh All’ tab (or F5) from the devices screen.

### GT3X+ BIOMETRIC INFO STORAGE ###

GT3X+ Devices (NEOxxxxxxxxxx) can **optionally** store extra biometric information during initialization which can be used for post-processing after downloading data from the device (see Figure 26 for details).  GT3X+ devices can store the following information in addition to the “Subject Name” which is standard on all devices:
* Gender – Male or Female
* Height – Subject height in inches or ft. /inches depending upon the settings.
* Weight – Subject weight in lbs. or kg, depending upon the settings.
* Date of Birth – Subject’s date of birth (mm/dd/yyyy)
* Race – Subject race: Asian/Pacific Islander, Black/African American, White/Caucasian, Latino/Hispanic, Other
* Limb – The limb on which the device is worn: Wrist, Waist, Ankle, Upper Arm
* Side – The side of the body that the patient is wearing the device.  Left or Right
* Dominance – Dominant or Non-Dominant.  This allows the researcher to store whether or not the wear location is on the subject’s dominant or non-dominant side.

This data is stored in the info.txt file as part of the *.gt3x zip file when data is downloaded from the GT3X+ device.

When all names have been entered, select the ‘Initialize All’ button and the progress is displayed in the ‘Status’ column (refer to Figure 24).  When the initialization is complete, the devices are ready to be removed. 

## DOWNLOADING DEVICES ##

### FILE FORMAT ###
Downloading data from the actigraph device is a simple process.  It is important to understand how the data on the device is formatted and what is contained in the file.  Except for GT3X+ devices, ActiLife stores data from the devices into the *.agd file format upon download.  This file format is compatible with the popular open source database SQLite ([http://www.sqlite.org/](http://www.sqlite.org/)).  The *.agd file schema can be found in Appendix A of this users guide.

### DOWNLOADING GT1M, GT3X, ASM, AND/OR ACTITRAINER DEVICES ###
To download data from GT1M, GT3X, ASM, or ActiTrainer devices, connect your device(s) to the computer – ActiLife will detect those devices and they will appear in the Devices grid.  Select (check the box) the devices that you wish to download and click “Download” at the top of the screen.  The Download Options screen will appear allowing you to select the type of file naming convention you would like.  The names can always be changed later or you can select ‘Prompt for Each Download’ to enter unique names for each downloaded device.  These options help to prevent name duplication during batch downloading.

![](/assets/img/DownloadOptions.png)

FIGURE 27 – DOWNLOAD OPTIONS WINDOW

To select a different download location, select “Select Download Location…” and browse to the desired download directory.  To make this directory the default download directory, check the box below the download location in the Download Options prompt.  This can also be changed by selecting the directory from the “Edit->Options->Directories” setting in the program’s main menu.

### SAVING BIOMETRIC DATA DURING DOWNLOAD ###

During the download process, ActiLife gives the user the option to store metadata information associated with each device and corresponding device wearer.  After clicking ‘Download’ from the devices grid, check the box entitled “Add biometric and user information” to expand the details grid below the download form.  This form is shown in Figure 28.  All of the fields shown here are optional.

![](/assets/img/DownloadBiometric.png)
 
FIGURE 28 - DOWNLOAD OPTIONS WITH BIOMETRIC INFORMATION

### SUBJECT NAME ###
Unless it is changed, the” Subject Name” will default to the subject name used to initialize the device.  Even if the biometric and user information grid is not expanded for population, the “Subject Name” will be stored with the *.gt3x or *.agd file upon download.  From this grid, the “Subject Name” can be changed prior to downloading.

### GENDER ###
Click the “Gender” column to reveal a dropdown menu.  Select Male or Female.

### HEIGHT ###
Use the “Height” column to enter the subject’s height in inches, centimeters, or feet/inches.  Select a different format by changing the Units of Measurement in the Options menu.

### WEIGHT ###
Use the “Weight” column to enter the subject’s weight in lbs or kg.  Select a different format by changing the Units of Measurement in the Options menu.

### DATE OF BIRTH ###
Use the “Date of Birth” column to edit the subject’s date of birth.  A calendar picker is provided, but it may be more convenient to simply type in the subject’s birthday.  The date format is mm/dd/yyyy.

### RACE ###
Use the “Race” column to select the subject’s race.  Select “White/Caucasian,” “Black/African American,” “Latino/Hispanic,” “Pacific Islander,” or “Other”.

### LIMB ###
Use the “Limb” column to select where the device was worn.  Options include “Wrist,” “Waist,” “Ankle,” and “Thigh.”

### SIDE ###
Use the “Side” column to specify the device wear location (left or right side of the body).

### DOMINANCE ###
The “Dominance” option allows users to specify whether the wear location side was the subject’s dominant or non-dominant side.

### CUSTOM FIELDS ###
When custom fields are collected as part of a template (see Building and Using a Template for more details), those custom fields will appear in the metadata grid as shown in Figure 29.  Additionally, the “Add Biometric and User Information” check box option will be permanently selected and entry of the custom fields will be required.

![](/assets/img/CustomFields.png)
FIGURE 29 – CUSTOM FIELDS IN THE BIOMETRIC AND USER INFORMATION GRID

Clicking “Download All Devices” from the form will download the data from the selected units and store the data in SQLite format stored with a *.agd file extension (See Appendix A – File Types in ActiLife6).

> ActiLife no longer stores data in DAT or CSV format. To convert data into one of those formats, select ‘File’ tab then the Import/Export option as shown in Figure 10.
>
>ActiLife can automatically create *.csv files on download by setting this in the edit menu.  Note that this only works for GT3X+ devices if an *.agd file is created during the download process.

### DOWNLOADING GT3X+ DEVICES ###
Downloading data from GT3X+ devices is very similar to download from other devices.  It is important to understand the difference in the file handling for this device.  In order to increase the efficiency of the download process, data from GT3X+ devices is downloaded in raw, binary format with file extension *.gt3x (see Appendix A – File Types in ActiLife which explains the *.gt3x format).  This binary format mirrors the proprietary compressed raw data format stored on the device itself and is unreadable by standard text editors.  In order to read the data or process the data with ActiLife, the *.gt3x files need to be uncompressed (i.e., exported to *.agd format) using ActiLife.  This can occur either during download or later when processing files.

To download data from a GT3X+, select the device(s) from the grid in the Devices tab and click “Download”.  A prompt similar to Figure 28 will appear.  Clicking “Download All Devices” will immediately download all of the data from the GT3X+ into the user’s default download directory.

### SCANNING OF GT3X+ DATA DURING DOWNLOAD ###
Data downloaded from GT3X+ devices can be scanned for problems at the time of download.  At this time, ActiLife can scan for null data (0s) which may indicate issues with the device accelerometer or non-compliance by the end-user.  To enable this scanning, open the Edit->Options menu and choose the Downloading submenu.  In the “Scan of GT3X+ Download” section, select the warning threshold.  Doing so will warn the user during the download process if the number of 0s within the file exceed the threshold.  To disable this feature, set the threshold to 100%.

To view the *.gt3x files, select “Communication->Show Download Folder” from the main menu in ActiLife5.  Files will appear in this folder as shown in Figure 30.

![](/assets/img/gt3xFiles.png)
FIGURE 30 – *.GT3X FILES

### UNCOMPRESSING *.GT3X FILES ###
Binary *.gt3x files can be uncompressed to *agd (for use in ActiLife), *csv, or *.dat file format.  Users have the option of creating *.agd files during the download process by checking “Create AGD File” from within the download prompt (see Figure 31).  Because GT3X+ devices record raw accelerometer data (see Appendix A – File Types in ActiLife for details), the parameters for the uncompressed file must be set at the time of download if the “Create AGD File” option is checked.  These parameters include the uncompressed epoch length, the number of axes, step counting, lux (light data), inclinometer (standing, sitting, lying, or off detection), and/or low frequency extension.  For an explanation of these parameters, see Available Channels (Modes) for details.

![](/assets/img/CreateAgd.png)
FIGURE 31 - CREATING AN AGD FILE ON DOWNLOAD

> Important: Creating an AGD file during the download process will increase the download time significantly depending upon the size of the download.

Binary *.gt3x files can be uncompressed at a later time if desired (e.g., after emailing or sharing the files).  To uncompress these files at a later time, select “File->Import/Export->Create AGD/CSV/DAT from Raw GT3X+” from the ActiLife main menu.  An export window similar to the one shown in Figure 32 will appear.  Individual *.gt3x files can be added by selecting the “Add GT3X+ Files(s)” option.  All of the *.gt3x files in a directory can be added by selecting “Add Directory…”  Once files are added, the desired file type(s), epoch length, and parameters can be selected within the export tool.  Select “Create File(s)” to export these files to the default download directory.

![](/assets/img/Gt3xExport.png)
FIGURE 32 – GT3X+ EXPORT TOOL

The GT3X+ export tool can also be accessed by clicking “finished downloading” hyperlink from the devices grid after downloading as shown in Figure 33.  

![](/assets/img/FinishedDownloading.png)
FIGURE 33 – FINISHED DOWNLOADING HYPERLINK IN DEVICES GRID

Clicking this link for GT3X or legacy ActiSleep devices as shown in Figure 34 will launch the AGD viewer, since these downloads produce an *.agd file by default (see Appendix A – File Types in ActiLife for more information).

![](/assets/img/FinishedDownloadLink.png)
FIGURE 34 – “FINISHED DOWNLOADING…” LINK IN STATUS COLUMN. LINKS TO AGD VIEWER FOR GT3X AND ACTISLEEP DEVICES

# BUILDING AND USING A TEMPLATE #
Templates were created to assist customers who deploy ActiGraph devices using remote distribution centers or who need to ensure consistency in the initialization and/or download process when multiple people (e.g., lab assistants) are distributing devices to patients.  Templates can be created only from within the full version of ActiLife (ActiLife Lite does not support template creation – only template usage).

Once a template is created, the template can be saved as an *.agt file.  This file can then be shared via email, jump drive, or any other means to various distribution centers or lab partners.  Opening this file will force ActiLife to use the settings defined in the template editor to initialize and download devices, thus ensuring data collection consistency.

## TEMPLATE EDITOR ##
ActiLife Full users will find an option in the File menu entitled “Template Editor.”  Clicking this option will load a form similar to the one shown in Figure 35.  Use this form to setup the desired default initialization and download parameters defined below in Template Parameters.

![](/assets/img/TemplateEditor.png)
FIGURE 35 – INITIALIZATION/DOWNLOAD TEMPLATE EDITOR

### TEMPLATE PARAMETERS ###

### INITIALIZATION TEMPLATE OPTIONS ###
Use the initialization options on the left side of the template editor to force template users to use specific settings during the initialization process.

### Template Name (required) ###
The name of the template that will appear at the top of ActiLife once the template is loaded.  An illustration is shown in Figure 15.  This is a required field.

### DEVICE SELECTION ###
Selecting “Enable Template for *****” within one or more of the device tabs will force ActiLife to use device-level settings during the initialization process for that particular device.
  
### START/STOP SETTINGS ###
Check either Start Date/Time or Stop Date/Time to force template users to use a Start or Stop time during the initialization process.  Use the Day selection box to choose a forced start time offset (e.g., +0 day, +1 day, +2 days, etc.) and use the time selection box to set the start time.  Use “Any” in the Day selection box to give the user the flexibility to choose which day the device should start collecting data but the rigidity to force a start time for data collection.  If the template start time has already passed, ActiLife will automatically default to the next day with the same start time.  For example, suppose the template is set to force users to start collecting data at “+0 day(s) at: 3:00pm.”  If a user initializes a device at 4:00pm, the start time will default to the next day at 3:00pm.

The Stop Date/Time option allows the template builder to set how many days the device should collect data before stopping.  Note that the Day setting refers to the number of days AFTER the start time.  Again, use “Any” in this field to give the user the flexibility of choosing the stop date but the rigidity of using a specific stop time.  Be sure to keep the battery life and memory limitation considerations in mind.  For more details about battery life, refer to the specific product manual for the ActiGraph device you are using.
 
Leaving either or both of the Start/Stop Settings unchecked will allow the user to select whether or not the start/stop times are used during the initialization process.

### SUBJECT NAME SETTINGS ###
Checking this option will force template users to use a certain convention when setting Subject Names for devices during the initialization process.  These options are self-explanatory with the exception of the “Static” option.  This option will force all Subject Names to exactly match the phrase typed here.

### DOWNLOAD TEMPLATE OPTIONS ###
Use the download options to force template users to use specific settings during the download process.

### CUSTOM FIELDS ###
Enable the “Custom Fields” option to force users to enter more information during the download process.  Use the “Max Characters” dropdown box to select the maximum number of characters allowed for this field.  This will prevent users from typing too many characters in this field.
  
The fields entered here will appear in the download grid as shown Figure 36 after clicking “Download” from the devices grid.  Note that these fields must be populated before users can proceed with the download.  In most cases (without a template in use), the “Add biometric and user information” check box can be de-selected (all of the biometric data is optional – see Saving Biometric Data during Download for details).  However, when custom fields are enabled in the template, this is required and users are forced to enter values for the custom field parameters.  Note that the custom fields are always on the right-hand side of the grid.  Users may need to scroll to the right to enter the fields.

Custom fields are stored with the *.gt3x files and/or *.agd files at download time.  When exporting *.gt3x files to *.agd format for analysis in ActiLife, the custom fields will be included as part of the export and will be contained in the *.agd file.  For details about the *.agd schema, see Appendix A – File Types in ActiLife.  In ActiLife version 5.6.0 or later, custom fields appear in the AGD File Viewer.

![](/assets/img/DownloadCustomFields.png)
FIGURE 36 – CUSTOM FIELDS AS THEY APPEAR AFTER CLICKING “DOWNLOAD”

### DOWNLOAD SETTINGS ###
Use the “Download Settings” in the download section of the template builder to force template users to utilize a specific file download location and/or a specific file naming convention.  By checking the “Force Download Location” and selecting a directory, template users will be forced to use the specific location.  Template builders can type in network URLs or any local directory address that may be applicable for the end-users’ specific sites.  

> Note: If the selected directory does not exist, ActiLife will attempt to create the directory (e.g., “C:\PatientDownloads”).  If the user does not have administrative permissions or otherwise cannot create the directory, this feature will automatically disable itself, thus allowing the user to select the directory of their choice.

To force a file naming convention for template users, check the “Force Naming Convention” option and select the desired naming convention.  During the download process, file names will be of the same format selected here for those users using the template.  The “Concatenate Custom Fields” option will concatenate the custom field characters entered by the user during download time.  Multiple custom fields will be concatenated with no dashes or separation punctuation.  At this time, there are no options for reordering or hyphenating the file name parameters when using the custom field naming convention.  These features will be added in later versions of ActiLife.

### SAVING AND SHARING TEMPLATES ###
Once the template parameters are set as desired, the template can be saved as a file and shared with other users.  Users can click the “Save” button in the bottom right-hand corner of the template editor or use the “File” menu to save the template file.  From the file menu, a template can be opened to make modifications (click “Open” then browse to the template file).  In addition, the template can be saved and immediately put into use by clicking “Save and Use.”  This option is helpful when testing the newly created template before emailing or sharing the template file.

Once the template is saved, a new file with an *.agt file extension will be created similar to the one shown in Figure 37.  This file can be emailed to distribution centers or shared over local networks within organizations.  Users who load this template will be forced to use the parameters as they were defined in the template editor.

![](/assets/img/TemplateFile.png)
FIGURE 37 – TEMPLATE FILE SAVED TO A USER’S DESKTOP

### LOADING TEMPLATES ###
Once the *.agt template file has been shared, ActiLife (Full or Lite) users can simply download the file to their local machine (anywhere) and double-click on the file.  Doing so will launch ActiLife and load the template.  When done correctly, the template name and “Last Modified” time will appear in the upper right-hand corner of the ActiLife software as shown in Figure 15 on page 10.  Once the template has been loaded once, the *.agt file can be removed from the end-user’s computer.  It is not necessary that the file remain on the user’s computer.

An alternative way of loading a template file in ActiLife is to use the “Load Template” option in the File menu.  Browse to the template file location and click ‘Open’ to load the template.

When a template is loaded in ActiLife, the template will remain present even after the software has been closed and re-opened. This ensures that the template settings remain unchanged when the host computer is shut down and restarted.  To remove a template, click “Remove Template” from the file menu.