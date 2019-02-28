---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Atualizações mais recentes
{: #latest_updates}

Uma lista das atualizações mais recentes para o serviço.

## 16 de janeiro de 2019: URLs de terminal de API atualizadas para a implementação da API de REST

O prefixo de região para Dallas mudou de `ng` para `us-south`. Os outros prefixos de região permaneceram iguais. As URLs de terminal da API de REST mudaram de `https://wasaas-broker.<region>.bluemix.net/wasaas-broker/api` para `https://wasaas-broker.<region>.websphereappsvr.cloud.ibm.com/wasaas-broker/api`. As URLs `bluemix.net` continuarão sendo suportadas, mas será necessário mudar as URLs de terminal da API de REST para usar `websphereappsvr.cloud.ibm.com`, se você usar as APIs de REST para gerenciar suas instâncias de serviço.

Para obter mais informações sobre as URLs de terminal da API de REST, consulte [Acesso ao sistema](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#system_access).

## 14 de dezembro de 2018: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}
* O fix pack 9.0.0.10 do WebSphere Application Server tradicional agora está disponível ao provisionar uma nova instância de serviço. Além do 9.0.0.10, outros fix packs do WebSphere Application Server tradicional, como o 9.0.0.9, o 8.5.5.14 e o 8.5.5.13, estão disponíveis para provisionamento.
* A versão do fix pack 18.0.0.4 do WebSphere Application Server Liberty agora está disponível ao provisionar uma nova instância de serviço. Além do 18.0.0.4, a versão do fix pack 18.0.0.3 do WebSphere Application Server Liberty está disponível para provisionamento.
* Integrada a manutenção de serviços diversos.

## 24 de outubro de 2018: agora, o faturamento com sua própria licença está disponível para o contrato de
reserva e os ambientes de locatário único

Se você tem licenças existentes do WebSphere Application Server, agora é possível usá-las em seu contrato de reserva ou nos ambientes de locatário único. Os ambientes com faturamento de sua própria licença oferecem os mesmos benefícios que o contrato de reserva padrão ou os ambientes de locatário único, mas são faturados a uma taxa reduzida. Para usar o seu próprio licenciamento, [entre em contato com Vendas IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

## 22 de agosto de 2018: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}
* O fix pack 8.5.5.14 do WebSphere Application Server tradicional agora é disponibilizado quando você fornece uma nova instância de serviço. Além do 8.5.5.14, outros fix packs do WebSphere Application Server tradicional, como o 9.0.0.8, o 9.0.0.7 e o 8.5.5.13, estão disponíveis para fornecimento.
* Integrada a manutenção de serviços diversos.

## 16 de julho de 2018: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* A versão de fix pack 9.0.0.8 do WebSphere Application Server tradicional agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 9.0.0.8, outras versões de fix pack do WebSphere Application Server tradicional, como a 9.0.0.7, a 8.5.5.13 e a 8.5.5.12, estão disponíveis para fornecimento.
* A versão de fix pack 18.0.0.2 do WebSphere Application Server Liberty agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 18.0.0.2, a versão de fix pack 18.0.0.1 do WebSphere Application Server
Liberty está disponível para fornecimento.
* [Várias vulnerabilidades de segurança tratadas](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window} no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}.
* Tratadas [várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window} no IBM SDK Java Technology Edition que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}.

## 13 de junho de 2018: faturamento de contrato de reserva agora disponível

Com o faturamento do contrato de reserva, você compra uma assinatura mensal pré-paga que garante o acesso a blocos de recursos
computacionais fisicamente reservados. Esses blocos de serviço são reservados para o seu uso exclusivo e não podem ser considerados como capacidade disponível para nenhum outro usuário do {{site.data.keyword.appserver_full}}. É possível usar as suas horas de bloqueio de serviço de qualquer maneira que você escolher durante o mês, com todos os excedentes sendo cobrados de acordo com o modelo de assinatura pré-pago típico.

Para saber mais sobre o faturamento do contrato de reserva, consulte [Opções de faturamento](/docs/services/ApplicationServeronCloud?topic=wasaas-about#billing-options).

## 30 de março de 2018: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* A versão de fix pack 9.0.0.7 do WebSphere Application Server tradicional agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 9.0.0.7, outras versões de fix pack do WebSphere Application Server tradicional, como a 9.0.0.6, a 8.5.5.13 e a 8.5.5.12, estão disponíveis para fornecimento.
* A versão de fix pack 18.0.0.1 do WebSphere Application Server Liberty agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 18.0.0.1, a versão de fix pack 17.0.0.4 do WebSphere Application Server Liberty está disponível para fornecimento.
* [Várias vulnerabilidades de segurança]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Diversas Vulnerabilidades no IBM ® Java SDK
  * Uma vulnerabilidade em que o IBM WebSphere Application Server poderia fornecer segurança mais fraca do que o esperado para o Console Administrativo.
  * Uma vulnerabilidade em que as instalações do IBM WebSphere Application Server que utilizam o Login de Formulário poderiam permitir que um invasor remoto conduzisse ataques de spoofing.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server pode permitir que um invasor local obtenha informações confidenciais, causadas pela manipulação indevida de solicitações de aplicativo, o que pode permitir acesso não autorizado à leitura de um arquivo.
  * Uma vulnerabilidade em que o Apache Commons FileUpload, conforme usado em vários produtos, pode permitir que um invasor
remoto execute código arbitrário no sistema, causado pela desserialização de dados não confiáveis na classe DiskFileItem da
biblioteca FileUpload. Um invasor remoto poderia explorar essa vulnerabilidade para executar código arbitrário sob o contexto do
processo atual.
  * Uma vulnerabilidade em que as CPUs do Intel Haswell Xeon, AMD PRO e ARM Cortex A57 podem permitir que um invasor autenticado local obtenha informações confidenciais, causadas por um desvio de verificação de limites no recurso de execução de instrução de ramificação especulativa da CPU. Ao conduzir ataques de canal do lado do cache de destino, um invasor pode explorar
essa vulnerabilidade para cruzar o limite de syscall e ler dados da memória virtual da CPU.
* Integrada a manutenção de serviços diversos.

## 8 de janeiro de 2018: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* A versão de fix pack 9.0.0.6 do WebSphere Application Server tradicional agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 9.0.0.6, outras versões de fix pack do WebSphere Application Server tradicional, como a 9.0.0.5, a 8.5.5.12 e a 8.5.5.11, estão disponíveis para fornecimento.
* A versão de fix pack 17.0.0.4 do WebSphere Application Server Liberty agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 17.0.0.4, a versão de fix pack 17.0.0.3 do WebSphere Application Server Liberty está disponível para fornecimento.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade em que o OpenSAML pode permitir que um invasor autenticado remoto obtenha informações confidenciais, causado por um erro ao analisar entidades XML.
  * Uma vulnerabilidade em que o Apache HTTP Server poderia permitir que um atacante remoto obtivesse informações confidenciais, causada por uma falha no método HTTP OPTIONS chamado Optionsbleed.
  * Uma vulnerabilidade em que o Apache Portable Runtime Utility (APR-util) é vulnerável a uma negação de serviço, causada pela falha ao validar a integridade dos arquivos de banco de dados SDBM usados pelas funções apr_sdbm*().
* Integrada a manutenção de serviços diversos.

## 21 de dezembro de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* WebSphere Application Server incluído no recurso de migração do IBM Cloud em Dallas, Londres e Sydney. Esse recurso fornece a migração completa de ponta a ponta dos ambientes v7, v8 ou v8.5.5 no local existentes para ambientes v9 no IBM Cloud. Para obter mais informações, consulte a [Ferramenta de migração de configuração do WebSphere para IBM Cloud ](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud).
* Integrada a manutenção de serviços diversos.

## 27 de outubro de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* Incluída a capacidade de fornecimento de um nível de fix pack mais antigo [(n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} por meio da guia Perfil de serviço no Painel de serviço do {{site.data.keyword.Bluemix_notm}} ou por meio da API de REST.
* A versão de fix pack 9.0.0.5 do WebSphere Application Server tradicional agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 9.0.0.5, outras versões de fix pack do WebSphere Application Server tradicional, como a 9.0.0.4, a 8.5.5.12 e a 8.5.5.11, estão disponíveis para fornecimento.
* A versão de fix pack 17.0.0.3 do WebSphere Application Server Liberty agora é disponibilizada quando você fornece uma nova instância de serviço. Além da 17.0.0.3, a versão de fix pack 17.0.0.2 do WebSphere Application Server Liberty está disponível para fornecimento.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade em que o IBM WebSphere Application Server pode criar arquivos usando as permissões padrão em vez das permissões customizadas quando scripts de inicialização customizados são usados.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server Proxy Server ou On-demand-router (ODR) pode permitir que um invasor local obtenha informações confidenciais, causadas por dados antigos que estão sendo armazenados em cache e, em seguida, servidos.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server é vulnerável ao cross-site scripting. Essa vulnerabilidade permite que os usuários integrem código JavaScript arbitrário na UI da web, alterando, assim, a funcionalidade desejada, potencialmente levando à divulgação de credenciais em uma sessão confiável.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server poderia fornecer segurança mais fraca do que o esperado depois de usar o Console Administrativo para atualizar as configurações de ligações de segurança de serviços da web.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server Versão 9.0.0.4 poderia fornecer segurança mais fraca do que o esperado depois de usar o comando PasswordUtil para ativar a criptografia de senha AES.
  * Uma vulnerabilidade em que o Apache MyFaces pode permitir que um invasor remoto obtenha informações confidenciais.
  * Uma vulnerabilidade em que o IBM WebSphere Application Server pode permitir que um invasor remoto obtenha informações confidenciais causadas por manipulação de erros incorreta por MyFaces no JSF.
* Integrada a manutenção de serviços diversos.

## 30 de agosto de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* Integrada a manutenção de serviços diversos.

## 30 de junho de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* Integrada a manutenção de serviços diversos.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}, de modo que o fix pack 8.5.5.12 ou 9.0.0.4 é instalado com as novas instâncias do WebSphere Application Server Tradicional.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}, de modo que o fix pack 17.0.0.2 é instalado com novas instâncias do WebSphere Application Server Liberty (Planos Core e ND).
* Incluído um recurso [Gerenciamento de configuração de VPN avançado](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#advancedVPN){: new_window} que pode ser usado para criar e gerenciar várias configurações de VPN nas regiões de Londres e Sydney.
* Aprimoramentos incluídos no recurso [Acesso à Internet pública](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#publicInternetAccess){: new_window} que permite que os clientes gerenciem melhor o seu endereço IP público.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window}
abordadas no IBM SDK Java Technology Edition que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}
incluindo:
  * Uma vulnerabilidade não especificada para o componente Java SE AWT que poderia permitir que invasores não autenticados assumissem o controle do sistema.
  * Uma vulnerabilidade não especificada para o componente Java SE JCE que poderia permitir que um invasor não autenticado assumisse o controle do sistema.
  * Uma vulnerabilidade não especificada para o componente Java SE JAXP que poderia permitir que um invasor não autenticado causasse uma negação de serviço, resultando em um impacto de alta disponibilidade ao usar vetores de ataque desconhecidos.
  * Uma vulnerabilidade não especificada para o componente Java SE Networking que poderia permitir que um invasor não autenticado causasse baixo impacto
de confidencialidade, baixo impacto de integridade e nenhum impacto de disponibilidade.
  * Uma vulnerabilidade não especificada para o componente Java SE Networking que poderia permitir que um invasor não autenticado causasse nenhum impacto
de confidencialidade, baixo impacto de integridade e nenhum impacto de disponibilidade.
  * Uma vulnerabilidade não especificada para o componente Java SE Security que poderia permitir que um invasor não autenticado causasse nenhum impacto de confidencialidade, baixo impacto de integridade e nenhum impacto de disponibilidade.
  * Uma vulnerabilidade a um erro de XML External Entity Injection (XXE) ao processar dados XML. Um invasor remoto pode explorar essa vulnerabilidade para expor informações altamente confidenciais ou consumir recursos de memória.
  * Um problema em que zlib é vulnerável a uma negação de serviço, causada por um ponteiro aritmético fora do limite em
inftrees.c.
  * Um problema em que a zlib é vulnerável a uma negação de serviço, causada por uma mudança à esquerda de um número negativo indefinido.
  * Um problema em que zlib é vulnerável a uma negação de serviço, causada por um ponteiro fora dos limites big-endian.

## 25 de maio de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* Integrada a manutenção de serviços diversos.
* Incluído um recurso [Gerenciamento de configuração de VPN avançado](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#advancedVPN){: new_window} que pode ser usado para criar e gerenciar várias configurações de VPN na região de Frankfurt.
* Atualizado o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} de modo que o JDK 8 seja instalado com todas as novas instâncias do serviço.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma potencial vulnerabilidade de segurança com o adaptador de recursos JCA do WebSphere Application Server MQ.
  * Uma vulnerabilidade não especificada para o componente Libraries que poderia permitir que um invasor remoto obtivesse informações confidenciais, resultando em um alto impacto de confidencialidade ao usar vetores de ataque desconhecidos.

## 21 de abril de 2017: WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}}

* Integrada a manutenção de serviços diversos.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade em que o WebSphere Application Server configurado com o OpenID Connect (OIDC) Trust Association
Interceptor (TAI) pode permitir que um usuário obtenha privilégios elevados no sistema.
  * Uma vulnerabilidade na qual o WebSphere Application Server pode fornecer segurança mais fraca do que o esperado. Um invasor remoto pode explorar essa fraqueza para obter informações confidenciais e obter acesso não autorizado ao console administrativo.
  * Um problema no qual o WebSphere Application Server é vulnerável à falsificação de solicitação entre sites, o que pode permitir que um invasor execute ações maliciosas e desautorizadas transmitidas por um usuário em que o website confia.


## 15 de março de 2017: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Integrada a manutenção de serviços diversos.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de modo que o fix pack 8.5.5.11 ou 9.0.0.3 seja instalado com novas instâncias do WebSphere Application Server Tradicional.
* [Várias vulnerabilidades de segurança](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window}
abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade não especificada para o componente Libraries que não tem impacto de confidencialidade, alto impacto de integridade e nenhum impacto de disponibilidade.
  * Uma vulnerabilidade não especificada para o componente Libraries que poderia permitir que um invasor remoto obtivesse informações confidenciais, resultando em um alto impacto de confidencialidade ao usar vetores de ataque desconhecidos.
  * Uma vulnerabilidade não especificada para o componente Libraries que poderia permitir que um invasor remoto causasse uma negação de serviço, resultando em um baixo impacto de disponibilidade ao usar vetores de ataque desconhecidos.
  * Uma vulnerabilidade no OpenSSL que poderia permitir que um invasor remoto obtivesse informações confidenciais, causadas por um erro na cifra DES/3DES, usada como parte do protocolo SSL/TLS.
  * Uma vulnerabilidade que permite que os usuários integrem código JavaScript arbitrário na IU da web, alterando, assim, a funcionalidade desejada, potencialmente levando à divulgação de credenciais dentro de uma sessão confiável.
  * Uma vulnerabilidade em ataques de divisão de resposta Apache HTTPD para HTTP, causada por validação imprópria da entrada fornecida pelo usuário.
  * Uma vulnerabilidade no Samba que poderia permitir que um invasor remoto autenticado obtivesse privilégios elevados no sistema, causada pela falha de manipulação da soma de verificação PAC.
  * Uma vulnerabilidade no Samba que poderia permitir que um invasor remoto autenticado obtivesse privilégios elevados no sistema, causada pelo encaminhamento de um Ticket Granting Ticket (TGT) para outro serviço que você usa para autenticação do Kerberos.
  * Uma vulnerabilidade no Samba para um estouro de buffer baseado em heap, causada por uma falha de quebra de número inteiro na função ndr_pull_dnsp_name().


## 10 de fevereiro de 2017: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Integrada a manutenção de serviços diversos.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de modo que o fix pack 8.5.5.11 ou 9.0.0.2 seja instalado com novas instâncias do WebSphere Application Server Tradicional.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de modo que o fix pack 16.0.0.4 seja instalado com novas instâncias do WebSphere Application Server Liberty (Planos Core e ND).
* [Várias vulnerabilidades de segurança](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window} abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade de negação de serviço, causada permitindo que objetos serializados de fontes não confiáveis executem e causem o consumo de recursos.
  * O uso de solicitações SOAP malformadas que poderiam permitir que um invasor remoto obtivesse informações confidenciais.


## 16 de dezembro de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Integrada a manutenção de serviços diversos.
* [Várias vulnerabilidades de segurança](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window}
abordadas no IBM SDK Java Technology Edition que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}
incluindo:
  * Uma vulnerabilidade não especificada no Oracle Java SE e no Java SE Embedded relacionada ao componente Hotspot que possui alto impacto de confidencialidade, alto impacto de integridade e alto impacto de disponibilidade.
  * Uma vulnerabilidade não especificada no Oracle Java SE e no Java SE Embedded relacionada ao componente Networking que poderia permitir que um invasor remoto obtivesse informações confidenciais, resultando em um alto impacto de confidencialidade ao usar vetores de ataque desconhecidos.
  *  Uma vulnerabilidade de cross-site scripting no IBM WebSphere Application Server que permite que os usuários integrem código JavaScript arbitrário na IU da web. O código pode alterar a funcionalidade desejada potencialmente, levando à divulgação de credenciais em uma sessão confiável.


## 8 de novembro de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Capacidade incluída para que os clientes solicitem um endereço [IP público](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#networkEnvironment) para sua VM do WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window} abordadas que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade no IBM WebSphere Application Server que poderia permitir que invasores remotos executassem código Java arbitrário com um objeto serializado de fontes não confiáveis.
  * Uma vulnerabilidade de negação de serviço que é causada por uma leitura fora de limites na função TS_OBJ_print_bio. Um atacante remoto poderia explorar essa vulnerabilidade usando um arquivo de registro de data e hora categorizado para causar o travamento do aplicativo.
  * Uma vulnerabilidade em potencial no OpenSSL que poderia permitir que um atacante remoto obtivesse informações confidenciais, causada por um erro no Triple-DES na cifra de bloco de 64 bits, usada como parte do protocolo SSL/TLS. Ao capturar grandes quantias de tráfego criptografado entre o servidor
SSL/TLS e o cliente, um invasor remoto capaz de realizar um ataque man-in-the-middle poderia explorar essa vulnerabilidade para recuperar os dados de texto simples e obter informações confidenciais. Essa vulnerabilidade é conhecida como o ataque SWEET32 Birthday.
  * O OpenSSL é vulnerável a uma negação de serviço. Ao solicitar repetidamente uma renegociação, um invasor remoto autenticado poderia enviar uma extensão da Solicitação de Status do OCSP
excessivamente grande para consumir todos os recursos de memória disponíveis.
  * O OpenSSL é vulnerável a uma negação de serviço, causada por um estouro de número inteiro na função MDC2_Update. Ao usar vetores de ataque desconhecidos, um invasor remoto poderia
explorar essa vulnerabilidade para acionar uma gravação fora dos limites e fazer com que o aplicativo travasse.
  * Uma potencial vulnerabilidade no OpenSSL que permite que um invasor remoto obtenha informações confidenciais, causada por um erro na implementação de DSA que permite seguir um caminho
de código de horário não constante para determinadas operações. Um invasor poderia explorar essa vulnerabilidade usando um ataque de sincronização de cache para recuperar a chave privada do DSA.
  * O OpenSSL é vulnerável a uma negação de serviço, causada por verificações de comprimento de mensagem ausente ao fazer a análise sintática de certificados. Um invasor remoto
autenticado poderia explorar essa vulnerabilidade para acionar uma leitura fora de limites e causar uma negação de serviço.

## 19 de setembro de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} para que as novas instâncias do WebSphere Application Server Liberty (Planos Core e ND) usem o fix pack 16.0.0.3.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window} abordadas que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade no IBM WebSphere Application Server Liberty que poderia permitir que um invasor remoto realizasse ataques de phishing.
  * Uma vulnerabilidade no IBM WebSphere Application Server Liberty para cross-site scripting em clientes OpenID Connect.
  * Uma potencial vulnerabilidade no IBM WebSphere Application Server Liberty que poderia permitir que um invasor remoto obtivesse informações confidenciais, causada pela manipulação
inadequada de exceções quando não existe uma página de erro padrão.
  * Uma vulnerabilidade no Apache Tomcat para uma negação de serviço, causada por um erro no componente Apache Commons FileUpload.
  * Uma vulnerabilidade no IBM WebSphere Application Server e no IBM WebSphere Application Server Liberty que poderia permitir que um invasor remoto obtivesse informações confidenciais, causada pela manipulação inadequada de respostas sob determinadas condições.
  * Uma vulnerabilidade não especificada para o componente Networking que não tem impacto de confidencialidade, baixo impacto de integridade e nenhuma disponibilidade.

## 17 de agosto de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de 8.5.5.9 a 8.5.5.10
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window} abordadas que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * As vulnerabilidades do Apache Struts que afetam o WebSphere Application Server e o console de administração do WebSphere Application Server Hypervisor Edition.
  * Uma potencial vulnerabilidade de negação de serviço com o IBM WebSphere Application Server que você usa para serviços SIP.
  * Várias vulnerabilidades que podem afetar o IBM HTTP Server usado pelo WebSphere Application Server.
  * Uma vulnerabilidade que permite o redirecionamento do tráfego HTTP com aplicativos CGI que pode afetar o IBM HTTP Server (IHS). Essa vulnerabilidade é conhecida como "HTTPOXY".
  * Uma vulnerabilidade de divulgação de informações no IBM WebSphere Application Server.
  * Uma vulnerabilidade potencial de restrição de segurança de bypass no IBM WebSphere Application Server que ocorre apenas em ambientes que têm a propriedade customizada do contêiner da web `HttpSessionIdReuse` ativada.


## 24 de junho de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Capacidade incluída para que os clientes escolham entre V8.5 e V9.0 ao criar uma nova instância _ND Tradicional_ ou _WebSphere Tradicional_.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} para que as novas instâncias do WebSphere Application Server Liberty (Planos Core e ND) usem o fix pack 16.0.0.2. 16.0.0.2 é o próximo fix pack após o 8.5.5.9. A partir da 16.0.0.2, todos os recursos opcionais do Liberty autorizados que são suportados para esses planos são instalados por padrão.
* [Várias vulnerabilidades de segurança](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window} abordadas que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} incluindo:
  * Uma vulnerabilidade XML External Entity Injection (XXE) no Apache Standard Taglibs que afeta o IBM WebSphere Application Server.
  * Um potencial para segurança mais fraca do que o esperado para o recurso de Descoberta da API do perfil Liberty do WebSphere Application Server e os documentos Swagger.
  * Uma vulnerabilidade potencial de divulgação de informações no Admin Center do IBM WebSphere Application Server Liberty.
  * Uma vulnerabilidade potencial de divisão de resposta HTTP no IBM WebSphere Application Server.
  * Vulnerabilidades do OpenSSL divulgadas em 3 de maio de 2016 pelo Projeto OpenSSL.

## 13 de junho de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* Incluída a capacidade de os clientes construírem, fornecerem, gerenciarem e excluírem instâncias da máquina
virtual por meio da criação de um aplicativo ou script que usa o WebSphere Application Server em APIs de RESTful do {{site.data.keyword.Bluemix_notm}}.
* Incluída função que permite que um cliente tenha um número fixo de instâncias INTERROMPIDAS com não mais de 10 endereços IP ou 64 GB de memória. Agora os clientes são cobrados por instâncias acumuladas no estado INTERROMPIDO a uma taxa reduzida de 5%.

## 26 de abril de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* [Vulnerabilidades de segurança em potencial](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window} abordadas no WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} se o FIPS 140-2
estiver ativado e múltiplas vulnerabilidades no Samba - incluindo Badlock.
* Integrada a manutenção de serviços diversos.

## 15 de abril de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado

* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de 8.5.5.8 a 8.5.5.9
* Tratada uma vulnerabilidade de [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window} no Liberty for Java para {{site.data.keyword.Bluemix_notm}} que afeta consumidores que usam o cliente de conexão OpenID (OIDC).
* Integrada a manutenção de serviços diversos.

## 19 de fevereiro de 2016: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado
* Incluída uma opção para clientes com aplicativos de uso intensivo de memória para "dimensionar corretamente" seu ambiente com máquinas virtuais maiores. Os clientes podem selecionar o tamanho do recurso específico de um determinado componente do WebSphere Application Server ou de um único sistema com máquinas virtuais de até 32 GB de RAM.
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de 8.5.5.7 a 8.5.5.8
* Várias vulnerabilidades abordadas no IBM SDK Java Technology Edition que afetam o WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} que são referenciadas comumente como [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}.
* Tratada uma vulnerabilidade [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window} que afeta consumidores da saída do provedor OAuth.
* Integrada a manutenção de serviços diversos.

## 11 de dezembro de 2015: WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} atualizado
* Nome de produto oficial mudado de IBM Application Server on Cloud no {{site.data.keyword.Bluemix_notm}} para IBM WebSphere Application Server no {{site.data.keyword.Bluemix_notm}}
* Novas capacidades incluídas no plano do WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} Network Deployment. O plano consiste em um ambiente de célula do WebSphere Application Server Network Deployment com duas ou mais máquinas virtuais. Esses novos recursos permitem que os
usuários configurem um ambiente em cluster para alta disponibilidade, failover e escalabilidade.
* Novas capacidades incluídas no plano WebSphere Application Server no {{site.data.keyword.Bluemix_notm}} Liberty Core. O plano inclui
o uso de um Liberty Collective, que é um domínio administrativo para um grupo de perfis Liberty
(servidores) e consiste em duas ou mais máquinas virtuais
* WebSphere Application Server atualizado no {{site.data.keyword.Bluemix_notm}} de 8.5.5.6 a 8.5.5.7
* Tratada uma [vulnerabilidade do Apache Commons Collections](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window} para manipular a desserialização
do objeto Java.
* Tratada uma vulnerabilidade que poderia permitir um [ataque
de divisão de resposta HTTP](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}.
* Integrada a manutenção de serviços diversos.

## 15 de outubro de 2015: Atualização do Application Server on Cloud
* Incluídos os dois novos planos a seguir:
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* Manutenção de serviços diversos
