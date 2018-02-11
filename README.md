# mediakit

MediaKit reports not enough disk space

On High Sierra - Drop to terminal:

diskutil list

diskutil unmountDisk force disk3

sudo dd if=/dev/zero of=/dev/rdisk3 bs=1024 count=1024

diskutil partitionDisk disk3 GPT JHFS+ "bluedisk" 0g

NOTE: 
disk3 is an example of (external, physical)
# Bluedisk is an example of the disk label I used
