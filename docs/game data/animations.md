## Animations

??? info "Authors metadata"
    - Author > Carl_Vercetti, dchaps/chaps
    - Last update > 28 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 28 June 2022


Animation IDs
```
100: Idle
101: Forward Walk
102: Backward Walk
103: Run
123: Shotgun Idle
124: Shotgun Walk
125: Shotgun Run
131: Danger Neutral
132: Dying Neutral
136: Danger Backward
137: Danger Forward
142: Dying Forward
143: Dying Backward
151: Rise from Dying
169: Support Danger NPC
170: Pick Up Dying NPC
193: Grab Item on Floor
195: Grab Item Dying
196: Recieve Item
208: Present Item
209: Recoil from Presenting
215: Spray
219: Equip Weapon
227: "Come on!"
233: Standard Tackle
234: Neutral Unarmed Aim
236: Exit Neutral Aim
237: Tackle Recoil
257: "Go!"
261: Upward Unarmed Aim
262: Downward Unarmed aim
264: Upward Knife Swing
265: Neutral Knife Swing
266: Downward Knife Swing
275: Neutral Stun Gun
277: Upward Stun Gun
279: Downwad Stun Gun
286: Stomp
340: Open Door Push
341: Open Door Push Danger
342: Open Door Pull
344: Unlock Door
346: Locked Door Push
347: Locked Door Pull
352: Initiate Hold Door Push
354: End Hold Door Push
355: Hold Door Push
357: Initiate Hold Door Pull
359: End Hold Door Pull
360: Hold Door Pull
378: Handgun Aim Right Turn
379: Handgun Aim Left Turn
380: Danger to Handgun Aim
381: Handgun Aim to Danger
410: Shotgun Aim Start
411: Shotgun Neutral Aim
412: Shotgun Neutral Fire
413: Shotgun Aim End
425: Assault Rifle Initiate Aim
426: Assault Rifle Neutral Aim
427: Assault Rifle Fire 1
428: Assault Rifle End Aim
461: Hunting Rifle Fire
464: Grenade Launcher Aim Start
465: Grenade Launcher Neutral Aim
466: Grenade Launcher Neutral Fire
472: Grenade Launcher Right Turn
473: Grenade Launcher Left Turn
475: Grenade Launcher Reload
518: Backward Up Stairs
519: Forward Up Stairs
521: Backward Down Stairs
522: Forward Down Stairs
524: Backward Up Stairs Danger
525: Forward Up Stairs Danger
527: Backward Down Stairs Danger
528: Forward Down Stairs Danger
546: Climb Waist High
547: Descend Waist High
566: Descend Over Head
567: Climb Over Head
586: Ladder Upward
587: Ladder Downward
588: Ladder Neutral
591: Fall from Ladder
592: Neutral Aim Melee Weapon
593: Upward Aim Melee Weapon
594: Downward Aim Melee Weapon
596: Neutral Melee Swing
597: Upward Melee Swing
598: Downward Melee Swing
607: Bottle Throw
733: Crawl Start
734: Crawl
737: Crawl End
770: Shimmy Initiate
772: Shimmy Neutral
773: Shimmy Right
774: Shimmy Left
776: Shimmy End
780: Shimmy Fall
838: Stagger Backward
839:
840: Stagger Forward
841: Hit at Feet
869: Open Drawer
872: Open Locker
904: Magnum Fire
907: Upward Melee Recoil
908: Neutral Melee Recoil
909: Downward Melee Recoil
922: Hanging Climb Right
923: Hanging Climb Left
929: Hanging Climb Neutral
935: Rocket Launcher Initiate Aim
936: Rocket Launcher Aim
937: Rocket Launcher Fire
938: Rocket Launcher End Aim
940: Assault Rifle Fire 2
941: Assault Rifle Fire 3
```

### Animation data files

General path to animation data:

- NETBIO00.DAT > ROMDATA.AFS > .bins

#### Enemies animations

File Format: E(enemyIdentifier)_(enemyAlternative).bin

```
E00_000.bin > Licker
E01_000.bin > Zombie
E02_000.bin > Dog
E03_000.bin > unused
E04_000.bin > unused
E05_000.bin > crow
E06_000.bin > wasp
```

#### Enemies grab/ko/special att. animations

Contains the animation of the main characters (and NPC) when grabbed, instant ko or get a special attack by enemies. 

File Format: EP(enemyID)_tbl.bin

```
EP00_tbl.bin > Licker (for example, you can find the suffocate animation when a licker grabs from the roof)
EP01_tbl.bin > Zombie grabs (front bite, rear bite, ground bite, pushed) and so on. Help you with a document about enemy identifiers
```

#### Playable characters animations

Contains the animation about the playable characters.

File Format: PL(MC_ID)_pc_000.bin

```
PL00_pc_000.bin
PL01_pc_000.bin
PL02_pc_000.bin
PL03_pc_000.bin
PL04_pc_000.bin
PL05_pc_000.bin
PL06_pc_000.bin
PL07_pc_000.bin
```

Only the 000 is used, in the other one there are unused animations (like run, walk and so on). 
This file contains the idle animation, the turn animation, run, walk, backwalk, special ability animation. 
In the PL06 (yoko) you can find shooting animation too for her stance with the gun. 

#### Scenario animations

FileFormat: SP_ScenarioID.bin

Contains all the animation for a scenario it includes:
- All aim position for all the weapons of the scenario
- Danger animation (walk idle backwalk)
- Caution stance
- Pick object
- Push object
- Climb wall