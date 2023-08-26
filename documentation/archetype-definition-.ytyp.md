# 📇 Archetype Definition (.ytyp)

Archetype definitions (.ytyp) is basically the configuration file to define properties of objects.\
\
inside the .ytyp you will find multiple Archetypes, each archetype is for one object, there is 3 types of archetypes, Base, Time and MLO. Base is for .ydr, .ydd, .yft objects, Time archetypes are for time based objects such as window emissives that only show up at night. MLO archetypes are for MLOs (.ybn) objects.\


## Archetype Definitions UI Layout

* ![](<../.gitbook/assets/image (33).png>)\
  \
  Type: Archetype type (Base, Time, MLO)\
  Name: Archetype Name\
  Special Attribute: 0-13 (mainly used for doors)\
  Texture Dictionary: Texture dictionary (.ytd)\
  Clip Dictionary: Linked YCD Animation (.YCD)\
  Drawable Dictionary: \
  Physics Dictionary: Blank or same as Archetype Name if embedded\
  HD Texture Distance: Distance at what the HD Textures (+hi.ytd, +hidr.ytd) load\
  LOD Distance: Distance at which the object unloads\
  Asset Type: Assetless, Drawable Dictionary (.YDD), Drawable (.YDR), Fragment (.YFT), Unintialized\
  Asset Name: Same as Archetype Name\
  Linked Object: Object in blender scene linked to YTYP



## Achetype Flags

![](<../.gitbook/assets/image (34).png>)\
\
Unknown 1:\
Unknown 2:\
Unknown 3:\
Unknown 4:\
Unknown 5:\
Static: Freeze entity, disables physics\
Unknown 7:\
Instance: Used for procedural objects\
Unknown 9:\
Bone Anims (YCD): Enable Bone Animations\
UV Anims (YCD): Enable UV Animations\
Invisible but blocks lights/shadows:\
Unknown 13:\
Object Won't Cast Shadow: Disable shadows for object\
Unknown 15:\
Unknown 16:\
Double-Sided Rendering: Toggle Backface Culling\
Dynamic: Enable Physics\
Unknown 19:\
Unknown 20:\
Unknown 21:\
Unknown 22:\
Unknown 23:\
Unknown 24:\
Unknown 25:\
Unknown 26:\
Enable Special Attribute: Enable Special Attribute\
Unknown 28:\
Disable Red Vertex Colour Channel: Disable Red Vertex Colours\
Disable Green Vertex Colour Channel: Disable Green Vertex Colours (used alot for props)\
Disable Blue Vertex Colour Channel: Disable Blue Vertex Colours\
Disable Alpha Vertex Colour Channel: Disable Alpha Vertex Colours

Archetype Extensions\
\
![](<../.gitbook/assets/image (35).png>)
----------------------------------------

Used to add things like particles, ped spawns, ladders, and light shafts to be attached to the entity\


### CExtensionDefExpression

Used for:\
![](<../.gitbook/assets/image (36).png>)\
Name: Extension Name\
Expression Dictionary Name:\
Expression Name:\
Creature Metadata Name:\
Initialize on Collision:\
Offset Position XYZ: Extension offset relative to entity origin

### CExtensionProcObject

Used For: Attaching / Spreading procedural objects\
![](<../.gitbook/assets/image (37).png>)\
Name: Extension Name\
Radius Inner:  Inside radius of a circle around the extension\
Radius Outer: outside radius of a circle around the extension\
Spacing: Distance between procedural objects\
Min Scale: Lowest possible scale value\
Max Scale: Highest possible scale value\
Min Scale Z: Lowest possible scale value on the Z axis\
Max Scale Z: Highest possible scale value on the Z acis\
Min Z Offset: lowest possible offset on the Z Axis\
Max Z Offset: Highest possible offset on the Z Axis\
Object Hash: procedural object to use\
Flags: \
Offset Position XYZ: Extension offset relative to entity origin\


### CExtensionDefWindDisturbance

Used for:\
![](<../.gitbook/assets/image (38).png>)\
\
Name: Extension Name\
Offset Rotation XYZ: Extension rotation\
Disturbance Type:\
Bone Tag: Linked bone's Bone Tag(Optional?)\
Size XYZW:\
Flags:\
Offset Position XYZ: Extension offset relative to entity origin

### CExtensionDefSpawnPointOverride

Used For: Spawning / overriding ped spawns\
![](<../.gitbook/assets/image (39).png>)\
\
Name: Extension Name\
Scenario Type: Scenario type from .ymt scenarios\
iTime Start Override: When the override should start\
iTime End Override: When the override should end\
Group: Ped Group\
Model Set: Ped Model Set\
Radius: Radius of the Spawn Point Override\
Time Till ped Leaves: time until ped stops task (in minutes?)\
Available in MP/SP: Wether it is SP only or MP\
Scenario Flags:\
Offset Position XYZ: Extension offset relative to entity origin

### CExtensionDefSpawnPoint

Used For: Attaching peds / ped scenarios to objects\
![](<../.gitbook/assets/image (40).png>)\
\
Name: Extension Name\
Offset Rotation XYZ: Extension rotation\
Spawn Type:\
Ped Type:\
Group: Ped Group\
Interior: Interior Name(if inside one)\
Required Map:\
Probability: Chance for the scenario to spawn\
Time Till Ped Leaves: time until ped stops task (in minutes?)\
Radius: Radius of the Spawn Point\
Start: Time the scenario starts\
End: Time the scenario ends\
High Priority: Prioritizes spawning of scenario\
Extended Range: Extend range at which the scenario can spawn relative to the player\
Short Range: Decrease range at which the scenario can spawn relative to the player\
Available in MP/SP: Wether it is SP only or MP\
Scenario Flags:\
Offset Position XYZ: Extension offset relative to entity origin

### CExtensionDefLightShaft

Used For: Light Rays / God Rays\
![](<../.gitbook/assets/image (41).png>)\
![](<../.gitbook/assets/image (42).png>)\
\
Density Type: How dense the light shaft should be\
Volume Type: Shape of the shaft\
Scale By Sun Intensity: Use in game sun intensity to effect brightness\
Direction Amount:\
Length: Length of the Light Shaft\
Color: Color of the Light Shaft\
Intensity: Intensity of the Light Shaft\
Flashiness: Flags for how fast and if the Light Shaft should flash / flicker\
Flags:\
Fade In Time Start: When the Light Shaft should begin to appear\
Fade in time End: when the Light Shaft is fully visible\
Fade Out Time Start: When the Light Shaft should begin fading away\
Fade Out Time End: when the Light Shaft Shouldnt be visible\
Fade Distance Start: Distance at which the Light Shaft begins Fading\
Fade Distance End: Distance at which the Light Shaft is fully Faded\
Softness:\
\
![](<../.gitbook/assets/image (43).png>)\
\
Corner A XYZ: Top Left Corner Coords\
Corner B XYZ: Top Right Corner Coords\
Corner C XYZ: Bottom Right Corner Coords\
Corner D XYZ: Bottom Left Corner Coords\
\
Offset Position XYZ:  Extension offset relative to entity origin
