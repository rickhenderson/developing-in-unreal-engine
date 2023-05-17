# Use Custome Player Character in Unreal Engine 5.1

## Create an Animation Blueprint

<img src="assets\new-animp-bp.png">

The Output Pose determines what action will be displayed by the player. The State Machine stores the various "states" of motion such as idle/walk/run (typically called the Locomotion state) and jumping.

The **Default Slot** is needed for when you want to add sequences called **Animation Montages** which can be used for combat animations and other things.

*The next steps can be done before or after creating the Blend Space.*

### Create the State Machine

<img src="assets\locomotion-state-machine.png>

In the Animation Blueprint Event Graph, use Character Movement to determine if the character is walking, and promote that to a variable to use in other blueprints.

<img src="assets\abp-determine-walk-speed.png">

* Determine how the character transitions between walking, jumping, and running in the Locomotion state (idle/walk/run).

<img src="assets\locomotion-walk-jump-transition.png">

Using the "Equal" node is an added safety to make sure nothing funny happens (tip from Production Crate).

Here is the rule for moving from jumping back to walking.

<img src="assets\locomotion-is-not-jumping.png">

You should now be ready to add animations to a **Blend Space**.

## Create a Blend Space for animations

A blend space is used to not only change from one animation state to another such as walking to running or running to jumping, it can automatically generate animations for *in between* poses as well.

In previous versions of Unreal, a BlendSpace1D may have been used but this section will show the power of a 2D BlendSpace in Unreal 5.1. The 1D blend space is still available (right-click > Animation > Legacy > BlendSpace1D).

The new BlendSpace allows for your character to change animations as it changes directions, but we'll simply set it up so you can add that later. For now, we just want to walk and run.

* Create the new BlendSpace asset.

The Walk Speed of your character (also called velocity - or technically the length of the velocity vector) starts at 0 when not moving. Unreal has a basic run speed of 600. You can have your character have a walk speed of 300, but some animations may look better at a speed of 150. You may want to experiment. Speedsters can go even faster if you want to add a speed boost :).


### Resources

* [How To Make An Animation Blueprint In Unreal Engine 5 | How To Animate A Character - UE5 Tutorial](https://youtu.be/TE-SsP3pigs)
* Video by ProdctionCrate