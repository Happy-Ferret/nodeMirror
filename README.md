![logo](https://raw.github.com/soliton4/nodeMirror/master/src/image/logo/logoReadme.png)
  
  
## tldr  
  
  --> [screenshots](#screenshots)
  
## follow me

  --> [@nodeMirror](https://twitter.com/nodeMirror)
  
## Usage  
  
```
npm install node-mirror  
  
node node_modules/node-mirror/bin/nodeMirror.js --port 3000 --dir /home/sol/projects --username sol --password mysupersecretpassword
```
  
or global installed
```
nodeMirror --port 3000 --dir /home/sol/projects --username sol --password mysupersecretpassword
```

```
http://127.0.0.1:3000/  
```

list of options
```
nodeMirror --help
```



## Description  
  
Create your App completely within the Browser.  
Administrate your Server and edit your Code from where ever you are.  
  
nodeMirror is a IDE utilizing CodeMirror.net, pty.js and other cool libraries.  
  
I wrote it to fit the needs of a Developer, especially me, and to make maximal usage of the CodeMirror Editor library.  
Giving you a powerful IDE and Admin tool.  

Ever asked yourself which Editor you should choose? This is trying to answer that Question once and for all ;)
  
  
## Requirements  
  
  - a Unix / Windows Computer (yes mac is unix)
  - node.js
  - the ability to start a node.js app


## Optional
   
   - you need imagemagick installed on your machine to view images  
   - for audio files and the beta video module you need avconv installed  
   - for the X11 Terminal you need the following programs installed:  
     xprop  
     xdotool  
     avconv (optional just ffmpeg - pass --x11videotool ffmpeg)  
     if you want to use the h264 console make sure avconv is compiled with libx264  
  
## Customizablity
  
  nodeMirror is open Source. You can easily customize it to your needs.  
  Everything is a module. If you are missing some functionality let me know or fork it and write a module.
  
  
## features include:
  
 - view / edit all content/types supported by CodeMirror.net  
 - view / edit all files in text mode, hex Editor or download them  
 - view all imagemagick supported image types
 - html tester / analyzer  
 - .less tester / .less online help / save your .less file immediately as .css file  
 - awesome hexeditor  
 - integrated pegjs parser debugger  
 - download directories as zip files  
 - Terminals (!)  
 - build in web server  
 - a freakin X11 terminal forwarder (!!)  
 - more ...  
  
  
## Files Module  
  
For every Content Type where a CodeMirror Mode exists, a CodeMirror instance will be opened. Also every content Type starting with text/* will be opened using CodeMirror.  
For all other files there is a download button or a Hex Editor.  
If a file is opened for which no native Text Mode exists it will be opened in a Hex Editor. You can switch between hex view and text view.
  
## Audio / Video Files
  
Audio and Video files are converted to a web format using avconv. make sure you have it installed.
the Video module is beta.
  
  
## Terminal Module  
  
utilizing pty.js nodeMirror allows you to have several terminals within your browser. the Terminals will stay open when you close your browser window. You can even have the same terminal open on different browsers / machines opening new possibilities for collaboration.   
  
## X11 Terminal Module  
  
a videostream encoded with avconv is forwarded to the client. client inputs are forwarded via xdotool.  
make sure you have avconv, xprop and xdotool installed.  
to activate the x11 module pass --x11terminal on the commandline. this feature stays optional because not every server has a x11 console.
  
a low latency h264 console is available. i apprechiate test reports of this bleeding edge technology.  
pls refer to requirements.  

  
## Debug Module  
  
this is early beta. feel free to play with it. basic breakpoint / exception and stepdebugging works. 
  
  
## Web Server
  
all files you are editing are available under /file/
  
  
## Security  
  
pass username and password to secure your local files from being hacked  
  
  
## miscellaneous  
  
i am using this for my development so you can expect more.  
  
the npm distribution is a dojo release build  
check out my git page to get the development version which you can use to customize NodeMirror  
call the build script to make your own version of NodeMirror  

```
cd build  
./build.sh  
```  
  
to switch of the terminal or the experimental debugger use this command line parameters  
  
```
node node_modules/node-mirror/bin/nodeMirror.js --no-terminal --no-debug
```  

## Special Thanks  
  
* CodeMirror ( http://codemirror.net/ )  
for creating the most developer friendly editor  
  
* pty.js ( https://github.com/chjj/pty.js )  
for making terminals in node.js possible  
  
* Broadway.js ( https://github.com/mbebenita/Broadway )  
for the h264 decoder used in the X11 remote console  
  
* all the contributers, testers and users  
for making this a great IDE  
  
  
## screenshots
  
![Folder view](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorFolder.png)
  Browse your project folder  
  
![JavaScript Editor](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorJavaScript.png)
  edit JavaScript with online Syntax Check  
  
![JavaScript Editor](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorHexEditor.png)
  edit huge Files with the Hex Editor  
  
![Terminal](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorTerminal.png)
  Yes you can use midnight commander in your Browser with your Mouse(!)  
  Thank you pty.js  
  
![less](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorLess.png)
  Have less online help available while testing your less file before saving it parallel as .less and .css file.  
  
![html](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorHtml.png)
  test and analyse your HTML  
  
![peg.js](https://raw.github.com/soliton4/nodeMirror/master/src/image/screenshots/nodeMirrorPegJs.png)
  try out that cool parser you just wrote  
  
  
## whats to expect for 0.2?
  
  - JavaScript debugging
  - more CodeMirror feature integrations
  
  
## contemporaty  
  
  - 0.1.15 check out the new tree and code folding features. you never get lost in the tree.
  also a beta implementation for the same feature in code is available in settings
    "code folding - float feature"
  
  - 0.1.8 has a new folder view. actually its 2 views now: list and details. the list view is a css hack. i was wondering if there are any issues with it on modern browsers. if so, pls report them.  
  also pls give feedback if you like the color coding. i believe representing files as icons is a deadend. i tried to make the filetype intuitive by color coding different types. tell me what you think.
  
  
## Contributions welcome!
  
  i am a good coder but my gui designs are poor.  
  while i am happy about all kinds of contributions i especially ask for icon designs / css.  
  
  
## License

BSD
