---
layout: post
title:  "Start automático dos agentes de build ao reiniciar"
date:   2017-10-18 08:00:00 +0530
categories: devops
author: "Alex Giannotti"
---

Oi Pessoas!

Essa semana a equipe de infraestrutura do meu cliente me questionou se não teria alguma forma de fazermos o start automático dos agentes de build ao reiniciar os servidores de build. Antes que alguém pense porque eu simplesmente não instalei os meus agentes como serviço no servidor, me deixe explicar. Por limitações de um dos projetos do cliente tive que instalar 2 agentes iterativos, e todas as vezes que reiniciamos a máquina de build tenho que entrar lá e iniciá-los manualmente.

Primeiro pensei em fazer um arquivo “.bat” para solucionar o meu problema, mas ao pensar na melhor forma de fazer isso me deparei com uma solução bastante simples e fácil de se implementar. Acompanhe! 🙂

Pasta “Startup”
Você deve conhecer ou pelo menos já ouviu falar em uma pasta chamada “Startup” do Windows, certo? Se nunca ouviu falar nela faça o passo a passo abaixo que você a encontrará facilmente.

Digite as teclas “Widows + R”, para abrir o “Run” do Windows.
No “Run” digite “shell:startup”.
A pasta “Startup” do Windows irá abrir automaticamente.


OU
Entre na pasta “C:\Users\<SEU-USUARIO>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup”.
start automático dos agentes de build ao reiniciar

Essa pasta é lida pelo Windows todas as vezes que ligamos nosso computador e ele inicia todos os shortcuts que estejam nela automaticamente. Pois bem, porque não colocar um shortcut para o nosso agente de build lá também? Foi exatamente isso que eu fiz! Veja!

O Shortcut
Crie um shortcut para o arquivo “run.cmd” do seu agente. Este arquivo estará localizado na pasta do seu agente.

start automático dos agentes de build ao reiniciar

Agora, basta você copiar esse shortcut para a pasta “startup”, que vimos acima, que o sistema operacional Windows se encarregará de executar o seu agente todas as vezes que a sua máquina for religada.

start automático dos agentes de build ao reiniciar

Espero ter ajudado! Até o próximo post!

Alex Giannotti