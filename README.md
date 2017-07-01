### TAGS

alpine-arm, alpine, arm, latest

debian-arm, debian

alpine-amd64, amd64

debian-amd64

### FROM

https://github.com/oblique/create_ap

### RUN

for arm ( tested on rpi3 built-in bcm43438 ):

```
docker run -d \
     --name ap \
     -e AP_SSID=pi  \
     -e AP_PASSPHRASE=RaspberryPi \
     --privileged --net host local/ss_ap \
     yangxuan8282/create_ap
```

for amd64 ( should work ):

```
docker run -d \
     --name ap \
     -e AP_SSID=pi  \
     -e AP_PASSPHRASE=RaspberryPi \
     --privileged --net host local/ss_ap \
     yangxuan8282/create_ap:amd64 
```

