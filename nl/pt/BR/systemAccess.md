---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Acesso ao sistema
{: #system_access}

Aprenda os métodos de criação e gerenciamento de uma instância de serviço e explore maneiras de acessar e configurar o acesso aos seus sistemas.
{: shortdesc}

## Uso da API de REST no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}
{: #restapi_usage}

As instâncias no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} são criadas, provisionadas, gerenciadas e excluídas de uma das formas a seguir:

* No catálogo e painel de serviço do {{site.data.keyword.Bluemix_notm}}.
* Por meio da criação de um aplicativo ou script que usa APIs RESTful.

Por meio do uso de APIs REST compatíveis com o Swagger 2.0, os clientes têm acesso à mesma função conforme fornecido no portal e no painel. Para obter mais informações sobre APIs de REST e recursos suportados, consulte o WebSphere Application Server na {{site.data.keyword.Bluemix_notm}} [Documentação da API de REST](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window}. Para o código de amostra que demonstra o uso das APIs de REST, faça download das {{site.data.keyword.Bluemix_notm}} [Amostras de API de REST](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window} do WebSphere Application Server hospedado no Git.

**Nota:** depois de criar uma instância de serviço, dependendo do tamanho que é criada, o seu serviço pode não estar imediatamente pronto para uso. Recomenda-se consultar o campo **Status** do JSON retornado para determinar o estado atual da instância de serviço.

** Nota:** A URL **apiEndpoint** referenciada nas [Amostras da API de REST](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window} aponta para a região de Dallas. Se estiver usando outras regiões, assegure-se de que seu aplicativo referencie a URL **apiEndpoint** apropriada.

*Tabela 1. URLs de terminal de API para implementação da API de REST*

| **Nome da região** | **Prefixo da região** | **URL de terminal de API** |       
|:-------------:|:--------------:|:-------------:|
| Dallas | `us-south` | https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Londres | `eu-gb` | https://wasaas-broker.eu-gb.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Frankfurt | `eu-de` | https://wasaas-broker.eu-de.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Sydney | `au-syd` | https://wasaas-broker.au-syd.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |

## Painel de serviço
{: #service_dashboard}

Depois de criar sua instância de serviço, você é levado para o painel de serviço. Sempre é possível voltar ao painel de serviço ao clicar no ícone de serviço a partir do painel da sua organização.
A partir do painel de serviço você poe acessar:

* Um link para esta documentação
* Um link para fazer o download dos arquivos de configuração OpenVPN necessários
* A capacidade de iniciar e parar a máquina virtual. A VM é ativada inicialmente.
* O nome do host
* O usuário administrativo e a senha administrativa
* Uma chave SSH privada
* O usuário administrador e a senha do administrador do WebSphere&reg;
* As URLs do Admin Center e do console administrativo


## Configurando o openVPN para o WebSphere Application Server em instâncias do {{site.data.keyword.Bluemix_notm}}
{: #setup_openvpn}

O OpenVPN é necessário para acesso a qualquer WebSphere Application Server na máquina virtual do {{site.data.keyword.Bluemix_notm}}. Ela deve estar instalada e em execução com privilégios de administrador.

### Configurar openVPN no Windows

1. Faça download do Windows Installer do openVPN para a sua arquitetura do sistema do website do openVPN:
  * Sistemas de 64 bits:  [ openvpn-install-2.3.4-I001-x86_64.exe ](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * Sistemas de 32 bits:
[openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. Assegure-se de [executar como um Administrador do Windows](https://technet.microsoft.com/en-us/magazine/ff431742.aspx){: new_window} e que o openVPN esteja instalado.
3. Faça download dos arquivos de configuração VPN do link de download do OpenVPN do WebSphere Application Server na
instância do {{site.data.keyword.Bluemix_notm}} no painel de serviço. Extraia os quatro arquivos no arquivo compactado para o diretório `{OpenVPN home}\config`. Por exemplo:

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. Inicie o programa cliente da openVPN "OpenVPN GUI". Assegure-se de selecionar **Executar como Administrador do Windows** para iniciar o programa. Se você não o fizer, pode não ser
capaz de se conectar.

### Configurar openVPN no Linux

1. Para instalar o openVPN, siga as instruções do [openVPN
para Linux](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}.

   Se precisar fazer download e instalar manualmente o RPM Package Manager, acesse o [download do openVPN unix/linux](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}. Você pode precisar de assistência de seu administrador Linux.
3. Faça download dos arquivos de configuração VPN do link de download do OpenVPN do WebSphere Application Server na
instância do {{site.data.keyword.Bluemix_notm}} no painel de serviço. Extraia os arquivos no diretório a partir do
qual você planeja iniciar o cliente OpenVPN. Você precisa de todos os quatro arquivos no mesmo
diretório.
3. Inicie o programa cliente da openVPN. Abra uma janela do terminal e acesse o diretório que contém os arquivos de
configuração. Execute o comando a seguir como root:

  ```
  openvpn -- config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### Configurar openVPN no Mac
1. Um método é instalar o [Tunnelblick](https://tunnelblick.net/){: new_window}, um produto de software livre.
2. Extraia os arquivos de configuração da VPN a partir do serviço WebSphere. o Tunnelblick solicita sua senha do administrador para Mac e inclui a
configuração no conjunto de VPNs que você pode usar para se conectar.
3. Conecte-se à VPN e, em seguida, poderá acessar sua máquina virtual. Após seu primeiro acesso, o Tunnelblick armazena a configuração em cache e você pode se conectar a partir do Tunnelblick. É possível colocar um ícone na barra de menus para facilitar o acesso.


## Usando SSH para acessar o WebSphere Application Server nas VMs do {{site.data.keyword.Bluemix_notm}}
{: #using_ssh}

Estas instruções assuem que você está usando o OpenSSH como seu cliente. O OpenSSH normalmente está disponível no Linux ou no Cygwin em execução no Windows. Ele também pode ser instalado para executar a partir de um prompt de comandos do Windows.

Para verificar a instalação do OpenSSH, execute o comando a seguir.
  ```
  ssh -V
  ```
  {: codeblock}

A mensagem a seguir é um exemplo da resposta:
  ```
  OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

Use as instruções a seguir para configurar o acesso SSH para seu WebSphere Application Server nas VMs do {{site.data.keyword.Bluemix_notm}}.

1. Revise a mensagem de aviso que aparece na primeira vez em que você conecta, "A autenticidade do host x.x.x.x não pode ser estabelecida." Essa mensagem é normal. Quando solicitado, selecione sim. A chave pública agora está instalada em sua VM para o usuário **virtuser**.
2. Efetue login em **virtuser** usando a chave privada. Para melhores resultados, use o método de autenticação de chave privada.
3. Copie o conteúdo da chave privada em um arquivo.
4. Conecte usando SSH executando o comando a seguir.

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. Ganhoe a autoridade completa do sysadmin alternando de **virtuser** para **root** executando o comando a seguir.

  ```
  sudo su root
  ```
  {: codeblock}

6. Se você tiver problemas ao acessar o sistema com a chave ssh privada, use a senha raiz que é fornecida. Efetue login como root executando o comando a seguir e forneça a senha.

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. Quer você acesse o sistema com a chave ssh privada
ou com a senha raiz, mude imediatamente a senha raiz.
8. Para simplificar seus comandos SSH, crie um arquivo que seja denominado `config` no diretório `%HOME%/.ssh`. Por exemplo:

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. Execute o comando a seguir para se conectar como **virtuser**.

   ```
   ssh VM1
   ```
   {: codeblock}

## Caminhos do sistema
{: #system_paths}

* Os comandos do Liberty podem ser emitidos de `/opt/IBM/WebSphere/Liberty/bin`.
* O local do perfil do servidor Liberty é `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1`.
* Os arquivos principais do produto do WebSphere Application Server tradicional, que são compartilhados por todos os perfis, estão localizados em `/opt/IBM/WebSphere/AppServer/`.
* Os comandos tradicionais do WebSphere Application Server podem ser emitidos do local do perfil padrão em `/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin`, em que:
  * `<profile_type>` é um valor de `AppSrv`, `Dmgr`, `Custom`, `AdminAgent`, `JobMgr` ou `SecureProxySrv`.
  * `<profile_number>` é um número sequencial que é usado para criar um nome do perfil exclusivo.


## Gerenciando servidores pela linha de comandos
{: #start_servers}

**Evite problemas:** ao gerenciar os servidores WebSphere da linha de comandos, certifique-se de usar o **wsadmin**, o ID administrativo do WebSphere, não o **virtuser**. Ao gerenciar o servidor IHS da linha de comandos, certifique-se de usar **root**.

## Usando os link do Centro Administrativo e do Console Administrativo
{: #console_links}

Ao clicar no link para o Admin Center ou Admin Console, será possível que receba um aviso de *Conexão não confiável*. A mensagem exata varia de acordo
com o navegador, assim como as etapas exatas para efetuar bypass ou eliminar o aviso.

Uma vez que você está usando links que são fornecidos pelo {{site.data.keyword.IBM}}, é possível ignorar o aviso e se conectar com segurança. Se o seu navegador oferecer armazenar
a exceção de segurança, fazê-lo é a maneira mais fácil de evitar o aviso no futuro.

Outra opção é exportar o certificado de assinante recebido e, então, importá-loem seu navegador como um certificado raiz confiável. Essa opção requer que você crie uma entrada em seu arquivo *hosts* que mapeie o endereço IP da VM (máquina virtual) para o nome comum do emissor do certificado. Esse nome está no formato a seguir: `wl<pureapplication.ibmcloud.com`. Se agora o nome do host for usado em vez do endereço IP na URL, será possível se conectar sem problemas. O Admin Center ou o Admin Console devem ser acessados usando esse nome do host em vez do endereço IP na URL.

Finalmente, os clientes frequentemente instalam seus próprios certificados raiz para
aplicativos que eles tornam externos. Para obter mais informações, consulte a documentação do [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} ou do [Liberty Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} no IBM Knowledge Center.

## Portas de firewall
{: #firewall_ports}

Talvez seja necessário abrir portas no firewall para permitir acesso a aplicativos e
bancos de dados. É possível abrir portas de firewall usando o script `openFirewallPorts.sh`, que é possível localizar nos locais a seguir.
  * Em cada WebSphere Application Server no nó do {{site.data.keyword.Bluemix_notm}}, o script `openFirewallPorts.sh` está no diretório `WAS_HOME/virtual/bin`.
  * Em cada host Liberty Collective, o `openFirewallPorts.sh` está no diretório `WAS_HOME/virtual/bin`.

### Uso

Execute o script `openFirewallPorts.sh` usando a sintaxe de comando a seguir.

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

em que:
* PORT é o número da porta
* PROTOCOL é TCP ou UDP
* `-persist` é `true` ou `false`

É possível especificar diversas portas em uma lista separada por vírgulas.

**Nota**: a porta s e porta d da porta que está aberta são abertas nas seções de ENTRADA e SAÍDA do firewall. Deve-se executar esse script como raiz usando `sudo`. Também é possível modificar iptables diretamente.

## Configurando o servidor da web
{: #configure_webserver}

Ao provisionar uma célula ou um coletivo, você receberá um ambiente pré-configurado. Especificamente, para uma célula do Network Deployment tradicional, você recebe o ambiente a seguir:

* Um Gerenciador de Implementação que está colocado com o IBM HTTP Server para propósitos de desenvolvimento e de teste.
* Um nó customizado federado ao Gerenciador de Implementação.
* O Gerenciador de Implementação, o Servidor IHS e o Agente do Nó são todos inicialmente provisionados ao estado INICIADO.

Se o servidor da web for necessário para manipular todas as solicitações do usuário, então poderá ser necessário gerar e propagar o plug-in após a implementação do seu aplicativo.

**Evite problemas:** antes de gerar e propagar o plug-in, assegure-se de que as tarefas de pré-requisito a seguir sejam concluídas.

* Em seu ambiente Windows, Linux ou MAC local, assegure-se de que a [openVPN](systemAccess.html#setup_openvpn) esteja configurada, iniciada e que você esteja conectado à região adequada.
* No WebSphere Application Server no painel de serviço do {{site.data.keyword.Bluemix_notm}}, clique em **Abrir o console administrativo** e efetue login com wsadmin e a Senha de Administrador que é fornecida no painel de serviço.
* No console administrativo, crie um servidor de aplicativos (por exemplo, ***server1***), porque o Deployment Manager é federado com um nó customizado vazio.
* Inicie o servidor que você criou.
* Durante a instalação do aplicativo, assegure-se de que os módulos de seu aplicativo sejam mapeados para o servidor que você acabou de iniciar e para o servidor da web (por exemplo, ***webserver1***).

As etapas de alto nível a seguir assumem que as tarefas de pré-requisito estão concluídas.

1. No Console Administrativo, gere o plug-in a partir da opção Ambiente.
   1. Escolha **Ambiente > Atualizar configuração de plug-in do servidor da web global**.
   2. Clique em **OK** ou em **Sobrescrever para gerar um novo arquivo de configuração de plug-in**.
2. No Deployment Manager, copie o plug-in na configuração do servidor da web.

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. Abra o arquivo `httpd.conf` no `IHS_HOME/conf` (por exemplo, `/opt/IBM/WebSphere/HTTPServer/conf`) e assegure-se de que as duas linhas a seguir existam.

    ```
    LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. Abra as portas executando os comandos a seguir.

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
   ```
   {: codeblock}
5. Pare e inicie o servidor da web executando os comandos a seguir:
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. Acesse seu aplicativo por meio do plug-in.
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**Nota:** as etapas que são fornecidas representam um caminho de muitos quando você está tentando configurar um servidor da web. Se assistência adicional for necessária, consulte [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window}.

Se não for possível acessar seu aplicativo, é provável que você esteja enfrentando um problema de acesso à porta no firewall. Portanto, pode ser necessário reiniciar qualquer um dos servidores a seguir: o servidor de aplicativos, o agente do nó, o servidor da web e o gerenciador de implementação. Além
disso, é possível que precise acessar o Painel de serviço do WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} e reinicie cada máquina virtual.
{: tip}

## Configuração de SSL
{: #ssl_configuration}

O WebSphere Application Server tradicional e o Liberty são configurados com o protocolo [SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window}. É possível mudar o protocolo modificando a configuração de SSL.

### WebSphere Application Server tradicional
{: #ssl-was}

1. Abra o arquivo `security.xml` no diretório `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` e modifique a linha a seguir.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}

2. Abra o arquivo `ssl.client.props` no diretório `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` e modifique a linha a seguir.

   ```
   com.ibm.ssl.protocol=SSL_TLSv2
   ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. Abra o arquivo `server.xml` no diretório `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` e modifique a linha a seguir dentro do elemento de configuração SSL `defaultSSLConfig`.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}
