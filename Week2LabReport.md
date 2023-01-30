# Week 2 Lab Report
Welcome and congradulations on making into the third week of the CSE 15L course. Today, I, your instructor, will show you the way on how to \
1.)  Create a server that adds strings and prints it on top of itself \
2.) Talk about bugs that have happened during the Lab Session today, and how you could possibly fix it. \
3.) Talk about things that was new overall. 

Are you ready? If so, lets get down to it!

## Part 1 - creating the site
So during week two of the CSE 15L course, we learned about how to make a server during our lab session. This material is very essential in the overall creation of our server.
Head to the [wavelet github](https://github.com/ucsd-cse15l-f22/wavelet) and download it onto your computer. 

Honestly speaking, you will not need the NumberServer.java since you will be recreating something else known as StringServer. \
Create a new file in the same folder called StringServer and import the following. 
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
```

By importing those, we can create ArrayList within the code that can be printed on the server/website.
Next fill the file up with the following code.
```
class Handler implements URLHandler {
    
    ArrayList<String> store = new ArrayList<>();

    public String handleRequest(URI url) {
        String holder = "";
        if (url.getPath().equals("/")) {
            for(int i = 0; i < store.size(); i++){
                holder += store.get(i) + "\n";
            }
            return holder;


        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");

                store.add(parameters[1]);

                for(int i = 0; i < store.size(); i++){
                    holder += store.get(i) + "\n";
                }
                return holder;
                
            }
            return "404 Not Found!";
        }
    }
}


public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
The following code uses the information that you use in the url and display them on the text. \
In the command prompt Javac the following:
```
javac Server.java StringServer.java
```
Next, you follow it up with a:
```
java StringServer {whatever port you want}
```
This allows you to start up the server with the program.

Within the url you can type after your port `/add-message?s={whatever message you want}`. Below is an example.
![image](https://i.imgur.com/aRsBrMv.png) \

You can add more and it will look something similar like this. \
![image](https://i.imgur.com/9iFHksY.png) \
