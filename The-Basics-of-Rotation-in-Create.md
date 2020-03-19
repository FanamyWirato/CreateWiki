Some of the most prominent machines and components require **Rotational Force** to operate. Sometimes the provided rotation speed and direction reflects their behaviour, and some components may have a more significant _cost_ than others. Trying to understand how exactly these components work together can become difficult so we recommend reading these 3 articles in order to help with that.

1. [[Generate & Convey|Generate and Convey]]
2. [[Changing Gear|Changing Gears]]
3. [[Stress & Capacity|Stress Units, Capacity and Impact]]

If you have already used Create 0.1 in the past and are familiar with rotation and speed, you may be able to catch up with the 0.2 update by just reading the paragraph below

## Stress & Capacity

_In Create 0.2+, a bit of balance had been brought to rotational power: something to resemble torque in a highly simplified fashion._ 

Rotational generators have limited capacity for what they power. "Stress Impact" and "Stress Capacity" are the two opposing values in a kinetic network: **generators add capacity, machines and components add impact**. If the capacity is exhausted, all connected parts will simply stop moving, until capacity is increased or stress is relieved again.
**Stress Impact is tied to rotation speed**. Increasing the speed increases a components stress impact or capacity proportionally. 

Consider the following example: 
Assume one Water Wheel can provide just enough power in order to power four fans at the same speed. 
* Doubling the speed of the fans using cogwheels will make the fans blow stronger, but the network will cease to function until the count of fans is halved, or the count of water wheels is doubled. 
* Similarly, you would be able to power eight fans running at half the speed of the water wheel.

By default, components used **only for relaying** rotational power, such as shafts and cogwheels, have **no stress impact** at all. This makes predicting the amount of generators required for your contraptions much simpler and prevents punishment for aesthetic detours between machines and generators.

Optimizing stress impact and comparing net capacity of sources at base speed can become quite scientific. For those who are interested in some more exhaustive information, check out [[this page|Stress Units, Capacity and Impact#SU and Speed]]