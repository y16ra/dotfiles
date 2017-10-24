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

# ドットファイルを更新する
設定を追加、変更などしたらcommit、pushします。
```
homesick commit dotfiles
```

コミットコマンドを打つとviの画面が開くのでコミットコメントを記載します。
このときdiffも確認しておく。
コミットができたらpushします。

```
homesick push dotfiles
```

これでGitHubにプッシュされます。

# ほかのMacでも同じドットファイルを利用する

```
$ gem install homesick
$ homesick clone y16ra/dotfiles

# ほかのMacで変更された内容を取り込む
$ homesick pull dotfiles
```
