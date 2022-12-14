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

Remove the `nano` profile:
```bash
sudo apparmor_parser -R /etc/apparmor.d/usr.bin.nano
```


