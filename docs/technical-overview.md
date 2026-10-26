# Technical overview — Nightfall: Tactical Encounter

## Animation and character

The project uses `ABP_Lab_Basico` with a locomotion state machine, Blend Space, montage slots, upper-body layering and aiming. The original mannequin was replaced by a human survival-character mesh using compatible skeletal data and animation retargeting concepts.

## Enemy AI

`BP_EnemyAIController` starts `BT_Enemy` on possession. The `BB_Enemy` Blackboard stores keys including `TargetActor`, `CanSeePlayer` and `PatrolLocation`. The Behaviour Tree gives higher priority to chasing the detected player and otherwise patrols navigable locations obtained by `BTT_FindPatrolLocation`. AI Perception updates detection state.

## Aiming and camera

Right mouse controls the aiming state. `TL_CameraAim` smoothly blends `CameraBoom` arm length and socket offset, and `WBP_Crosshair` becomes visible while aiming. The aim transition is reversible.

## Shooting and damage

The `EVT_ExecuteShot` event plays the gunshot, traces from the camera's location and forward direction, and uses `Apply Damage` on valid blocking hits. `BP_EnemyCharacter` responds in `Event AnyDamage` by subtracting damage from Health, then marking itself dead and destroying the actor if Health reaches zero.

## Audio and Blueprint communication

The firing sound uses the `MSS_Pistol_Fire` MetaSound with randomized pitch. Training targets and other gameplay interactions also demonstrate Blueprint event dispatchers.

## Scope and limitations

This is a technical learning/demo scene, not a complete game. It demonstrates AI patrol and pursuit, not advanced tactics or enemy ranged attacks. The level and human character use third-party content; the technical focus and contribution are on Blueprint logic, integration and debugging.
