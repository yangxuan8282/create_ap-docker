FROM debian

COPY create_ap /usr/bin/
COPY create_ap.conf /etc/

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
	bash hostapd iproute2 iw dnsmasq iptables \
  && rm -rf /var/lib/apt/lists/*

ENV AP_WIFI_IFACE=wlan0 AP_INTERNET_IFACE=eth0 AP_SSID=MyAccessPoint AP_PASSPHRASE=MyPassPhrase 

COPY run_create_ap /usr/bin/
CMD ["/usr/bin/run_create_ap"]
