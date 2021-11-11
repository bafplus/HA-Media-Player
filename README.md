# HA-Media-Player

A variation on the [Radio Content player](https://www.digitaldomo.nl/homeassistant/dashboards/radio-content-player/).

![lovelace](https://www.digitaldomo.nl/wp-content/uploads/2021/08/image-4-768x303.png)

The big differance to the above script is that in this version each (radio)stream allong with all its variables are within 1 block.
This makes it easier to maintain because everything is placed inside 1 block instead of scatered thruout the script making it easy to find and change/adapt the variables. As a big plus you can now extend each block with extra metadata or even different type of media so you can now mix audio with video like youtube.
The installation stays the same as the original script.
Within the script you see 3 examples, one for a mediafile like a MP3, one for a radiostream and one for a youtube video.
The aim of this script is to work with google speakers and chromecast devices, but may possibly work on other mediaplayers like Echo dots etc. Just play around with the values for media_content_id and its metadata to fit your target device.

To add a file, stream or video just copy/paste the needed condition as much as you need.

# Installation

- Create a helper named "radio_volume" and type "input_number". We need to add this within the UI because you cant add this type from the configuration.yaml. (a restart of HA may be needed afterwards)
![radio_volume](https://www.digitaldomo.nl/wp-content/uploads/2021/08/image-3-1004x1024.png)
- Add the contents of helpers.yaml in your configuration.yaml or link the file with "input_select: !include helpers.yaml". In this file there are 2 helpers to populate the dropdownlists. Make sure you use the exact names as the ones you use for each condition in the script. 
- Copy the contents of script.yaml into your script.
- Add the content of lovelace-card.yaml into a new card on your lovelace dashboard.
- Check if the script entity matches your script
![card](https://www.digitaldomo.nl/wp-content/uploads/2021/08/image-2-768x486.png)




A big shoutout to [@TheFes](https://github.com/TheFes) for helping out!
