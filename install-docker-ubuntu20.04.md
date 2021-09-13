#Install docker
```shell
$ sudo apt update
```
```shell
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
```shell
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```shell
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```
```shell
$ sudo apt update
```
```shell
$ apt-cache policy docker-ce
```
```shell
$ sudo apt install docker-ce
```
```shell
$ sudo systemctl status docker
```

#Permission
```shell
$ sudo usermod -aG docker ${USER}
```
```shell
$ su - ${USER}
```
```shell
$ id -nG
```
```shell
$ sudo usermod -aG docker username
```
