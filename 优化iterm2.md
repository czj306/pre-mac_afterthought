# 优化iterm2插件


- 安装iterm2软件
```bash
brew install --cask item2
```

- 安装zsh，升级旧zsh
```bash
brew install zsh
# 查看shell命令 cat /etc/shells
# 指定zsh为默认shell
chsh -s /bin/zsh
```

- 高亮提示插件
```bash
# 1. 第一种方式
brew install zsh-syntax-highlighting
# 根据实际情况执行以下命令
# echo 'source /usr/local/Cellar/zsh-syntax-highlighting/0.7.1/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc

# 2. 第二种方式
# git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

- 语法糖提示插件
```bash
# 1. 第一种方式
brew install zsh-autosuggestions
# 根据实际情况执行以下命令
# echo 'source /usr/local/Cellar/zsh-autosuggestions/0.7.0/share/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc

# 2. 第二种方式
# git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

- 目录跳转插件
```bash
brew install autojump
```

- 插件配置使用
```bash
vim ~/.zshrc

# 找到plugins
plugins=(
  git
  # 通过 git clone 的方式需要手动设置
	# autojump
  # zsh-autosuggestions
	# zsh-syntax-highlighting
)
```

- 更换主题
```bash
ZSH_THEME='random'

# 设置显示时间
SPACESHIP_TIME_SHOW="true"

# 设置显示用户名，并改用户名颜色为猛男粉
SPACESHIP_USER_SHOW="always"
SPACESHIP_USER_COLOR="212"
```

- 启用插件
```bash
source ~/.zshrc
```

- 设置iterm2支持滚动
```bash
iterm2 >> preferences >> advanced >> mouse
Scroll wheel down >> set to \k
Scroll wheel down >> set to \j
```

- 安装npm
```bash
brew install npm
# 多源切换命令安装
npm install -g nrm
# 查看当前可用源
nrm ls
# 使用淘宝源
nrm use taobao
```

- 生成ssh key
```bash
ssh-keygen
```