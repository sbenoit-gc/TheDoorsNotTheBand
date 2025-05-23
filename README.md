# Project Name  TheDoorsNotTheBand

<img src="Saved/AutoScreenshot.png" width="320"  align="right" />

## Descripton

A github repository for the in-class automatic opening door discussion. 

## Usage
Used as one of the weekly demonstrations, just a collection of examples as we explore UE5

Clone, or download the zip, to a local directory. Open in Unreal Engine 5.4 

Four versions of door blueprints are demonstrated.

### BP_DoorPopOpen<br>
Uses 2 static meshes and a large collision box around door to implement automatic door that pops open when player approaches. Uses the set relative rotation node. 

### BP_DoorSwingOpen<br>
Same as above but uses a TimeLine node and LERP to gradually swing door open close s layer approaches.

### BP_DoorInteractToOpen<br>
Similar to above but the main collision box is used to enable input when player is near, instead of opening door. We added new InputAction to the system, IA_Interact and bound the F key to it. With player in the collision box, input is enabled and the player can pass the F key to interact with the door, ie open or close it. Optionally, the door closes when player leaves the collision box. Note the addition of a second collision box nested under the door mesh. This second collision box is sized similar to the door and has its collision setting set to BlockAll in order to prevent the layer from walking through the closed door.

### BP_DoorInteractToOpenWithKey<br>
Same as above but the status of the player object's HasKey? boolean is checked. If it's true, the player is allowed to interact with door by pressing F to open/close door.

### NOTE:<br>
This example does NOT use blueprint interface (BPI) methodology which would be a better implementation of object interactions. We will discuss BPI in a future lesson.

## Attributions: 
Door sound, OpenGameArt ; < https://opengameart.org/content/202-more-sound-effects >
