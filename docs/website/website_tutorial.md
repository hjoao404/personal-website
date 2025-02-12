## Introdução
Criar um website pode parecer complicado, mas, na verdade, é possível fazê-lo sem saber programar. O objetivo deste guia é explicar como construí o meu website, passo a passo, através da ferramenta MkDocs.

!!! warning "Importante"

    Este conteúdo é baseado na documentação oficial do MkDocs e do MkDocs Material. Pode ser que, quando estiveres a ler isto, esta página esteja desatualizada. Recomendo sempre consultar a documentação oficial do [MkDocs](https://www.mkdocs.org/getting-started/) e do [MkDocs Material](https://squidfunk.github.io/mkdocs-material/getting-started/) para obter informações mais recentes.

## Passo 1: Escolher uma Ferramenta para Criar o Website
Existem muitas formas de criar um website, desde plataformas como Wix ou WordPress, até ferramentas mais técnicas como MkDocs. Eu escolhi o MkDocs Material porque:

* É simples de usar;

* Permite escrever o conteúdo em Markdown;

* Gera automaticamente um website estático bem estruturado;

* Oferece um design moderno e personalizável.

No entanto, não é por eu usar esta ferramenta que deves usá-la também. Este guia está focado no MkDocs, por isso todos os passos apresentados baseiam-se nele. Existem muitas ferramentas interessantes para a construção de websites, e se não achas que o MkDocs é para ti, recomendo que explores outras opções.

Se procuras algo que te permita manter notas organizadas e bem apresentadas, MkDocs é uma excelente opção.

## Passo 2: Instalar os Pré-Requisitos
Antes de começar, é necessário ter o Python instalado, pois o MkDocs é uma ferramenta baseada em Python.

??? question "O que é o Python?"

    Python é uma linguagem de programação muito utilizada para automação, desenvolvimento web e ciência de dados. É necessário para correr o MkDocs no teu computador.

1. Faz download do Python em [python.org](https://www.python.org/) e instala-o.
2. Durante a instalação, certifica-te de que a opção "Add Python to PATH" está selecionada.
3. Para confirmar a instalação, abre um terminal e escreve:
``` py
python --version
```
ou, em alguns sistemas:
``` py
python3 --version
```
4. O pip já vem incluído com o Python, mas podes atualizá-lo com:
``` py
python -m pip install --upgrade pip
```
??? question "O que é o pip?"

    O pip é o gestor de pacotes do Python. Ele permite instalar e gerir bibliotecas e ferramentas desenvolvidas para Python. Vamos utilizá-lo para instalar o MkDocs e outras dependências.

## Passo 3: Criar o Projeto MkDocs
Agora que o Python e o pip estão instalados, podemos criar o nosso website. Como já mencionado, o tema que eu utilizo neste website é o Material. Podes explorar mais temas neste [link](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes), mas depois terás que ver a documentação associado ao tema escolhido.

1. Abre o terminal na pasta onde queres que o website seja criado.
2. Instalar o MkDocs e o tema Material:
``` py
pip install mkdocs-material
```
3. Criar uma nova pasta para o projeto e iniciar o MkDocs:
``` py
mkdir meu-site
cd meu-site
mkdocs new .
```
4. Para ver o website localmente:
``` py
mkdocs serve
```

Depois, basta abrir um navegador e ir para [http://127.0.0.1:8000/](http://127.0.0.1:8000/).
??? question "O que é http://127.0.0.1:8000/?"

    Este endereço representa o localhost, ou seja, o teu próprio computador. O número 127.0.0.1 é um endereço IP especial que sempre aponta para o dispositivo onde estás a executar o servidor. O 8000 é a porta onde o MkDocs está a servir o website. Sempre que quiseres visualizar o teu site localmente, basta aceder a este [link](http://127.0.0.1:8000/) enquanto o comando mkdocs serve estiver a correr.

## Passo 4: Escolher um Editor de Texto
Para editar os ficheiros do website, precisas de um editor de texto adequado.
??? question "O que é um Editor de Texto?"

    Um editor de texto é uma ferramenta que permite escrever e modificar código ou documentos. Alguns dos mais populares são: Visual Studio Code (VS Code), Sublime Text, Notepad++ ou até o Notepad padrão do teu computador.

Eu utilizo o VS Code porque tem funcionalidades como auto-completar e integração com GitHub. Como não vamos "programar", qualquer coisa dá.

## Passo 5: Personalizar o Website
Agora que o website básico está a funcionar, é possível personalizá-lo editando o ficheiro mkdocs.yml. Por exemplo, para mudar o nome do site:
``` yml
site_name: hjoao
```
Para adicionar uma nova página ao website, basta criar um ficheiro .md dentro da pasta docs. O nome do ficheiro será o nome da página no site. Por exemplo:

1. Criar um ficheiro chamado novapagina.md dentro da pasta docs.
2. Escrever o conteúdo da página em Markdown. Exemplo:
``` md
# Título da Página

Este é o conteúdo da minha nova página.
```
3. Para que a página apareça no menu do site, adiciona-a ao ficheiro mkdocs.yml na secção nav:
``` yml
nav:
  - Home: index.md
  - Nova Página: novapagina.md
```

Lembra-te de que o MkDocs utiliza Markdown, uma linguagem de formatação simples. Se não estás familiarizado com Markdown, podes consultar este [guia de Markdown](https://www.markdownguide.org/) e usar um [preview online](https://markdownlivepreview.com/) para testar o teu conteúdo antes de adicioná-lo ao site.

Podemos também modificar cores, fontes e navegação. A melhor maneira de saber o que se pode, e como fazer é através da [documentação](https://squidfunk.github.io/mkdocs-material/setup/).

## Passo 6: Publicar o Website

Esta é a parte mais complicada para quem nunca trabalhou com Git e GitHub, mas vou explicar tudo passo a passo.

### Instalar o Git

??? question "O que é o git?"

    Git é um sistema de controlo de versões que permite guardar e gerir o histórico de alterações do teu projeto. Ele facilita a colaboração e permite reverter mudanças, caso algo corra mal.

1. Faz download do Git em [git-scm.com](https://git-scm.com) e instala-o.
2. Para confirmar a instalação, abre o terminal e escreve:
``` git
git --version
```

### Criar uma Conta no GitHub

??? question "O que é o GitHub?"

    GitHub é uma plataforma online que permite armazenar repositórios Git na nuvem. Vamos usá-lo para hospedar o nosso website com GitHub Pages.

1. Acede a [github.com](https://github.com) e cria uma conta gratuita.
2. Depois de criar a conta, inicia sessão.

### Criar o repositório no GitHub

1. Clica no botão "New" (Criar novo repositório).
2. Dá um nome ao repositório, por exemplo, my-website.
3. Escolhe "Public" (público). Privado é uma opção importante para se ter em conta, mas para o GitHub pages funcionar, esta opção tem que estar em "Public".
4. Não seleciones nenhuma opção extra (README, .gitignore, etc.).

### Criar um Personal Access Token no GitHub

??? question "O que é o PAT?"

    Um Personal Access Token (PAT) é necessário porque o GitHub descontinuou o suporte para autenticação com senha ao usar a API e a linha de comando (CLI). Isso significa que, para interagir com repositórios privados ou realizar ações autenticadas (coisa que iremos fazer nos próximos passos), precisas de um PAT em vez de uma senha tradicional.

1. Vai a GitHub → Settings → Developer settings.
2. Clica em "Personal access tokens" → "Fine-grained tokens" → "Generate new token".
3. Em "Repository access", escolhe "Only select repositories" e seleciona o repositório que criaste.
4. Em "Permissions", define:
    * Contents → Read and write
    * Workflows → Read and write
5. Clica em "Generate token" e copia o PAT (guarda-o num local seguro, pois não podes vê-lo novamente).

### Conectar a tua Pasta Local ao Repositório do GitHub

1. No teu PC inicializa um repositório Git na pasta do teu projeto MkDocs:
``` git
git init
git add .
git commit -m "Primeira versão do Website"
```
Um commit guarda as alterações feitas no repositório. Sempre que deres um commit, a mensagem deve descrever claramente as mudanças realizadas.
2. Estabelece a ligação ao repositório remoto
``` git
git branch -M main
git remote add origin https://github.com/teu-username/teu-rep.git
git push -u origin main
```
O link do "remote add origin" encontras na página do repositório.
3. Quando pedirem o username, escreve o teu nome de utilizador do GitHub.
4. Quando pedirem a password, cola o PAT que geraste (não vais ver os caracteres ao colar, mas ele está lá).
Se tudo correr bem, o código será enviado para o GitHub. Consegues verificar isto ao abrir o teu repositório.

### Criar o workflow de deploy

Agora precisamos de criar um ficheiro que vai automatizar o deploy do MkDocs sempre que fizeres um git push.

1. No teu projeto, cria a seguinte pasta:
``` cmd
mkdir -p .github/workflows
```
2. Dentro dessa pasta, cria um ficheiro chamado ci.yml:
``` cmd
touch .github/workflows/ci.yml
```
3. Abre o ficheiro ci.yml e cola o seguinte código:
``` yml
name: ci 
on:
  push:
    branches:
      - master 
      - main
permissions:
  contents: write
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Configure Git Credentials
        run: |
          git config user.name github-actions[bot]
          git config user.email 41898282+github-actions[bot]@users.noreply.github.com
      - uses: actions/setup-python@v5
        with:
          python-version: 3.x
      - run: echo "cache_id=$(date --utc '+%V')" >> $GITHUB_ENV 
      - uses: actions/cache@v4
        with:
          key: mkdocs-material-${{ env.cache_id }}
          path: .cache
          restore-keys: |
            mkdocs-material-
      - run: pip install mkdocs-material 
      - run: mkdocs gh-deploy --force
```
Este código é encontrado na documentação do [MkDocs Material](https://squidfunk.github.io/mkdocs-material/publishing-your-site/).

4. Guarda o ficheiro e faz commit novamente:
``` git
git add .github/workflows/ci.yml
git commit -m "Adiciona GitHub Actions para deploy automático"
git push
```

### Configurar o GitHub Pages

Agora que o código já está no GitHub, vamos garantir que o site seja automaticamente publicado usando o GitHub Pages.

1. Vai até ao GitHub e abre o repositório.
2. Clica em Settings (em cima à direita do repositório).
3. No menu lateral, vai a Pages.
4. Em Source, escolhe a branch gh-pages (vai ser criada automaticamente) e clica em Save.

O GitHub Pages vai agora começar a construir o teu site.

### Verificar e Atualizar o teu site

O site vai ficar disponível em: https://teu-username.github.io/teu-rep/

Agora, para atualizar o site automaticamente sempre que fizeres alterações, basta seguir este processo:

1. Faz as alterações no conteúdo do teu site localmente.
2. Adiciona as alterações ao Git:
``` git
git add .
git commit -m "Mensagem sobre a alteração"
```
3. Faz o push para o GitHub:
``` git
git push origin main
```

Depois de fazeres o push, o site será atualizado automaticamente, geralmente em poucos minutos. É simples e qualquer alteração que faças localmente será automaticamente refletida no site sem precisares de fazer mais nada.