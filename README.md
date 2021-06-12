# klipper-macros

A collection of my Klipper G-code macros.

## Usage
Copy the `macros` folder alongside your printer configuration file and edit it to add:

```
[include macros/*.cfg]
```

## Configuration
You can configure some macros using [SAVE_VARIABLE](https://github.com/KevinOConnor/klipper/blob/master/docs/G-Codes.md#save-variables) in the following way:

```
[save_variables]
filename: ~/variables.cfg

[delayed_gcode macros_initialize]
initial_duration: 1
gcode:
  INITIALIZE_VARIABLE VARIABLE=park_x VALUE=30
  INITIALIZE_VARIABLE VARIABLE=park_y VALUE=30
  INITIALIZE_VARIABLE VARIABLE=bowden_len VALUE=300
```

Here's the list of parameters you can configure:
| Name       | Default      | Description             |
|:----------:|:------------:|:-----------------------:|
| park_x     | *x_min* + 20 | Default X park position |
| park_y     | *y_min* + 20 | Default Y park position |
| bowden_len | 100          | Bowden tube length      |

## Macros
* [G27](/macros/G27.cfg)
* [G29](/macros/G29.cfg)
* [M204](/macros/M204.cfg)
* [M205](/macros/M205.cfg)
* [M600](/macros/M600.cfg)
* [M701](/macros/M701.cfg)
* [M702](/macros/M702.cfg)
* [M900](/macros/M900.cfg)
* [POWEROFF](/macros/POWEROFF.cfg)
* [NOTIFY](/macros/NOTIFY.cfg)
* [LAZY_HOME](/macros/LAZY_HOME.cfg)
* [RETRACT](/macros/RETRACT.cfg)
* [PAUSE_PARK](/macros/PAUSE_PARK.cfg)
* [PRE_START](/macros/PRE_START.cfg)
* [POST_END](/macros/POST_END.cfg)
* [WIPE_LINE](/macros/WIPE_LINE.cfg)
* [INITIALIZE_VARIABLE](/macros/INITIALIZE_VARIABLE.cfg)
* [SAVE_AT_END](/macros/SAVE_AT_END.cfg) by [Makoto](https://klipper.info/macro-examples-1/makotos-conditional-config-saving)
* [SAVE_IF_SET](/macros/SAVE_IF_SET.cfg) by [Makoto](https://klipper.info/macro-examples-1/makotos-conditional-config-saving)
