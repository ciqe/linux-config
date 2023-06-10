# Add aliases for ROOT user

1. Run as `sudo`.
```bash
sudo su
```

2. Copy below code 
```bash
if [ -f /home/kali/.bash_aliases ]; then
    . /home/kali/.bash_aliases
fi
```

3. Edit `.zshrc` file for root user and add the code in the end of the file
```bash
nano /root/.zshrc
```

4. Edit `.bashrc` file for root user and replace the code with code described in `5`.
```bash
nano /root/.bashrc
```

5. Default `.bash_aliases` in `/root/.bashrc`
```bash
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
```
