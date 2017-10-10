
RUN
---
```bash
git clone 
docker-compose build
docker-compose up
```
Comment following line in ```nginx.conf``` if you want to publish without validating with your app server
```
on_publish http://docker.for.mac.localhost:10010/hooks/publish/start; //use docker.for.mac.localhost to communicate to localhost outside container
on_publish_done http://docker.for.mac.localhost:10010/hooks/publish/start/stop;

```
See HLS Content
---
Uncomment HTL configuration in nginx.conf  below lines and re-type ```docker-compose up```and you can see content in localhost:8080/index.html

```
    #hls on;
    #hls_path /etc/nginx/hls/;
    #hls_fragment 3;
    #hls_playlist_length 60;
```

## See RTMP Content
Use one of following Live streaming subscriber to see the streaming content from RTMP

# Live streaming publisher and subscribers

rtmp://[host_name]/live/[stream_name]

## Publisher
[OBS](https://obsproject.com/)
[Android](https://github.com/begeekmyfriend/yasea)

## Subscriber

[Wowza RTMP Test Player](https://www.wowza.com/testplayers)

[Vitamio for Android](https://github.com/yixia/VitamioBundle)


# Nginx RTMP Module Configuration
https://github.com/arut/nginx-rtmp-module/wiki/Directives


# TODO
- [ ] (Need study) Use WebRTC's codec to streaming to RTMP server which we can make react-native-webrtc to unify the client platform.

# Protochol related

[Latency comparsion among RTMP/HLS/DASH/WebRTC](https://www.nanocosmos.de/blog/2017/05/interactive-live-streaming-with-ultra-low-latency-2/)

[RTMP Latency](https://github.com/arut/nginx-rtmp-module/issues/962)


[HLS Latency]()


[DASH v.s HLS](https://stackoverflow.com/questions/15687434/what-is-the-difference-between-hls-and-mpeg-dash)


## References

https://obsproject.com/forum/resources/how-to-set-up-your-own-private-rtmp-server-using-nginx.50/
