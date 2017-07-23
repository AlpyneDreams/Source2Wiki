<details>
<summary>Current steamtours.fgd</summary>

```java
//===================== Copyright (c) Valve Corporation. All Rights Reserved. ======================
//
// Defines entity classes specific to Destinations Mod
//
//==================================================================================================

@include "base.fgd"
@include "lights.fgd"
@include "ai_basenpc.fgd"

@helpinfo( "Destinations", "tools/help/fgd/steamtours.txt" )

//-------------------------------------------------------------------------
//
// NPCs
//
//-------------------------------------------------------------------------

@BaseClass base(BaseNPC) = BaseBird
[
	input FlyAway( void ) : "Forces the bird to fly to a nearby crow flyto hint node."
	input FlyPath( string ) : "Forces the bird to fly the path, starting with the specified path corner. Bird must have line of sight to the specified path corner."
	input FlyToHint( string ) : "Forces the bird to fly to the specific crow flyto hint node."

	deaf(choices) : "Deaf?" : 0 =
	[
		0 : "No."
		1 : "Yes. Ignore sounds."
	]
]

@NPCClass base(BaseBird) editormodel("models/creatures/crow/crow.vmdl") = npc_crow : "Crow"
[
]

@NPCClass base(BaseBird) editormodel("models/creatures/seagull/seagull.vmdl") = npc_seagull : "Seagull"
[
]

@NPCClass base(BaseBird) editormodel("models/creatures/pigeon/pigeon.vmdl") = npc_pigeon : "Pigeon"
[
]


//-------------------------------------------------------------------------
//
// Misc entities
//
//-------------------------------------------------------------------------

@PointClass base(BasePropDoorRotating) model() = prop_door_rotating :
	"An entity used to place a door in the world. If two doors have the same name, they will open and close together as double doors."
[
]


@SolidClass base(worldbase) = worldspawn : 
	"This is the world entity. Each map can only contain one, and it's automatically created for you."
[
	pvstype(choices) : "Precomputed Visibility" : 0 : "" = 
	[
		0 : "Disabled"
		1 : "Test map (open space, no skybox)"
		10 : "Full visibility solve"
	]
]


@PointClass
	iconsprite( "materials/editor/env_fog_controller.vmat" )
	base( Targetname )
	gradientfog()
= env_gradient_fog
[
	fogstart(float) : "Fog Start Distance" : "0.0"
	fogend(float) : "Fog End Distance" : "4000.0"
	fogstartheight(float) : "Fog Start Height" : "0.0"
	fogendheight(float) : "Fog End Height" : "200.0"
	farz(string) : "Far Z Clip Plane" : "-1"
	gradientfogtexture(resource:texture) : "Fog Gradient Texture" : "materials/effects/example_gradient_fog.vtex"
]

//-------------------------------------------------------------------------
//
// Teleport entities
//
//-------------------------------------------------------------------------

@PointClass base( Targetname ) editormodel( "models/effects/teleport/teleport_marker.vmdl" ) = vr_teleport_marker
[
	locked(boolean) : "Locked" : "No"
	forwarding(boolean) : "Forwarding" : "No"
	info(boolean) : "Info" : "No"
	StartsAsCurrent(boolean) : "Starts As Current" : "No"

	// Outputs
	output OnTeleportTo(void) : "Fired when a player teleports to this teleport marker."
	output OnTeleportFrom(void) : "Fired when a player teleports away from this teleport marker."
]

@SolidClass base( Targetname, PhysicsTypeOverride_Mesh ) = vr_teleport_area
[
]

//-------------------------------------------------------------------------
//
// UI entities
//
//-------------------------------------------------------------------------

@PointClass base( Targetname ) orientedwidthheightfixed( 45, 70 ) = point_clientui_steamvr_world_panel :
	"An entity used to place one of the SteamVR breakout panels in the world"
[
	panel_type(Choices) =
	[
		0: "Recent Apps"
		1: "Friends"
		2: "Public Lobbies"
	]
]

@PointClass base( Targetname ) = flex_background
[
	sequenceName(string) : "Sequence Name"
	defaultSequenceName(string) : "Default Sequence Name"
	model(resource:model) : "Model"

	// Inputs
	input SetSequence(string) : "Sets the script model's sequence."
	input SetDefaultAnimation(string) : "Set the Default Animation to the one specified in the parameter."

]

@PointClass base(BasePropPhysics, BaseFadeProp) model() sphere(fademindist) sphere(fademaxdist) = prop_destinations_physics :
	"A prop that is picked up on use."
[
	frozen(boolean) : "Frozen" : "No"
]

@PointClass base(BasePropPhysics, BaseFadeProp) model() sphere(fademindist) sphere(fademaxdist) = prop_destinations_tool :
	"A prop that when picked up, can attach to the player's hand and have additional functionality which is defined in the vscript."
[
	HasCollisionInHand(boolean) : "Has Collision When Held" : "No"
]
```
</details>

<details>
<summary>Removed Lighting Entities</summary>

```java
@PointClass
	iconsprite( "materials/editor/light_sky.vmat" )
	bakeskylight( color, intensity, lower_hemisphere_is_black )
= light_sky
[
	color(color255) : "Color" : "255 255 255"
	intensity(float) : "Intensity" : "1.0"
	lower_hemisphere_is_black(boolean) : "Lower Hemisphere Is Black" : "1"
]

@PointClass
	iconsprite( "materials/editor/light_ambient.vmat" )
	bakeambientlight( color )
= light_ambient
[
	color(color255) : "Color" : "255 255 255"
]

@PointClass
	iconsprite( "materials/editor/light_ambientocclusion.vmat" )
	bakeambientocclusion( max_distance, weight )
= light_ambientocclusion
[
	max_distance(float) : "Max Distance" : "512.0"
	weight(float) : "Weight" : "1.0"
]
```
</details>