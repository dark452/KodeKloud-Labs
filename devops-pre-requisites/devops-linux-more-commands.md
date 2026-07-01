# devops-linux-more-commands

1.- Which user is current user on `host01` server?

```bash
thor@host01 ~$ whoami 
thor
```

2.- What is id of `thor` user?

```bash
thor@host01 ~$ id
uid=1001(thor) gid=1001(thor) groups=1001(thor),10(wheel)
```

3.- Which command you will use to switch to `ansible` user?

```bash
su ansible
```

4.- Which command you will use to login to other server with IP `172.16.238.3` and `thor` user?

```bash
thor@host01 ~$ ssh thor@172.16.238.3
```

5.- Which of the following files is present in the `/root` directory?

Note: Normal user doesn't have permission to view files under `/root` directory so you will have to gain higher privileges to see files under the `/root`.

```bash
thor@host01 ~$ sudo su
root@host01 /home/thor# ll /root
bash: ll: command not found
root@host01 /home/thor# ls -larth /root
total 64K
-rw-r--r-- 1 root root  129 Aug 10  2021 .tcshrc
-rw-r--r-- 1 root root  100 Aug 10  2021 .cshrc
-rw-r--r-- 1 root root  141 Aug 10  2021 .bash_profile
-rw-r--r-- 1 root root   18 Aug 10  2021 .bash_logout
-rw------- 1 root root 3.8K Jul  8  2024 original-ks.cfg
-rw------- 1 root root  435 Jul  8  2024 anaconda-post.log
-rw------- 1 root root   95 Jul  8  2024 anaconda-post-nochroot.log
-rw------- 1 root root 4.1K Jul  8  2024 anaconda-ks.cfg
-rw-r--r-- 1 root root  518 Apr  2 15:14 .bashrc
drwxr-xr-x 3 root root 4.0K Jun 29 01:05 .local
dr-xr-x--- 1 root root 4.0K Jun 29 01:05 .
drwx------ 1 root root 4.0K Jun 29 02:13 .ssh
drwx------ 2 root root 4.0K Jun 29 02:13 .terminal_logs
dr-xr-xr-x 1 root root 4.0K Jun 29 02:21 ..
```

6.- Which command can't be used to download file over internet?

- [ ] `curl`
- [x] **`ping`**
- [ ] `wget`

7.- Download the target file to `host01`.

Target file name: `dummy.pdf`

Target file URL: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`

Target directory: `/home/thor`

```bash
thor@host01 ~$ wget https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf
--2026-06-29 02:24:44--  https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf
Resolving www.w3.org (www.w3.org)... 104.18.22.19, 104.18.23.19, 2606:4700::6812:1713, ...
Connecting to www.w3.org (www.w3.org)|104.18.22.19|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13264 (13K) [application/pdf]
Saving to: ‘dummy.pdf’

dummy.pdf            100%[====================>]  12.95K  --.-KB/s    in 0s      

2026-06-29 02:24:44 (116 MB/s) - ‘dummy.pdf’ saved [13264/13264]

thor@host01 ~$ ls -alrth
total 48K
-rw-r--r-- 1 thor thor  13K Aug 27  2007 dummy.pdf
-rw-r--r-- 1 thor thor   18 Feb 15  2024 .bash_logout
drwxr-xr-x 1 root root 4.0K Apr  2 15:14 ..
-rw-r--r-- 1 thor thor  581 Apr  2 15:14 .bashrc
-rw-r--r-- 1 thor thor  695 Jun 29 01:05 .bash_profile
-rw-r--r-- 1 thor thor  165 Jun 29 02:24 .wget-hsts
drwx------ 1 thor thor 4.0K Jun 29 02:24 .
thor@host01 ~$ pwd
/home/thor
```

8.- Where can you find OS information of the Linux servers?

```bash
/home/thor
thor@host01 ~$ cat /etc/os-release 
NAME="CentOS Stream"
VERSION="9"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="9"
PLATFORM_ID="platform:el9"
PRETTY_NAME="CentOS Stream 9"
ANSI_COLOR="0;31"
LOGO="fedora-logo-icon"
CPE_NAME="cpe:/o:centos:centos:9"
HOME_URL="https://centos.org/"
BUG_REPORT_URL="https://issues.redhat.com/"
REDHAT_SUPPORT_PRODUCT="Red Hat Enterprise Linux 9"
REDHAT_SUPPORT_PRODUCT_VERSION="CentOS Stream"
```

9.- Which OS is running on `host01` server?

From previous output is CentOS Stream

10.- Which version of the CentOS is running on the `host01` server?
From previous output is CentOS Stream 9