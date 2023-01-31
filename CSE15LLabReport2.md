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
In this part of the lab report, I will pick a bug from the starter code provided to us for lab 3. After that, I will provide some inputs for and symptoms of the buggy program before explaining the code change required to fix the program. So, let's consider the reversed method in the ArrayExamples class which takes an array of integers as input and returns a new array with all the elements of the input array in reversed order. On testing the method as the JUnit test provided in the code block below, we get the wrong output.
```
@Test
  public void testReversed1() {
    int[] input2 = {34, 56, 89, 100};
    assertArrayEquals(new int[]{100, 89, 56, 34}, ArrayExamples.reversed(input2));
  }
```
The test above takes in the input array {34, 56, 89, 100} and, according to the way the method reversed is supposed to work, should return a new array {100, 89, 56, 34}. However, on running the test above we do not get the expected output. 
```
 @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
However, in contrast to testReversed1(), testReversed(), the test shown in the code block above, works perfectly well and produces the output we expect it to produce. The image below serves as the symptom of the bug for the method reversed.
![image](https://user-images.githubusercontent.com/122566208/215669236-1f9cfed3-2f37-4af2-a025-58c88e508dfc.png)
In order to fix the bug, we have to change the reversed method from its original state, shown in the code block below.
```
 static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
From this original state, we change the method into the code block shown below in order to fix the bug.
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
So, in order to fix the bug, we have to change a couple of things in the original code block. Firstly, the original code block, instead of modifying the elements of the new array while looping through them, modifies the elements of the input array while looping through them instead. In order to fix this, change the for loop so that it iterates through and modifies the elements of the new array. Secondly, the original code block returns the input array instead of returning a new array as the method is supposed to. Therefore, we change the return statement of the method so that it returns a new array instead of the input array. By making these changes, we are able to fix the reversed method in ArrayExamples.java

Part 3:
In the final part of this lab report, I will describe something that I learned over the course of the last few labs that I didn't know before. Over the course of the last 2 labs, I learned how to create and set up a web server of my own, which is something I didn't know how to do before. I feel that this is a very exciting skill for me to learn because I have always wanted to create websites and web pages of my own. After learning this skill, I really want to learn even more about developing web pages and setting up servers because not only have I been very interested in doing so as I mentioned above but also because I think it is an essential and useful skill to possess in the modern world.
