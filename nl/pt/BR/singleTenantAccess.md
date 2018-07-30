---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Acesso ao Ambiente Único do Locatário
{: #singleTenantEnvironment}


As etapas a seguir discutem o acesso ao ambiente de locatário énico, juntamente com os métodos de criação
de uma instância de serviço.
{: shortdesc}


## Acessando seu Ambiente de Locatário Único
{: #accessSTE}

1. Em seu navegador, acesse o catálogo do [{{site.data.keyword.cloud_notm}} ](https://console.bluemix.net/catalog/){: new_window}.

2. Clique em **Efetuar login** e efetue login com o seu IBMid.

6. No filtro de procura do catálogo, insira **WebSphere Application Server**.

    ![alt text](images/filter.png "Search Filter")

7. Em **Application Services**, clique no quadro do **WebSphere Application Server**.

    ![alt text](images/iconWAS.png "WebSphere Application Server tile")

8. No menu **Ambiente**, selecione o seu ambiente de locatário único.

    ![texto alternativo](images/environmentSTE.png "Nome do ambiente de locatário único")

    **Evitar problemas: ** o ambiente público pode ser mostrado como o padrão. A exibição do nome do ambiente correto assume que você está com login efetuado na região correta e um membro de uma organização que tem permissão para acessar o seu ambiente de locatário único.

    **Nota:** se você selecionar um dos ambientes públicos, poderá haver um encargo por hora. Portanto, se você não vir o seu nome do ambiente de locatário único, abra um chamado de suporte conforme definido na página [Obtendo suporte ao cliente](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}.

9. Selecione o plano apropriado e clique em **Criar**.

    ![texto alternativo](images/createSTE.png "Escolha um plano e crie o seu serviço")


**Nota:** a precificação por hora não se aplica a ambientes de locatário único. Um ambiente de locatário único inclui um número fixo de **blocos** que são chamados de cota. Um ambiente pequeno contém 64 blocos. Um médio contém 128 blocos e um grande contém 256 blocos.

Um  ** bloco **  é definido como a seguir:
  * 1 vCPU
  * Disco de 12,5 GB [ 1 ]
  * 2 GB de RAM

[1] *Tecnicamente, um sistema pequeno contém apenas 12 GB de disco. Um sistema de mídia contém 25 GB de disco, um grande contém 50 GB e assim por diante. *

Para cada máquina virtual criada, especifique o tamanho da camiseta que você deseja: S, M, L, XL ou XXL, que corresponde a 1,
2, 4, 8 e 16 blocos. Ao selecionar um tamanho de camiseta, o número de blocos correspondente é diminuído da sua cota.

Por exemplo, suponha que você tenha um ambiente pequeno, que contenha 64 blocos. Nesse ambiente, você configurou instâncias de
serviço que contêm duas XXLs, três XLs e 1 L para um total de 60 blocos usados. Se você selecionar um tamanho de camiseta médio para uma nova assinatura do Liberty Core, uma mensagem poderá ser exibida, que indica a sua cota e o número de blocos ainda disponíveis:

> **A sua cota de memória de único locatário para esse serviço é de 64 blocos. Incluindo a sua configuração atual, você tem 2 blocos restantes. Para aumentar a cota de memória, entre em contato com Vendas IBM. **


## Ambiente de Rede Privado
{: #private_network}

Após o seu WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}: o ambiente de locatário único é fornecido e é possível fazer download de suas credenciais VPN e estabelecer uma conexão OpenVPN. Para obter mais informações, consulte os links a seguir:

* [ Acesso VPN ](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#vpnAccess){: new_window}
* [ Configurando OpenVPN ](https://console.bluemix.net/docs/services/ApplicationServeronCloud/systemAccess.html#setup_openvpn){: new_window}

## Gerenciando seu Ambiente de Locatário Único
{: #manageSTE}

Para incluir capacidade extra em seu WebSphere Application Server existente no {{site.data.keyword.Bluemix_notm}}: ambiente de locatário único ou para solicitar capacidade em outro data center, entre em contato com a central de atendimento das Américas, o representante IBM local ou o seu Parceiro de Negócios IBM. Para identificar o seu representante ou parceiro, ligue para 800-426-4968. Para obter mais informações, entre em contato com as centrais de atendimento das Américas. Telefone: 800-IBM-CALL (426-2255) Fax: 800-2IBM-FAX (242-6329).


## Suportando seu Ambiente de Locatário Único
{: #supportingSTE}

Se você tiver problemas, será possível receber assistência abrindo um chamado de suporte conforme definido na página [Obtendo suporte ao cliente](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}.
