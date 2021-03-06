---
### Bot spawns (version 0.2.6)
Adds a number of options and ways to handle bot spawns

 * [Plugin - botspawns.smx](plugins/botspawns.smx?raw=true)
 * [Source - botspawns.sp](scripting/botspawns.sp)

Adjust bot spawning and rules to increase game control. In early beta, only navmesh spawning and multiple lives supported right now.

#### Dependencies
 * [gamedata/insurgency.games.txt](gamedata/insurgency.games.txt)

#### CVAR List
 * "sm_botspawns_enabled" "0" //Enable enhanced bot spawning features
 * "sm_botspawns_spawn_mode" "0" //Only normal spawnpoints at the objective, the old way
 * "sm_botspawns_respawn_mode" "0" //Do not respawn
 * "sm_botspawns_counterattack_mode" "0" //Do not alter default game spawning during counterattacks
 * "sm_botspawns_counterattack_finale_infinite" "0" //Obey sm_botspawns_counterattack_respawn_mode
 * "sm_botspawns_counterattack_frac" "0.5" //Multiplier to total bots for spawning in counterattack wave
 * "sm_botspawns_min_counterattack_distance" "3600" //Min distance from counterattack objective to spawn
 * "sm_botspawns_min_spawn_delay" "1" //Min delay in seconds for spawning. Set to 0 for instant.
 * "sm_botspawns_max_spawn_delay" "30" //Max delay in seconds for spawning. Set to 0 for instant.
 * "sm_botspawns_min_player_distance" "1200" //Min distance from players to spawn
 * "sm_botspawns_max_player_distance" "16000" //Max distance from players to spawn
 * "sm_botspawns_min_objective_distance" "1" //Min distance from next objective to spawn
 * "sm_botspawns_max_objective_distance" "12000" //Max distance from next objective to spawn
 * "sm_botspawns_min_frac_in_game" "0.75" //Min multiplier of bot quota to have alive at any time. Set to 1 to emulate standard spawning.
 * "sm_botspawns_max_frac_in_game" "1" //Max multiplier of bot quota to have alive at any time. Set to 1 to emulate standard spawning.
 * "sm_botspawns_total_spawn_frac" "1.75" //Total number of bots to spawn as multiple of number of bots in game to simulate larger numbers. 1 is standard, values less than 1 are not supported.
 * "sm_botspawns_min_fireteam_size" "3" //Min number of bots to spawn per fireteam. Default 3
 * "sm_botspawns_max_fireteam_size" "5" //Max number of bots to spawn per fireteam. Default 5
 * "sm_botspawns_stop_spawning_at_objective" "1" //Stop spawning new bots when near next objective
 * "sm_botspawns_remove_unseen_when_capping" "1" //Silently kill off all unseen bots when capping next point
 * "sm_botspawns_spawn_snipers_alone" "1" //Spawn snipers alone, can be 50% further from the objective than normal bots if this is enabled?

#### Todo
 * [X] Instead of spawning all bots in one spot, spawn them at hiding spots in the navmesh
 * [X] Find path between current and next point, add bots around that axis
 * [X] Add option for minimum spawn distance to keep bots from spawning on top of players
 * [X] Create variables for how far off the path to spawn
 * [X] Create option to either spawn and keep X number of bots in game, or simply spawn on random timer (also an option)
 * [X] Create functionality to respawn bots to simulate more bots than game can support


