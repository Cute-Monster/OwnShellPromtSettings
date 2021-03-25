# Windows Terminal settings 

## ***Installig terminal app, images directory and fonts used by it***

### *Windows Terminal App*

Firstly you should install `Windows Terminal` or `Windows Terminal Preview` for Windows Store. 

### *Background images directory*
Copy `Terminal_Background_Images` folder to where you want, but it's better to copy it to the home directory of the user located at `~/`.
After that change path to some of the images at this directory at [settings.json](./settings.json#59) to use it as backgroung image at terminal.

> **Important!!**
Better to to use full path to the image and replace `\` with `\\` at path-string

## Configuring terminal app

After installing open it and press `Ctr + ,` to open settings menu. When navigate to botom left corner and press it to open `settings.json` with associated editor. 

When file is opened find its full-path location and replace it with this file. Another way is to copy [file content](./settings.json) and replace source content with it... 
