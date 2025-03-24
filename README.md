
# Dio | Resumos Git e GitHub

Repositorio para armazenar resumos sobre Git e GitHub do curso de Versionamento de Código com Git e GitHub da DIO (Digital Innovation One).

## 💻 Resumo das Aulas 

### CRIANDO UM RESPOSITORIO

Para criar um repositorio siga o passo a passo abaixo:

1️⃣Criar uma nova pasta e entrat nela 
```
mkdir repo-local
cd repo-local/
```
- mkdir repo-local cria uma pasta chamada repo-local.

- cd repo-local/ entra nessa pasta.


2️⃣Inicializar um repositório Git 
```
git init
```
- Cria um repositório Git vazio dentro da pasta repo-local.


3️⃣ Verificar os arquivos ocultos para confirmar a criação do repositório
```
ls -a
```
- O ls -a mostra arquivos ocultos, incluindo a pasta .git, que armazena o histórico do repositório.

### CLONANDO UM REPOSITORIO

Agoara se você precisa clonar um repositorio siga o passo a passo abaixo:

1️⃣Clonar um repositório remoto corretamente
```
git clone https://github.com/livsXC/DP-100.git
Clona o repositório remoto DP-100 para a pasta repo-local/DP-100.
```
- Se quiser escolher um nome diferente para a pasta do clone, use:
```
git clone https://github.com/livsXC/DP-100.git repo-clonado
```
- Isso cria uma pasta chamada repo-clonado com o conteúdo do repositório.


5️⃣ Configurar um repositório remoto no repositório local
```
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
```
- O git remote add origin define a origem do repositório remoto.

Substitua seu-usuario/seu-repositorio.git pela URL do seu repositório no GitHub.


6️⃣ Verificar se o repositório remoto foi adicionado corretamente
```
git remote -v
```
- Exibe a URL do repositório remoto configurado.

### SALVANDO AS ALTERAÇÕES 

Aqui está um passo a passo para salvar as alterações no repositório local usando Git:

1️⃣ Criar ou modificar arquivos no repositório
Se ainda não houver arquivos, crie um novo:
```
echo "Meu primeiro arquivo no Git" > arquivo.txt
Isso cria um arquivo chamado arquivo.txt com um texto dentro.
```
- Se já houver arquivos, basta editá-los com qualquer editor de texto.

2️⃣ Verificar o status do repositório
Antes de salvar as alterações, veja quais arquivos foram modificados:
```
git status
```
- Isso mostrará os arquivos que foram criados, modificados ou removidos.


3️⃣ Adicionar os arquivos ao controle do Git
Para salvar alterações de um arquivo específico
```
git add arquivo.txt
```
- Para adicionar todos os arquivos modificados de uma vez:
```
git add .
```
- Isso prepara os arquivos para serem salvos no histórico do Git.


4️⃣ Criar um commit (salvar as alterações no histórico)
Depois de adicionar os arquivos, crie um commit com uma mensagem explicando a alteração:
```
git commit -m "Adicionando meu primeiro arquivo"
```
- Isso registra a alteração no histórico do Git.

5️⃣ Verificar o histórico de commits (opcional)
Para ver os commits feitos até agora:
```
git log --oneline
```
- Isso mostra os commits com um resumo.

## Desafazendo Alterações

1️⃣ Desfazer alterações em arquivos não adicionados ao Git (git add)
Se você fez modificações, mas ainda não rodou git add, pode simplesmente descartar as alterações com:
```
git checkout -- nome-do-arquivo
```
- Ou, para desfazer todas as alterações em arquivos não adicionados:
```
git checkout -- .
```
- ⚠️ Isso remove todas as mudanças feitas nos arquivos sem salvá-las.


2️⃣ Desfazer git add antes do commit
Se você adicionou um arquivo ao staging area (usou git add), mas ainda não fez o commit, use:
```
git reset nome-do-arquivo
```
- Para remover todos os arquivos adicionados:
```
git reset
```
- Isso os tira do staging, mas mantém as alterações no arquivo.


3️⃣ Desfazer um commit local (antes do push)
- Se você já fez um commit, mas ainda não enviou para o GitHub, pode desfazê-lo:

Para manter as alterações no código, mas remover o commit:
```
git reset --soft HEAD~1
```
- Para remover o commit e as alterações do código:
```
git reset --hard HEAD~1
```
- ⚠️ O segundo comando apaga as mudanças do código, então use com cuidado!

4️⃣ Desfazer um commit já enviado para o GitHub
- Se você já fez um git push, mas quer desfazer o commit, use:
```
git revert HEAD
```
- Isso cria um novo commit que desfaz o anterior, mantendo o histórico seguro.


# 🔎Referencias

Dio {https://web.dio.me/track/microsoft-certification-challenge-dp-100}

Eliadina {https://github.com/elidianaandrade/dio-curso-git-github}
