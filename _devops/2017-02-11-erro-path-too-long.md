---
layout: post
title:  "Erro Path Too Long no Build VNext Agent? E agora?"
date:   2017-02-11 08:00:00 +0530
categories: devops
author: "Alex Giannotti"
---

Oi Pessoas!!!

Erro Path Too Long no Build VNext Agent? E agora??? Se você se deparou com um erro igual ou parecido com o abaixo, calma! Não arranque seus cabelos ainda! Leia o post antes…

“Error : The specified path, file name, or both are too long. The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters.”

Primeiro você precisa verificar se o seu serviço está ativo ou parado, caso esteja ativo o pare. Agora precisamos copiar alguns arquivos para a nova pasta do agente de build. Crie uma pasta nova, com o menor número possível de caracteres direto na raiz do seu disco. Por exemplo: “C:\agent”

Vá até a pasta onde os arquivos do seu agente atual está e as copie para o novo path que acabamos de criar. A pasta deverá ficar da seguinte forma:

Erro Path Too Long no Build VNext Agent?
 

Agora precisamos alterar o arquivo “settings.json” (repare na imagem acima) com o caminho novo. Abra o arquivo em seu editor preferido e altere os caminhos conforme a imagem abaixo:

Erro Path Too Long no Build VNext Agent?
 

Precisamos alterar o “RootFolder” e o “WorkFolder”, deixe o resto do arquivo como está, o salve e feche o editor.

Agora precisamos nos certificar que o serviço está apontando para a nova pasta também. Entre na tela de serviços da máquina do agente de build e ache o seu serviço:

Erro Path Too Long no Build VNext Agent?
 

Clique com o botão esquerdo no seu serviço e vá na opção “propriedades”. A tela abaixo irá abrir:

Erro Path Too Long no Build VNext Agent?
 

Repare no caminho que está em “Path to executable”, repare que o caminho que está lá é o caminho antigo ainda.

Agora para alterar esse caminho você deve abrir um command prompt como administrador e executar o comando abaixo:

Erro Path Too Long no Build VNext Agent?
 

“sc config <service name> binPath= <Path to executable>”

Você deve substituir o “service name” pelo nome do serviço (esse valor está nas propriedades do seu serviço) e o “Path to executable” pelo novo caminho para o arquivo “VsoAgentService.exe” que está dentro da pasta “agent”.

Erro Path Too Long no Build VNext Agent?
 

Esse comando irá alterar o registrykey do serviço do agente de build na máquina. Eu não recomento alterar esses valores na mão, mas se tiver segurança em fazê-lo vá em frente.

Agora só precisamos reconfigurar o serviço do agente e ele deverá funcionar como antes. Abra o command prompt como administrador, entre na pasta nova do agente e execute o “ConfigureAgent.cmd” que deverá estar na raiz da pasta do agente. Siga os passos e reconfigure o seu agente, após terminado ele voltará a funcionar como antes.

Espero ter ajudado vocês!

Abraços!

Alex Giannotti