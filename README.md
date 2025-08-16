# Tutorial Completo: Git no Windows (com VS Code)

**Versão usada nos exemplos:** Git 2.49.0 (x64)  
**Público-alvo:** iniciantes e intermediários  
**Pré-requisitos:** Windows 10/11, internet, privilégios para instalar programas

---

## Sumário
1. [Baixar e instalar o Git e VS Code no Windows](#1-baixar-e-instalar-o-git-e-vs-code-no-windows)  
2. [Configuração inicial do Git](#2-configuração-inicial-do-git)  
3. [Criando e iniciando um repositório (VS Code)](#3-criando-e-iniciando-um-repositório-vs-code)  
4. [Criar arquivos e commit inicial (VS Code)](#4-criar-arquivos-e-commit-inicial-vs-code)  
5. [Trabalhando com branches (VS Code)](#5-trabalhando-com-branches-vs-code)  
6. [Criando e resolvendo conflitos no terminal](#6-criando-e-resolvendo-conflitos-no-terminal)  
7. [Criando e resolvendo conflitos no VS Code](#7-criando-e-resolvendo-conflitos-no-vs-code)  
8. [Visualizando histórico de commits no VS Code](#8-visualizando-histórico-de-commits-no-vs-code)  
9. [Clonando repositório via VS Code](#9-clonando-repositório-via-vs-code)  
10. [Sincronizando com GitHub pelo VS Code](#10-sincronizando-com-github-pelo-vs-code)  
11. [Dicas rápidas e comandos úteis](#11-dicas-rápidas-e-comandos-úteis)  
12. [Glossário rápido (opcional)](#12-glossário-rápido-opcional)  
13. [Como substituir as imagens de exemplo](#13-como-substituir-as-imagens-de-exemplo)  
14. [Licença](#14-licença)

---

## 1. Baixar e instalar o Git e VS Code no Windows

### 1.1 Git
1. Acesse: <https://git-scm.com/downloads>  
2. Clique em **Download for Windows** e execute o instalador.  
3. Siga a instalação padrão (**Next → Next → Finish**).  
4. Verifique no **Git Bash** ou **Prompt**:

```bash
git --version
# Exemplo de saída esperada:
# git version 2.49.0.windows.1
```
Figura 1 — Página oficial do Git (botão “Download for Windows”)
![Figura 1 — Git download](docs/images/fig1-git-download.png)

1.2 Visual Studio Code (VS Code)

Acesse: https://code.visualstudio.com/download

Baixe a versão para Windows e instale.

Abra o VS Code e confira Help → About (opcional).

Figura 2 — Página oficial do VS Code (botão “Download for Windows”)
![Figura 2 — VS Code download](docs/images/fig2-vscode-download.png)

>Observação: O VS Code já inclui integração com Git e tem extensões úteis como Git Graph e GitLens.

2. Configuração inicial do Git

Defina seu nome e e-mail (essas informações aparecem nos commits):

```sh
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@email.com"
git config --list
```


Figura 3 — Git Bash: configurando nome e e-mail
![Figura 3 — Git config](docs/images/fig3-git-config.png)

> [!NOTE]
>--global aplica a todos os repositórios do seu usuário.
>--local (executado dentro de um repositório) sobrescreve o global apenas para aquele projeto.

3. Criando e iniciando um repositório (VS Code)

No Windows Explorer, crie a pasta desenvolvimento e dentro dela exemplo1.

Abra o VS Code → File → Open Folder… → selecione exemplo1.

Abra o terminal integrado (`Ctrl + ``) e execute:

```sh
git init
```

Figura 4 — VS Code: File → Open Folder (Explorer com pasta exemplo1)
![Figura 4 — Open Folder](docs/images/fig4-vscode-open-folder.png)

Figura 5 — VS Code: Terminal integrado após git init
![Figura 5 — git init](docs/images/fig5-git-init.png)

>Isso cria a pasta oculta .git no diretório, iniciando o repositório.
