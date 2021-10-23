# widevine-L3-WEB-DL-Script
This is a script created to WEB-DL L3 Widevine Content.

Works well with .mpd files , for m3u8 please use n_m3u8 program (not included in this script).

## How to use
### Requirements
* Widevine Key Guesser
  * Download zip from https://github.com/parnexcodes/widevine-l3-guesser-modified
  * Activate developer mode in Chrome Extensions
  * Use "Load unpacked" to load the extracted extension folder

### Get the keys
Go to the protected stream you want to download. Activate the plugin (restart may be required after installing the extension) and download the extracted keys (keys.json).

### Decode the video
Open the project in Google Colab. Copy the downloaded keys.json file to the folder (/content).

Mount Google Drive & Install Dependencies then run the downloader.

The script will look in the keys.json file, starting from the second element in the JSON array. If the script can't find any keys, either modify the script (line 27 and 31), or the keys.json. See <https://gist.github.com/parnexcodes/74fef2e33a2171031000a97c371a1a65> for examples for some common use cases.

If there are multiple `mpd_url`s in the file and it isn't working, try changing them around. You can also change the `mpd_url` for a custom one if you have one.

### Options
**-id** = Manually enter video and audio id from ytdl

## Report Issues

Open Issue on Github if you get any problem.
