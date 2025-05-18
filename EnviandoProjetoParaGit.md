# Principais e básicos comandos Git

```
git init

git status

git add .  ou git add + caminho

git status

git commit -m "first commit"

git branch -M main

git remote add origin + link repo.

git push -u origin main
```

### Caso de erro no link do user:

```
git config --global user.name "Matheus"
git config --global user.email "matheus.nalbuquerque@ufn.edu.br"

```

### Comando para puxar do GitHub arquivos que faltam:

```
git pull origin main --rebase

git push -u origin main

```

### Git add e Git reset

```
git add + caminho (adiciona na lista para enviar para o git)

git reset + caminho (tira ele da lista)

```


### Após ja ter feito o primeiro commit

```
git status

git add .

git commit -m "Mensagem"

git push -u origin main

```
