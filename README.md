# GitGitHub
Comandos básicos Git/GitHub


```git
git init
git status
git add .
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <link do repo>
git push -u origin main
```

# Convenções de Git e Fluxo de Trabalho

### 1. Mensagens de Commit (Conventional Commits)
**Formato:** `tipo: descrição curta em letras minúsculas`

| Tipo | Nome | Quando usar? | Exemplo |
| :--- | :--- | :--- | :--- |
| **feat** | Feature | Nova funcionalidade para o usuário. | `feat: adiciona filtro de especialidades` |
| **fix** | Bug Fix | Correção de um erro ou bug. | `fix: resolve erro no cálculo de data` |
| **docs** | Documentation | Alterações apenas em documentações (Ex: README). | `docs: detalha configuração do banco` |
| **style** | Style | Formatação, espaços, linting (sem mudar lógica). | `style: ajusta indentação nos modelos` |
| **refactor**| Refactor | Mudança que melhora o código sem alterar lógica. | `refactor: simplifica lógica de permissões` |
| **test** | Test | Adição ou alteração de testes. | `test: cria testes para a API de pacientes` |
| **chore** | Chore | Mudanças em ferramentas, build ou dependências. | `chore: atualiza Django para versão 5.0` |

---

### 2. Nomes de Branches (Git Flow)
**Formato:** `prefixo/nome-da-tarefa`

| Prefixo | Nome | Objetivo | Exemplo |
| :--- | :--- | :--- | :--- |
| **feature/** | Feature Branch | Desenvolvimento de uma nova funcionalidade. | `feature/dashboard-estatisticas` |
| **bugfix/** | Bugfix Branch | Correção de bugs encontrados em desenvolvimento. | `bugfix/ajuste-token-auth` |
| **hotfix/** | Hotfix Branch | Correção urgente em ambiente de produção. | `hotfix/vazamento-de-memoria` |
| **docs/** | Documentation | Branches exclusivas para escrita técnica. | `docs/guia-de-api` |
| **refactor/**| Refactor Branch | Organização ou melhoria de código existente. | `refactor/limpeza-de-views` |


# Comandos Git (Essenciais e Avançados)

### 1. Configuração e Início
| Comando | Descrição |
| :--- | :--- |
| `git config --global user.name "Seu Nome"` | Configura seu nome para os commits. |
| `git config --global user.email "seu@email.com"` | Configura seu e-mail para os commits. |
| `git init` | Inicializa um novo repositório local. |
| `git clone <url>` | Clona um repositório existente para sua máquina. |

### 2. O Ciclo de Alterações (Staging & Commit)
| Comando | Descrição |
| :--- | :--- |
| `git status` | Lista arquivos alterados, deletados ou novos. |
| `git add .` | Adiciona todas as mudanças para a área de preparação. |
| `git add <arquivo>` | Adiciona um arquivo específico. |
| `git commit -m "mensagem"` | Salva as alterações com uma descrição. |
| `git commit --amend` | Edita a mensagem do último commit (antes do push). |

### 3. Gestão de Branches (Ramificações)
| Comando | Descrição |
| :--- | :--- |
| `git branch` | Lista todas as branches locais. |
| `git checkout -b <nome>` | Cria uma nova branch e já muda para ela. |
| `git checkout <nome>` | Alterna para uma branch existente. |
| `git branch -d <nome>` | Deleta uma branch local (após o merge). |
| `git merge <nome>` | Une a branch especificada à branch atual. |

### 4. Sincronização com Servidor (GitHub/GitLab)
| Comando | Descrição |
| :--- | :--- |
| `git remote add origin <url>` | Vincula seu repositório local ao servidor. |
| `git push origin <branch>` | Envia seus commits locais para o servidor. |
| `git pull origin <branch>` | Baixa as novidades do servidor e as mescla ao seu código. |
| `git fetch` | Baixa as novidades do servidor, mas **não** as mescla (seguro para ver mudanças). |
| `git remote -v` | Lista os endereços remotos conectados. |

### 5. Histórico e Diferenças
| Comando | Descrição |
| :--- | :--- |
| `git log` | Mostra o histórico de commits. |
| `git log --oneline` | Mostra o histórico resumido em uma linha por commit. |
| `git diff` | Mostra exatamente o que mudou nas linhas de código antes do add. |
| `git show <hash-do-commit>` | Mostra o que foi alterado em um commit específico. |

### 6. Desfazendo Coisas
| Comando | Descrição |
| :--- | :--- |
| `git checkout -- <arquivo>` | Descarta as mudanças feitas em um arquivo (volta ao último commit). |
| `git reset HEAD <arquivo>` | Tira um arquivo do "stage" (desfaz o `git add`). |
| `git reset --soft HEAD~1` | Desfaz o último commit, mas mantém seu código alterado. |
| `git reset --hard HEAD~1` | **CUIDADO:** Apaga o último commit e todas as alterações feitas nele. |
| `git stash` | "Esconde" suas alterações atuais para limpar a pasta sem perder o trabalho. |
| `git stash pop` | Recupera o que foi escondido pelo `stash`. |
