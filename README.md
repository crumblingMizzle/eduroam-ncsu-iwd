# Eduroam at NCSU with IWD
### Info
This is a modified version of the SecureW2_JoinNow.run script that is normally downloaded from the [eduroam distribution page](https://cloud.securew2.com/public/12117/eduroam/).

The modifications stop the script from trying to connect to NetworkManager and instead generate an iwd config file for the eduroam connection. The best way to do this is to connect to ncsu-guest or a hotspot, download the script and run it, and then forget ncsu-guest/the hotspot. In theory iwd should recognize the config file as properly formed and the eduroam network should allow your device to connect.

Note that this is a hacky modification of the script that could very well not work in a few months and will only work for NCSU, no other institutions. Technical details: NCSU uses EAP-TLS while most other institutions use EAP-TTLS or EAP-PEAP + MSCHAPv2, which is why all the other eduroam iwd guides you've tried haven't worked :)

### Usage
```
git clone https://github.com/crumblingMizzle/eduroam-ncsu-iwd
cd eduroam-ncsu-iwd
chmod +x SecureW2_JoinNow.run
./SecureW2_JoinNow.run
```
