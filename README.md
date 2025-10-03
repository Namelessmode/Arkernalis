# Overview
A lightweight ASCII art, terminal greetings, polished-personalized configuration bundle for **fastfetch** and **fish shell**.
<p align="center">
 <img src="./Screenshots/FastFish.png" style="width: 100%;">
</p>

# Dependencies
**Before cloning the git repository, make sure to have the following dependencies installed on the system.**
- [fastfetch](https://github.com/fastfetch-cli/fastfetch)
- [fish shell](https://github.com/fish-shell/fish-shell)
- [ImageMagick](https://github.com/ImageMagick/ImageMagick) (for ```.png``` image display - Mendatory)

# Installation
Clone this repository to your configuration directory:

```
 git clone https://github.com/Namelessmode/Arkernalis.git ~/.config/Arkernalis
```
> Note: If you have your own configuration for fish or fastfetch, make sure to either delete or back things up before cloning.
```
cp -r ~/.config/fastfetch ~/.config/fastfetch.backup && cp -r ~/.config/fish ~/.config/fish.backup
```
# Usage
- fastfetch

Move the following fastfetch config to the destined directory:

```
#Move
mv ~/.config/Arkernalis/fastfetch ~/.config/fastfetch
```
Or use symlink to avoid overwriting existing configs
```
#Symlink
ln -s ~/.config/Arkernalis/fastfetch ~/.config/fastfetch
```
> Important: Do not move copy/move/symlink ```~/.config/Arkernalis/fastfetch``` to fastfetch directory itself. Copy/Move/Symlink them outside the fastfetch directory, ```~/.config/Arkernalis/fastfetch``` > ```~/.config/``` to overwrite the fastfetch directory. This condition only applies if fastfetch directory exists inside ```~/.config/``` and it is free to run the command above if it doesn't exist.

Preview
<p align="center">
 <img src="./Screenshots/FastFetch.png" style="width: 100%;">
</p>

 > _To display images in `*.png` format, set_:

```
sudo pacman -Syu imagemagick
```

---
- fish

Move or Symlink the following fish config to the destined directory:
```
#Move
mv ~/.config/Arkernalis/fish ~/.config/fish
```
```
#Symlink
ln -s ~/.config/Arkernalis/fish ~/.config/fish
```
> Important!: Do not move/copy/symlink ```~/.config/Arkernalis/fish``` to fish directory itself```~/.config/fish/```. Copy/Move/Symlink them outside the fish directory, ```~/.config/Arkernalis/fish``` > ```~/.config/``` to overwrite the fish directory. This condition only applies if fish directory exists inside ```~/.config/``` and it is free to run the command above if it doesn't exist.

After moving or symlinking the configuration file to the destination (~/.config/fish/), go back to ```~/.config/fastfetch/``` and rename ```USER.jsonc``` to your username. (Example, ```Andy.jsonc``` or ```configs.jsonc```.)
```
#For nano
nano ~/.config/fastfetch/USER.jsonc
```
```
#For VIM
vim ~/.config/fastfetch/USER.jsonc
```
```
#FOR NVIM
nvim ~/.config/fastfetch/USER.jsonc
```
Write the following ```USER.jsonc``` with your Arch username by following the command ```:wq! YOUR_USERNAME.jsonc``` -> ```Enter``` for NVIM/VIM. 
For nano, write with ```Ctrl + O``` -> ```Write to File: YOUR_USERNAME.jsonc``` -> ```ENTER``` -> ```Save file under Different Name?: Y``` -> ```Ctrl + X```.

Then, Activate the greeting function:

```
source ~/.config/fish/functions/fish_greeting.fish
```
Preview
<p align="center">
 <img src="./Screenshots/fish.png" style="width: 100%;">
</p>

As easy as that, we're done!!
# Troubleshoot
If fish throws error code:
Navigate to ```~/.config/fish/functions/``` and use an editor to edit ```fish_greeting.fish```
Open VIM/NVIM/Nano:
```
# For Nano
nano ~/.config/fish/functions/fish_greeting.fish
```
```
# For VIM
vim ~/.config/fish/functions/fish_greeting.fish
```
```
For NVIM
nvim ~/.config/fish/functions/fish_greeting.fish
```

Replace ```$USER.jsonc``` with your ```$USER``` (Ex. ```USER``` can be ```Andy```) and hit ```ESC```, ```:wq!``` for VIM/NVIM. For nano, hit 'Ctrl + O -> Enter -> Ctrl + X -> Enter' to exit and save.
> Important!: You must put the exact Username as your Arch Linux Username (Not Hostname). Mismatch might cause errors

Then run the activating greet function:
```
source ~/.config/fish/functions/fish_greeting.fish
```

# Credit
Inspiration and references taken from:
- [mylinux4work/dotfiles](https://github.com/mylinuxforwork/dotfiles)
- [HyDE-Project/HyDE](https://github.com/HyDE-Project/HyDE)
- [LierB/fastfetch](https://github.com/LierB/fastfetch)
- [sofijacom/dotfiles-fastfetch](https://github.com/sofijacom/dotfiles-fastfetch)
