Graphing Tab
============

--------------

ActiLife’s graphing tab allows users to quickly see graphs of each day
in a given dataset. Click “Select Dataset” and browse to an .agd file
containing data. The graphs will load vertically and will be ordered
from latest to most recent date, ascending downward. Zooming is
accomplished by dragging the mouse over the area of interest as shown in
Figure 48. Graphs can be reset by clicking the small icon in the bottom
left-hand corner of the graph which is also illustrated in Figure 48.

EXPORTING
---------

Graphs can be exported to a PDF by clicking “Export to PDF” in the top
right corner of the Graphing tab. Selecting “Keep any zoom information”
will output the graph with the current zoom view (if any). Individual
days can be exported to pdf by checking or unchecking the days in the
Export dialog.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/GraphingExport.png
   :alt: 

FIGURE 64 – GRAPHING EXPORT DIALOG

MODE OPTIONS
------------

The “Mode Options” section to the right of the graphs gives users the
ability to add or remove data items and change the color of various
items on the graphs. If a dataset contains three-axis activity
information (i.e., if the device was set to collect three-axis data upon
initialization), all three axes will be available for selection (not
disabled) in the “Mode Options” section. Deselecting any axis will
remove it from the graph view. Multiple axes can be enabled
simultaneously; however, in order to avoid cluttering the graph view,
only one alternative data point can be shown simultaneously with
activity data. To enable Steps, Heart Rate, Lux, or Inclination, select
the radio button corresponding to the correct data point. A legend
explaining the meaning of each data point will appear below the “Mode
Option” section when a given data point is selected as shown in Figure
65. Axis values can be scaled by entering new values into the activity
scale boxes to the right of the graphs.

Parameter graph colors can be selected by clicking the palette icon to
the right of the variable of interest and choosing the desired color.
The graph will immediately update with the new color.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/GraphingLegend.png
   :alt: 

FIGURE 65 – GRAPH LEGENDS

AXES SCALING
------------

Unless specified, each day shown in the graphing area is scaled
individually according to the maximum values collected on that day. By
checking the “Equal Scales” option on the right, all activity graphs
will be scaled evenly according to the number in the scale box. These
scale boxes can be seen in Figure 65.

INCLINOMETER
------------

The inclinometer tool can be used to detect positional information when
any 3 axis device is worn on the waist or thigh. Thigh-worn devices are
inherently better at detecting sedentary (sitting/lying) versus
non-sedentary (standing/stepping) than are waist-worn devices.

If an *.agd dataset contains no inclinometer data, a message similar to
the one shown in Figure 66 will appear. To utilize the inclinometer
tool, select “Inclinometer” when initializing a GT3X or when creating an
*.agd file from a GT3X+ device. It is important that the device
wear-location be specified for any *.agd file. To edit the wear
location, open the *.agd file in the AGD File Viewer and edit the
biometric information; update the “Limb” to be either “Waist” or
“Thigh”.

    Note: Only Waist and Thigh worn devices can be used with the
    Inclinometer tool

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/GraphingNoInclinometer.png
   :alt: 

FIGURE 66 - FILE WITH NO INCLINOMETER DATA

Once an appropriate file has been loaded, the Inclinometer tool will
display a breakdown of hourly positional information as shown in Figure
67. The calendar on the right can be used to navigate among days in the
dataset to quickly jump to an area of interest. Any notes written in the
Notes area will be stored with the \*.agd file and will be available in
the PDF report and in any subsequent interaction with the Inclinometer
tool for that particular file.

.. figure:: https://s3.amazonaws.com/ActiLifeManualImages/GraphingInclinometer.png
   :alt: 

FIGURE 67 - INCLINOMETER OUTPUT

Note that the graph colors can be changed by using the color palette on
the right hand side as well.

CREATING AN INCLINOMETER REPORT
-------------------------------

A PDF report of the Inclinometer output can be created by clicking the
“Export to PDF…” button. Users will be given the option to choose which
days to export to the report.

    Important: The inclinometer feature was designed by the ActiGraph
    engineering team as a viable way to detect user positional trends
    over a period of time. The thigh worn algorithm is best suited for
    positional detection as it is difficult to algorithmically determine
    the difference between sitting and standing for waist-worn devices.
    For more information about the waist-worn inclinometer algorithm,
    see our Inclinometer White Paper.
