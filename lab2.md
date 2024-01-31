**# Lab Report 2:
---
**Code of `ChatServer`**
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String chatMessages = "";

    public String handleRequest(URI url) {
        if(url.getPath().equals("/")) {
            return "What is the message implemented?";
        }
        else if (url.getPath().equals("/add-message")) {
            String query = url.getQuery();
            int messageIndex = query.indexOf("s=");
            int ampersandIndex = query.indexOf("&");
            int userIndex = query.indexOf("user=");

            if(messageIndex != -1 && userIndex != -1) {
                String message = query.substring(messageIndex + 2, ampersandIndex);
                String user = query.substring(userIndex + 5);
                chatMessages +=String.format("%s: %s%n", user, message);
            }
            return chatMessages.toString();
        } else {
            return "404 Not Found!";
        }
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
        }
}
```
**Using the `/add-message` on the port that prints out the message**
