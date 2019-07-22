# fed_in_box

This image is based on Fedora, it has already installed shellinabox in it which make it easier to access, this image can be used to create a platform where you want to provide multiple container of linux at different ports .

To use this Image:

```docker run -d -p port:4200 fed_in_box```

## Note: Here port is a random generated port number which is free on your system.

This command will launch a container and deattach it and now you can access you container via this link :
https://localhost:port
## Defaults 
Default user is ```Harsh```,
Default password is ```vijay```

If you want to change the default user and password just make a new docker file via using this image and
add these line in the file
 
```RUN sudo  useradd -m -p $(openssl passwd PASSWORD_HERE) USER_HERE```

```RUN sudo echo "USER_HERE   ALL=(ALL)       ALL" >>/etc/sudoers ```

The first line will add a user with username "USER_HERE" and password "PASSWORD_HERE", change theme according to your need
and the second line will add the new user in sudoers file so that new user can also become root user. 

You can skip second line image will work anyways
