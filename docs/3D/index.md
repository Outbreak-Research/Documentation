# RESIDENT EVIL OUTBREAK SERIES Characters, Enemies, and Object Data Tables
- version 1.1 by Richard Mandel
- revision 1.2 by Bia10

## Introduction

This is based mostly on the more complete tables of Outbreak File 2. It also applies to Outbreak File 1.

With this release, I am including my recent research into the data that appears in both of the original Japanese retail versions of
File 1 and File 2, as well as the U.S. Public Beta 1.0 gametest disc for Outbreak File 1. Anything significant from these will be
noted as "Japanese" and "Public Beta" respectively.

This is the first version of this document to include preliminary tables for all items you can obtain in the game - either in normal
gameplay or high-poly cutscene forms.

My thanks to Rusty, DXP, and all their friends over at the RE 123 Modding Forums for their original research.

## General Observations

Here's a good rule-of-thumb regarding Outbreak character model resolutions:

- Super lo-res/lo-poly (>1200 polys) - distance shots of zombies
- Lo-res/lo-poly (~2000 polys) - general gameplay
- Mid-res/mid-poly (~3500 polys) - main characters and some cutscene models
- Hi-res/hi-poly (>7000 polys) - almost all cutscene models

Likewise, gameplay objects will be fairly low in poly count (usually less than 1000 polys, frequently less than 300)
and cutscene objects fairly high (2000-3000 or higher).

You'll soon learn that Outbreak uses the same basic generic face types for various different NPC and zombie characters.
Each looks different because these generic faces are mapped differently on different models - as well as having different hair,
zombie features (blood, bruisers, etc.), minor tweaking of facial features to better fit the model, and so on.
If you spend enough time with these models, you'll also learn to spot most of the basic face types. You can have a lot of fun
swapping these around yourself to create all-new Outbreak characters, as I did with my custom Ellen Long - a female RPD officer
with Elena's face on Kathy's head and attached to Rita's body.

Some models have more than one version - with or without certain gear and clothes, normal or zombie versions, and so on.
I've tried to distinguish which is which.

A fair amount of Outbreak data got reused for the two Chronicles games (REUC & REDC). I've tried to let you know when that occurs.
Generally speaking, ported Outbreak models - especially zombies or NPCs - are usually fairly easy to spot because they will have
only one or two texture tiles - although they might be large ones intended for high-poly models. With Outbreak models, in most
cases, it will use one texture for everything, or the first will generally be for the head and the second for the rest of the body.
High-poly model textures from later Resident Evil games - beginning with RE0 and RE1R - tend to have anywhere from three to six
textures (as of 2014), and these are usually for dedicated body parts - head, torso, limbs, and so on. This is not a hard-and-fast
rule - especially where monsters and mutants are concerned - but it helps.

### Player Characters (this is P0x_xx in File 1)

1. P00 - Kevin Ryman (policeman)
    +  00 - RPD uniform
    +  01 - Final cutscene (cowboy duds)
    +  02 - Casual (RPD bomber jacket with plaid shirt and jeans)
2. P01 - Mark Wilkins (security guard)
    + 00 - Security guard uniform
    + 01 - Final cutscene (polor shirt and shorts)
    + 01 - Army dress greens, rank of lt. colonel (Vietnam service)
3. P02 - Jim Chapman (subway worker)
    + 00 - Subway worker unform
    + 01 - Final cutscene ("hoopz dudz")
    + 02 - Bicycle messenger
4. P03 - George Hamilton (surgeon)
    + 00 - Green suit with vest and tie
    + 01 - Raccoon Volunteer Corps outfit
    + 02 - Hospital scrubs with mask
5. P04 - David King (plumber and handyman)
    + 00 - Plumber's outfit
    + 01 - Casual (open-neck white shirt with gold chain and sport jacket)
    + 02 - Bare-chested
6. P05 - Alyssa Ashcroft (journalist)
    + 00 - Newspaper reporter
    + 01 - Black workout togs with hair bun and green goggles (somewhat similar to outfit worn in final cutscene)
    + 02 - Red slip and heels (same as Alice in first RE feature film)
    + 03 - Dojo clothes, aka "karate outfit"
    + 04 - Marathon runner
7. P06 - Yoko Suzuki (former Umbrella employee)
    + 00 - University student
    + 01 - Simple long green dress
    + 02 - High school gym clothes (Japanese style)
    + 03 - Traditional green Chinese pantsuit with Mao cap
    + 04 - High school swimsuit (Japanese style)
8. P07 - Cindy Lennox (waitress)
    + 00 - Waitress uniform
    + 01 - Final cutscene (blue blouse with white capri pants)
    + 02 - Playboy bunny suit
    + 03 - Black leathers and boots
    + 04 - White bikini (both parts) and "Daisy Dukes" mini-shorts

### N20x - Player Character Cameos

This is set up as a continuation of the gameplay NPC table, due to the way Outbreak treats player character cameos.

The Outbreak series apparently uses a player character cameo model whenever it needs to generate one specifically for an event in
a given scenario. This feature is used a lot in Outbreak File 2. For example, Cindy will appear at the gate to the zoo of
"Wild Things" if she has not been selected by (any of) the player(s), and she will be killed there (!) when Oscar (the mutant
elephant) begins his rampage. Here's another example. If not chosen as a player character, David will appear as a zombie in the
Sewers near the ladder that leads up to the street outside the Apple Inn in "End of the Road." I've personally seen Kevin and
Yoko appear as zombies in other scenarios as well under similar circumstances (they aren't picked by any players).
This is my best guess at present as to why the N20x table exists for player characters. For modding/hacking purposes, these models
are identical to the regular player character gameplay models and can be treated as such.

There are no player character cameo models of alternate outfits, although they could undoubtedly be swapped in as needed with the
appropriate data from the normal player character model table.

1. N200 - Kevin
2. N201 - Mark
3. N202 - Jim
4. N203 - George
5. N204 - David
6. N205 - Alyssa
7. N206 - Yoko
8. N207 - Cindy

### HP0x - High Poly (HP) Player Characters

These are used exclusively for generating in-game cutscenes. There are no hi-poly versions of player character alternate outfits.

1. HP00 - Kevin
2. HP01 - Mark
3. HP02 - Jim
4. HP03 - George
5. HP04 - David
6. HP05 - Alyssa
7. HP06 - Yoko
8. HP07 - Cindy

### E0x_xx - Enemies (gameplay resolution monsters and zombies)

None of the currently available textures will map properly with the unused zombies. Parts of them can be made to work, but usually
the head won't map right. For example, none of the USS character textures, either normal human or zombie, will map properly with
the unused Miguel zombie. Parts of the uniform can be made to work, but that's about it. I wound up having to hack my own custom
texture for the Miguel zombie. You will have to do the same if you plan on texturing these unused models yourself.

Ricky's cutscene model texture (slot HN008) can almost be made to work (!) with the unused Subway Worker Zombie 1 (slot E036) -
provided you retool it so that it is arranged like those of the other Subway Worker Zombies. The only parts that don't match up
are the (overlaid zombie) eyes and ears, but these may have been located in the proper places on the original low-poly texture
(if it existed). This could mean that Capcom originally had plans for Ricky to re-animate during "Underbelly" after you found him,
and then abandoned those plans - but I'm speculating.

Some of the enemies farther down the enemies table have what seem to be rather high poly counts that defy the general rules of thumb. Bear in mind that these are models of LARGE enemeies - so they will have high poly counts as a result. You can compare the few that also exist in the high-poly enemies table to see just how big a difference in detail (usually three times the polys) exist between the two.

E00 - Licker (two different types, E00_00 and E00_01)
(see also REUC slot ELK1 and REDC slot ELS1)
E01 - Various zombies (40-52, 57-58, 90, and 94 are lo-res)

01 - Generic Male Zombie (unused, no texture)
02 - Generic Sewer Zombie (unused, no texture)
03 - Bald Zombie 1
04 - Sewer Zombie 1
05 - Bald Zombie 2
06 - Miguel Zombie (unused, no texture - File 2 only)
07 - Sewer Zombie 2
08 - Sewer Zombie 3
09 - Nick Zombie
10 - Sean Zombie
11 - Donald Zombie (aka "Don Zombie")
12 - Suit Zombie (not same as Phillip - different character)
13 - Colin Zombie (aka "Denim Zombie")
14 - Robert Zombie
15 - Chuck Zombie
16 - Ginger Zombie
17 - Laura Zombie (aka "Businesswoman Zombie 1")
18 - Amelia Zombie (aka "Businesswoman Zombie 2")
19 - RPD Male Zombie 1 (I named this one "Vince")
20 - RPD Male Zombie 2 (I named this one "Bill")
21 - RPD Male Zombie 3 (I named this one "Hal" or "Harold")
22 - RPD Male Zombie 4 (This was the basis for my David Ford)
23 - RPD Male Zombie 5 no texture (This was the basis for my Scott Ford)
24 - RPD Female Zombie 1 (I named this one "Jane")
25 - RPD Female Zombie 2 (I named this one "Maria")
26 - Generic Doctor Zombie 1
27 - Generic Doctor Zombie 2
28 - Generic Doctor Zombie 3
29 - Nurse Zombie (no texture)
30 - Nurse Zombie (no texture)
31 - "Flash Back" Plant Zombie 1 (Ted?)
32 - "Flash Back" Plant Zombie 2 (Tim?)
33 - Umbrella Lab Tech Zombie 1
34 - Umbrella Lab Tech Zombie 2
35 - Umbrella Lab Tech Zombie 3
36 - Subway Worker Zombie 1 (unused, no texture - might be Ricky?)
37 - Subway Worker Zombie 2
38 - Subway Worker Zombie 3
39 - U.S.S. Zombie 1
40 - Colin Zombie (lo-res, File 2 only)
41 - Robert Zombie - alternate version (lo-res, File 2 only)
42 - Don Zombie - alternate version (lo-res, File 2 only)
43 - Nick Zombie - alternate version (lo-res, File 2 only)
44 - Sean Zombie (lo-res, File 2 only)
45 - Phillip Zombie (lo-res, File 2 only)
46 - Amelia Zombie (lo-res, File 2 only)
47 - Sewer Zombie 3 (lo-res, File 2 only)
48 - Chuck Zombie (lo-res)
49 - Matthew Zombie (lo-res)
50 - Robert Zombie (lo-res)
51 - Suit Zombie (lo-res)
52 - Donald Zombie (lo-res)
54 - Donald Zombie (repeated from slot 11, same resolution)
56 - Fifteen 2D tiles of a walking zombie (File 2 only - identical poses)
57 - Laura Zombie (lo-res, File 2 only)
58 - Nick Zombie (lo-res)
59 - U.S.S. Zombie 2
60 - U.S.S. Zombie 3
90 - Super lo-res zombies 1 (8 different kinds)
94 - Super lo-res zombies 2 (8 different kinds)
99 - Zombie Boy (File 2 only, untextured in File 1)
100 - Matthew Zombie

E02 - Cerebus hounds (four different types, E02-00 to E02-03)
(E02-01 to E02-03 reused in both REUC and REDC)
(E02-00 has two heads and a unique body texture; unused in Outbreak)

E03 - Cockroach (also used in REDC)
E04 - Rat
E05 - Crow (has wings for both at rest and in flight)
E06 - Giant bee
E07 - Giant spider
E08 - Normal (or "baby") spider
E09 - Giant moth (also used in REDC)
E10 - Giant caterpillar
E11 - Short roof-hanging plant tentacle with flattened end ("Flash Back")
E12 - Long roof-hanging plant tentacle with flattened end ("Flash Back")
(Two different versions - E12 and E12_N)
E13 - Pitcher plant variant ("Flash Back")
E14 - Mobile plant branch or vertical tentacle ("Flash Back")
(Two different versions - E14 and E14_N)
E15 - Some kind of bug (crashes on conversion - File 2 only)

E16 - Giant alligator (also seen in REDC)

01 - Intact
02 - Without tail

E017 - Eight 2D tiles of eight different common zombies (to fill out crowds)

00 - Walking
01 - Walking
02 - Dead or immobile

E18 - Giant flea ("Underbelly")
E19 - Queen leech ("The Hive")
E20 - Regis Licker ("Hellfilre")
E21 - Early form Grave Digger?
E22 - Alpha hunter, MA-124 variant (unique to Outbreak)
(also includes frozen versions in numbering variants - E22_01, etc)
E23 - Gamma hunter (smaller version used in REDC)
E24 - Centipede ("Flash Back?")
E25 - Mutant Neptune shark ("The Docks" and "Decisions, Decisions")
E26 - Mutant Neptune shark, repeated ("The Docks" and "Decisions, Decisions")
E27 - Leechman with arms extended, different character bases ("The Hive")

00 - Leechman Kevin
01 - Leechman Mark
02 - Leechman Jim
03 - Leechman George
04 - Leechman David
05 - Leechman Alyssa
06 - Leechman Yoko
07 - Leechman Cindy
08 - Leechman Hirsh
09 - Leechman Scott Jones (original base)

E28 - Birkin form 1 holding a slime-covered Matthew (unused)

NOTE - Birkin NEVER APPEARS in Outbreak, save in pre-release trailers made
back when the game was still in its earliest private beta testing phases.
He was supposed to appear in at least the "USS scenario." This probably
explains why Birkin is grouped with the G-Mutant in the enemy data tables.
This appears to be a low-poly version of the Birkin form 1 mutant that
appears in the Outbreak File 1 opening credits (but without Matthew in his
right hand, of course).

E29 - G-Mutant

00 - Full form G-mutant (Outbreak's is different than RE2 and REDC!)
01 - G-Embryo
02 - G-Mutant gibs

E31 - Naked fat zombie with sewn-up stomach (unused)
E32 - Oscar the infected elephant ("Wild Things")
E33 - Infected lions ("Wild Things")

00 - Male lion
02 - Lioness (female)

E34_01 - Upright mutant plant stalk ("Flash Back")

NOTE - There's apparently bad data at this point starting with the Japanese
original. Both the coatless normal Tyrant and the long-armed, one-armed
prototype Tyrant also appear here, in slots E34_01 and E34_02 respectively.
Were they originally supposed to appear in "Flash Back?" It would be in
keeping with "Flash Back's" unique origins. It is based on an abandoned
sequel to RE1 known as BIOHAZARD DASH. Tyrants would have been encountered
in the basement levels of the DASH original of the hospital. Probably just
a coincidence; even so ....

E35 - Mobile plant root ("Flash Back")
E36 - Scissortail (E36_00 and E36_02 are brown, E36_01 is "Flash Back" dark gray)
E37 - EXTREMELY low-poly zombies with darkened textures (only 85 or so polys!)

00 - Mathhew Zombie
01 - Robert Zombie
02 - Colin Zomibe
03 - Robert Zombie (repeated)

E38 - Moth coccoon for victim
E39 - Grubworm (moth larvae, "Below Freezing Point")
E40 - Prototye Thantos Tyrant, RE1 style but simpler (unused)
(somewhat simlar to REUC's slot ETY1 but closer to old RE1 version)
E41 - Normal Tyrant, "Mister X" outfit (see also REDC slot T103)
(Elimination Tyrant is the same but with red-tinted texture applied)

Variations (File 2 only)

00 - "Mister X" outfit
01 - Transformed, retail version
02 - "Mister X" outfit (repeated)
03 - Elimination Tyrant (red "Mister X" but has spiked head and is VERY fast)

E42 - Thanatos Tyrant transformed, retail version
E43 - Thanatos Tyrant

00 - Classic RE1 style, without clothes or gear (unused, not transformed)
01 - Transformed and injured, only one arm

E44 - Prototype Injured Thanatos Tyrant (one very long arm and one short arm)
(probably early or orignal form of E43_01)
E45 - Axeman Al with axe ("Flash Back")
E46 - Large flower bloom ("Flash Back")

00 - Closed
01 - Open

E47 - Pitcher plant ("Flash Back")

00 - Main blossom or "pitcher"
01 - Long horizontal tentacle or vine (appears to be fixed to roof)

E48 - Normal sized bee ("Flash Back")
E59 - Pair of severed arms (for grappling through broken windows?)
E63 - Baby flea? (File 2 only)
E65 - Hyena ("Wild Things," File 2 only)

### HExx - High Poly (HP) enemies

SPECIAL NOTE REGARDING BETA HIGH-POLY ENEMIES

Not all of the high poly zombies that were created for Outbreak appear in the data tables; however, some of these missing ones
eventually wound up in the two Chronicles games (REUC & REDC). Almost two dozen Outbreak high-poly enemy models were among the
Outbreak assets reused (and updated) for the Chronicles series. In such cases, I will attempt to show you both where they should
have gone in the Outbreak data tables, and where they can be found in the appropriate Chronicles game. It should be noted that all
of the Outbreak models that got reused for Chronicles received both updated models AND textures, so they may look slightly different
than their older Outbreak counterparts.

HE00 - Licker (two different types, HE00_00 and HE00_01)
(see also REUC slot ELK1 and REDC slot ELS1)
HE01 - HD Zombies (various types)

01 - Stock zombie boy
02 - Stock zombie male teenager
03 - Stock zombie man (black shirt brown trousers)
04 - Stock zombie man (brown shirt blue jeans)
06 - Stock zombie man (white shirt green jeans)
07 - Stock zombie man (blue slacks beginning to decompose)
08 - Stock zombie man (tan slacks white shirt unbuttoned)
09 - Nick, aka Nicholas (see also REUC slot EZ30 for alternate version)
10 - Female RPD officer (top half only, "Desperate Times") - File 2 only
11 - Don (Don Zombie) (see also REUC slot EZ31)
12 - Stock zombie man (tan check shirt blue jeans decomposing)
(NOTE - This should have been the Suit Zombie - see REUC slot EZ32)
13 - Colin (Denim Zombie) (see also REUC slot EZ27)
14 - Robert (Jacket Zombie) - File 2 only (see also REUC slot EZ28)
15 - Chuck (Red Plaid Zombie) (see also REUC slot EZ33)
16 - Ginger (not included, see REUC slot EZ34)
17 - Laura (Businesswoman Zombie #1)
18 - Amelia (Businesswoman Zombie #2 - not included, see REUC slot EZ35)
19 - Male RPD officer #1 (not included, see REUC slot EZ36 for alternate ver.)
(I renamed this one "Vince" for my various efforts)
20 - Male RPD officer #2 (not included, see REUC slot EZ37)
(I renamed this one "Bill" for my various efforts)
22 - Male RPD officer #4 (not included, see REUC slot EZ38)
(The low-poly version of this was the basis for my custom RE2 David Ford)
24 - Female RPD officer #1 ("Desperate Times") - File 2 only
(I renamed this one Darcy Powell for my various efforts)
25 - Female RPD officer #2 (not included, see REUC slot EZ29)
(I renamed this one "Maria" for my various efforts)
37 - Subway Zombie 2 (not included, see REUC slot EZ26 for alternate version)
56 - Gibs (severed arm)

HE02 - Cerebus hounds (three different types, HE02-01 to HE02-03)
(reused in both REUC and REDC)
HE03 - Kevin Ryman beta version (provided textures won't map correctly)
(NOTE - I have no clue as to why this is in the Enemies table)
HE06 - Giant Bee
HE07 - Giant Spider
(same as REDC's "Web Spinner")
HE09 - Giant Moth
(same as REDC's "Giant Gypsy Moth")
HE18 - Giant Flea
HE22 - Alpha Hunter (MA-124 variant, unique to Outbreak)
HE23 - Gamma Hunter
(smaller version reused in REDC's "Operation Xavier")
HE29 - G-Mutant
(NOTE - This is different from REDC's "G-Creature!" The REDC verison
is more like the G-Mutant that appears in RE2 than Outbreak File 1.)
HE36 - Scissortail
HE41 - Thanatos Tyrant (various forms)

00 - Normal Tyrant, "Mister X" outfit
(Elimination Tyrant is same with red texture)
(see also REDC slot T103)
01 - Mutated Tyrant, retail version

HE43 - Thanatos Tyrant (injured)

01 - Retail version (one long arm, other missing entirely)

HE99 - Gibs (severed arm, repeated)


### Nxxx - NPCs (non-playable characters in normal game, some can be earned)

SPECIAL NOTES REGARDING NPC MODELS

There's an alternate version of the MacDowell beta placeholder model that occasionally appears in the NPC gameplay tables. It has
texture mapping issues with the head, but this might be an NBDX ripping/conversion error. I've only listed the first occurrence.

Both Clint and Bone are believed to belong to "The Docks," based on their proximity to Austin and Clint's clothing (he's wearing a
life vest). Austin was apparently the pilot of the ship in "The Docks" before being reallocated to "Wild Things," per a surviving
beta test gameplay still.

The name of the NPC zombie that occupies slot 30 is officially unknown. My guess is that it is Jack, the owner of Jack's Bar
("J's Bar" in the game) based on his proximity to Bob and his clothing. His outfit is not unlike Will's save for the color, and
Will is the bartender there ....

I'm fairly certain that Jake and Gary were intended for "A Day in Raccoon," as they're grouped with Mickey in the game data.
Jake appears to be some kind of official, possibly an Umbrella executive. He's a George type, with appropriate medical gear, when
enabled for gameplay. Gary is probably an old acquaintence - possibly antagonistic - and that would make Richard Jake's bodyguard.
Gary is unique, whereas Richard appears to be a variation on UBCS Arnold, and is most likely an undercover USS operative who was
assigned the job of guarding Jake. Richard's presence, if I am right, would explain why both Gary and Mickey are shot dead during
the course of "A Day in Raccoon," and later revive as zombies. Other fans have their own opinions and theories ....

The Yoko as Umbrella researcher model ("Yoko Z" in the game data) is from the opening cutscene to "Outbreak," the game's very first
scenario. That's why it has long hair.

The unused nurse model appears to be an injured version of Raccoon Hospital's Kathy (it has Kathy's head). Elena's head will also
work with it, although the mesh for their newer outfits won't map correctly on the older model. I wound up having to make my own
custom texture in order to properly recreate this model.

Rodney does not appear in any gameplay scenario in either File 1 or File 2 as far as I know; however, he can be earned as a playable
character. He may have been part of the development for "Streets," and his story would have most likely been told in the unreleased
Outbreak File 3.

N000 - Mac, aka MacDowell (UBCS) - lost Streets scenario
N001 - Rodriguez (USS) - "End of the Road," lost USS scenario
N002 - Conrad (USS) - lost USS scenario
N003 - HUNK (USS) - lost USS scenario
N004 - HUNK no mask (USS) - lost USS scenario
N005 - Miguel (USS) - lost USS scenario
* N006 - MacDowell beta placeholder (INCORRECT!! Actually is Miguel with eye-patch and unfinished texture)
N007 - Luke (USS) - lost USS scenario
N008 - MacDowell beta placeholder
N009 - Arnold (UBCS) - "End of the Road"
N010 - Matt (UBCS) - lost Streets scenario
N011 - Billy (UBCS) - lost Streets scenario
N012 - Hirsh - "The Hive"
N013 - Hirsh duplicate - "The Hive"
N014 - Leechman Hirsh - "The Hive"
N015 - Scott Jones, the original Leechman - "The Hive"
N016 - Peter Jenkins - "Decisions, Decisions"
N017 - Marvin (RPD) - "Desperate Times"
N018 - Fred (RPD) - "Desperate Times"
N019 - Andy wounded (RPD) - "Desperate Times"
N020 - Marvin wounded (RPD) - "Desperate Times"
N021 - Jean (RPD) - "Underbelly"
N022 - Tony (RPD) - "Desperate Times"
* N023 - Tony injured (RPD) - "Desperate Times"(File1); Patrick zombie (File2)
N024 - Patrick Reyes - "Wild Things"
N025 - Lloyd Stewart - "Wild Things"
N026 - Austin Taylor - lost Docks scenario
N027 - Clint - lost Docks scenario
N028 - Bone (co-worker of David's) - lost Docks scenario?
N029 - Bob - "Outbreak"
N030 - Jack zombie - "Outbreak" unused
N031 - Nathan Donelly (RPD inmate) - "Desperate Times"
N032 - Samuel Kirk (RPD inmate) - "Desperate Times"
N033 - MacDowell beta placeholder
N034 - Will - "Outbreak"
N035 - Will zombie - "Outbreak"
N036 - Roger - stock character (unused?)
N037 - MacDowell beta placeholder
N038 - Carter - "End of the Road"
N039 - Dr. Gregory Mueller - "Decisions, Decisions"
N040 - Frost - "Below Freezing Point"
N041 - Frost with unfrozen hand - "Below Freezing Point"
N042 - Jake - "A Day in Raccoon"
N043 - Gary - "A Day in Raccoon"
N044 - Richard - "A Day in Raccoon"
! N046 - Mickey zombie - "A Day in Raccoon" (I think this should be N45, not N46)
! N047 - Mickey - "A Day in Raccoon" (I think this should be N46, not N47)
N047 - Dr. Albert Lester, aka Al - "Flash Back"
N048 - Al as Axeman - mask and no shirt - "Flash Back"
N049 - Al no shirt - "Flash Back"
N050 - Ben Bertolucci - "Desperate Times"
N051 - Lucy Mallet - "Flash Back" side quest
N052 - Regen Mallet with bandaged arm - "Flash Back" side quest
N053 - Regen Mallet no bandage on arm - "Flash Back" side quest
N054 - Monica Stevens - "Below Freezing Point"
N055 - Linda Washington - "End of the Road"
N056 - Rita Burnside (RPD) - "Desperate Times"
N057 - MacDowell - duplicate (UBCS)
N058 - Mary - lost Streets scenario
N059 - Kate - stock character
N060 - MacDowell beta placeholder
N061 - MacDowell beta placeholder
N062 - Danny (fireman) - "Hellfire," "Decisions, Decisions"
(also appears in a still from the lost "Streets" scenario)
N063 - Danny wearing gear (fireman) "Hellfire," "Decisions, Decisions"
N064 - Gill (fireman) - "Hellfire," "Decisions, Decisions"
N065 - Gill wearing gear (fireman) - "Hellfire," "Decisions, Decisions"
* N069 - Ethan - "The Hive"
N072 - Cindy stock (cameo) - "Wild Things"
N073 - Keith (doctor at bridge) - "Flash Back"
N080 - Kurt - "Flash Back"
N081 - Kurt Zombie - "Flash Back"
N082 - Gary Zombie - "A Day in Raccoon"
N083 - Al young version - "Flash Back"
N086 - Dorothy Lester - "Flash Back"
N090 - Yoko long hair - "Outbreak" (opening cutscene)
N099 - Stickman Mr. Grey
N100 - Raymond (RPD) - "Outbreak," "Desperate Times"
N101 - Arthur (RPD) - "Outbreak"
N102 - Aaron (RPD) - "Outbreak," "Desperate Times"
N103 - Dorian (RPD) - "Desperate Times"
N104 - Elliot (RPD) - "Outbreak," "Desperate Times"
N105 - Eric (RPD) - "Outbreak,"
N106 - Harry (RPD) - "Outbreak," "Desperate Times"
N107 - Stickman Mr. Red
N108 - Stickman Mr. Blue
N109 - Stickman Mr. Green
N110 - Stickman Mr. Gold
N111 - Stickman Mr. Black
N112 - Karl (UBCS) - "Decisions, Decisions"
N113 - Dustin v1 (UBCS) - "Decisions, Decisions"
N114 - Dustin v2 (UBCS) - "Decisions, Decisions"
N115 - Derek (USS) - "End of the Road"
N116 - Stickman Ms. White
N117 - Stickman Ms. Peach
N118 - Stickman Ms. Water
N119 - Len (fireman) - "Hellfire" (doubles as Charlie in same)
N120 - Nick, aka Nicholas - stock character
N121 - Sean - stock character
N122 - Phillip - stock character
N123 - Don, aka Donald - stock character
N124 - Matthew - stock character
N125 - Robert - stock character
N126 - Chuck - stock character
N127 - Ginger - stock character
N128 - Laura, aka Businesswoman v1 - stock character
N129 - Amelia, aka Businesswoman v2 - stock character
* N130 - Ethan (dupicate) - "The Hive"
N131 - Ethan Zombie - "The Hive"
N132 - Howard - "The Hive"
N133 - Hospital Zombie 1 - "The Hive"
N134 - Isaac - "The Hive"
N135 - Hospital Zombie 2 - "The Hive"
N136 - Kathy - "The Hive"
N137 - Kathy zombie - "The Hive"
N138 - Elena - "The Hive"
N139 - Elena zombie - "The Hive"
N140 - Frank - "Decisions, Decisions"
N141 - Kathy injured (texture missing) - "The Hive"
N150 - Rodney - unused Streets scenario?
N199 - Cindy (missing skirt) - use unknown

### HNxxx - High-Poly NPC Meshes

The high-resolution meshes are for cutscenes only. Some game characters exist only as hi-res meshes - like Tommy Neilson, for
instance. A small handful of cutscene models (Len, Kurt, etc.) are mid-poly models instead of high-poly ones. I can but guess as
to the reason why. Fan hackers have found various ways to use the cutscene models within the game itself, but that discussion lies
well beyond the scope of this document.

There's a medium-res version of the beta version of UBCS MacDowell that gets repeated again and again as a placeholder. I'm only
listing its first appearance, save for one important exception (see table).

The sheer number of unused cutscene models ALONE for "Flash Back" point to a far larger (and probably more entertaining) earlier
version of this most unique of Outbreak's many scenarios. It (and they) probably got cut due to release deadlines and the fact that
Outbreak File 1 did not sell as well as had been hoped. It's a shame, because it looks like it would have played a lot closer to its
source (the sypnosis for the undeveloped RE1 sequel BIOHAZARD DASH) than what we ultimately got.

Of all of the unused high-poly NPC cutscene models, there is only one remaining for which I cannot clearly associate any given
gameplay scenario. That is the one I have come to call the "U.S.S. Commander" (slot HN087). My placing him with the lost U.S.S.
scenario is a best guess based on his outfit alone. He could in fact belong to any of the early version, unreleased, or undeveloped
Outbreak scenarios.

The cutscene model for Joseph Murrows that was developed for "Wild Things" ultimately went unused. Apparently he was to have been
the one who was crushed to death at the zoo gate whenever Oscar the elephant makes his first appearance. That part was given to
Cindy instead (in a cameo appearance) for the retail release of Outbreak File 2.

HN000 - MacDowell (UBCS) (lost "Streets" scenario)
HN001 - Rodriguez (USS) (lost USS scenario, "End of the Road")
HN002 - Conrad (USS) (USS scenario - unused)
HN003 - HUNK (USS) (USS scenario - unused - i.e. Rusty's "HD Luke")
HN004 - HUNK no mask (USS) (USS scenario - unused)
HN005 - Miguel (USS) (USS scenario - unused)
HN008 - Ricky ("Hellfire" - dead subway worker on toilet)
HN009 - Arnold (UBCS) (lost USS scenario, "End of the Road")
HN010 - Matt (UBCS) (lost "Streets" scenario)
HN011 - Billy (UBCS) (lost "Streets" scenario)
HN012 - Hirsh ("The Hive")
HN013 - Hirsh ("The Hive")
HN014 - Leechman Hirsh ("The Hive")
HN015 - Len (fireman) - medium-res ("Hellfire")
HN017 - Marvin (RPD) ("Desperate Times")
HN018 - Fred (RPD) ("Desperate Times")
HN020 - Marvin wounded (RPD) ("Desperate Times")
HN026 - Austin Taylor ("The Docks," "Wild Things")
HN027 - Clint ("The Docks")
HN029 - Bob ("Outbreak")
HN030 - "Jack" ("Outbreak" - unused)
HN031 - Nathan Donnelly ("Desperate Times," unused)
(as documented in Famitsu)
HN032 - Samuel Kirk ("Desperate Times," unused)
(as documented in Famitsu)
HN034 - Will ("Outbreak")
HN038 - Carter ("End of the Road")
HN039 - Dr. Gregory Mueller, aka Greg ("Decisions, Decisions")
HN045 - Mickey zombie ("A Day in Raccoon")
HN046 - Mickey ("A Day in Raccoon")
HN047 - Dr. Albert Lester, aka Al ("Flash Back")
HN048 - "Axeman" early version ("Flash Back" original version)
HN049 - Al shirtless ("Flash Back")
HN051 - Lucy Mallet ("Flash Back" side quest)
(this is the Famitsu early beta version with long pigtails)
HN052 - Regen Mallet ("Flash Back" side quest)
HN054 - Monica Stevens ("Below Freezing Point")
HN055 - Linda Washington ("End of the Road")
HN056 - Rita Burnside ("Desperate Times")
HN057 - Monica Stevens ("Below Freezing Point," repeated)
HN058 - Mary (lost "Streets" scenario)
HN062 - Danny (lost "Streets" scenario, "Hellfire," "Decisions ...")
HN063 - Gill ("Decisions, Decisions")
HN070 - Joseph Murrows ("Wild Things," unused)
HN071 - "Pierce" ("The Docks?" - best guess based on outfit)
HN073 - "Ted" ("Flash Back")
HN074 - "Ted" ("Flash Back," repeated)
HN075 - Ruby (Madison's mother) - unused ("The Streets of Raccoon City")
HN076 - Ruby Zombie - unused ("The Streets of Raccoon City")
HN077 - Madison zombie - unused ("The Streets of Raccoon City")
HN078 - Miguel with cracked helmet and gas mask (lost USS scenario)
HN079 - Nicholai Ginovaef ("Decisions, Decisions")
HN080 - Kurt - medium-res ("Flash Back")
HN081 - Kurt Zombie ("Flash Back")
HN083 - Dr. Albert Lester younger version ("Flash Back" original version)
HN084 - David King younger version ("Flash Back" original version)
HN085 - Alyssa Ashcroft younger version ("Flash Back" original version)
HN086 - Dorothy Lester still human ("Flash Back" original version)
HN087 - The "U.S.S. Commander" (USS scenario? - unused)
HN088 - Monica Stevens (repeated)
HN089 - Frost ("Below Freezing Point")
HN090 - "Tim" ("Flash Back?")
HN091 - MacDowell beta version
(hi-poly version - as documented in Famitsu - lost "Streets" sc.)
HN096 - Tommy Neilson - "End of the Road"
HN097 - Dorothy corpse ("Flash Back")
HN100 - Raymond Douglas ("Outbreak")
HN101 - Arthur ("Outbreak" - cap-wearing officer with bullhorn)
HN102 - Aaron ("Outbreak, "Desperate Times")
HN103 - Dorian ("Outbreak")
HN104 - Elliot ("Outbreak," "Desperate Times")
HN105 - Eric ("Outbreak")
HN106 - Harry ("Outbreak," "Desperate Times")
HN110 - David King (use unknown)
HN119 - Len (fireman) - medium-res, repeated

### Gameplay Objects

This is set up as a continuation of the Enemies table, for some reason. The similarity in number schemes caused me to overlook them
when I first put this FAQ together. My thanks to George Chief for asking a question that, while not related, caused me to re-examine
the data and discover my mistake.

I have no clue as to why Outbreak considers these "enemies."

E49 - Tropical bird ("Wild Things")
E50 - Long strip of stained wallpaper ("Hellfire?")
E51 - Large packing crate
E53 - Large packing crate (repeated)
E54 - Claymore; i.e. anti-personnel mine ("End of the Road")
E55 - Broken or severed tentacle tip ("Flash Back?")
E56 - A group of five long rusted steel rods clustered together in parallel
E58_00 - Five gallon gasoline jerrican
E58_01 - Overhead Valve (in particular, "The Hive" final battle)
E61 - Save Typewriter

00 - by itself
01 - on a pedestal

E62 - Save Typewriter on a pedestal (repeated)


### Gameplay Resolution Objects Within Scenarios

File name format:

OBJSxx - All of the items you can pick up in scenario number xx - low-poly form
(weapons, herbs, sprays, tools, papers, etc.)

These are all grouped together in what I have (somewhat affectionately) come to call "the big pile of s--t." When you rip them and
then attempt to load the resulting OBJ file, be sure to turn off "Load as single mesh" or whatever similar option exists in your
favorite 3D modeling program. It's the only way you can load them individually.

While many objects are the same across gameplay scenarios, there are a few that are not. What I am going to do is give you a list
of the items that most people seem to want to find. Things like weapons, healing items, and so on. I'll also throw in some rather
unique items that some of you would probably like to have for your Outbreak mesh model collection - even though they might exist only
as a low-poly model. While it won't be a complete list of EVERY single item, this should be mostly complete in terms of uniqueness
of the item(s) in question.

Just because I don't list something in a given scenario's "pile of s--t" doesn't mean it's not there. Common items, such as
9mm hanguns, 9mm ammo boxes, potted herbs of healing, and so on are present in ALL scenario object data clusters. I just didn't
feel like listing all of them every single time.

If you're looking mainly for low-poly weapons, your quickest path is to search the
data clusters for the Elimination or Extra Battle scenarios. That way you'll get most of them at one shot.

R001 - "Outbreak" (File 1 - OBJS01.NBD)

9mm Ammo Boxes
Assorted Tagged Keys (various types)
Ammo Clip
Beretta M93R pistol
Broken Broom Handle (two versions - long and short)
Browning HP .45 ACP handgun
Crescent Wrench (double-ended)
David's Homemade Handheld Torch (insecticide spray + lighter)
David's Homemade Spear (carving knife + broom handle)
Eric's Detonator (both versions, with or without handle)
First Aid Spray
Grenade Launcher rounds
Healing Herbs (potted - all three colors)
Healing Powders (various mixes)
Insecticide Spray
Iron Pipes (three kinds - straight, somewhat bent, and really bent)
Knives (two different kinds - a pairing knife and a big carving knife)
M203 Grenade Launcher (with shoulder stock)
Magnum Speedloader
Molotov Cocktails
Nail Gun
Newspaper Pages (various)
Pills (various)
Push Broom
Whiskey Bottle (resembles Jack Daniels [TM] brand)
Zippo (TM) cigarette lighter

R015 - "Desperate Times" (File 2 - OBJS15.NBD)

NOTE - There's more handguns in this data cluster than almost any other three
scenarios put together, with one exception.

Battery
Beretta "Burst Handgun"
Burst Handgun Extended Ammo Clip
Dart Gun (or is that the Pill Shooter?)
David's Homemade Taser (iron pipe + battery + wires)
Frenchi SPAS-12 Shotgun
Heckler & Koch MP-5 Submachine Gun
Switch With Wiring
Knockout Gas Cannister
Wooden Planks

R026 - "Flash Back" (File 1 - OBJS26.NBD)

Axe
David's Homemade Mace (iron pipe + rock)
Remington 12-gauge Pump Shotgun (with shoulder stock)
Crutch
Rock

R028 - "The Hive" (File 1 - OBJS28.NBD)

Blood Pack (for i.v. transfusions, used to bait the Leechman)
Ledgers (various)

R035 - "Below Freezing Point (File 1 - OBJS35.NBD)

(One of the few data clusters with more than one shotgun - two SPAS-12s! I
also noticed this data cluster has about as many handguns as "Desperate Times.")

Gasoline Jerrican (5 gallons)
Handheld Propane Torch
Large Adjustable Crescent Wrench
Pill Bottles (various)
Red Umbrella Key Card
Valve Handle (an RE classic - you just KNEW it had to be here somewhere!)

R040 - "Wild Things" (File 2 - OBJS40.NBD)

Hunting Rifle (generic .30-06, belongs to Austin)
Hunting Knife

R041 - "Decisions, Decisions" (File 1 - OBJS41.NBD)

Daylight Anti-Virus Vial
Colt M4 .223 Machine Gun
Peter's Glasses (Peter Jenkins)
Rocket Launcher

### Cutscene Resolution Objects Within Scenarios

Once you start to tear into the Outbreak scenario data, you'll see a group of files that are named according to the following
general format:

File name format:

OBJnn_nn_L_nn ... - High-poly object(s) that appear within a scenario

These are "hero" or high-poly versions of Outbreak's common objects, which are intended solely for in-game cutscene use.
The number of high-poly objects in the Outbreak series are quite limited in comparison to the gameplay resolution ones (both common
and scenario-specific); however, there are some in this table that appear nowhere else within the series.

Multiple copies of these appear, usually for different versions of in-game generated cutscenes (for different player characters).
I'm only going to list the FIRST time a particular high-poly object appears in the scenario data table. It's a waste of time listing
every single instance or occurrence, as the repeated data is identical.

R001 - "Outbreak" (File 1)

OBJ00_06_A_00 - Coaster
OBJ00_06_A_001 - Hexagonal shot glass (version 1)
OBJ00_06_A_002 - Hexagonal shot glass (version 2)
OBJ00_06_A_02 - Alyssa's laptop computer
OBJ00_06_A_03 - Jim's book of crosswords
OBJ00_06_A_04 - Jim's pencil
OBJ00_06_A_05 - Mark's Fork (distorted lengthwise)
OBJ00_06_A_06 - Mark's Spoon (distorted lengthwise)
OBJ00_06_A_07 - Mark's bowl of soup
OBJ00_06_A_08 - Mark's plate of food
OBJ00_06_A_08 - Mark's drinking glass
OBJ02_02_A_00 - Front door of J's Bar
OBJ02_08_G_00 - Baseboard vent cover (J's Bar bathrooms)
OBJ05_00_A_00 - Beretta M93R pistol
OBJ09_00_A_00 - Key with round green tag (for alley gate?)
OBJ11_00_A_00 - Raymond's SPAS-12 shotgun
OBJ13_00_A_00 - Raymond's Zippo (TM) lighter
OBJ15_03_A_00 - Fire department door tag with Roy DeSoto's name on it
(reference to the old NBC-TV series EMERGENCY)
OBJ18_00_A_00 - RPD SWAT van with windows (static, not moveable)
OBJ19_00_A_00 - RPD SWAT van with windows (moving version)
OBJ20_00_A_00 - Jim's subway uniform ball cap
OBJ23_00_A_00 - Detonator (no handle)
OBJ28_00_B_00 - Nail gun
OBJ31_00_A_00 - Walkie-talkie
OBJ33_00_A_00 - Arthur's megaphone (bullhorn)

R002 - "Hellfire" (File 1)

OBJ02_00_A_00 - Walkie-talkie
OBJ05_01_A_00 - Fire department door tag with Roy DeSoto's name on it
(reference to the old NBC-TV series EMERGENCY)
OBJ31_00_A_00 - Walkie-talkie

R006 - "End of the Road" (File 2)

OBJ01_02_A_00 - Virus sample cylinder, metal ends only
OBJ01_02_A_01 - Virus sample cylinder, middle glass
OBJ06_00_A_00 - Stock wooden door

R015 - "Desperate Times" (File 2)

OBJ00_00_A_0x - RPD front gate (00 is one side and 01 the other)
OBJ00_01_A_00 - Marvin's map of the RPD's first floor
OBJ00_01_A_01 - Walkie-talkie
OBJ02_00_A_00 - Beretta M93R pistol
OBJ02_01_A_00 - Stock metal door
OBJ02_02_A_00 - RPD newer police car (Chevy Caprice)
OBJ04_00_A_00 - RPD SWAT van (Outbreak version with windows)
OBJ04_08_A_06 - RPD newer police car with passengers (Cindy and Frost)
(used to allude to opening of RE2 in closing cutscene)

R026 - "Flash Back" (File 2)

OBJ01_00_A_00 - Stock wooden door (cabin door?)
OBJ01_00_A_01 - Tabletop picture frame with photo of Al and Dorothy Lester
OBJ11_00_A_01 - Axeman's Mask (collapsed as if taken off and dropped)

R028 - "The Hive" (File 1)

OBJ04_00_A_00 - Two glass window panes side-by-side
OBJ04_00_A_01 - Nurses' Station counter curtains
OBJ04_00_A_03 - Singler large glass window pane
OBJ04_00_A_05 - Six-drawer rolling instrument cart
OBJ11_00_A_00 - Flat-bottom fishing boat with motor

R035 - "Below Freezing Point" (File 1)

OBJ01_00_A_01 - Monica's Beretta M93R pistol (identical to RPD version)
OBJ03_00_A_01 - G-virus sample case
OBJ03_00_A_02 - Red Umbrella card key (Yoko's)
OBJ05_00_A_00 - Platform elevator
OBJ11_01_A_02 - "Shaft Type L" sliding door (Birkin's lab)
OBJ11_02_A_03 - Train turntable elevator key
OBJ20_00_A_00 - Handheld propane torch
OBJ20_00_A_02 - Control console trip handle (for HVAC system control panel)
OBJ24_00_A_01 - Virus sample cylinder broken glass

R040 - "Wild Things"

OBJ02_00_A_0x - Raccoon Zoo front gates (01 is one side, 02 is the other)
OBJ02_00_A_02 - Gate chain
OBJ08_00_A_00 - City trolley, two cars (camera side only parts present!)

R041 - "Decisions, Decisions" (File 1)

OBJ30_00_A_00 - Rooftop door (cutscene right before final boss battle)
OBJ30_00_A_01 - Danny and Gill's helicopter (verson with searchlight)
OBJ31_00_A_00 - Danny and Gill's helicopter (verson without searchlight)

### Other Files of Note

EFxx - Gun effects (shells, splats, etc.) for a given scenario

### BONUS - Quick List of Outbreak Scenario Numbers

Outbreak scenarios appear to have been numbered in the order that they were conceived or created, and not when they were intended for
release. Capcom's programmers also deliberately left gaps in the sequence, as they were planning an entire series of Outbreak games.
They also backtracked on the numbering scheme in File 2's case, which makes things even more confusing for the Outbreak researcher.
I've seen public statements and magazine articles talking about up to eighteen scenarios all told in various stages of development
across the three intended retail released (Files 1-3), but no more. It should be noted there are slots in the Outbreak scenario
table for far more than that.

In most cases, all of the texture files for rooms and room objects within a given scenario share the same room number prefix as the
scenario itself ... but there ARE some interesting exceptions. Some scenarios apparently got renumbered and moved during the
development process. "The Hive," for instance, apparently originally existed in slot R019 early on, and then got moved wholesale
to slot R028 - for reasons still unknown. All of its texture tiles have the prefix "R019" instead of "R028," as they should have
been. "Desperate Times" has three different sets of texture tiles, with prefixes of R015, R019, and R40 respectively. Apparently
this also got revised a lot during development, which may help explain why it was not released until File 2. There are several other
examples of this. The room/texture naming scheme alone appears to point to four additional Outbreak scenarios that either never got
released or existed in forms earlier than what wound up released for retail.

Most fans believe that "Hellfire" replaced "A Day in Raccoon," and several fan experts have noted numerous similarities between the
rooms and textures for both. It's quite possible that "A Day in Raccoon" originally occupied slot R002 and was subsequently
overwritten by "Hellfire" for retail release. If true, this would help explain the similarities between them - but this is
speculation on my part.

I do not know where either of the two other documented unreleased Outbreak scenarios - "The Streets of Raccoon City" and "The Docks"
- fit into this scenario naming scheme. I've made a wild-ass guess in the case of "Streets" - but in either case, there simply isn't
enough data to be certain.

R001 - "Outbreak" (File 1)
(This is the oldest of all scenarios - "OutbreaK" is its official name)

R002 - "Hellfire" (File 2)
(May have overwritten "A Day in Raccoon" in this slot?)

R004 - unreleased
(This was probably the original version of "Below Freezing Point" - which
is also known as the lost U.S.S. scenario)

R006 - "End of the Road" (File 2)

R010 - "Underbelly" (File 1)

R015 - "Desperate Times" (File 2)

R016 - unreleased
(lots of city-based texture tiles came from here - is this where "Streets"
went?)

R019 - unreleased
(This was probably the original version of "The Hive" - the one that also
had the EXTERIOR of Raccoon Hospital as well as the park across the street,
per RE3 and early game trailers)

R020 - practice level (based on File 1's "Outbreak")

R021 - Elimination/Battle level - mixed rooms (?)
R022 - Elimination/Battle level - mixed rooms (?)
R023 - Elimination/Battle level - mixed rooms (?)

R026 - "Flash Back" (File 2)
(There were apparently plans for a somewhat different version of "Flash Back"
that did not make it to retail. Some of the early trailer shots don't agree
with the retail data, and unused [but present] cutscene models exist that
appear to point to events that took place six years earlier. Only allusions
and references to these past events appear in the final retail version. The
fully rendered cutscene models for both the younger Al and Dorothy Lester
are part of this data - only a picture of them exists in gameplay proper.)

R027 - Elimination/Battle level - mixed rooms (?)

R028 - "The Hive" (retail version)
(Almost all of its texture tiles originally belonged to R019)

R029 - Elimination/Battle level - mixed rooms (?)
R030 - Elimination/Battle level - mixed rooms (?)

R035 - "Below Freezing Point" (File 1)
(Most of its texture tiles originally belonged to R004)

R039 - unreleased
(A scene involving an aerial tram car from this lost scenario appears in
some Elimination or Battle levels. That is all that is known about it.)

R040 - "Wild Things" (File 2)
(this appears to have been the last official addition to the scenario
lineup for retail release - texture data from it appears in the final retail
version of "Desperate Times")

R041 - "Decisions, Decisions" (File 1)