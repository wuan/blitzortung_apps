---
weight: 10
title: "Android App"
bookToc: false
---

Overview
--------

The **Blitzortung Lightning Monitor** Android app visualizes lightning data provided by the [blitzortung.org](https://www.blitzortung.org/) network.

For information about the Blitzortung.org network and **important information on how to use the data**, see [blitzortung.org](https://www.blitzortung.org/de/contact.php). This information also applies to data use within this project.

-   [Android app @ Google Play Store](https://play.google.com/store/apps/details?id=org.blitzortung.android.app)
-   [Android app @ F-Droid](https://f-droid.org/de/packages/org.blitzortung.android.app/)

## Available translations

-   Czech
-   Dutch
-   English
-   French
-   German
-   Hungarian
-   Italian
-   Polish
-   Slovak
-   Russian
-   Spanish

Translation offers are welcome! Please contact us via `blitzortung at tryb.de`

## User privacy

The app uses device location to show your position on the map and for lightning warnings. This feature **can also be used without location permissions** - you can set your location manually via preferences or by long-pressing the map.

The app does not send any device ID or any other unique identifier to the server.

For efficient data transfer, the app fetches the last 10 minutes of lightning activity in a 5° x 5° area. This data cannot be used to track users because:

-   A 5×5 degree area covers ~555 km - too coarse to pinpoint a location
-   Coordinates are quantized to a grid, making it impossible to distinguish between users in the same region

## License

[Apache-2.0](https://github.com/wuan/bo-android/blob/main/LICENSE)

If you like to contribute by

-   reporting a bug
-   improving code or
-   improving localization

please have a look at the project <https://github.com/wuan/bo-android>.

Any contribution is welcome!

## Topics

-   GIS
-   Android Application
-   Lightning Network
-   Weather App
