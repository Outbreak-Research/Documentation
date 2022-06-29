## Animations

??? info "Authors metadata"
    - Author > Carl_Vercetti
    - Last update > 28 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 28 June 2022

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