# CallOfIsaac

## Game concept

- Puzzle game inspired by The Binding of Isaac with a FP perspective twist
- Procedurally generated rooms with a prebuilt layouts
- First Person Shooter with ULTRAKILL-inspiration (verticality, gun power ups, grenades, graphically…)
- Go to the next room / level after defeating wave/s of mobs (ranged / melee)
- After each room > possibility of accessing shop / chests for new guns / power-ups
- Lowpoly art style with cartoonish shaders / textures (inspired from The Binding of Isaac)

## Organisational

All the orgainzational information is provided in here. This includes the layout for commit messages as well as the separation of the features and which features we use.

### Branches

Develop features on their own branches and only push them to the main branch when the feature is completely finished. This aims to reduce the number of merge conflicts.

### Dev Diary

Since the dev diary is generated with the commit messages, they have to provide information what was being done and how long it took.
Note: Make sure to always commit on the day the feature was developed even if it isn't finished completely.

The commit messages should follow this pattern (please round the time to 15m):
```
[Time worked in the format XXhXXm] Short conclusion what was done

More precise information about the achievements of the working session.
```

e.g.
```
[30m] Updated README

Ported the information from the design document into the README
```

### Development

We decided to implement the following features:

- **World builder tweaks**: UnrealEngine’s Procedural Content Generator (PCG) for map randomization (either randomized room layouts or by randomized room elements)
- **Text/UI**: Explanation text for the powerups, and shopkeeper with text visualization of the communcation (with a corresponding UI, think decision-based games)
- **Audio**: Spatial audio -> the mobs and objects will make some noise/sounds
- **Image/UI**: Custom UI elements for ammunition, health, powerups, etc. which change over the course of the game
- **Video**: Short cut scene to place the player in the dungeon (seamless transition); short animation overlays before boss fights
- **Effects and Programming**: Minimap similar to Binding of Isaac -> only display rooms that have already been visited and the ones adjacent to that; Maybe enable simultaneous play with a split screen.


