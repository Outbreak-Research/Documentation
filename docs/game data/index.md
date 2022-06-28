# Introduction 

This sections describes how are data mapped from disc files into memory and what these memory structures contain.

## File formats used by the game

| File extension | Official name     | Relates to                 | Description                                                         | Tools |
| -------------- |--------------     |----------------------------|---------------------------------------------------------------------| ----- |
| .nbd           |                   | 3D models, textures, bones | Contains other chunks of other file formats like .amo, .tex        | |
| .dat           |                   | generic archive file format| Stores other file formats, can have different encoding/compression  | |
| .img           | Munge file format | images file format         |                                                                     | Game Graphics Studio, AFSTool, AFSExplorer |
| .amo           |                   | 3D models, (Animated model object?) |                                                            | |
| .tex           |                   | texture image format       |                                                                     | |
| .tm2           | TIM2              | image format               | TIM2 is an image format commonly used in PlayStation 2              | [Tim2 Tools](https://outbreak-research.github.io/Documentation/textures/#tools) |
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
| .rdt           |                   | room data, multiplayer data           | Used in ingame scripts                                              | |
| .tbl           |                   | item distribution patterns          | Tabular data format                                                 | |
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
