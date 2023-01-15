# Lab Report 1

## Installing VSCode
1. [Click Here](https://code.visualstudio.com/download) <br /> Should bring up this page:
<img width="951" alt="Screen Shot 2023-01-15 at 10 09 44 AM" src="https://user-images.githubusercontent.com/97646090/212559028-47ae8b4a-fce4-405c-bfbc-352b20e9d31b.png">

2. **Click** and **download** the appropriate version for your device
3. **Follow** the install wizard to **complete** the setup
4. Congrats! You now have VSCode installed!

---
## Remotely Connecting
1. Open a terminal(either on VSCode or command line)on your device
2. Paste `ssh cs15lwi23zz@ieng6.ucsd.edu` in your terminal
3. Replace the 'zz' to turn 'cs15lwi23zz@ieng6.ucsd.edu' into your account name 
<br /> It should look like this:
<img width="554" alt="Screen Shot 2023-01-15 at 9 00 57 AM" src="https://user-images.githubusercontent.com/97646090/212559594-5b999057-e74d-45d1-8524-2a5b1f1a7f1c.png">

4. Hit return and if this is your first time connecting, you will probably get a message querying if you want to continue, to which you should respond yes.
5. Then enter your account **password** <br />
If successful your terminal should show:
<img width="515" alt="Screen Shot 2023-01-15 at 10 24 30 AM" src="https://user-images.githubusercontent.com/97646090/212559756-8ced1a35-d4fd-4f88-ad7d-bf426e5ac454.png">

6. Type `pwd` into your terminal and you should get `/home/linux/ieng6/cs15lwi23/cs15lwi23alt` (with your own account of course)
7. You're in!

---
## Trying Some Commands
Here are some basic commands:
* `cd` 
  - changes directory, ex(`cd path` will change your current directory to `~/path`, assuming path is a directory within your previous working directory)
* `ls`
  - prints all of the items in your current directory
* pwd
  - prints the path of your working directory
* mkdir
  - makes a new directory, ex(`mkdir orange` will make a new directory called 'orange' in your current directory)
* cp
  - copies file/directory to another directory, ex(`cp hello.txt ~/folder/blue` will copy `hello.txt`, assuming the file exists to `~/folder/blue`)
* exit
  - exits the ssh
  - should look like this:
<img width="337" alt="Screen Shot 2023-01-15 at 3 38 49 PM" src="https://user-images.githubusercontent.com/97646090/212573804-aa55f883-98ff-43a6-b95d-3a5066eea431.png">
