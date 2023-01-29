# Lab Report #2
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
