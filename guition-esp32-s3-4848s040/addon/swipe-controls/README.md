# Swipe-Up Controls for ESPHome Media Player

This addon adds swipe-up functionality to the ESPHome Media Player interface, allowing you to access lighting controls and scenes by swiping up from the bottom of the screen.

## Features

- Swipe detection area at the bottom of the screen
- Animated panel that slides up when activated
- Light control buttons (customizable for your setup)
- Scene activation buttons (customizable for your setup)
- Smooth animations for panel transitions

## Installation

The swipe-up controls are automatically included when you use the modified packages.yaml file that includes:

```yaml
swipe_controls: !include addon/swipe-controls/controls.yaml
```

## Customization

To customize the controls for your specific Home Assistant setup:

1. **Modify the button labels** in `addon/swipe-controls/controls.yaml` to match your light and scene names
2. **Update the button IDs** to match your Home Assistant entity IDs
3. **Change colors** to match your theme preferences
4. **Add more buttons** if needed by duplicating the existing button structures

## Button Events

Each button currently has placeholder functionality. To connect them to your Home Assistant entities, you would add event handlers like:

```yaml
event_handlers:
  on_click:
    - homeassistant.service:
        service: light.toggle
        data:
          entity_id: light.your_light_entity
```

## Panel Positioning

The panel is designed for a 480x480 display. If you're using a different display size, you may need to adjust:
- The `y` positions of elements
- The panel height (currently 200px)
- The swipe detection area position

## Future Enhancements

Planned improvements:
- Actual integration with Home Assistant entities
- More control types (climate, security, etc.)
- Customizable panel height
- Gestural swipe detection (instead of click)
