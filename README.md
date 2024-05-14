# HLS Internet Radio Demo

HTTP Live Streaming (HLS) was released by Apple in 2009. It is standard and supported by almost everything.

We should be doing more with the internet, we should be creative for the sake of being creative (and marketing).

## tech sandwich

- Microphone/Queued Playlist (source)
- OBS (encoder)
- MediaMTX (transcoder/segmenter)
- TODO: Nginx (HLS Proxy)
- TODO: Nginx (Load Balancer)
- HLS.js

## todo

- [x] put together a simple demo of HLS so that people can see live/queued audio working with OBS
- [ ] write the proxy server so that we can scale horizontally
- [ ] write the load balancer so that we can send users to the least utilized server
- [ ] make the client more robust and share as an embeddable widget for the web

## setup

- OBS
    - Settings > Stream
        - URL: rtmp://localhost
        - Stream Key: mystream
- MediaMTX
    - `cd mediamtx`
    - `sudo mediamtx`
- Client
    - I'm just using the port forwarding feature in VSCode to forward port 8000 & 8888 (may differ for you).