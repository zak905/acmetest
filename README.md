# acmetest
Unit test project for le project https://github.com/Neilpang/acme.sh



# Here are the latest status:

| Platform | Status| Last Run Time| Comments|
-----------|-------|--------------|---------|
|windows-cygwin| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/windows-cygwin.svg?1462640779)| Sat, May 07, 2016  5:06:19 PM| Passed |
|freebsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/freebsd.svg?1465015684)| Sat Jun  4 04:48:04 UTC 2016| Passed |
|openbsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/openbsd.svg?1465044824)| Sat Jun  4 12:53:44 UTC 2016| Passed |
|pfsense| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/pfsense.svg?1465046607)| Sat Jun  4 13:23:27 UTC 2016| Passed |
|ubuntu:14.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-14.04.svg?1465046657)| Sat Jun  4 13:24:17 UTC 2016| Failed |
|ubuntu:15.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-15.04.svg?1465046676)| Sat Jun  4 13:24:36 UTC 2016| Failed |
|ubuntu:16.04| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-16.04.svg?1465046696)| Sat Jun  4 13:24:56 UTC 2016| Failed |
|ubuntu:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-latest.svg?1465046719)| Sat Jun  4 13:25:19 UTC 2016| Failed |
|debian:7| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-7.svg?1465046739)| Sat Jun  4 13:25:39 UTC 2016| Failed |
|debian:8| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-8.svg?1465046758)| Sat Jun  4 13:25:58 UTC 2016| Failed |
|debian:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-latest.svg?1465046779)| Sat Jun  4 13:26:19 UTC 2016| Failed |
|centos:5| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-5.svg?1465046799)| Sat Jun  4 13:26:39 UTC 2016| Failed |
|centos:6| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-6.svg?1465046822)| Sat Jun  4 13:27:02 UTC 2016| Failed |
|centos:7| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-7.svg?1465046847)| Sat Jun  4 13:27:27 UTC 2016| Failed |
|centos:latest| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-latest.svg?1465046867)| Sat Jun  4 13:27:47 UTC 2016| Failed |
|fedora:21| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-21.svg?1465046891)| Sat Jun  4 13:28:11 UTC 2016| Failed |
|fedora:22| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-22.svg?1465046914)| Sat Jun  4 13:28:34 UTC 2016| Failed |
|fedora:23| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-23.svg?1465046929)| Sat Jun  4 13:28:49 UTC 2016| Failed |
(The openssl in CentOS 5 doesn't support ECDSA, so the ECDSA test cases failed. However, RSA certificates are working there.)

# How to run tests

First point at least 2 of your domains to your machine, 
for example: `aa.com` and `www.aa.com`

And make sure 80 port is not used by anyone else.

```
cd acmetest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./letest.sh
```

# How to run tests in all the platforms through docker.

You must have docker installed, and also point 2 of your domains to your machine.

Then test all the platforms :

```
cd acmetest
TestingDomain=aa.com   TestingAltDomains=www.aa.com  ./rundocker.sh  testall
```

The script will download all the supported platforms from the official docker hub, then run the test cases in all the supported platforms.






