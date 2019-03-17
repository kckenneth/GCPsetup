
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

Go to your instance --> Metadata --> SSH Keys --> paste the copied key into the box and save 

### Testing 
Copying from local to GCP instance 
```
scp -i ~/.ssh/w261 testfile.txt kchen@<GCP-external-IP-address>:/home/kchen/
```





