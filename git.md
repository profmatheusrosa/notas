
# Sumário
- [1. Introdução](#introdução)
  - [1.1. Visão Geral](#visão-geral)
    - [1.1.1. Objetivos](#objetivos)
    - [1.1.2. Escopo](#escopo)
- [2. Contexto](#contexto)
    - [1.2.1. Histórico](#histórico)
    - [1.2.2. Relevância Atual](#relevância-atual)


1. [Introdução](#introdução)
   1.1. [Visão Geral](#visão-geral)
   1.2. [Contexto](#contexto)
   
# Introdução

## Visão Geral

### Objetivos
O objetivo desta seção é apresentar uma visão geral do conteúdo abordado no documento, destacando os principais pontos que serão discutidos. Buscamos fornecer uma introdução clara e concisa, estabelecendo o propósito e a direção do material apresentado.

### Escopo
O escopo desta introdução abrange os tópicos que serão discutidos ao longo do documento, delimitando as áreas de interesse e estabelecendo as fronteiras do estudo. Aqui, especificamos os limites do conteúdo e o foco principal da análise.

[Voltar ao Sumário](#sumário)
# Contexto

### Histórico
Nesta subseção, discutimos o histórico do tema abordado, explorando suas origens e a evolução ao longo do tempo. Fornecemos uma perspectiva histórica para contextualizar a importância do assunto e como ele se desenvolveu até o presente.

### Relevância Atual
A relevância atual do tema é destacada nesta parte, onde discutimos a importância contemporânea do assunto em questão. Analisamos como ele impacta o cenário atual e sua significância em contextos específicos, como em áreas de pesquisa, mercado ou sociedade.


## Configurações
| Comando                          | Descrição                                      | Exemplo Prático                                       |
|----------------------------------|------------------------------------------------|-------------------------------------------------------|
| `git config --global user.name "<Seu Nome>"` | Define o nome do usuário globalmente.    | `git config --global user.name "João da Silva"`   |
| `git config --global user.email "<seu-email@example.com>"` | Define o email do usuário globalmente. | `git config --global user.email "joao@example.com"` |
| `git config --global core.editor "<editor>"` | Define o editor de texto padrão.        | `git config --global core.editor "vim"`             |
| `git config --global color.ui auto` | Ativa a colorização da saída do Git.   | `git config --global color.ui auto`                |
| `git config --global alias.<alias-name> "<command>"` | Cria um alias para um comando.  | `git config --global alias.st status`                |
| `git config --list` | Lista todas as configurações do Git.  | `git config --list`                                  |


| Comando                          | Descrição                                      | Exemplo Prático                                       |
|----------------------------------|------------------------------------------------|-------------------------------------------------------|
| `git init`                       | Inicia um novo repositório Git.                | `git init`                                            |
| `git clone <url>`                 | Clona um repositório existente.                | `git clone https://github.com/exemplo/repo.git`        |
| `git add <arquivo>`               | Adiciona alterações ao índice (staging area).  | `git add arquivo.txt`                                 |
| `git commit -m "Mensagem"`       | Grava as alterações no repositório.            | `git commit -m "Adiciona funcionalidade X"`            |
| `git status`                     | Exibe o estado das alterações.                 | `git status`                                          |
| `git diff`                       | Mostra as diferenças entre alterações.         | `git diff`                                            |
| `git log`                        | Exibe o histórico de commits.                  | `git log`                                             |
| `git log --oneline`              | Histórico de commits de forma resumida.        | `git log --oneline`                                   |
| `git branch`                     | Lista as ramificações locais.                  | `git branch`                                          |
| `git branch <nome>`              | Cria uma nova ramificação.                     | `git branch nova-feature`                             |
| `git checkout <ramificação>`     | Muda para uma ramificação específica.          | `git checkout desenvolvimento`                         |
| `git checkout -b <nome>`         | Cria e muda para uma nova ramificação.        | `git checkout -b nova-feature`                        |
| `git merge <ramificação>`        | Mescla alterações de uma ramificação.          | `git merge feature-branch`                            |
| `git pull`                       | Atualiza o repositório local.                  | `git pull origin master`                              |
| `git push`                       | Envia alterações locais para o remoto.         | `git push origin master`                              |
| `git fetch`                      | Busca alterações do repositório remoto.        | `git fetch origin`                                    |
| `git merge origin/<ramificação>` | Mescla alterações remotas na local.            | `git merge origin/main`                               |
| `git mergetool`                  | Abre ferramenta de mesclagem.                  | `git mergetool`                                       |
| `git reset HEAD <arquivo>`       | Remove um arquivo do índice.                  | `git reset HEAD arquivo.txt`                          |
| `git revert <commit>`            | Desfaz um commit específico.                   | `git revert abc123`                                   |
| `git reset --hard <commit>`      | Retorna o repositório para um commit.           | `git reset --hard abc123`                             |
