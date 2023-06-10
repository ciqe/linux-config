# Install Python 3 on Ubuntu / Debian / Kali / Parrot

1. Install Python 3

```bash
sudo apt install python3
```

2. Install PIP from python3

```bash
sudo apt install python3-pip
```

3. Set Python3 as Default On Ubuntu

- [Show Steps](./Python3-as-Default/README.md)

<br/><br/><br/>

## Upgrade All Python Package with one Command

```bash
pip3 list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip3 install -U
```
