# Rancher OS

### Cloud-init example config for `Rancher OS`.

Install Rancher OS with cloud-init config file.
Do not restart automatically after installation. Shutdown the machine and disconnect the ISO after stop.

```bash
$ sudo mkfs.ext4 -L RANCHER_STATE /dev/sda
$ sudo reboot
$ sudo ros install -c https://raw.githubusercontent.com/li_zhixin/rancheros/main/cloud-config.yml -d /dev/sda -a rancher.password=rancher
$ sudo halt
```

