# Laptop installation

## Ubuntu
* Encrypt harddisk (LUKS)

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

## KeepassXC
```bash
sudo add-apt-repository ppa:phoerious/keepassxc
sudo apt update
sudo apt install keepassxc
```
* Launch KeepassXC
* Add to favorites
* Einstellungen -> Auto-Type: Strg+Umschalt+P

## Transfer secure keys from USB
* .ssh
* .keys

## Synology Drive Client
https://www.synology.com/de-de/support/download/DS216+#utilities
```bash
sudo dpkg --install synology-drive-client-11078.x86_64.deb
```
* Launch Synology Drive Client

## Dropbox
https://linuxconfig.org/ubuntu-20-04-dropbox-installation-and-desktop-integration

```bash
snap-store.ubuntu-software --search dropbox
# Install
# Start Dropbox
# Login
```

## Chrome
```bash
sudo apt install gdebi-core
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo gdebi google-chrome-stable_current_amd64.deb
```

## Slack
```bash
snap-store.ubuntu-software --search slack
```

## KVM
```
sudo apt install -y qemu qemu-kvm libvirt-daemon bridge-utils virt-manager virtinst
sudo systemctl is-active libvirtd
sudo usermod -aG libvirt $USER
sudo usermod -aG kvm $USER
```
* Logout / Login from Gnome

## Convert VirtualBox Windows 10 VM to KVM
http://blog.it-concepts.de/2019/08/migration-von-windows-10-virtualbox-guest-nach-kvm/?lang=en
https://techpiezo.com/linux/shared-folder-in-qemu-virtual-machine-windows/
```bash
qemu-img convert -f vdi -O qcow2 Windows10.vdi ~/tmp/Windows10.qcow2
```

## Laptop tools
```bash
sudo apt install powertop
```

## Ansible-Pull (not in use yet)
```bash
sudo ansible-pull -U https://github.com/MrSnyder/ansible.git
```

