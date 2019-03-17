
### Local computer 

`ssh-keygen -t rsa -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]`
I don't add the username. And restrict the private key so that it cannot be modified. 
```
ssh-keygen -t rsa -f ~/.ssh/w261 
chmod 400 ~/.ssh/w261
```

### Google Cloud 


