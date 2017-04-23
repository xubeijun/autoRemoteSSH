# autoRemoteSSH
This bash script help you auto connect to remote SSH server through  your springboard VPN server.

### step 1.
Please scp your rsa files to your springboard VPN server.
eg.
```linux
# scp folder
scp -r local_folder remote_username@remote_ip:remote_folder 

# scp file
scp local_file remote_username@remote_ip:remote_folder
```

### step 2.
Please config the param which is marked as **"need_you_config"**.
```linux
vim ./ssh/autoRemoteSSH
```

Make sure this file have the excute permission.
```
chmod -R 744 ./ssh/autoRemoteSSH
```

Your can see the **./example/autoRemoteSSH**, and see these params which is marked as **"need_you_config"**.

1.  vpnPath
1.  vpnKey
1.  vpnIP
1.  vpnUser
1.  vpnPort
1.  remotePath
1.  helpMsg
1.  abbreviation mapping list

### step 3. 
Add this SSH command to your local machine configuration file
```linux
vim ~/.bash_profile
```

 
### step 4.
copy code to bash_profile file
Please replace the **yourSSHscriptPath** to your real script path
```bash
function ssh_remote(){
   /{yourSSHscriptPath}/autoRemoteSSH.sh $@
}
```

### step 5.
Restart your local machine configuration file
```linux
source ~/.bash_profile
```

### step 6.
Get the help message in your terminal
```linux
ssh_remote --help
```

### awesome!
You can enter the sort code to remote SSH server!
eg.
```
ssh_remote 111
```
