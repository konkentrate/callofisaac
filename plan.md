# Implementation Plan

Systems to implement:

- Weapon System
    - Ammo logic (Ammo pickups on some monster deaths, spawns relevant ammo type; specific ammo bound to specific projectile type)
    - Projectile types (Normal, Rocket, Lob)
    - Different gun pickups with different ammo and projectiles (Rifle, Rocket Launcher, Minigun) Katana? :D
- Health System
    - AC_HealthComponent for easy integration on players and AI or any other distructables for example
    - Health Pickups (only for players)
- Custom Movement Component
    - Wall Jump https://www.youtube.com/watch?v=pd1KZASjSy0
    - Rocket Jump*
        - Setup Rocket Physical Power inside ProjectileRocket
    - Sprinting

Helpful links:

https://www.youtube.com/watch?v=WRG-5xlQDU8

https://www.youtube.com/watch?v=pd1KZASjSy0

https://www.youtube.com/watch?v=He4O4pdfoYI



Progress:

1) Quake-like movement
2) Camera tilt on strafe
    1. Tilt also when air strafing (go off of Characters lateral velocity)
3) Rocket Jumping (Impulse at launch location or close to it to launch player, Impulse on Hit Surface for exploding hit objects)

TODO:

- [x] Documentation
- [ ] Make projectiles not be able to hit Gun or Character meshes (for fixing rocket jumping)
- [ ] https://www.youtube.com/watch?v=O-m1tARfNRU

To Document:

- New blueprint and logic flow **Character -> Interface -> Weapon**
- Usage of Sockets on SkeletalMesh for accurate firing position of projectiles
- Inheritance on Weapon Types:
    - OUTDATED BP_Weapon will be the base class -> create children with different settings (meshes, projectile type, sounds, etc.)
    - Use SpawnActor BP_Weapon with the necessary variables set in the function to specify what weapon type you would like to spawn (kind of procedural, def during runtime)

Notes:

BP_Weapon handles: pickup, it attaches itself to player, launches projectile on event called from BP_Character; has children for each different weapon-type to launch different projectile types (will have several different, maybe inherited actors)