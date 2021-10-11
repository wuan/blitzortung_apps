---
weight: 10
title: "Main Screen"
bookToc: false
---

# Main screen

![](/app/android/main_realtime_25.png)

## Elements

### Top left -- Legend

![](/app/android/legend_40.png)

  * Show time range for color coded strike activity age used on map
  * Additional information
    * Grid baseline e. g. "Grid: 10km"
    * Region 
      * Europe, North America, Asia, ...
      * Local, for limited local area
      * Not given for Global data
    * Count threshold setting
      * Not displayed for inactive threshold
      * E. g. "# > 5" for a threshold of 5
      * Only raster areas with strike counts greater or equalt to the threshold are displayed
  * Tap for quick settings:

    ![](/app/android/quick-settings_25.png)

### Top right -- Menu / History

| realtime | history |
|----------|---------|
| ![](/app/android/menu-realtime.png) | ![](/app/android/menu-history.png) |


  * Open menu (on devices without menu button)
  * Browser through history
    * Time step can be changed in the settings.
    * Can be used to browse through the last 24 hours of ligthning activity.

### Bottom left -- Alarm radar

| active | inactive |
|----------|---------|
| ![](/app/android/alarm-radar-active_40.png) | ![](/app/android/alarm-radar-inactive_40.png) |


  * Shows activity by distance for the current location
  * Requires
  	* lightning data
  	* known location
  	* realtime mode
  * Tap to center map around location
  * Long press to open bigger version of Alarm radar

### Bottom right -- Histogram

![](/app/android/histogram_40.png)

  * Shows the development of strike rate over the given time period (for the data region)
  * Tap to zoom out on region

## Menu

### Preferences
 
Open Detailed App settings

### Alarms

Open the alarm radar:

![](/app/android/alarm-radar_25.png)

Color coding of last strike activity is shown according to the legend information.

### Application log

Show dialog with internal app application log. Can be used for immediate debugging. Creates an Email to send in the application log to get help.

### Change log

Show dialog containing recent app features by version number

### Information

Show a dialog with app related information.