# Arquivos no Linux

No Linux, os arquivos são organizados em uma estrutura hierárquica começando pelo diretório raiz (`/`). Tudo no Linux é tratado como um arquivo, incluindo dispositivos de hardware e processos, o que torna o sistema extremamente flexível e unificado.

---

## **Tipos de Arquivos no Linux**

1. **Arquivos Comuns**:
   - Contêm dados, texto, ou código de programas.
   - Representados como `-` no início das permissões (ex.: `-rw-r--r--`).

2. **Diretórios**:
   - Contêm outros arquivos e diretórios.
   - Representados como `d` no início das permissões (ex.: `drwxr-xr-x`).

3. **Links**:
   - **Simbólicos (Soft Links)**:
     - Atalhos para outros arquivos ou diretórios.
     - Representados como `l` no início das permissões (ex.: `lrwxrwxrwx`).
   - **Físicos (Hard Links)**:
     - Referências adicionais para o mesmo conteúdo de um arquivo.

4. **Arquivos de Dispositivo**:
   - Representam hardware do sistema.
   - **Caracteres (`c`)**: Dispositivos que operam em modo de caracteres (ex.: terminais).
   - **Blocos (`b`)**: Dispositivos de armazenamento (ex.: discos rígidos).

5. **Arquivos de FIFO (Named Pipes)**:
   - Usados para comunicação entre processos.
   - Representados como `p` no início das permissões.

6. **Sockets**:
   - Usados para comunicação entre processos, geralmente na rede.
   - Representados como `s` no início das permissões.

6. **Extensão**:
- A extensão serve para identificar o tipo do arquivo. A extensão são as letras após um “.” no
nome de um arquivo, explicando melhor:

• relatório.txt - O .txt indica que o conteúdo é um arquivo texto.
• script.sh - Arquivo de Script (interpretado por "/bin/sh").
• system.log - Registro de algum programa no sistema.
• arquivo.gz - Arquivo compactado pelo utilitário "gzip".
• index.html - Página de Internet (formato Hypertexto).

---

## **Estrutura de Nomeação**

- **Caminhos Absolutos**:
  - Começam com `/` e indicam a localização desde o diretório raiz.
  - Exemplo: `/home/usuario/documento.txt`.

- **Caminhos Relativos**:
  - Relacionados ao diretório atual.
  - Exemplo: `../outro-diretorio/arquivo.txt`.

---

## **Permissões de Arquivo**

1. **Estrutura de Permissões**:
   - **r**: Leitura.
   - **w**: Escrita.
   - **x**: Execução.
   - Exemplo: `-rw-r--r--`.

2. **Categorias de Usuários**:
   - **Usuário (u)**: Proprietário do arquivo.
   - **Grupo (g)**: Grupo ao qual o proprietário pertence.
   - **Outros (o)**: Todos os demais usuários.

3. **Gerenciamento de Permissões**:
   - Modificar permissões: 
     ```bash
     chmod u+x arquivo
     ```

---

## **Comandos Úteis para Arquivos**

| Comando          | Função                                           |
|-------------------|--------------------------------------------------|
| `ls`             | Lista arquivos e diretórios.                     |
| `cd`             | Navega entre diretórios.                         |
| `cp`             | Copia arquivos ou diretórios.                    |
| `mv`             | Move ou renomeia arquivos.                       |
| `rm`             | Remove arquivos ou diretórios.                   |
| `touch`          | Cria um arquivo vazio ou atualiza o timestamp.   |
| `cat`            | Exibe o conteúdo de um arquivo.                  |
| `less`/`more`    | Exibe o conteúdo de arquivos com rolagem.        |
| `find`           | Localiza arquivos com base em critérios.         |
| `grep`           | Pesquisa por texto em arquivos.                  |

---

## **Sistemas de Arquivos no Linux**

1. **Tipos Comuns**:
   - **ext4**: Padrão em distribuições Linux modernas.
   - **xfs**: Ideal para grandes sistemas e servidores.
   - **btrfs**: Avançado, com suporte a snapshots.

2. **Gerenciamento**:
   - Montagem: 
     ```bash
     mount /dev/sda1 /mnt
     ```
   - Desmontagem:
     ```bash
     umount /mnt
     ```

---

## **Características Importantes**

- **Case Sensitive**:
  - Arquivos com nomes diferentes de maiúsculas e minúsculas são tratados como distintos.
  - Exemplo: `Arquivo.txt` ≠ `arquivo.txt`.

- **Arquivos Ocultos**:
  - Começam com `.` e não aparecem na listagem padrão.
  - Exemplo: `.bashrc`.

- **Logs do Sistema**:
  - Armazenados em `/var/log`.

---

## **Conclusão**

O gerenciamento de arquivos no Linux é versátil e robusto, oferecendo controle detalhado sobre permissões, estrutura e manipulação. Entender a organização e os comandos básicos é essencial para trabalhar de forma eficiente no sistema.

Ir para: [Gerenciando Arquivos](3_Gerenciando_arquivos.md)