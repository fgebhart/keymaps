# Corne Keyboard 3x6

## Flashing

Using Puchi-C requires to tell `qmk` to use the `dfu` bootloader, because default bootloader for corne is `caterina`.

```
qmk flash -kb crkbd -km default -e BOOTLOADER=atmel-dfu
```

## Wiring from left to right half

In total there are 10 wires going from right (MCU half) to left (no MCU half):
* 6 columns
* 4 rows

## Flashing

1. first configure the default firmware, flash it and ensure it works (only MCU half is expected to work) see https://docs.qmk.fm/#/newbs_building_firmware
    - `qmk new-keymap`
    - `qmk compile`
    - `qmk flash -e BOOTLOADER=atmel-dfu`
2. apply custom changes in order to enable second half on same MCU:
    https://github.com/fgebhart/qmk_firmware/pull/1/files
3. modify keymap according to needs: https://github.com/fgebhart/qmk_firmware/blob/fgebhart_single_mcu_corne/keyboards/crkbd/keymaps/fgebhart/keymap.c
4. connect keyboard and flash again: `qmk flash -e BOOTLOADER=atmel-dfu`


## Layout

![](https://raw.githubusercontent.com/fgebhart/keymaps/main/corne/3x6/keymap.svg)
