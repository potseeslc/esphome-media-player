# Swipe-Up Controls for ESPHome Media Player

This addon adds swipe-up functionality to the ESPHome Media Player interface, allowing you to access lighting controls and scenes by swiping up from the bottom of the screen. The controls are fully configurable through the Home Assistant device settings page.

## Features

- Swipe detection area at the bottom of the screen
- Animated panel that slides up when activated
- 3 configurable light control buttons
- 2 configurable scene activation buttons
- Smooth animations for panel transitions
- Fully configurable through Home Assistant device settings

## Installation

The swipe-up controls are automatically included when you use the modified packages.yaml file that includes:

```yaml
swipe_controls: !include addon/swipe-controls/controls.yaml
```

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

## Button Events

Buttons are pre-configured to work with Home Assistant entities:

- Light buttons toggle the corresponding light entity
- Scene buttons activate the corresponding scene entity

## Panel Positioning

The panel is designed for a 480x480 display. If you're using a different display size, you may need to adjust:
- The `y` positions of elements
- The panel height (currently 200px)
- The swipe detection area position
