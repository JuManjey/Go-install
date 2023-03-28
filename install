sudo apt update && sudo apt upgrade -y
sudo apt install make clang pkg-config libssl-dev libclang-dev build-essential git curl ntp jq llvm tmux htop screen unzip cmake -y
cd /usr/src
sudo rm -Rf go*
sudo wget https://go.dev/dl/`curl -s https://go.dev/dl/?mode=json | jq -r '.[0].version'`.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go*.linux-amd64.tar.gz
cat <<EOF >> ~/.bash_profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF
source ~/.bash_profile
go version
sudo rm -rf /usr/src/go*.linux-amd64.tar.gz
cd ~
