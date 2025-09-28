# Exercise-02d-Scenes-And-Menus
9/27/25
Exercise for MSCH-C220

A user-controlled ship for a space-shooter game. Recently added a new enemy, a background, and an enemy generation system. (Also some other small tweaks that aren't really important? Bullets fly further, score is in the thousands instead of the ones, bullets are black and become transparent, etc etc.) Created in Unity.

## Implementation

Created using [Unity 2022.3.45f](https://unity.com)

Assets are provided by [Kenney.nl](https://kenney.nl/assets/space-shooter-extension), provided under a [CC0 1.0 Public Domain License](https://creativecommons.org/publicdomain/zero/1.0/).

The explosion spritesheet was released into the public domain by [StumpyStrust](https://opengameart.org/content/explosion-sheet)

### Bonus Points:
Added a background (+1) - I wanted to do my own assets, but I ran out of time and could only add a background.

New enemy (+2 for complexity) - The blue laser enemy rotates around (0,0) until it is facing the player. It then stops and charges up a laser that can kill the player. The laser spans the entire screen, but is easy to manage and locks the enemy in place for several seconds. After firing a laser, it rotates harmlessly without looking for the player for a few seconds.

Random enemy generation (+2, could be +1 because of jank and issues with randomness) - Asteroids, sin-wave enemies, and laser enemies are each on their own timer. Every 7-9 seconds for asteroids, 11-13 seconds, for sin enemies, and 13-15 seconds for laser enemies, a timer will elapse and spawn the chosen entity at one of six locations across the top and sides of the screen, with slight random offset. There is a greater chance for enemies to spawn from the top of the screen than from the side. Every 10 seconds, the "intensity" will be raised, making each timer 1 second shorter (e.g. after 10 seconds, a asteroid will spawn every 6-8 seconds). When the player dies, the intensity is lowered and each timer becomes 1 second longer. Laser enemies don't spawn at random positions but the radius of the circle they orbit is random.

## References
None

## Future Development
None

## Created by
Nathan Mishler
