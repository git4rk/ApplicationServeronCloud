---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Informationen
{: #about}

{{site.data.keyword.appserver_full}} ermöglicht das schnelle Einrichten einer vordefinierten Instanz von WebSphere Application Server Liberty, Network Deployment (klassisch) oder WebSphere Java EE (klassisch) in einer gehosteten Cloud-Umgebung in {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

## Übersicht zu WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} bietet Nutzern vorkonfigurierte klassische WebSphere-Server und Liberty-Server. Das Programm wird auf virtuellen Gastmaschinen mit Rootzugriff auf das Gastbetriebssystem gehostet. Wenn Sie einen eigenen Service erstellen, müssen Sie zwischen _Liberty_, _klassischem ND_ und _klassischem WebSphere_ wählen.

**Hinweis:** Kunden können nun zwischen der aktuellen Fixpackstufe und einer älteren Version [(n oder n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} auswählen, wenn sie eine beliebige Instanz von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} erstellen.

Sie erhalten eine vertraute WebSphere-Administrationserfahrung und uneingeschränkten Zugriff auf das zugrunde liegende Betriebssystem. Sie können bereits vorhandene Scripts weiterverwenden und am System die für die Arbeit mit eigenen Frameworks oder Frameworks von Dritten erforderlichen Optimierungsschritte vornehmen. Admin Center und Administrationskonsolen werden ähnlich Ihren lokalen WebSphere-Konfigurationen zur Verwaltung Ihrer WebSphere Application Server Liberty-, ND- oder klassischen Services bereitgestellt.

Der Network Deployment-Plan von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} besteht aus einer WebSphere Application Server Network Deployment-Zellenumgebung mit mindestens zwei virtuellen Maschinen. Die erste virtuelle Maschine enthält den Deployment Manager und IBM HTTP Server und die übrigen virtuellen Maschinen enthalten angepasste Knoten (Knotenagenten), die in den Deployment Manager integriert sind. Mithilfe der vorhandenen wsadmin-Scripts können Sie eine eigene WebSphere-Konfiguration erstellen oder Sie können WebSphere Admin Console verwenden, um die Umgebung manuell zu konfigurieren. Mit diesen neuen Funktionen können Benutzer eine Clusterumgebung konfigurieren, die ein entscheidender Aspekt einer Middleware-Unternehmensanwendung ist. Kunden können nun auswählen, dass für eine Topologie ein Cluster gebildet werden soll, um in zwei oder mehr Instanzen einen Lastausgleich für Anforderungen durchzuführen.

Darüber hinaus umfasst der Network Deployment-Plan von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} die Verwendung eines Liberty-Verbunds. Der Liberty-Verbund ist eine Verwaltungsdomäne für eine Gruppe von Liberty-Profilen (Servern), die aus mindestens zwei virtuellen Maschinen besteht. Die erste virtuelle Maschine enthält den Liberty-Server für den Verbundcontroller, einen Steuerpunkt für den Liberty-Verbund. Zusätzlich zum Liberty-Verbund enthält diese virtuelle Maschine auch IBM HTTP Server, wodurch Zugriff auf Ihre Anwendungen über einen Web-Browser ermöglicht wird. Die übrigen virtuellen Maschinen sind Verbundhosts, in denen sich die Verbundmember befinden (Liberty Profile-Server). Das Liberty Admin Center-Feature ist auf dem Liberty-Controller-Server ebenfalls aktiviert.

In der folgenden Abbildung ist die Umbgebungsarchitektur der Network Deployment-Zelle von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} und des Liberty-Verbunds dargestellt.

Abbildung 1. Architektur der Network Deployment-Zelle sowie des Liberty-Verbunds

![Abbildung 1. Architektur der Network Deployment-Zelle sowie des Liberty-Verbunds](images/CellCollectiveDiagram.gif)

**Hinweis**: In der oben dargestellten _Abbildung 1_ dient das Muster, das die Kollokation des Deployment Managers oder des Verbundcontrollers mit dem IBM HTTP Server darstellt, Entwicklungs- und Testzwecken. Mit WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} haben Sie außerdem die Möglichkeit, die vorinstallierte Software den Erfordernissen der Produktionsanwendung und den betrieblichen Anforderungen entsprechend anzupassen, wie es vor Ort in der Regel der Fall ist. Wenn es ausschließlich um Produktionsanforderungen geht, können Sie sich an den IBM Vertriebsbeauftragten wenden, der Sie gerne über das IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}-Single-Tenant-Angebot informiert, das isolierte Netz- und Rechenressourcen umfasst.


## Betriebsumgebung
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} ist ein Service, mit dem Gäste (virtuelle Maschinen) in einer gemeinsam genutzten Umgebung zur Verfügung gestellt werden, mit denen Nutzer Anwendungen bereitstellen können. Der öffentliche Service wird mithilfe eines VPNs vor generischen Port-Scans und anderen unerwünschten netzbasierten Angriffen geschützt. Es ist jedoch wichtig zu wissen, dass das Service-VPN, das Sie für den Zugriff auf Ihre Serviceinstanz nutzen, möglicherweise mit mehreren {{site.data.keyword.Bluemix_notm}}-Organisationen und -Benutzern gemeinsam genutzt wird. Auf den virtuellen Maschinen werden Berechnungs-, Speicher- und Ein-/Ausgaberessourcen bereitgestellt, die sich in einem gemeinsamen Pool von IaaS-Ressourcen befinden.

Da bestimmte Berechnungs-, Speicher- und Ein-/Ausgaberessourcen von virtuellen Maschinen in einer gemeinsam genutzten Umgebung ausgeführt werden, können die Servicekonfigurationen variieren. Die Konfigurationen für die einzelnen Serviceinstanzen können über die Service-Dashboards und -Portale für IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} angezeigt werden.

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} stellt VM-Instanzen bereit. Mit diesen Instanzen nutzen Kunden für die Erstellung und Verwaltung von WebSphere Application Server-Bereitstellungen für Unternehmen ein einfaches Portal; dabei ist für die Optimierung von Anwendungen neben Konsistenz und wiederholter Anwendbarkeit auch eine erhebliche Flexibilität von Bedeutung. Benutzer können mit vorkonfigurierten WebSphere Application Server Liberty-, ND- oder konventionellen VMs in einer gehosteten Cloudumgebung arbeiten. Benutzer können vorhandene WebSphere Application Server-Anwendungen nach {{site.data.keyword.Bluemix_notm}} migrieren und das zugrunde liegende Betriebssystem und die Middleware uneingeschränkt nutzen.

## Größe der virtuellen Maschine bestimmen
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} bietet eine Preisstruktur auf der Basis von T-Shirt-Größen, mit der Sie die geeignete Umgebungsgröße für speicherintensive Anwendungen einrichten können, indem Sie größere virtuelle Maschinen bereitstellen. Für jede virtuelle Maschine, die Sie für die Ausführung von WebSphere Application Server bereitstellen, kann die Größe unabhängig an den erwarteten Ressourcenbedarf angepasst werden.

Die Größen- und Preisstruktur für virtuelle Maschinen basiert auf *Blöcken*. Für jeden in T-Shirt-Größen angegebenen Block werden der virtuellen Maschine die folgenden Ressourcen bereitgestellt.
* 1 virtuelle CPU (vCPU)
* 2 GB RAM
* 12,5 GB Festplattenspeicherplatz (12,0 GB für Einzelblock-VMs)


| T-Shirt | Blöcke | vCPU | RAM (GB) | FP (GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
| S | 1 | 1 | 2 | 12 |
| M | 2 | 2 | 4 | 25 |
| L | 4 | 4 | 8 | 50 |
| XL | 8 | 8 | 16 | 100 |
| XXL | 16 | 16 | 32 | 200 |
{: caption="Tabelle 1. Blöcke nach T-Shirt-Größen" caption-side="top"}

Jeder Server oder Knoten wird in einer einzelnen virtuellen Maschine bereitgestellt. Beispiel: Wenn Sie im Rahmen des Network Deployment-Plans eine virtuelle Maschine der Größe M (2 Blöcke) für den Deployment Manager und 8 virtuellen Maschinen der Größe S (1 Block) für Anwendungsknoten bereitstellen, fallen Gebühren von insgesamt 10 Blöcke an.

## Abrechnungsoptionen
{: #billing-options}

Die Preisstruktur für den jeweiligen Block ist abhängig von den ausgewählten Abrechnungsoptionen:
* **[Nutzungsabhängige Preisstruktur](#pay-as-you-go):** Nutzungsabhängige Abrechnung in Stunden pro genutztem Block
* **[Reservierungsvertrag](#reserve-contract):** Vorausbezahlte monatliche Abonnements reservierter Ressourcen

### Nutzungsabhängige Preisstruktur
{: #pay-as-you-go}

Eine nutzungsabhängige Preisstruktur findet Anwendung, wenn der IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}-Service bereitgestellt wird, ohne dass der IBM Vertrieb hinsichtlich alternativer Abrechnungsoptionen kontaktiert wird. Nutzungsgebühren fallen für die volle Stunde oder ein entsprechendes Stundensegment für jeden Block an, der während des monatlichen Abrechnungszeitraums genutzt wird. Als Mindestabrechnungszeitraum ist 1/4 Blockstunde festgelegt.

**Hinweise**: Aufgrund einer bestimmten Menge an Rechen-, Speicher- und E/A-Ressourcen wird für gestoppte Instanzen ein reduzierter Gebührensatz von 5 % des stündlichen Blocksatzes berechnet. Innerhalb des Service sind gestoppte Instanzen auf 10 IP-Adressen oder 64 GB Speicherplatz begrenzt.

#### Preisstruktur der Pläne

Der Preis pro Block variiert abhängig vom ausgewählten WebSphere Application Server-Plan.

In der folgenden Tabelle ist der Gesamtpreis pro Stunden für jede in T-Shirt-Größen angegebene virtuelle Maschine aufgeführt. Die Preise entsprechen den IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}-Plänen zum 01. April 2016 und sind in US-Dollar (USD) angegeben. Informationen zu den aktuellen Preisen in Ihrer Region finden Sie im Katalog.

| T-Shirt | Blöcke | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
| S | 1 | $ 0,21 | $ 0,30 |  $ 0,70 |
| M | 2 | $ 0,42 | $ 0,60 |  $ 1,40 |
| L | 4 | $ 0,84 | $ 1,20 |  $ 2,80 |
| XL | 8 | $ 1,68 | $ 2,40 |  $ 5,60 |
| XXL | 16 | $ 3,36 | $ 4,80 |  $ 11,20 |
{: caption="Tabelle 2. Liberty Core-Plan" caption-side="top"}


### Reservierungsvertrag
{:#reserve-contract}

Bei der Abrechnung im Rahmen eines Reservierungsvertrags erwerben Sie ein vorausbezahltes monatliches Abonnement, mit dem der Zugriff auf Blöcke mit physisch reservierten Rechenressourcen garantiert wird. Diese Serviceblöcke werden zu Ihrer exklusiven Nutzung reserviert und stehen anderen WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}-Benutzern nicht als verfügbare Kapazität zur Verfügung. [Kontaktieren Sie den IBM Vertrieb](reportingIssues.html#contacting-sales), um die Abrechnung im Rahmen eines Reservierungsvertrags einzurichten.

Abonnements sind in 8-Block-Stufen verfügbar. Die Gesamtzahl der Blockstunden basiert auf der Anzahl der Stunden im Monat, die Blockstunden können jedoch zu jedem beliebigen Zeitpunkt innerhalb des Monats genutzt werden. Beispiel: Ein Monat mit 30 Tagen umfasst 720 Stunden. Multipliziert mit einem 8-Blöcke-Abonnement ergibt dies insgesamt 5.760 Blockstunden.

  ```
30 Tage * 24 Stunden pro Tag * 8 Blöcke = 5.760 Blockstunden
  ```

Sie können anpassen, wie und wann die Blöcke genutzt werden, um variable Workloadanforderungen zu erfüllen; z. B. können Sie 4 Blöcke nutzen, dann die Nutzung auf 12 Blöcke erhöhen und wieder auf 8 Blöcke reduzieren. Unter der Voraussetzung, dass die Gesamtzahl der Blockstunden im Monat nicht überschritten wird, fallen keine zusätzlichen Gebühren an.

#### Überschreitungen

Wenn die Nutzung die monatlichen Blockstunden im Abonnement überschreitet, werden Überschreitungsgebühren dem nutzungsabhängigen Abrechnungsmodell entsprechend berechnet; dabei werden nur für die zusätzlich genutzten Blockstunden Gebühren fällig. Die Blocknutzung wird auf der Basis einer vollen Stunde oder eines entsprechenden Stundensegments gemessen. Als Mindestabrechnungszeitraum ist 1/4 Blockstunde festgelegt.

Blöcke im Rahmen des nutzungsabhängigen Modells stellen keine reservierte Kapazität dar und stammen aus einem gemeinsamen Ressourcenpool.

#### Gebührensätze für anteilmäßige Verrechnung zur flexiblen Nutzung

Bei der Abrechnung im Rahmen eines Reservierungsvertrags basieren Blöcke auf dem WebSphere Application Server Network Deployment-Plan, Sie können die Blöcke jedoch auch für andere Pläne verwenden. Bei anderen Plänen wird die Nutzung anteilmäßig verrechnet. D. h., eine Blockstunde wird durch den Gebührensatz der anteilmäßigen Verrechnung des jeweiligen Plans reduziert, wenn sie in den verbleibenden Blockstunden des Reservierungsvertrags wiedergegeben wird.

Die folgende Tabelle enthält die Gebührensätze für die anteilmäßige Verrechnung innerhalb des jeweiligen Plans und den effektiven Preis pro tatsächlicher Blockstunde nach der anteilmäßigen Verrechnung. Die aktuellen Preise in der jeweiligen Region erhalten Sie beim [IBM Vertrieb](reportingIssues.html#contacting-sales).

| Plan | Gebührensatz für anteilmäßige Verrechnung | Preis/Stunde nach anteilmäßiger Verrechnung|
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0,3 | $ 0,21 |
| WebSphere Application Server Base  | 0,43 | $ 0,30 |
| WebSphere Application Server Network Deployment | 1,0 | $ 0,70 |
{: caption="Tabelle 3. Gebührensätze für anteilmäßige Verrechnung unterteilt nach Plänen" caption-side="top"}

Beispiel: Sie verfügen über eine WebSphere Application Server Base-Instanz der Größe M (2 Blöcke), die 51 Stunden lang ausgeführt wird. Zur Berechnung der genutzten Blockstunden Ihres Reservierungsvertrags werden die tatsächlichen Blockstunden mit dem Gebührensatz der anteilmäßigen Verrechnung multipliziert. Dies ergibt 43,86 Blockstunden:

```
2 Blöcke * 51 Stunden * 0,43 Gebührensatz für anteilmäßige Verrechnung = 43,86 Blockstunden nach anteilmäßiger Verrechnung
```

Die Gesamtkosten bleiben unverändert, Sie können jedoch mehr tatsächliche Blockstunden im Rahmen der anteilmäßig verrechneten Pläne nutzen, da diese weniger Blockstunden Ihres Reservierungsvertrags verbrauchen.
{:.tip}
