# Repository with scripts to verify system against CVE
Scripts to verify vulnerable software

Run with: 

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
