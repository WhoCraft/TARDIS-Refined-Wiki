# Flight

The TARDIS can go anywhere and everywhere... within reason.

## Flight Limitations / Where can't you go

TARDIS Refined has hardcoded some limitations to the TARDIS's flight. 
1. The TARDIS cannot travel to the end whilst there is an active Ender-dragon.
2. The TARDIS cannot exceed the max world bounds, both up and down.
3. The TARDIS cannot land on the roof of the Nether

Server Owners and Modpack creators may wish to restrict what dimensions a TARDIS can travel to. A dimensional blacklist exists within the mod's configuration files which can be edited per-world.

## Starting Flight

The following must be true in order for the TARDIS to take off.

1. The Handbrake is disengaged
2. The Throttle is greater than 0.
3. The TARDIS has more than 5% fuel remaining.

## Flying the TARDIS

### Flight Events
During flight, the TARDIS will experience turbulence which may miss-align a control. You might be able to hear this happen, so keep your ears pealed.

A control's state can be viewed by looking at the icon to the left of its name. If a control has been misaligned, it will progressively get worse over time. In order to correct the control, interact with it until it is restored to it's green state.

You can use the AR Glasses to view misaligned controls as they happen.

![ar_glassed_particles.png](ar_glassed_particles.png)

If a control becomes too misaligned, it will no longer be able to be used and will remain damaged until flight has ended. Too many misaligned controls and the TARDIS will crash.

![control_accuracy.png](control_accuracy.png)

![control_red.png](control_red.png)

_Shown: A control nearly at the failing stage._

### Viewing Flight Progress
The flight progress can be seen by looking at Computer Bank.

### Burning Fuel
Flying great distances comes with a cost. During flight the TARDIS will consume fuel. Going faster burns the fuel faster.

![flight_progress.png](flight_progress.png)

## Ending Flight

### On flight end
Flight comes with rewards. The TARDIS will gain XP based on the distance travelled. If the TARDIS is less than 10% of fuel, a warning sound will echo through the TARDIS.

### Ending flight early 
If flight is ended before the TARDIS has reached the destination, it will land at how far it had progressed through the flight. There are four ways in which a flight might be ended early...

Safely by Pilot (Recommended)
: Set the throttle to 0 and then engage the handbrake.

Unsafe by Pilot
: Engage the handbrake whilst at speed.

Running out of Fuel
: Have the fuel drain before arriving.

Crashing
: Have too many damaged controls.

## So, you crashed.
As of Version 2.0, crashing the TARDIS doesn't do any permanent damage. Upon crashing the console will leak smoke and controls will burn to the touch. After 10 minutes, the console will cool down enough to be used again.

> For creative players, interacting with the console block holding an ice block will end the cooldown early.