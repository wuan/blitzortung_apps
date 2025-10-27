---
weight: 10
title: "Background and History"
bookToc: false
---

# Background and History

Development started in 2012 as a for fun project using [Blitzortung.org](http://blitzortung.org) data using the basic ideas:

## Privacy considerations

* Do not use Ads to monetize the app.
* Do not track individual devices / users.
* Do not use push notifications (Which might impact user privacy on the push notification service side).
* Do not track source IPs. (Just using a local GeoIP database for rough location estimation)

## Initial configuration

Initially the user needed to select a region (bounding box on the map which roughly resembles the region which is used by Blitzortung.org )

## Introducing Alerts

### Device location

* Location data should not leave the device
* Using full region data which requires that the user sets the correct region he is currently located in.
* Overall location data is not required to run the app.
* The user also can select a manual location which will allow alerts but without the device tracking the user's location.

### Periodic data updates

* Poll data for configured region
* Background operation of app service will require extra permissions.
* This can impact battery life especially with periodic updates in the range of 1 minute. (We found that 5 minute periods are a good compromise)

## Introducing Global / Local Data mode

The requirement to configure the correct region has always been a problem for our non-EU users (EU being the configured default region)

In order to minimise the impact on the server load, overall data transfer, and device network usage we introduced a Local data mode which only will request data in a local region around the device location.

This is done by sampling the longitude and latitude of the device location to a 5° increment which should be coarse enough to not allow any user tracking better than the IP location. The data will be transmitted for a 15° x 15° tile surrounding that user area to allow having full coverage even when being at the edge of the region.

   ![](/app/background/local_data.png)

## Moving from Google Maps to OpenStreetMap

April 2019 (Version 1.6.5 to 2.0.0)

This step has been planned for a while, and it should solve multiple issues:

* Getting independent of Google Play Store should also allow deploying the app to F-Droid for all users trying to avoid using Google services.
* Google Maps V1 has been deprecated and needed a replacement.

On the downside we needed to replace the (relatively dark) satellite image view with the default rendered tiles of OpenStreetMap (the decision has been to avoid on device rendering to allow usage on older devices).

It took us some time in the beginning to figure out the best configuration and display settings (brightness and scaling) for OpenStreetMap tiles. This also included the correct permissions for storing data locally in order to cache downloaded tiles.

We had many unhappy users and received many one-star ratings where people tried to push us back using Google Maps which was not an option because of the reasons given above.

| ![](/app/background/gmapv1_1.6.5.png) | ![](/app/background/osm_2.0.0.png) |
|---|---|

## Introducing automatic grid size and local data mode

Introduced in June 2020 with Version 2.1.0 (265)

Introducing the local data mode has already been a big step forward for minimising the data transfer and server load for background operation. Still having global data queries with 5 km raster from interactive app usage has been hitting the servers.

So it was time to introduce an automatic selection of grid size and data mode for interactive app usage which should be totally transparent. Having global data mode for small zoom levels (world / continent) overview and automatically switching to local data mode when users are zooming in to a specific region.

## Introducing animation mode and history slider

October 2023 Version 2.2.0 (313)

{{< raw_html >}}
<video width="100%" autoplay loop muted controls>
  <source src="/app/android/main_animation.webm" type="video/webm">
  Your browser does not support the video tag.
</video> 
{{< /raw_html >}} 

Animation mode has been on our feature list for a long time. With the added caching mechanism, it is possible to implement a time slider for the history allowing direct access to past data.

<video width="100%" autoplay loop muted controls>
  <source src="/app/android/main_history.webm" type="video/webm">
  Your browser does not support the video tag.
</video> 

## Internal modernisation

Introduced in August 2025 Version 2.4.0 (341)

With increasing complexity of modern Android permission management we completely rewrote the permission handling and related code which already had created some issues for our users. 


