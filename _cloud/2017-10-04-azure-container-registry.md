---
layout: post
title:  "Azure container registry"
date:   2017-10-04 08:00:00 +0530
categories: cloud
author: "Alex Giannotti"
---

Oi Pessoas!

Hoje vou explicar para vocês como funciona e para que serve o Azure Container Registry. Bom, um container registry serve para você poder guardar e gerenciar as suas imagens dos containers docker em um lugar privado, neste caso no Azure.

Como Funciona
Primeiro de tudo será necessário criar um container registry em sua conta Azure. Se não souber como faz isso, você pode entrar neste link onde você terá acesso a documentação.

Depois de criar o seu Azure Container Registry você pode começar a salvar as suas imagens. Para isso siga os passos abaixo:

Logue na sua conta
“docker login <login server>”
Azure Container Registry

Para achar o login server, observe a imagem abaixo:



Para achar o Login e Senha, observe a imagem abaixo:

Azure Container Registry

Suba uma imagem para o seu Azure Container Registry
Primeiro, você deve ter uma imagem docker na sua máquina. Para isso use o comando “docker pull <nome da imagem>” para baixar uma da Docker Store.
Assim que já tiver uma imagem na sua máquina você pode usar o comando abaixo para colocar uma Tag na sua imagem com o login server do seu Container Registry.
“docker tag <nome da imagem base> <login server>/<nome da sua imagem>”

Azure Container Registry

Agora é só subir a sua imagem com o comando abaixo.
“docker push <login server>/<nome da sua imagem>”

Azure Container Registry

Pronto! Sua imagem estará salva e privada para que você possa utilizá-la como quiser.

Azure Container Registry

Até o próximo post! Abraços!

Alex Giannotti