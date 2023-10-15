# <h1 align="center"><font color = #119fbf>Git e GitHub</font></h1>
Neste repositório estou compartilhando algumas anotações para a consulta sobre os principais comandos do GIT.

<div align="center"><img src='https://media.licdn.com/dms/image/C4D12AQGXkZf6DJB9kA/article-cover_image-shrink_600_2000/0/1625492357429?e=2147483647&v=beta&t=Za25mgxxiTJH1l0K34GrCEsktnjfn2p_onibFuL2Z0Y' style='width: 50%;'></div>
<!--div align="center"><img src='https://storage.googleapis.com/workover/courses/banners/93388ff2b17bf2c8b3cf1c780c23d120.png' style='width: 50%;'></div-->
                    
## Sobre 
Git é um sistema de versionamento de código que guarda os registros de versão como estado do projeto, além da referência para os registros

## Estados do git
**1. Unmodified:** Arquivo já está mapeado pelo GIT, ou seja, já passou pelo staged e já foi "commitado". Todas as alterações foram salvas;

**2. Modified:** Arquivos que foram modificados;

**3. Staged:** Área preparatória para realizar o commit;

**4. Untracked:** Estado inicial, ou seja, o git ainda não conhece nenhuma versão da existência do arquivo;

<div align="center"><img src='https://github.com/andressagomes26/git-commands/assets/60404990/653b4a3b-d415-43f2-911e-0a2b013ed18c'></div>

## Configurando o Git
⭐ ```git init```: Inicia um repositório GIT;

⭐ ```git config --global user.name "Nome"```: Configurando o nome do usuário;

⭐ ```git config --global user.email "name@gmail.com"```: Configurando o email do usuário;

⭐  ```git clone```: Clonar repositório GIT.

## Comandos Básicos
⭐ ```git status```: Exibe informações sobre o status, por exemplo, qual a branch atual, se a branch está atualizada em relação ao repositório remoto, mostra qual arquivo foi modificado e se há mudanças para ser commitadas;

⭐ ```git diff```: Exibe as linhas de código modificada;

-  ```git diff --staged```: Exibe as linhas de código modificadas dos arquivos em staged.
  
⭐ ```git add```: Adiciona as modificações para a área staged;

- ```git add .```: Adiciona todos os aquivos;
  
- ```git add nome_arquivo```: Adiciona apenas o arquivo passado.

⭐ ```git commit -m "mensagem"```: Commit das alterações para salvar o estado do projeto;

⭐ ```git log```: Exibe um histórico dos últimos commits;

⭐ ```git restore .\README.md```: Remover as modificações de um arquivo;

- ```git restore --staged .\README.md```: Remover as modificações de um arquivo da área de staged (ou seja, após o git add) para modified;

## Repositórios Remotos

⭐ ```git remote```: Verificar as informações do respositório remoto;

⭐ ```git push```: Enviar commits locais para um repositório remoto;

⭐ ```git push origin master```: Enviar as alterações para a branch master do repositório remoto origin;
  - *origin*: Repositório remoto;
  - *master*: Branch;
  - ```git push --set-upstream origin master```: O ```--set-upstream ``` ou ```-u``` indica que está sendo configurando o branch local atual (por exemplo, "main" ou "master") para rastrear o branch "master" no repositório remoto (origin). Isso significa que, no futuro, ao usar o git push, o Git saberá para onde enviar as atualizações sem a necessidade de especificar origin master.
    
⭐ ```git pull```: Trazer as alterações do repositório remoto fazendo um merge no repositório local;

⭐ ```git fetch```: Verificar quais alterações serão feitas ao usar o ```git pull```;
- ```git diff origin/master```: Verificar as alterações no repositório origin e branch master.

## Trabalhando com Branchs

⭐ ```git branch```: Verificar as branchs que existem e qual a branch atual;

⭐ ```git branch name_branch```: Criar uma nova branch;

⭐ ```git log --oneline --decorate```: Indica para onde o head está apontando;

⭐ ```git checkout name_branch2```: Ir para uma nova branch;

⭐ ```git checkout -b name_branch3```:  Criar uma nova branch e já ir para ela;

⭐ ```git merge development```: Faz o merge das alterações existentes na branch 'development' com a branch atual 'master';

## Referências

✅ [Ada Tech - Let's Code](https://comunidade.ada.tech/cursos/37f4b5d2-dbab-4c45-ab61-aac1ba2c7d19)

✅ [Git e Github para iniciantes](https://www.udemy.com/course/git-e-github-para-iniciantes/)


### Contato
- Andressa Gomes Moreira - andressagomesm26@gmail.com




