# NIGHTFALL: TACTICAL ENCOUNTER

**A Third-Person Combat & Enemy AI Prototype — Unreal Engine 5**

*Blueprint gameplay · Animation Blueprints · Behaviour Trees · AI Perception · Camera-based shooting*

![Nightfall player character standing in front of the barn](screenshots/01-barn-character.jpg)

**[▶ Watch the 36-second gameplay highlights](media/nightfall-gameplay-highlights.mp4)** | [More gameplay screenshots](screenshots/) | [Technical implementation](docs/technical-overview.md)

## About the project

**Nightfall: Tactical Encounter** is a personal gameplay systems prototype built with Unreal Engine 5. The player explores a night-time barn environment, aims a pistol in third person and encounters enemy AI that patrols and pursues the player. Shots are evaluated using camera-based line traces and can damage and eliminate enemies.

My focus was to **learn how to build and connect gameplay systems in Blueprints**—not to create the third-party character model or environment art from scratch. This repository is a **portfolio showcase and technical breakdown**, not a downloadable complete Unreal project.

The internal Unreal project was developed under the working name `Animation_Prototype`; only the public portfolio title was changed.

## Gameplay footage

[![Gameplay preview - third-person encounter](screenshots/06-enemy-engagement.jpg)](media/nightfall-gameplay-highlights.mp4)

**[Watch the edited MP4 (36.5 s)](media/nightfall-gameplay-highlights.mp4)** — selected scenes from the original recorded gameplay, including the environment, enemy encounters, movement, aiming and barn traversal.

## Gameplay and technical systems

| Area | Implementation |
| --- | --- |
| **Animation** | Idle/walk/run Blend Space, jump state, animation montages and notifies, Aim Offset, and upper-body layered blends |
| **Character** | Third-person controls, a human survival-character Skeletal Mesh, animation compatibility and retargeting |
| **Enemy AI** | AI Controller, Behaviour Tree, Blackboard, AI Perception, navigation, random patrol destinations, and player pursuit |
| **Combat** | Pistol attachment, camera-based line trace, hit detection, `Apply Damage`, health and enemy elimination |
| **Aiming / UI** | Right-mouse ADS, Timeline camera transition, Spring Arm length and socket-offset interpolation, on-screen crosshair |
| **Audio** | MetaSound gunshot with randomized pitch |
| **Blueprint communication** | Event Dispatchers for gameplay interactions and training targets |
| **Level design integration** | Imported ready-made barn scene with player and AI placed into a playable level |

## Selected gameplay screenshots

| Combat encounter | Barn interior |
| --- | --- |
| ![Player confronts an enemy](screenshots/02-enemy-encounter.jpg) | ![Playable barn interior](screenshots/04-barn-interior.jpg) |

## Selected Blueprint graphs

**Camera-based shooting trace**

![The camera-based line trace graph](docs/blueprints/line_trace_camera.png)

**Crosshair widget setup**

![The crosshair widget design](docs/blueprints/crosshair_widget.png)

## Key Blueprint assets

- `BP_ThirdPersonCharacter` — player controls, aiming, line trace and damage application
- `ABP_Lab_Basico` — animation state and layered character animation
- `BP_EnemyCharacter` — enemy health and damage response
- `BP_EnemyAIController`, `BT_Enemy`, `BB_Enemy` — AI detection and decisions
- `BTT_FindPatrolLocation` — navigable random patrol targets
- `TL_CameraAim` — camera transition for aiming
- `WBP_Crosshair` — crosshair UI
- `MSS_Pistol_Fire` — gunshot MetaSound

See [docs/technical-overview.md](docs/technical-overview.md) for more detail, and [docs/final-checklist.md](docs/final-checklist.md) for the local testing checklist.

## Technology and scope

- **Engine:** Unreal Engine 5.8.x (local development version 5.8.3)
- **Implementation:** Blueprints (no custom C++ in this prototype)
- **Target:** Windows / desktop prototype, tested locally in Unreal Editor
- **Status:** Learning project and playable technical showcase, **not** a complete commercial game

## Third-party assets and licensing

The environment, survival character and certain audiovisual assets come from third-party content packages. Rights remain with the respective creators. My contribution is the Blueprint-based integration and gameplay logic described above. To respect those licenses, this public repository intentionally **does not contain** the original mesh, texture, audio, animation, map or other licensed `.uasset` files, and it is **not a redistribution of the full game project**.

## Developer

- **Portfolio:** https://lucashoelzle.pages.dev/
- **GitHub:** https://github.com/lukyi124
- **LinkedIn:** https://www.linkedin.com/in/lucas-hoelzle-891b10145/
