### TAGS

alpine-arm, alpine, arm, latest

[![](https://images.microbadger.com/badges/image/yangxuan8282/create_ap.svg)](https://microbadger.com/images/yangxuan8282/create_ap "Get your own image badge on microbadger.com")

alpine-amd64, amd64

[![](https://images.microbadger.com/badges/image/yangxuan8282/create_ap:amd64.svg)](https://microbadger.com/images/yangxuan8282/create_ap:amd64 "Get your own image badge on microbadger.com")

debian-amd64

[![](https://images.microbadger.com/badges/image/yangxuan8282/create_ap:debian-amd64.svg)](https://microbadger.com/images/yangxuan8282/create_ap:debian-amd64 "Get your own image badge on microbadger.com")

### FROM

https://github.com/oblique/create_ap

### RUN

for arm ( tested on rpi3 built-in bcm43438 ):

```
docker run -d \
     --name ap \
     -e AP_SSID=pi  \
     -e AP_PASSPHRASE=RaspberryPi \
     --privileged --net host \
     yangxuan8282/create_ap
```

for amd64 ( should work ):

```
docker run -d \
     --name ap \
     -e AP_SSID=pi  \
     -e AP_PASSPHRASE=RaspberryPi \
     --privileged --net host \
     yangxuan8282/create_ap:amd64 
```

