# Information disclosure on debug page

Per usual, I generated a HTTP request, captured it, and send the packet to Repeater. I then send the packet to the server. In the response, I saw a path **/cgi-bin/phpinfo.php** directing me to a debug page so I appended this to the URL.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/3fb66a74-b196-485d-8b7d-4fb9cce2c3fa" />
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/a7f65917-faa0-4854-a205-0537e7fc3b0b" />

To solve the lab, I have to find the **SECRET_KEY** which I can simply **ctrl+f** and search for which completes this lab.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/0735f1f5-b42f-4b62-b220-b85f1b57ede4" />
