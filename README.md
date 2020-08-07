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

## Dropbox
https://linuxconfig.org/ubuntu-20-04-dropbox-installation-and-desktop-integration

```bash
snap-store.ubuntu-software --search dropbox
# Install
# Start Dropbox
# Login
```

## KVM
```
sudo apt install -y qemu qemu-kvm libvirt-daemon bridge-utils virt-manager virtinst
sudo systemctl is-active libvirtd
sudo usermod -aG libvirt $USER
sudo usermod -aG kvm $USER
```
* Logout / Login from Gnome


## Ansible-Pull (not in use...yet)
```bash
sudo ansible-pull -U https://github.com/MrSnyder/ansible.git
```

