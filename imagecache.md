# imagecache
Functions controlling the configuration of the Image Cache.

These functions are only available if Image Cache support was included at compile time.
## imagecache/config/load
TODO
## imagecache/config/save
TODO
## imagecache/config/clean
Delete all files from the image cache and re-load, in the same way as Configuration -> General -> Image Cache -> Clean Image (icon) Cache in the GUI.
- `clean` Required parameter, must be 1 - the value is not used.
## imagecache/config/trigger
Trigger a re-load of the image cache, in the same way as Configuration -> General -> Image Cache -> Re-fetch Images in the GUI.
- `trigger` Required parameter, must be 1 - the value is not used.
