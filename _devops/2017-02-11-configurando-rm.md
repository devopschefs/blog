---
title: "Configurando o Release Mangement"
excerpt: "Release Management fora do domínio"
toc: false
last_modified_at: 2020-12-09
author: Alex Giannotti
header:
  overlay_image: "/assets/images/posts_header/opensslonwindows.jpg"
  overlay_filter: 0.5
  teaser: "/assets/images/posts_header/opensslonwindows.jpg"
show_overlay_excerpt: true
categories:
  - devops
tags:
  - windows
  - openssl

#date:   2017-02-11 08:00:00 +0530
#categories: devops
#author: "Alex Giannotti"
---

Oi Pessoas!!!

Configurando Release Management em um Servidor Fora do Domínio? Bom, a resposta parece e na verdade é mesmo simples, mas se você não prestar atenção aos detalhes você pode se perder. Para solucionar esse problema utilizei shadow accounts.

Vamos lá!

1. Em meu cenário eu tenho:

– Duas VMs com Windows Server 2012 R2 instalados.

– Uma está no domínio de meu cliente (RMServer) e a outra não (RMDeploy).

– Na RMServer eu tenho o Release Management Server e o Release Management Client instalados e configurados.

– Na RMDeploy eu tenho o Release Management Agent instalado (não se preocupe em configura-lo por enquanto).

2. Antes de começarmos vamos criar as contas do usuário “ServerUser” nos dois servidores, o RMServer e o RMDeploy. Adicione os usuários no grupo de administradores em cada um dos servidores e se certifique que as senhas são idênticas.

Configurando Release Management em um Servidor Fora do Domínio?
 

3. Agora crie mais um usuário chamado “DeployUser”, também nos dois servidores, o RMServer e o RMDeploy. Adicione os usuários no grupo de administradores em cada um dos servidores e se certifique que as senhas são idênticas.

Configurando Release Management em um Servidor Fora do Domínio?
 

4. Adicione o usuário “ServerUser” no Release Management, utilizando o RM Client, deixe o usuário configurado nas roles “Release Manager” e “Service User”.

Configurando Release Management em um Servidor Fora do Domínio?
 

5. Adicione o usuário “DeployUser” no Release Management, utilizando o RM Client, deixe o usuário configurado na role “Service User”.
Configurando Release Management em um Servidor Fora do Domínio?

6. No servidor de deploy, o RMDeploy, abra o Deployment Agent como o usuário “ServerUser”.

7. Na tela de configuração do Deployment Agent, no campo Account entre com a conta “DeployUser” e no campo Password a senha do usuário. No campo URL coloque a URL do seu Release Management Server e depois em Apply.

Configurando Release Management em um Servidor Fora do Domínio?
 

8. A tela de configuração deverá ter sucesso.

Configurando Release Management em um Servidor Fora do Domínio?
 

9. Entre na tela “Servers” do seu Release Management Client e execute o scann para novos servidores com agentes configurados e o novo servidor deverá aparecer.

Parabéns! Você configurou o seu Release Manager para deploy em um servidor fora de seu domínio utilizando shadow accounts.

*************************************

Link que mencionei acima:

Configuring Release Management Deployment Agent on a Non-Domain server — http://bharathsundaresan.com/2015/02/configuring-release-management-deployment-agent-non-domain-server/#sthash.lGEuCC1W.dpuf

*************************************

Outro link com um caminho alternativo:

Configuring Release Management to work across untrusted domains — http://blogs.msdn.com/b/visualstudioalm/archive/2013/12/12/configuring-release-management-to-work-across-untrusted.aspx

Abraços!

Alex Giannotti