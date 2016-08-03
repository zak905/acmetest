# acmetest
Unit test project for le project https://github.com/Neilpang/acme.sh



# Here are the latest status:

| Platform | Status| Last Run Time| Comments|
-----------|-------|--------------|---------|
|windows-cygwin| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/windows-cygwin.svg?1462640779)| Sat, May 07, 2016  5:06:19 PM| Passed |
|freebsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/freebsd.svg?1466114181)| Thu Jun 16 21:56:21 UTC 2016| Passed |
|openbsd| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/openbsd.svg?1466148414)| Fri Jun 17 07:26:54 UTC 2016| Passed |
|pfsense| ![](https://cdn.rawgit.com/Neilpang/letest/master/status/pfsense.svg?1466154740)| Fri Jun 17 09:12:20 UTC 2016| Passed |
|ubuntu:14.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-14.04.svg?1470195716)| Wed Aug  3 03:41:56 UTC 2016| Passed |
|ubuntu:15.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-15.04.svg?1470195871)| Wed Aug  3 03:44:31 UTC 2016| Passed |
|ubuntu:16.04| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-16.04.svg?1470196051)| Wed Aug  3 03:47:31 UTC 2016| Passed |
|ubuntu:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/ubuntu-latest.svg?1470196230)| Wed Aug  3 03:50:30 UTC 2016| Passed |
|debian:7| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-7.svg?1470196382)| Wed Aug  3 03:53:02 UTC 2016| Passed |
|debian:8| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-8.svg?1470196538)| Wed Aug  3 03:55:38 UTC 2016| Passed |
|debian:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/debian-latest.svg?1470196691)| Wed Aug  3 03:58:11 UTC 2016| Passed |
|centos:5| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-5.svg?1470196788)| Wed Aug  3 03:59:48 UTC 2016| Failed |
|centos:6| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-6.svg?1470196949)| Wed Aug  3 04:02:29 UTC 2016| Passed |
|centos:7| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-7.svg?1470197121)| Wed Aug  3 04:05:21 UTC 2016| Passed |
|centos:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/centos-latest.svg?1470197292)| Wed Aug  3 04:08:12 UTC 2016| Passed |
|fedora:21| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-21.svg?1470197465)| Wed Aug  3 04:11:05 UTC 2016| Passed |
|fedora:22| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-22.svg?1470197645)| Wed Aug  3 04:14:05 UTC 2016| Passed |
|fedora:23| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-23.svg?1470197816)| Wed Aug  3 04:16:56 UTC 2016| Passed |
|fedora:latest| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/fedora-latest.svg?1470197988)| Wed Aug  3 04:19:48 UTC 2016| Passed |
|opensuse:13.2| \![](https://cdn.rawgit.com/Neilpang/letest/master/status/opensuse-13.2.svg?1470198142)| Wed Aug  3 04:22:22 UTC 2016| Passed |
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






