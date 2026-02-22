# ESPHome Media Player with Swipe-Up Controls

## Overview
This enhanced version of the ESPHome Media Player adds swipe-up controls that allow you to access lighting and scene controls directly from the bottom of the screen.

## Key Features Added
- Swipe detection area at the bottom of the screen
- Animated control panel that slides up when activated  
- 3 configurable light control buttons
- 2 configurable scene activation buttons
- Fully configurable through Home Assistant device settings

## Configuration
After flashing and connecting to Home Assistant:

1. Go to **Settings > Devices & Services > ESPHome** and click on your device
2. Under the **Configuration** section, you'll find 5 new text fields:
   - **Light 1 Entity** - Enter the entity ID of your first light (e.g., `light.living_room`)
   - **Light 2 Entity** - Enter the entity ID of your second light
   - **Light 3 Entity** - Enter the entity ID of your third light
   - **Scene 1 Entity** - Enter the entity ID of your first scene (e.g., `scene.movie_time`)
   - **Scene 2 Entity** - Enter the entity ID of your second scene

## Usage
1. Swipe up from the bottom of the screen to reveal the controls panel
2. Tap any light button to toggle that light on/off
3. Tap any scene button to activate that scene
4. Tap the X button or swipe down to dismiss the panel

## Technical Implementation
The enhancement adds a new addon (`addon/swipe-controls/`) with:
- Text sensors for storing entity IDs
- Smooth animations for panel transitions
- Pre-configured Home Assistant service calls
- Responsive button layout for touch interaction

## Files Modified/Added
- `addon/swipe-controls/controls.yaml` - Main implementation
- `addon/swipe-controls/README.md` - Documentation
- `addon/swipe-controls/ha_integration_example.yaml` - Integration examples
- Updated main `README.md` with information about the feature
