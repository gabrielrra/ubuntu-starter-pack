# Ubuntu Starter Pack - React Native Edition

From: me

To: me

## 1 - Terminal things

### Install usefull tools

```sh
sudo apt update
sudo apt install curl git zsh default-jre default-jdk
```

### Instal [Oh My ZSH](https://github.com/ohmyzsh/ohmyzsh)

```sh
curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh; zsh
#In case ZSh doesn't become default shell (Make sure to logout and login again from Ubuntu to see if the changes aplpied before doing this)
sudo usermod --shell $(which zsh) $USER
```

### ZSH customization

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

- **PowerLevel10K** Theme

> Works best with this **Meslo** font: https://github.com/romkatv/powerlevel10k#Fonts

> Store the fonts at `~/.fonts`. Go to terminal settings and change the font (**Meslo**)

Download theme:

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`

### Install [n](https://github.com/mklement0/n-install) - Node version Management

```zsh
curl -L https://git.io/n-install | bash
```

Open new terminal and run `n` to check if it's all good.

## 2 - Snap Store (Ubuntu Software)

### Android Studio

> After installation, open and start a new project. Don't forget to create an AVM. You can delete the project afterwards.

Add environment variables at `~/.zshrc`:

```zsh
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

### Visual Studio Code

Change **terminal font** at `settings.json` and restart it:

```json
{
  "terminal.integrated.fontFamily": "MesloLGS NF"
}
```

Extensions:

- Dracula (**NON OPTIONAL, MUST HAVE**)
- Github Markdown Preview
- Gitlens
- ESLint
- Prettier
- Rocketseat React Native

## 3 - Install Google Chrome browser

Enter FireFox, only to [download chrome](https://www.google.com/intl/pt-BR/chrome/) from the official site (sorry foxy)

To install the .deb that you downloaded.

```zsh
sudo dpkg -i path_to_deb_file
```

Remove firefox: `sudo apt remove firefox`
