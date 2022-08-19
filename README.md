# simple zero disk eraser
Writes zeros to the free space of the disk to create disk images with efficient compression.
```sh
dd if=/dev/zero of=zero.small.file bs=1024 count=102400
cat /dev/zero > zero.file
sync
rm zero.small.file
rm zero.file
```
to see evolution of the space : 
```sh
watch -d -n 1 df -h
```
