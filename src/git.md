
# 📝 Git Cheat Sheet

## 📦 Configuração Inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --list
```

## 🗃️ Criação e Clonagem de Repositórios

```bash
git init                         # Inicializa um novo repositório
git clone <url-do-repositório>   # Clona um repositório existente
```

## 📂 Status e Logs

```bash
git status                       # Mostra status dos arquivos
git log                          # Mostra histórico de commits
git log --oneline --graph        # Visualização simplificada do histórico
```

## ➕ Adicionar Arquivos

```bash
git add <arquivo>                # Adiciona arquivo específico
git add .                        # Adiciona todas as alterações
```

## ✅ Commit

```bash
git commit -m "Mensagem"         # Realiza commit com mensagem
git commit -am "Mensagem"        # Adiciona e comita arquivos já versionados
```

## 🔄 Sincronização

```bash
git pull                         # Puxa alterações do repositório remoto
git push                         # Envia alterações para o repositório remoto
git push -u origin <branch>      # Seta branch upstream
```

## 🌿 Branches

```bash
git branch                       # Lista branches
git branch <nome-branch>         # Cria nova branch
git checkout <nome-branch>       # Troca de branch
git checkout -b <nome-branch>    # Cria e troca para nova branch
git merge <nome-branch>          # Mescla branch ao atual
git branch -d <nome-branch>      # Deleta branch local
```

## 🛠️ Stash

```bash
git stash                        # Salva alterações temporariamente
git stash pop                    # Aplica e remove o último stash
git stash list                   # Lista stashes
```

## 🗑️ Remover Arquivos

```bash
git rm <arquivo>                 # Remove arquivo do Git e do diretório
git rm --cached <arquivo>        # Remove arquivo do Git, mas mantém no diretório
```

## ⏪ Reverter Alterações

```bash
git checkout -- <arquivo>        # Desfaz alterações locais no arquivo
git reset --hard                 # Desfaz todas as alterações locais
git revert <hash>                # Cria um commit revertendo o commit especificado
```

## 🔍 Comparações e Diferenças

```bash
git diff                         # Mostra diferenças não adicionadas
git diff --staged                # Mostra diferenças adicionadas
```

## 🔗 Remotos

```bash
git remote -v                    # Lista remotos
git remote add origin <url>      # Adiciona um remoto
git remote remove <nome>         # Remove um remoto
```

## 🧹 Limpeza

```bash
git clean -f                     # Remove arquivos não versionados
git clean -fd                    # Remove arquivos e diretórios não versionados
```

## 🛡️ Segurança

```bash
git config --global credential.helper cache       # Cache de credenciais temporário
git config --global credential.helper store       # Armazena credenciais em texto
```

## 🎯 Tags

```bash
git tag                          # Lista tags
git tag <tag>                    # Cria uma nova tag
git push origin <tag>            # Envia tag para remoto
```

---

## 📚 Recursos Úteis

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Cheatsheet Oficial](https://education.github.com/git-cheat-sheet-education.pdf)
- [GitHub Docs](https://docs.github.com/en/get-started/using-git)


[Voltar para HOME](https://github.com/pvstelles/cheat-sheet/blob/main/README.md)
