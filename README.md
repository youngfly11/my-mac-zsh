# my-mac-zsh
Mac OS zsh configuration

## Configure Results

### 1.Set brew source 
```
cd "$(brew --repo)"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git

cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git

brew update
```
### 2.Set zsh
- Install iterm2 and open iterm2  
- Install zsh `brew install zsh zsh-completions`
- Install wget `brew install wget`
- Install oh-my-zsh : a tool to manage and configure zsh
`$ wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh`
- Change to zsh: `chsh -h /bin/zsh`
- Close and re-open iterm2 
### 3.Add more tools to zsh
- Change the theme:
    - Open `vi ~/.zshrc`
    - Comment the `ZSH_THEME` and add `ZSH_THEME="ys"`
    I think this theme is suitable for dev.
    - Save and Close
    - `source ~/.zshrc` to use this theme
- Add autosuggestion
    -  `git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
    - Open `.zshrc`, change plugins from `plugins=(git)` to `plugins=(zsh-autosuggestions git)`
    - Save and Close
    - `source ~/.zshrc`
- Add highlight synatx
    - `brew install zsh-syntax-highlighting`
    - Open `.zshrc` and insert `source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`
    - Save and Close
    - `source .zshrc`
