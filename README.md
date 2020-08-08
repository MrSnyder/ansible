# Laptop installation

## Ubuntu
* Encrypt harddisk (LUKS)

## Fix audio device switching when plugging docking station
TODO

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

* Add extension "URL in title"

## Slack
```bash
snap-store.ubuntu-software --search slack
```

## Laptop tools
```bash
sudo apt install powertop
```

## VirtualBox
https://www.virtualbox.org/wiki/Linux_Downloads
```bash
sudo su -
echo "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian focal contrib" > /etc/apt/sources.list.d/virtualbox.list
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | apt-key add -
apt update
apt-cache policy virtualbox-6.1
apt install virtualbox-6.1
```

* Download extension pack: https://www.virtualbox.org/wiki/Downloads
* Install via UI (Einstellungen -> Zusatzpakete)
* Restore folder "VirtualBox VMs"
* Add Virtual Machine files via UI
* Datei -> Host-only Netzwerk Manager -> Erzeugen

```bash
# get usb devices to show up
sudo usermod -a -G vboxusers $USER
```

## KVM
```bash
sudo apt install -y qemu qemu-kvm libvirt-daemon bridge-utils virt-manager virtinst
sudo systemctl is-active libvirtd
sudo usermod -aG libvirt $USER
sudo usermod -aG kvm $USER
```
* Logout / Login from Gnome

## Install Windows 10 in KVM
https://dennisnotes.com/note/20180614-ubuntu-18.04-qemu-setup/
https://techpiezo.com/linux/shared-folder-in-qemu-virtual-machine-windows/

```bash
virt-xml win10 --edit --confirm --qemu-commandline '-net nic -net user,smb=/home/markus/.kvm-share'
```

## Ansible-Pull (not in use yet)
```bash
sudo ansible-pull -U https://github.com/MrSnyder/ansible.git
```

