# Pam-mysql fork from source forge with some fix

Pam-mysql seems to be unmaintained, so i decided to provide some fixes.

  - Memory leak error | Fix
  - SHA1 and MD5 encryption | Fix

## Compilation

```sh
$ ./configure --with-cyrus-sasl2 --with-openssl
$ make
$ make install 
```
Compiled files can be found here :

```sh
/lib/security/pam_mysql.so
/lib/security/pam_mysql.la
```

### Enable SHA1 and MD5 encryption

Thanks to : https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=418500#50

### Memory leak - error output before fix

Thanks to : http://sourceforge.net/p/pam-mysql/bugs/27/#c2aa

``` sh
Can t initialize threads: error 11
AUTH-PAM: BACKGROUND: user 'xxx' failed to authenticate: Permission denied
```
