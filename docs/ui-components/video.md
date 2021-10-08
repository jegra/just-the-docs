---
layout: default
title: Video
parent: UI Components
nav_order: 8
---

# Video
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Vimeo

Support for Vimeo-hosted videos is included in the theme.  To embed a Vimeo video, use the `vimeo.html` include file, along with the video's ID value (can be copied from the URL of the video).  For example:

{% raw %}
```liquid
{% include vimeo.html id="158396727" %}
```
{% endraw %}

There are a number of optional parameters that can be added to the include to adjust the way the video is displayed.  To add a parameter, insert it within the enclosing brackets like so:

{% raw %}
```liquid
{% include vimeo.html id="158396727" autoplay=true muted=true time="1m" %}
```
{% endraw %}

In the example above, we're indicating that the video should be muted and should autoplay, and that it should start at the 1 minute mark.  Note that some values can be overridden by the embed settings assigned on Vimeo's video configuration page (namely, `title`, `byline`, `color`, and `portrait`). 

Availabe parameters include

| Parameter  | Supported Values | Default Value | Description
|:--------------|:------------|:------|:----------------------|
| `autoplay`    | true, false | false | Automatically start playback of the video.<br>**Note:** May require `muted` to be set to `true`, depending on browser and device.
| `byline`      | true, false | false | Show the author of the video (byline).†
| `color`       | [hex value] | "00adef" (Vimeo blue) | Color of the video controls.†‡
| `controls`    | true, false | true  | Hide all elements in the player (play bar, sharing buttons, etc) for a chromeless experience.‡
| `loop`        | true, false | false | Play the video again when it reaches the end, infinitely.
| `muted`       | true, false | false | Mute the audio on load (can be re-enabled by user, if controls are displayed).
| `playsinline` | true, false | true  | Play video inline on mobile devices instead of automatically going into fullscreen mode.
| `portrait`    | true, false | false | Show the author’s profile image (portrait).†
| `speed`       | true, false | false | Show speed controls in the player.‡
| `time`        | Time in minutes and/or seconds (for example, time="1m2s") | "0m" (Start of video) | Used to automatically begin playback at a specific point in time.
| `texttrack`   | A lowercase language code and optionally the locale and type of text track. (examples: "en", "en-US", "en.captions", "en.subtitles") | false | Displays a given cc/subtitle track by default in the player (provided the cc/subtitle track is available). 
| `title`       | true, false | false | Show the video's title.†

† Value specified in the video's embed settings on site may override this.  
‡ Requires a **Plus** account or higher.

---

## YouTube

Support for YouTube-hosted videos is also included in the theme.  To embed a YouTube video, use the `youtube.html` include file, along with the video's ID value (can be copied from the URL of the video).  For example:

{% raw %}
```liquid
{% include youtube.html id="fnxBvgJQmtY" %}
```
{% endraw %}

There are a number of optional parameters that can be added to the include to adjust the way the video is displayed.  To add a parameter, insert it within the enclosing brackets like so:

{% raw %}
```liquid
{% include youtube.html id="fnxBvgJQmtY" autoplay=true mute=true start="90" %}
```
{% endraw %}

In the example above, we're indicating that the video should be muted and should autoplay, and that it should start at the 90 second mark.

Availabe parameters include

| Parameter  | Supported Values | Default Value | Description
|:--------------|:------------|:------|:----------------------|
| `autoplay`    | true, false | false | Automatically start playback of the video.<br>**Note:** May require `muted` to be set to `true`, depending on browser and device.
| `controls`    | true, false | true  | Hide all playback control elements in the player.
| `loop`        | true, false | false | Play the video again when it reaches the end, infinitely.
| `mute`        | true, false | false | Mute the audio on load (can be re-enabled by user, if controls are displayed).
| `playsinline` | true, false | true  | Play video inline on mobile devices instead of automatically going into fullscreen mode.
| `playlist`    | A comma-separated list of video IDs to play | false | If you specify a value, the first video that plays will be the video ID specified in the `id` parameter, and the videos specified in the playlist parameter will play thereafter.
| `related`     | true, false | true | The display of related videos at the end of playback can no longer be fully disabled, but if set to `false`, videos from the same channel as the video that was just played will be displayed. 
| `start`       | Time in seconds (for example, start="90") | "0" (Start of video) | Used to automatically begin playback at a specific point in time.

