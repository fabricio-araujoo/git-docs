# Git Docs
Projeto para backup de comandos git, como um lembrete!

## Documentação de Comandos Git

### Configuração Inicial

```sh
# Configurar nome e e-mail globalmente
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

# Verificar configurações
git config --list
```

### Inicialização e Clonagem

```sh
# Inicializar um repositório Git
git init

# Clonar um repositório remoto
git clone <url-do-repo>
```

### Trabalhando com Commits

```sh
# Verificar o status do repositório
git status

# Adicionar arquivos ao staging area
git add <arquivo>  # Adiciona um arquivo específico
git add .          # Adiciona todas as mudanças

# Criar um commit
git commit -m "Mensagem do commit"

# Adicionar e commitar ao mesmo tempo
git commit -am "Mensagem do commit"
```

### Trabalhando com Branches

```sh
# Criar uma nova branch
git branch <nome-da-branch>

# Trocar para outra branch
git checkout <nome-da-branch>

# Criar e mudar para a nova branch diretamente
git switch -c <nome-da-branch>

# Listar branches
git branch

# Excluir uma branch
git branch -d <nome-da-branch>
```

### Sincronização com o Repositório Remoto

```sh
# Verificar os remotos
git remote -v

# Adicionar um remoto
git remote add origin <url-do-repo>

# Enviar alterações para o repositório remoto
git push origin <branch>

# Baixar as alterações do repositório remoto
git pull origin <branch>

# Atualizar o repositório local sem fazer merge automático
git fetch origin
```

### Merge e Rebase

```sh
# Fazer merge de uma branch na branch atual
git merge <nome-da-branch>

# Rebase para reescrever a história do commit
git rebase <branch>
```

### Revertendo Alterações

```sh
# Desfazer mudanças em arquivos não commitados
git checkout -- <arquivo>

# Resetar staging area
git reset HEAD <arquivo>

# Resetar para um commit anterior (mantendo mudanças locais)
git reset --soft <commit-id>

# Resetar completamente para um commit anterior (apagando mudanças locais)
git reset --hard <commit-id>

# Reverter um commit já enviado
git revert <commit-id>
```

### Histórico e Inspeção

```sh
# Ver o histórico de commits
git log --oneline --graph --decorate --all

# Ver diferenças entre commits
git diff
```

### Stash (Salvar e Restaurar Alterações Temporárias)

```sh
# Guardar mudanças temporárias
git stash

# Listar stashes
git stash list

# Restaurar último stash
git stash pop

# Restaurar um stash específico
git stash apply stash@{n}
```

### Submódulos

```sh
# Clonar um repositório com submódulos
git clone --recurse-submodules <url-do-repo>

# Inicializar submódulos
git submodule update --init --recursive
```

### Outros Comandos Úteis

```sh
# Limpar arquivos não rastreados
git clean -fd

# Corrigir último commit sem alterar a mensagem
git commit --amend --no-edit
```
