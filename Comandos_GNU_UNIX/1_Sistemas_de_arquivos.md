# Sistema de Arquivos do Ubuntu

O sistema de arquivos do Ubuntu segue a estrutura hierárquica do padrão **Filesystem Hierarchy Standard (FHS)**, comum nas distribuições Linux. Essa organização facilita a navegação e o gerenciamento de arquivos e diretórios.

---

## **Estrutura Principal**

### 1. **Raiz (`/`)**
- O ponto de início de todos os diretórios e arquivos no Ubuntu.
- Contém subdiretórios importantes que organizam o sistema.

### 2. **Diretórios Principais**

| Diretório      | Descrição                                                                 |
|----------------|---------------------------------------------------------------------------|
| **`/bin`**     | Binários essenciais do sistema acessíveis a todos os usuários (ex.: `ls`, `cp`). |
| **`/boot`**    | Arquivos de inicialização do sistema, incluindo o kernel.                |
| **`/dev`**     | Arquivos de dispositivos (ex.: discos, USBs, etc.).                      |
| **`/etc`**     | Arquivos de configuração do sistema.                                     |
| **`/home`**    | Diretórios pessoais dos usuários (ex.: `/home/usuario`).                 |
| **`/lib`**     | Bibliotecas essenciais compartilhadas por programas do sistema.          |
| **`/media`**   | Pontos de montagem automáticos para dispositivos removíveis.             |
| **`/mnt`**     | Pontos de montagem temporária para dispositivos externos.                |
| **`/opt`**     | Software e pacotes adicionais instalados manualmente.                   |
| **`/proc`**    | Sistema de arquivos virtual que fornece informações sobre processos e o kernel. |
| **`/root`**    | Diretório pessoal do superusuário (root).                                |
| **`/run`**     | Arquivos de dados temporários criados no tempo de execução.              |
| **`/sbin`**    | Binários de administração do sistema (ex.: `reboot`, `ifconfig`).        |
| **`/srv`**     | Dados de serviços fornecidos pelo sistema (ex.: servidores web).         |
| **`/tmp`**     | Arquivos temporários (limpados automaticamente após a reinicialização).  |
| **`/usr`**     | Programas e arquivos de usuários, incluindo binários e bibliotecas adicionais. |
| **`/var`**     | Dados variáveis como logs, cache e emails.                              |

---

## **Características do Sistema de Arquivos do Ubuntu**

1. **Formato Padrão**
   - **Ext4**: Sistema de arquivos padrão no Ubuntu. É robusto, rápido e confiável.

2. **Permissões de Arquivo**
   - Controle de acesso baseado em:
     - **Usuário**: Proprietário do arquivo.
     - **Grupo**: Grupo de usuários com acesso.
     - **Outros**: Permissões para todos os outros usuários.
   - Permissões principais:
     - **r**: Leitura.
     - **w**: Escrita.
     - **x**: Execução.

3. **Sistema de Links**
   - **Links simbólicos**: Atalhos para arquivos/diretórios.
   - **Links físicos**: Referências diretas ao conteúdo do arquivo.

4. **Montagem**
   - Dispositivos externos (ex.: USB, discos) são montados em diretórios específicos para acesso.

5. **Sistema de Logs**
   - Logs do sistema são armazenados em **`/var/log`** para análise e diagnóstico.

---

## **Comandos Importantes**

| Comando         | Função                                                 |
|------------------|--------------------------------------------------------|
| `ls`            | Lista arquivos e diretórios.                           |
| `cd`            | Navega entre diretórios.                               |
| `pwd`           | Exibe o diretório atual.                               |
| `cp`            | Copia arquivos e diretórios.                           |
| `mv`            | Move ou renomeia arquivos e diretórios.                |
| `rm`            | Remove arquivos ou diretórios.                         |
| `chmod`         | Altera permissões de arquivos.                         |
| `df -h`         | Exibe o uso de espaço em disco.                        |
| `mount`         | Monta sistemas de arquivos.                            |
| `umount`        | Desmonta sistemas de arquivos.                         |

---

## **Conclusão**
O sistema de arquivos do Ubuntu é organizado e eficiente, seguindo padrões amplamente reconhecidos. Ele oferece flexibilidade, segurança e controle, facilitando o gerenciamento do sistema e arquivos, tanto para iniciantes quanto para usuários avançados.

Ir para: [Arquivos](Comandos_GNU_UNIX/2_Arquivos.md)