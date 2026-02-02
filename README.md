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

Push em repositório, branch, e outras modificações:

    git remote add origin https://github.com/rafaelfortunat/My-Project.git
    git branch -M main
    git push -u origin main

🔁 Fluxo mental do cenário 1

    *Criar/alterar arquivos
    *git init
    *git status (opcional)
    *git add .
    *git commit -m "first commit"
    *git branch -M main
    
    Arquivo → git init → git add → git commit → git remote → git push

🔁 Fluxo mental do cenário 2
    
    *# edita README.md ou qualquer outro arquivo
    *git status
    *git add .
    *git commit -m "Atualiza README"
    *git push (não precisa do "-u origin main")

    Editar → git add → git commit → git push



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


    FLAGS (SUB-COMANDOS)

🔧 FLAGS GERAIS (aparecem em vários comandos)

    -v / --verbose → exibe mais detalhes da execução do comando.
    Ex.: git remote -v

    -q / --quiet → executa o comando sem quase nenhuma saída no terminal.

    --help → mostra a ajuda do comando.
    Ex.: git commit --help

📂 FLAGS DE ARQUIVOS / STAGING

    -A → adiciona todas as alterações (novos, modificados e removidos).
    Ex.: git add -A

    . (ponto) → adiciona todos os arquivos do diretório atual.
    Ex.: git add .

💾 FLAGS DE COMMIT

    -m "mensagem" → define a mensagem do commit direto no comando.
    Ex.: git commit -m "mensagem"

    --amend → altera o último commit (mensagem ou conteúdo).
    Ex.: git commit --amend

    --no-edit → mantém a mensagem do commit anterior (muito usado com amend).
    Ex.: git commit --amend --no-edit

🌿 FLAGS DE BRANCH

    -b → cria uma nova branch e já muda para ela.
    Ex.: git checkout -b feature-x

    -c → cria uma branch nova (usado com git switch).
    Ex.: git switch -c feature-x

    -d → remove uma branch já mesclada.
    Ex.: git branch -d feature-x

    -D → remove uma branch à força (mesmo não mesclada).
    Ex.: git branch -D feature-x

    -M → renomeia a branch atual forçando o nome.
    Ex.: git branch -M main

🌍 FLAGS DE REMOTO / PUSH / PULL

    -u / --set-upstream → define a branch remota padrão para push/pull futuros.
    Ex.: git push -u origin main

    --force → força a atualização do repositório remoto, sobrescrevendo histórico.
    Ex.: git push --force

    --all → executa a ação para todos os remotes ou branches.
    Ex.: git fetch --all

    --prune → remove referências remotas que não existem mais.
    Ex.: git fetch --prune

🔀 FLAGS DE MERGE / PULL

    --allow-unrelated-histories → permite juntar históricos que não têm ancestral comum.
    Ex.: git pull origin main --allow-unrelated-histories

    --no-ff → força a criação de um commit de merge (sem fast-forward).
    Ex.: git merge feature --no-ff

    --rebase → aplica commits locais sobre o histórico remoto.
    Ex.: git pull --rebase

🧨 FLAGS DE RESET

    --soft → volta commits, mantendo arquivos no staging.
    Ex.: git reset --soft HEAD~1

    --mixed → (padrão) volta commits e remove do staging, mantendo arquivos.
    Ex.: git reset HEAD~1

    --hard → volta commits e apaga alterações dos arquivos.
    Ex.: git reset --hard HEAD~1

🧹 FLAGS DE CLEAN

    -f → força a remoção de arquivos não rastreados.
    Ex.: git clean -f

    -d → remove diretórios não rastreados.
    Ex.: git clean -fd

🔍 FLAGS DE LOG / DIFF

    --oneline → mostra commits resumidos (1 linha por commit).
    Ex.: git log --oneline

    --graph → exibe o gráfico de branches.
    Ex.: git log --graph

    --all → mostra commits de todas as branches.
    Ex.: git log --all

    --staged → mostra diferenças apenas do staging.
    Ex.: git diff --staged