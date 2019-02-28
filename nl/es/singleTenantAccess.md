---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Acceso a un solo entorno de un solo arrendatario
{: #singleTenantEnvironment}


En los pasos siguientes se explica cómo acceder su entorno de un solo arrendatario, junto con los métodos para crear una instancia de servicio.
{: shortdesc}


## Acceso a su entorno de un solo arrendatario
{: #accessSTE}

1. En su navegador, vaya al [catálogo de {{site.data.keyword.cloud_notm}}](https://{DomainName}/catalog/){: new_window}.

2. Pulse **Iniciar sesión** e inicie la sesión con su IBMid.

6. En el filtro de búsqueda del catálogo, escriba **WebSphere Application Server**.

    ![Filtro de búsqueda](images/filter.png)

7. En **Servicios de aplicación**, pulse el mosaico **WebSphere Application Server**.

    ![Mosaico de WebSphere Application Server](images/iconWAS.png)

8. En el menú **Entorno**, seleccione su entorno de un solo arrendatario.

    ![Nombre del entorno de un solo arrendatario](images/environmentSTE.png)

    **Evite problemas:** es posible que se muestre el entorno público como valor predeterminado. Si se muestra el nombre de entorno correcto, se da por supuesto que ha iniciado la sesión en la región correcta y que es miembro de una organización con permiso para acceder a su entorno de un solo arrendatario.

    **Nota:** si selecciona uno de los entornos públicos, es posible que incurra en un cargo por hora. Por lo tanto, si no ve su nombre de entorno de un solo arrendatario, abra una incidencia de soporte tal como se explica en la página [Obtención de ayuda](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues){: new_window}.

9. Seleccione el plan adecuado y pulse **Crear**.

    ![Elija un plan y cree su servicio](images/createSTE.png)


**Nota:** el precio por hora no se aplica a los entornos de un solo arrendatario. Un entorno de un solo arrendatario incluye un número fijo de **bloques** que se denominan cuotas. Un entorno pequeño contiene 64 bloques. Un entorno mediano contiene 128 bloques, y uno grande contiene 256 bloques.

Un **bloque** se define de la forma siguiente.
  * 1 vCPU
  * 12.5 GB de disco[1]
  * 2 GB de RAM

[1] *Técnicamente, un sistema pequeño solo contiene 12 GB de disco. Un sistema mediano contiene 25 GB de disco y uno grande contiene 50 GB, y así sucesivamente.*

Para cada máquina virtual que cree, especifique el tamaño de camiseta que desee: S, M, L, XL o XXL, lo que corresponde a 1, 2, 4, 8 y 16 bloques. Cuando selecciona un tamaño de camiseta, el número correspondiente de bloques se reduce a partir de su cuota.

Por ejemplo, suponga que tiene un entorno pequeño, que contiene 64 bloques. En este entorno, ha configurado las siguientes instancias de servicio: dos XXL, tres XL y 1 L, lo que constituye un total de 60 bloques utilizados. Si selecciona un tamaño de camiseta mediano para una nueva suscripción de Liberty Core, podría aparecer un mensaje que indique su cuota y el número de bloques que quedan disponibles:

> **Su cuota de memoria de un solo arrendatario para este servicio es de 64 bloques. Incluyendo la configuración actual, quedan 2 bloques. Para aumentar su cuota de memoria, póngase en contacto con el equipo de ventas de IBM.**


## Entorno de red privada
{: #private_network}

Después de que se suministre su entorno de un solo arrendatario, puede descargar las credenciales de VPN y establecer una conexión OpenVPN. Para obtener más información, consulte los siguientes enlaces:

* [Acceso VPN](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#vpnAccess){: new_window}
* [Configuración de OpenVPN](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#setup_openvpn){: new_window}

## Gestión del entorno de un solo arrendatario
{: #manageSTE}

Para añadir capacidad a su entorno de un solo arrendatario existente o para solicitar capacidad en otro centro de datos, póngase en contacto con los centros de atención al cliente de América, con el representante local de IBM o con su Business Partner de IBM. Consulte [Cómo ponerse en contacto con el equipo de ventas](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales) para obtener más información.
