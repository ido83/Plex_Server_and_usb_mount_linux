# Plex_Server_and_usb_mount_linux
TBD

# Mount usb drive in ubuntu
1. Find what the drive is called
```
lsblk
sudo blkid
sudo fdisk -l
```
2. Create a mount point
```
sudo  mkdir /media/usb
```
3. Mount!
```
   sudo mount /dev/sdb1 /media/usb
   if need to unmount do:
   sudo umount /media/usb
```
4. Get Drive UUID and Type
   ```
   lsblk -o NAME,FSTYPE,UUID,MOUNTPOINTS
   ```
5. Edit fstab
   ```
   sudo nano /etc/fstab
   ```
6. Set mount point (updated UUID and path)
```
UUID=632D-7154 /media/USB1   exfat    defaults        0       0
```
7. before restart Test fstab
```
sudo findmnt --verify
```
8. Restart Ubuntu Server / Linux OS
 ```
sudo reboot
  ```
9. Test the Mount Point
```
lsblk -o NAME,FSTYPE,UUID,MOUNTPOINTS
```
