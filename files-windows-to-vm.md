# Send files/folders from Windows to SSH VM and vice versa 
### How will you send a file or folder from your host machine to VM and vice versa?

Imagine you did SSH to your VM and is opened in your terminal. You want to send a file/folder from your host machine to this VM. For this, there comes handy a great protocol 'SCP' which is there in windows PC by default.

### From Host to VM:
```sh
scp -i 'path\to\key_pair.pem' 'Your\local\directory' VMuser@ipaddress:path/to/remote/folder
```
### From VM to Host:
```sh
scp -i '\path\to\key_pair.pem' -r VMuser@ipaddress:path/to/remote/folder 'Your\local\directory' 
```
Here
* -i is for path to the key pair, which you used to ssh to your VM.

* -r is used only when you have to send files/folders from VM to your host windows machine.
