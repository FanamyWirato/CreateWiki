Just alone having components rotate is not enough.  Sometimes more control over the speed of rotation is necessary. This is especially important for machines that require a _minimum level of speed_ to operate (e.g. the Mechanical Mixer). To make this possible, some kinetic blocks have the ability to _speed up_ or _slow down_ connected components:

### Cogwheels

Cogwheels are not only useful for relaying rotation but can also serve as a simple way to control the speed. By attaching a large cogwheel diagonally to a regular sized one, as seen below, one can double/half the speed of the other.

 &nbsp; &nbsp; &nbsp; ![](https://cdn.discordapp.com/attachments/622867820170182676/690188497910628382/Annotation_2020-03-19_142022r.png) <br>
Powering the _large cogwheel_ results in the _smaller_ one turning at **double** the speed<br>
Powering the _small cogwheel_ results in the _larger_ one turning at **half** the speed

### Analog Belt Pulley

The Analog Belt Pulley, when used in combination with encased belts, gives finer control over speed than cogwheels. It can increase _input_ speed for attached belts, or decrease _output_ speed of shafts connected to belts.

While acting as an input, the Analog Belt Pulley will increase the speed of attached belts based on the analog redstone signal it receives. A full power of 15 will double all belts' speed while values below will interpolate the factor from 2x to 1x.<br>
![](https://cdn.discordapp.com/attachments/622867820170182676/690208484377231400/Annotation_2020-03-19_154031r.png)

While acting as an output, the Analog Belt Pulley will decrease the speed of connected shaft. A full power of 15 will half the speed and values below will interpolate the factor from 0.5x to 1x.<br>
![](https://cdn.discordapp.com/attachments/622867820170182676/690207594568089602/Annotation_2020-03-19_151829r.png)

When unpowered, the belt pulley will not affect the speed at all and behaves like an encased belt.

### Rotation Speed Controller

While having a more expensive recipe, the RSC also has the finest control over speed change. When a large cogwheel is attached to the controllers top, it will try its best to keep it spinning at the speed configured in the scroll field. When holding down _shift_ while scrolling, the speed will increase/decrease by 1.

![](https://cdn.discordapp.com/attachments/622867820170182676/690195537252974672/Annotation_2020-03-19_144335r.png)

### Overpowering

Connecting faster components to other slower components **directly** will cause the faster network to overpower the rest, aligning the speed of the component network (that is, if the direction lines up). 