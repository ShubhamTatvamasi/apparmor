# apparmor

Check the status of apparmor:
```bash
sudo systemctl status apparmor
```

Check all the loaded profiles:
```bash
sudo aa-status
```

Install `aa-genprof` and other utility packages:
```bash
sudo apt install apparmor-utils
```

Generate a profile for `nano` text editor: 
```bash
sudo aa-genprof nano
```

Restart apparmor to load the profile:
```bash
sudo systemctl restart apparmor
```

Disable `nano` profile:
```bash
sudo ln -s /etc/apparmor.d/usr.bin.nano /etc/apparmor.d/disable/usr.bin.nano
```

Enable `nano` profile:
```bash
sudo rm /etc/apparmor.d/disable/usr.bin.nano
```

Reload apparmor config to kernal:
```bash
sudo apparmor_parser -r /etc/apparmor.d/usr.bin.nano
```

Remove the `nano` profile:
```bash
sudo apparmor_parser -R /etc/apparmor.d/usr.bin.nano
```

