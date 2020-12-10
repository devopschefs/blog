---
layout: post
title:  "Você sabe qual a sua versão do PowerShell?"
date:   2017-03-22 08:00:00 +0530
categories: more
author: "Alex Giannotti"
---

Oi Pessoas!

Vocês já se depararam querendo saber a versão do Poweshell no seu servidor e não conseguindo dar um simples “powershell –version” para saber? Pois eu sim! Outro dia em um cliente, eu reparei que a versão do Powershell no meu PC tinha mais comandos que o instalado em meu servidor de build, e para a minha surpresa o comando acima não funcionou… Pois bem, quais são as versões do Powershell… você sabe qual é a sua?

Versões do Powershell
O Powershell tem 5 versões, ao longo dos anos ele foi evoluindo junto com os sistemas operacionais da Microsoft e desde a versão 2.0 podemos ver uma importantíssima ferramenta para os SIS Admins automatizarem uma série de atividades do dia a dia.

Para saber mais da história, diferenças entre as versões e evolução da ferramenta, clique aqui.

Mas… você sabe qual é a sua?
Bom, de forma rápida e prática posso listar abaixo os sistemas operacionais e quais as versões que vem com eles.

Powershell 1.0 – Foi feito para Windows XP SP2, Windows Server 2003 SP1 e Windows Vista. E é um componente opcional para Windows Server 2008.
Powershell 2.0 – Integrado com o Windows 7 e Windows Server 2008 R2. No Windows XP está disponível com o SP3, para o Windows Server 2003 com o SP2, e Windows Vista com o SP1.
Powershell 3.0 – Integrado com o Windows 8 e Windows Server 2012. No Windows 7, Windows Server 2008 e Windows Server 2008 R2 está disponível nos respectivos SP1.
Powershell 4.0 – Integrado com o Windows 8.1 e com o Windows Server 2012 R2. No Windows 7, Windows Server 2008 R2 e Windows Server 2012 está disponível nos respectivos SP1.
Powershell 5.0 – Integrado com o Windows Server 2016 e Windows 10 (no update de aniversário). A compatibilidade com o Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012 e Windows Server 2012 R2 foi lançada em 19 de janeiro de 2017.
Mas, mesmo assim, se você assim como eu quiser descobrir isso via command line, apenas digite a variável “$PSVersionTable” em seu Powershell, como segue na imagem abaixo, e a versão irá aparecer.

 

powershell.version2

Upgrade para o Powershell 5.0
Caso a sua versão não seja a 5.0 faça o upgrade apenas baixando e instalando em seu PC ou servidor o Windows Management Framework 5.o, neste link aqui. Fique atento aos pré-requisitos de sistema e se certifique que o seu PC ou serivdor está de acordo com todos eles.

Saiba mais sobre Powershell
Para saber mais sobre a ferramenta e aprender a automatizar suas tarefas via script veja mais conteúdo no site da Microsoft, aqui.

Até o próximo post! Abraços!

Alex Giannotti