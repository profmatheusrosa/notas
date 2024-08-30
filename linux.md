# Sumário

- [Filosofia do Software Livre e de Código Aberto](#filosofia-do-software-livre-e-de-código-aberto)
- [Arquitetura](#arquitetura)
- [Interface Gráfica (GUI) e Linha de Comando (CLI)](#interface-gráfica-gui-e-linha-de-comando-cli)
- [Estrutura do Sistema de Arquivos Linux](#estrutura-do-sistema-de-arquivos-linux)
- [Comandos para Navegação no Sistema de Arquivos](#comandos-para-navegação-no-sistema-de-arquivos)
- [Permissões de Arquivos](#permissões-de-arquivos)
- [Gerência de Arquivos e Diretórios](#gerência-de-arquivos-e-diretórios)
- [Editores de Texto no Terminal](#editores-de-texto-no-terminal)
- [Filesystems](#filesystems)
- [Inode]
- [Gerência de Usuários](#gerência-de-usuários)
- [Gerência de Processos](#gerência-de-processos)
- [Gerência de Memória](#gerência-de-memória)
- [Gerência do Kernel](#gerência-do-kernel)
- [LVM (Logical Volume Manager)](#lvm-logical-volume-manager)
- [Gerência de Sistema e Diversos](#gerência-de-sistema-e-diversos)
- [Principais Arquivos de Configuração do Sistema](#principais-arquivos-de-configuração-do-sistema)

---
# Modificações futuras
- [ ] setuid 

# Filosofia do Software Livre e de Código Aberto
### Software Livre:
Definido pela Free Software Foundation (FSF).
Quatro liberdades essenciais: usar, estudar, modificar e distribuir.

### Código Aberto:
Definido pela Open Source Initiative (OSI).
Ênfase na qualidade do software, colaboração e desenvolvimento aberto.

# Interface Gráfica (GUI) e  Linha de Comando (CLI)
### Principais Ambientes de Desktop:
GNOME, KDE Plasma, XFCE, LXDE, Mate
### Navegação na Interface Gráfica:
Explorador de arquivos: Nautilus (GNOME), Dolphin (KDE), Thunar (XFCE)
### Acessando o terminal:
GNOME Terminal, Konsole (KDE), xterm, Terminator (emulador).

[Voltar ao Sumário](#sumário)
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

[Voltar ao Sumário](#sumário)
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

[Voltar ao Sumário](#sumário)
# Permissões de Arquivos
- [ ] UGO
- [ ] notação octal
- [ ] notação simbolica
- [ ] umask
As permissões de arquivos em sistemas Unix/Linux são representadas por três grupos de três bits cada:

1. **Dono do arquivo**: Leitura (r), escrita (w), e execução (x).
2. **Grupo**: Leitura (r), escrita (w), e execução (x).
3. **Outros usuários**: Leitura (r), escrita (w), e execução (x).

-### Permissões Octais

Essas permissões são representadas em octal (base 8) da seguinte maneira:
- **4**: Leitura (r)
- **2**: Escrita (w)
- **1**: Execução (x)

Esses valores são somados para formar as permissões para cada grupo. Por exemplo, `r-x` seria 4 + 1 = 5.

### Bits Especiais

Além das permissões básicas, existem três bits especiais:

1. **setuid (Set User ID)**: Quando definido, faz com que o arquivo seja executado com as permissões do dono do arquivo, não com as permissões do usuário que o está executando. Em octal, o bit `setuid` é representado por **4**.

2. **setgid (Set Group ID)**: Quando definido em um arquivo, faz com que o arquivo seja executado com as permissões do grupo do arquivo. Em um diretório, faz com que novos arquivos criados no diretório herdem o grupo do diretório. O bit `setgid` é representado por **2** em octal.

3. **sticky bit**: Usado em diretórios para garantir que somente o dono do arquivo pode deletar ou renomear seus próprios arquivos dentro do diretório. Em octal, o sticky bit é representado por **1**.

Para aplicar esses bits especiais, adicionamos um valor adicional ao início da permissão octal normal. O `4` no início indica que o bit `setuid` está ativado.

Então, no caso das permissões `-rwsr-xr-x`:

- O `rws` indica que o dono do arquivo tem permissão de leitura, escrita e execução, com o bit `setuid` ativado.
- Isso se traduz em **4** (para `setuid`) + **7** (para `rwx`) = **4755** em octal.

Portanto, a permissão octal `4755` representa o arquivo com o bit `setuid` ativado e as permissões `rwxr-xr-x`.

[Voltar ao Sumário](#sumário)
# Editores de Texto no Terminal
## Editor Nano

| **Ação**                    | **Comando**                |
|-----------------------------|----------------------------|
| Abrir arquivo               | `nano arquivo.txt`         |
| Salvar                      | `Ctrl + O`, depois `Enter` |
| Sair                        | `Ctrl + X`                 |
| Cortar linha                | `Ctrl + K`                 |
| Colar linha                 | `Ctrl + U`                 |
| Procurar texto              | `Ctrl + W`, digite o texto e pressione `Enter` |
| Ir para linha               | `Ctrl + _`, digite o número da linha e pressione `Enter` |

## Editor Vi/Vim
| **Ação**                    | **Comando**                |
|-----------------------------|----------------------------|
| Abrir arquivo               | `vi arquivo.txt` <br> `vim arquivo.txt` |
| Entrar no modo de inserção  | `i` (inserir) <br> `a` (adicionar) |
| Salvar e sair               | `:wq` e pressione `Enter`   |
| Sair sem salvar             | `:q!` e pressione `Enter`   |
| Navegar no texto            | `h` (esquerda) <br> `j` (baixo) <br> `k` (cima) <br> `l` (direita) |
| Excluir linha               | `dd`                       |
| Copiar linha                | `yy`                       |
| Colar linha                 | `p`                        |
| Buscar texto                | `/texto` e pressione `Enter` |
| Substituir texto            | `:%s/antigo/novo/g` e pressione `Enter` |
| Visualizar alterações       | `u` (desfazer) <br> `Ctrl + r` (refazer) |

## Editor Emacs (Opcional)
| **Ação**                    | **Comando**                |
|-----------------------------|----------------------------|
| Abrir arquivo               | `emacs arquivo.txt`        |
| Salvar                      | `Ctrl + x`, depois `Ctrl + s` |
| Sair                        | `Ctrl + x`, depois `Ctrl + c` |
| Cortar texto                | `Ctrl + k`                 |
| Colar texto                 | `Ctrl + y`                 |
| Buscar texto                | `Ctrl + s`, digite o texto e pressione `Enter` |

[Voltar ao Sumário](#sumário)
# Filesystems
## Tipos Comuns de Sistemas de Arquivos

### 1. **Ext4 (Fourth Extended File System)**
- **Descrição:** É o sistema de arquivos padrão para a maioria das distribuições Linux. Oferece melhorias significativas em relação ao ext3, como suporte a volumes maiores e maior eficiência na alocação de espaço.
- **Características:**
  - Tamanho máximo de arquivo: 16 TB
  - Tamanho máximo de sistema de arquivos: 1 EB (Exabyte)
  - Suporte a journaling para recuperação após falhas
  - Melhoria na performance e no gerenciamento de espaço
- **Comandos:**
  - `mkfs.ext4 /dev/sdXn` – Formata a partição com ext4
  - `e2fsck -f /dev/sdXn` – Verifica e corrige o sistema de arquivos

### 2. **XFS**
- **Descrição:** Um sistema de arquivos de alta performance desenvolvido pela SGI (Silicon Graphics) que é bem adequado para grandes volumes e sistemas de arquivos de grande porte.
- **Características:**
  - Tamanho máximo de arquivo: 8 EB
  - Tamanho máximo de sistema de arquivos: 8 EB
  - Suporte a journaling
  - Bom desempenho em operações com grandes arquivos
- **Comandos:**
  - `mkfs.xfs /dev/sdXn` – Formata a partição com xfs
  - `xfs_repair /dev/sdXn` – Verifica e corrige o sistema de arquivos

### 3. **Btrfs (B-tree File System)**
- **Descrição:** Um sistema de arquivos avançado que oferece suporte a recursos como snapshots, controle de versão e verificação de integridade dos dados.
- **Características:**
  - Tamanho máximo de arquivo: 16 EB
  - Tamanho máximo de sistema de arquivos: 16 EB
  - Suporte a snapshots e subvolumes
  - Controle de integridade e correção automática de erros
- **Comandos:**
  - `mkfs.btrfs /dev/sdXn` – Formata a partição com btrfs
  - `btrfs check /dev/sdXn` – Verifica e corrige o sistema de arquivos

### 4. **FAT32 e NTFS**
- **Descrição:** Sistemas de arquivos usados principalmente em ambientes Windows, mas também suportados no Linux para interoperabilidade.
- **Características:**
  - **FAT32:** Suporte a tamanhos menores de arquivo e sistema de arquivos comparado ao NTFS.
  - **NTFS:** Suporte a permissões de arquivos, criptografia e outros recursos avançados.
- **Comandos:**
  - `mkfs.vfat /dev/sdXn` – Formata a partição com FAT32
  - `ntfs-3g /dev/sdXn /mnt/ntfs` – Monta uma partição NTFS
 
## Comandos de Montagem e Desmontagem

| Ação          | Comando                                 | Descrição                                      |
|---------------|-----------------------------------------|------------------------------------------------|
| Montar        | `mount /dev/sdXn /ponto/de/montagem`    | Torna o sistema de arquivos acessível          |
| Desmontar      | `umount /ponto/de/montagem`             | Remove o acesso ao sistema de arquivos         |

## Verificação e Reparação de Sistemas de Arquivos

| Ação          | Comando                  | Descrição                                             |
|---------------|--------------------------|-------------------------------------------------------|
| Verificar     | `fsck /dev/sdXn`         | Verifica e corrige erros em sistemas de arquivos    |
| Ajustar       | `tune2fs -l /dev/sdXn`   | Exibe informações sobre sistemas de arquivos ext2/ext3/ext4 |

## Gerenciamento de Espaço em Disco

| Ação          | Comando                    | Descrição                                      |
|---------------|----------------------------|------------------------------------------------|
| Espaço Livre   | `df -h`                    | Exibe o uso de espaço em disco em formato legível por humanos |
| Uso de Disco   | `du -sh /caminho/para/diretorio` | Estima o uso de espaço por arquivos e diretórios |

[Voltar ao Sumário](#sumário)
# Gerência de Usuários
| **Comando** | **Descrição** | **Exemplo** |
|-------------|---------------|-------------|
| `useradd` | Cria um novo usuário no sistema. | `useradd matheus` |
| `useradd -m` | Cria o diretório home do usuário. | `useradd -m matheus` |
| `useradd -s /bin/bash` | Define o shell padrão do usuário. | `useradd -s /bin/bash matheus` |
| `usermod` | Modifica as propriedades de um usuário existente. | `usermod -aG sudo matheus` |
| `usermod -aG` | Adiciona o usuário a um grupo adicional. | `usermod -aG sudo matheus` |
| `usermod -l` | Altera o nome do usuário. | `usermod -l novo_nome matheus` |
| `usermod -d` | Muda o diretório home do usuário. | `usermod -d /novo/home matheus` |
| `userdel` | Remove um usuário do sistema. | `userdel matheus` |
| `userdel -r` | Remove também o diretório home do usuário. | `userdel -r matheus` |
| `passwd` | Define ou altera a senha de um usuário. | `passwd matheus` |
| `groupadd` | Cria um novo grupo. | `groupadd desenvolvedores` |
| `groupmod` | Modifica as propriedades de um grupo existente. | `groupmod -n devs desenvolvedores` |
| `groupdel` | Remove um grupo do sistema. | `groupdel desenvolvedores` |
| `id` | Exibe informações sobre o usuário atual ou especificado. | `id matheus` |
| `su` | Permite trocar para outro usuário ou executar comandos como outro usuário. | `su - matheus` |
| `su -` | Muda para o superusuário root. | `su -` |
| `sudo` | Executa um comando como outro usuário, geralmente root. | `sudo useradd matheus` |
| `who` | Exibe uma lista de usuários atualmente logados no sistema. | `who` |
| `chage` | Gerencia as políticas de expiração de senha de um usuário. | `chage -l matheus` |
| `chage -M` | Define o número máximo de dias antes que a senha expire. | `chage -M 90 matheus` |
| `chage -E` | Define a data de expiração da conta. | `chage -E 2024-12-31 matheus` |

[Voltar ao Sumário](#sumário)
# Gerência de Processos
- [ ] componentes de um processo
- [ ] nohup
- [ ] ps
- [ ] top
- [ ] jobs
- [ ] bg
- [ ] fg
- [ ] free
- [ ] nice
- [ ] renice
- [ ] kill
- [ ] killall

[Voltar ao Sumário](#sumário)
# Gerência de Memória
| **Comando**      | **Descrição**                                                   | **Exemplo**                           |
|------------------|-------------------------------------------------------------------|---------------------------------------|
| **free**         | Exibe informações sobre o uso de memória no sistema.             | `free`                                |
| `free -h`        | Exibe informações de memória em um formato legível por humanos.   | `free -h`                             |
| **top**          | Exibe uma visão geral dinâmica dos processos em execução e do uso de memória. | `top`                                 |
| **htop**         | Versão melhorada do `top`, com uma interface mais amigável e opções interativas. | `htop`                                |
| **vmstat**       | Fornece informações sobre processos, memória, paginação, blocos de entrada/saída, interrupções e atividade de CPU. | `vmstat`                               |
| `vmstat 5`       | Exibe informações de memória a cada 5 segundos.                   | `vmstat 5`                            |
| **ps**           | Mostra informações sobre processos em execução.                  | `ps aux`                              |
| `ps aux --sort=-%mem` | Exibe processos ordenados pelo uso de memória.                | `ps aux --sort=-%mem`                 |
| **pmap**         | Exibe o mapeamento de memória de um processo específico.           | `pmap <PID>`                          |
| **smem**         | Relata o uso de memória de processos com informações de memória compartilhada e não compartilhada. | `smem`                                |
| **free -t**      | Exibe o total de memória utilizada e disponível.                  | `free -t`                             |
| **sysctl**       | Permite modificar parâmetros do kernel em tempo real.             | `sysctl -a | grep mem`                |
| `sysctl vm.swappiness` | Exibe o valor atual da variável de swappiness.                | `sysctl vm.swappiness`               |
| **swapon**       | Mostra o status das áreas de swap ativas.                         | `swapon --show`                       |
| **swapoff**      | Desativa uma área de swap.                                        | `swapoff /swapfile`                  |
| **swapon**       | Ativa uma área de swap.                                           | `swapon /swapfile`                   |
| **dd**           | Pode ser usado para criar um arquivo de swap.                     | `dd if=/dev/zero of=/swapfile bs=1M count=1024` |
| `mkswap`         | Cria uma área de swap em um arquivo ou partição.                   | `mkswap /swapfile`                   |
| `swapon`         | Ativa o arquivo de swap.                                          | `swapon /swapfile`                   |


[Voltar ao Sumário](#sumário)
# Gerência do Kernel

[Voltar ao Sumário](#sumário)
# LVM (Logical Volume Manager)
LVM (Logical Volume Management) é uma tecnologia de gerenciamento de armazenamento no Linux que permite maior flexibilidade na gestão de discos rígidos e partições. Com LVM, é possível redimensionar, mover e gerenciar volumes lógicos de forma dinâmica sem interromper o funcionamento do sistema.

### 2. Conceitos Básicos
- **Physical Volume (PV):** Corresponde ao disco físico ou partição em que o LVM será implementado. Cada PV pode ser um disco inteiro ou uma partição específica.
- **Volume Group (VG):** Um grupo de volumes físicos que são combinados para formar um pool de armazenamento. Um VG pode conter vários PVs.
- **Logical Volume (LV):** Um volume lógico que é criado dentro de um VG e pode ser usado para criar sistemas de arquivos. É similar a uma partição, mas oferece muito mais flexibilidade, como redimensionamento dinâmico.
- **Logical Extents (LE) e Physical Extents (PE):** Pequenas unidades de armazenamento, normalmente de 4 MB, em que os LVs e PVs são divididos. Cada LE mapeia diretamente para um PE.

### 3. Por que Usar LVM?
- **Flexibilidade:** LVM permite redimensionar volumes lógicos sem precisar parar o sistema ou desmontar partições.
- **Facilidade de Gerenciamento:** Adicionar ou remover discos de um volume group é simples e não requer reparticionamento.
- **Snapshots:** LVM permite criar snapshots (cópias congeladas) de volumes lógicos para backups ou testes.
- **Desempenho:** LVM pode melhorar o desempenho ao distribuir dados entre múltiplos discos.

[Voltar ao Sumário](#sumário)
# Gerência de Sistema e Diversos

[Voltar ao Sumário](#sumário)
# Principais Arquivos de Configuração do Sistema
### Arquivos de Configuração do Sistema
| **Caminho**                                | **Arquivo**                | **Descrição**                                                        |
|--------------------------------------------|----------------------------|------------------------------------------------------------------------|
| `/etc/passwd`                              | Arquivo de Senhas          | Contém informações básicas sobre usuários, como nome e ID.            |
| `/etc/shadow`                              | Arquivo de Senhas Criptografadas | Armazena senhas criptografadas dos usuários e dados relacionados à expiração de senhas. |
| `/etc/group`                               | Arquivo de Grupos          | Define os grupos de usuários no sistema.                              |
| `/etc/gshadow`                             | Arquivo de Senhas dos Grupos | Armazena informações de senhas para grupos e dados de controle de acesso. |
| `/etc/network/interfaces`                  | Arquivo de Configuração de Rede (Debian) | Configura as interfaces de rede (para distribuições baseadas em Debian). |
| `/etc/sysconfig/network-scripts/ifcfg-*`   | Arquivo de Configuração de Rede (Red Hat) | Configura interfaces de rede (para distribuições baseadas em Red Hat). |
| `/etc/hostname`                            | Arquivo de Configuração do Hostname | Define o nome do host do sistema.                                     |
| `/etc/hosts`                               | Arquivo de Configuração do Hosts    | Mapeia nomes de host para endereços IP.                               |
| `/etc/samba/smb.conf`                      | Arquivo de Configuração do Samba     | Configura o servidor e cliente Samba.                                 |
| `/etc/ssh/sshd_config`                     | Arquivo de Configuração do SSH       | Configura o daemon SSH, incluindo permissões e opções de autenticação. |
| `/etc/crontab`                             | Arquivo de Configuração do Cron       | Define tarefas agendadas para o sistema.                              |
| `/etc/systemd/system/`                    | Arquivo de Configuração do Systemd   | Contém unidades e configurações do `systemd`.                         |

### Arquivos de Configuração do Sistema de Arquivos

| **Caminho**                                | **Arquivo**                                | **Descrição**                                                        |
|--------------------------------------------|--------------------------------------------|------------------------------------------------------------------------|
| `/etc/fstab`                              | Arquivo de Tabelas de Partição             | Define as partições de disco a serem montadas automaticamente.         |
| `/etc/default/grub`                       | Arquivo de Configuração do GRUB            | Contém opções de configuração do carregador de inicialização GRUB.     |

### Arquivos de Log

| **Caminho**                                | **Arquivo**                                | **Descrição**                                                        |
|--------------------------------------------|--------------------------------------------|------------------------------------------------------------------------|
| `/var/log/syslog`                          | Log de Sistema                             | Contém mensagens do sistema e do kernel.                              |
| `/var/log/kern.log`                        | Log do Kernel                              | Registra mensagens do kernel.                                         |
| `/var/log/auth.log`                        | Log de Autenticação                        | Registra eventos relacionados à autenticação.                         |
| `/var/log/messages`                       | Log de Mensagens Gerais                    | Contém mensagens gerais de vários serviços do sistema.                |

[Voltar ao Sumário](#sumário)
