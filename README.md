# cheatsheet

## First Installs

### Install Curl

```bash
sudo apt install curl
```

### Install Git

```bash
sudo apt install git
```

### Install zsh

```bash
sudo apt install zsh
```
Make zsh default shell : 
```bash
chsh -s $(which zsh)
```
Then `logout` and `login`

### oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Then `logout` and `login`

### Install fonts

In the fonts folder, the 4 Meslog
then
```bash
sudo apt install fonts-firacode
```

then enable Meslog font in terminal.

### Powerlevel10k

#### Installation

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
Then edit .zshrc and add `ZSH_THEME="powerlevel10k/powerlevel10k"`
Then `logout` and `login`

### Configuration

##### Syntax highlighting

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```
activate it by addin the plugin in .zshrc
`plugins=(git ... zsh-syntax-highlighting ...)`


## Install Docker

```bash
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
add Docker's GPG Key: 

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

set up stable repo :
```bash
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

install docker engine :
```bash
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io
```

post install steps : 

create the docker group :
```bash
sudo groupadd docker
```

add current user to group :
```bash
sudo usermod -aG docker $USER
```

## TroubleShoot

> Ubuntu Software is not lauching

Try to uninstall and re install it : 
```bash
sudo snap remove snap-store
sudo snap install snap-store
```

