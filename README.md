# Laptop installation

## KeepassXC
```bash
sudo add-apt-repository ppa:phoerious/keepassxc
sudo apt update
sudo apt install keepassxc
```

* Launch KeepassXC
* Add to favorites
* Einstellungen -> Auto-Type: Strg+Umschalt+P


## Bluetooth mouse
```bash
bluetoothctl
list
select XX:XX:XX:XX:XX:XX
power on
# put mouse in discovery mode before this
scan on
scan off
pair YY:YY:YY:YY:YY:YY
connect YY:YY:YY:YY:YY:YY
trust YY:YY:YY:YY:YY:YY
```

## Dropbox
https://linuxconfig.org/ubuntu-20-04-dropbox-installation-and-desktop-integration

```bash
snap-store.ubuntu-software --search dropbox
# Install
# Start Dropbox
# Login
```


```bash
sudo ansible-pull -U https://github.com/MrSnyder/ansible.git
```

