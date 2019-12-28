# Comandos Git
## Lista com os principais comandos usados no Git
### Iniciando
* git config --global user.name "vinicius": **seta seu nome no Git**
* git config --global user.email "*vinicius@vinicius.com*": **seta seu email no Git**
* git config user.name: **retorna o nome que foi setado no Git**
* git config user.email: **retorna o email que foi setado no Git**
* git version: **retorna a versão**

### Primeiro commit
* git init: **inicia um repositório local**
* git add *: **adiciona todos os arquivos do projeto ao container**
* git add .: **adiciona todos os arquivos do projeto ao container**
* git add *nome do arquivo*: **adiciona o arquivo ao container**
* git commit -m "alterei o arquivo vinicius.txt": **adiciona o container ao repositório local juntamente com a mensagem digitada**
* git diff: **mostra as linhas que foram alteradas de cada arquivo. Funciona apenas antes de commitar**
* git status: **mostra os arquivos que foram alterados e os comandos para desfazer essas alterações**

### Logs e grafo de commits
* git log: **mostra os logs do commits realizados**
* git log --oneline: **mostra de uma maneira mais simples os logs do commits realizados**
* git log --graph: **mostra os logs no grafo de commits**
* git log --oneline --graph: **mostra apenas os logs do grafo de commits nos nodos**
* git log --oneline --graph --all: **mostra os logs de todas as ramificações do projeto e nao apenas a que o projeto se encontra**

### Controle de versões
* git checkout 3r421ew: **retorna o projeto para a versão desejada, sendo os caracteres devem ser referentes hash de cada versão do projeto. Este comando não deleta as versões mais recentes, ele apenas retorna o projeto para a versão desejada**
* git checkout master: **retorna o projeto para a sua última versão**
* git reset --hard er321td: **deleta um commit. A hash informada deve ser da versão em que o projeto deve se encontrar e não da versão que deve ser excluída, assim ele retornará para a versão desejada e excluirá as subsequentes**

### Ramificações
* git branch: **identifica o ramo em que o projeto se encontra**
* git checkout -b meuRamo: **cria um novo ramo, o qual sempre herdará os commits anteriores**
* git checkout meuRamo: **muda o projeto de ramificação**
* git merge meuRamo: **esse comando une o meuRamo ao ramo master. Para executar tal precisamos estar no ramo master**

### Copiar repositório local para o GitHub
* git remote: **verifica se já existe um repositório remoto**
* git remote -v: **mostra os datalhes do repositório remoto, caso ele exista**
* git remote add origin link: **adiciona um repositório remoto. Cada repositório terá seu link único**
* git push -u origin master: **empurra os dados do repositório local para o repositório remoto**

### Copiar repositório remoto para o repositório local
* git clone: **Faz uma cópia do repositório remoto em nossa máquina. Cada repositório terá seu link único**

### Conflitos entre reposotório local e remoto
git fetch: **faz o download das alterações no repositório remoto sem altera nada no local**
git checkout origin: **muda para o ramo origin, que é o novo ramo que o comando *git fetch* cria, podendo assim ser possível visualizar as inconsistências entre os dois repositórios.**
git pull: **uma vez resolvidos os conflitos, esse comando faz um merge nas duas remificações**
