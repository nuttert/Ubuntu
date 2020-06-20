# Ubuntu

```
apt-get -y install sudo vim npm python3-pip docker docker.io &&
pip3 install flask flask_cors freeport
```
Новая Ubuntu на докере с красивым терминалом:
```
docker run -e LANG=C.UTF-8 -e LC_ALL=C.UTF-8 -e TERM=$TERM -it --rm ubuntu bash -uexc '
  apt update && apt install -y git curl zsh autojump && cd /root
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" --skip-chsh --unattended
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
  curl -fsSLO http://bit.ly/Spaceship10kTheme
  echo "source ~/Spaceship10kTheme" >~/.zshrc
  exec zsh'
  ```
