---

copyright:
  years: 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Tutorial Introdução
{:#getting-started}

Com o {{site.data.keyword.appserver_full}}, é possível configurar um ambiente pré-configurado do WebSphere Application Server tradicional ou do Liberty em minutos. Este tutorial de introdução orienta o provisionamento de um ambiente do WebSphere Application Server em uma máquina virtual em apenas algumas etapas.
{: shortdesc}

## Antes de Começar
{: #prereqs}

Se você desejar um ambiente com recursos de máquina virtual mais dedicados, como um contrato de reserva ou um ambiente de locatário único, será necessário entrar em contato com Vendas IBM antes de criar o serviço. Saiba mais sobre essas opções em [Sobre](index.html).

## Etapa 1: Criar o Serviço
{: #create}

1. Acesse a página [ {{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) no catálogo do {{site.data.keyword.cloud_notm}}.
1. Efetue login com o seu IBMid ou inscreva-se em uma conta do {{site.data.keyword.cloud_notm}}.
1. Na página do catálogo, revise as seleções para a configuração de serviço.

  Para ambientes pré-pagos, use as seleções padrão ou modifique-as para se adequarem às suas necessidades. Se você tiver um contrato de reserva ou um ambiente de locatário único, observe as opções a seguir.

  * **Contrato de reserva:** em **Escolha uma região/local na qual implementar**, verifique se a região selecionada é a região correta para o seu contrato.

  * **Ambiente de locatário único:** em **Escolha uma região/local na qual implementar**, verifique se a região selecionada é a mesma em que o ambiente de locatário único está implementado. Em **Ambiente**, selecione o seu ambiente de locatário único. Por padrão, o ambiente público pode ser mostrado.

    Se não vir o ambiente de locatário único listado, verifique se você está na região correta e se a sua organização tem acesso ao ambiente de locatário único.
    {: tip}
1. Selecione o plano de precificação para a edição do {{site.data.keyword.appserver_short}} que você deseja implementar.
1. Clique em  ** Criar **.


## Etapa 2: escolha o seu ambiente
{: #choose_env}

{{site.data.keyword.appserver_short}} Os planos Base e Liberty Core têm apenas servidores únicos, portanto, se você tiver escolhido esses planos, poderá ignorar essa etapa.

Para o plano de implementação de rede, escolha o perfil e a arquitetura para o seu ambiente.

* ** Perfil: **  Escolha  {{site.data.keyword.appserver_short}}  tradicional ou Liberty
* **Arquitetura:** escolha um ambiente de servidor único ou um ambiente em cluster com células
tradicionais ou Liberty Collectives


## Etapa 3: Tamanho Máquinas Virtuais
{: #vm_sizing}

É possível dimensionar individualmente a máquina virtual para cada componente em seu ambiente. O dimensionamento da máquina
virtual é feito em partes em [tamanhos de camisetas](index.html#vm-size) de blocos de recursos.

Clique na guia para o componente, como o servidor, o gerenciador de implementação ou o nó do aplicativo e selecione o tamanho
da camiseta para a sua máquina virtual.

## Etapa 4: Provisão de seu ambiente
{: #service_profile}

Revise os detalhes no resumo da configuração de serviço, incluindo o tempo estimado para o fornecimento. Clique em
**Fornecimento** para configurar o seu ambiente do {{site.data.keyword.appserver_short}}.

## Próximas etapas
{: #anchor_value}

Saiba como acessar e gerenciar o seu novo ambiente {{site.data.keyword.appserver_short}} em [Acesso de sistema](systemAccess.html).
