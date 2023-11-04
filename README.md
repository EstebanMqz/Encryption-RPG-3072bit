<div align="center"><h1><b>GPG RSA Encryption</h1></div></b>

---

<div align="right">

[<img width="25px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Logo_windows_simples.svg/2280px-Logo_windows_simples.svg.png?f=webp">](https://www.microsoft.com/en-us/windows/) &nbsp; [![GPG Encryption](https://img.shields.io/badge/GPG_Encryption-0093D6?style=flat&amp;logo=gnu-privacy-guard&amp;logoColor=white)](https://www.gnupg.org/)

</div>

There are plenty of time consuming encryption programs, nevertheless git provides most of the best encryptions right from your terminal. <br>
This is due to the fact of git file(s) processing efficiency as you already know. <br>

<i>(Optional:)</i> A file anyone must be wanting to encrypt if using Windows OS might be the .crd: <br>

``` cmd
rem Back Up @ PATH
rundll32.exe keymgr.dll,KRShowKeyMgr %USERNAME%.crd 
rem Read saved .crd
rundll32.exe keymgr.dll,KRShowKeyMgr PATH.crd
rem Encrypt.crd...
```

<br><br>

<div align="center">
    <span style="font-size: 18px;">
    
<b>1026-4096 bits </b><i>(low &rarr; high)</i> GPG encryption: <br><br>
</div>
    </span>

1. <b>Create</b> Git <i>built-in</i> Encryption:

``` bash
gpg --version #GPG Installation
gpg --gen-key # Create GPG key with default options.
gpg --full-generate-key # Create GPG key with advanced options.
gpg --list-keys # Retrieve GPG (Confirm).  
```
<br>

<i>Advanced / Default</i> options <i><b>Encryption key</i></b> user prompt (among others): <br>

+ `<Name>`
+ `<Email>`
+ `<Passphrase>`

<br>

+ <i>(Optional:)</i> Key(s) deletion: <br><br>

    ``` bash
    gpg --delete-keys #Delete public keys.
    gpg --delete-secret-keys #Delete secret keys.
    ```

</i>
<br>

2. Add Encryption key to Environment <b>PATH</b> for further use:

``` bash
which gpg # Obtain key PATH.
export PATH=$PATH:/usr/bin/ && echo $PATH # Export GPG keys to System Env & confirm.   
```

<br>

3. <b>GPG file(s) Encryption</b> with key:

``` bash
gpg --encrypt --recipient <Email> <path/filename>
git rm <filename> -f #Delete unencrypted file to backup on cloud (Check local/remote .git).
```

<br>

+ <i>(Optional:)</i> &#9729;<i> Encrypted files Cloud back-up: <br><br>

    ``` bash
    gpg --decrypt Key.crd.gpg > Key.crd
    rundll32.exe keymgr.dll,KRShowKeyMgr PATH.crd (Optional) 
    ```
    
</i>
<br>

###### References:

<font size="2">

+ [Credential Manager](https://github.com/microsoft/Git-Credential-Manager-for-Windows)<br>
+ [Git .crd](https://github.com/microsoft/Git-Credential-Manager-for-Windows)<br>
+ [GPG](https://www.gnupg.org)<br>
</font>


