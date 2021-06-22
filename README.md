# Usage

```bash
curl -SsL https://akamai.github.io/akr-pkg/debian/KEY.gpg | sudo apt-key add -
sudo curl -SsL -o /etc/apt/sources.list.d/akr.list https://akamai.github.io/akr-pkg/debian/akr.list
sudo apt update
sudo apt install kr
```

