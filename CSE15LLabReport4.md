This is my lab report 4 for CSE 15L. In this lab report, I will go over how I completed the tasks mentioned in the lab 7 competition on my own. I will describe the keys that I pressed and the steps that I took to complete each task and get the desired outcome. There are 5 steps in total and I will describe each of them starting from the first one below.

1.) Log into ieng6

Keys pressed: `<command + c>` `<command + v>` `<enter>` `<command + c>` `<command + v>` `<enter>`

To log into ieng6, I had to copy paste the command "ssh cs15lwi23apl@ieng6.ucsd.edu" into the terminal and the password associated with my account into the terminal to log in. Hence I had to use the `<command + c>` `<command + v>` to copy and paste. 
![image](https://user-images.githubusercontent.com/122566208/221774014-467bdcec-b86e-4edf-87c9-f3669dd0f81d.png)

2.) Clone your fork of the repository from your Github account

Keys pressed: "git" "clone" `<command + c>` `<command + v>` `<enter>`

To clone my fork of the lab 7 repository, I had to type in the words "git" and "clone" into the terminal. After that, in order to copy and paste the URL of my fork of the repository into the terminal, I had to use the keys `<command + c>` `<command + v>`.
![image](https://user-images.githubusercontent.com/122566208/221777441-5b02c596-7ad2-4540-86ca-1d9bfc944ad8.png)

3.) Run the tests, demonstrating that they fail

Keys pressed: `<command + c>` `<command + v>` `<up>` `<enter>`



In order to run the Junit tests, I had to copy and paste the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command into the terminal using `<command + c>` `<command + v>`. Furthermore, in order to access the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ` command from the command above I used the `<up>` command.
![image](https://user-images.githubusercontent.com/122566208/221780067-aede4f0c-a27e-466f-9c00-e8b83a19f402.png)

4.) Edit the code file to fix the failing test

Keys pressed: "nano ListExamples.java" `<enter>` `<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>` `<delete>` `<delete>` `<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>``<down>` `<delete>` "2" `<ctrl + o>` `<ctrl + x>` 

In order to access the java file "ListExamples.java", I need to enter the "nano" command followed by the file name. After that, in order to access and correct the bugs in the code in the file "ListExamples.java", I had to use the `<down>` and `<delete>` keys a lot. The  `<down>` keys were used to get to the bug in the code and `<delete>` keys were used to delete lines/words of code causing the bugs. `<ctrl + o>` `<ctrl + x>` were used to save the changes in the code and to exit the file respectively.
![image](https://user-images.githubusercontent.com/122566208/221785534-c9c38491-4896-451f-935f-4c8490992f03.png)
![image](https://user-images.githubusercontent.com/122566208/221785620-83e40a58-b1f3-4cd6-b2a6-19011eb2e3b8.png)

5.) Run the tests, demonstrating that they now succeed

Keys pressed: `<up>` `<up>` `<enter>` `<up>`  `<up>`  `<up>` `<enter>` 

In order to run the Junit tests again, I just used the `<up>` key to access the commands used to compile and run the Junit tests previously. The compile command given by `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` was accessed first using the `<up>` key. Thereafter, the tests were run using the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ` command which was also accessed using the `<up>` key.
![image](https://user-images.githubusercontent.com/122566208/224869267-002712b4-7d04-4501-b18d-c19f3e15bedd.png)

5.) Commit and push the resulting change to your Github account

Keys pressed: "git" `<tab>` "add" `<tab>` "ListExamples.java" `<enter>` "git" `<tab>` "commit" `<tab>` "-m" `<tab>` ""x"" `<enter>` "git" `<tab>` "push" `<tab>` "origin" `<tab>` "main"  `<enter>`

In order to push the changes made to the "ListExamples.java" file, I used the " add", "commit", and "push" commands.
![image](https://user-images.githubusercontent.com/122566208/224887064-c4e4b7c5-29ab-4b3d-9e17-b4f0ede57a6d.png)


