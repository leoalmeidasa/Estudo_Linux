# Resumo de Caracteres e Operadores no Linux

## 1. Operadores de Redirecionamento
Usados para redirecionar entrada, saída e erros.

| Operador | Descrição                                         | Exemplo                          |
|----------|---------------------------------------------------|----------------------------------|
| `>`      | Redireciona saída padrão para um arquivo (sobrescreve). | `ls > arquivo.txt`              |
| `>>`     | Redireciona saída padrão para um arquivo (anexa).  | `echo "texto" >> arquivo.txt`   |
| `<`      | Redireciona entrada padrão de um arquivo.         | `cat < arquivo.txt`             |
| `2>`     | Redireciona erros padrão para um arquivo.         | `comando 2> erro.txt`           |
| `2>&1`   | Redireciona erros padrão para a saída padrão.     | `comando > saida.txt 2>&1`      |
| `|`      | Pipe: redireciona a saída de um comando para outro. | `ls | grep "arquivo"`           |

---

## 2. Caracteres Especiais
Usados para manipulação de comandos, arquivos e scripts.

| Caractere | Descrição                                         | Exemplo                          |
|-----------|---------------------------------------------------|----------------------------------|
| `*`       | Coringa: combina zero ou mais caracteres.         | `ls *.txt`                      |
| `?`       | Coringa: combina exatamente um caractere.         | `ls arq?.txt`                   |
| `[]`      | Combina qualquer caractere listado no conjunto.   | `ls [aeiou]*`                   |
| `{}`      | Expande sequências de texto.                     | `echo {1..5}`                   |
| `~`       | Representa o diretório inicial do usuário.        | `cd ~/Documentos`               |
| `$`       | Indica uma variável.                             | `echo $HOME`                    |
| `#`       | Inicia um comentário em scripts.                 | `# Este é um comentário`        |
| `\`       | Escapa caracteres especiais.                     | `echo \$HOME`                   |

---

## 3. Operadores Lógicos e Condicionais
Usados para controle de fluxo.

| Operador | Descrição                                         | Exemplo                          |
|----------|---------------------------------------------------|----------------------------------|
| `&&`     | Executa o próximo comando se o anterior for bem-sucedido. | `mkdir pasta && cd pasta`       |
| `||`     | Executa o próximo comando se o anterior falhar.   | `comando1 || comando2`          |
| `;`      | Separa comandos, executa todos independentemente. | `comando1; comando2`            |

---

## 4. Operadores em Regex (Expressões Regulares)
Usados para busca e manipulação de texto.

| Operador | Descrição                                         | Exemplo                          |
|----------|---------------------------------------------------|----------------------------------|
| `.`      | Combina qualquer caractere.                      | `grep "a.e" arquivo.txt`        |
| `^`      | Indica início de linha.                          | `grep "^inicio" arquivo.txt`    |
| `$`      | Indica final de linha.                           | `grep "fim$" arquivo.txt`       |
| `*`      | Combina zero ou mais ocorrências do caractere anterior. | `grep "a*" arquivo.txt`        |
| `+`      | Combina uma ou mais ocorrências do caractere anterior. | `grep "a+" arquivo.txt`        |
| `?`      | Combina zero ou uma ocorrência do caractere anterior. | `grep "a?" arquivo.txt`        |
| `|`      | Alternativa (ou lógico).                         | `grep "opcao1|opcao2" arquivo.txt` |
| `()`     | Agrupamento de padrões.                          | `grep "a(bc|de)f" arquivo.txt`  |

---

## 5. Operadores de Comparação em Scripts
Usados em scripts `bash`.

| Operador | Descrição                                         | Exemplo                          |
|----------|---------------------------------------------------|----------------------------------|
| `-eq`    | Igual a.                                          | `[ $a -eq $b ]`                 |
| `-ne`    | Diferente de.                                     | `[ $a -ne $b ]`                 |
| `-lt`    | Menor que.                                        | `[ $a -lt $b ]`                 |
| `-gt`    | Maior que.                                        | `[ $a -gt $b ]`                 |
| `-le`    | Menor ou igual a.                                 | `[ $a -le $b ]`                 |
| `-ge`    | Maior ou igual a.                                 | `[ $a -ge $b ]`                 |

---

## 6. Operadores de Permissão
Usados para manipular permissões de arquivos.

| Operador | Descrição                                         | Exemplo                          |
|----------|---------------------------------------------------|----------------------------------|
| `+`      | Adiciona permissão.                               | `chmod +x arquivo.sh`           |
| `-`      | Remove permissão.                                 | `chmod -w arquivo.txt`          |
| `=`      | Define permissão explicitamente.                  | `chmod u=r arquivo.txt`         |

---

Com esses operadores, você pode manipular e executar tarefas no Linux de forma eficiente.

Ir para: [Comando Tar](6_Comando_tar.md)
