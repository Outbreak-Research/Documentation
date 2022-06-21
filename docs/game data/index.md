# Game Data 

This sections describes how are data mapped from disc files into memory and what these memory structures contain.

## Main Characters(MCs) and other NPCs

### MCs model scaling data

Every 12 bytes is 1 MC and every 4 bytes float define scaling along 1 axis:

- X-axis 4 bytes float
- Y-axis 4 bytes float
- Z-axis 4 bytes float

#### File #1

??? info
    - Author > [Machi](https://github.com/Machi13)
    - Last update > 19 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 22 June 2022

```
File > GAME.BIN
Start > 001A6CB0
End > 001A6D0DF
```

```
Offset 00-03 > Scaling multiplier along X axis
Offset 04-07 > Scaling multiplier along Z axis
Offset 08-0B > Scaling multiplier along Y axis
```

```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
001A6CB0  66 66 86 3F 66 66 86 3F 66 66 86 3F CD CC 8C 3F  ff†?ff†?ff†?ÍÌŒ?
001A6CC0  CD CC 8C 3F CD CC 8C 3F AE 47 81 3F AE 47 81 3F  ÍÌŒ?ÍÌŒ?®G.?®G.?
001A6CD0  AE 47 81 3F 5C 8F 82 3F 5C 8F 82 3F 5C 8F 82 3F  ®G.?\.‚?\.‚?\.‚?
001A6CE0  14 AE 87 3F 14 AE 87 3F 14 AE 87 3F 5C 8F 82 3F  .®‡?.®‡?.®‡?\.‚?
001A6CF0  5C 8F 82 3F 5C 8F 82 3F 33 33 73 3F 33 33 73 3F  \.‚?\.‚?33s?33s?
001A6D00  33 33 73 3F AE 47 81 3F AE 47 81 3F AE 47 81 3F  33s?®G.?®G.?®G.?
---------------------------------------------------------------------------
```

#### File #2

??? info
    - Author > [Machi](https://github.com/Machi13)
    - Last update > 19 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 22 June 2022

```
Location > 2.DAT
Start > 001E5540
End > 0001E559F
```

```
Offset 00-03 > Scaling multiplier along X axis
Offset 04-07 > Scaling multiplier along Z axis
Offset 08-0B > Scaling multiplier along Y axis
```

```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
001E5540  66 66 86 3F 66 66 86 3F 66 66 86 3F CD CC 8C 3F  ff†?ff†?ff†?ÍÌŒ?
001E5550  CD CC 8C 3F CD CC 8C 3F AE 47 81 3F AE 47 81 3F  ÍÌŒ?ÍÌŒ?®G.?®G.?
001E5560  AE 47 81 3F 5C 8F 82 3F 5C 8F 82 3F 5C 8F 82 3F  ®G.?\.‚?\.‚?\.‚?
001E5570  14 AE 87 3F 14 AE 87 3F 14 AE 87 3F 5C 8F 82 3F  .®‡?.®‡?.®‡?\.‚?
001E5580  5C 8F 82 3F 5C 8F 82 3F 33 33 73 3F 33 33 73 3F  \.‚?\.‚?33s?33s?
001E5590  33 33 73 3F AE 47 81 3F AE 47 81 3F AE 47 81 3F  33s?®G.?®G.?®G.?
---------------------------------------------------------------------------
```