# File Path Traversal, Simple Case

**Scenario**: This lab contains a path traversal vulnerability in the display of product images.
To solve the lab, retrieve the contents of the /etc/passwd file.

This lab was extremely easy and quick. One HTTP request to be modified with an altered path in the header and that's it. As you can see below, I modified the file name to be **../../../etc/passwd**, forwarded the request, and the response from the server was a dump of the content from the **/etc/passwd** file.

<img width="1918" height="920" alt="image" src="https://github.com/user-attachments/assets/4584a45f-3a54-4657-bb2e-85c329d643ff" />


