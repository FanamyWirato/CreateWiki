The **cogwheel** is a basic mechanical component in Create that relays rotation. When two cogwheels are adjacent, if [rotational force](The-Basics-of-Rotation-in-Create) is provided to either cogwheel, this force will also be provided to the other cogwheel.

The **large cogwheel** is a larger variant of the cogwheel that can relay rotation around corners and power [[Rotation Speed Controllers|Rotation Speed Controller]].

## Connecting components

Cogwheels have three main methods of interlocking:
* Two cogwheels can be placed on the same face of two adjacent blocks. As such, when rotational force is provided to one of the cogwheels, equivalent force will be provided to the other cogwheel at the same speed but in the opposite direction.
* Two large cogwheels can be placed on adjacent faces of the same block, allowing for rotational force to be conveyed around corners. As above, speed will not be changed but direction will be reversed. Note that large cogwheels placed on three adjacent faces cannot rotate.
* A cogwheel and a large cogwheel can be placed on the same face of two diagonally adjacent blocks. The large cogwheel will rotate at half the speed of the other.

In addition to connecting rotational force between adjacent cogwheels, a cogwheel can frequently be used like a [[shaft]], allowing mechanical components to be connected to each end. This can also be used to connect multiple cogwheels along the same axis.

## Adjusting speed
Using the aforementioned mechanic of changing speed between cogwheels and large cogwheels, the speed of a component can be easily doubled or halved. This is useful for powering mechanical components that require a minimum rotation speed, such as the [[Mechanical Mixer]]. Connecting large and small cogwheels along the same axis can be used to apply this mechanic repeatedly as a gear train, able to multiply or divide speed by any power of two, provided that no mechanical component rotates more quickly than Create's speed limit of 256 RPM.

Alternatively, a large cogwheel can be connected to a [[Rotation Speed Controller]], which can be used to compactly adjust speed with great precision.