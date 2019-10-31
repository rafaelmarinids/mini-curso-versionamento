# Minicurso Versionamento
Repositório para demonstração de práticas realizadas durante o minicurso.

# Comandos apresentados durante o minicurso
Criar e configurar um repositório
```
git init
git config --global user.name "Rafael Marini"
git config --global user.email "emsouza@unaerp.br"
```
Adicionar ao stage e realizar o commit
```
echo "Meu primeiro arquivo" > arquivo-1.txt
git status
git add .
git commit -m "Commit inicial do projeto"
git log --oneline
```
Criar um branch e visualizar commits herdados
```
git checkout -b branch-2 ou git branch branch-2 58cffab (cria um branch a partir de um commit)
git branch (visualiza a lista de branches)
git log --oneline (visualize os commits herdados do master)
```
Realizar o merge
```
git checkout master
git merge branch-2
git branch -d nome-do-branch
```
Resolver conflitos durante o merge
```
git mergetool
```
Desfazendo modificações em arquivos
```
git reset HEAD arquivo-1.txt (remove do stage)
git checkout -- arquivo-1.txt
git checkout .
```
Reverter commits
```
git reset --soft HEAD~1 (mantém o diretório de trabalho e o stage intactos)
git reset --hard HEAD~1 
git revert 58cffab (remove as alterações do commit especificado e realiza um novo commit)
```
Configurar e enviar para o repositório remoto
```
git remote add origin https://github.com/rafaelmarinids/mini-curso-versionamento.git
git push -u origin master
git push origin nome_da_branch (envia o branch para o repositório remoto)
git push --all origin
```
Criar tag
```
git tag (lista as tags disponíveis)
git tag -a v1.0.0 -m "Minha primeira versão"
git show v1.0.0 (informações da tag)
git push origin v0.0.1 (envia a tag para o repositório remoto)
git push origin --tags
git push origin --delete v1.0.0 (deleta a tag do repositório remoto)
```
Analisar arquivos e branchs
```
git blame arquivo-1.txt
git log --all --decorate --oneline --graph
```
Armazenar temporariamente alterações
```
git stash
git stash list
git stash pop stash@{0}
git stash drop stash@{0}
git stash show -p stash@{0}
```
Reescrever mensagem de commit
```
git commit --amend
```
Rebase
```
git checkout meu-branch
git rebase master
```
Ignorando arquivos e mantendo pastas
```
.gitignore
.gitkeep
```
