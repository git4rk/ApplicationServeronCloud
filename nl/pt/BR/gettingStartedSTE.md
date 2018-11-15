---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-25"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Ambientes de Locação Única
{: #getting_startedSTE}

O {{site.data.keyword.appserver_full}}:ambiente de locatário único fornece aos clientes uma carga de trabalho isolada do WebSphere, um ambiente híbrido totalmente integrado e dados seguros. Esse guia de introdução é projetado para identificar os elementos chave que auxiliam os clientes no acesso e no gerenciamento de seu WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: ambiente de locatário único.
{: shortdesc}

## Solicitando um ambiente de locatário único
{:#ordering}

Os ambientes de locatário único não podem ser criados por meio do catálogo do {{site.data.keyword.Bluemix_notm}} e devem ser solicitados entrando em contato com Vendas IBM. Ao solicitar o ambiente, é possível escolher um ambiente de locatário único padrão ou com sua própria licença. Os ambientes de locatário único padrão incluem toda a infraestrutura necessária e as licenças do WebSphere Application Server. Os ambientes de locatário único com sua própria licença permitem a utilização de licenças separadas do WebSphere Application Server.

Para solicitar um ambiente de locatário único, [entre em contato com Vendas IBM](reportingIssues.html#contacting-sales). A equipe de vendas pode ajudar com a configuração de um ambiente customizado para as suas necessidades.

## Visão geral do WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: ambiente de locatário único
{: #overviewSTE}

O WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: a oferta de locatário único fornece aos consumidores sua própria instância privada do serviço, rede privada e recursos isolados. Embora a oferta seja gerenciada independentemente, os painéis criados de serviço e de instância de serviço são acessíveis por meio de uma região pública específica do {{site.data.keyword.Bluemix_notm}}, conforme indicado na figura a seguir:

Figura 1. Arquitetura do WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: ambiente de locatário único

![Figure1. Arquitetura do Ambiente de Locatário Único](images/WASaaS.png)


## Gerenciamento de Organização
{: #organization_management}

O WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: o ambiente de locatário único é configurado de acordo com o seu pedido. Se você fornecer um ou mais nomes de organização do {{site.data.keyword.Bluemix_notm}} como parte do pedido, poderá iniciar o acesso ao seu ambiente agora. Se você não forneceu um ou mais nomes de organização ou se desejar mudar essa configuração, abra um [chamado de suporte](reportingIssues.html#reporting_issues) para **serviços de aplicativo** no console do {{site.data.keyword.Bluemix_notm}} de sua região. O nome da organização (ORG) pode ser localizado no canto superior direito do console do {{site.data.keyword.Bluemix_notm}}, conforme mostrado na figura a seguir:

Figura 2. Local do nome da organização

![Figure2. Local do nome do ORG](images/myORG.png)


**Nota:** para acessar o seu ambiente de locatário único, consulte [Acesso ao ambiente do locatário único](singleTenantAccess.html#singleTenantEnvironment).
