# Pass paswordstore.org
## Pass installation
```
sudo pacman -S pass
```
Check where the pass program is:
```
which pass
```
## Initialize pass
```
pass init <GPG_KEY_ID or GPG_KEY_EMAIL>
```
It creates dedicated folder `~\.passowrd-store`

## Save password
```
pass insert Email/gmail.com
```
Save multiline information with key \-m
```
pass insert Social/vk -m
```

## Check stored password
```
pass
```
## Get stored password
```
pass Email/gmail.com
```
## Password generation
```
pass generate Email/mail.ru 15
```
Where 15 is the length of the password.
## Remove password
```
pass rm Email/mail.ru
```
