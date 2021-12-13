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
echo 'source /usr/local/Cellar/zsh-syntax-highlighting/0.7.1/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc

# 2. 第二种方式
# git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

- 语法糖提示插件
```bash
# 1. 第一种方式
brew install zsh-autosuggestions
# 根据实际情况执行以下命令
echo 'source /usr/local/Cellar/zsh-autosuggestions/0.7.0/share/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc

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

- 安装npm切换源
```bash
brew install npm
# 多源切换命令安装
npm install -g nrm
# 查看当前可用源
nrm ls
# 使用淘宝源
nrm use taobao
```

- 安装yarn切换源
```bash
npm install -g yrm
# 多源切换命令安装
yrm ls
# 使用淘宝源
yrm use taobao
```

- 安装pip切换源
```bash
pip install pqi
# 查看当前可用源
pqi ls
# 使用淘宝源
pqi use aliyun
```

- 生成ssh key
```bash
# 生成ssh钥匙
ssh-keygen
# github使用ssh key公钥
xxx.pub
```

- 安装pip
```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py   # 下载安装脚本
# 一般情况 pip 对应的是 Python 2.7，pip3 对应的是 Python 3.x
sudo python get-pip.py    # 运行安装脚本
sudo python3 get-pip.py    # 运行安装脚本。
alias pip=/usr/bin/pip3
```
- 安装python虚拟环境
```bash
#虚拟环境搭建
brew install virtualenv # 正常情况下，该扩展包已满足使用
brew install virtualenvwrapper

# 找到相应目录路径进行操作
vim ~/.zshrc
# 在最后一行中补充
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source /usr/local/Cellar/virtualenvwrapper/4.8.4_1/bin/virtualenvwrapper.sh
```

- iterm 配置导出&迁移
```bash
iTerm -> Preferences -> Profiles -> Other Actions
# Copy Profile as JSON （复制选中的当前配置）
```

