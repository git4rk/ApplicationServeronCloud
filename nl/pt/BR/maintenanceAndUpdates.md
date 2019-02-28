---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Atualizando seu Ambiente
{: #updating-your-environment}

## Estratégia de manutenção
{: #maintenance-strategy}

O {{site.data.keyword.appserver_full}} é atualizado em uma cadência regular, assegurando que novas instâncias de
serviço sejam criadas com os fix packs e correções atuais. A
nuvem traz fornecimento fácil e rápido de novas instâncias de serviço para o gerenciamento de middleware.

É possível criar um WebSphere Application Server na instância do {{site.data.keyword.Bluemix_notm}} no nível do fix
pack atual ou anterior (n ou n-1) para uma versão específica do produto. O uso do fix pack atual fornece as atualizações e os recursos
mais recentes, mas pode ser necessário que o fix pack anterior esteja em conformidade com os requisitos de
implementação de nuvem híbrida.

Ao criar uma nova instância, é possível escolher dentre os seguintes níveis de fix pack na guia **Perfil de serviço** na instância de serviço:

** Liberty **
  * 18.0.0.4
  * 18.0.0.3

** WebSphere Application Server tradicional **
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## Aplicando correções e atualizações de fix pack
{:#applying-fixes}

A maneira mais rápida de atualizar para o nível de manutenção mais recente é criar uma nova instância. No entanto, se você preferir reter instâncias de serviço de longa duração, será possível aplicar manutenção à sua instalação existente executando o script `installService.sh` fornecido ou usando o IBM Installation Manager conforme descrito nas seções a seguir.

### Atualizando usando o script installService.sh

A sua instância de serviço é configurada com um repositório do Installation Manager que é atualizado com frequência com correções de segurança disponíveis e fix packs do WebSphere Application Server. É possível usar o script `/home/virtuser/installService.sh` para aplicar essas correções e fix packs. O script deve ser executado como o usuário raiz.

A quantidade de espaço em disco que é necessária para instalar as atualizações varia, dependendo dos tipos de atualizações que você instalar. A instalação apenas de correções temporárias requer 1 GB de espaço livre na máquina virtual. A instalação de fix
packs aumentou o espaço em disco necessário para 1.3 GB.

A execução do script executa as seguintes ações:

* Para todas as instâncias do WebSphere Application Server e do IBM HTTP Server em execução
* Opcionalmente, instala os fix packs mais recentes para o Installation Manager, o WebSphere Application Server, o IBM HTTP Server e o Java&trade; SDK
* Instala as correções temporárias mais recentes para o WebSphere, o IBM HTTP Server e o Java&trade; SDK
* Reinicia todas as instâncias

#### Opções
* **`-fixpacks`**

    Atualiza todos os pacotes para o fix pack mais recente.
* **`-noprompt`**

    Não solicita confirmação antes da atualização.

#### Exemplos de sintaxe

```
./installService.sh -?
```
{:.codeblock}

Exibe o texto da ajuda.


```
./installService.sh
```
{:.codeblock}

Instala todas as correções temporárias aplicáveis, mas nenhum fix pack.


```
./installService.sh -fixpacks
```
{:.codeblock}

Instala todos os fix packs disponíveis e, em seguida, instala todas as correções temporárias aplicáveis.

### Atualizando com o Installation Manager
{:#installation-manager}

O [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} é instalado no diretório `/home/virtuser/IBM/Installation Manager` e pode ser executado diretamente para aplicar correções e fix packs.

**Evite problemas:**como os arquivos binários subjacentes são instalados como `virtuser`, um usuário virtual administrativo limitado, assegure-se de que o Installation Manager seja sempre executado como `virtuser`.

## Aplicando atualizações do sistema em máquinas virtuais
{:#vm-system-updates}

A aplicação de atualizações do sistema em uma máquina virtual é semelhante à atualização de um sistema físico do Red Hat Enterprise Linux&reg; (RHEL). Usando o gerenciador de pacotes Yum, é possível instalar, atualizar, desinstalar e, de outra forma, gerenciar pacotes. O WebSphere Application Server em sistemas {{site.data.keyword.Bluemix_notm}} está configurado para receber atualizações do servidor Red Hat Satellite da IBM, que fornece pacotes seguros da rede do Red Hat. O servidor Satellite é gerenciado
pela IBM e não pode ser modificado de seu sistema.

Para obter mais informações, consulte [Aplicando atualizações de pacote no Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} e [Yum, o gerenciador de pacote do Red Hat](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
