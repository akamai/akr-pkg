# akr
deb/rpm repository for [akr](https://github.com/akamai/akr)

The signing key is published at https://akamai.github.io/akr-pkg/KEY.gpg.

## Ubuntu

Supported: 22.04, 24.04, 26.04. Replace `<VERSION>` with `22`, `24`, or `26`.

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -SsL https://akamai.github.io/akr-pkg/KEY.gpg \
  | sudo gpg --dearmor -o /etc/apt/keyrings/akr.gpg
echo "deb [signed-by=/etc/apt/keyrings/akr.gpg] https://akamai.github.io/akr-pkg/ubuntu/<VERSION> ./" \
  | sudo tee /etc/apt/sources.list.d/akr.list
sudo apt update
sudo apt install akr
```

## RHEL / Rocky Linux

Supported: 8, 9, 10. Replace `<VERSION>` with `8`, `9`, or `10`.

```bash
sudo tee /etc/yum.repos.d/akr.repo <<'EOF'
[akr]
name=akr repository
baseurl=https://akamai.github.io/akr-pkg/rhel/<VERSION>/
gpgcheck=1
gpgkey=https://akamai.github.io/akr-pkg/KEY.gpg
enabled=1
EOF
sudo yum -y install akr
```

## CentOS Stream

Supported: 9, 10. Replace `<VERSION>` with `9` or `10`.

```bash
sudo tee /etc/yum.repos.d/akr.repo <<'EOF'
[akr]
name=akr repository
baseurl=https://akamai.github.io/akr-pkg/centos/<VERSION>/
gpgcheck=1
gpgkey=https://akamai.github.io/akr-pkg/KEY.gpg
enabled=1
EOF
sudo yum -y install akr
```
