# windows-container-but-useful
The actually useful Windows 10 Container


This is the repo for a Docker container made by myself and Darren Fraser-Green (git.darren.lol) which is the base Windows 10 container by `mcr.microsoft.com/windows:1909`, only, its actually useful.

The container isn't recomended for production out of the box, but that's for you to figure out.

What's includes:

- Win32-OpenSSH by default.  Empty Password and PubKey Authentication enabled.
     - `git-bash` is the default OpenSSH shell/
- Scoop with `extras` and `java` buckets
- Chocolatey
- `git`
- `wget`
- `which`
- `curl`
- `sudo`
- `nano`
- `vim`
- `unzip`
- `unrar`
- `7zip`
- `dos2unix`
- `grep`
- `findutils`
