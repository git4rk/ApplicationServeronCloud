---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

keywords: overview, websphere, liberty, version, cell, collective, vm, virtual machine, t-shirt, block, price, reserve contract

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Acerca de
{: #about}

{{site.data.keyword.appserver_full}} facilita una configuración rápida en una instancia preconfigurada de WebSphere Application Server Liberty, Traditional Network Deployment o Traditional WebSphere Java EE en un entorno de nube alojado en {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

## Visión general de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}
{: #overview}

WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} proporciona a los consumidores servidores de WebSphere tradicional y Liberty ya configurados. Está alojado en invitados de máquinas virtuales con acceso raíz al sistema operativo invitado. Cuando cree un servicio, elija entre _Liberty_, _Traditional ND_ o _Traditional WebSphere_.

**Nota:** ahora los consumidores pueden elegir entre el nivel de fixpack actual o una versión más antigua de [(n o n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} al crear cualquier WebSphere Application Server en la instancia de {{site.data.keyword.Bluemix_notm}}.

Se le proporciona una experiencia de administración de WebSphere familiar y tiene acceso completo al sistema operativo subyacente. Puede reutilizar los scripts existentes y realizar los pequeños ajustes necesarios en el sistema para trabajar con infraestructuras propias o de terceros. El centro de administración y las consolas de administración se proporcionan para administrar su servicio de WebSphere Application Server Liberty, ND o tradicional, igual que las configuraciones de WebSphere locales.

El Plan de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} Network Deployment consiste en un entorno de células de WebSphere Application Server Network Deployment con dos o más máquinas virtuales. La primera máquina virtual contiene el Gestor de despliegue e IBM HTTP Server y las demás máquinas virtuales contienen nodos personalizados (agentes de nodo) federados en el Gestor de despliegue. Utilice sus scripts wsadmin existentes para crear su configuración de WebSphere o utilizar la consola de administración de WebSphere para configurar manualmente el entorno. Estas nuevas funciones permiten a los usuarios configurar un entorno en clúster, lo que constituye un aspecto básico para cualquier aplicación de empresa de middleware. Ahora los clientes pueden optar por agrupar en clúster una topología para cargar solicitudes de carga en dos o más instancias.

WebSphere Application Server en el {{site.data.keyword.Bluemix_notm}} Network Deployment Plan también incluye el uso de un colectivo de Liberty. El colectivo de Liberty es un dominio administrativo para un grupo de perfiles de Liberty (servidores) y consta de dos o más máquinas virtuales. La
primera máquina virtual contiene el servidor Liberty del controlador del colectivo, que es un punto de control
para el colectivo de Liberty. Además del colectivo de Liberty, esta máquina virtual también
contiene el servidor HTTP de IBM, que permite el acceso a sus aplicaciones desde un navegador web. Las
máquinas virtuales restantes son hosts colectivos donde residen los miembros colectivos (servidores de perfil de Liberty). La función Liberty Admin Center también está activada en el servidor controlador de Liberty.

En la figura siguiente se muestra la arquitectura de WebSphere Application Server en entornos de célula de despliegue de red de {{site.data.keyword.Bluemix_notm}} y de colectivo de Liberty.

Figura 1. Arquitectura de la célula de despliegue de red y de colectivo de Liberty

![Figura 1. Arquitectura de la célula de despliegue de red y de colectivo de Liberty](images/CellCollectiveDiagram.gif)

**Nota**: en la _Figura 1_ anterior, el patrón que muestra la colocación de Deployment Manager o del controlador del colectivo con IBM HTTP Server está pensado para entornos de desarrollo y de prueba. WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} también le ofrece la libertad de volver a configurar el software preinstalado para que se ajuste a sus requisitos operativos y de las aplicaciones de producción; al igual que lo haría con el entorno local. Además, para los requisitos de producción más estrictos, póngase en contacto con el representante de ventas de IBM, quien le dará información sobre la oferta IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} de un solo arrendatario, que ofrece recursos aislados de red y de cálculo.


## Entorno operativo
{: #operational_environment}

IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} es un servicio que devuelve invitados (máquinas virtuales) en un entorno compartido para que los consumidores desplieguen aplicaciones. Una VPN protege el servicio público de exploraciones de puerto genéricas y otros ataques basados en red no solicitado. Sin embargo, es importante tener en cuenta que la VPN del servicio que se utiliza para acceder a la instancia de servicio puede compartirse entre varias organizaciones y usuarios de {{site.data.keyword.Bluemix_notm}}. Las máquinas virtuales proporcionan recursos de cálculo, memoria y E/S, que vienen de una agrupación compartida de recursos de IaaS.

Puesto que los recursos específicos de cálculo, memoria y E/S los ejecutan máquinas virtuales en un entorno compartido, las configuraciones de servicio pueden variar. Las configuraciones para cada instancia de servicio determinada se pueden visualizar a través de los paneles de control y portales del servicio IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}.

IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} ofrece instancias de máquina virtual. Con estas instancias, los clientes utilizan un portal simple para crear y gestionar despliegues de WebSphere Application Server de forma repetible y coherente y con gran flexibilidad para ajustar sus aplicaciones. Los usuarios pueden empezar a trabajar con sus máquinas virtuales WebSphere Application Server Liberty, ND o tradicional ya configuradas en un entorno de nube alojado. Los usuarios pueden migrar las aplicaciones existentes de WebSphere Application Server a {{site.data.keyword.Bluemix_notm}} y tener un control total del sistema operativo y el middleware subyacentes.

## Tamaño de la máquina virtual
{: #vm-size}

IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} proporciona diversos tamaños de camiseta para que pueda definir el tamaño correcto para aplicaciones que utilizan mucha memoria al ofrecer máquinas virtuales de mayor tamaño. Cada máquina virtual que suministre para que ejecute WebSphere Application Server se puede dimensionar por separado según los requisitos estimados de los recursos.

Las máquinas virtuales se dimensionan y se facturan en *bloques*. Para cada bloque del tamaño de camiseta, la máquina virtual se suministra con los recursos siguientes.
* 1 CPU virtual (vCPU)
* 2 GB de RAM
* 12,5 GB de espacio en el disco duro (12,0 GB para las VM de un solo bloque)


| Camiseta | Bloques | vCPU | RAM (GB) | DD (GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
| S | 1 | 1 | 2 | 12 |
| M | 2 | 2 | 4 | 25 |
| L | 4 | 4 | 8 | 50 |
| XL | 8 | 8 | 16 | 100 |
| XXL | 16 | 16 | 32 | 200 |
{: caption="Tabla 1. Bloques por tamaño de camiseta" caption-side="top"}

Cada servidor o nodo se suministra en una única máquina virtual. Por ejemplo, en el plan de despliegue de red, si suministra una máquina virtual M (2 bloques) para el gestor de despliegue y 8 máquinas virtuales S (1 bloque) para los nodos de aplicación, se le facturará un total de 10 bloques.

## Opciones de facturación
{: #billing-options}

El precio de cada bloque depende de la opción de facturación que elija:
* **[Pago según uso](#pay-as-you-go):** facturación según uso; el precio se calcula en horas por bloque utilizado
* **[Contrato de reserva](#reserve-contract):** suscripciones mensuales de prepago de recursos reservados

### Pague según uso
{: #pay-as-you-go}

Se aplica el método de pago según uso si suministra el servicio IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} sin ponerse en contacto con el equipo de ventas de IBM para buscar opciones de facturación alternativas. El uso se carga por hora completa o por hora parcial de cada bloque que se utiliza durante el periodo de facturación mensual. La facturación mínima es 1/4 de bloque hora.

**Nota**: debido a una cantidad específica de recursos de cálculo, memoria y recursos de E/S, se carga por las instancias detenidas a una tasa reducida del 5% de la tasa de bloque por hora. Dentro del servicio, las instancias detenidas están limitadas a 10 direcciones IP o 64 GB de memoria.

#### Precios de los planes

El precio por bloque varía en función del plan de WebSphere Application Server que elija.

En la tabla siguiente se muestra el precio total por hora de cada máquina virtual de tamaño de camiseta. Los precios representan los planes de IBM WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} a 1 de abril de 2016 y se muestran en dólares de los EE.UU. (USD). Consulte el catálogo para ver los precios actuales en su región.

| Camiseta | Bloques | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
| S | 1 | 0,21 $ | 0,30 $ |  0,70 $ |
| M | 2 | 0,42 $ | 0,60 $ |  1,40 $ |
| L | 4 | 0,84 $ | 1,20 $ |  2,80 $ |
| XL | 8 | 1,68 $ | 2,40 $ |  5,60 $ |
| XXL | 16 | 3,36 $ | 4,80 $ |  11,20 $ |
{: caption="Tabla 2. Plan Liberty Core" caption-side="top"}


### Contrato de reserva
{:#reserve-contract}

Con la facturación de contrato de reserva, adquiere una suscripción mensual de prepago que garantiza el acceso a los bloques de recursos de cálculo reservados físicamente. Estos bloques de servicio se reservan para su uso exclusivo y no se pueden considerar como capacidad disponible para ningún otro usuario de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}. Si ya tiene licencias de WebSphere Application Server, puede elegir un contrato de reserva para traer su propia licencia, que utiliza estas licencias y tiene una tarifa de facturación reducida. Para configurar la facturación del contrato, [póngase en contacto con el equipo de ventas de IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

Las suscripciones están disponibles en incrementos de 8 bloques. Las horas totales de bloque se basan en el número de horas del mes, pero puede utilizar horas de bloque en cualquier momento del mes. Por ejemplo, un mes de 30 días tiene 720 horas, que, si se multiplica por una suscripción de 8 bloques, da como resultado un total de 5.760 horas de bloque.

  ```
30 días * 24 horas al día * 8 bloques = 5.760 horas de bloque
  ```

Puede personalizar la forma y el momento eh que se utilizan los bloques para satisfacer la demanda de carga de trabajo variable; puede, por ejemplo, utilizar 4 bloques, aumentar a 12 bloques y luego reducir a 8 bloques. Mientras permanezca por debajo del total de horas de bloque del mes, no hay ningún cargo adicional.

Se puede elegir entre utilizar los bloques de contrato de reserva o utilizar la facturación de pago según uso cuando se aprovisiona cada entorno.

**Nota:** Si suprime una instancia de servicio, puede que tenga que esperar unos 30 minutos para que sus bloques estén disponibles para las nuevas instancias de servicio.

#### Excedentes

Si su uso supera las horas de bloque mensuales de su suscripción, el exceso se carga de acuerdo con el modelo de facturación de pago según uso, de modo que solo se le facturarán las horas de bloque adicionales que utilice. El uso de bloques se calcula en una base a horas completa o parciales, y el uso mínimo es de 1/4 de una hora de bloque.

Los bloques del modelo de pago según uso no constituyen capacidad reservada y proceden de una agrupación de recursos comunes.

#### Tasas de prorrateo para un uso flexible

Los bloques de la facturación del contrato de reserva se basan en el plan de despliegue de red de WebSphere Application Server, pero también puede utilizar los bloques para otros planes. Con los otros planes, el uso se prorratea de modo que se resta una hora de bloque de la tasa de prorrateo del plan cuando se refleja en las horas de bloque restantes del contrato de reserva.

En la tabla siguiente se muestran las tasas de prorrateo para cada plan y el precio efectivo por hora de bloque real después de calcular el prorrateo. Para ver los precios actuales en su región, [póngase en contacto con el equipo de ventas de IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

| Plan | Tasa de prorrateo | Precio/hora después del prorrateo |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0,3 | 0,21 $ |
| WebSphere Application Server Base  | 0,43 | 0,30 $ |
| WebSphere Application Server Network Deployment | 1,0 | 0,70 $ |
{: caption="Tabla 3. Tasas de prorrateo de hora de bloque por plan" caption-side="top"}

Por ejemplo, supongamos que tiene una instancia M (2 bloques) de WebSphere Application Server Base que se ejecuta durante 51 horas. Para calcular las horas de bloque utilizadas del contrato de reserva, las horas de bloque reales se multiplican por la tasa de prorrateo, lo que da un total de 43,86 horas de bloque:

```
2 bloques * 51 horas * 0,43 de prorrateo = 43,86 horas de bloque prorrateadas
```

El coste total es el mismo, pero puede utilizar más horas de bloque reales de los planes prorrateados porque restan menos de las horas de bloque del contrato de reserva.
{:.tip}
