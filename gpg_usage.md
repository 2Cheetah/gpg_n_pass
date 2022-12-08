# GPG

## Installing GPG & keys generation

- Installing GPG
```
sudo pacman -S gpg
```
- Creating gpg keys
```
gpg --full-gen-key
```
- Checking created keys
  - Public keys
  ```
  gpg -k
  gpg --list-keys
  ```
  - Secret keys
  ```
  gpg -K
  gpg --list-secret-keys
  ```
- Removing keys
  - Removing secret keys
  ```
  gpg --delete-secret-key <KEY-ID>
  ```
  - Removing public keys
  ```
  gpg --delete-key <KEY-ID>
  ```

## Encrypting and decrypting files

- Encrypt file (\-e encrypt, \-a ASCII format, \-r gpg key to use) 
```
gpg -e -a -r <KEY_ID or EMAIL> <FILE_TO_ENCRYPT>
```
- Decrypt file (\-d decrypt, \-o output file)
```
gpg -d -o <DECRYPTED_FILENAME> <FILE_TO_DECRYPT>
```

## Exporting GPG keys

\-a ASCII
```
gpg --export -a <KEY_ID or EMAIL> > public.gpg
gpg --export-secret-key -a <KEY_ID or EMAIL> > secret.gpg
```

## Importing GPG keys

```
gpg --import public.gpg
gpg --import secret.gpg
```

## Regular workflow
1. Install GPG
2. Create GPG keys
3. Export GPG keys to cloud based vault
4. Delete local GPG keys

