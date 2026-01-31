# Authentication bypass via information disclosure

My first step here was to enter my username **wiener** and password **peter** and generate a GET request by logging in with these credentials. I forwarded this packet to Repeater and changed **/my-account** to **admin** to see if I would get a specific response from the server. I got a 401 meaning the authentication failed. 

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/49d8f891-bfc4-4e87-87b8-525180f19322" />

My next course of action was to change the GET method to **TRACE**. This will force the server to respond back with how my request looks like after going through all middleware and proxies. It basically echoes my original request and is used for diagnostics which means most servers prevent this type of request from returning to the end-user. I can see the **X-Custom-IP-Authorization** was included in the echo response with my machine's IP.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/db3a5b30-824e-4b22-b663-f17e52af1438" />

From here, I can go back to the Proxy and then **Match and replace**. I then selected **Add** under the **HTTP match and replace**. I left everything the same but added **X-Custom-IP-Authorization: 127.0.0.1** under **Replace**. I then selected test and saw in the auto-modified request that my machine's IP was added to the header.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/51574552-c956-45ba-8e63-5d77df9a1dd8" />

I can see to access the admin panel, I need to send the GET request with my machine's IP in the header of the packet.
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/3d70f4af-e75d-4788-9cd8-b002299c2221" />

After the request is forwarded, I can now see the admin panel is appearing.
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/390011d1-29a1-4f67-8c29-2bab32842f50" />

After clicking on the admin panel, I can now delete carlos.
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/bdafe65c-3c34-43d5-a873-bc898d623b96" />
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/d62324ac-18be-4427-acdf-18c76a6a7907" />
