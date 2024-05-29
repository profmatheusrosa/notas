# Sumário

- [Filosofia do Software Livre e de Código Aberto](#filosofia-do-software-livre-e-de-código-aberto)
- [Interface Gráfica (GUI) e Linha de Comando (CLI)](#interface-gráfica-gui-e-linha-de-comando-cli)
- [Estrutura do Sistema de Arquivos Linux](#estrutura-do-sistema-de-arquivos-linux)
- [Comandos para Navegação no Sistema de Arquivos](#comandos-para-navegação-no-sistema-de-arquivos)
- [Permissões de Arquivos](#permissões-de-arquivos)
- [Gerência de Arquivos e Diretórios](#gerência-de-arquivos-e-diretórios)
- [Editores de Texto no Terminal](#editores-de-texto-no-terminal)
- [Filesystems](#filesystems)
- [Gerência de Usuários](#gerência-de-usuários)
- [Gerência de Memória e Processos](#gerência-de-memória-e-processos)
- [Gerência do Kernel](#gerência-do-kernel)
- [LVM (Logical Volume Manager)](#lvm-logical-volume-manager)
- [Gerência de Sistema e Diversos](#gerência-de-sistema-e-diversos)

---

# Filosofia do Software Livre e de Código Aberto
## Software Livre:
Definido pela Free Software Foundation (FSF).
Quatro liberdades essenciais: usar, estudar, modificar e distribuir.

## Código Aberto:
Definido pela Open Source Initiative (OSI).
Ênfase na qualidade do software, colaboração e desenvolvimento aberto.

# Interface Gráfica (GUI) e  Linha de Comando (CLI)
## Principais Ambientes de Desktop:
GNOME, KDE Plasma, XFCE, LXDE, Mate
## Navegação na Interface Gráfica:
Explorador de arquivos: Nautilus (GNOME), Dolphin (KDE), Thunar (XFCE)
## Acessando o terminal:
GNOME Terminal, Konsole (KDE), xterm, Terminator (emulador).

# Estrutura do Sistema de Arquivos Linux
| Diretório    | Descrição                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------|
| `/`          | Diretório raiz, o ponto de partida da hierarquia do sistema de arquivos.                           |
| `/bin`       | Contém binários essenciais do sistema, acessíveis a todos os usuários.                             |
| `/boot`      | Arquivos necessários para a inicialização do sistema, incluindo o kernel e inicializadores.        |
| `/dev`       | Arquivos de dispositivos que representam hardware e periféricos do sistema.                        |
| `/etc`       | Arquivos de configuração do sistema e scripts de inicialização.                                    |
| `/home`      | Diretórios pessoais dos usuários. Cada usuário tem um subdiretório dentro de `/home`.              |
| `/lib`       | Bibliotecas compartilhadas essenciais para os binários em `/bin` e `/sbin`.                        |
| `/lib64`     | Bibliotecas compartilhadas para sistemas 64-bit.                                                   |
| `/media`     | Pontos de montagem para dispositivos de mídia removíveis (CDs, DVDs, pen drives).                  |
| `/mnt`       | Ponto de montagem temporário para sistemas de arquivos montados manualmente.                       |
| `/opt`       | Pacotes de software opcionais e aplicativos de terceiros.                                          |
| `/proc`      | Sistema de arquivos virtual que fornece informações sobre o sistema e processos em execução.       |
| `/root`      | Diretório pessoal do usuário root (superusuário).                                                  |
| `/sbin`      | Binários essenciais do sistema usados para administração e manutenção do sistema.                  |
| `/srv`       | Dados específicos de serviço, como páginas web para servidores web.                                |
| `/tmp`       | Arquivos temporários criados por aplicativos. Esse diretório é limpo regularmente.                 |
| `/usr`       | Hierarquia secundária de programas e dados, contendo a maioria dos aplicativos e utilitários do usuário. |
| `/var`       | Arquivos variáveis, como logs do sistema, caches, filas de impressão e bancos de dados temporários.|

# Comandos para Navegação no Sistema de Arquivos
| **Comando** | **Descrição** | **Exemplo** |
|-------------|---------------|-------------|
| **ls** | Lista arquivos e diretórios no diretório atual. | `ls` |
| `ls -l` | Lista arquivos e diretórios com detalhes. | `ls -l` |
| `ls -a` | Lista todos os arquivos, incluindo os ocultos. | `ls -a` |
| `ls -lh` | Lista arquivos com tamanhos legíveis por humanos. | `ls -lh` |
| **cd** | Muda o diretório atual. | `cd /home/user` |
| `cd ..` | Vai para o diretório pai. | `cd ..` |
| `cd ~` | Vai para o diretório home do usuário. | `cd ~` |
| `cd -` | Volta para o diretório anterior. | `cd -` |
| **pwd** | Imprime o diretório de trabalho atual. | `pwd` |
| **cp** | Copia arquivos ou diretórios. | `cp arquivo1.txt /destino` |
| `cp -r` | Copia diretórios recursivamente. | `cp -r /origem /destino` |
| `cp -i` | Pede confirmação antes de sobrescrever arquivos. | `cp -i arquivo1.txt /destino` |
| **mv** | Move ou renomeia arquivos ou diretórios. | `mv arquivo1.txt /destino` |
| `mv -i` | Pede confirmação antes de sobrescrever arquivos. | `mv -i arquivo1.txt /destino` |
| **rm** | Remove arquivos ou diretórios. | `rm arquivo1.txt` |
| `rm -r` | Remove diretórios recursivamente. | `rm -r /diretorio` |
| `rm -f` | Força a remoção sem pedir confirmação. | `rm -f arquivo1.txt` |
| **mkdir** | Cria novos diretórios. | `mkdir novo_diretorio` |
| `mkdir -p` | Cria diretórios recursivamente. | `mkdir -p /novo/diretorio` |
| **rmdir** | Remove diretórios vazios. | `rmdir diretorio_vazio` |
| **touch <arquivo>** | Cria arquivos vazios ou atualiza a data de modificação de existentes | `touch arquivo.txt` |
| `touch <arquivo1> <arquivo2>` | Cria múltiplos arquivos ao mesmo tempo. | `touch arquivo1.txt arquivo2.txt` |
| **cat** | Concatena e exibe o conteúdo de arquivos. | `cat arquivo1.txt` |
| **more** | Exibe o conteúdo de arquivos, página por página. | `more arquivo1.txt` |
| **less** | Exibe o conteúdo de arquivos, página por página, com mais funcionalidades. | `less arquivo1.txt` |
| **head** | Exibe as primeiras linhas de um arquivo. | `head arquivo1.txt` |
| `head -n` | Exibe um número específico de linhas no início do arquivo. | `head -n 5 arquivo1.txt` |
| **tail** | Exibe as últimas linhas de um arquivo. | `tail arquivo1.txt` |
| `tail -n` | Exibe um número específico de linhas no final do arquivo. | `tail -n 5 arquivo1.txt` |
| **find** | Busca arquivos e diretórios no sistema de arquivos. | `find /home -name "*.txt"` |
| `find . -type f` | Busca apenas arquivos no diretório atual e subdiretórios. | `find . -type f` |
| `find /home -size +1M` | Busca arquivos maiores que 1MB. | `find /home -size +1M` |
| **grep** | Busca por padrões de texto dentro de arquivos. | `grep "termo" arquivo.txt` |
| `grep -r` | Busca recursivamente em diretórios. | `grep -r "termo" /diretorio` |
| `grep -i` | Busca sem diferenciar maiúsculas de minúsculas. | `grep -i "termo" arquivo.txt` |
| **nano** | Editor de texto simples no terminal. | `nano arquivo.txt` |
| **vi** | Editor de texto avançado no terminal. | `vi arquivo.txt` |
| `vim` | Versão melhorada do vi com mais funcionalidades. | `vim arquivo.txt` |

# Permissões de Arquivos


# Editores de Texto no Terminal
## Editor Nano
### Comando para abrir arquivos:
```bash
nano arquivo.txt
```
### Comandos básicos:
* Salvar: Ctrl + O
* Sair: Ctrl + X
* Cortar linha: Ctrl + K
* Colar linha: Ctrl + U

## Editor Vi/Vim
### Comando para abrir arquivos:
```bash
vi arquivo.txt`
```
### Comandos básicos:
* Entrar no modo de inserção: i
* Salvar e sair: :wq
* Sair sem salvar: :q!
* Navegar no texto: h, j, k, l (esquerda, baixo, cima, direita)

# Filesystems

# Gerência de Usuários
- [ ] adduser
- [ ] useradd
- [ ] userdel
- [ ] deluser

# Gerência de Memória e Processos
# Gerência do Kernel
# LVM (Logical Volume Manager)
# Gerência de Sistema e Diversos
