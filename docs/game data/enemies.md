## Enemies

### Enemy respawn points

??? info "Authors metadata"
    - Authors > hill73n, IgusaTaro, Zuko
    - Last update > 10 April 2021
    - Last modification > [Bia10](https://github.com/Bia10) at 1 July 2022

General path to enemy respawn points data:

- NETBIO00.DAT > [r0xx.afs] > r0xx.epp

#### Header

Size of the header varies depending on the number of rooms included.

For each room we have:

- 4 bytes roomID
- 4 bytes offset

Once room data ends:

- 8 bytes terminator FF

So the total size of header is n x 8 bytes + 8 bytes.

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

Each respawn data chunk can contain one or more positions.

#### Respawn point data

Structure is not yet completely understood!

Each spawn location represented by 20 bytes of data:

- 4 bytes unknown, (seems to affect enemy type somehow. Edit: Actually, i think it indicates door ID where a zombie or hunter respawns)
- 4 bytes int representing X coordinate data
- 4 bytes int representing Z coordinate data
- 4 bytes int representing Y coordinate data
- 4 bytes int unknown, seems always 00 00 00 00 a terminator ??


#### Example respawn points of r40.epp (Wild Things)

- Room 01 (Elephant Restaurant)
```
Spawn location 00-00
---------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000040  00 01 00 40 7F 33 00 00 4E 00 00 00 6D 39 00 00  ...@.3..N...m9..
00000050  00 00 00 00 
---------------------------------------------------------------------------

Spawn location 00-01
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                      00 01 00 40 72 33 00 00 55 00 00 00  .......@r3..U...
00000060  73 39 00 00 00 00 00 00 
---------------------------------------------------------------------------
```

- Room 02 (Back Alley)
```
Spawn location 01-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                  00 01 00 40 11 33 00 00  s9.........@.3..
00000070  0C 00 00 00 23 34 00 00 00 00 00 00 
```


### Enemy route tracking points
### Enemy characteristics