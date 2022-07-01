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
Each respawn data chunk (room) can contain one or more positions.

For each room we have:

- 4 bytes roomID
- 4 bytes offset

Once room data ends:

- 8 bytes terminator FF

So the total size of header is n x 8 bytes + 8 bytes.

#### Example header of r40.epp (Wild Things)
```
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

#### Respawn point data

Structure is not yet completely understood!

Each spawn location represented by 20 bytes of data:

- 4 bytes unknown (seems to affect enemy type somehow. Edit: Actually, i think it indicates door ID where a zombie or hunter respawns)
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
---------------------------------------------------------------------------
```

- Room 03 (In front of Elephant Restaurant)
```
Spawn location 02-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                              01 00 00 94  ....#4.........”
00000080  74 33 00 00 26 00 00 00 68 2D 00 00 00 00 00 00  t3..&...h-......
---------------------------------------------------------------------------

Spawn location 02-01
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000090  00 00 00 BD D9 33 00 00 54 00 00 00 66 39 00 00  ...½Ù3..T...f9..
000000A0  00 00 00 00
---------------------------------------------------------------------------
```

- Room 06 (North Concourse)
```
Spawn location 03-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                      00 00 00 F5 CC 25 00 00 5D 00 00 00  .......õÌ%..]...
000000B0  6E 19 00 00 00 00 00 00 
---------------------------------------------------------------------------

Spawn location 03-01
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                  00 00 00 3E 4E 17 00 00  n..........>N...
000000C0  00 00 00 00 EF 19 00 00 00 00 00 00 
---------------------------------------------------------------------------
```

- Room 0E (Connecting Passage)
```
Spawn location 04-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                              00 00 00 7E  ....ï..........~
000000D0  B5 24 00 00 2C 01 00 00 FC 13 00 00 00 00 00 00  µ$..,...ü.......
---------------------------------------------------------------------------
```

- Room 12 (Lakeside)
```
Spawn location 05-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
000000E0  00 00 00 80 EF 16 00 00 94 00 00 00 81 13 00 00  ...€ï...”.......
000000F0  00 00 00 00
---------------------------------------------------------------------------
```

- Room 13 (Path in front of Observation Deck)
```
Spawn location 06-00
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                      00 00 00 00 4C 19 00 00 B4 00 00 00  ........L...´...
00000100  21 16 00 00 00 00 00 00 
---------------------------------------------------------------------------

Spawn location 06-01
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                  00 00 00 83 AC 10 00 00  !..........ƒ¬...
00000110  C8 00 00 00 AA 19 00 00 00 00 00 00 
---------------------------------------------------------------------------

Spawn location 06-02
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
                                              00 00 00 F2  È...ª..........ò
00000120  5E 19 00 00 43 00 00 00 99 16 00 00 00 00 00 00  ^...C...™.......
---------------------------------------------------------------------------

Spawn location 06-03
--------------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000130  00 00 00 4C 2E 0F 00 00 32 00 00 00 A4 18 00 00  ...L....2...¤...
00000140  00 00 00 00                                      ....
---------------------------------------------------------------------------
```
### Enemy route tracking points

??? info "Authors metadata"
    - Authors > hill73n, IgusaTaro, dchaps
    - Last update > 15 August 2021
    - Last modification > [Bia10](https://github.com/Bia10) at 1 July 2022

General path to enemy route tracking points data:

- NETBIO00.DAT > [r0xx.afs] > r0xx.rtp

#### Header

Size of the header varies depending on the number of rooms included.

- 4 bytes number of rooms (roomCnt)

Depending on the number of rooms we have

- 2 bytes short for each room IDs

then 

- 2 bytes offset for each tracking route

Size of the header is 4 + (2 x roomCnt) + (2 x roomCnt) = 4 + (4x roomCnt)

#### Example header of r40.rtp (Wild Things)
```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000000  07 00 00 00 00 01 00 03 00 04 01 04 00 05 00 06  ................
00000010  00 0C 00 00 64 00 EC 00 80 01 14 02 8C 02 F0 02  ....d.ì.€...Œ.ð.
---------------------------------------------------------------------------

We can see:
- Room count 07 00 00 

- 00 01	Elephant Restaurant
- 00 03	In Front of Elephant Restaurant
- 00 04	South Concourse (before Titan Enters cutscene)
- 01 04	South Concourse (after Titan Enters cutscene)
- 00 05	East Concourse
- 00 06	North Concourse
- 00 0C	Elephant Stage

- 00 00 Tracking route offset 00
- 64 00 Tracking route offset 01
- EC 00 Tracking route offset 02
- 80 01 Tracking route offset 03
- 14 02 Tracking route offset 04
- 8C 02 Tracking route offset 05
- F0 02	Tracking route offset 06

At offset 1F header terminates.
```

#### Example route data of r40.rtp (Wild Things)

General outline of tracking route:

- 4 bytes tracking route data set quantity
- 4 bytes tracking route sequence quantity

for each route data set 

- 4 bytes route start offset

for each route sequence

- 4 bytes route sequence offset

for each route data set

- 4 bytes position X
- 4 bytes position Y
- 4 bytes position Z

after route data sets, sequence beings:

- 1 byte source room
- 1 byte destination room
- 1 byte sequence steps quantity

for each sequence step

- 1 byte associating them to the route data set

```
Tracking Route 0
----------------
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000020  05 00 00 00 01 00 00 00 20 00 00 00 2C 00 00 00  ........ ...,...
00000030  38 00 00 00 44 00 00 00 50 00 00 00 5C 00 00 00  8...D...P...\...
00000040  00 18 51 46 00 80 A7 42 00 94 66 46 00 44 52 46  ..QF.€§B.”fF.DRF
00000050  00 80 A7 42 00 84 6A 46 00 D4 5C 46 00 80 A7 42  .€§B.„jF.Ô\F.€§B
00000060  00 04 68 46 00 50 59 46 00 80 A7 42 00 F0 62 46  ..hF.PYF.€§B.ðbF
00000070  00 48 51 46 00 80 A7 42 00 90 64 46 03 03 05 00  .HQF.€§B..dF....
00000080  01 02 03 04
---------------------------------------------------------------------------

Using the above we can see:

Start address of first tracking route (TROFF_00) = HeaderBytes + TROFF_00 = 4 + (4 x 07) + 0x0000 = 0x0020
Tracking Route Data Set Quantity (TRDSQ) = 05 00 00 00 = 5 route data sets
Route Sequence Quantity (RSQ) = 01 00 00 00 = 1 sequence

Since there are 5 route data sets there are 5 offsets:

RDOFF_00 = 20 00 00 00
RDOFF_01 = 2C 00 00 00
RDOFF_02 = 38 00 00 00
RDOFF_03 = 44 00 00 00
RDOFF_04 = 50 00 00 00

Tracking Route Data Sets (TRDS):

TRDS_00_Address = TROFF_00 + RDOFF_00 = 0x0020 + 20 00 00 00
TRDS_00_X = 00 18 51 46 = 13382
TRDS_00_Y = 00 80 A7 42 = 83.75
TRDS_00_Z = 00 94 66 46 = 14757

TRDS_01_Address = TROFF_00 + RDOFF_01 = 0x0020 + 2C 00 00 00
TRDS_01_X = 00 44 52 46 = 13457
TRDS_01_Y = 00 80 A7 42 = 83.75
TRDS_01_Z = 00 84 6A 46 = 15009

TRDS_02_Address = TROFF_00 + RDOFF_02 = 0x0020 + 38 00 00 00
TRDS_02_X = 00 D4 5C 46 = 14133
TRDS_02_Y = 00 80 A7 42 = 83.75
TRDS_02_Z = 00 04 68 46 = 14849

TRDS_03_Address = TROFF_00 + RDOFF_03 = 0x0020 + 44 00 00 00
TRDS_03_X = 00 D4 5C 46 = 14133
TRDS_03_Y = 00 80 A7 42 = 83.75
TRDS_03_Z = 00 04 68 46 = 14849

TRDS_04_Address = TROFF_00 + RDOFF_04 = 0x0020 + 50 00 00 00
TRDS_04_X = 00 48 51 46 = 13394
TRDS_04_Y = 00 80 A7 42 = 83.75
TRDS_04_Z = 00 90 64 46 = 14628

Since there is 1 route sequence there is 1 offset:

RSOFF_00 = 5C 00 00 00

Route Sequence (RS):

RS_00_Address = TROFF_00 + RSOFF_00 = 0x0020 + 5C 00 00 00
Source Room ID (SRID_00) = 03
Destination Room ID (DRID_00) = 03
Sequence Steps Quantity (SSQ_00) = 05
Sequence Step 00 (SS_0_00) = TRDS_00
Sequence Step 01 (SS_0_01) = TRDS_01
Sequence Step 02 (SS_0_02) = TRDS_02
Sequence Step 03 (SS_0_03) = TRDS_03
Sequence Step 04 (SS_0_04) = TRDS_04
```

### Enemy characteristics