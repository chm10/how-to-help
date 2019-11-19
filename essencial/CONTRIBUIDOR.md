# Seja um Contribuidor!

Se você chegou até está etapa então já tem seu ambiente todo configurado e preparado para contribuir! 


Primeiro ache um projeto de interesse. Faça fork dele para separar uma cópia do projeto para seu espaço.

## Github 

Faça fork. 

![img](/imgs/fork.gif)

Terminado o fork é possível baixar de várias maneira um projeto. Utilizando http ou ssh ou por zip ou usar programa do github. 


* Https: Comando utilizado no terminal para baixar o projeto é mais fácil de utilizar. Toda vez que fizer upload da contribuição o terminal vai perguntar seu login e senha o que pode ser chato.

* Ssh: Comando utilizado no terminal para baixar o projeto é mais chato de configurar. Mas toda vez que fizer upload da contribuição o terminal não pedira mais login.

* Zip: Mais fácil, mas precisa configurar várias coisas.

## Git

Vá no menu inicial.

Abra terminal do git (bash).

Digite este comando para criar uma pasta com nome myProject ou altere e crie um nome que desejar.

```
mkdir myProject
```

Digite este comando para entrar no novo diretório.

```
cd myProject
```

### Configuração do seu usuário

Antes de continuar, verifique se configurou sua conta do github e nome de usuário no Git local. Ela é utilizada para mostrar quem fez a contribuição no Github. 

Exemplo:

```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

Primeiro associa o seu nome e o segundo associa seu e-mail.

Configure uma chave SSH. Essa chave é utilizada  para autentar seu git ao Github sem precisar digitar o login e a senha.

Gere uma chave  [seguindo este tutorial](https://git-scm.com/book/pt-br/v1/Git-no-Servidor-Gerando-Sua-Chave-P%C3%BAblica-SSH).

Para voltar a pasta do projeto digite `cd` e arraste o diretório do projeto até o terminal isso fará que ele irá autocompletar o caminho até o diretório.

![tips](/imgs/path.gif)

## Baixando repositório

Baixe um repositório. Escolha a opção por meio do SSH.

```
git clone git@github.com:chm10/cpm-joao-XXIII.git
```

Entre na pasta do projeto
```
cd <nome da pasta do projeto>
```

Digite esse comando. 
```
git remote
```

Saída será...
```
Origin
```

Origin é a referencia para repositório do dono no Github é preciso fazer Pull Request para conseguir inserir uma contribuição.


Adicione então o repositório que você deu fork nessa lista. (Lembre-se que é aquela cópia do repositório do dono no seu Github)

```
git remote add upstream <link do repositório que você tem acesso>
```

Quando utilizar `git remote` irá parecer agora.

```
origin
upstream
```

Você associará ao seu repositório. 

```
git fetch upstream
```

## Boas práticas de contribuição

Geralmente um projeto tem branch master. Linha do tempo oficial do projeto. branch development para inserção de novas features. Cria-se branch do master para arrumar bugs e do development para inserir um novo recurso. 

### Use tag e release para representar um lançamento. 

Versão oficial | novos recursos | fix bug

A primeira versão poderia ser 1.0.0. Indentifica-se um bug e atualizam o software. A versão passaria a ser 1.0.1. Adicionado um novo recurso seria lançada 1.1.0. E assim por diante. O lançamento de uma release bem grande geralmente faz a mudança do 1.1.0 para 2.0.0. Recomeçando o processo. 

Você pode nomear seus release com um nome por meio da tag.

### Crie um branch
```
git checkout -b <nome da branch>
``` 

Para trocar entre branch use `git checkout <nome da branch>`.


