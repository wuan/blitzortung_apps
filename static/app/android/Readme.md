# Static images

Created screenshots using emulator with Google Pixel 2 XL API 27.

Create smaller versions and crops of images using ImageMagick:

```
magick main_realtime.png -resize 25% main_realtime_25.png
magick main_history.png -resize 25% main_history_25.png
magick main_history.png -resize 25% main_history_25.png
magick main_quick_settings.png -resize 25% main_quick_settings_25.png
```

```
magick main_realtime.png -resize 50% -crop 100x300+620+80 menu_realtime_50.png
magick main_history.png -resize 50% -crop 100x300+620+80 menu_history_50.png
magick main_animation.png -resize 50% -crop 100x300+620+80 menu_animation_50.png
```