# wordpress-on-docker
docker-compose files for wordpress on docker

The original contents is [karelie](https://www.karelie.net/free-fast-wordpress-site/).
I added own updates to this contents & put it here.  
I hope this will help.


## memo
```
free -m
sudo dd if=/dev/zero of=/swapfile bs=1M count=1024
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
sudo sed -i '$ a /swapfile                                 swap                    swap    defaults        0 0' /etc/fstab
sudo reboot
```
```
free -m
```
```
sudo apt-get update
sudo apt install -y \
     apt-transport-https \
     ca-certificates \
     curl \
     software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
     "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
     $(lsb_release -cs) \
     stable"
sudo apt-get update
sudo apt install -y docker-ce

sudo systemctl status docker
sudo systemctl enable docker

```
```
export compose='1.24.0'
sudo curl -L https://github.com/docker/compose/releases/download/${compose}/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```


