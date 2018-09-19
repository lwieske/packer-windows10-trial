# Packer-Windows10-Trial (Redstone 4 / April 2018)

Makes a Windows 10 x64 box for use with Virtualbox.

Inspired by so many other repositories on GitHub.

| Build	| Version | Codename | Date | Marketing Name |
|---:|---:|---|---|---|
|       |      | 19H2        |                 |                      |
|       |      | 19H1        |                 |                      |
|       | 1809 | Redstone 5  |                 | October 2018 Update  |
| **17134** | **1803** | **Redstone 4**  | **March 2018**      | **April 2018 Update**    |
| 16299 | 1709 | Redstone 3  | September 2017  | Fall Creators Update |
| 15063 | 1703 | Redstone 2  | March 2017      | Creators Update      |
| 14393	| 1607 | Redstone 1  | August 2016     |                      |
| 10586	| 1511 | Threshold 2 | November 2015   |                      |
| 10240	| 1507 | Threshold 1 | July 2015       |                      |


```
$ packer build -force -only=virtualbox-iso windows10-trial.json

$ vagrant box add --name windows10-trial builds/windows10-trial.virtualbox.box --force

$ vagrant init windows10-trial

$ vagrant up
```

This repository is based on **Redstone1 (RS1)** and the build does the following:

* Autonunattend.xml
  * update windows
  * enable winrm
* windows10.trial.json
  * restart windows
    * enables rdp
    * enables ssh
    * installs guest tools
  * restart windows
    * installs packages
    * does some tweaks
    * compacts the drive
