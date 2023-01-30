# Lab Report #2
## Part 1
### StringServer.java
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> strings = new ArrayList<>();

    public String handleRequest(URI url) {
        //format: /add-message?s=<string>
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            strings.add(parameters[1]);
            return String.join("\n", strings);
        }
        return "404 improper request";
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

### Examples of add-message
<img width="528" alt="Screen Shot 2023-01-29 at 12 06 20 PM" src="https://user-images.githubusercontent.com/97646090/215353104-c04e2ff1-5899-4030-bd3e-94765d0fcf0b.png">

* Calls the handleRequest method
* Argument is "http://localhost:4000/add-message?=loop" and the local field strings is empty
* Changes the strings field by adding the string "loop" to it <img width="518" alt="Screen Shot 2023-01-29 at 12 07 15 PM" src="https://user-images.githubusercontent.com/97646090/215353018-29b23bbd-125a-4ea0-a619-447a5fdb0c11.png">
* Calls the handleRequest method
* Argument is "http://localhost:4000/add-message?=loop" and the local field strings is ["loop","de"]
* Changes the strings field by adding the string "loop" to it

## Part 2
Induces Failure:
```
  @Test 
	public void testReverseInPlaceFails() {
    int[] input1 = {1,2,3,4,5,6};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{6,5,4,3,2,1}, input1);
	}
```
Doesn't Induce Failure:
```
   @Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
Symptom:
The test that Induced Failure returned with the following messange:
<img width="571" alt="Screen Shot 2023-01-29 at 5 52 42 PM" src="https://user-images.githubusercontent.com/97646090/215371394-acdc098a-160d-49e3-9a6d-f725a96dae5b.png">

Before:
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
After:
```
  static void reverseInPlace(int[] arr) {
    int[] reverse = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      reverse[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < reverse.length; i++){
      arr[i] = reverse[i];
    }
  }
```
Why the changes fixed the problem: <br />
The bug in the before code was that `arr` was being overwritten in the middle of the program. So, to fix this, we make a new array object so as to not overwrite `arr`.

## Part 3
In lab 2 I learned how to set up a server in java, how you need specific port numbers, and how you can use a url as an argument.
