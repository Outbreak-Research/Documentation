## Virus Gauge

??? info
    - Author > [Machi](https://github.com/Machi13)
    - Last update > 19 June 2022
    - Last modification > [Bia10](https://github.com/Bia10) at 22 June 2022

### Definitions

- MC/NPC max virus gauge (**mvg**): 
    Max possible value before becoming zombie
- MC/NPC virus gauge increment (**vgi**):
     Incremental value by which virus gauge increases per one tick 
- NPC virus gauge increment multiplier (**vgim**): 
    Virus gauge increment is multiplied with this value
- A (**tick**) which is equal to passage of 1 second ingame roughly at ~60fps

### Equations

- MCs virus gauge ${\displaystyle = {\frac {(vgi * tick) * 100} {mvg}}}$

- NPCs virus gauge ${\displaystyle = {\frac {(vgi * vgim * tick) * 100} {mvg}}}$

### Examples

- Assuming 1 second has passed since scenario started.

#### MC

- Kevin max virus gauge = 151200
- Kevin virus gauge increment = 30
- Kevin virus gauge: ${\displaystyle {\frac {(30 * 1) * 100} {151200}} = 0.01984126984 \approx 0.02 \%}$

#### NPC

- Billy max virus gauge = 151200
- Billy virus gauge increment = 30
- Billy virus gauge multiplier = 1,2
- Billy virus gauge: ${\displaystyle {\frac {(30 * 1.2 * 1) * 100} {151200}} = 0.0238095238 \approx 0.02 \%}$