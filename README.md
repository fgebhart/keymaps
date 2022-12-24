# keymaps

This is where I host my keymaps.

## Usage

### Generate a Keymap

1. Go to the [QMK configurator](https://config.qmk.fm/).
2. Select Keyboard and Layout as needed, see [docs](https://docs.qmk.fm/#/newbs_building_firmware_configurator).
3. Download the `keymap.json` file.

### Flash Keymap to Keyboard
Steps needed to flash a given keymap to a keyboard:

1. Install the QMK CLI, see [docs](https://docs.qmk.fm/#/cli?id=qmk-cli).
2. Use the QMK CLI to flash the keymap of choice to your keyboard using.

```shell
qmk flash <keymap>.json
```
