# Week 7 Lab Report

Hello and welcome back to Lab Reports with Ethan. This week we are going over the concept that was done during the week 7 lab. Buckle up since there is many things that we are going to go over today.




Lets begin with the setup should we? 

To start off, we need to fork the repository given to us. Which is this [link](https://github.com/ucsd-cse15l-w23/lab7) <--.
![image](https://i.imgur.com/dG84LSh.png)

After you for the repository you are ready to begin the steps.

## Step 1: Login to your ieng6 account
Login to your ieng6 account with `ssh cs15lwi23___@ieng6.ucsd.edu`(fill in the blank with your unique username).
![image](https://i.imgur.com/xVL9acX.png)

## Step 2: Cloning your github repository
Go to your github that you have previously forked. 

Go to Clone>Local>SSH and copy the link so you can prepare the clone.
![image](https://i.imgur.com/u6Hygu2.png)

After copying that link go back to your terminal and type the following `git clone {github url that you copied)`. To paste the url that you have copied just do `<right click>` on your mouse at the area where you want to paste it.

 ![image](https://i.imgur.com/fL6YIZ3.png)
  
  Congratulations! You have now cloned the repository into your `ieng6` account.
  
  ## Step 3: Failing our Tests
That's right you read it properly. We need to show that we failed our tests. 
First, we have to change our directory to the right one, so let's cd into lab7.
Simply just type `cd l<tab>` and it should automatically turn to `cd lab7/`.

![image](https://i.imgur.com/fhoiklU.png)

For the next part, we can reference our week 3 lab and copy the following code.
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java 
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ________
```

In the blank, you want to fill that with `L<tab>`. Unfortunately, we are unable to just tab this one easily this time, because it'll become `<ListExamples>` you have to type `<T><tab>` for it to become `<ListExamplesTests.>` At that point, just `<backspace>` to delete the extra period so it'll beomce `ListExamplesTests.

Either way, we should now be able to see the failure after you run the two lines of code there.
![image](https://i.imgur.com/YJ4YKSn.png)

## Step 4: Fixing the issue
So now that we found out that we are wrong, we need to fix it. 

For this we will utilize the `nano` command. The error is in the file `ListExamples.java` on line 43 character 13, so we can type something like `nano +43,13 L<tab>.java` and it will look something like this.

![image](https://i.imgur.com/S9zi829.png)

After submitting that command you will be taken to the code and the exact area of the error. Do the following `<backspace> <2>`. That way you will edit the `index1` into `index2` and then click `<ctrl> + <x>, <y>, <enter>` and the file should now be saved with the new edit.

![image](https://i.imgur.com/F5oUcYe.png)
![image](https://i.imgur.com/ADcvvgH.png)
![image](https://i.imgur.com/m1OC8pZ.png)

## Step 5: Redemption Hour
That's right, lets see if our code works now. Do the following `<up>, <up>, <up>` and you should reach the javac command from earlier. After compiling the files, we can run it. Press `<up>, <up>, <up>` to get to the Java command and run it.
  ![image](https://i.imgur.com/wsBivpA.png)
  
  Congrats! Your new code now works.
  
## Step 6: Commiting and pushing
  So, we basically want to save all this information in our Github account. So to do that we need to git add the changed file and commit it then push it.
  so do `git add L<tab>.java`. Then do `git commit -m "done"` which essentially commits the file with the comment of "done". And lastly we only need to push it with a `git push` command. 
  
  ![image](https://i.imgur.com/T7ao17E.png)
  
## El Fin
  Congratulations, you have completed the task, now you can find stupid ways to speed it up like making it in mostly one command like this. 
  
  ```
  ssh cs15lwi23xxx@ieng6.ucsd.edu

git clone git@github.com:helisoai/lab7.git && cd lab7 && javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java && java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples 


nano +43,13 ListExamples.java



javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java && java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples && git add ListExamples.java && git commit -m "done" && git push
  ```
