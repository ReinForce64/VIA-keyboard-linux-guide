**How to use VIA keyboard software on arch linux**

1. Download the latest release of VIA software from their official github page
	1. https://github.com/the-via/releases/releases/
2. Right click the downloaded app image file, right click it and go to _properties_, in _permissions_ check the "allow executing" box
3. Run this command on the app image file `sudo setcap 'cap_sys_rawio=+ep' your_appimage_file.AppImage`
	1. e.g. if your file is in the Downloads folder, you would run `sudo setcap 'cap_sys_rawio=+ep' ~/Downloads/via-3.0.0-linux.AppImage`
4. Optional:
	1. If your keyboard isn't detected but the key presses are working in the _Key Tester_, then you need to manually download the json definitions file from keychrons website
	2. e.g. Q series definitions files are here: https://www.keychron.com/pages/how-to-use-via-to-pair-with-keychron-q-series-keyboard
	3. e.g. V series definitions files are here: https://www.keychron.com/pages/firmware-and-json-files-of-the-keychron-qmk-v-and-v-max-series-keyboards
	4. in the _settings_ tab of VIA software, select _show design tab_
	5. in the _design_ tab, select _Load_, select the json file, remember to extract it from the downloaded zip file first
5. Connect your keyboard using a USB cable, flip the switch on the keyboard to "wired"
6. Good Luck.
