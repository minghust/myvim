# MyVim
Synchronize my vim everywhere

## Prepare
```bash
git clone https://github.com/minghust/myvim.git ~/.vim
```

## Sync all bundles from remote to local
```bash
cd ~/.vim
git submodule init
git submodule update
```

## Install new bundels
```bash
cd ~/.vim
git submodule add <bundel_git_addr> bundle/<bundel_name> # You can just use `git clone` in ~/.vim/bundle/, but for *sync* reasons, I use submodule that would help
e.g., git submodule add git://github.com/tpope/vim-pathogen.git bundle/vim-pathogen
```

You can use [pathogen](https://github.com/tpope/vim-pathogen) to manage your bundles. It's awsome.

## Update bundel
After adding submodules, we need to update them for installations

- Method 1

```bash
cd ~/.vim
cd bundel/<bundel_name>
git checkout master
git pull
```

- Method 2

```bash
cd ~/.vim
git submodule foreach 'git checkout master && git pull'
```

## Remove bundel
```bash
rm -rf bundle/<bundel_name>
git rm -r bundle/<bundel_name>
```

## Do NOT forget to push updates should any changes are made
```bash
git add .
git commit -m "update"
git push origin master
```
