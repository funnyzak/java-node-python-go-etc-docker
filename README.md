# java-node-python-go-etc docker

[![Docker Stars](https://img.shields.io/docker/stars/funnyzak/java-node-python-go-etc.svg?style=flat-square)](https://hub.docker.com/r/funnyzak/java-node-python-go-etc/)
[![Docker Pulls](https://img.shields.io/docker/pulls/funnyzak/java-node-python-go-etc.svg?style=flat-square)](https://hub.docker.com/r/funnyzak/java-node-python-go-etc/)
[![Image Size](https://img.shields.io/docker/image-size/funnyzak/java-node-python-go-etc)](https://hub.docker.com/r/funnyzak/java-node-python-go-etc/)

[Docker hub image: funnyzak/java-node-python-go-etc](https://hub.docker.com/r/funnyzak/java-node-python-go-etc)

Docker Pull Command: `docker pull funnyzak/java-node-python-go-etc`

---

## Environment

### Main Modules
* java 1.8
* go 1.16.7
* python 3.6.8
* nodejs 10.24.0
* npm 8.1.4
* yarn 1.22.17
* mvn 3.3.9
* nginx 1.14
* ossutil64
* openssh 8.1
* zip 3.0
* unzip 6.0
* tar 1.32
* wget 1.20.3
* curl 7.66
* rsync 3.1.3
* git 2.22
* bash 5.0.0
* gzip 1.10
* bzip2 10.06
* webhook [Help](https://github.com/adnanh/webhook)


---

## Docker Run

### Nginx Run

```Docker
docker run -d -t -i --name jnpge --restart always --privileged=true \
-p 81:80 funnyzak/java-node-python-go-etc nginx -g 'daemon off;'
```

### Install Modules

```bash
# mysql 
docker exec jnpge yum install mysql.x86_64

# install node
# n latest
# n 10.23.1
# n 12.22.7
# n 14.18.2
# n 16.13.1
docker exec jnpge n latest
```

### Set Modeules

```bash
# ossutil64 set
ossutil64 config -e ${ALIYUN_OSS_ENDPOINT} -i ${ALIYUN_OSS_AK_ID} -k ${ALIYUN_OSS_AK_SID} -L CH

# osutils64 sync
ossutil64 sync -f /app/package/  oss://bucket-name/app/package/
```