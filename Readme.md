# ptz_pad

Package containing [robotnik_pad](http://www.github.com/RobotnikAutomation/robotnik_pad) plugins for teleoperating ptz cameras.

## Installation

The package depends on some Robotnik packages:

- robotnik_pad [🔗](https://github.com/RobotnikAutomation/robotnik_pad/)
```bash
git clone https://github.com/RobotnikAutomation/rcomponent
```

This package also depends on robotnik msgs:

- robotnik_msgs [🔗](https://github.com/RobotnikAutomation/robotnik_msgs)
```bash
git clone https://github.com/RobotnikAutomation/robotnik_msgs
```

## Parameters

This an example of a config file loading the ptz plugin:

```yaml
plugins:
  - Ptz

Ptz:
  type: ptz_pad_plugins/Ptz
  cmd_topic_ptz: ptz/command
  
  speed_increment: 0.5
  speed_limit: 3.14

  home_pan_position: 0.0
  home_tilt_position: 0.0
  home_zoom_position: 0.0
  
  position_increment: 0.1
  position_increment_limit: 0.5
  min_pan_position: -3.14
  max_pan_position: 3.14
  min_tilt_position: -1.57
  max_tilt_position: 1.57
  max_zoom_position: 12000

  config:
    button_deadman: 5
    button_home: 12
    button_pan:  10
    button_tilt: 9
    button_zoom_in: 4 
    button_zoom_out: 6
    button_increment_up: 2 
    button_increment_down: 0
    button_ptz_mode: 8
```

