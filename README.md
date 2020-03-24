# windows-container-but-useful
The actually useful Windows 10 Container


This is the repo for a Docker container made by myself and Darren Fraser-Green (git.darren.lol) which is the base Windows 10 container by `mcr.microsoft.com/windows:1909`, only, its actually useful. It is more useful than the base Windows 10 Image as it contains several useful packages, 2 package managers and ssh enable by default with a default user.  Default username and password can be found below.

The container isn't recomended for production out of the box, but that's for you to figure out.

What's included:

- Win32-OpenSSH by default.  Empty Password and PubKey Authentication enabled.
- Scoop with `extras` and `java` buckets e.g. `scoop`
- Chocolatey e.g. `choco`
- `7zip`
- `curl`
- `dos2unix`
- `findutils`
- `git`
- `grep`
- `nano`
- `sudo`
- `unrar`
- `unzip`
- `vim`
- `wget`
- `which`

#How to use:
```
Default User:

Username=user
Password=password
```
##Make a Dockerfile and add your own user

```
FROM craigtho/windows-but-useful:latest

RUN net USER myownuser "myownpassword" /ADD ; net localgroup "Administrators" "user" /ADD
```
Then:
```
docker run -it --rm -m=8GB --cpus=4 -p 1222:22/tcp craigtho/windows-container-but-useful:latest
```
 And then:

 ```ssh -p 1222 myownuser@127.0.0.1```

#Use Docker-compose.yml

```
#This will build the Dockerfile inside the `main` folder of the repo by default.

docker-compose up
```

And then:

```ssh -p 1222 user@127.0.0.1```

See the example folder on GitHub for Pointers.
