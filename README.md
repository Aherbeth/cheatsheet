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

### COnfiguration

##### Syntax highlighting

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```
activate it by addin the plugin in .zshrc
`plugins=(git ... zsh-syntax-highlighting ...)`



## TroubleShoot

> Ubuntu Software is not lauching

Try to uninstall and re install it : 
```bash
sudo snap remove snap-store
sudo snap install snap-store
```

