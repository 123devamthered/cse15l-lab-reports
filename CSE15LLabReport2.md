This is my Lab Report 2 for CSE 15L. This lab report will be split into 3 parts. In part 1, I will describe and explain my program for a web server called StringServer, which keeps track of a string and adds to that string on commands/requests. In part 2, I will go over the process of debugging a buggy method from our starter code for lab 3. Lastly, in part 3 I will describe a new concept/idea that I learned over the course of our last two labs.
Part 1:
For part 1, I wrote a web server call StringServer. StringServer is a web server which keeps track of a string and adds to that aforementioned string upon commands. My code for the program StringServer is shown below.
![image](https://user-images.githubusercontent.com/122566208/215642853-782ebfba-4e99-4b61-bcc7-ca178038c97d.png)
The server implements a  /add-message request which concatenates a new line and returns the string after the "=" sign in the URL. 
