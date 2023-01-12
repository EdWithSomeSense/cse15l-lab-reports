#  Week 1 Lab Report 
Welcome and congradulations on making into the CSE 15L course. Today, I, your instructor, will show you the way on how to access your course-specific account on `ieng6`. 

## Part 1 - Finding your `ieng6` account 
It's quite simple in trying to find your ieng6 account by clicking on the following [link](https://sdacs.ucsd.edu/~icc/index.php) you will be taken to the UCSD Educational Technologies Service Website.\
![Image](https://i.imgur.com/KvPLtlJ.png)
Once you enter your credentials you would want to click on the ETS account name.
![Image](https://i.imgur.com/SVe127u.png)

Follow the [following tutorial](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) provided by Professor Joe on how to properly change your password for your `ieng6` account so that you won't accidentally change your `AD` account password as well.

## Part 2 - Downloading Visual Studio Code
(If you are using one of the lab computers, you can skip this process)

To download Visual Studio Code, go to their [website](https://code.visualstudio.com/) and follow their instructions on how to download and install VSC on your computer. 

After downloading Visual Studio Code you should open up to something that looks similarily to this.
![Image](https://i.imgur.com/wcq3T8s.png)
If you were to see the following application then congradulations, you have succeeded in downloading Visual Studio Code.

## Part 3 - Connecting to your `ieng6` account
So first and foremost, there are still some things that you need to install if you are on Windows.\
If you are on Windows, please install `git` for windows as it provides some of the useful tools that is required later.
[Here is the link](https://gitforwindows.org/)

Once you have finished installing Git for Windows you will be able to use git bash in Visual Studio Code.
![Image](https://i.stack.imgur.com/1AGtr.png)

Next we will have to use the `ssh` command in USC.
Open up Visual Studio Code's Terminal by either using Ctrl/Cmd + or click on new Terminal in the menu. 

Input the following command into the VSC terminal:
**Note:** replace the xy with your account letters.
```
$ ssh cs15lwi23xy@ieng6.ucsd.edu
```

When you get connected to the server it will look something like this.

![Image](https://i.imgur.com/frKefe8.png)


When connecting to a new server for the first time, this message will typically show up. However, if you are using this on a server that you are typically using then it could mean that someone is trying to listen in or control the connection.

Anyhow, continue by inputting `yes` into the terminal, and it will look like the following.

![Image](https://i.imgur.com/jgV4eO7.png)


This is where you input the password that you have created while following the instructions on Step 1.

After inputting your password, you are now connected to a computer in the CSE basement and the commands that you run in your terminal will now run in that specific computer.

## Part 4 - Testing
Now here you can test whether you have successfully connected to the computer in the CSE basement.\
Feel free to run and commands like `cd`, `ls`, `pwd`, `mkdir`, and `cp` and look at the results that come up. When you are done you can log our of the remote server in your terminal with two methods.\
1.) Ctrl/CMD - D\
2.) running the command `exit`


Congratulations on making it this far! You have succesfully accessed your `ieng6` account using VSC and are now ready to venture on. Join me next time as I teach you how to do more stuff with it.
