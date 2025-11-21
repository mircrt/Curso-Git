# toda vez que iniciar um novo repositoriao usar
git init

# parar sair de um comando git
q

# para adicionar tudo "."
git add . 
git add --all

# para adicionar somente um arquivo  index.html 

git add index.html 
git add *.js
git add arquivo1.txt arquivo2.js pasta/

# para adicionar somente uma pasta

git add "nome da pasta"/
git add  img/

# Verificar o status de adição
git status

# fazer commit com comentario
git commit -m "Descrição das alterações"

# fazer uma verigificar dos log
git log

# fazer uma verigificar dos log modo graph
git log --graph

# fazer uma verigificar dos log modo oneline
git log --oneline

# veridicar o que foi modificado
git diff 
git diff --cached

# criar arquivo .gitignore e colocar dentro os nome dos arquivos e diretorios ignoraods
# comocar no diretorio doda pasrta do progeto raiz
.gitignore

info.txt
logo/


# desfazer alterações no local antes do git add.
git restore indefex.html

# restaurar oq ue esta no state
git restore --staged <file>
git restore --staged  indefex.html


# aleralção reset apos add e commit - desfaz o comit quantos forem HEAD~
git reset --soft HEAD~1 -> coloca um til ants do 1 "~1"


# os status que podem ser apresentados

Untracked: arquivo existe mais o git ignora. Não rastreado
Staged: O arquivo já foi adicionado "git add ." 
Committed: Arquiv ja az aprte do historico gi commit
Modified: Indica alteração no arquvi apos o commit

# Ciclo de vida do arquivo
Modificações "Untracked"
Working Dir ->  git add.
 "Staged"
Staging Dir -> git commit
"Committed"
Head ->  se modificar de posi do comit
"Modified"


# fazer todas as modificações de uma vez
git commit -m 'mensgem' --all


# comando --help
git log --help


#  posiçãoe de restauro
git restore  -> do local
git restore --staged ->  do staging para o local
git reset --soft HEAD~1 -> do commit para staging


# renomer arquvio tem que esta adicionado antes de renomear
git add .
git mv info2.txt info22.txt

# quando quero remover um git add . caso tenha deletado algum arquivo faço um apdate
git add -u 

deletar um arquivo que esteja  no staging
git rm intos2.txt

# reseta todo o conteudo
git reset 


# visualizar mais infroamções do commit
# usar o commit 54b25a5bd57a5e0457d6052dadfa5f9d0e8af2fe do git log
git show 54b25a5bd57a5e0457d6052dadfa5f9d0e8af2fe



# manipular BRANCHES
# saida poder acontecer de ser 'master' ou 'main'
git branch

# crir nova branch
git branch novabranch

# mudar de branch 
git checkout novabranch

# excluir uma branch  -d ou -D 'força excluir'
git branch -d master 

# trabalhar com MERGE juntar 2 BRANCH gerar conflitos
# juntar BRANCH corrente "A" com a BRANCH "B" nivela as duas BRANCH no mesmo patamar
git checkout A
git merge B


# USAR O GITHUB
# Verificar se tem algum repositori remoto ja configurado
git remote -v


# adicionar um remote repositorio
git remote add origin https://github.com/mircrt/Curso-Git.git -> exempo isso muda conforme o repositorio

# mandar para o repositorio remoto
git branch -M main -> confirmar o branch 
git push -u origin main -> enviar
git push --force origin main


# publicar ja tudo configurado
git push


1. Clone (Primeira vez)

Se é a primeira vez que está baixando o repositório:
bash

git clone https://github.com/usuario/repositorio.git

2. Pull (Atualizações)

Se já tem o repositório local e quer atualizar com as mudanças mais recentes:
bash

git pull origin main

Ou, se a branch for diferente:
bash

git pull origin nome-da-branch

3. Pull com rebase

Para integrar as mudanças de forma mais limpa:
bash

git pull --rebase origin main

4. Verificar status

Antes de fazer pull, pode verificar o status:
bash

git status
git fetch  # Verifica mudanças sem aplicar

5. Configurar upstream (se necessário)

Se a branch local não está rastreando a remota:
bash

git branch --set-upstream-to=origin/main main