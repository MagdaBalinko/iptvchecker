# IPTV Checker

A simple GUI tool that checks your IPTV connection using an Xtream API login, fetches live channel data, and exports information to CSV. It uses **FFmpeg**/**FFprobe** to probe streams and determine their status.

It bundles the necessary Python libraries, so users **do not need to install Python**.

It's based on Ron Mexico's and NewsGuyTor's great ideas, with a basic GUI and a couple of minor extra functionalities added. Go and check out their repos:

- [Ron Mexico's IPTV Checker](https://github.com/sudo-ronmexico/IPTVChecker-BitRate)
- [NewsGuyTor's IPTV Checker](https://github.com/NewsGuyTor/IPTVChecker)

## The Idea

With the increasing popularity of IPTV services and the vast number of channel groups/countries supplied, it can be overwhelming to figure out which groups or channels you want to disable to make your playlist more user-friendly. I personally struggled with this, even when using great tools like **m3u-editor** or **Dispatcharr**, so I decided to use AI to combine existing tools into one. It's entirely AI coded, with my input only being the list of functions and the basic GUI design.

I think it’s worth sharing, both the Python script and a small Windows executable.

---

## Requirements

Before running the tool, make sure you have **FFmpeg** and **FFprobe** installed on your machine and accessible from the command line.

- Download **FFmpeg** from [here](https://ffmpeg.org/download.html).
- Ensure **FFmpeg** and **FFprobe** are added to your system's **PATH** environment variable.

You can verify this by running:

```bash
ffmpeg -version
ffprobe -version
Your own playlist / Xtream API login details

The EXE includes all required Python libraries — users do not need to install Python.

Running as Python Script
If you prefer to run the Python script directly, follow these steps:

Install Python dependencies:

pip install -r requirements.txt
Run the Python script:

python IPTV_Checker_v2_4.py
Usage:
Give a name to the service (this will be included in the filename with a date stamp).

Enter the server URL, user ID, and password.

Click Test Connection.



This step is mandatory — checks if the connection is alive and gives you the number of groups (Live TV) recognized/included.



Modes (3 different modes included):
Export Group List – Exports all group names and the number of channels per group included in your subscription.

Export Channel List – Exports all channels/channel IDs included in your subscription + direct link to the stream.

Probe Streams – Strongly recommended to select a handful of groups; otherwise, your provider might block you. It also displays direct stream URLs. Gives you an indication of whether a channel is alive or dead, what group it is listed under, stream ID, codec, resolution, FPS, video bitrate, audio codec, and bitrate.

Example outputs:

For Export Group List:



For Export Channel List:



For Probe Streams:



Downloads
Precompiled Windows executable and Python script are available on the Releases page:
👉 Releases

Extra Features/Important Notes:
If you probe multiple playlists or groups, make sure to change the filename before running it.

The tool adds the service name and a date stamp (in DD-MM-YYYY format) to the CSV file.

To probe or extract channels from specific groups, click on the down arrow and select the needed groups. Multiple selections work (Ctrl + Left mouse button). You can also use the search feature, and it’s recommended to use country prefixes (e.g., UK, US, HU, IE) depending on your provider.



Disclaimer
I’ve tested it with 4-5 different providers via Xtream API login (m3u is not supported). It worked with all except one.

Contributing
Issues and pull requests are welcome! Feel free to suggest improvements.

That's all, Folks! 😊
