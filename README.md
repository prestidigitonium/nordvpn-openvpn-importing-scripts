# nordvpn-ovpn-importing-scripts

### Description
Two scripts capable of downloading all ovpn configurations from NordVpn website and add them in network manager, automatically, with credentials.

`download-configs.sh`

- downloads all .ovpn configurations in a folder (`OVPN_PATH` variable) and keeps TCP configs only
- remove old configurations from the folder

![import](https://i.postimg.cc/LHtnL4H6/import.png)

---

`import-configs.sh`

- import all .ovpn configurations from a folder (`OVPN_PATH` variable) to networkmanger
- randomize which configuration will be imported, up to a theshold (`limit` variable). Default is 3 randomized configurations for uk, it, de, fr, jp, us, nl countries
- import username and password to all configurations (`USERNAME`, `PASSWORD` variables)
- add settings in order to not leak DNS using openvpn

![imported](https://i.postimg.cc/MW2nnfJF/imported.png)
