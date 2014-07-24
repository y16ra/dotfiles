dotfiles
========

Macで利用しているドットファイル管理リポジトリ

# homesickでドットファイルを管理する

```
# install homesick
gem install homesick

# ドットファイルをGitHubで管理する準備
mkdir ~/dotfiles && cd ~/dotfiles
git init

mkdir home && cd home
# 管理したいドットファイルを集める
cp ~/.zshrc .
cp ~/.bash_profile .
```
GitHubにPushしたら、
```
homesick clone y16ra/dotfiles
cd ~
homesick symlink dotfiles
```
cloneすると、「~/.homesick/repos/dotfiles」にGitHubから取得したファイルが置かれます。
symlinkコマンドでシンボリックリンクが作成されます。

# ほかのMacでも同じドットファイルを利用する

```
gem install homesick
homesick clone dotfiles

# ほかのMacで変更された内容を取り込む
homesick pull dotfiles
```
