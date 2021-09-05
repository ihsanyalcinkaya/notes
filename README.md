## Notes to myself

### Displaylink on Ubuntu 20.04
Sometimes the kernel release and the evdi release, that is in the displaylink driver, do not match. Therefore, displaylink does not work on Ubuntu. In this case;  

1- Remove the displaylink driver. [link](https://support.displaylink.com/knowledgebase/articles/683699-how-to-uninstall-displaylink-ubuntu-software)
```
sudo displaylink-installer uninstall
```

2- Evdi should be manually removed. Note that, version of evdi might be different.
```
sudo dkms remove evdi/1.9.1 --all 
```

3- Install displaylink with a evdi with a compatible version. See the [link](https://www.displaylink.org/forum/showpost.php?p=92453&postcount=3). This is based on [porting the displaylink](https://support.displaylink.com/knowledgebase/articles/679060-porting-the-displaylink-ubuntu-driver-to-other-lin) manual.

### Set headset as default sound output on Ubuntu 20.04
```
pactl set-default-sink alsa_output.pci-0000_00_1f.3.analog-stereo
```
***Remark:*** Add this to ~/.profile file.

