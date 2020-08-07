# ansible

## Pair bluetooth mouse
```bash
bluetoothctl
list
select XX:XX:XX:XX:XX:XX
power on
scan on
scan off
pair YY:YY:YY:YY:YY:YY
connect YY:YY:YY:YY:YY:YY
trust YY:YY:YY:YY:YY:YY
``

```bash
sudo ansible-pull -U https://github.com/MrSnyder/ansible.git
```

