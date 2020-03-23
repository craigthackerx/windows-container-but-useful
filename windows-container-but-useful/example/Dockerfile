#From my base image - Windows 10 1909 with Scoop and Choco installed
FROM craigtho/windows-container-but-useful:latest

MAINTAINER "craigthackerx@gmail.com"
MAINTAINER "im@darren.lol"

#Use Powershell
SHELL ["powershell", "-Command"]

ADD id_rsa.pub $HOME/.ssh/id_rsa.pub
ADD id_rsa $HOME/.ssh/id_rsa
ADD authorized_keys $HOME/.ssh/authorized_keys

#Never tested, try adding the full ssh directory
ADD .ssh/ $HOME/.ssh
