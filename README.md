NOTICE!
Please acknowledge that Wake is still in development and you may experience issues while using Wake. 


Wake -

Wake is a regular Wayland compositor that is meant to be lightweight. It is based off tinywl.
To use wake, the following packages are required 

- ninja
- meson
- Wayland development libs
- wlroots libraries and others for wake

  To build it from source, copy this Github repository link. Or you can copy the following commands

  git clone https://github.com/znxbinx/Wake
cd wake

after that, install the following packages 
sudo pacman -S --needed base-devel git meson ninja (I'm using arch so it might be different depending on your distro)

Then, configure the build using 
meson setup build

After, you can compile wake and install it
ninja -C build
sudo ninja -C build install

(If the build fails. Make sure you have all the required development libraries are installed and wayland libs)

After that, you can enjoy wake

KEYBINDS

If your not familiar with TinyWL, the modifier key is ALT. 

open terminal: ALT + RETURN
kill: ALT + Q
dragging windows: ALT + MOUSE LEFT
resizing windows: ALT + MOUSE RIGHT
full screen: ALT + F

