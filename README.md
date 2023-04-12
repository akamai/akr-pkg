# akr
deb/rpm repository for akr

## Debian/Ubuntu

```bash
curl -SsL https://akamai.github.io/akr-pkg/ubuntu/KEY.gpg | sudo apt-key add -
sudo curl -SsL -o /etc/apt/sources.list.d/akr.list https://akamai.github.io/akr-pkg/ubuntu/akr.list
sudo apt update
sudo apt install akr
```

## RHEL/CentOS

Add repository setting

```
$ sudo vim /etc/yum.repos.d/akr.repo
[akr]
name=akr repository
baseurl=https://akamai.github.io/akr-pkg/rpm/
gpgcheck=0
enabled=1

$ sudo yum -y update
$ sudo yum -y install akr
```


## RHEL-9/CentOS-9

Add repository setting

```
$ sudo vim /etc/yum.repos.d/akr.repo
[akr]
name=akr repository
baseurl=https://akamai.github.io/akr-pkg/rpm-9/
gpgcheck=0
enabled=1

$ sudo yum -y update
$ sudo yum -y install akr
