# Setting Up ZSH with `oh-my-zsh` and other customization.

<br>

0. **Check Shell**

```bash
echo $0
```

1. Install Git, cURL, wget as prequisites

```bash
sudo apt install curl git wget
```

2. Install ZSH shell

```bash
sudo apt install zsh
```

3. Change Default Shell 

```bash
chsh -s $(which zsh)
```
[Alternative 3 ways](https://www.linuxshelltips.com/change-shell-linux/)

### Oneliner for Step 1-3:

```bash
sudo apt install curl git wget zsh && chsh -s $(which zsh)
```

<br>

### ------------------------><em>Now Reboot The Computer (Linux)</em><------------------------

<br><br>

### Oneliner for Step 5-8 [without font part]:

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" && git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions && git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

<br><br>

4. Check Shell Again

```bash
echo $0
```

5. Download [Oh-My-ZSH](https://ohmyz.sh/)

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

6. Download any [Powerline Font](https://github.com/powerline/fonts) ---> [Fira font](https://github.com/tonsky/FiraCode), [Hack Font](https://github.com/source-foundry/Hack) or others to get best experience.
```bash
git clone https://github.com/tonsky/FiraCode.git

# Another Powerline font Hack:
https://github.com/powerline/fonts/raw/master/Hack/Hack-Regular.ttf
```

7. Download [ZSH Auto Suggestion](https://github.com/zsh-users/zsh-autosuggestions)

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

8. Download [ZSH Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

9. Add this to ~/.zshrc file 

### Obviously before ```source $ZSH/oh-my-zsh.sh``` part

```bash
# default theme
# ZSH_THEME="robbyrussell"
ZSH_THEME="agnoster"

plugins=(
    git
    history
    zsh-autosuggestions
    zsh-syntax-highlighting
    command-not-found
)
```

10. (Optional) Download Power Level 10k Theme

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

11. (If you chose 10) Go to powerlevel10k folder & run this to customize style

```bash
p10k configure
```





