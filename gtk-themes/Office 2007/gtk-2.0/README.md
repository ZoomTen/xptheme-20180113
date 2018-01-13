This theme is currently incomplete!

Using this theme with LibreOffice is pretty much a hack:

1. Copy this folder to your themes directory (most likely will be `~/.themes`, or maybe even `.local/themes`)

2. Create a folder named `.bin` in your home directory if you haven't yet

3. Save the following text to "libreoffice" in that directory:
```
#!/bin/bash

env SAL_USE_VCLPLUGIN=gtk GTK2_RC_FILES="$HOME/.themes/Office 2007/gtk-2.0/gtkrc" /usr/bin/libreoffice "$@"
```

4. Open a terminal in that directory and run:
```
	chmod +x libreoffice
```

5. Update all your menu shortcuts for LibreOffice by changing all instances of `libreoffice` in the "Command:" input to
```
    /(your home directory)/.bin/libreoffice
```

:/
