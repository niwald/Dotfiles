# Dotfiles
These are my custom dotfiles for the development environment.
Install the required packages. Copy or clone all folders to the **~/.config** directory.
Set permissions for shell scripts ```chmod +x bspwmrc```. Enjoy!

![Environment](https://github.com/niwald/Dotfiles/blob/main/img/twm-de-2.png)

**Required** packages: 
+ bspwm
+ sxhkd
+ tint2
+ rofi

**Optional** packages: 
+ nm-applet
+ compton
+ nvidia-settings
+ lxappearance



## bspwm
The TWM of choice here. Currently the config is built to work along with XFCE. 
This means that it uses **xfsettings** and **xfce4-terminal** for a quick setup. 
However, on Arch distributions these can be replaced or removed from **bspwmrc** file.
Colors are matched with the **Dark Pastels** theme of the xfce4-terminal.

## sxhkd
X daemon by baskerville that reacts to input events by executing commands. Debian repositories have it bundled and installed with the bspwm package.
On Arch, it needs to be installed separately. Used also to run **rofi** and virtually any other program. Everything is in **sxhkdrc** file: 
```sh
rofi -combi-modi run,drun -show combi -modi combi -show-icons
```

## compton
Lightweight compositor. Used for transparency, fade and shadows in this case. 
Makes the environment handling easier on the eyes and is available in Debian and Arch repositories. 

## tint2 
Lightweight panel with very good customization options. Also supports Shell scripts out of the box and provides a systray area.
Another plus is that its already included in the Debian and Arch repositories. Polybar is just bloated. 

## nvidia-settings
Solving the tearing issue with NVIDIA cards by enabling the CompositionPipeline on TWM start:

```sh
nvidia-settings --assign CurrentMetaMode="nvidia-auto-select +0+0 { ForceFullCompositionPipeline = On }"
```

## lxappearance
Desktop-independent theme switcher for GTK+. Useful for quick theme settings because you might want to run those as well in your TWM.
