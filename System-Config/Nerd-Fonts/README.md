# Nerd Font

Download, Install and Config Nerd Fonts

```bash
mkdir nerd-fonts && cd nerd-fonts/ && wget --quiet https://github.com/source-foundry/Hack/releases/download/v3.003/Hack-v3.003-ttf.zip && unzip Hack-v3.003-ttf.zip && wget --quiet https://github.com/tonsky/FiraCode/releases/download/6.2/Fira_Code_v6.2.zip && unzip Fira_Code_v6.2.zip && find . -type f -iname "*.ttf" -exec mv {} . \; && sudo mkdir -p /usr/share/fonts/truetype/nerd && sudo mv *.ttf /usr/share/fonts/truetype/nerd/ && fc-cache -v
```
