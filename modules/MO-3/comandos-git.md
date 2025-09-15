## 🔧 Configuração

- git config --global user.name "Seu Nome" → define o nome do autor dos commits.

- git config --global user.email "seu@email.com" → define o e-mail do autor.

- git config --list → mostra as configurações atuais do Git.


## 📂 Iniciando um repositório

- git init → cria um novo repositório Git na pasta atual.

- git clone <url> → baixa um repositório remoto para sua máquina.


## 📊 Status e histórico

- git status → mostra o estado dos arquivos (modificados, prontos para commit, etc.).

- git log → exibe o histórico de commits.

- git log --oneline --graph --decorate --all → log resumido e visual.

## 📝 Adicionando e confirmando mudanças

- git add <arquivo> → adiciona um arquivo específico à staging area.

- git add . → adiciona todos os arquivos modificados.

- git commit -m "mensagem" → salva as alterações no histórico com uma mensagem.


## 🌿 Trabalhando com branches

- git branch → lista as branches.

- git branch <nome> → cria uma nova branch.

- git checkout <nome> → muda para outra branch.

- git switch <nome> → forma mais moderna de mudar de branch.

- git checkout -b <nome> → cria e muda para a nova branch.

- git merge <branch> → mescla outra branch na atual.


## 🔄 Sincronizando com repositório remoto

- git remote add origin <url> → conecta o repositório local ao remoto.

- git fetch → baixa mudanças do repositório remoto sem aplicar.

- git pull → baixa e aplica as mudanças (fetch + merge).

- git push → envia suas alterações para