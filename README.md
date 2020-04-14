# Ubuntu Starter Pack - React Native Edition
From: me 

To: me

## 1 - Terminal things

#### Install usefull tools

```sh
sudo apt install curl git zsh
```

#### Instal [Oh My ZSH](https://github.com/ohmyzsh/ohmyzsh)
```sh
curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh; zsh
#In case ZSh doesn't become default shell (Make sure to logout and login again from Ubuntu to see if the changes aplpied before doing this)
sudo usermod --shell $(which zsh) $USER
```

#### ZSH customization

- Plugins:

```zsh
#zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

Add plugins at ~/.zshrc: (no commas to separate them)

```
...
plugins={
   git
   zsh-syntax-highlighting
   zsh-autosuggestions
   ...
}
...

```

- Look and feel

**PowerLevel10K** Theme

> Works best with this Font (**Meslo**): https://github.com/romkatv/powerlevel10k#Fonts

>Store the fonts at `~/.fonts`. Go to terminal settings and change the font (**Meslo**)

>In VSCode add this line to `settings.json` and restart it: 

```json
{
   "terminal.integrated.fontFamily": "MesloLGS NF"
}
```

Install theme:

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`


## 2 - Snap Store (Ubuntu Software)

### Android Studio

>After installation, open and start a new project. Don't forget to create an AVM. You can delete the project afterwards.

### Visual Studio Code

Extensions:

 - Dracula (**NON OPTIONAL, MUST HAVE**)
 - Github Markdown Preview
 - Gitlens
 - ESLint
 - Prettier
 - Rocketseat React Native


#### Android Studio

## 2 - Instalar Chrome

Enter FireFox, only to download chrome from the official site (sorry foxy)

To install the .deb that you downloaded.

```sudo dpkg -i path_to_deb_file```
