<div align="center"><h2><b>3072-bit RSA public GPG Encryption keys</h2></div></b>

---
<div align="left">

[![GPG Encryption](https://img.shields.io/badge/GPG_Encryption-0093D6?style=flat&logo=gnu-privacy-guard&logoColor=white)](https://www.gnupg.org)

</div>

There are plenty of time consuming encryption programs, nevertheless git provides most of the best encryptions right from your terminal. <br>
This is due to the fact of git file(s) processing efficiency as you already know. <br>

Steps to create a 3072-bit (high) encryption: <br><br>

1. Create encryption GPG key

``` bash
gpg --gen-key
```
<br>

<i>Prompted to create an <b>encryption key:</b></i><br>
+ `<Name>`
+ `<Email>`
+ `<Passphrase>`

<br>

2. Encrypt files with personal GPG key:

``` bash
gpg --encrypt --recipient <Email> " <path/filename> "
git rm <filename> #keep filename.gpg 
```
<br>
3. Add encryption key to Environment PATH to use it further:

``` bash
gpg --list-keys # Retrieve GPG 
which gpg # Obtain PATH
export PATH=$PATH:/usr/bin & echo $PATH # Export GPG keys to System Env & confirm.   
```