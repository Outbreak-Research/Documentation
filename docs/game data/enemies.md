## Enemies

### Enemy respawn points

??? info "Authors metadata"
    - Authors > hill73n, IgusaTaro, Zuko
    - Last update > 10 April 2021
    - Last modification > [Bia10](https://github.com/Bia10) at 1 July 2022

General path to enemy respawn points data:

- NETBIO00.DAT > [r0xx.afs] > r0xx.epp

#### Header

- 4 bytes roomID
- 4 bytes offset
- 8 bytes terminator FF

```
Example header of r40.epp (Wild Things)

Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000000  01 00 00 00 40 00 00 00 02 00 00 00 68 00 00 00  ....@.......h...
00000010  03 00 00 00 7C 00 00 00 06 00 00 00 A4 00 00 00  ....|.......¤...
00000020  0E 00 00 00 CC 00 00 00 12 00 00 00 E0 00 00 00  ....Ì.......à...
00000030  13 00 00 00 F4 00 00 00 FF FF FF FF FF FF FF FF  ....ô...ÿÿÿÿÿÿÿÿ
---------------------------------------------------------------------------

We can see:
- Room 01 respawn data begin at offset 40
- Room 02 respawn data begin at offset 68
- Room 03 respawn data begin at offset 7C
- Room 06 respawn data begin at offset A4
- Room 0E respawn data begin at offset CC
- Room 12 respawn data begin at offset E0
- Room 13 respawn data begin at offset F4

At offset 38 header terminates.
```

### Enemy route tracking points

### Enemy characteristics