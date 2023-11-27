# Winter-thinkphp

```sh
echo "
	deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy main restricted universe multiverse
	deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
	deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
	deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
" > /etc/apt/sources.list

export DEBIAN_FRONTEND=noninteractive

apt update -y

composer -n -V > /dev/null 2>&1 || apt install -y composer

composer -n config -g repos.packagist composer https://mirrors.cloud.tencent.com/composer/

composer -n global update

if [ ! -d ~/Winter-thinkphp ]; then cd ~/ ; git clone https://github.com/AndyInAi/Winter-thinkphp.git; fi

cd ~/Winter-thinkphp

php think run -p 8080

# starting HTTP server at http://0.0.0.0:8080
```
