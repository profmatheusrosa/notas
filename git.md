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
| `git merge <ramificação>`        | Mescla alterações de uma ramificação.          | `git merge feature-branch`                            |
| `git pull`                       | Atualiza o repositório local.                  | `git pull origin master`                              |
| `git push`                       | Envia alterações locais para o remoto.         | `git push origin master`                              |
| `git fetch`                      | Busca alterações do repositório remoto.        | `git fetch origin`                                    |
| `git merge origin/<ramificação>` | Mescla alterações remotas na local.            | `git merge origin/main`                               |
| `git mergetool`                  | Abre ferramenta de mesclagem.                  | `git mergetool`                                       |
| `git reset HEAD <arquivo>`       | Remove um arquivo do índice.                  | `git reset HEAD arquivo.txt`                          |
| `git revert <commit>`            | Desfaz um commit específico.                   | `git revert abc123`                                   |
| `git reset --hard <commit>`      | Retorna o repositório para um commit.           | `git reset --hard abc123`                             |
