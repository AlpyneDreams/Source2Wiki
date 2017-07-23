Almost all of these strings are probably from around 2015-2017, most were retrieved from Robot Repair. Some of these later found their way into Destinations as well.

### Entities (hl3.txt leak of FGD file help info from Dota 2)
- item_generic
- prop_zipline
- shared_procedural_spawn_template_info
- shared_procedural_spawn_reuse_info
- shared_procedural_spawn_area_info
- shared_enable_disable
- info_procedural_spawn_template
- info_procedural_spawn_target
- info_procedural_spawn_manager
- info_procedural_spawn_subgroup
- func_procedural_spawn_volume
- procspawn_var_volume
- procspawn_var_entity
- procspawn_constraint_volume_volume_distance
- procspawn_constraint_target_volume_distance
- procspawn_constraint_target_in_volume
- procspawn_constraint_target_near_entity
- procspawn_constraint_target_far_from_class
- procspawn_constraint_subgroup_distance
- procspawn_constraint_target_facing_player
- procspawn_modifier_rotation_traced
- procspawn_modifier_move_traced
- procspawn_modifier_2joint_traced
- npc_quest_citizen
- npc_hunter_invincible
- npc_turret_ceiling_pulse
- info_quest_dialog
- prop_fixed
- point_quest_goal
- procspawn_bias_linetoplayer
- logic_player_volume_tracker

### CPP Paths
```
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl2\weapon_spygrenade.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl2\weapon_stunstick.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl2\weapon_stunstick.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl2\weapon_zipline.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl2\weapon_zipline_bolt.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\entity_persist.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\gravity_vortex_controller.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\info_quest_dialog.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\npc_quest_citizen.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\npc_quest_citizen.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\npc_turret_ceiling_pulse.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\partial_entity_manager.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\point_quest_goal.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_constraint.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_constraint.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_manager.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_manager.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_target.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_target.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_template.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_template.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_volume.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procedural_spawn_volume.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procspawn_bias_line.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procspawn_bias_line.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procspawn_modifier.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\procspawn_variable.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\prop_fixed.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\hl3\utllogicconstraintsolver.h

c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\info_spawngroupstream.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\info_spawngroupstream.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\info_worldlayer.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\info_worldlayer.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\inforemarkable.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\intermission.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\item_generic.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\item_generic.h
c:\buildslave\vrgdc2015_staging_win64\build\src\game\server\item_world.cpp

c:\buildslave\vrgdc2015_staging_win64\build\src\game\shared\prop_zipline.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\shared\hl3\hl3_vscriptgamesystem.cpp
c:\buildslave\vrgdc2015_staging_win64\build\src\game\shared\hl3\imposter_manager.cpp

c:\buildslave\vrgdc2015_staging_win64\build\src\game\client\hl3\c_point_quest_goal.h
```

### Other Leaks


source1import_txtmap.txt
```
"models\headcrab.mdl"
{
	"mod"				"hl3"
	"importfunc"			"importMDLtoVMDL"
	"getSkinningFromLod0"	"1"
}
```

hl3_usermessages.proto
```protobuf
enum HL3UserMessageIds {
	UM_Geiger = 300;
	UM_Battery = 301;
	UM_Damage = 302;
}

message CUserMessageGeiger {
	optional uint32 geiger = 1;
}

message CUserMessageBattery {
	optional int32 armorvalue = 1;
}

message CUserMessageDamage {
	optional int32 dmg_save = 1;
	optional int32 dmg_take = 2;
	optional int32 visible_damage_bits = 3;
	optional float damage_origin_x = 4;
	optional float damage_origin_y = 5;
	optional float damage_origin_z = 6;
}
```

### Convars and Commands
```
Name						Value		Flags
---------------------------------------------------------------------
quest_citizen_stop_see_player_timeout		2		game
quest_dialog_duration_chars_per_second		20		game
quest_dialog_duration_max			15		game
quest_dialog_duration_min			1		game
quest_dialog_text_drop_shadow_depth_offset	0.25		game
quest_dialog_text_drop_shadow_vertical_offset	0.25		game
quest_dialog_text_offset			80		game
quest_goal_depth				256		game
quest_goal_num_ticks				64		client
sv_crowbar_zipline				0		game
```

### Sources
- [Robot Repair server.dll Strings](https://pastebin.com/F0gzEeDD)
- [Robot Repair clinent.dll Strings](https://pastebin.com/EAEx4ArP)