---
layout: post
title:  "Build e Release pipelines concorrentes com VSTS"
date:   2017-05-03 08:00:00 +0530
categories: devops
author: "Alex Giannotti"
---

Oi Pessoas!

Vocês devem ter reparado que o jeito como os pipelines funcionam no VSTS mudou. Então hoje vou explicar para vocês como funciona o novo build e release pipeline com o VSTS e porque que com essas mudanças algumas coisas ficaram melhores do que antes. Vamos ver então como ficou o novo modelo de licenciamento para os build e release pipelines concorrentes com VSTS.

Antes x Depois
Como eu disse mais acima, tudo mudou com relação ao licenciamento dos agentes, antes nós tínhamos que adquirir licenças a partir do segundo agente privado instalado e para cada agente hosted que ultrapassasse mais de 260 minutos (que já tínhamos grátis em nossa conta). Agora, está disponível um modelo em que temos um build e release pipeline e um agente hosted grátis, ou seja, dentro dessa licença grátis do build e release pipeline podemos ter quantos agentes privados quisermos e o agente hosted continua com no máximo 260 minutos grátis.

O que mudou então? Bom, podemos ter vários agentes de build e release instalados em nossos servidores, mas somente um irá realizar o build e/ou o release por vez.

 

Quanto custava x Quanto custa
Os preços para os agentes hosted não foram alterados, continuam R$150,00 cada. Quanto aos agentes privados, também continuam R$56,25 cada (preços calculados em, link).

Preço para os agentes:

AgentesVSTS

Se eu tiver esquecido de algum detalhe importante ou algo não tenha ficado claro, me envie uma mensagem nas redes sociais ou comente aqui embaixo. Até o próximo post! Abraços!

Alex Giannotti

Fontes:

[Concurrent build and release pipelines in VSTS](https://www.visualstudio.com/en-us/docs/build/concepts/licensing/concurrent-pipelines-ts)

[Concurrent release pipelines in Team Foundation Server](https://www.visualstudio.com/en-us/docs/build/concepts/licensing/concurrent-pipelines-tfs)