# Normal Wild / Friend Safari RNG - Alternative method

### Tools needed:
* [3DS RNG Tool](https://github.com/wwwwwwzx/3DSRNGTool/releases)
* [Tiny Finder](https://github.com/Bambo-Rambo/TinyFinder#readme) (The latest build)
* [Pcalc G6](https://gbatemp.net/threads/pokecalcntr-for-gen-6-the-rng-tool-suite-for-the-3ds.473221/) (Retail) or [CitraRNG](https://github.com/Admiral-Fish/CitraRNG/releases) (Emulator)

### Recommended in game
* Repels
* Shiny Charm if going for shinies
* One completely empty side in the bag. I discarded all my berries since I don't need them

![](https://i.imgur.com/B19lgMa.png)

### Extra
* [Gen 6 Encounter Slots](https://sites.google.com/site/pokemonslots/gen-vi)

### Introduction

When using honey or sweet scent in most gen 6 areas, hordes are generated instead of single wild Pokemon.

This means that for abusing single Pokemon in the wild, you have to trigger the desired encounter by moving in the grass.

The gender, IVs and shininess for wild encounters in gen 6 games, are generated using the main initial seed/state (MT).

The slot (species), nature sync and most important, the successful (or not) encounter trigger, are generated using a second state consisting of 4 hex numbers (TinyMT).

The 2 states need to be manipulated together in order to get the desired Pokemon (when reaching the target frame, your current index should generate the desired results).

The main initial seed advances by 2 per frame or 60 per second, while the TinyMT state is more complicated and is affected by multiple factors.

Until recently, a special timeline was required to combine the 2 states and match the main seed with TinyMT.

But with this new method, all we gotta do is deal with TinyMT alone first, and then wait until we reach our target main frame to get the correct stats and shiny.


### Getting Started

It is recommended to have saved the game in the route/place your target Pokemon appears.

Boot the game with Pcalc, connect your console to 3DS RNG Tool using the NTR Helper (see [here](https://github.com/wwwwwwzx/3DSRNGTool/wiki/NTR-Helper-Usage)) 
and reseed until you find a nice spread. 
Connect with Tiny Finder as well (Generator -> Extra -> NTR Helper).

![](https://i.imgur.com/R1QI3Af.png)

When in game, use a repel and start walking around until it is consumed.
Then stand in the recommended spot according to the following links:
* [XY](https://imgur.com/a/pGk0bhM)
* [ORAS](https://imgur.com/a/B3URhjo)

You can't trigger encounters directly from booting the game and a few steps are required to get rid of that restriction (around 5 for grass and many more for caves).

For consistency purposes, I always use a repel.

If you accidentaly get a random encounter after the repel effects ends, use another one and repeat then freeze the game by pressing Start + Select.

In Tiny Finder, select the location (very important epsecially in XY) or check the Cave button if true.

Check the "Long Grass" box if needed (ORAS only).

The value of Min Index is also important and since I am gonna RNG for a wild Zoroark in Pokemon Village I need to set it to 27 according to the albums above.

Finally, fill in the filters of the 3rd box in Tiny Finder to search for your target and press "Update".

All the following indexes generate successful and synced encounter with slots 10-12 which are Zoroarks in Pokemon Village.

Since index 46 is very close to 27, I am gonna aim for that.

![](https://i.imgur.com/kUJ1nyd.png)

Enter the bag and press "Update again.

All you need to do now is reach index 46.

The TinyMT state is now freezed and won't advance until we manually do it ourselves, so we have full control now.

Here are some ways to advance inside the bag:

* Attempting to teach one of your Pokemon a new move and reject it, advances by 1 index (In fact what advances here, is checking the summary screen of the Pokemon). 
Teaching the move will advance more so you need to avoid it.
* Giving your Pokemon a held item, usually advances by 3. (rarely by 4).
* Turning on/off the EXP Share advances by 3 * number of Party. This means that if you have 4 Pokemon in your party, using the Exp Share, will advance 3 * 4 = 12 indexes etc

When I entered the bag, the TinyMT also advanced once before freezing so the target index became 45.

45 - 27 = 18 so I need to advance 18 indexes inside the bag.

And since my party consists of 6 Pokemon (6 x 3 = 18), all I need to do now, is turn on the Exp Share once and I am done with the TinyMT part.

At this time I was really lucky but sometimes the target index may be far away.

See [here](https://github.com/Bambo-Rambo/RNG-Guides/blob/main/NormalWild-FS-RNG.md#ways-to-advance-the-tinymt-state-fast) on how to advance TinyMT indexes faster.

![](https://i.imgur.com/ovcPCW1.png)

### Finalizing - Hitting the target Pokemon

Stay in the empty side of the bag and freeze the game (Start + Select), around ~110 main frame before your target.

Tap Start and immediatly 'B' as fast as you can to exit to the X menu.

It would be ideal to hold 'B' and tap Start to unfreeze, but 3ds doesn't allow simultaneous use of the two buttons.

While exiting the bag, freeze the game again and be careful not to miss your frame.

If everything done right, you will land on your target index.

Now all you need to do is reach exactly 10 frames before your target so start spamming Select presses.

At 10 frames away, hold 'X' and start tapping Select carefully in order to slowly close the menu.

Do that 8 times and your current frame will be -2 from your target (the game is still frozen).

Hold a D pad arrow in a direction different to the one your character is facing and press 'A' to finally rotate the character and trigger the encounter.

![](https://i.imgur.com/4VaKWy2.gif)

### Ways to advance the TinyMT state fast
* If you can find a rainy, place you will have huge advancements per frame. In ORAS you can use the south part of Route 120. In XY, possible rainy places include: Route 8, Route 16, Route 14, Route 19, Laverre City.
* At route 16, there are 2 roller skaters. Stand in front of them to block their way and you will have 1 advance per 2 frames.
* Using Poke Amie in the lower screen also advances by 1 index per frame, but it may break if you have communicated online with random users (unfinished).

### Notes
* Inside the bag, frames advance 1 by 1 so the odd/even issue is not a thing.
After exiting the bag though, your frame type will be odd if you exited in an odd frame and vice versa.
This is controllable if the game is frozen when exiting, but since B and Select buttons cannot be pressed together, it is pretty much out of your control.
For this reason, the shiny charm is necessary if going for shinies because it gives 3 consecutive identical shiny frames, and thus solves the odd/even issue.
Alternatively, you can exit the bag by holding 'X' and tap Start to exit in the overworld (Only for quiet places and also +1 index advance. See below why).
* After exiting the bag, if you also close the 'X' menu, the lower screen functions (PSS, Poke Amie etc) are reloaded and they cause 1 TinyMT advance.
This occurs after 12 frames which would be enough to ruin everything. 
However, by unfreezing slowly using the D Pad + Select, let's say that this process is "postponed" for a few frames. 
This also the case for Route 9/17 even though I thought they were affected.
Hold the D Pad arrow until the encounter starts. The delay in those places is also 20 instead of 6 so keep that in mind.
* Tiny Finder supposes that all NPCs in an area are active. 
If you fight one of them accidentaly and stops moving afterwards, leave the area and return to enable them again.