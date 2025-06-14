# HuggingFace Robotic Arm Simulator - Hackathon

This repository contains a modified version of the HuggingFace robotic arm simulator with enhanced keyboard control and manual intervention features.

## Modifications

- Prevents automatic resets after the initial reset
- Forces intervention mode to stay active for continuous manual control
- Changes gripper controls to use more intuitive 'o' and 'c' keys
- Increases step limit from 100 to 1000 for longer manual control sessions

## Installation Instructions

1. Uninstall the existing gym-hil package if it's installed:
   ```
   pip uninstall gym-hil
   ```

2. Install the modified gym-hil package from this repository:
   ```
   cd gym-hil
   pip install -e .
   ```

## Running the Simulator

Run the robotic arm simulator with the following command:
```
mjpython lerobot/scripts/rl/gym_manipulator.py --config_path config_mac_gui.json
```

## Keyboard Controls

- **WASD**: Move the arm in the XY plane
- **Q/E**: Move the arm up/down (Z-axis)
- **O**: Open gripper
- **C**: Close gripper
- **I**: Toggle intervention mode (should stay active by default)
- **Arrow keys**: Rotate the arm