# Appendices #

----------

## Appendix A - FILE TYPES IN ACTILIFE ##

### COMPARISON OF GT3X+ AND GT3X DEVICES ###

Before explaining the difference between the *.gt3x and *.agd files, it would be useful to explain the paradigm differences between the GT3X and GT3X+ device platforms.  GT3X devices sample accelerometer data 30Hz (only).  This data is then filtered and accumulated into user-selected epoch sizes (60s, for instance) inside of the device.  Because this data is being processed and accumulated into epoch-size chunks, on-board storage requirements are relatively small.  Whenever ActiLife downloads data from these devices, it produces an *.agd file (epoch-level file) which can then be processed inside of ActiLife.

GT3X+ platform devices are different in that the user selects the rate at which raw data is sampled from the accelerometer (the user can choose any frequency between 30-100Hz in 10Hz increments).  The GT3X+ then stores every sample, making the data storage requirement for this device type much greater.  Upon download, the GT3X+ device produces a *.gt3x file (raw data).  The ActiLife software can then be used to band pass filter and accumulate that raw data into epoch-level data, thus producing an *.agd file that is equivalent to the one produced from the GT3X device as described above.  The benefit of the GT3X+ device is that the user can produce any epoch-level output from the raw data.  In addition, the raw data is available to perform other analyses outside of the scope of this discussion.  

Figure 75 graphically explains the difference between the GT3X and GT3X+ devices.

![](/assets/img/FileComparison.png)

FIGURE 75 - COMPARISON OF THE GT3X AND GT3X+ DEVICES (AND ACTILIFE'S ROLE)

### *.GT3X FILE FORMAT ###

GT3X+ devices produce an interim compressed file with file extension *.gt3x.  This is a compressed file and must be extracted to a usable format using ActiLife’s import/export tool which is accessible from the File menu in ActiLife.  The file can be exported to *.agd format for processing in ActiLife or *.csv/*.dat format for processing using third party tools.  The *.gt3x file can also be exported directly to *.agd format during the download process by checking “Create AGD File” from the download prompt (see Downloading GT3X+ Devices for more information).

### *.AGD FILE FORMAT ###

The *.agd file format is ActiLife’s native file format and is the desired file type for all ActiLife operations and tools such as Wear Time Validation, Data Scoring, Sleep Scoring, and Graphing.  These *.agd files are database files formatted for use with the popular SQLite architecture (www.sqlite.org).  These files can be viewed in the ActiLife AGD viewer (available from the File menu).  Alternatively, the SQLite browser (publically available on the SQLite website) can be used to browse the details of the *.agd files.  A file schema is provided in Figure A1.

![](/assets/img/AgdSchema.png)

FIGURE 76 - *.AGD FILE SCHEMA

*.agd files are created in ActiLife immediately when data from a GT1M, GT3X, ActiTrainer, or ActiSleep device is downloaded through the “Devices” tab.  These *.agd files typically contain post-filtered and accumulated data as this is the only type of data that ActiLife can properly handle.  The rows in the database represent whole-number epoch summations (1s, 5s, 10s, 30s, 60s, etc.).  However, at the time of this writing all GT1M, GT3X, ActiTrainer, and ASM products that have been initialized to collect raw data (12Hz or 30Hz) will produce an *.agd file on download.  Although the file cannot be processed in ActiLife, the *.agd format can be exported to *.csv or *.dat through ActiLife’s import/export tool or AGD viewer tool, both accessible from the File menu.

GT3X+ and ActiSleep+ devices produce a *.gt3x file on download (see *.gt3x File Format).  In order to process in ActiLife, the file must be exported to *.agd format.  This can be done at the time of download by checking “Create AGD File” from the download dialog box or by using ActiLife’s built-in import/export tool available from the File menu.
 
### *.AGD DATA TABLE FORMAT ###

The data table in the *agd database consist of the following parameters.  Their calculations are explained.

**dataTimeStamp** – a measure of total Ticks.  A single tick represents one hundred nanoseconds or one ten-millionth of a second. There are 10,000 ticks in a millisecond.  The value of this property represents the number of 100-nanosecond intervals that have elapsed since 12:00:00 midnight, January 1, 0001.  More information available at http://msdn.microsoft.com/en-us/library/system.datetime.ticks.aspx

**axis 1** – Post filtered and accumulated per-epoch vertical activity data

**axis 2** (optional) – Post filtered and accumulated per-epoch horizontal activity data

**axis 3** (optional) – Post filtered and accumulated per-epoch perpendicular activity data
 
**steps** (optional) – Total steps per epoch

**hr** (optional) – Heart beats-per-epoch.  This data is only gathered by ActiTrainer devices when those devices are initialized to collect heart rate data AND when the Polar® Heart Monitor (wireless heart strap) is worn by the user.

**Lux** (optional) – Ambient light sampled once per second (on GT3X+ and ASM devices only) and averaged over the length of the selected epoch.  (e.g., for 60s epochs, this would be the light values summed once per second and divided by 60).

**Inclinometer** (optional) – Device orientation information.  This is calculated by sampling the angle of the device over the entire length of the epoch (30 times per second) and selecting the predominant angle; i.e., the angle “range” that appeared the majority of the time over the epoch.  For details about inclinometer functionality, see the Inclinometer Whitepaper.

### *.DAT FILE FORMAT ###

Older versions of ActiLife produced *.dat files when downloading data from devices.  These files consist of ten (10) lines of header data (meta information about the content) followed by epoch accumulated/filtered data.  This “DAT” file stores all of the activity (1 to 3 axis), pedometer, Inclinometer, and/or heart rate data in ASCII format.  This file also contains the Serial Number, Start Time, Start Date, Epoch Period, Download Time, Download Date, Current Memory Address Pointer, Current Battery Voltage, Mode and First Start Time (used to build the DAT file) as part of its ten (10) line header information.  The file can be viewed with any standard text editor such as MS Notepad. The Mode value given in the header of the DAT file outlines which features were active during data collection for the file.  Table 6 outlines the values of the Mode variable.

![](/assets/img/ModeWordDefinition.png)

TABLE 6 - MODE WORD DEFINITIONS

## Appendix B - VECTOR MAGNITUDE ##

The term Vector Magnitude is used frequently throughout this manual and often when working with ActiGraph devices.  Vector Magnitude refers to the magnitude of the resulting vector that forms when combining the sampled acceleration from all three axes on any device.  Figure 77 illustrates the axes orientation for all ActiGraph devices.

![](/assets/img/AxisDefinitions.png)

Figure 77 - Axis Definitions for ActiGraph Devices

When looking at epoch level data (post filtered and accumulated data), the Vector Magnitude (or VM) can be defined as 

![](/assets/img/VectorMagnitude.png)

This value can be calculated on a per-epoch basis or as a sum for all axes over time.
