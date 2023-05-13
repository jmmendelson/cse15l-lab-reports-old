# Part 1  

This is my code for StringServer. I changed the StringServer we used for the skill demo to create this one.  

<img width="687" alt="Screen Shot 2023-05-12 at 9 28 45 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/8446c248-fa4f-473a-872a-6d8b183c77cb">

---

This is the terminal running the server:  

<img width="601" alt="Screen Shot 2023-05-12 at 9 30 43 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/2fed15d7-814c-4a03-9bd8-dc7fde0588ad">

---

This is the first screenshot of using add-message:  

<img width="394" alt="Screen Shot 2023-05-12 at 9 32 02 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/20ec0134-fb4a-4856-8535-659db6d534ec">  

The method called is .start with the class Server. The first argument we are sending is the port number, which we get from the first argument as a string and parse it into an integer. The second argument is the StringHandler class I wrote in StringServer.java. After going to Server.java we use the method handleRequest which we pass in the url as an argument. We declare an empty ArrayList outside of the method that will hold all the words we type at the end of the url. First, we check if the key word "/add-message" is in the url, then if it is it checks whether the query, which follows a ?, starts with "s=" which indicates that we'll enter a string. Then we add the string to the right of the equal sign to the ArrayList, and then we print the string we wrote which is "hello".

---

This is the second screenshot of using add-message:

<img width="495" alt="Screen Shot 2023-05-12 at 9 32 26 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/548a05cb-623c-432c-896b-08ac5b1b9e99">

The same methods were called here as before, the difference is that now when we add "how are you" everything in the ArrayList is printed so it prints the first message we wrote, "hello", and then prints "how are you".

---

# Part 2  

A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown):

`@Test`  
`public void testReverseInPlaceBug() {`   
`    int[] input1 = {3, 4};`  
`    ArrayExamples.reverseInPlace(input1);`  
`    assertArrayEquals(new int[]{4, 3}, input1);`  
`}`  

---

An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown):  
  
`@Test`  
`public void testReverseInPlaceBug() {`   
`    int[] input1 = {3, 4};`  
`    ArrayExamples.reverseInPlace(input1);`  
`    assertArrayEquals(new int[]{4, 3}, input1);`  
`}`  

---

The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above) 
  
First input:

<img width="935" alt="Screen Shot 2023-05-12 at 11 38 20 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/fbd3c1ed-fdae-4242-ae5c-9929d7fa3867">  
  
Second input:  

<img width="149" alt="Screen Shot 2023-05-12 at 11 40 04 PM" src="https://github.com/jmmendelson/cse15l-lab-reports/assets/130113062/67048604-f378-4563-ac60-e29681c84778">  

---

The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)  

Before:  

`static void reverseInPlace(int[] arr) {`  
`    for(int i = 0; i < arr.length; i += 1) {`  
`        arr[i] = arr[arr.length - i - 1];`  
`    }`  
`}`  
  
After:  
`static void reverseInPlace(int[] arr) {`  
`    for(int i = 0; i < arr.length / 2; i += 1) {`  
`        int temp = arr[i];`  
`        arr[i] = arr[arr.length - i - 1];`  
`        arr[arr.length - i - 1] = temp;`  
`    }`  
`}`  
  
This new code fixes the issue by introducing a temporary variable that can store the variable to to be swapped, and the for loop iterates to the middle of the array, with each iteration switching the current element with the one opposite the middle of the array.

---

# Part 3  

Something that I learned in week 2 that I didn't know before was that you can create a server using Java. It hadn't occurred to me that you could create a server/ working url within an IDE.
