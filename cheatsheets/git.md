# Git Cheat Sheet

Este cheat sheet traz uma referência rápida para Git com tags essenciais, boas práticas e exemplos práticos.

---

## Configuração Inicial

```bash
# Configuração de Identidade
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"

# Verificar Configurações
git config --list
```

**Explicação Detalhada**:
- Define identidade para commits
- `--global`: Configura para todos projetos
- Essencial para rastrear autoria das modificações

---

## Repositórios

### Criar Repositórios
```bash
# Criar novo repositório local
git init

# Clonar repositório existente
git clone https://github.com/usuario/repositorio.git
```

**O que acontece**:
- `git init`: Inicializa repositório Git na pasta atual
- `git clone`: Baixa repositório completo com histórico

---

## Fluxo Básico de Trabalho

### Estados dos Arquivos
```bash
# Verificar status
git status

# Adicionar arquivo para staged
git add arquivo.txt
git add . # Adiciona todos arquivos

# Commitar mudanças
git commit -m "Mensagem descritiva"

# Commitar pulando staged
git commit -am "Mensagem"
```

**Explicação de Estados**:
- `Untracked`: Arquivo novo, não rastreado
- `Modified`: Arquivo modificado
- `Staged`: Arquivo pronto para commit
- `Committed`: Arquivo salvo no repositório local

---

## Branches

### Operações com Branches
```bash
# Listar branches
git branch

# Criar nova branch
git branch nova-feature

# Mudar de branch
git checkout nova-feature

# Criar e mudar para branch
git checkout -b outra-feature

# Mergear branches
git merge nova-feature

# Deletar branch
git branch -d nova-feature
```

**Detalhamento**:
- Branches são "linhas de desenvolvimento" independentes
- Permite trabalhar em recursos sem afetar branch principal
- `merge`: Combina históricos de branches diferentes

---

## Trabalhando com Remoto

### Sincronização
```bash
# Adicionar repositório remoto
git remote add origin https://github.com/usuario/repo.git

# Enviar commits
git push origin main

# Baixar atualizações
git pull origin main

# Verificar repositórios remotos
git remote -v
```

**O que acontece**:
- `push`: Envia commits locais para repositório remoto
- `pull`: Baixa e mescla commits do repositório remoto
- Mantém repositórios locais e remotos sincronizados

---

## Histórico e Inspeção

### Visualizar Mudanças
```bash
# Ver modificações não commitadas
git diff

# Histórico de commits
git log

# Log resumido
git log --oneline

# Detalhes de um commit específico
git show hash-do-commit
```

**Explicação**:
- `diff`: Mostra alterações não commitadas
- `log`: Exibe histórico completo de commits
- Fundamental para rastrear mudanças

---

## Desfazer Mudanças

### Reverter e Resetar
```bash
# Descartar mudanças locais
git checkout -- arquivo.txt

# Resetar staged
git reset HEAD arquivo.txt

# Reverter último commit
git revert HEAD

# Resetar para commit específico
git reset --hard hash-do-commit
```

**Detalhamento**:
- Permite corrigir erros e voltar estados anteriores
- Diferentes níveis de "desfazer"
- Cuidado com `reset --hard`! Pode perder trabalho

---

## Estratégias Avançadas

### Stash
```bash
# Salvar mudanças temporariamente
git stash

# Aplicar stash salvo
git stash pop
```

**Uso**:
- Guarda mudanças sem commitar
- Útil para trocar de branch rapidamente

## Links Úteis 🌐

### Documentação e Aprendizado
- [Git Oficial](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/pt/repositories)
- [GitLab Docs](https://docs.gitlab.com/ee/topics/git/)
- [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)

### Comunidades
- [Stack Overflow - Git](https://stackoverflow.com/questions/tagged/git)
- [Reddit - Git](https://www.reddit.com/r/git/)

## Boas Práticas

### Dicas Importantes
- Commits pequenos e frequentes
- Mensagens de commit descritivas
- Use branches para novas funcionalidades
- Sempre puxe atualizações antes de trabalhar
- Evite commitar arquivos grandes/binários

## Ferramentas Complementares
- GitHub Desktop
- GitKraken
- SourceTree
- VS Code Git Integration