# Lab Report 2 - Servers and SSH Keys (Week 3) {#week-3-lab-report}
# Part 1 ChatServer.java
<br>![Image](ChatServer.png)
<br>
<br>**ScreenShot 1**
<br>![Image](addMessage1.png)
<br>**Which methods in your code are called?** -> The `main` method and `handleRequest` method are called.
<br>**What are the relevant arguments to those methods, and the values of any relevant fields of the class?** -> The argument to `main` are the command line arguments, which is `4000` for the port number. The argument to `handleRequest` is the URL of the server browser, which is `http://localhost:4000/add-message?s=Hello&user=achiuwei`. The value of the `String` chat field is originally `""`.
<br>**How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.** -> The value of the `String` chat field is updated from `""` to `"achiuwei: Hello"`. This is because of the query of the URL.
<br>
<br>**ScreenShot 2** 
<br>![Image](addMessage2.png)
<br>**Which methods in your code are called?** -> The `main` method and `handleRequest` method are called.
<br>**What are the relevant arguments to those methods, and the values of any relevant fields of the class?** -> The argument to `main` are the command line arguments, which is `4000` for the port number. The argument to `handleRequest` is the URL of the server browser, which is `http://localhost:4000/add-message?s=Hi`. The value of the `String` chat field is originally `""`.
<br>**How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.** -> The value of the `String` chat field is not updated because the query of the URL was missing the correct elements. Instead of the the `String` chat field updating and displaying, an error message, `/add requires two query parameters seperated by &`, was displayed instead.
<br>
# Part 2 SSH Key
<br>**The absolute path to the private key for your SSH key for logging into `ieng6`**
<br>![Image](privateKey.png)
<br>
<br>**The absolute path to the public key for your SSH key for logging into `ieng6`**
<br>![Image](publicKey.png)
<br>
<br>**A terminal interaction where you log into your `ieng6` account without being asked for a password**
<br>![Image](noPass.png)
<br>
# Part 3 ChatServer.java
<br>From the lab in week 2, I learned how to create and run my own server. In this process, I also learned how to get arguments from a URL and change what is displayed and stored based on the URL. In addition, I also learned how to get command line arguments when I had to get the port number to run the server.
