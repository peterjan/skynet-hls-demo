# Skynet HLS Demo

## What is HLS

HLS stands for HTTP Live Streaming. In short, HLS is a media streaming protocol for delivering visual and audio media to viewers over the internet.  
[This](https://www.dacast.com/blog/hls-streaming-protocol/) is a great resource to learn more about HLS.

## HLS on Skynet

#### Does Skynet support HLS streaming?
> Yes

#### No way!
> Yes way!

## Instructions
You can test it yourself in a couple of easy steps.

1. Find an audio or video file you want to stream using HLS. This repo contains a test file that you can use with some nice jelly fish.
2. Use ffmpeg to turn your file into a playlist file and .ts chunks
```bash
ffmpeg -i jellyfish.mp4 -profile:v baseline -level 3.0 -s 640x360 -start_number 0 -hls_time 10 -hls_list_size 0 -f hls index.m3u8
```
3. Upload that directory to [Skynet](https://siasky.net)

You might have to install a plugin if your browser does not support native HLS playback. 
For chrome [Native HLS Playback](https://chrome.google.com/webstore/detail/native-hls-playback/emnphkkblegpebimobpbekeedfgemhof) is a good one.

## Demo URL

The best place to test your HLS steams is on https://hls-js.netlify.com/demo/.

This is a [working HLS demo](https://hls-js.netlify.com/demo/?src=https%3A%2F%2Fsiasky.net%2FAACaBKPpZmzoky48x8S2a1vYUNlC1p6647eV7cyIz_Bcrg%2Fjellyfish%2Findex.m3u8&demoConfig=eyJlbmFibGVTdHJlYW1pbmciOnRydWUsImF1dG9SZWNvdmVyRXJyb3IiOnRydWUsImR1bXBmTVA0IjpmYWxzZSwibGV2ZWxDYXBwaW5nIjotMSwibGltaXRNZXRyaWNzIjotMX0=) of the jelly fish.


