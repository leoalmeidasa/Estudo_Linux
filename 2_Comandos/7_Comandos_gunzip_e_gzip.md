# Resumo de `gzip` e `gunzip` no Linux

## 1. O que são?
- **`gzip`**: Utilizado para compactar arquivos.
- **`gunzip`**: Utilizado para descompactar arquivos `.gz` criados pelo `gzip`.

---

## 2. Sintaxe Geral
### `gzip`
```bash
gzip [OPÇÕES] [ARQUIVO(S)]
```

### `gunzip`
```bash
gunzip [OPÇÕES] [ARQUIVO(S)]
```

---

## 3. Exemplos de Uso

### 3.1 Compactar com `gzip`
- **Compactar um único arquivo**:
  ```bash
  gzip arquivo.txt
  ```
  *O arquivo `arquivo.txt` será substituído por `arquivo.txt.gz`.*

- **Compactar múltiplos arquivos**:
  ```bash
  gzip arquivo1.txt arquivo2.txt
  ```

- **Compactar recursivamente uma pasta**:
  ```bash
  gzip -r pasta/
  ```

---

### 3.2 Descompactar com `gunzip`
- **Descompactar um único arquivo**:
  ```bash
  gunzip arquivo.txt.gz
  ```
  *O arquivo `arquivo.txt.gz` será substituído por `arquivo.txt`.*

- **Descompactar múltiplos arquivos**:
  ```bash
  gunzip arquivo1.txt.gz arquivo2.txt.gz
  ```

- **Descompactar recursivamente uma pasta**:
  ```bash
  gunzip -r pasta/
  ```

---

### 3.3 Usar `gzip` com `tar`
- **Compactar com `tar` e `gzip` (criação de arquivo `.tar.gz`)**:
  ```bash
  tar -czf arquivo.tar.gz pasta/
  ```

- **Extrair um arquivo `.tar.gz`**:
  ```bash
  tar -xzf arquivo.tar.gz
  ```

---

## 4. Opções Comuns do `gzip` e `gunzip`

### `gzip`
| Opção        | Descrição                                         |
|--------------|---------------------------------------------------|
| `-v`         | Modo verboso: exibe informações detalhadas.       |
| `-r`         | Compacta arquivos recursivamente em pastas.       |
| `-k`         | Mantém o arquivo original após compactação.       |
| `--fast`     | Compactação rápida (menor taxa de compressão).    |
| `--best`     | Melhor compressão possível (mais lento).          |

### `gunzip`
| Opção        | Descrição                                         |
|--------------|---------------------------------------------------|
| `-v`         | Modo verboso: exibe informações detalhadas.       |
| `-r`         | Descompacta recursivamente.                       |
| `-k`         | Mantém o arquivo compactado após descompactação.  |

---

## 5. Dicas e Notas
- **Verificar o tamanho compactado:** 
  ```bash
  gzip -l arquivo.txt.gz
  ```
  *Exibe o tamanho antes e depois da compactação.*

- **Compatibilidade com outros utilitários:**
  - Use `zcat` para visualizar o conteúdo de arquivos compactados:
    ```bash
    zcat arquivo.txt.gz
    ```
  - Use `zgrep` para buscar padrões em arquivos compactados:
    ```bash
    zgrep "termo" arquivo.txt.gz
    ```

- **Compactação em nível máximo com gzip**:
  ```bash
  gzip --best arquivo.txt
  ```

Com esses comandos, você pode facilmente compactar e descompactar arquivos no Linux usando `gzip` e `gunzip`.

Ir para: [Shell](../Shell/1_Introducao.md)
