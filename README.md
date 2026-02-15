Hi All

## IPTV Checker

A simple GUI tool that checks your IPTV connection using an Xtream API login, fetches live channel data and exports information to CSV. It uses FFmpeg/FFprobe to probe streams and determine their status.

It bundles the necessary Python libraries, so users do **not need to install Python**.


It's based on Ron Mexico's and NewsGuyTor's great ideas, with a basic GUI and a couple of minor extra functionalities added. Go and check out their repos

https://github.com/sudo-ronmexico/IPTVChecker-BitRate

https://github.com/NewsGuyTor/IPTVChecker

The idea behind is with the increasing popularity of ITPV services and the vast number of channel groups/countries supplied. When you get a new sub
it can be extremely overwhelming to determine what groups, channels you plan to disable to make your playlist more user friendly. I personally struggled
with this, even when using great tools like m3u-editor or Dispatcharr so I decide I use AI to combine existing tools into a new one. It's entirely AI coded, 
my input is just the list of functions and the basic GUI design.

I come to a stage when I think it's worth sharing, both the Pyhton script and a small Windows Executable.

## Requirements

Before using this tool you must have:

- **FFmpeg** installed and added to your system PATH
- **FFprobe** installed and added to your system PATH
- **Your own** playlist / Xtreme API login details

> The EXE includes all required Python libraries — users do **not** need to install Python.


Usage:
1. Give a name to the service, this will be included in the filename (with date stamp)
2. Enter the server URL (aka DNS), user ID & password
3. Click Test Connection
   
<img width="722" height="586" alt="image" src="https://github.com/user-attachments/assets/e98c661d-c56f-4393-939b-f34cf0d88b53" />

3.A. This is mandatory, checks if the connection is alive and gives you the number of groups (Live TV) recognized/included

<img width="407" height="123" alt="image" src="https://github.com/user-attachments/assets/a6ef1b12-f893-4af5-91e8-a57a273526d6" />

4. Modes - 3 different mode is included
4. A. Export Group List - this exports all groups names and number of channels per group is included in your sub
4. B. Export Channel List - this exports all channels/channel ID included in your sub + direct link to the stream
4. C. Probe streams - Strongly recommended to select a handful number of groups otherwise your provider might have an issue, also
   displaying direct stream URL. Gives you an indication if channel is alive or dead, what group is listed, stream ID, codec, resolution,
   FPS, Video bitrate, Audio codec and bitrate and stream URL. Can't figure out why it is not pulling video bitrate on all alive channels, it's
   really a hit & miss at the moment.

Example output:

For 4.A.

<img width="671" height="75" alt="image" src="https://github.com/user-attachments/assets/3b01df44-61f2-42f1-873b-4564bc960b28" />

For 4.B

<img width="1110" height="57" alt="image" src="https://github.com/user-attachments/assets/96411b3d-a83c-4dd8-bdb1-cb22f146278b" />

For 4.C

<img width="1251" height="57" alt="image" src="https://github.com/user-attachments/assets/cacd314a-8da2-4531-8985-ad054e3a4c52" />

## Downloads

Precompiled Windows executable and Python script are available on the **Releases** page:
👉 https://github.com/MagdaBalinko/iptvchecker/releases


Extra features/important stuff

* If you probe multiple playlists, groups, channesl make sure to change file name before running it
* It adds Service name + date stamp (in DD-MM-YYYY format) to the CSV file
* If you want channel extract or probing of a specific number(s) of groups pls click on the down arrow and select the groups needed. Multiple
  selectio works, CrtL + Left mouse button. Search works, depending on the provider I suggest using country pre-fixes (i.e. UK, US, HU, IE, etc)

<img width="848" height="597" alt="image" src="https://github.com/user-attachments/assets/7d57adc8-6d3d-496f-86e9-4007184a5fd9" />

Disclaimer: I tested it with 4-5 different provider via Xtreme API login (m3u is not supported) it worked with all except one. 

## Contributing

Issues and pull requests are welcome! Feel free to suggest improvements.


That's all, Folks! 
