# Dotfiles
These are my custom dotfiles for the development environment. Following packages are required: 
+ bspwm
+ tint2
+ rofi
+ nm-applet (optional)
+ compton (optional)
+ nvidia-settings (optional)

## bspwm
The TWM of choice here. Currently the config is built to work along with XFCE. 
This means that it uses **xfsettings** and **xfce4-terminal** for a quick setup. 
However, on Arch distributions these can be replaced or removed from **bspwmrc** file.

## compton
Lightweight compositor. Used for transparency, fade and shadows in this case. 
Makes the environment handling easier on the eyes. 

## tint2 
Lightweight panel with very good customization options. Also supports Shell scripts out of the box and provides a systray area.
Polybar is just bloated. 

## nvidia-settings
Solving the tearing issue with NVIDIA cards by enabling the CompositionPipeline on TWM start:

```sh
nvidia-settings --assign CurrentMetaMode="nvidia-auto-select +0+0 { ForceFullCompositionPipeline = On }"
```
