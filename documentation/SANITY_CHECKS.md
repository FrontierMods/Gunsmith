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

While ultimately it renders the resulting weapons several dozen grams lighter, the upsides of this unrealistic rendition are

* simpler assembly and part management
* fewer loose parts lying around
* easier assembly process modelling

Embracing small details like this may be possible in the future with an updated gunmod system. It would make the process that much more precise. However, at this stage, the decision was taken to leave such details behind.


## Specific to the AR-15 Platform


### Mil-Spec vs. Commercial Buffer Tubes

There exist two standards of buffer tubes – the part that serves mostly to house components that counter recoil – for the AR-15 and similar platforms: *mil-spec* and *commercial*.

Briefly: the difference between them amounts to a few parts of an inch in diameter. In reality, this amounts to either being unable to install mil-spec stock onto a commercial buffer tube, or noise during shooting when installed vice versa.

While it's certainly possible to do the latter, in the game it's restricted. Since there's no way to coordinate gunmods, it would be impossible to apply a debuff to an ill-fitting part of the mechanism.

As such, installation of commercial stocks on mil-spec buffer tubes is prohibited until there's a way to handle it more meaningfully.


### Buffer Tube Sizes

AR-15-platform buffer tubes come in several sizes. The most common are: *pistol*, *carbine*, and *rifle*.

In reality, gunsmith must be mindful of these sizes because other buffer components ­– the buffer and the buffer spring – are designed with these in mind: using incompatible parts is possible, though likely to damage the parts over time.

In Gunsmith, this means forcibly separating components by intended size.

Where this comes into play as a sanity check is a niche type of stocks, called *stock plates* among other things. These only ever latch on the very tip of the buffer tube and don't require any specific tube length to serve its purpose.

As it stands, it's impossible to allow installing stock plates onto all lengths of buffer tubes without some unnecessary and tiresome voodoo, on both the developer and the player side of things. As such, stock plates are instead restricted to a handful of buffer tubes that were specifically intended to only accept stock plates.


### Buffer Weights and Caliber

Ordinarily, the weight of the buffer corresponds with how much it reduces felt recoil. The heavier the buffer, the less the recoil.

Buffer is also responsibly for properly cycling the rifle after firing: balancing bolt carrier group and buffer is important for achieving appropriate rate of cycling, which reduces chances of jamming at the point of case ejection.

Because of operational differences with different calibers, AR-15-platform rifles require a much heavier buffer in order to balance things with the caliber's bolt carrier group.

Restricting heavier buffers to smaller calibers seems a step to far for the mod: there are legitimate uses for heavier buffers in rifle-caliber BCGs. The closest Gunsmith gets to managing this disparity is by significantly increasing the amount of recoil experienced by the firearm with a smaller-caliber BCG installed, thus effectively requiring a heavier buffer.

The main issue of this compromise is that it leaves out the negative effects of an overly-heavy buffer: no bolt carrier malfunction can occur because of a mismatch in weight/momentum between the two parts. In other words, this means heavier buffers are automatically always better than lighter ones as far as recoil is concerned.


### Barrel Length vs. Handguard Length

In reality, it's highly recommended that the muzzle end of your rifle would end up farther than the end of the handguard. If handguard ends up covering the muzzle, the heat and carbon dust from the exiting gases may damage the handguard.

Because there's no way to coordinate gun parts, there's no way to limit installing barrels of certain length with handguards of certain length, or vice versa.

Establishing a length system similar to that of buffer tubes and stocks is one solution, but the fact that the mod would have to manage these limitation in three dimensions (barrel vs. handguard vs. gas system; see below) makes for a miserable development experience, nevermind gameplay.

At present, barrels of any length could be installed with handguards of any length.


### Barrel Length vs. Gas System Length

Because there's no way to coordinate gun part parameters, gas systems are mostly left out of the process of gunsmithing. Installing the gas system on an AR-15-platform rifle correctly is important in reality, so simulating it within Gunsmith is desirable.

Ordinarily, the length of the gas system (distance from bore to gas block) would define overall reliability of the rifle: it dictates how much gas comes against the bolt carrier and how quickly, affecting recoil and internals fouling from the carbon dust of the captured gases. Pistol-length barrels, for example, would require installing shorter gas systems, which would put a lot more pressure on the cycling mechanism, thus potentially damaging the components involved.

Because there's no way to coordinate gun parts, this important aspect is left out. It's assumed under the [*Pins and Small Furniture*](#pins-and-small-furniture) sanity check to be adequately supplied by default.

Another important aspect of this system missing is the fact that the original Colt gas block also plays the part of the front iron sight – a fact that several popular handguards use for their design.