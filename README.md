# <div align="center"> Comandos Avançados  :memo: ​ </div>

<div align="center"> <img alt="GitHub forks" src="https://img.shields.io/github/forks/tayhsn/git-advanced?logoColor=red&style=social"> <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/tayhsn/git-advanced?logoColor=orange&style=social"> </div>

### Comandos que vão elevar sua performace com Git :octocat:

Você pode copiar esse repositório para o seu perfil com FORK ou salvá-lo com uma STAR. :sparkles:

<hr>

### Reset

​	```git reset -- [SOFT / MIXED / HARD] [HASH / HEAD] ``` 

Esse comando reseta as alterações salvas no commit, e suas variações são:

-- soft: reseta o commit e retorna a **stagging área/index**

--mixed: reseta o commit e retorna **ao working directory** (opção padrão)

--hard: reseta o commit e **descarta as alterações**

<hr>

### Revert

​	```git revert [HASH / HEAD] ```

Com esse comando, o git como inverte as alterações salvas pelo commit e cria um novo commit com o conteúdo resultante.

> Exemplo: Você faz o primeiro commit "C1", e depois faz um segundo commit "C2" alterando uma linha.  
>
> Se você usar o comando para reverter "C2", o git descarta a alteração da linha e cria um novo commit com o que estava no "C1". A mensagem padrão do commit criado pelo revert é "Revert commit HASH".
>
> Se você usar o comando para reverter "C1", o git descarta o arquivo pois anteriormente a esse commit o arquivo não existia.

<hr>

### Stash

​	```git stash [save "contexto"] [list] [pop index] [clear] ```

Esse comando salva temporariamente os commits na branch em que foram feitos, evitando assim que ao mudar de branch, os arquivos commitados se movam com você. 

**Os commits são salvos em um array e acessados através do índice.**

> Exemplo: Se você commitar arquivos na branch feature e precisar ir pra branch main, eles irão se mover junto com você, e se você commitar e versionar arquivos da branch main, os arquivos que você trouxe serão versionados junto. O stash previne esse problema.

<u>git stash:</u> salva o commit com uma mensagem padrão.

<u>save "contexto"</u> : salva o commit com uma mensagem contextualizada (fortemente indicado!).

<u>list</u>: lista todos os commits salvos.

<u>pop index</u>: remove o commit da área de stash, sendo acessado atráves do índice

<u>clear</u>: remove todos os commits salvos.

<hr>

### Log

​	```git log [dir] [arquivo] -- [oneline / graph] ```

Esse comando permite visualizar o log (informações) de commits de variadas maneiras, as mais comuns são:

<u>dir</u>: visualiza todos os commits de um diretório/pasta especifico.

<u>arquivo</u>: visualiza todos os commits de um arquivo especifico.

--oneline: visualiza hash e titulo do commit em uma linha única

--graph: acrescenta a árvore de commits na visualização.

**Para sair do log: Q + ENTER**

<hr>

### Commit

​	```git commit ```

Esse comando permite escrever o commit no editor de texto padrão, assim você pode acrescentar além do titulo (header), o corpo (body) e o rodapé (footer).

Título: Será a primeira linha, não pode ultrapassar 50 caracteres, seja direto e conciso.

-- é necessário inserir uma quebra de linha-- 

Corpo: Será a segunda linha, não tem limite de caracteres, explique bem qual o propósito desse commit. 

-- é necessário inserir uma quebra de linha-- 

Rodapé (opcional): Será a terceira linha, e aqui pode você fazer referência a issues ou pull requests.

> Exemplo: 
>
> Rodapé: Closes #1 Ref #123 -> Este commit encerra a issue #1 e faz referência ao pull request #123

<hr>

Sobre a estrutura dos commits:

- Os comandos que tem " -- " antes são propriedades que mudam o comportamento do comando, esses são chamados de flags.
- Os comandos dentro de " [ ] " são atributos do mesmo tipo. Não é necessário utilizar todos.
- Os comandos em " [ ] " diferentes são atributos de tipos diferentes. Não é necessário utilizar todos.
- HASH é o identificador do commit, e se parece com: "097cf90577316b0271b807acf22def39c92421a8" 
- HEAD é a cabeça, ou seja, a ponta ou o último commit válido, você pode se guiar pela cabeça utilizando HEAD~1

<hr>

Documentação oficial: https://git-scm.com/docs

Git Command Explorer: https://gitexplorer.com/
