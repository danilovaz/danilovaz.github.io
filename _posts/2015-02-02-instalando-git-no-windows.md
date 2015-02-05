---
layout: post
title: Instalando Git no Windows
feature-img: "img/tela-azul-windows.png"
---

Antes que me crucifiquem, esse post tem o intuito nobre de ajudar um amigo a migrar do desenvolvimento "desktop" pra desenvolvimento web, que é onde ele tem mais interesse e por isso vou dar um help no que eu puder passar do pouco que sei.

Enquanto ele não providencia um Linux ou um Mac :p vamos de ~~Ruindows~~ Windows mesmo.

## Instalando Git no Windows

Para a surpresa geral da nação, instalar o Git no Windows é muito fácil. Basta acessar o site do [MsysGit](http://msysgit.github.io/), baixar o Git SCM, instalar o `.exe` e ser feliz (até onde é possível com Windows).

## Usando Git no Windows

Ao instalar o Git, você terá duas formas de utilizá-lo: Git GUI e Git BASH.

O Git GUI nada mais é do que uma interface gráfica "bonitinha" onde tudo que você precisa fazer é clicar e clicar e clicar.

Particularmente, eu prefiro utilizar o prompt de comando (terminal, bash, whatever). Considero ser mais prático e rápido. Mas gosto é igual, você sabe, cada um tem o seu.

Já que para esse post, o intuito é nortear um caminho para meu amigo aprender de uma maneira mais correta o que a web tem de melhor, vou utilizar exemplos partindo do BASH.

## Configurando Git

A primeira coisa a se fazer após instalar o Git, é configurar sua identidade para que o Git possa identificar você e suas ações/requisições.

Para isso, abra o Git BASH e defina seu username"

```
$ git config --global user.name "José das Couves"
```

Após configurar seu username, vamos configurar o seu e-mail (deve ser o mesmo que você se cadastrou no [Github](http://github.com))

```
$ git config --global user.email josecouves@couves.com.br
```

Pronto, seu Git está configurado. Mas por via das dúvidas rode o seguinte comando para verificar se suas informações estão corretas:

```
$ git config --list
```

Por hoje é só isso, foi um post curto e simples apenas para mostrar como instalar Git no Windows e utilizá-lo pelo prompt de comando.

Esse é o primeiro post de uma série sobre Git, no qual vou ensinar do básico até algumas dicas mais avançadas para quem ainda não conhece Git.

Sem mais delongas, inté!

>"Mostre-me teu código que te digo quem tu és."
> - Danilo Vaz
