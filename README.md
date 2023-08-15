# zsh
# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="$HOME/.oh-my-zsh"

# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="agnoster"

# Add wisely, as too many plugins slow down shell startup.
plugins=(
        git
        zsh-syntax-highlighting
        zsh-autosuggestions

)

source $ZSH/oh-my-zsh.sh

# User configuration
alias python=/usr/bin/python3
source /usr/share/colcon_cd/function/colcon_cd.sh
source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.zsh
source ~/ros2_humble/install/setup.zsh

export APOLLO_HOME=/opt/build_tools/rootfs/x86/apollo/bin
#source $APOLLO_HOME/setup.bash
export BAGBLENDER_HOME=~/bagblender
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$BAGBLENDER_HOME/lib
export PATH=$BAGBLENDER_HOME:$PATH:$APOLLO_HOME
