# Firefox: How to reduce height of bars

<br>

### *OPTION ONE: (My Preferred)*

1. go to 
```bash
about:config
```
in your URL bar.

2. search for 
```bash
browser.compactmode.show
```
and change the value to true .

3. Finally, go to the ```Hamburger-Menu``` > ```More-tools``` > ```Customize-toolbar``` and at the bottom of the page, click ```Density``` and select ```Compact```.

<br><br><br>

### *OPTION TWO (recommended):*

1. go to 
```bash
about:config
```
in your URL bar.

2. search for 
```bash
layout.css.devPixelsPerPx
```

3. Finally, double click on the value and change it to less than ```1.0```. After you set the value, press ```ENTER``` to apply the changes. For example, you can use ```0.75``` or if that is too big, you could try ```0.5```.
