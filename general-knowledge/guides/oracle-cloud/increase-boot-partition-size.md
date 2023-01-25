```bash
df -h
sudo su -
```

```bash
sudo dd iflag=direct if=/dev/<device_name> of=/dev/null count=1
		echo "1" | sudo tee /sys/class/block/<device_name>/device/rescan
```

```bash
growpart /dev/sda 1 
resize2fs /dev/sda1 

df -h
```