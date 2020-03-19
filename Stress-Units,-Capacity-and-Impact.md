![](https://i.imgur.com/E3wHL9a.jpg)

### Stress

Now that we have [[Rotation|Generate and Convey]] and [[Speed|Changing Gears]] covered we need to talk about the last important mechanic: _Stress_. Stress is Create's simplified implementation of torque that allows for some balancing around rotation. To understand stress, we have to split components into 2 groups, _Generators_ and _Consumers_. Generators have a certain _Stress Capacity_ associated with them, while Consumers have a _Stress Impact_. As long as the total capacity of a system is greater or equal to the total impact the system will turn and all components will work. If however the total stress impact gets to large, the system will Overstress preventing all components from working. This state persists until either the impact gets lowered or some capacity added.

### SU and Speed

The amount of Stress a component has also scales with its current speed. All components have a certain _Base Value_, which refers to a speed of _1 RPM_. To get the effective impact or capacity all you need to do is multiply that base value by its current speed. For example a water wheel (base value of 32 SU) turning at 5 RPM will add a total of 160 SU of capacity to the system, while the same wheel turning at 10 RPM will add 320 SU. The same logic applies to consumers: A crushing wheel running at 20 RPM adds 640 SU of impact to the system.

By default, components used **only for relaying** rotational power, such as shafts and cogwheels, have **no stress impact** at all. This makes predicting the amount of generators required for your contraptions much simpler and prevents punishment for aesthetic detours between machines and generators.

### Quick Example

In the end this means that if you want to run 2 crushing wheels you'll need 2 water wheels running at the same speed or you can get away with just a single one if you slow down the crushers to half its speed instead. Read more about changing speeds [[here|Changing Gears]]

***

### Goggles and Gauges

Optimizing stress impact and comparing net capacity of sources at base speed can become quite scientific. For those who are interested in seeing some actual numbers and more exhaustive information, it is recommended to look into crafting a pair of Goggles and a Stress Gauge:

Stats of a water wheel turning at 10 RPM: 

![](https://cdn.discordapp.com/attachments/622867820170182676/690166859856609280/unknown.png)

Stats of a crushing wheel working at 20 RPM:

![](https://cdn.discordapp.com/attachments/622867820170182676/690167926669705249/unknown.png)

Example of a stress gauge:

![](https://cdn.discordapp.com/attachments/622867820170182676/690179829395488996/unknown.png)
