Adicionando um ReadMe.md

Segue aqui os principais comandos Git a serem usados:

Para criação/primeiras modificações:

    echo "# My-Project" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/rafaelfortunat/My-Project.git
    git push -u origin main

Push em repositório, e outras modificações:

    git remote add origin https://github.com/rafaelfortunat/My-Project.git
    git branch -M main
    git push -u origin main

    

Segue aqui outros comandos, possivelmente úteis no futuro:

    git init → inicializa um repositório Git vazio na pasta atual.

    git status → exibe o estado atual do repositório (arquivos modificados, em staging ou não rastreados).

    git add → adiciona arquivos à staging area, preparando-os para o commit.
    Ex.: git add . adiciona todos os arquivos.

    git commit → grava as alterações versionadas no histórico do Git com uma mensagem descritiva.

    git log → mostra o histórico de commits do projeto.

    git diff → exibe as diferenças entre versões dos arquivos (antes do commit).

    git branch → lista, cria ou remove branches do repositório.

    git checkout → muda de branch ou restaura arquivos (comando mais antigo).

    git switch → alterna entre branches de forma mais segura e moderna.

    git merge → une uma branch à branch atual.

    git rebase → reaplica commits sobre outra base, reorganizando o histórico.

    git remote → gerencia repositórios remotos (ex.: adicionar, listar ou remover origin).

    git fetch → baixa atualizações do repositório remoto sem alterar o código local.

    git pull → busca e integra alterações do remoto no repositório local.

    git push → envia commits do repositório local para o repositório remoto.

    git reset → desfaz commits ou remove arquivos da staging area (pode perder alterações).

    git revert → desfaz um commit criando um novo commit de reversão (não altera histórico).

    git clean → remove arquivos não rastreados do diretório de trabalho.

    git clone → cria uma cópia local de um repositório remoto existente.