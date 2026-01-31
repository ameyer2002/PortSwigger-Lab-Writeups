# Source code disclosure via backup files

Since this lab is focused on checking for the source code, I went ahead and generated a HTTP request which I forwarded to Repeater and found nothing interesting in the returned HTML. What I did here was append **/robots.txt** to the URL of the web app. Essentially, what this does is it has search engines check the root of the website to see what is available to users and what isn't. As seen below, the path **/backup** is technically not allowed to be accessed but for the sake of this lab and learning, I'll want to append this to the URL now.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/536850fa-3df5-4d0f-862e-fa0c0be9be72" />
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/bcbfdfbd-689d-4613-a13f-f2f6662b05a7" />

After accessing this page, I can open up this file to look at the source code written in JS. The goal for this lab is to find the database password which is supposed to be hardcoded in the source code. After reviewing everything, I can see there is a long string of numbers and letters which tells me this is likely the password. I can see the port number **5432** which is PostgreSQL's port number is listed right above too.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/5cc30fa1-3ffa-4c39-abe7-845d771ba9d3" />
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/12209d78-2fe0-4769-be6a-bb461f924e18" />
