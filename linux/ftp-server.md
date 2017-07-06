
# Ftp Server

## Install

install `vsftpd` and `xinetd`
```
    sudo apt-get install vsftpd
    sudo apt-get install xinetd
    sudo service vsftpd start
```

## Configure
create `/etc/xinetd.d/vsftpd` file, and put config inside
```
service ftp
{
        disable                 = no
        socket_type             = stream
        wait                    = no
        user                    = root
        server                  = /usr/sbin/vsftpd
        per_source              = 5
        instances               = 200
        no_access               = 10.1.1.10
        banner_fail             = /etc/vsftpd.busy
        log_on_success          += PID HOST DURATION
        log_on_failure          += HOST
}
```

in the file `/etc/vsftpd.conf`, change config,
```
    listen=NO
    write_enable=YES
    #anonymous_enable=YES
```


stop `vsftpd` and restart `xinetd`, and test it
```
sudo service vsftpd stop
sudo service xinetd restart
netstat -ant | grep 21
```

config ftp file location
```
sudo mkdir /home/sammy/ftp/files
sudo chown sammy:sammy /home/sammy/ftp/files
```


## Reference
https://www.digitalocean.com/community/tutorials/how-to-set-up-vsftpd-for-a-user-s-directory-on-ubuntu-16-04#step-3-—-preparing-the-user-directory