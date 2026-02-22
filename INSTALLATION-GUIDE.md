# Installation Guide for Enhanced ESPHome Media Player

## Prerequisites
- Guition ESP32-S3-4848S040 device
- USB-C cable
- Home Assistant instance with lights and scenes configured

## Installation Steps

### Step 1: Flash the Enhanced Firmware
1. Connect your Guition device to your computer via USB-C
2. Visit the Web Installer at https://jtenniswood.github.io/esphome-media-player/
3. Click **Install** and select your device
4. Wait for flashing to complete

### Step 2: Connect to WiFi
1. After flashing, the device creates a WiFi hotspot
2. Connect to the hotspot from your phone/computer
3. Enter your home WiFi credentials in the captive portal
4. The device will restart and connect to your network

### Step 3: Adopt in Home Assistant
1. Home Assistant should automatically discover the device
2. Go to **Settings > Devices & Services** and look for ESPHome notification
3. Click **Configure** and follow prompts to adopt the device

### Step 4: Configure Media Player
1. Go to **Settings > Devices & Services > ESPHome** and click on your device
2. Under **Configuration**, find the **Media Player** text field
3. Enter the entity ID of the media player you want to control (e.g., `media_player.living_room`)

### Step 5: Enable Device Controls
1. Go to **Settings > Devices & Services > Integrations** and click on **ESPHome**
2. Find your device and click the **cog icon** to open its settings
3. Enable **"Allow the device to perform Home Assistant actions"** and click **Submit**

### Step 6: Configure Swipe-Up Controls
1. In the same device settings page, find the new configuration fields:
   - **Light 1 Entity** - Enter your first light entity (e.g., `light.living_room`)
   - **Light 2 Entity** - Enter your second light entity
   - **Light 3 Entity** - Enter your third light entity
   - **Scene 1 Entity** - Enter your first scene entity (e.g., `scene.movie_time`)
   - **Scene 2 Entity** - Enter your second scene entity
2. The swipe-up controls will now work with your specified entities

## Usage
- Swipe up from the bottom of the screen to access lighting/scene controls
- Tap light buttons to toggle lights on/off
- Tap scene buttons to activate scenes
- Tap the X button or swipe down to dismiss the panel
