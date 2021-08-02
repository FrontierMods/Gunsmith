# Sanity Checks

## Assembly Sequence

Because the game was never designed with this system in mind, there is currently no way to determine certain components as essential for the operation of the gun or as providing some particular functionality.

As such, some components had to be gated behind one another: that is, restricted from installation until the previous necessary part is installed. This is sometimes an unfair practice, but a necessary component to making the mod provide reasonable limits of the assembly process.


## Receiver as a Gun

[*relevant issue*](https://github.com/FrontierMods/Gunsmith/issues/2)

Due to the way the game handles firearms, the mod has to designate the receiver – the part that is typically only a structural one – as an active, usable gun. As per the game engine, this means the lower receiver void of actual mechanical components

* has a default caliber it can take
* accepts magazines loaded with that caliber
* can actually fire the ammo provided

The current implementation of the mechanism to prevent it from being used as a firearm relies on an error. When moving the cursor away from the character during firing a stripped lower, you should get the error about exceeding range. It's safe to ignore, as it does not prevent finished weapons from aiming or firing.


## Pins and Small Furniture

The mod doesn't model the installation of pins and other small furniture required to keep bigger parts in place. This includes gas tubes.

While ultimately it renders the resulting weapons lighter by several dozen grams, the upsides of this unrealistic rendition are

* simpler assembly and part management
* fewer loose parts lying around
* easier assembly process modelling

Embracing small details like this may be possible in the future with an updated gunmod system. It would make the process that much more precise. However, at this stage, the decision was taken to leave such details behind.