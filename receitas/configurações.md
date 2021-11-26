# Passo a passo para usar o GitHub

## Configuração inicial
 - Necessário criar chaves SHA1 (reveja as aulas)
 
 # Histórico  das configurações do GitHub
 
 
SUP08@SUP04 MINGW64 /c/workspace
$ mkdir livro-de-receitas

SUP08@SUP04 MINGW64 /c/workspace
$ cd livro-de-receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas
$ git init
Initialized empty Git repository in C:/workspace/livro-de-receitas/.git/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls -a
./  ../  .git/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --global user.email "jemerson.soares@hotmail.com"

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --global user.name Perkles

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add *

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "commit incial"
[master (root-commit) a26abed] commit incial
 1 file changed, 16 insertions(+)
 create mode 100644 suco.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
suco.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ mkdir receitas

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
receitas/  suco.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ mv suco.md ./receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ cd receitas

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas/receitas (master)
$ ls
suco.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas/receitas (master)
$ cd ..

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    suco.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        receitas/

no changes added to commit (use "git add" and/or "git commit -a")

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add suco.md receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    suco.md -> receitas/suco.md


SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "cria pasta receitas,movoe arquivo para receitas"
[master 99d585d] cria pasta receitas,movoe arquivo para receitas
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename suco.md => receitas/suco.md (100%)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ echo > README.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
README.md  receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status README.md
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add *
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
README.md  receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md


SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "adiciona index"
[master 9f6e836] adiciona index
 1 file changed, 5 insertions(+)
 create mode 100644 README.md

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=jemerson.soares@hotmail.com
user.name=Perkles
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config -- global --unset user.name
error: key does not contain a section: global

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --global --unset user.name

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=jemerson.soares@hotmail.com
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --global user.name "jemersonsoares"

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=jemerson.soares@hotmail.com
user.name=jemersonsoares
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ ls
README.md  receitas/

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git remote add origin https://github.com/jemersonsoares/livro-de-receitas.git

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git remote -v
origin  https://github.com/jemersonsoares/livro-de-receitas.git (fetch)
origin  https://github.com/jemersonsoares/livro-de-receitas.git (push)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git push origin master
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 918 bytes | 459.00 KiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jemersonsoares/livro-de-receitas.git
 * [new branch]      master -> master

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   receitas/suco.md

no changes added to commit (use "git add" and/or "git commit -a")

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add *

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   receitas/suco.md


SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "correcao do titulo contendo o nome da receita"
[master f9eb38f] correcao do titulo contendo o nome da receita
 1 file changed, 1 insertion(+), 1 deletion(-)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git push origin master
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 373 bytes | 373.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jemersonsoares/livro-de-receitas.git
   9f6e836..f9eb38f  master -> master

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   receitas/suco.md

no changes added to commit (use "git add" and/or "git commit -a")

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add *

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   receitas/suco.md


SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "Correção da receita"
[master bf25074] Correção da receita
 1 file changed, 5 insertions(+), 3 deletions(-)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git push origin master
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 540 bytes | 540.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jemersonsoares/livro-de-receitas.git
   f9eb38f..bf25074  master -> master

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        "receitas/configura\303\247\303\265es.md"

nothing added to commit but untracked files present (use "git add" to track)

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git add *

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   "receitas/configura\303\247\303\265es.md"


SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git commit -m "Adição do passo a passo para usar o Github"
[master aed471d] Adição do passo a passo para usar o Github
 1 file changed, 8 insertions(+)
 create mode 100644 "receitas/configura\303\247\303\265es.md"

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 506 bytes | 506.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jemersonsoares/livro-de-receitas.git
   bf25074..aed471d  master -> master

SUP08@SUP04 MINGW64 /c/workspace/livro-de-receitas (master)
$

	

	
