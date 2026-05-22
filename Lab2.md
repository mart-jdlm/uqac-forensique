# Lab2



##### Partition 1

**000001be: 8020 2100 0c61 2100 0008 0000 0010 0000**

###### bootable flag

* Hex : 80
* Dec : 128

###### System ID

* Hex : 0c
* Type : FAT32 with LBA

###### RelSec

* Hex : 0x00000800
* Dec : 2048

###### PartLength

* Hex : 0x00001000
* Dec : 4096



##### Partition 2\*

**000001ce: 0061 2200 053e 1d01 0018 0000 2036 0000**

###### bootable flag

* Hex : 00
* Dec : 0

###### System ID

* Hex : 05
* Type : Extended partition

###### RelSec

* Hex : 0x00001800
* Dec : 6144

###### PartLength

* Hex : 0x00003620
* Dec : 13856



##### Partition 3

**003001be: 0082 0300 83a2 2200 0008 0000 0008 0000**

###### bootable flag

* Hex : 00
* Dec : 0

###### System ID

* Hex : 83
* Type : Linux

###### RelSec

* Hex : 0x00000800
* Dec : 2048

###### PartLength

* Hex : 0x00000800
* Dec : 2048



##### Partition 4\*

**003001ce: 00a2 2300 0525 2401 0010 0000 0020 0000**

###### bootable flag

* Hex : 00
* Dec : 0

###### System ID

* Hex : 05
* Type : Extended partition

###### RelSec

* Hex : 0x00001000
* Dec : 4096

###### PartLength

* Hex : 0x00002000
* Dec : 8192



##### Partition 6

**005001be: 00c3 0400 8225 2401 0008 0000 0018 0000**

###### bootable flag

* Hex : 00
* Dec : 0

###### System ID

* Hex : 82
* Type : Linux swap space / GNU/Hurd / Solaris x86

###### RelSec

* Hex : 0x00000800
* Dec : 2048

###### PartLength

* Hex : 0x00001800
* Dec : 6144
