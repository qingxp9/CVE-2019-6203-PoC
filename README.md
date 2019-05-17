# CVE-2019-6203-PoC
There is a PEAP bug in all Apple devices that would allow an attacker to force any Apple device (iOS, macOS or tvOS) to associate with a malicious access point.

This is a PoC for CVE-2019-6203, works on < iOS 12.2, macOS < 10.14.4, tested on Kali Linux.

You need a Wi-Fi card that supports **AP mode** to run this PoC. You can check this by running ```iw list```, outputs like:
```
Supported interface modes:
	 * IBSS
	 * managed
	 * AP
	 * AP/VLAN
	 * monitor
	 * mesh point
```

## Usage
```
apt install hostapd-wpe dnsmasq
git clone https://github.com/qingxp9/CVE-2019-6203-PoC
cd CVE-2019-6203-PoC
python CVE-2019-6203-PoC.py -i wlan0

#with Internet
python CVE-2019-6203-PoC.py -i wlan0 -o eth0
```

## Reference
- https://sensepost.com/blog/2019/understanding-peap-in-depth/
- https://www.freebuf.com/vuls/203484.html

video: https://youtu.be/UEzdtkcnrYw

