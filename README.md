# Gunsmith

*Gunsmith* is a mod for *Cataclysm: Dark Days Ahead*.

It overhauls the gun modification system by providing a more in-depth view into the process. As a benefit, this overhaul also allows players to build their firearms from found parts.


## The Process of Assembly

Understanding the process of firearm assembly is essential for both gunsmithing and modification of the gun with this mod.

Refer to [~`/ASSEMBLY_GUIDES/`~](/ASSEMBLY_GUIDES/) for overview and detailed guides for each firearm platform.


## Sanity Checks

While this mod's main goal is to produce an accurate and meaningful firearm assembly / modification process, in some ways it is limited by the game engine.

The measures taken to address or overcome said limitations are referred to as *sanity checks*. This section goes on to review the checks in order to provide players with a greater understanding of using this mod.

The author's hope is to be able to address these issues over time, either via the game engine or on the mod side.


### Assembly Sequence

Because the game was never designed with this system in mind, there is currently no way to determine certain components as essential for the operation of the gun or as providing some particular functionality.

As such, some components had to be gated behind one another: that is, restricted from installation until the previous necessary part is installed. This is sometimes an unfair practice, but a necessary component to making the mod provide reasonable limits of the assembly process.


### Receiver as a Gun

Due to the way the game handles firearms, the mod has to designate the receiver – the part that is typically only a structural one – as an active, usable gun. As per the game engine, this means the lower receiver void of actual mechanical components

* has a default caliber it can take
* accepts magazines loaded with that caliber
* can actually fire the ammo provided

The current implementation of the mechanism to prevent it from being used as a firearm relies on an error. When moving the cursor away from the character during firing a stripped lower, you should get the error about exceeding range. It's safe to ignore, as it does not prevent finished weapons from aiming or firing.


# License

MIT