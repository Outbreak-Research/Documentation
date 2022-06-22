## Main Characters(MCs) and other NPCs


### NPCs data

Every 12 bytes describes one NPC data.

#### File #1

??? info
    - Author > [Machi](https://github.com/Machi13)
    - Last update > 19 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 22 June 2022

```
File > SUBMAIN.BIN
Start > 00018F00
End > 00019337
```

```
Offset 00-01 > Model ID
Offset 02 > Main character type
Offset 03 > Pointer into HP range table
Offset 04 > Starting condition (Fine, Danger)
Offset 05 > Pointer into virus gauge increment multiplier table
Offset 06 > Pointer into animation speed table
Offset 07 > ??? 
Offset 08-0B > Attack power multiplier
```

```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00018F00  00 00 03 03 00 03 04 00 CD CC 8C 3F 01 00 04 04  ........ÍÌŒ?....
00018F10  00 01 02 00 3D 0A 97 3F 02 00 00 02 00 03 03 00  ....=.—?........
00018F20  00 00 80 3F 03 00 00 03 00 04 03 00 66 66 A6 3F  ..€?........ff¦?
00018F30  04 00 00 05 00 04 02 00 66 66 A6 3F 05 00 00 03  ........ff¦?....
00018F40  00 03 03 00 66 66 86 3F 07 00 00 04 00 04 03 00  ....ff†?........
00018F50  CD CC 8C 3F 09 00 01 05 00 03 01 00 F6 28 9C 3F  ÍÌŒ?........ö(œ?
00018F60  0A 00 03 02 00 03 03 00 EC 51 78 3F 0B 00 00 03  ........ìQx?....
00018F70  00 04 03 00 85 EB 51 3F 0C 00 03 03 01 04 03 00  ....…ëQ?........
00018F80  66 66 66 3F 10 00 02 03 00 01 02 00 3D 0A 97 3F  fff?........=.—?
00018F90  11 00 01 03 00 04 04 00 00 00 80 3F 12 00 03 02  ..........€?....
00018FA0  00 03 03 00 00 00 80 3F 13 00 02 03 01 03 03 00  ......€?........
00018FB0  E1 7A 54 3F 15 00 02 04 00 02 02 00 1F 85 6B 3F  ázT?.........…k?
00018FC0  16 00 01 04 01 04 02 00 C3 F5 68 3F 18 00 03 03  ........Ãõh?....
00018FD0  00 03 04 00 00 00 80 3F 19 00 04 03 00 03 03 00  ......€?........
00018FE0  33 33 73 3F 1A 00 01 03 00 03 03 00 AE 47 61 3F  33s?........®Ga?
00018FF0  1B 00 01 04 00 02 04 00 CD CC 8C 3F 1C 00 00 02  ........ÍÌŒ?....
00019000  00 04 03 00 00 00 80 3F 1D 00 01 05 01 04 02 00  ......€?........
00019010  48 E1 7A 3F 1F 00 04 03 00 02 03 00 29 5C 8F 3F  Ház?........)\.?
00019020  20 00 02 04 00 03 04 00 3D 0A 97 3F 22 00 02 02   .......=.—?"...
00019030  00 04 04 00 EC 51 78 3F 24 00 04 03 00 03 03 00  ....ìQx?$.......
00019040  00 00 80 3F 26 00 03 03 00 02 02 00 1F 85 6B 3F  ..€?&........…k?
00019050  27 00 03 06 00 02 03 00 9A 99 59 3F 28 00 03 04  '.......š™Y?(...
00019060  00 02 01 00 8F C2 75 3F 29 00 03 03 00 03 03 00  .....Âu?).......
00019070  00 00 80 3F 2A 00 03 01 00 02 03 00 52 B8 5E 3F  ..€?*.......R¸^?
00019080  2B 00 03 03 00 01 02 00 A4 70 7D 3F 2C 00 03 04  +.......¤p}?,...
00019090  00 03 03 00 00 00 80 3F 2E 00 02 02 00 03 02 00  ......€?........
000190A0  7B 14 6E 3F 2F 00 03 03 00 03 03 00 52 B8 5E 3F  {.n?/.......R¸^?
000190B0  30 00 04 05 00 04 03 00 D7 A3 B0 3F 31 00 00 02  0.......×£°?1...
000190C0  00 02 03 00 85 EB 91 3F 32 00 04 03 00 03 03 00  ....…ë‘?2.......
000190D0  C3 F5 88 3F 34 00 05 03 00 02 03 00 00 00 80 3F  Ãõˆ?4.........€?
000190E0  35 00 06 03 01 06 03 00 85 EB 51 3F 36 00 05 02  5.......…ëQ?6...
000190F0  00 02 03 00 48 E1 7A 3F 37 00 07 02 00 03 03 00  ....Ház?7.......
00019100  8F C2 75 3F 38 00 05 04 00 02 03 00 D7 A3 90 3F  .Âu?8.......×£.?
00019110  3A 00 07 03 00 01 02 00 EC 51 78 3F 3B 00 05 03  :.......ìQx?;...
00019120  00 03 03 00 0A D7 63 3F 3E 00 00 04 00 01 02 00  .....×c?>.......
00019130  29 5C 8F 3F 3F 00 00 05 00 03 01 00 E1 7A 94 3F  )\.??.......áz”?
00019140  40 00 01 02 00 05 03 00 8F C2 75 3F 41 00 01 03  @........Âu?A...
00019150  00 04 04 00 EC 51 78 3F 49 00 03 04 00 03 03 00  ....ìQx?I.......
00019160  1F 85 6B 3F 50 00 03 03 00 04 03 00 00 00 80 3F  .…k?P.........€?
00019170  51 00 02 03 01 04 03 00 EC 51 78 3F 52 00 03 03  Q.......ìQx?R...
00019180  01 02 02 00 00 00 80 3F 53 00 03 03 00 03 03 00  ......€?S.......
00019190  00 00 80 3F 56 00 07 05 00 04 03 00 E1 7A 54 3F  ..€?V.......ázT?
000191A0  5A 00 06 04 00 06 02 00 D7 A3 70 3F 64 00 00 03  Z.......×£p?d...
000191B0  00 03 03 00 5C 8F 82 3F 65 00 03 02 00 02 04 00  ....\.‚?e.......
000191C0  00 00 80 3F 66 00 01 05 00 03 02 00 48 E1 9A 3F  ..€?f.......Háš?
000191D0  67 00 03 03 00 02 03 00 66 66 86 3F 68 00 01 04  g.......ff†?h...
000191E0  00 03 02 00 EC 51 98 3F 69 00 04 02 00 02 03 00  ....ìQ˜?i.......
000191F0  33 33 93 3F 6A 00 03 02 00 03 01 00 3D 0A 57 3F  33“?j.......=.W?
00019200  70 00 00 05 00 02 03 00 3D 0A 97 3F 71 00 00 04  p.......=.—?q...
00019210  00 03 02 00 48 E1 9A 3F 73 00 02 03 01 04 03 00  ....Háš?s.......
00019220  1F 85 8B 3F 77 00 03 04 00 01 02 00 7B 14 8E 3F  .…‹?w.......{.Ž?
00019230  78 00 03 03 00 02 04 00 8F C2 75 3F 79 00 03 05  x........Âu?y...
00019240  00 04 01 00 29 5C 8F 3F 7A 00 04 04 00 03 03 00  ....)\.?z.......
00019250  EC 51 78 3F 7B 00 01 03 00 02 03 00 52 B8 5E 3F  ìQx?{.......R¸^?
00019260  7C 00 02 03 00 03 03 00 00 00 80 3F 7D 00 04 04  |.........€?}...
00019270  00 03 03 00 1F 85 8B 3F 7E 00 02 02 00 02 04 00  .....…‹?~.......
00019280  00 00 80 3F 7F 00 07 04 00 04 02 00 D7 A3 90 3F  ..€?........×£.?
00019290  80 00 05 02 00 02 03 00 00 00 80 3F 81 00 06 03  €.........€?....
000192A0  00 06 03 00 00 00 80 3F 82 00 03 02 00 02 02 00  ......€?‚.......
000192B0  AE 47 61 3F 84 00 03 03 00 04 03 00 00 00 80 3F  ®Ga?„.........€?
000192C0  86 00 03 04 00 01 04 00 D7 A3 90 3F 88 00 07 02  †.......×£.?ˆ...
000192D0  00 02 03 00 EC 51 78 3F 8A 00 05 04 00 06 03 00  ....ìQx?Š.......
000192E0  3D 0A 57 3F 8C 00 03 04 01 04 04 00 C3 F5 68 3F  =.W?Œ.......Ãõh?
000192F0  96 00 00 02 00 03 03 00 D7 A3 70 3F 6B 00 00 00  –.......×£p?k...
00019300  01 06 00 00 00 00 C0 3F 6C 00 03 00 00 00 04 00  ......À?l.......
00019310  CD CC 4C 3F 6D 00 02 06 00 06 04 00 00 00 80 3F  ÍÌL?m.........€?
00019320  6E 00 01 06 00 00 04 00 00 00 C0 3F 6F 00 04 06  n.........À?o...
00019330  01 00 00 00 C3 F5 A8 3F                          ....Ãõ¨?
---------------------------------------------------------------------------
```

#### File #2

??? info
    - Author > [Machi](https://github.com/Machi13)
    - Last update > 19 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 22 June 2022

```
Location > 0.DAT
Start > 00017080
End > 000174DB
```

```
Offset 00-01 > Model ID
Offset 02 > Main character type
Offset 03 > Pointer into HP range table
Offset 04 > Starting condition (Fine, Danger)
Offset 05 > Pointer into virus gauge increment multiplier table
Offset 06 > Pointer into animation speed table
Offset 07 > ??? 
Offset 08-0B > Attack power multiplier
```

```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00017080  00 00 03 03 00 03 04 00 CD CC 8C 3F 01 00 04 04  ........ÍÌŒ?....
00017090  00 01 02 00 3D 0A 97 3F 02 00 00 02 00 03 03 00  ....=.—?........
000170A0  00 00 80 3F 03 00 00 03 00 04 03 00 66 66 A6 3F  ..€?........ff¦?
000170B0  04 00 00 05 00 04 02 00 66 66 A6 3F 05 00 00 03  ........ff¦?....
000170C0  00 03 03 00 66 66 86 3F 07 00 00 04 00 04 03 00  ....ff†?........
000170D0  CD CC 8C 3F 09 00 01 05 00 03 01 00 F6 28 9C 3F  ÍÌŒ?........ö(œ?
000170E0  0A 00 03 02 00 03 03 00 EC 51 78 3F 0B 00 00 03  ........ìQx?....
000170F0  00 04 03 00 85 EB 51 3F 0C 00 03 03 01 04 03 00  ....…ëQ?........
00017100  66 66 66 3F 10 00 02 03 00 01 02 00 3D 0A 97 3F  fff?........=.—?
00017110  11 00 01 03 00 04 04 00 00 00 80 3F 12 00 03 02  ..........€?....
00017120  00 03 03 00 00 00 80 3F 13 00 02 03 01 03 03 00  ......€?........
00017130  E1 7A 54 3F 15 00 02 04 00 02 02 00 1F 85 6B 3F  ázT?.........…k?
00017140  16 00 01 04 01 04 02 00 C3 F5 68 3F 18 00 03 03  ........Ãõh?....
00017150  00 03 04 00 00 00 80 3F 19 00 04 03 00 03 03 00  ......€?........
00017160  33 33 73 3F 1A 00 01 03 00 03 03 00 AE 47 61 3F  33s?........®Ga?
00017170  1B 00 01 04 00 02 04 00 CD CC 8C 3F 1C 00 00 02  ........ÍÌŒ?....
00017180  00 04 03 00 00 00 80 3F 1D 00 01 05 01 04 02 00  ......€?........
00017190  48 E1 7A 3F 1F 00 04 03 00 02 03 00 29 5C 8F 3F  Ház?........)\.?
000171A0  20 00 02 04 00 03 04 00 3D 0A 97 3F 22 00 02 02   .......=.—?"...
000171B0  00 04 04 00 EC 51 78 3F 24 00 04 03 00 03 03 00  ....ìQx?$.......
000171C0  00 00 80 3F 26 00 03 03 00 02 02 00 1F 85 6B 3F  ..€?&........…k?
000171D0  27 00 03 06 00 02 03 00 9A 99 59 3F 28 00 03 04  '.......š™Y?(...
000171E0  00 02 01 00 8F C2 75 3F 29 00 03 03 00 03 03 00  .....Âu?).......
000171F0  00 00 80 3F 2A 00 03 01 00 02 03 00 52 B8 5E 3F  ..€?*.......R¸^?
00017200  2B 00 03 03 00 01 02 00 A4 70 7D 3F 2C 00 03 04  +.......¤p}?,...
00017210  00 03 03 00 00 00 80 3F 2E 00 02 02 00 03 02 00  ......€?........
00017220  7B 14 6E 3F 2F 00 03 03 00 03 03 00 52 B8 5E 3F  {.n?/.......R¸^?
00017230  30 00 01 05 00 04 03 00 D7 A3 B0 3F 31 00 00 02  0.......×£°?1...
00017240  00 02 03 00 85 EB 91 3F 32 00 04 03 00 03 03 00  ....…ë‘?2.......
00017250  C3 F5 88 3F 34 00 05 03 00 02 03 00 00 00 80 3F  Ãõˆ?4.........€?
00017260  35 00 06 03 01 06 03 00 85 EB 51 3F 36 00 05 02  5.......…ëQ?6...
00017270  00 02 03 00 48 E1 7A 3F 37 00 07 02 00 03 03 00  ....Ház?7.......
00017280  8F C2 75 3F 38 00 05 04 00 02 03 00 D7 A3 90 3F  .Âu?8.......×£.?
00017290  3A 00 07 03 00 01 02 00 EC 51 78 3F 3B 00 05 03  :.......ìQx?;...
000172A0  00 03 03 00 0A D7 63 3F 3E 00 00 04 00 01 02 00  .....×c?>.......
000172B0  29 5C 8F 3F 3F 00 00 05 00 03 01 00 E1 7A 94 3F  )\.??.......áz”?
000172C0  40 00 01 02 00 05 03 00 8F C2 75 3F 41 00 01 03  @........Âu?A...
000172D0  00 04 04 00 EC 51 78 3F 49 00 03 04 00 03 03 00  ....ìQx?I.......
000172E0  1F 85 6B 3F 50 00 03 03 00 04 03 00 00 00 80 3F  .…k?P.........€?
000172F0  51 00 02 03 01 04 03 00 EC 51 78 3F 52 00 03 03  Q.......ìQx?R...
00017300  01 02 02 00 00 00 80 3F 53 00 03 03 00 03 03 00  ......€?S.......
00017310  00 00 80 3F 56 00 07 05 00 04 03 00 E1 7A 54 3F  ..€?V.......ázT?
00017320  5A 00 06 04 00 06 02 00 D7 A3 70 3F 64 00 00 03  Z.......×£p?d...
00017330  00 03 03 00 5C 8F 82 3F 65 00 03 02 00 02 04 00  ....\.‚?e.......
00017340  00 00 80 3F 66 00 01 05 00 03 02 00 48 E1 9A 3F  ..€?f.......Háš?
00017350  67 00 03 03 00 02 03 00 66 66 86 3F 68 00 01 04  g.......ff†?h...
00017360  00 03 02 00 EC 51 98 3F 69 00 04 02 00 02 03 00  ....ìQ˜?i.......
00017370  33 33 93 3F 6A 00 03 02 00 03 01 00 3D 0A 57 3F  33“?j.......=.W?
00017380  70 00 00 05 00 02 03 00 3D 0A 97 3F 71 00 00 04  p.......=.—?q...
00017390  00 03 02 00 48 E1 9A 3F 73 00 02 03 01 04 03 00  ....Háš?s.......
000173A0  1F 85 8B 3F 77 00 03 04 00 01 02 00 7B 14 8E 3F  .…‹?w.......{.Ž?
000173B0  78 00 03 03 00 02 04 00 8F C2 75 3F 79 00 03 05  x........Âu?y...
000173C0  00 04 01 00 29 5C 8F 3F 7A 00 04 04 00 03 03 00  ....)\.?z.......
000173D0  EC 51 78 3F 7B 00 01 03 00 02 03 00 52 B8 5E 3F  ìQx?{.......R¸^?
000173E0  7C 00 02 03 00 03 03 00 00 00 80 3F 7D 00 04 04  |.........€?}...
000173F0  00 03 03 00 1F 85 8B 3F 7E 00 02 02 00 02 04 00  .....…‹?~.......
00017400  00 00 80 3F 7F 00 07 04 00 04 02 00 D7 A3 90 3F  ..€?........×£.?
00017410  80 00 05 02 00 02 03 00 00 00 80 3F 81 00 06 03  €.........€?....
00017420  00 06 03 00 00 00 80 3F 82 00 03 02 00 02 02 00  ......€?‚.......
00017430  AE 47 61 3F 84 00 03 03 00 04 03 00 00 00 80 3F  ®Ga?„.........€?
00017440  86 00 03 04 00 01 04 00 D7 A3 90 3F 88 00 07 02  †.......×£.?ˆ...
00017450  00 02 03 00 EC 51 78 3F 8A 00 05 04 00 06 03 00  ....ìQx?Š.......
00017460  3D 0A 57 3F 8C 00 03 04 01 04 04 00 C3 F5 68 3F  =.W?Œ.......Ãõh?
00017470  96 00 00 02 00 03 03 00 D7 A3 70 3F 6B 00 00 00  –.......×£p?k...
00017480  01 06 00 00 00 00 C0 3F 6C 00 03 00 00 00 04 00  ......À?l.......
00017490  CD CC 4C 3F 6D 00 02 06 00 06 04 00 00 00 80 3F  ÍÌL?m.........€?
000174A0  6E 00 01 06 00 00 04 00 00 00 C0 3F 6F 00 04 06  n.........À?o...
000174B0  01 00 00 00 C3 F5 A8 3F 74 00 05 00 00 06 04 00  ....Ãõ¨?t.......
000174C0  CD CC AC 3F 75 00 06 06 01 00 02 00 00 00 80 3F  ÍÌ¬?u.........€?
000174D0  76 00 07 06 00 00 04 00 00 00 40 3F              v.........@?
---------------------------------------------------------------------------
```

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