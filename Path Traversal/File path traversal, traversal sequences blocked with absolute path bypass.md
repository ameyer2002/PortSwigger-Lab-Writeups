# File Path Traversal, Traversal Sequences Blocked with Absolute Path Bypass

**Scenario**: This lab contains a path traversal vulnerability in the display of product images.
The application blocks traversal sequences but treats the supplied filename as being relative to a default working directory.
To solve the lab, retrieve the contents of the /etc/passwd file.

Very easy and short lab. I changed the file name to **/etc/passwd** and the server responded with a dump of the file. /etc/passwd is a Unix system file that contains user account information. Passwords are not included but sensitive information is still provided. 

<img width="1918" height="920" alt="image" src="https://github.com/user-attachments/assets/5f81fc44-ad0c-4a13-9428-8bbc12ea1069" />

The difference between **/etc/passwd** and **../../../etc/passwd/**:
* /etc/passwd is an absolute path and starts from the filesystem root /. It goes directly to the file /etc/passwd.
* ../../../etc/passwd uses .. to go up one directory. ../../../ goes up three directories then goes into the file etc/passwd.
