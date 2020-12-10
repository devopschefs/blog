Oi Pessoas!

Hoje vou falar um pouco sobre as diferenças entre VSTS e TFS, vou passar pelas maiores diferenças sobre os dois produtos da Microsoft e tentar passar para vocês a minha visão de como os produtos podem atender as necessidades da sua empresa.

Você já se deparou com essa pergunta? Qual eu devo adotar para a minha empresa? VSTS ou TFS? As maiores razões para as empresas mudarem para o VSTS são:

Manutenção de servidores simplificada.
Acesso imediato as últimas features do produto.
Conexão melhorada com sites remotos.
Uma transição entre gastos com manutenção da infraestrutura para gastos operacionais.
 

https://www.visualstudio.com/en-us/articles/adopting-vsts

We ship updates every sprint to VSTS, which means every three weeks you get new features. Since you always have the latest features, you never have to worry about upgrades. You also don’t need to maintain the servers (e.g., replace disks that fail, power supplies that fail, etc.). You don’t need to manage operating system and other updates to stay secure. You don’t have to backup the server in case of disaster. You don’t have to replace aging hardware. You can access your account from anywhere without having to properly configure a TFS server to be accessible over the internet. You can add users using Microsoft accounts (MSAs) or Azure Active Directory identities. You can take advantage of the hosted build machine pool to run your builds.

The features in TFS missing from VSTS are primarily SharePoint integration and SQL Reporting Services (warehouse and cube). You can use PowerBI with VSTS in addition to the built-in reporting you can do with the VSTS dashboards.

As you can tell, I’d recommend VSTS over TFS unless you are required to have the server in your own infrastructure.

Abraços!

Alex Giannotti