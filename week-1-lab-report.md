# Week 1 Lab Report

In this tutorial you will learn how to: 

1. Install VS Code
2. Remotely Connect
3. Try New Commands
4. Move Files With scp
5. Set an ssh Key
6. Optimize Remote Running

---

**Step One: Installing VS Code**

* Click on [this link](https://code.visualstudio.com/) to install VS Code if you haven't already

* It should lead you to this page (This link and image is for Windows)

![my image](VS-Code.png)

* Download VS Code and follow the installer steps as well as the tutorial 

---

**Step Two: Remotely Connecting**

* Go to terminal in VS Code and open a new terminal 
* Then type in your course-specific account to remotely connect. If you have not already, reset your course account password [here](https://sdacs.ucsd.edu/~icc/index.php) before proceeding. 
* This link should tell you your specific username in cs15lfa22XX where the XX is specific to you. 
Once you have reset your password, type in this command in the terminal and replace the XX with your specific username.

```
$ ssh cs15lafa22XX@ieng6.ucsd.edu
```
* Select (Yes) and enter your password 

* If you have successfully logged in, your terminal should look something like this. 

![terminal](terminal.png)

---

**Step 3: Trying Some Commands**

* There are several commands that you can run once successfully remotely connected either on your computer or the remote one. These include: 

1. cd
2. ls
3. pwd
4. mkdir
5. cp

* This is an example of some commands being run in the terminal

![commands](commands.png)

---

**Step Four: Moving Files with scp**

* The scp command allows us to copy and move files from our home computer as well as the computer that we are remotely logged into. However, we wil always run the scp commmand from the home computer. 

* For now, log out of your remote computer by pressing Ctrl + D. 

* Create a new file on your computer and follow the code listed below. 

![whereAmI](whereAmI.png)

* Once you've done this, open a new terminal and type in the following commands into your terminal. 



