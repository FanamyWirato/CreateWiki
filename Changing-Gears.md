Just alone having Components rotate is not enough however, sometimes some more control over the speed of rotation is needed. This is especially important for machines that require a _minimum level of speed_ to operate (e.g. the Mechanical Mixer). To make this possible, some kinetic blocks have the ability to _speed up_ or _slow down_ connected components:

### Cogwheels

Cogwheels are not only useful for relaying rotation but can also serve as a simple way to control the speed. By attaching a large cogwheel diagonally to a regular sized one like seen below you can double/half the speed of the other.

 &nbsp; &nbsp; &nbsp; ![](https://cdn.discordapp.com/attachments/622867820170182676/690188497910628382/Annotation_2020-03-19_142022r.png) <br>
Powering the _large cogwheel_ results in the _smaller_ one turning at **double** the speed<br>
Powering the _small cogwheel_ results in the _larger_ one turning at **half** the speed

### Analog belt Pulley

The belt pulley is used in combination with encased belts to give some finer control over speed than the cogwheels allow for. It can be viewed as an _input_, when powering other connected belts or as an _output_, when powered from belts instead.

While acting as an input it will increase the speed of attached belts based on the analog redstone signal it recieves. A full power of 15 will double all belt's speed while values below will interpolate the factor from 2x to 1x accordingly.<br>
![](https://cdn.discordapp.com/attachments/622867820170182676/690208484377231400/Annotation_2020-03-19_154031r.png)

While acting as an output, it will decrease the speed of connected shaft instead. A full power of 15 will half the speed and values below will interpolate the factor from 0.5x to 1x accordingly.<br>
![](https://cdn.discordapp.com/attachments/622867820170182676/690207594568089602/Annotation_2020-03-19_151829r.png)

When not being powered, the belt pulley won't affect the speed at all and just behave like a encased belt.

### Rotation Speed Controller

While having a more expensive recipe, the RSC also has the finest control over speed change. When a large cogwheel is attached to the controllers top, it will try its best to keep it spinning at the speed configured in the scroll field. When holding down _shift _while scrolling, the speed will increase/decrease by only 1.

![](https://cdn.discordapp.com/attachments/622867820170182676/690195537252974672/Annotation_2020-03-19_144335r.png)

### Overpowering

Connecting faster components to other slower components **directly** will cause the faster network to overpower the rest, alinging the speed of everything that is now part of it. (That is, if the direction lines up) 