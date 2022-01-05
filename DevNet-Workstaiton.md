```bash
DEVNET Workstation
# https://developer.cisco.com/learning/lab/containers-dev-ubuntu/step/7
# Create gmail account for devel and sso to postman etc
# Instal ubuntu
# Enable ssh and xrdp
#Install devel packages and postman
apt install curl libssl-dev build-essential git 
apt python3 python3-pip python3-virtualenv
apt install python3.8-venv
snap install postman

apt install nodejs npm
nodejs -v

#Setup git
git --version
cd ~/Desktop
mkdir dev
cd dev
git clone https://github.com/CiscoDevNet/hello_network
cd hello_network
 ./hello_network.sh


git config --global user.name "pithei"
git config --global user.email "rwx2dev@gmail.com"
git config --global credential.helper store
# Verify git settings
# Remote token, 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
git config --list
git config user.name
git status
git log 

# initialize remote git repo
cd ~/Desktop/dev/
git clone https://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@github.com/pithei/py100.git
git remote add origin https://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@github.com/pithei/py100.git


# initiaize local repo?
# some notes
# git remote set-url origin https://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@github.com/pithei/py100.git
# git push https://<GITHUB_ACCESS_TOKEN>@github.com/<GITHUB_USERNAME>/<REPOSITORY_NAME>.git
# git push https://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@github.com/pithei/snippet.git
# git push origin master
# $ git checkout main
# $ git pull origin main
#### Git branches
git branch
git branch test_br
git checkout test_br
git branch


## or
git checkout -b test_br
git branch

git branch -d test_br

# Merging branches
git merge lincoln

# Statshing changes, 
git stash
git stash pop

# install git bash for windows

# fake rest api
jsonplaceholder.typicode.com
curl https://jsonplaceholder.typicode.com/posts/3
curl -i https://jsonplaceholder.typicode.com/posts/3

curl -I https://jsonplaceholder.typicode.com/posts/3
curl --head https://jsonplaceholder.typicode.com/posts/3

curl -i -o data.txt https://jsonplaceholder.typicode.com/posts/3
## just downloads file
curl -O https://jsonplaceholder.typicode.com/posts/3
curl -O --limit-rate 1000B https://jsonplaceholder.typicode.com/posts/3

curl --data "title=Hello&body=Help World" https://jsonplaceholder.typicode.com/posts
curl -X PUT --data "title=Hello" https://jsonplaceholder.typicode.com/posts/3
curl -X DELETE https://jsonplaceholder.typicode.com/posts/3

curl -u user:passwd <url>

curl http://google.com # Redirects to www.google.com
curl -L http://google.com # follow the redirect

curl -u ftpuser@ftpserver:ftppasswd -T hello.txt ftp://ftp.server.com  # upload file to ftp via curl
curl -u ftpuser@ftpserver:ftppasswd -O ftp://ftp.server.com/hello.txt  # download file from ftp via curl



# Setup python
python3 -V
python3 -m venv py3-venv
source py3-venv/bin/activate
python -V
which python





# Setup postman
git clone https://github.com/taylonr/postman
cd postman
npm install

npm run start:dev
## Create token for request
# Key, value
G-TOKEN, ROM831ESV
localhost:3000/books
# test postman with keys
# Key, Value
title, waste
author, john
localhost:3000/books/search

# Delete, authorizaion admin / admin

### You can download postman results
## create presets in headers tab, with custom headers to load on demand

### environmental variables	{{variable}}

npm run start:test
# curl 'http://localhost:3000/books' \
#   -H 'Connection: keep-alive' \
#   -H 'sec-ch-ua: "Google Chrome";v="95", "Chromium";v="95", ";Not A Brand";v="99"' \
#   -H 'sec-ch-ua-mobile: ?0' \
#   -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/95.0.4638.54 Safari/537.36' \
#   -H 'Content-Type: application/json' \
#   -H 'Accept: */*' \
#   -H 'g-token: ROM831ESV' \
#   -H 'cache-control: no-cache' \
#   -H 'postman-token: 94e03697-36ba-33d0-bf88-eae6aeb4380e' \
#   -H 'sec-ch-ua-platform: "Linux"' \
#   -H 'Origin: http://localhost:3000' \
#   -H 'Sec-Fetch-Site: same-origin' \
#   -H 'Sec-Fetch-Mode: cors' \
#   -H 'Sec-Fetch-Dest: empty' \
#   -H 'Referer: http://localhost:3000/ui' \
#   -H 'Accept-Language: en-US,en;q=0.9' \
#   --data-raw '{"title":"pithei","author":"theman","isbn":"121345","releaseDate":"201"}' \
#   --compressed

## impot query from google chrome devel tools, exported as curl requeust
localhost:3000/ui
# postman proxy, for fuks sake
## postman, code snippets oO

## postman tests

# ngrok

# IDE and editor

# Chrome
sudo nano /etc/apt/sources.list.d/google-chrome.list
deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main


wget https://dl.google.com/linux/linux_signing_key.pub
sudo apt-key add linux_signing_key.pub

sudo apt update
sudo apt install google-chrome-stable

# OpenConnect
sudo apt-get install openconnect
sudo openconnect -b dcloud-rtp-anyconnect.cisco.com

sudo ps -ax | grep openconnect
sudo kill 22741

# Docker, Application container engine
apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo apt install docker-ce
sudo systemctl status docker
sudo usermod -aG docker $USER
### Log out and log back in so that your group membership is re-evaluated.

docker run busybox
docker ps -a


docker run --privileged -it -p 8000:8000 -p 8443:8443 ciscodevnet/vs-code-iox-client:latest
http://127.0.0.1:8443
```
