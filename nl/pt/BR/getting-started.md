---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-18"

keywords: migrate websphere, create service, profile, architecture, vm, virtual machine, provision

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Tutorial de Introdução
{: #getting-started}

Com o {{site.data.keyword.appserver_full}}, é possível configurar um ambiente pré-configurado do WebSphere Application Server tradicional ou do Liberty em minutos. Este tutorial de introdução orienta o provisionamento de um ambiente do WebSphere Application Server em uma máquina virtual em apenas algumas etapas.
{: shortdesc}

## Antes de Começar
{: #prereqs}

Se você desejar um ambiente com recursos de máquina virtual mais dedicados, como um contrato de reserva ou um Ambiente de Locatário Único, entre em contato com Vendas IBM antes de criar o serviço. Saiba mais sobre essas opções em [Sobre](/docs/services/ApplicationServeronCloud?topic=wasaas-about#about).

### Migrando um ambiente existente do WebSphere

Para migrar um ambiente existente do WebSphere Application Server Network Deployment para esse serviço, use o [WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}}![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}. A ferramenta faz upload da configuração do perfil e dos aplicativos para seu servidor independente ou nós de célula para uma instância de serviço no {{site.data.keyword.cloud_notm}}. Para obter uma visão geral da migração de nuvem e um roteiro passo a passo do uso da ferramenta, consulte [o guia do WebSphere Configuration Migration Tool for IBM Cloud ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo") ](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window} em WASdev.

As etapas a seguir orientam a criação de um novo ambiente no
{{site.data.keyword.appserver_full}}.

## Etapa 1: Criar o Serviço
{: #create}

1. Acesse a página [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server) no catálogo do {{site.data.keyword.cloud_notm}}.
1. Efetue login com o seu IBMid ou inscreva-se em uma conta do {{site.data.keyword.cloud_notm}}.
1. Na página do catálogo, revise as seleções para a configuração de serviço.

  Para ambientes pré-pagos, use as seleções padrão ou modifique-as para se adequarem às suas necessidades.

  Se você tiver um contrato de reserva ou um ambiente de locatário único, observe as opções a seguir.

  * **Contrato de reserva:** em **Escolha uma região/local na qual implementar**, verifique se a região selecionada é a região correta para o seu contrato.

  * **Ambiente de locatário único:** em **Escolha uma região/local na qual implementar**, verifique se a região selecionada é a mesma em que o ambiente de locatário único está implementado. Em **Ambiente**, selecione o seu ambiente de locatário único. Por padrão, o ambiente público pode ser mostrado.

    Se seu Ambiente de Locatário Único não estiver listado, verifique se você está na região correta e se sua organização tem acesso ao Ambiente de Locatário Único.
    {: tip}
1. Selecione o plano de precificação para a edição do {{site.data.keyword.appserver_short}} que você deseja implementar.
1. Clique em **Criar**.


## Etapa 2: escolha seu ambiente (somente implementação de rede)
{: #choose_env}

Os planos Base e Liberty Core do {{site.data.keyword.appserver_short}} têm apenas servidores únicos, portanto, se você tiver escolhido esses planos, poderá ignorar essa etapa.

Para o plano de implementação de rede, escolha o perfil e a arquitetura para o seu ambiente.

* **Perfil:** escolha {{site.data.keyword.appserver_short}} tradicional ou Liberty
* **Arquitetura:** escolha um ambiente de servidor único ou um ambiente em cluster com células
tradicionais ou Liberty Collectives


## Etapa 3: dimensione suas máquinas virtuais
{: #vm_sizing}

É possível dimensionar individualmente a máquina virtual para cada componente em seu ambiente. As máquinas virtuais são fragmentadas em [tamanhos](/docs/services/ApplicationServeronCloud?topic=wasaas-about#vm-size) de blocos de recursos.

Clique na guia para o componente, como o servidor, o gerenciador de implementação ou o nó do aplicativo e selecione o tamanho
para a sua máquina virtual.

## Etapa 4: provisione seu ambiente
{: #service_profile}

Revise os detalhes no resumo da configuração de serviço, incluindo o tempo estimado para o fornecimento.

**Contrato de reserva:** certifique-se de que a opção **Faturamento** esteja configurada como _Contrato de reserva_. Se você não vir a opção, verifique se
[a sua organização](/docs/account?topic=account-orgsspacesusers){:new_window} é exatamente a mesma do nome da
organização para o seu contrato, incluindo as letras maiúsculas e minúsculas e os espaços em branco. Se você
fornecer o serviço sem selecionar o faturamento de contrato de reserva, o faturamento pré-pago será usado.

Clique em
**Fornecimento** para configurar o seu ambiente do {{site.data.keyword.appserver_short}}.

## Próximas etapas
{: #anchor_value}

Saiba como acessar e gerenciar o seu novo ambiente {{site.data.keyword.appserver_short}} em [Acesso de sistema](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access).
