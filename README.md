# Repository with scripts to verify system against CVE
Scripts to verify vulnerable software

Update: 12-07-2022 Updated script to include the new vulnerability of OpenSSL CVE-2022-2068

    wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2022-2068.sh -O -|bash
    
Update: 13-06-2022 Added script to check OpenSSL c_rehash script vulnerability CVE-2022-1292

    wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2022-1292.sh -O -|bash

Update: 04-05-2022 Added script to check Nimbuspwn vulnerability CVE-2022-1292 (Privilege escalation vulnerabilities discovered in Linux)

    wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2022-29799_CVE-2022-29800.sh -O -|bash


Update: 02-02-2022 Added script to check Samba vulnerability CVE-2021-44142 (Out-of-bounds heap read/write vulnerability in VFS module vfs_fruit allows code execution)

    wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-44142.sh -O -|bash

Run with (change the name of script based on CVE you want check): 

wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-4034.sh -O -|bash

or with older distribution (with no support for TLS...)

wget -q --no-check-certificate https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-4034.sh -O -|bash

Note: adding --fix the script try to patch the system

Example:

manager@elk2:~$ wget -qO - https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-4034.sh | bash

Detected O.S. : Ubuntu 20.04 focal

My version (0.105-26ubuntu1.1) is lower than version (0.105-26ubuntu1.2) with the patch

System vulnerable!


Example with auto-fix (require sudo):

manager@elk2:~$ wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-4034.sh -O -|sudo bash /dev/stdin --fix

Run with auto-fix enabled!

Detected O.S. : Ubuntu 20.04 focal

My version (0.105-26ubuntu1.1) is lower than version (0.105-26ubuntu1.2) with the patch

System vulnerable!


manager@elk2:~$ wget -q https://raw.githubusercontent.com/backloop-biz/CVE_checks/main/CVE-2021-4034.sh -O -|sudo bash /dev/stdin --fix

Run with auto-fix enabled!

Detected O.S. : Ubuntu 20.04 focal

My version (0.105-26ubuntu1.2) is same than version (0.105-26ubuntu1.2) with the patch

System not vulnerable
