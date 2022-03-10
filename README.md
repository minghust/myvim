# vim-git
use pathogen to manage vim bundles

## prepare
```bash
cd ~
git clone https://github.com/minghust/myvim.git ~/.vim
cd .vim
```
    
## install bundel
```bash
git submodule add <bundel_git_addr> bundle/<bundel_name>
e.g. git submodule add git://github.com/tpope/vim-pathogen.git bundle/vim-pathogen
```

## update bundel
```bash
cd ~/.vim/bundel/<bundel_name>/
git checkout master
git pull
~~~~~~~~~~~~
    **or**    
~~~~~~~~~~~~
git submodule foreach 'git checkout master && git pull'
```

## remove bundel
```bash
rm -rf bundle/<bundel_name>
git rm -r bundle/<bundel_name>
```

## push to origin
```bash
git add; git commit; git push
```

## sync from remote to local
```bash
cd ~/.vim
git submodule init
git submodule update
```
