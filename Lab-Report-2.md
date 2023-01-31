# Lab Report 2 - Servers and Bugs
## Part 1: StringServer
![Image](https://cdn.discordapp.com/attachments/368995972975558656/1069832195893645332/Screen_Shot_2023-01-30_at_8.10.46_PM.png)
This is my code for `StringServer`. I used code from `Server.java` and `NumberServer.java` to help me get started.

![Image](https://cdn.discordapp.com/attachments/368995972975558656/1069832195298050068/Screen_Shot_2023-01-30_at_8.10.22_PM.png)
Using `add-message`, I added "Hello" into my String var `test` with `/add-message?s=Hello`. After compiling with javac and java, it runs the URL through start which starts a new `localhost:___` link for me.  After going through `StringServer` class's main method which validifies port number and start, it calls my handleRequest method. This runs the URL argument `localhost:5007/add-message?s=Hello` through the method and splits the url by the `=` and then in another if statement, splits it again by `s`. This leaves the remaining String after the `=` which is then added to my String test and returned. Test is changed from empty to containing "Hello" due to the `test.concat(parameters[1] + "\n";` line which adds it to the end of the String. 

![Image](https://cdn.discordapp.com/attachments/368995972975558656/1069832195562287156/Screen_Shot_2023-01-30_at_8.10.31_PM.png)
Here, I used the url `localhost:5007/add-message?s=How%20are%20you ` with `%20` in place of spaces. Like earlier, after going through the class's main method, it runs the url argument through handleRequest. However, this time, the argument `parameters[1]` is representing "How are you". The String `How are you` is now added to String `test` on a new line after `Hello`. 

## Part 2: Bugs
```
*  int[] input2= {1, 5, 6};
*  assertArrayEquals(new int[]{6, 5 ,1}, ArrayExamples.reversed(input2)); Expected [6] but was [0]
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
 
The bug I tackled was the reversed method in `ArrayExamples.java`. 

A test that didn't induce failure was:
`int[] input3= {0};`
`assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input3));`
 
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1069841421516939264/Screen_Shot_2023-01-30_at_8.45.40_PM.png)
 ![Image](https://cdn.discordapp.com/attachments/368995972975558656/1069841421760221226/Screen_Shot_2023-01-30_at_8.46.39_PM.png)
 
**Before and After**
Before:
```
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
 Before, the bug was due to `arr[i] = newArray[arr.length-i-1];` as it wasn't grabbing the right index due to the combination of `-i-1`. Also, newArray was  only initialized with size and not data so it was just replacing the `arr[]` values with 0. 

After:
```
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    int tempCount= arr.length;
    for(int i = 0; i < arr.length; i++) {
      newArray[i] = arr[--tempCount];
    }
    return newArray;
  }
```
  To fix the issue, I changed `newArray` to be the array that I was changing the values of and made a int of the original `arr.length` to be safe just in case something changes `arr`'s length. I didn't want to use `arr` directly incase I messed something up that would mess up the rest of the array. I used `tempCount` to keep track of my index with `--` infront so it'd always be one less first when looping. I then changed the return value to `newArray` as it has the new reversed array. 
  
# Part 3: What Have I Learned

To start, the lab was the first time I used jUnit. It took me awhile to understand the differences between the asserts (assertEquals vs assertArrayEquals) and which order to put the arguments in since I was already confused due to a worksheet in class. I also had to understand what could be compared and whatnot, like array to array or size to elements in an array. Adding onto that, I didn't realize we had to create a new object for our expected argument and so that also kind of overwhelmed me along the other `@test` methods but after actually reading the code it made sense.
 
