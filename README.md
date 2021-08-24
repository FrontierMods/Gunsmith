# Gunsmith

*Gunsmith* (`gunsmith`) is a mod for *Cataclysm: Dark Days Ahead*.

It overhauls the gun modification system by providing a more in-depth view into the process. As a benefit, this overhaul also allows players to build their firearms from found parts.


## Status

*Gunsmith* is currently in **DEMO 1**.

**DEMO 1** is a non-playable (i.e. unusable in a genuine playthrough) demonstration of the potential of an enhanced gunmod system. It overhauls the AR-15, an extremely modular rifle platform, and adds hundreds of new parts for dozens new slots. Overall, the overhauled system resembles the real gunsmithing experience (without the tools and the time requirements) closely.

The goal of **DEMO 1** is to gauge public interest and get feedback on both the concept and the details of implementation. Use debug menu to spawn the entire pack of additions or separate new parts, and leave your impressions in the Discussions section, and criticism or feature requests – in the Issues section.

**NOTE**: this mod, including demo versions, is compatible with the latest stable release only.


### Getting the New Stuff

Use the debug menu to spawn an item called `Gunsmith Demo 1 package`. Deconstruct the package to receive one of every single part available for the AR-15. The package includes an "empty" AR-15 (i.e., the lower receiver) from which you can start a fresh assembly, as well as two example pre-assembled AR-15s, to visually demonstrate the potential difference all the parts make.

Alternatively, use the debug menu to spawn each item individually.

Because the guns assembled this way must follow a protocol of sorts, use [this guide](/documentation/ASSEMBLY_GUIDES/ar15.md) to figure out how to build an awesome AR-15 from scratch.

Try using duct tape as a grip wrapper for the pistol grip, for enhanced handling. Some forward grips can receive a grip wrapper too.


### Known Issues

1. Most parts don't add length to the gun when attached. This is a base game limitation.
2. Conversion of AR-15 to different calibers (e.g. 9mm, for which the parts exist) doesn't work. The cause is unknown.
3. The bare lower receiver has all the characteristics of a firearm, yet causes an error when aiming with it is attempted. This has been taken into account. The error is safe to ignore. Fully assembling the firearm (see below) will result in a perfectly functional rifle.
4. Replacing an "early" part removes all the "later" parts (e.g. removing upper receiver removes everything from barrel to foregrips to sights). See below for explanation, or follow [this guide](/documentation/ASSEMBLY_GUIDES/ar15.md). Sorry for the tedium.
5. Pre-assembled example rifles are likely to crash when disassembly is attempted. The cause is unknown. Make sure to save before attempting disassembly in order to have a save point to return to in case of a crash.
6. There are no rifle-length buffer tubes in Demo 1, nor are there pistol-length stocks. There are also no commercial stocks of any kind. This is a limitation of research.
7. Migration does not transform, remove, or replace base-game generic attachment with new specific ones. The cause is unknown.
8. The built-in titanium material declaration throws errors during loading. These are safe to ignore.


# Gameplay & Design

## The Process of Assembly

Understanding the process of firearm assembly is essential for gunsmithing with this mod.

Refer to [`/documentation/ASSEMBLY_GUIDES/`](/documentation/ASSEMBLY_GUIDES/) for overview and detailed guides for each firearm platform.


## Sanity Checks

While this mod's main goal is to produce an accurate and meaningful firearm assembly / modification process, the mod remains limited by the game engine.

The measures taken to address or overcome said limitations are referred to as *sanity checks*. Refer to [`/documentation/SANITY_CHECKS.md`](/documentation/SANITY_CHECKS.md) for the complete up-to-date list. The author's hope is to be able to address these issues over time.


# License

MIT