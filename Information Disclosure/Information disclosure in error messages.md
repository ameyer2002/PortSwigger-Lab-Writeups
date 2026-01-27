# Information disclosure in error messages

As usual, it's essential to generate a HTTP request that can be captured. I generated a GET request and then forwarded it to Repeater so I could modify the packet before sending it to the server. This lab was focused on information leakage within the error message so I had to change the **productId** to a string since the server was expecting an integer. This would generate a proper error message that could be analyzed for potential sensitive information. I looked at the response from the server and found an interesting piece of information at the bottom. **Apache Struts 2 2.3.31** is an open-source web app framework which tells me what the lab is using. 

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/9c67f8c7-ce9e-4ff8-9429-391058bfc54d" />
