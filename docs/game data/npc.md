## NPCs

### NPC cameos

??? info "Authors metadata"
    - Authors > hill73n
    - Last update > 2 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 2 July 2022

Note: The word cameo in this context stands for a small role/part that npc plays in particular scenario

General path to npc cameos data:

- NETBIO00.DAT > [r0xx.afs] > r0xx.npc

#### Header

For each npc cameo defined:

- 4 bytes offset to npc cameo data
- 4 bytes size of npc cameo data in bytes

#### Example header of r40.npc (Wild Things)
```
Offset(h) 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F
---------------------------------------------------------------------------
00000000  28 00 00 00 88 00 00 00 B0 00 00 00 88 00 00 00  (...ˆ...°...ˆ...
00000010  38 01 00 00 88 00 00 00 C0 01 00 00 88 00 00 00  8...ˆ...À...ˆ...
00000020  48 02 00 00 88 00 00 00 
---------------------------------------------------------------------------

We can see 5 npc cameos begin defined:

- 1st npc cameo starts at 0x000028 and has size of 0x000088 (136) bytes of data.
- 2nd npc cameo starts at 0x0000B0 and has size of 0x000088 (136) bytes of data.
- 3rd npc cameo starts at 0x000138 and has size of 0x000088 (136) bytes of data.
- 4rd npc cameo starts at 0x0001C0 and has size of 0x000088 (136) bytes of data.
- 5rd npc cameo starts at 0x000248 and has size of 0x000088 (136) bytes of data.
```

#### Data section

```
Offset 00-03: Always 01 00 00 00 (Probably start of data marker as this is used in .emd files too.)
Offset 04-08: Always 08 00 00 00 - Unknown function
Offset 09-0B: Always 01 00 00 00 - Unknown function
Offset 0C-0F: Room ID 
Offset 10-13: Room sub-ID (usually 00, but some rooms have multiple models due to events)
Offset 14-17: NPC model ID (main character cameos use the N20x.NBD versions, not the P0x_0x.nbd)
Offset 18-1B: Spawning position X coordinates
Offset 1C-1F: Spawning position Y (elevation) coordinates
Offset 20-23: Spawning position Z coordinates
Offset 24-27: Spawning position rotation value
Offset 28-33: Always 00 00 00 00 - Unknown function
Offset 34-37: Message ID ?? (These messages are located in r040.bin)
```