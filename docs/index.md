# Welcome to RE Outbreak docs!

This is a collaborative effort to reverse engineer the game data and mechanics of Resident Evil Outbreak file 1#, 2# and "3#" which was never officialy released.

## File formats used by the game

| File extension | Official name     | Relates to                 | Description                                                         | Tools |
| -------------- |--------------     |----------------------------|---------------------------------------------------------------------| ----- |
| .nbd           |                   | 3D models, textures, bones | Contains other chuncks of other file formats like .amo, .tex        | |
| .dat           |                   | generic archive file format| Stores other file formats, can have different encoding/compression  | |
| .img           | Munge file format | images file format         |                                                                     | Game Graphics Studio, AFSTool, AFSExplorer |
| .amo           |                   | 3D models, (Animated model object?) |                                                            | |
| .tex           |                   | texture image format       |                                                                     | |
| .tm2           | TIM2              | image format               | TIM2 is an image format commonly used in PlayStation 2              | Game Graphics Studio, OPTPiX iMageStudio 3 |
| .bin           | Binary file       | non-text data              | Can store anything, usually not related to text                     | |
| .txt           |                   | text                       | A standard text document                                            | Word, Notepad, Notepad++ |
| .wmd           |                   |                            |                                                                     | |
| .mat           |                   |                            |                                                                     | |
| .tsb           |                   |                            |                                                                     | |
| .tq            |                   |                            |                                                                     | |
| .snp           |                   |                            |                                                                     | |
| .sdt           | Audio file        | sound                      |                                                                     | |
| .snd           | Raw Sound Data    | sound                      | Uses compression ADPCM(Adaptive Differential Pulse-Code Modulation) | MFAudio |
| .sld           |                   |                            |                                                                     | |
| .rdt           |                   | multiplayer data           | Used in ingame scripts                                              | |
| .tbl           |                   |                            |                                                                     | |
| .itt           |                   |                            |                                                                     | |
| .evb           |                   | event list                 | Used in ingame scripts                                              | |
| .npc           |                   | NPC data                   |                                                                     | |
| .sto           |                   |                            |                                                                     | |
| .lig           |                   |                            |                                                                     | |
| .fog           |                   |                            |                                                                     | |
| .rtp           |                   |                            |                                                                     | |
| .emd           |                   | enemy data                 |                                                                     | |
| .epp           |                   |                            |                                                                     | |
| .sgl           |                   | single player data         |                                                                     | |
| .adx           |                   | sound                      | Mainly tracks played in rooms                                       | |