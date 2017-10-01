






# RUN
```bash
git clone 
docker-compose build
docker-compose up
```
## See HLS Content
Uncomment HTL configuration below lines and if you want to see from localhost:8080/index.html

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
### OBS

### Android

## Subscriber

### Wowza RTMP Test Player
> https://www.wowza.com/testplayers
### Android
> Use [Vitamio](https://github.com/yixia/VitamioBundle) Video View to display 


# Nginx RTMP Module Configuration
https://github.com/arut/nginx-rtmp-module/wiki/Directives


# TODO
- [ ] (Need study) Use WebRTC's codec to streaming to RTMP server which we can make react-native-webrtc to unify the client platform.


# Protochol related

## Latency comparsion between RTMP/HLS/DASH/WebRTC

https://www.nanocosmos.de/blog/2017/05/interactive-live-streaming-with-ultra-low-latency-2/

## RTMP Latency

https://github.com/arut/nginx-rtmp-module/issues/962

## HLS Latency
- Decrease the video bitrate of client side can shorten latency

## DASH v.s HLS

> https://stackoverflow.com/questions/15687434/what-is-the-difference-between-hls-and-mpeg-dash


## References

https://obsproject.com/forum/resources/how-to-set-up-your-own-private-rtmp-server-using-nginx.50/
