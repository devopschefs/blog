---
layout: post
title:  "Azure resource manager service endpoint no VSTS"
date:   2017-04-26 08:00:00 +0530
categories: cloud
author: "Alex Giannotti"
---

Oi Pessoas!

A um tempo atrás eu estava tentando configurar um Service Endpoint para conectar o Azure da empresa em que trabalho com o meu VSTS, embora essa tarefa pareça fácil não foi tão simples assim realizar essa tarefa já que eu sou administrador do VSTS mas não do Azure da empresa. Qual o problema nisso? Bom, para que eu pudesse ter as informações que eu precisava para adicionar um Azure Resource Manager service endpoint no VSTS, eu precisaria depender de alguém que tivesse o acesso ou eu precisaria arrumar outra forma de consegui-los. Foi ai que me deparei com uma documentação da Microsoft que vou explicar aqui com mais detalhes (link no fim do post).

Adicionando o Service Endpoint
Quando entramos na página do VSTS para conectarmos um service endpoint nos deparamos com a seguinte tela:

 

Endpoint

 

Para conectar uma conta do Azure ao VSTS teremos duas opções, “Azure Classic” e “Azure Resource Manager”. Pois bem, qual a diferença entre as duas? A opção “Azure Classic” vai conectar o seu VSTS ao seu Azure no portal antigo, ou seja, na arquitetura “ASM” do Azure. Já a opção “Azure Resource Manager” vai conectar o seu VSTS ao seu Azure no portal novo, ou seja, na arquitetura “ARM” do Azure. A primeira opção está sendo substituída pela segunda gradualmente pela Microsoft, então é uma recomendação que você migre as suas coisas para o novo portal.

Voltando para o VSTS, ao clicar na opção “Azure Resource Manager” vamos ver a seguinte tela:

 

Resource Manager Connection

 

Se no seu caso o seu VSTS estiver conectado em um Azure, ou seja, você tiver adicionado a sua conta lá ou tiver criado ela a partir do Azure, a sua subscription irá aparecer nesta tela e você só terá que adicionar um nome a conexão. No meu caso o meu VSTS não tem relação alguma com o Azure da empresa em que trabalho, mas mesmo assim eu precisava que os dois se comunicassem para que eu pudesse fazer um release em um WebSite.

Repare que nesta tela acima na última frase que aparece está escrito, “If your subscription is not listed above, or your account is not backed by Azure Active Directory or to specify an existing Service Principal click here”, ou seja, se não há uma relação de confiança entre o VSTS e o Azure em questão clique no link para mais opções. Ao clicar neste link mencionado vamos ver a seguinte tela:

 

Resource Manager Connection 2

 

Connection Name: Neste campo você só precisa adicionar um nome qualquer para a conexão que estamos fazendo.
Environment: Se você está em qualquer região que não seja o governo dos EUA, China ou Alemanha, deixe a opção default acima “Azure Cloud”.
Subscription ID: Essa informação você vai encontrar facilmente em seu Azure, na parte da sua subscription mesmo.
Subscription Name: Essa informação estará junto com a Subscription ID.
Service Principal Client ID / Service Principal Key / Tenant ID: Essas informações não são encontradas facilmente no Azure e principalmente se não sabemos onde procurar fica mais difícil ainda de encontrar. Siga a leitura para ver como eu resolvi essa questão…
Como eu resolvi o problema
Lendo a documentação da Microsoft eu encontrei o seguinte script, aqui. Executando ele em meu powershell ISE eu obtive todas as informações de que precisava para a conexão com o Azure. Veja a imagem abaixo:

 

Resultado Script Azure

 

É importante saber que para executar o script que mencionei acima se faz necessário importar o módulo “AzureRM” em seu powershell, para isso basta executar o comando “Install-Module AzureRM” no powershell. Para saber mais sobre esse módulo clique aqui.

Ao final do script, como mostra acima, você encontrará todas as informações que vai precisar para preencher a tela do VSTS. Após preencher clique em “Verify Connection” e se o símbolo ao lado ficar verde é só clicar em “Ok” e você já estará pronto para utilizar o seu Azure em seu VSTS. Veja a imagem abaixo para uma melhor visualização do que eu disse.

 

Resource Manager Connection 3

Mais uma vez, espero ter ajudado vocês! Até o próximo post! Abraços!

Alex Giannotti

Fonte: https://www.visualstudio.com/en-us/docs/build/concepts/library/service-endpoints#sep-azure-rm