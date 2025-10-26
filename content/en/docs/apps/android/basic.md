---
weight: 10
title: "Main Screen"
bookToc: false
---

# Main screen

![](/app/android/main_realtime_25.png)

The time slider in the bottom allows to select a point in time out of the last 24 hours to be shown on the map. Moving the slider to the right activates the realtime mode.

## Elements

### Top left -- Legend

![](/app/android/legend_50.png)

  * Time range for color-coded strike activity age used on map:
    * "white": latest lightning activity within the last 10 minutes
    * ...
    * "dark orange": latest lightning activity between 40 or 50 minutes ago
    * "dark red": latest lightning activity older than 50 minutes
  * Additional information
    * Region 
      * Europe, North America, Asia, ...
      * Local[&lt;size&gt;], for limited local area data. `<size>` degrees region size.
      * Not given for Global data. 
    * Grid baseline e. g. "Grid: 10km"
      * Not given for Blitzortung.org data.
    * Count threshold setting
      * Not displayed for inactive count threshold setting
      * For example, "# > 5" for a threshold of 5
      * Only raster areas with strike counts greater or equalt to the threshold are displayed
  * Tap the legend to open "Quick settings" dialog:

    ![](/app/android/main_quick_settings_25.png)

### Top right -- Menu / Control

| Realtime                               | History                               | Animation                               |
|----------------------------------------|---------------------------------------|-----------------------------------------|
| ![](/app/android/menu_realtime_50.png) | ![](/app/android/menu_history_50.png) | ![](/app/android/menu_animation_50.png) |


  * Open menu (on devices without menu button)
  * Realtime mode:
    * Start Animation
  * History mode:
    * Start Animation
    * Jump to Realtime
  * Animation mode:
    * Stop Animation

### Bottom left -- Alarm radar

| active | inactive |
|----------|---------|
| ![](/app/android/alarm-radar-active_40.png) | ![](/app/android/alarm-radar-inactive_40.png) |


  * Shows activity by distance for the current location
  * Requires
  	* lightning data
  	* known location
  	* realtime mode
  * Tap to center map around the location
  * Long press to open a bigger version of Alarm radar

### Bottom right -- Histogram

![](/app/android/histogram_40.png)

  * Shows the development of strike rate over the given time period (for the data region)
  * Tap to zoom out on region

### Map content

The lightning activity is shown on the map in tiles with variable size (5 km, 10 km, 25 km, 50 km, 100 km). Each tile with recorded lightning activity in the selected time range gets colored with respect to the most recent activity within the current interval. The numbers which appear inside the tiles show the number of lightning events recorded in the area of the tile during the relevant time interval.

![](/app/android/main_map_data.png)

## Menu

### Preferences
 
Open Detailed App settings

### Alarms

Open the alarm radar:

![](/app/android/alarm-radar_25.png)

Color coding of last strike activity is shown according to the legend information.

### Application log

Show a dialog with internal app application log content. Can be used for immediate debugging. Creates an Email to send in the application log to get help.

### Change log

Show a dialog containing recent app features by version number

### Information

Show a dialog with app-related information.

## Map usage

Operations:

  * Double-tap to zoom in
  * Pinch to zoom
  * Slide to move
  * Long press to select location for manual location mode
