---

copyright:
  years: 2017, 2018
lastupdated: "2018-12-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Latest updates
{: #latest_updates}

A list of the latest updates to the service.


## December 14, 2018: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* The 9.0.0.10 fix pack of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 9.0.0.10, other fix packs of traditional WebSphere Application Server, such as 9.0.0.9, 8.5.5.14, and 8.5.5.13, are available for provisioning.
* The 18.0.0.4 fix pack version of WebSphere Application Server Liberty is now available when you provision a new service instance. In addition to 18.0.0.4, the 18.0.0.3 fix pack version of WebSphere Application Server Liberty is available for provisioning.
* Integrated miscellaneous service maintenance.

## October 24, 2018: Bring-your-own-license billing now available for reserve contract and Single Tenant environments

If you have existing WebSphere Application Server licenses, you can now use these licenses in your reserve contract or Single Tenant environments. Environments with bring-your-own-license billing offer the same benefits as the standard reserve contract or Single Tenant environments, but are billed at a reduced rate. To use bring-your-own licensing, [contact IBM sales](reportingIssues.html#contacting-sales).

## August 22, 2018: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* The 8.5.5.14 fix pack of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 8.5.5.14, other fix packs of traditional WebSphere Application Server, such as 9.0.0.8, 9.0.0.7, and 8.5.5.13, are available for provisioning.
* Integrated miscellaneous service maintenance.

## July 16, 2018: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* The 9.0.0.8 fix pack version of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 9.0.0.8, other fix pack versions of traditional WebSphere Application Server, such as 9.0.0.7, 8.5.5.13, and 8.5.5.12, are available for provisioning.
* The 18.0.0.2 fix pack version of WebSphere Application Server Liberty is now available when you provision a new service instance. In addition to 18.0.0.2, the 18.0.0.1 fix pack version of WebSphere Application Server Liberty is available for provisioning.
* Addressed [several security vulnerabilities](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window} in the IBM SDK Java Technology Edition that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.

## June 13, 2018: Reserve contract billing now available

With reserve contract billing, you purchase a pre-paid monthly subscription that guarantees access to blocks of physically reserved computational resources. These service blocks are set aside for your exclusive use and cannot be considered as available capacity for any other {{site.data.keyword.appserver_full}} users. You can use your service block hours in any way you choose throughout the month, with any overages being charged according to the typical pay-as-you-go subscription model.

To learn more about reserve contract billing, see [Billing options](index.html#billing-options).

## March 30, 2018: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* The 9.0.0.7 fix pack version of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 9.0.0.7, other fix pack versions of traditional WebSphere Application Server, such as 9.0.0.6, 8.5.5.13, and 8.5.5.12, are available for provisioning.
* The 18.0.0.1 fix pack version of WebSphere Application Server Liberty is now available when you provision a new service instance. In addition to 18.0.0.1, the 17.0.0.4 fix pack version of WebSphere Application Server Liberty is available for provisioning.
* Addressed [several security vulnerabilities]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * Multiple Vulnerabilities in IBM® Java SDK
  * A vulnerability where IBM WebSphere Application Server could provide weaker than expected security for the Administrative Console.
  * A vulnerability where IBM WebSphere Application Server installations that use Form Login could allow a remote attacker to conduct spoofing attacks.
  * A vulnerability where IBM WebSphere Application Server could allow a local attacker to obtain sensitive information, caused by improper handling of application requests, which could allow unauthorized access to read a file.
  * A vulnerability where Apache Commons FileUpload, as used in several products, could allow a remote attacker to execute arbitrary code on the system, caused by deserialization of untrusted data in DiskFileItem class of the FileUpload library. A remote attacker could exploit this vulnerability to execute arbitrary code under the context of the current process.
  * A vulnerability where Intel Haswell Xeon, AMD PRO and ARM Cortex A57 CPUs could allow a local authenticated attacker to obtain sensitive information, caused by a bounds check bypass in the CPU speculative branch instruction execution feature. By conducting targeted cache side-channel attacks, an attacker could exploit this vulnerability to cross the syscall boundary and read data from the CPU virtual memory.
* Integrated miscellaneous service maintenance.

## January 8, 2018: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* The 9.0.0.6 fix pack version of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 9.0.0.6, other fix pack versions of traditional WebSphere Application Server, such as 9.0.0.5, 8.5.5.12, and 8.5.5.11, are available for provisioning.
* The 17.0.0.4 fix pack version of WebSphere Application Server Liberty is now available when you provision a new service instance. In addition to 17.0.0.4, the 17.0.0.3 fix pack version of WebSphere Application Server Liberty is available for provisioning.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability where OpenSAML could allow a remote authenticated attacker to obtain sensitive information, caused by an error when parsing XML entities.
  * A vulnerability where Apache HTTP Server could allow a remote attacker to obtain sensitive information, caused by a flaw in the HTTP OPTIONS method called Optionsbleed.
  * A vulnerability where Apache Portable Runtime Utility (APR-util) is vulnerable to a denial of service, caused by failing to validate the integrity of SDBM database files used by apr_sdbm*() functions.
* Integrated miscellaneous service maintenance.

## December 21, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Added the WebSphere Application Server in IBM Cloud Migration Feature in Dallas, London & Sydney. This feature provides complete end-to-end migration from existing v7, v8, or v8.5.5 on-premises environments to v9 environments in IBM Cloud. For more information, see the [WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud).
* Integrated miscellaneous service maintenance.

## October 27, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Added the ability to provision an older fix pack level [(n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} through the Service Profile tab in the {{site.data.keyword.Bluemix_notm}} Service Dashboard or via the REST API.
* The 9.0.0.5 fix pack version of traditional WebSphere Application Server is now available when you provision a new service instance. In addition to 9.0.0.5, other fix pack versions of traditional WebSphere Application Server, such as 9.0.0.4, 8.5.5.12, and 8.5.5.11, are available for provisioning.
* The 17.0.0.3 fix pack version of WebSphere Application Server Liberty is now available when you provision a new service instance. In addition to 17.0.0.3, the 17.0.0.2 fix pack version of WebSphere Application Server Liberty is available for provisioning.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability where IBM WebSphere Application Server might create files by using the default permissions instead of the customized permissions when custom startup scripts are used.
  * A vulnerability where IBM WebSphere Application Server Proxy Server or On-demand-router (ODR) could allow a local attacker to obtain sensitive information, caused by stale data being cached and then served.
  * A vulnerability where IBM WebSphere Application Server is vulnerable to cross-site scripting. This vulnerability allows users to embed arbitrary JavaScript code in the Web UI thus altering the intended functionality potentially leading to credentials disclosure within a trusted session.
  * A vulnerability where IBM WebSphere Application Server could provide weaker than expected security after you use the Admin Console to update the web services security bindings settings.
  * A vulnerability where IBM WebSphere Application Server Version 9.0.0.4 could provide weaker than expected security after you use the PasswordUtil command to enable AES password encryption.
  * A vulnerability where Apache MyFaces could allow a remote attacker to obtain sensitive information.
  * A vulnerability where IBM WebSphere Application Server could allow a remote attacker to obtain sensitive information caused by improper error handling by MyFaces in JSF.
* Integrated miscellaneous service maintenance.

## August 30, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.

## June 30, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} such that fix pack 8.5.5.12 or 9.0.0.4 is installed with new instances of Traditional WebSphere Application Server.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} such that fix pack 17.0.0.2 is installed with new instances of WebSphere Application Server Liberty (Core and ND Plans).
* Added an [Advanced VPN Configuration Management](networkEnvironment.html#advancedVPN){: new_window} feature that you can use to create and manage multiple VPN configurations in the London and Sydney regions.
* Added enhancements to the [Public Internet Access](networkEnvironment.html#publicInternetAccess){: new_window} feature that allows clients to better manage their public IP address.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window} in the IBM SDK Java Technology Edition that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * An unspecified vulnerability for the Java SE AWT component that could allow an unauthenticated attacker to take control of the system.
  * An unspecified vulnerability for the Java SE JCE component that could allow an unauthenticated attacker to take control of the system.
  * An unspecified vulnerability for the Java SE JAXP component that could allow an unauthenticated attacker to cause a denial of service, resulting in a high availability impact by using unknown attack vectors.
  * An unspecified vulnerability for the Java SE Networking component that could allow an unauthenticated attacker to cause low confidentiality impact, low integrity impact, and no availability impact.
  * An unspecified vulnerability for the Java SE Networking component that could allow an unauthenticated attacker to cause no confidentiality impact, low integrity impact, and no availability impact.
  * An unspecified vulnerability for the Java SE Security component that could allow an unauthenticated attacker to cause no confidentiality impact, low integrity impact, and no availability impact.
  * A vulnerability to an XML External Entity Injection (XXE) error when processing XML data. A remote attacker could exploit this vulnerability to expose highly sensitive information or consume memory resources.
  * An issue where zlib is vulnerable to a denial of service, caused by an out-of-bounds pointer arithmetic in inftrees.c.
  * An issue where zlib is vulnerable to a denial of service, caused by an undefined left shift of a negative number.
  * An issue where zlib is vulnerable to a denial of service, caused by a big-endian out-of-bounds pointer.

## May 25, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Added an [Advanced VPN Configuration Management](networkEnvironment.html#advancedVPN){: new_window} feature that you can use to create and manage multiple VPN configurations in the Frankfurt region.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  such that JDK 8 is installed with all new instances of the service.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A potential security vulnerability with the WebSphere Application Server MQ JCA Resource adapter.
  * An unspecified vulnerability for the Libraries component that could allow a remote attacker to obtain sensitive information, resulting in a high confidentiality impact by using unknown attack vectors.

## April 21, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability where WebSphere Application Server configured with OpenID Connect (OIDC) Trust Association Interceptor (TAI) could allow a user to gain elevated privileges on the system.
  * A vulnerability where WebSphere Application Server could provide weaker than expected security. A remote attacker could exploit this weakness to obtain sensitive information and gain unauthorized access to the admin console.
  * An issue where WebSphere Application Server is vulnerable to cross-site request forgery, which could allow an attacker to execute malicious and unauthorized actions transmitted from a user that the website trusts.


## March 15, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  such that fix pack 8.5.5.11 or 9.0.0.3 is installed with new instances of Traditional WebSphere Application Server.
* Addressed [several security vulnerabilities](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * An unspecified vulnerability for the Libraries component that has no confidentiality impact, high integrity impact, and no availability impact.
  * An unspecified vulnerability for the Libraries component that could allow a remote attacker to obtain sensitive information, resulting in a high confidentiality impact by using unknown attack vectors.
  * An unspecified vulnerability for the Libraries component that could allow a remote attacker to cause a denial of service, resulting in a low availability impact by using unknown attack vectors.
  * A vulnerability in OpenSSL that could allow a remote attacker to obtain sensitive information, caused by an error in the DES/3DES cipher, used as a part of the SSL/TLS protocol.
  * A vulnerability that allows users to embed arbitrary JavaScript code in the Web UI, thus altering the intended functionality potentially leading to credentials disclosure within a trusted session.
  * A vulnerability in Apache HTTPD to HTTP response splitting attacks, caused by improper validation of user-supplied input.
  * A vulnerability in Samba that could allow a remote authenticated attacker to gain elevated privileges on the system, caused by the failure of handling the PAC checksum.
  * A vulnerability in Samba that could allow a remote authenticated attacker to gain elevated privileges on the system, caused by forwarding a Ticket Granting Ticket (TGT) to other service you use Kerberos authentication.
  * A vulnerability in Samba to a heap-based buffer overflow, caused by an integer wrap flaw in the ndr_pull_dnsp_name() function.


## February 10, 2017: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  such that fix pack 8.5.5.11 or 9.0.0.2 is installed with new instances of Traditional WebSphere Application Server.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  such that fix pack 16.0.0.4 is installed with new instances of WebSphere Application Server Liberty (Core and ND Plans).
* Addressed [several security vulnerabilities](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability to denial of service, caused by allowing serialized objects from untrusted sources to run and cause the consumption of resources.
  * The use of malformed SOAP requests that could allow a remote attacker to obtain sensitive information.


## December 16, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Integrated miscellaneous service maintenance.
* Addressed [several security vulnerabilities](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window} in the IBM SDK Java Technology Edition that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * An unspecified vulnerability in Oracle Java SE and Java SE Embedded related to the Hotspot component that has high confidentiality impact, high integrity impact, and high availability impact.
  * An unspecified vulnerability in Oracle Java SE and Java SE Embedded related to the Networking component that could allow a remote attacker to obtain sensitive information resulting in a high confidentiality impact by using unknown attack vectors.
  *  A cross-site scripting vulnerability in IBM WebSphere Application Server that allows users to embed arbitrary JavaScript code in the Web UI. The code can alter the intended functionality potentially, leading to credentials disclosure within a trusted session.


## November 8, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Added ability for clients to request a [Public IP](networkEnvironment.html#networkEnvironment) address for their WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window} that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability in IBM WebSphere Application Server that could allow remote attackers to execute arbitrary Java code with a serialized object from untrusted sources.
  * A denial-of-service vulnerability that is caused by an out-of-bounds read in the TS_OBJ_print_bio function. A remote attacker could exploit this vulnerability by using a specially crafted time-stamp file to cause the application to crash.
  * A potential vulnerability in OpenSSL that could allow a remote attacker to obtain sensitive information, caused by an error in the Triple-DES on 64-bit block cipher, used as a part of the SSL/TLS protocol. By capturing large amounts of encrypted traffic between the SSL/TLS server and the client, a remote attacker able to conduct a man-in-the-middle attack could exploit this vulnerability to recover the plaintext data and obtain sensitive information. This vulnerability is known as the SWEET32 Birthday attack.
  * OpenSSL is vulnerable to a denial of service. By repeatedly requesting renegotiation, a remote authenticated attacker could send an overly large OCSP Status Request extension to consume all available memory resources.
  * OpenSSL is vulnerable to a denial of service, caused by an integer overflow in the MDC2_Update function. By using unknown attack vectors, a remote attacker could exploit this vulnerability to trigger an out-of-bounds write and cause the application to crash.
  * A potential vulnerability in OpenSSL that allows a remote attacker to obtain sensitive information, caused by an error in the DSA implementation that allows the following of a non-constant time codepath for certain operations. An attacker could exploit this vulnerability by using a cache-timing attack to recover the private DSA key.
  * OpenSSL is vulnerable to a denial of service, caused by missing message length checks when parsing certificates. A remote authenticated attacker could exploit this vulnerability to trigger an out-of-bounds read and cause a denial of service.

## September 19, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  so that new instances of WebSphere Application Server Liberty (Core and ND Plans) use fix pack 16.0.0.3.
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window} that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * A vulnerability in IBM WebSphere Application Server Liberty that could allow a remote attacker to conduct phishing attacks.
  * A vulnerability in IBM WebSphere Application Server Liberty to cross-site scripting in OpenID Connect clients.
  * A potential vulnerability in IBM WebSphere Application Server Liberty that could allow a remote attacker to obtain sensitive information caused by improper handling of exceptions when a default error page does not exist.
  * A vulnerability in Apache Tomcat to a denial of service, caused by an error in the Apache Commons FileUpload component.
  * A vulnerability in IBM WebSphere Application Server and IBM WebSphere Application Server Liberty that could allow a remote attacker to obtain sensitive information, caused by the improper handling of responses under certain conditions.
  * An unspecified vulnerability for the Networking component that has no confidentiality impact, low integrity impact, and no availability.

## August 17, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  from 8.5.5.9 to 8.5.5.10
* Addressed [several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window} that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * Apache Struts vulnerabilities that affect the WebSphere Application Server and WebSphere Application Server Hypervisor Edition Administration Console.
  * A potential denial of service vulnerability with IBM WebSphere Application Server you use SIP services.
  * Several vulnerabilities that may affect the IBM HTTP Server used by WebSphere Application Server.
  * A vulnerability that allows redirecting of HTTP traffic with CGI applications that may affect IBM HTTP Server (IHS). This vulnerability is known as "HTTPOXY".
  * An Information Disclosure Vulnerability in IBM WebSphere Application Server.
  * A potential bypass security restriction vulnerability in IBM WebSphere Application Server that only occurs in environments that have the web container custom property `HttpSessionIdReuse` enabled.


## June 24, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Added ability for clients to choose between V8.5 and V9.0 when you create a new _Traditional ND_ or _Traditional WebSphere_ instance.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  so that new instances of WebSphere Application Server Liberty (Core and ND Plans) use fix pack 16.0.0.2. 16.0.0.2 is the next fix pack after 8.5.5.9. As of 16.0.0.2, all entitled Liberty optional features that are supported for these plans are installed by default.
* Addressed [Several security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window} that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} including:
  * An XML External Entity Injection (XXE) vulnerability in the Apache Standard Taglibs that affects IBM WebSphere Application Server.
  * A potential for weaker than expected security for the WebSphere Application Server Liberty profile API Discovery feature and Swagger documents.
  * A potential information disclosure vulnerability in Admin Center for IBM WebSphere Application Server Liberty.
  * A potential HTTP response splitting vulnerability in IBM WebSphere Application Server.
  * OpenSSL vulnerabilities disclosed on May 3, 2016 by the OpenSSL Project.

## June 13, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Added ability for clients to build, provision, manage, and delete virtual machine instances through the creation of an application or script that uses WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} RESTful APIs.
* Added function that allows a client to have a fixed number of STOPPED instances with no more than 10 IP addresses or 64 GB of memory. Clients are now charged for accumulated instances in the STOPPED state at a reduced rate of 5%.

## April 26, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Addressed  [potential security vulnerabilities](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} if FIPS 140-2 is enabled and multiple vulnerabilities in Samba - including Badlock.
* Integrated miscellaneous service maintenance.

## April 15, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} from 8.5.5.8 to 8.5.5.9
* Addressed a [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window} vulnerability in Liberty for Java for {{site.data.keyword.Bluemix_notm}} that affects consumers that use the OpenID Connect (OIDC) client.
* Integrated miscellaneous service maintenance.

## February 19, 2016: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Added an option for clients with memory-intensive applications to "right-size" their environment with larger virtual machines. Clients can select the specific resource size of a given WebSphere Application Server component or single system up to 32 GB RAM virtual machines.
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} from 8.5.5.7 to 8.5.5.8
* Addressed multiple vulnerabilities in IBM SDK Java Technology Edition that affect WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} that are commonly referred to as [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}.
* Addressed a [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window} vulnerability that affects consumers of the OAuth provider output.
* Integrated miscellaneous service maintenance.

## December 11, 2015: Updated WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Changed the official product name from IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} to IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Added new capabilities to the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment plan. The plan consists of a WebSphere Application Server Network Deployment cell environment with two or more virtual machines. These new capabilities allow users to set up a clustered environment for high availability, failover, and scalability.
* Added new capabilities to the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core plan. The plan includes the use of a Liberty Collective, which is an administrative domain for a group of Liberty profiles (servers) and consists of two or more virtual machines
* Upgraded the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} from 8.5.5.6 to 8.5.5.7
* Addressed an [Apache Commons Collections vulnerability](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window} for handling Java object deserialization.
* Addressed a vulnerability that could allow an [HTTP response splitting attack](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}.
* Integrated miscellaneous service maintenance.

## October 15, 2015: Updated Application Server on Cloud
* Added the following two new plans:
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* Miscellaneous service maintenance
