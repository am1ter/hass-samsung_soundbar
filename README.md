Samsung Soundbar HW-MS650 Home Assistant custom component
============
Control volume, and source of your multiroom device like Samsung Soundbar K650, HW-MS650 or Q90R. 
This is a fork of idmedia's [ha_samsung_multi_room] (https://github.com/IDmedia/hass-samsung_soundbar), original version is custom_component by macbury's [ha_samsung_multi_room](https://github.com/macbury/ha_samsung_multi_room) working on the latest version of Home Assistant.

## Installation using HACS (Recommended)
1. Navigate to HACS and add a custom repository  
    * **URL:** https://github.com/am1ter/hass-samsung_soundbar
    * **Category:** Integration
2. Install module as ussual
3. Restart Home Assistant

## Configuration
| Key | Default | Required | Description
| --- | --- | --- | ---
| name | | yes | Name of the media player.
| host | 127.0.0.1 | no | The ip of your soundbar.
| port | 55001 | no | The port which the soundbar uses. My MS650 uses 55001, but the port might differ, try 56001.
| max_volume | 30 | no | Limit the max volume.
| power_options | true | no | Enable or disable the power options

## Example
Add the following to your `configuration.yaml`:
```
media_player:
  - platform: samsung_soundbar
    name: "Soundbar"
    host: 192.168.1.227
    port: 55001
    max_volume: 30
    power_options: True
```

# Sources

* bt - bluetooth
* aux
* optical
* hdmi
* wifi

# Api support
Based on information gathered from: https://github.com/bacl/WAM_API_DOC/blob/master/API_Methods.md
