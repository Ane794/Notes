# ZSH

## Oh My Zsh

### 安裝

```sh
# 通過 curl 安裝.
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 通過 wget 安裝.
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

### 主題

- [`powerlevel10k`]

  ```sh
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
  ```

### 插件

- [`zsh-autosuggestions`]

  ```sh
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```

- [`zsh-syntax-highlighting`]

  ```sh
  git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```

[`powerlevel10k`]: https://github.com/romkatv/powerlevel10k
[`zsh-autosuggestions`]: https://github.com/zsh-users/zsh-autosuggestions
[`zsh-syntax-highlighting`]: https://github.com/zsh-users/zsh-syntax-highlighting
