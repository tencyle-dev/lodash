# Fork of lodash

Note: This is *not* an official release of lodash and it is not associated with the official lodash maintainers

## Versions available

* v3.10.1 with critical vulnerabilities resolved by means of backporting

If you are looking for the official version of lodash v3.10.1, it can be found in https://github.com/lodash/lodash/3.10.1


##  v3.10.1 fork details

This is a fork of lodash v3.10.1 with the following critical vulnerabilities *resolved* by means of bacport:

* CVE-2021-23337
* CVE-2019-10744
* CVE-2018-16487
* CVE-2018-3721

The following vulnerabilities *still exist* in this version:
* CVE-2020-28500
* CVE-2019-1010266
* CVE-2020-8203 (but see note below)

### Note regarding cve CVE-2020-8203: 
This CVE deals with zipObjectDeep API which doesn't exist yet in 3.10.1.
However, the root cause of the issue seems to be that the path functions allow setting of 'prototype', '__proto__' and 'constructor'. This behaviour isn't a vulnerability in it of itself, however, users must be careful using the path api.

We decided not to resolve this since it isn't a vulnerability on its own and it could break code that uses lodash and depends on this behavior (as indeed lodash's unit testing in version 3.10.1 does!)

-- Tencyle Dev
