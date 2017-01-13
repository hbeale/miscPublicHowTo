How to create a user on an Ubuntu server
====================

Overview
---------------------

I use this on Open Stack after creating an instance and logging in as "Ubuntu".

### Create user
    newID=hbeale
    sudo adduser  --disabled-password $newID
### Enable login with ssh key only
    sudo su - $newID
    whoami # expect:  [user]
    pwd # expect: /home/ [user]
    mkdir .ssh
    chmod 700 .ssh
    touch .ssh/authorized_keys
    nano !$
    paste your public key (~/.ssh/id_rsa.pub on the computer you will ssh from) and save the file
    when you're done, type exit to become ubuntu again
### Make user sudo capable
    whoami # should be ubuntu
    sudo usermod -aG sudo $newID
    # per http://askubuntu.com/questions/147241/execute-sudo-without-password
    sudo visudo
    # at the bottom of the file, add
    # [user] ALL=(ALL) NOPASSWD: ALL
### Test login
    # log out
    # ssh [wherever]@[wherever]
    ssh hbeale@10.50.100.111


