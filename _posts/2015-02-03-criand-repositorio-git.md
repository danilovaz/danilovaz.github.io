---
layout: post
title: Criando repositório Git
feature-img: "img/github.png"
---

No artigo anterior eu ensinei como [instalar Git no Windows](http://danilovaz.github.io/2015/02/02/instalando-git-no-windows.html). Agora vou ensinar como criar um repositório local e enviá-lo para o Github e começar a fazer o controle de versionamento do seu projeto.


## Criando o repositório local

Para criar um repositório local, acesse o terminal e crie a pasta que vai conter o seu projeto.

```bash
$ cd Documents/User/Projetos

$ mkdir meu-primeiro-repositorio

$ cd meu-primeiro-repositorio
```

Pronto, agora que criou a pasta do seu projeto e está dentro dele, vamos rodar o comando ```git init```

```bash
$ git init
```

Esse comando vai criar em nosso projeto uma pasta invisível chamada .git e criar uma branch para controlar nossos arquivos. Mas até o momento não temos nenhum arquivo sendo controlado, vamos então criar o arquivo README.md que será uma espécial de manual dentro do seu repositório

```bash
$ touch README.md
```

Legal, criamos o arquivo. Agora temos que verificar se esse arquivo está sendo apontado pelo Git como um arquivo que precisa ser incluído em seu Stage para que possa ser commitado.
Para isso, rode o comando

```bash
$ git status
```

Esse comando lista todos os arquivos locais de nosso projeto que: são novos, sofreram modificações ou foram deletados.

Veja que o README.md apareceu como `untracked file`, ou seja, esse arquivo não está sendo controlado pelo Git.

Existem duas formas aqui para que possamos incluir o README.md ao Stage:

```bash
$ git add -A
```

Esse comando adiciona à Stage todos os arquivos novos ou que sofreram modificações. Esse comando requer atenção quando você está trabalhando em um repositório com várias pessoas, pois, pode ser que você coloque na trilha de Stage arquivos que só deviriam ter em sua máquina local. Por isso fique atento e sempre rode ```git status``` para ter certeza dos arquivos que devem ser enviados.

A outra maneira de adicionar arquivos à Stage é adicionando uma por uma "na mão". Dependendo das alterações é trabalhoso, porém mais para frente vou ensinar um comando que facilita a vida. Mas por hora, como vamos adicionar um arquivo só rode

```bash
$ git add README.md
```

Pronto, adicionamos o README.md à Stage. Para verificar se está tudo certo, rode o ```git status``` agora deve ser exibido ```new file``` antes do nome do README.md

Estamos quase no fim. Agora vamos commitar as alterações no repositório para que depois possamos enviar ao servidor. O processo de commit basicamente pega todos os arquivos que você adicionou à Stage e envia para o HEAD que aponta para o último commit do repositório remoto.
Vamos commitar.

```bash
$ git commit -m "Adiciona README.md"
```

Agora vou mostrar um passo que não precisa ser feito sempre, apenas quando criamos o repositório por linha de comando via ```git init```. Quando criamos o repositório direto no Github esse passo pode ser pulado.

```bash
$ git remote add origin https://github.com/username/repo-name.git
```

E por fim, mas não menos importante vamos enviar para o repositório remoto o nosso commit.

```bash
$ git push -u origin master
```

WOW! Parabéns, você criou seu primeiro commit :smiley:

Agora é só você acessar o Github e visualizar seu primeiro repositório!

Fique ligado nos próximos posts.

Sem mais delongas, inté!

>"Mostre-me teu código que te digo quem tu és."
> - Danilo Vaz
