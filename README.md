# Corne Keyboard Setup

A repository containing all corne keymaps that i have made! latest version is v1-2!
![image of the keyboard's keymaps](https://github.com/user-attachments/assets/e396b43e-4ecf-4153-8140-ad0a587c97aa)

## Steps in Order
1) Choose the configuration you want by looking at the json files, dummy
2) Obtain the .hex file (Option to download or compile yourself)
3) Flash to your keyboards!

## Viewing
1) download the .json file of the version to view
2) go to [the online QMK configurator](https://config.qmk.fm/#/crkbd/rev1/LAYOUT_split_3x6_3) and load the .json file
3) view the keymaps!
4) It allows you to compile through the web, so there's no stress!

## Compiling by yourself
So you chose the hard way, eh?
1) download the QMK JSON file
2) convert it into its "keymap.c" version
```bash
# you can also combine this with the next command if you want to
qmk json2c -o keymap.c <json config file>
```
3) place it into the correct keymap folder
```bash
# EXAMPLE, your keymap name might be different
mv keymap.c %HOMEPATH%\qmk_firmware\keyboards\crkbd\dannyhoang_testkeymap
```
4) you can try compiling it to check validity
```bash
qmk compile -km dannyhoang_testkeymap
```
5) Do your modifications here! I have added [sm_td, which should improve quantum keys](https://github.com/stasmarkin/sm_td)
6) compile again! you should find the correct hex file in the qmk_firmware root folder!


## Flashing 
1) download the .hex file of the version you want to use
2) use QMK Toolbox to flash the keymaps to the boards

## Things to update
- consider removing the arrow key HRMs because they provide no value for the downside
- consider a layout without HRMs for an easier life (remember to name it v2)
- maybe move the locations of space to the thumb modifiers because it isn't being used (specifially the right thumb)
