This is my Lab Report 2 for CSE 15L. This lab report will be split into 3 parts. In part 1, I will describe and explain my program for a web server called StringServer, which keeps track of a string and adds to that string on commands/requests. In part 2, I will go over the process of debugging a buggy method from our starter code for lab 3. Lastly, in part 3 I will describe a new concept/idea that I learned over the course of our last two labs.

Part 1:
For part 1, I wrote a web server call StringServer. StringServer is a web server which keeps track of a string and adds to that aforementioned string upon commands. My code for the program StringServer is shown below.
![image](https://user-images.githubusercontent.com/122566208/215642853-782ebfba-4e99-4b61-bcc7-ca178038c97d.png)
The server implements a /add-message request which concatenates a new line and the string after the "=" sign in the URL to the existing string. After doing that, it returns the modified existing string. An example of this is shown below when the string "Hello" is added to an existing empty string. 
![image](https://user-images.githubusercontent.com/122566208/215657313-1a6c4b30-37fc-4a21-ab46-2621b51d783d.png)
In the image above, the handleRequest method inside class Handler is called. The arguement to the method is the URL "http://localhost:5000/add-message?s=Hello". Since this the first modification applied on the original string "yum", the value of yum is going to be the original value "". After running the request, the value of yum changes from "" to "Hello". 
![image](https://user-images.githubusercontent.com/122566208/215663561-ab53a6df-2911-476b-97f6-31ec70efea90.png)
In the image above, the handleRequest method imside the Handler class is called again. The argument to the method is going to be the URL "http://localhost:5000/add-message?s=What%20is%20your%20name?". The value of yum is going to be "Hello" since that was what the last modification of yum left us with. However, after running the request shown in the image above, the value of yum will change from "Hello" to "Hello" and then "What is your name?" in the new line.

Part 2:
