# <h1 align="center"><font color = #119fbf>Git e GitHub</font></h1>
Neste repositório estou compartilhando algumas anotações para a consulta sobre os principais comandos do GIT.

<div align="center"><img src='https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png' style='width: 50%;'></div>

## Sobre 
Git é um sistema de versionamento de código que guarda os registros de versão como estado do projeto, além da referência para os registros

## Estados do git
**1. Unmodified:** Arquivo já está mapeado pelo GIT, ou seja, já passou pelo staged e já foi "commitado". Todas as alterações foram salvas;

**2. Modified:** Arquivos que foram modificados;

**3. Staged:** Área preparatória para realizar o commit;

**4. Untracked:** Estado inicial;

<div align="center"><img src='https://github.com/andressagomes26/git-commands/assets/60404990/653b4a3b-d415-43f2-911e-0a2b013ed18c'></div>

## Configurando o Git
⭐ ```git init```: Inicia um repositório GIT;

⭐ ```git config --global user.name "Nome"```: Configurando o nome do usuário;

⭐ ```git config --global user.email "name@gmail.com"```: Configurando o email do usuário;

⭐  ```git clone```: Clonar repositório GIT;

## Comandos Básicos
⭐ ```git status```: Exibe informações sobre o status, por exemplo, qual a branch atual, se a branch está atualizada de acordo com o repositório remoto. Mostra qual arquivo foi modificado e se há mudanças para ser commitadas;

⭐ ```git add```: Adiciona as modificações para a área staged.

- ```git add .```: Adiciona todos os aquivos;
  
- ```git add nome_arquivo```: Adiciona apenas o arquivo passado.
