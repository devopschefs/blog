---
title:  "Instalando o Sharepoint 2013 quando a porta SQL não é a padrão"
date:   2017-02-11 08:00:00 +0530
categories: more
author: "Alex Giannotti"
---

Oi Pessoas!

Instalando SharePoint 2013 quando a porta SQL não é a padrão? Bom, tive esse problema ao instalar um SharePoint 2013 em um servidor em que o SQL foi configurado na porta 1633 (que não é a padrão). Diferente do TFS o SharePoint não reconhece se colocarmos o “nome do servidor,a porta do SQL”. Então como podemos fazer para o SharePoint reconhecer o servidor do SQL sem esse problema? Simples! Colocamos um Alias para esse SQL! Se o computador for 64 bits coloque o Alias no SQL Native Client Configuration 32 e 64 bits, ok. Abaixo segue o passo a passo da resolução…

Primeiro entre no SQL Server Configuration Manager do servidor do SharePoint:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

Agora selecione a aba “SQL Native Client 11.0 Configuration (32bit)”:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

Dentro dessa opção selecione “Aliases”:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

A pasta de Aliases vai estar vazia, mas se você clicar com o botão direito do mouse aparecerá a opção “New Alias”. Selecione essa opção e a tela abaixo deverá aparecer:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

Instalando SharePoint 2013 quando a porta SQL não é a padrão?

 

Preencha as opções de acordo com as informações que você precisa e clique em apply e depois em Ok.

A tela deverá ficar assim:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

Faça a mesma coisa na aba “SQL Native 11.0 Configuration”, se o servidor for 64bits:

Instalando SharePoint 2013 quando a porta SQL não é a padrão?
 

Depois volte na instalação do SharePoint e coloque o nome do seu Alias no lugar do nome do servidor. Ao fazer o “test” ele vai reconhecer o servidor e sua porta SQL.

Abraços!

Alex Giannotti