# <h1 align="center"><font color = #119fbf>Git e GitHub</font></h1>
Neste repositório estou compartilhando algumas anotações para a consulta sobre os principais comandos do GIT.

<!--div align="center"><img src='https://media.licdn.com/dms/image/C4D12AQGXkZf6DJB9kA/article-cover_image-shrink_600_2000/0/1625492357429?e=2147483647&v=beta&t=Za25mgxxiTJH1l0K34GrCEsktnjfn2p_onibFuL2Z0Y' style='width: 50%;'></div>
<div align="center"><img src='https://storage.googleapis.com/workover/courses/banners/93388ff2b17bf2c8b3cf1c780c23d120.png' style='width: 50%;'></div>
<div align="center"><img src='https://media.licdn.com/dms/image/D4D12AQHE7UE23B_hOg/article-cover_image-shrink_720_1280/0/1683080824955?e=2147483647&v=beta&t=Ykjy6NhzQTinufBmJV0H8syHEPv2R8Wj7sziWTa5NTs' style='width: 50%;'></div-->
<div align="center"><img src='https://hermes.dio.me/articles/cover/d2489f96-d56f-4b82-bc7f-84fbc9fb1368.jpg' style='width: 50%;'></div>

## Sobre 
Git é um sistema de versionamento de código que guarda os registros de versão como estado do projeto, além da referência para os registros

## Estados do git
**1. Unmodified:** Arquivo já está mapeado pelo GIT, ou seja, já passou pelo staged e já foi "commitado". Todas as alterações foram salvas;

**2. Modified:** Arquivos que foram modificados;

**3. Staged:** Área preparatória para realizar o commit;

**4. Untracked:** Estado inicial, ou seja, o git ainda não conhece nenhuma versão da existência do arquivo;

<div align="center"><img src='https://github.com/andressagomes26/git-commands/assets/60404990/f94610c3-140b-4ccc-8992-59c78591f2a8'></div>

## Configurando o Git
⭐ ```git init```: Inicia um repositório GIT;

⭐ ```git config --global user.name "Nome"```: Configurando o nome do usuário;

⭐ ```git config --global user.email "name@gmail.com"```: Configurando o email do usuário;

⭐  ```git clone```: Clonar repositório GIT.

## Comandos Básicos
⭐ ```git status```: Exibe informações sobre o status, por exemplo, qual a branch atual, se a branch está atualizada em relação ao repositório remoto, mostra qual arquivo foi modificado e se há mudanças para ser commitadas;

⭐ ```git diff```: Exibe as linhas de código modificadas;

-  ```git diff --staged```: Exibe as linhas de código modificadas dos arquivos em staged.
  
⭐ ```git add```: Adiciona as modificações para a área staged;

- ```git add .```: Adiciona todos os aquivos;
  
- ```git add nome_arquivo```: Adiciona apenas o arquivo passado.

⭐ ```git commit -m "mensagem"```: Commit das alterações para salvar o estado do projeto;

⭐ ```git log```: Exibe um histórico dos últimos commits;

 - ```git log --author:"Andressa"```: Exibe um histórico dos últimos commits desse autor;

 - ```git log --graph```: Exibe um histórico dos últimos commits de forma gráfica;
   
## Repositórios Remotos

⭐ ```git remote```: Verificar as informações do respositório remoto;

⭐ ```git remote add origin git@github.com:andressagomesm26/git-commands.git```: Adicionar um repositório remoto (origin) à configuração do repositório git local.

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

⭐ ```git branch -a```: Listar todas as branches disponíveis, incluindo as remotas

⭐ ```git branch name_branch```: Criar uma nova branch;

⭐ ```git log --oneline --decorate```: Indica para onde o head está apontando;

⭐ ```git checkout name_branch2```: Ir para uma nova branch;

⭐ ```git checkout -b name_branch3```:  Criar uma nova branch e já ir para ela;

⭐ ```git branch -D name_branch```: Apagar uma branch.

⭐ ```git merge development```: Faz o merge das alterações existentes na branch 'development' com a branch atual 'master';

## Desfazendo Mudanças 
⭐ ```git restore .\README.md```: Remover as modificações de um arquivo;

- ```git restore --staged .\README.md```: Remover as modificações de um arquivo da área de staged (ou seja, após o git add) para modified;

⭐ ```git reset HEAD .\README.md```: Remover um arquivo modificado da área de staged;

- ```git reset --soft HEAD```: Volta um arquivo para área de staged após ele ser commitado, deixando-as prontas para serem incluídas no próximo commit;
- ```git reset --mixed HEAD```: Volta um arquivo para área de modified após ele ser commitado;
- ```git reset --hard HEAD```: Ignora a existência do commit

#  Git Flow
O Git Flow é um modelo ou um fluxo de trabalho muito utilizado por equipes de desenvolvimento de software. É recomendado para projetos que utilizam versionamento semântico ou que precisam oferecer suporte a várias versões de seu software.

<div align="center"><img src='https://blog.haposoft.com/content/images/2021/06/git-flow-logo-1.png'  style='width: 50%;'></div>

## Funcionamento
O Git Flow trabalha com duas branches principais, a Develop e a Master e três branches de suporte, Feature, Release e Hotfix, que são temporários e duram até realizar o merge com as branches principais. É ideal que todos os commits na branch Master sejam marcados com um número de versão.

📌 **Master:** Onde temos todo o código de produção;
  
📌 **Develop:** Onde fica o código do próximo deploy. Possui funcionalidades que ainda não foram publicadas e que posteriormente vão ser associadas com a branch Master.
  
📌 **Feature:** São branches utilizadas para o desenvolvimento de funcionalidades específicas. É recomendável que essas branches sigam uma convenção de nome, por exemplo, “feature/desenvolvimento-forum”. Essas features branches são criadas sempre a partir da branch Develop.
  
📌 **Hotflix:** É uma branch criada a partir da master para realizar correções imediatas encontradas no sistema em produção.
  
📌 **Release**: A Branch Release serve como ponte para fazer o merge da Develop para a Master. Ela funciona como ambiente de homologação e é removida após realizar os testes do merge com a Master. Caso seja encontrado algum bug e haja alguma alteração, ela também deve ser sincronizada com a Develop.

<div align="center"><img src='https://www.alura.com.br/artigos/assets/git-flow-o-que-e-como-quando-utilizar/imagem3.png'  style='width: 50%;'></div>

## Implementação   

⭐ ```git flow init```: Inicia o git flow;

⭐ ```git flow feature start name_feature```: Cria uma nova branch feature => 'feature/name_feature';

⭐ ```git flow feature finish name_feature```: Finaliza a branch feature fazendo um merge com a develop;

⭐ ```git flow release start 1.0```: Cria uma nova branch release => 'release/1.0';

⭐ ```git flow release finish 1.0```: Finaliza a branch release. Atualiza a master e develop e cria uma tag;

⭐ ```git flow hotfix start 1.1```: Cria uma nova branch hotfix a partir da master => 'hotflix/1.1';

⭐ ```git flow hotfix finish name_hotfix```: Finaliza a branch hotfix. Atualiza a develop e cria uma tag.

## Referências

✅ [Ada Tech - Let's Code](https://comunidade.ada.tech/cursos/37f4b5d2-dbab-4c45-ab61-aac1ba2c7d19)

✅ [Git e Github para iniciantes](https://www.udemy.com/course/git-e-github-para-iniciantes/)

✅ [Git Flow: entenda o que é, como e quando utilizar](https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar)

✅ [Trabalhando em equipe com Git Flow](https://www.youtube.com/watch?v=394mc6PV8t8&t=1063s)

### Contato
- Andressa Gomes Moreira - andressagomesm26@gmail.com




