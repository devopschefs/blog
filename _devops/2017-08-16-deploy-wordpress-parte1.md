---
layout: post
title:  "Configurando o deploy do Wordpress - Parte 1"
date:   2017-08-16 08:00:00 +0530
categories: devops
author: "Alex Giannotti"
---

Oi Pessoas!

Hoje venho trazer para vocês como podemos configurar o nosso ambiente para a automação de deploy do WordPress – parte 1, então continuem acompanhando. Essa necessidade apareceu para mim, pois quero automatizar a publicação deste blog com um novo tema, customizado por mim. Em breve estarei disponibilizando o novo tema em produção. Aguardem! Então vamos ver como eu estou configurando a automação de deploy do wordpress aqui.

Bom, para trabalhar com a automatização do deploy do site WordPress o mínimo que irão precisar na máquina de vocês é o PHP e o WP-CLI instalados. Há também como instalar o WordPress e o WP-CLI via uma ferramenta chamada Composer, mas veremos isso em outro post.

Instalando o PHP
Isso pode parecer simples para quem já tem ou teve contato com o PHP antes, mas para alguém novo pode não ser. O que precisamos fazer é, na verdade, bem simples. Precisamos apenas fazer o download da versão que preferirmos, descompactá-la no HD e aponta-la no path.

Download do PHP
No próprio site do PHP podemos encontrar todas as versões que podemos ter, para o download clique aqui.

Descompactando o “.zip”
Como a imagem abaixo mostra, podemos simplesmente descompactar o conteúdo do zip do passo anterior diretamente em uma pasta na raiz do HD.

php-folder

Adicionando o PHP no path
Após descompactar o PHP no seu HD você pode adicioná-lo ao path do sistema, como mostra a imagem abaixo.



Para se certificar que o PHP está funcionando como deveria, você pode executar o comando “php -version” no powershell ou outro comand line de preferência. Veja a imagem abaixo.

Configurando a Automação de Deploy do WordPress

Instalando o WP-CLI
Como eu tenho um SO Windows no meu computador, vou estar falando como instalar o WP-CLI nele, mas caso precisem instalar em outro SO podem verificar as opções aqui.

Antes de continuar, certifique-se que você seguiu os passos acima para a instalação do PHP, sem ele o WP-CLI não irá funcionar corretamente. Faça o download do “wp-cli.phar”, aqui, crie uma pasta na raiz do seu HD com o nome “wp-cli” e coloque o arquivo .phar dentro. Veja a imagem a seguir.

wp-cli-phar

Agora, crie um arquivo chamado “wp.bat”, dentro da pasta que você acabou de criar acima, e insira o código a seguir nele.

 @ECHO OFF
php "c:/wp-cli/wp-cli.phar" %*
A pasta acima deve ficar com os dois arquivos dentro dela. Veja a imagem a seguir.

wp-cli-floder

Para finalizar, adicione a pasta “wp-cli” no path do seu sistema também. Veja a imagem a seguir.

Configurando a Automação de Deploy do WordPress

Pronto! Agora temos o nosso ambiente pronto para automatizar o processo de deploy do WordPress em nossa máquina ou na VM de Build, claro. 🙂

Para continuar acompanhando o restante dos posts relacionados e este, clique aqui.

Até o próximo post! Abraços!

Alex Giannotti