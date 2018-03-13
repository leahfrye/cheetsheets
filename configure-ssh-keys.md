# Configuring SSH Keys
## On a remote server

### Create a key on your local machine:
Run `ssh-keygen` to create a new local key. 
If you used the default filenames, it will create an "id_rsa" and "id_rsa.pub". "id_rsa.pub" is the public key that you want to copy over to your remote server.
Note: If you set a passphrase, you will have to enter the passphrase every time you use the key.

### Copy the key to the local server

`cat ~/.ssh/id_rsa.pub | ssh username@remote_host "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"`

## On Github or Gitlab

### Create a key on your local machine:

Create the key the same way as above. Run `ssh-keygen`.

### Copy the key and paste in Github/Gitlab
Run `cat ~/.ssh/id_rsa.pub`. Copy the entire output to your clipboard, then go to your account settings in Github/Gitlab, create a new key, and paste it in.
