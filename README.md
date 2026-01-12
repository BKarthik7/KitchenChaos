# Kitchen Chaos - Polish Edition

A fast-paced cooking game built with Unity, based on the Kitchen Chaos tutorial series by Code Monkey.

## Overview

Kitchen Chaos is a fun and challenging game where players must prepare and deliver recipes within a time limit. The game features multiple counters, ingredient management, recipe tracking, and dynamic time extensions based on successful deliveries.

## Features

- **Dynamic Gameplay**: Orders spawn continuously and must be completed within the time limit
- **Recipe Management**: Track waiting orders and successfully completed deliveries
- **Time System**: Starting with 30 seconds, each successful delivery adds 25 seconds (capped at max)
- **Pause Functionality**: Pause and resume the game at any time
- **State Management**: Game progression through multiple states (Waiting, Countdown, Playing, Game Over)
- **Audio System**: Music management with state-based audio handling
- **Polish Edition**: Enhanced version with additional polish and improvements

## Project Structure

```
Assets/
├── Scripts/          # Core game scripts
│   ├── Counters/     # Counter logic
│   ├── Kitchen/      # Kitchen-related components
│   └── ...           # Other game systems
├── Scenes/           # Game scenes
├── Prefabs/          # Reusable game objects
├── ScriptableObjects/# Game configuration data
├── Shaders/          # Custom shaders
└── Settings/         # Game settings and configuration
```

## Key Systems

### Game Manager (`KitchenGameManager.cs`)
- Manages overall game state and flow
- Handles countdown timer before game starts
- Tracks gameplay timer and game over conditions
- Manages pause functionality

### Delivery Manager (`DeliveryManager.cs`)
- Spawns random recipes for the player to complete
- Validates delivered recipes
- Tracks successful deliveries
- Manages the waiting recipe queue

### Game Input (`GameInput.cs`)
- Handles player input and interactions
- Manages pause action bindings
- Integrates with Unity's new Input System

## Time Mechanics

- **Initial Time**: 30 seconds
- **Time Addition**: +25 seconds per successful recipe delivery
- **Maximum Time**: Capped at 30 seconds (no time accumulation beyond max)
- **Game Over**: When timer reaches 0

## Controls

- **Interact**: Default interact action (configurable)
- **Pause**: Default pause action (configurable)

## Credits

This project is based on the **Kitchen Chaos tutorial series** by **Code Monkey**.

🎬 **Tutorial Link**: https://www.youtube.com/watch?v=AmGSEH7QcDg

**Code Monkey** YouTube Channel: https://www.youtube.com/c/CodeMonkey

A huge thanks to Code Monkey for the excellent tutorial and guidance in creating this game!

## Requirements

- **Unity Version**: 2022 LTS or later
- **Render Pipeline**: Universal Render Pipeline (URP)
- **Input System**: New Input System package

## Installation

1. Clone the repository
2. Open the project in Unity 2022 LTS or later
3. Load the main scene from `Assets/Scenes/`
4. Press Play to start the game

## License

This is a learning project based on Code Monkey's tutorial. Please refer to Code Monkey's license and terms for any usage or distribution.

## Additional Notes

This version includes the "Polish Edition" enhancements and improvements to the base Kitchen Chaos game, including optimized timer mechanics and better state management.

---

*Made with ❤️ while following Code Monkey's tutorial*
