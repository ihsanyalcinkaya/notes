## Notes to myself

### Displaylink on Ubuntu
Sometimes kernel releases and evdi releases do not match. Therefore, displaylink does not work on Ubuntu. In this case; 
1- Remove the displaylink driver. [link](https://support.displaylink.com/knowledgebase/articles/683699-how-to-uninstall-displaylink-ubuntu-software)
```
sudo displaylink-installer uninstall
```

2- Evdi should be manually removed. Note that, version of evdi might be different.
```
sudo dkms remove evdi/1.9.1 --all 
```

3- Install displaylink with a evdi with a compatible version. See the [link](https://www.displaylink.org/forum/showpost.php?p=92453&postcount=3). This is based on [porting the displaylink](https://support.displaylink.com/knowledgebase/articles/679060-porting-the-displaylink-ubuntu-driver-to-other-lin) manual.

