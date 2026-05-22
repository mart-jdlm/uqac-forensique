# Lab4


```
$ mmls multi1.dd
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000008191   0000006144   Linux (0x83)
003:  000:001   0000008192   0000012287   0000004096   Win95 FAT32 (0x0c)
004:  000:002   0000012288   0000014335   0000002048   Linux Swap / Solaris x86 (0x82)
005:  000:003   0000014336   0000019999   0000005664   Linux (0x83)

$ mmls multi2.dd
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000006143   0000004096   Win95 FAT32 (0x0c)
003:  Meta      0000006144   0000019999   0000013856   DOS Extended (0x05)
004:  Meta      0000006144   0000006144   0000000001   Extended Table (#1)
005:  -------   0000006144   0000008191   0000002048   Unallocated
006:  001:000   0000008192   0000010239   0000002048   Linux (0x83)
007:  Meta      0000010240   0000018431   0000008192   DOS Extended (0x05)
008:  Meta      0000010240   0000010240   0000000001   Extended Table (#2)
009:  -------   0000010240   0000012287   0000002048   Unallocated
010:  002:000   0000012288   0000018431   0000006144   Linux Swap / Solaris x86 (0x82)
011:  -------   0000018432   0000019999   0000001568   Unallocated
```

```
$ fls fileadded.dd
d/d 4:  dir101
v/v 3270387:    $MBR
v/v 3270388:    $FAT1
v/v 3270389:    $FAT2
V/V 3270390:    $OrphanFiles

$ fls fileadded.dd 4
r/r 582:        testprint
```

```
$ istat fileadded.dd 582
Directory Entry: 582
Allocated
File Attributes: File, Archive
Size: 6771
Name: TESTPR~1

Directory Entry Times:
Written:        2015-02-23 19:04:18 (UTC)
Accessed:       2015-02-23 00:00:00 (UTC)
Created:        2015-02-23 19:04:19 (UTC)

Sectors:
441 442 443 444 445 446 447 448
449 450 451 452 453 454 0 0
```

```
$ ./testprint.sl
-bash: ./testprint.sl: Permission denied
$ chmod +x testprint.sl
$ ./testprint.sl
Hello World!
$ sha256sum testprint.sl
577c8067b04b0d1d2b4501d52ef380a65a848279a645bca1105b5e7a79de19ba  testprint.sl
```

```
$ sha256sum testprint.2.sl
577c8067b04b0d1d2b4501d52ef380a65a848279a645bca1105b5e7a79de19ba  testprint.2.sl
```

```
$ blkcalc -f fat -u 4 filedeleted.dd
441
```

```
$ blkcat fileadded.dd 441 14 | head -c 6771 > testprint.carv.v2
```

```
$ head -c 445984 image.jpg > fichier_perdu.jpg
$ sha256sum fichier_perdu.jpg
cbd7f73a8c1b3d37cd3cecc6fc28bae333c753e95aaabf335eb942fc51757f52  fichier_perdu.jpg
``