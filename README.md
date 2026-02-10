# LAB 01 - Navegação no Terminal Linux

Sistemas Operacionais - 2026/1

- **Objetivo**: Familiarizar-se com a navegação e manipulação de arquivos em sistemas UNIX pelo terminal e também praticar o fluxo básico de entrega via Git, que será usado em todos os laboratórios seguintes.
---
## Referências Essenciais

- [Guia de comandos básicos do Linux (Ubuntu Docs)](https://documentation.ubuntu.com/desktop/en/latest/tutorial/the-linux-command-line-for-beginners/)
- [UNIX: Uso básico do Shell (Prof. Carlos Maziero)](https://wiki.inf.ufpr.br/maziero/doku.php?id=unix%3Ashell_basico)
- [UNIX: Comandos em arquivos (Prof. Carlos Maziero)](https://wiki.inf.ufpr.br/maziero/doku.php?id=unix%3Acomandos_basicos)


### Sobre o Codespaces

O terminal do Codespaces funciona como qualquer terminal Linux. A diferença principal é que seu diretório inicial será `/workspaces/<nome-do-repositorio>` em vez do tradicional `/home/<usuario>`. Para os exercícios, considere esse diretório como sua "pasta de trabalho".

### Gravando sua sessão
Antes de começar os exercícios, execute no terminal (substitua `<SEU_RA>` pelo seu RA):

```bash
script LAB1SO_<SEU_RA>.txt
```

Esse comando grava tudo o que você digitar e toda saída do terminal em um arquivo de texto. Quando terminar todos os exercícios, encerre a gravação com:

```bash
exit
```

Não se preocupe com erros durante a sessão, eles fazem parte do processo e ficarão registrados normalmente.

---

## Exercícios

### Exercício 1 - Navegação básica

1. Exiba o caminho do seu diretório atual.
2. Liste todos os arquivos do diretório, incluindo os ocultos.
3. Crie um diretório com o nome que preferir.
4. Entre no diretório criado.
5. Volte para o diretório anterior.
6. Volte para o diretório de trabalho inicial (`/workspaces/<nome-do-repositorio>`).

### Exercício 2 — Manipulação de arquivos

1. Entre no diretório criado no exercício anterior.
2. Crie um arquivo vazio chamado `teste.txt`.
3. Escreva seu nome completo dentro deste arquivo (usando o comando ou editor que preferir).
4. Exiba o conteúdo do arquivo no terminal.
5. Faça uma cópia do arquivo chamada `teste_backup.txt`.
6. Liste os arquivos para confirmar que os dois existem.
7. Renomeie `teste.txt` para `final.txt`.

### Exercício 3 — Estrutura de diretórios

1. No seu diretório de trabalho (`/workspaces/<nome-do-repositorio>`), crie a seguinte estrutura com **um único comando** (pesquise sobre `mkdir -p`):

```
SO2025/
├── laboratorios/
│   └── lab01/
├── projetos/
└── anotacoes/
```

2. Navegue pela estrutura de diretórios na seguinte ordem:
   - Use um **caminho absoluto** para ir até `laboratorios/lab01/`.
   - Use um **caminho relativo** para ir de `lab01/` até `projetos/`.
   - Use `cd -` para alternar entre os dois últimos diretórios visitados e terminar em `laboratorios/lab01/`.

3. **Sem sair de `laboratorios/lab01/`**, crie:
   - Um arquivo chamado `ideias.txt` dentro de `projetos/`.
   - Um arquivo chamado `comandos.md` dentro de `anotacoes/`.

4. Volte para `SO2025/` e use o comando `find` com diferentes flags para:
   - Listar apenas os diretórios dentro da estrutura.
   - Encontrar apenas os arquivos com extensão `.txt`.

5. Use o comando `echo` com redirecionamento de saída (`>>`) para adicionar conteúdo ao arquivo `anotacoes/comandos.md` sem abrir um editor. Adicione a descrição de pelo menos 3 comandos que você usou durante o laboratório. Exemplo de como o conteúdo do arquivo deve ficar:

```
## Comandos Uteis

cd - : navega para o diretorio anterior
pwd : mostra o diretorio atual
find : busca arquivos e diretorios com base em criterios
```

---

## Entrega

Ao final dos exercícios, você deve ter dois arquivos de entrega dentro de `/workspaces/<nome-do-repositorio>`:

| Arquivo | Descrição |
|---|---|
| `LAB1SO_<SEU_RA>.txt` | Gravação da sessão do terminal (gerado pelo `script`) |
| `SO2025/anotacoes/comandos.md` | Arquivo com a descrição dos comandos (Exercício 3.5) |

Certifique-se de que a gravação foi encerrada (comando `exit` no `script`) antes de prosseguir.

### Enviando pelo Git

No terminal, execute os comandos abaixo na ordem indicada. Eles adicionam seus arquivos ao repositório e enviam para o GitHub:

```bash
# 1. Volte para o diretório de trabalho (raiz do repositório)
cd /workspaces/<nome-do-repositorio>

# 2. Adicione todos os arquivos modificados e criados
git add .

# 3. Crie um registro (commit) com uma mensagem descritiva
git commit -m "Entrega Lab 01 - <SEU_RA>"

# 4. Envie para o GitHub
git push
```

Para confirmar que a entrega foi realizada, acesse seu repositório no GitHub pelo navegador e verifique se os arquivos aparecem lá.

---
