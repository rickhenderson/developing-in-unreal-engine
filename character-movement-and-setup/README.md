# Movement Setup

Much of this information for the player character can be applied to AI controlled NPCs as well. You may want to consider fully fleshing out the movement of your player characater, and then making the AI NPCs a child class of your character.

## Basic Walking and Moving

* Download Assets from Mixamo
* Download first just the character in T-Pose
* For every animation, download without the skin.

### Setting Up the BlendSpace

* To allow the animation blueprint to implment idle/walk/run as a single state, you need to place the 3 animations into a BlendSpace.
* The legacy 1D BlendSpace is still avaible in the Legacy menu, but you should use the 2D blendsplace from now on.

This image uses the new 2D BlendSpace, but is only using the Speed variable on one the horizontal axis.

<img src="move_2d-blendspace.png">

This image shows the BlendSpace for the Animation Starter Pack, available from the [Unreal Marketplace](https://www.unrealengine.com/marketplace/en-US/product/animation-starter-pack).

<img src="move_2d-blendspace.png">



# Vault

<img src="assets\vault-stage-01.png">

<img src="assets\vault-02-calc-forward-distance-blueprint.png">
Note that if you find that your line traces keep ending at the back corner (0,0,0) then the End Position is not calculated properly. Make sure you have added the starting location.

