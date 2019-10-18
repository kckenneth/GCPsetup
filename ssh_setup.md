
### Local computer 

`ssh-keygen -t rsa -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]`  
I don't add the username. And restrict the private key so that it cannot be modified. 
```
ssh-keygen -t rsa -f ~/.ssh/w261 
chmod 400 ~/.ssh/w261
```

We need to copy w261.pub key into Google cloud instance. First we will copy the public key 
```
cd ~/.ssh/
vi w261.pub
```
copy the entire key 

### Google Cloud 

--> Go to compute engine 
--> click the instance 
--> click Edit (You'd see no SSH Keys) 
--> Add the w261.pub key (Note: If you created the ssh keys with the username, it's automatically appear the username, let's call it kchen here)
--> Also enable HTTP, HTTPS as well. 

--> Note the external IP address as well. 

<a href=https://www.youtube.com/watch?v=R8C66NwMJLs>Source</a>

### Testing 
Copying from local to GCP instance 
```
scp -i ~/.ssh/w261 testfile.txt kchen@<GCP-external-IP-address>:/home/kchen/
```





