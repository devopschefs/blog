---
layout: post
title:  "Configurando task groups no VSTS"
date:   2017-08-23 08:00:00 +0530
categories: devops
author: "Alex Giannotti"
---

Oi Pessoas!

Hoje vamos falar sobre uma funcionalidade chamada Task Groups no VSTS. Essa funcionalidade foi criada para agruparmos tasks que serão utilizadas em várias definições de Build e/ou Release, sem termos que configurar todos os passos novamente, facilitando ainda mais o processo de construção da definição.

Criando Tasks Groups
Para chegar no menu onde construímos as Task Groups no VSTS, vá em “Build & Release” e lá estará o menu “Task Groups”. Veja a imagem abaixo.

Configurando Task Groups no VSTS

Uma vez nesta tela você conseguirá ver as Task Groups já criadas e terá a opção de editar elas, entre outras coisas que já vamos ver. Veja a imagem abaixo.

Configurando Task Groups no VSTS

No meu caso não tenho nenhuma Task Group criada ainda. Então, como podemos criar novas Task Groups? Bom, basta ir em uma definição de Build ou Release, selecionar as tasks que deseja incluir na Task Group, clicar com o botão direito e verá a opção, como mostram as imagens abaixo.

Configurando Task Groups no VSTS

Configurando Task Groups no VSTS

Após a seleção da opção para criar a Task Group no Build e/ou Release, uma tela irá abrir e você poderá preencher os detalhes da nova Task Group que você está criando. Depois você verá que as tasks selecionadas serão substituídas por uma única task. Veja as imagens abaixo.

Configurando Task Groups no VSTS

Configurando Task Groups no VSTS

Configurando Task Groups no VSTS

Configurando Task Groups no VSTS

Agora que já criamos as Tasks Groups vamos ver como gerenciá-las no menu “Tasks Groups”.

Gerenciando as Tasks Groups
Configurando Task Groups no VSTS

Properties –  Aqui você conseguirá editar as configurações básicas da Task Group e poderá colocar uma descrição para cada variável adicionada às tasks.

Tasks – Aqui você poderá adicionar, remover e editar cada uma das tasks da Task Group. Eu aconselho a colocarem o máximo de variáveis possível nelas. Assim quando importar uma Tasks Group nas definições de Build e Release ficará mais fácil de preencher tudo o que precisa.

History – Nesse menu você poderá ver todo o histórico de alterações feitas na Task Group.

References – Esta é a funcionalidade mais bacana, que eu acho, nesta tela, onde vocês vão poder verificar onde a Task Group em questão está sendo utilizada. (acreditem, antes desta opção existir eu controlava quais Task Groups eram utilizadas em quais Builds ou Releases em uma planilha excel. Era realmente difícil de mantê-la atualizada!)

OBS: Também é possível adicionar uma Task Group dentro de outra Task Group. Por isso nesta última tela há a opção Task Groups.

OBS2: O menu “References” foi lançado em uma das últimas releases no VSTS e na minha opinião ajudou muito a minha vida e provavelmente a de outras pessoas que utilizam muito as Tasks Groups nos projetos.

Caso queira saber mais sobre como utilizar as Tasks Groups, clique aqui, e você poderá acessar a documentação completa da Microsoft sobre essa funcionalidade do VSTS.

Até o próximo post! Abraços!

Alex Giannotti