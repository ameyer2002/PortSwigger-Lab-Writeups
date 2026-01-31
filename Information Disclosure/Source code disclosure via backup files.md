# Source code disclosure via backup files

Since this lab is focused on checking for the source code, I went ahead and generated a HTTP request which I forwarded to Repeater and found nothing interesting in the returned HTML. What I did here was append **/robots.txt** to the URL of the web app. Essentially, what this does is it has search engines check the root of the website to see what is available to users and what isn't. As seen below, the path **/backup** is technically not allowed to be accessed but for the sake of this lab and learning, I'll want to append this to the URL now.

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/536850fa-3df5-4d0f-862e-fa0c0be9be72" />
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/bcbfdfbd-689d-4613-a13f-f2f6662b05a7" />

