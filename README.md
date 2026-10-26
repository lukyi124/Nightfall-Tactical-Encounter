# NIGHTFALL: TACTICAL ENCOUNTER

**Third-Person Combat & Enemy AI Prototype | Unreal Engine 5**

*Blueprint gameplay · Animation Blueprints · Behaviour Trees · AI Perception · Camera-based shooting*

![Nightfall player character standing in front of the barn](screenshots/01-barn-character.jpg)

**[▶ Gameplay highlights (36.5 seconds)](#gameplay-footage)** · [Screenshots](#selected-gameplay-screenshots) · [Technical systems](#gameplay-and-technical-systems)

## About the project

**Nightfall: Tactical Encounter** is a personal gameplay systems prototype developed in Unreal Engine 5. The player explores a nighttime barn environment, aims a pistol in third person, and encounters enemy AI that patrols the area and pursues the player when detected. Camera-based line traces register shots, apply damage, and allow enemies to be eliminated.

The goal was to **learn and integrate gameplay systems using Blueprints**: character animation, AI behavior, hit detection, aiming, and UI. The character and environment art come from third-party assets; my work focuses on gameplay logic, implementation, integration, and testing.

This is a **technical portfolio showcase**, not a downloadable, complete Unreal Engine project. The local project was developed under the working title `Animation_Prototype`.

## Gameplay footage




## Gameplay footage

**Full gameplay showcase — 36.5 seconds, with audio**

https://github.com/user-attachments/assets/da274885-5e39-4f14-bd76-713b6dec4da6

The gameplay demonstration includes exploration, enemy encounters, character movement, aiming, shooting, and barn traversal.

**[Download gameplay MP4](media/nightfall-gameplay-highlights.mp4)**


## Gameplay and technical systems

| Area | Implementation |
| --- | --- |
| **Animation** | Idle/walk/run Blend Space, jump state, montages, animation notifies, Aim Offset, and upper-body layered blends |
| **Player character** | Third-person controls, human survival-character Skeletal Mesh, and integration with existing animation systems |
| **Enemy AI** | AI Controller, Behaviour Tree, Blackboard, AI Perception, navigation, random patrol locations, and player pursuit |
| **Combat** | Pistol attachment, camera-based line tracing, hit detection, `Apply Damage`, enemy health, and elimination |
| **Aiming and UI** | Right-mouse ADS, Timeline-driven camera transitions, Spring Arm interpolation, and an on-screen crosshair |
| **Audio** | MetaSound pistol firing effect with pitch variation |
| **Blueprint communication** | Event Dispatchers for gameplay interactions and training targets |
| **Environment integration** | Ready-made barn environment adapted into a playable combat and AI test level |

## Selected gameplay screenshots

| Enemy encounter | Barn interior |
| --- | --- |
| ![Player confronting an enemy](screenshots/02-enemy-encounter.jpg) | ![Barn interior gameplay scene](screenshots/04-barn-interior.jpg) |

![Enemy engagement during gameplay](screenshots/06-enemy-engagement.jpg)


## Selected Blueprint graphs

### Camera-based shooting — Line Trace

This Blueprint demonstrates camera-based hit detection and the shooting logic implemented for the player character.

![Camera-based Line Trace Blueprint](docs/blueprints/line_trace_camera.png)

### Crosshair Widget — UMG

This widget provides the aiming crosshair used by the third-person aiming system.

![Crosshair Widget Blueprint](docs/blueprints/crosshair_widget.png)

## Technical documentation

For a closer look at the Blueprint implementation and gameplay architecture:

- [Technical Overview — Animation, AI, Combat and Aiming](docs/technical-overview.md)
- [Project Validation and Testing Checklist](docs/final-checklist.md)



## Key Blueprint assets

- `BP_ThirdPersonCharacter` — player movement, aiming, camera trace, and damage application
- `ABP_Lab_Basico` — animation state logic and layered character animation
- `BP_EnemyCharacter` — enemy health, damage response, and elimination
- `BP_EnemyAIController`, `BT_Enemy`, `BB_Enemy` — AI perception and behavior decisions
- `BTT_FindPatrolLocation` — randomly selected navigable patrol targets
- `TL_CameraAim` — smooth aim camera transitions
- `WBP_Crosshair` — aiming reticle widget
- `MSS_Pistol_Fire` — gunshot MetaSound

## Technology and scope

- **Engine:** Unreal Engine 5.8.3 (local development)
- **Implementation:** Blueprints; no custom C++ in this prototype
- **Platform:** Windows desktop; locally tested in Unreal Editor
- **Status:** Playable learning prototype and portfolio showcase, not a commercial release

## Third-party assets and licensing

The barn environment, survival character, and some audiovisual assets were created by third-party artists and remain subject to their respective licenses. My contribution is the Blueprint implementation, integration, and gameplay logic described above.

To respect third-party licenses, this public repository intentionally does **not** redistribute those packages, meshes, textures, animations, sounds, or other licensed `.uasset` files. The repository contains portfolio documentation and gameplay media rather than a full Unreal Engine project.

## Developer

- **Portfolio:** https://lucashoelzle.pages.dev/
- **GitHub:** https://github.com/lukyi124
- **LinkedIn:** https://www.linkedin.com/in/lucas-hoelzle-891b10145/
