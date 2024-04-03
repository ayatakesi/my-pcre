# pcre
GNU Emacs30.0.50に含まれる`java/INSTALL`にしたがって取得したpcreモジュール(libselinuxの依存モジュール)のレポジトリ。

# 作成した手順

1. [Google Gitのpcre](https://android.googlesource.com/platform/external/pcre)をclone

```bash
$: git clone https://android.googlesource.com/platform/external/pcre
```

2. `nougat-release`ブランチから修正用ブランチ`my/nougat-release`をcheckout

```bash
$: cd pcre
$: git checkout nougat-release
$: git checkout -b my/nougat-release
```

3. 空レポジトリにpush

```bash
$: git add -A
$: git commit -m 'nanika commit messages...'
$: gh repo create my-pcre --public
$: git remote add mine https://github.com/JIBUN/my-pcre.git
$: git branch -M my/nougat-release
$: git push -u mine my/nougat-release
```
