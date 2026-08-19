# Tema 29 — Fuentes

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
>
> **Criterio**: todo dato del contenido cita un **ID** inline (p. ej. `[RFC6143]`). Tier 1 = especificaciones técnicas de estándares abiertos (IETF, DMTF, ISO/IEC), marcos de referencia canónicos de gestión de servicios TI (ITIL 4, ISO/IEC 20000-1, COBIT 2019) y normativa española directamente aplicable (ENS, RGPD/LOPDGDD). Tier 2 = documentación de productos, herramientas y guías concretas, citada para ilustrar sin atar el tema a un único fabricante. Tier 3 = marco administrativo y organizativo de contexto, no citado como contenido técnico puro.

---

## Tier 1 — Especificaciones, marcos de referencia y normativa

| ID | Referencia |
|---|---|
| `[RFC6143]` | IETF. *RFC 6143: The Remote Framebuffer Protocol* (2011). Especificación del protocolo **RFB**, base de VNC: transmisión de *framebuffer* (píxeles) y eventos de teclado y ratón. Puerto de referencia TCP 5900. |
| `[RFC4251]` | IETF. *RFC 4251: The Secure Shell (SSH) Protocol Architecture* (2006). Arquitectura de SSH en tres capas: transporte, autenticación y conexión. |
| `[RFC4252]` | IETF. *RFC 4252: The Secure Shell (SSH) Authentication Protocol*. Métodos de autenticación: contraseña, clave pública, *host-based*. |
| `[RFC4253]` | IETF. *RFC 4253: The Secure Shell (SSH) Transport Layer Protocol*. Intercambio de claves, cifrado, integridad y autenticación del servidor. Puerto TCP 22. |
| `[RFC4254]` | IETF. *RFC 4254: The Secure Shell (SSH) Connection Protocol*. Multiplexación de canales, sesiones interactivas y **reenvío de puertos** (*port forwarding*, túneles). |
| `[RFC8446]` | IETF. *RFC 8446: The Transport Layer Security (TLS) Protocol Version 1.3* (2018). Cifrado del canal de las herramientas de asistencia remota y de las consolas web de gestión. |
| `[RFC5280]` | IETF. *RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile*. Certificados usados para autenticar servidores de mediación, agentes y puestos. |
| `[RFC4120]` | IETF. *RFC 4120: The Kerberos Network Authentication Service (V5)*. Autenticación mediante tiques (TGT/TGS) en dominios corporativos. Puerto 88. |
| `[RFC4511]` | IETF. *RFC 4511: Lightweight Directory Access Protocol (LDAP): The Protocol*. Directorio corporativo de identidades y grupos. Puertos 389 y 636 (sobre TLS). |
| `[RFC2865]` | IETF. *RFC 2865: Remote Authentication Dial In User Service (RADIUS)* y *RFC 2866 (Accounting)*. Modelo **AAA**: autenticación, autorización y contabilidad/registro. |
| `[RFC3411]` | IETF. *RFC 3411-3418: An Architecture for Describing SNMP Management Frameworks* (SNMPv3). Gestión y monitorización remota de dispositivos. Puertos UDP 161 (consultas) y 162 (*traps*). |
| `[RFC6241]` | IETF. *RFC 6241: Network Configuration Protocol (NETCONF)*. Configuración remota de dispositivos sobre SSH (puerto 830). |
| `[RFC9110]` | IETF. *RFC 9110: HTTP Semantics* (2022). Base de las consolas de gestión y de las API REST de las plataformas ITSM. |
| `[RFC862]` | IETF. *RFC 862: Echo Protocol* y *RFC 863: Discard Protocol*. Puertos UDP 7 y 9, usados convencionalmente como destino del paquete mágico de **Wake-on-LAN**. |
| `[DSP0226]` | DMTF. *Web Services for Management (WS-Management) Specification, DSP0226*. Estándar de gestión remota sobre servicios web, implementado por **WinRM**. |
| `[DSP0266]` | DMTF. *Redfish Scalable Platforms Management API Specification, DSP0266*. Gestión **fuera de banda** (*out-of-band*) sobre HTTPS/REST, sucesora de IPMI. |
| `[IPMI2]` | Intel/HP/NEC/Dell. *Intelligent Platform Management Interface Specification v2.0*. Gestión fuera de banda a través del controlador **BMC**, con el equipo apagado. Puerto UDP 623. |
| `[ITIL4]` | Axelos/PeopleCert. *ITIL 4 Foundation: ITIL 4 Edition* — Sistema de Valor del Servicio (SVS), cadena de valor, cuatro dimensiones, siete principios guía y las 34 **prácticas**, entre ellas *Service desk*, *Gestión de incidencias*, *Gestión de peticiones de servicio*, *Gestión de problemas*, *Monitorización y gestión de eventos*, *Gestión de niveles de servicio*, *Gestión del conocimiento* y *Mejora continua*. |
| `[ITILV3]` | Axelos. *ITIL Service Operation (edición 2011)*. Versión anterior del marco, en la que la gestión de incidencias es un **proceso** y el *Service Desk* una **función**; sigue siendo referencia habitual en temarios y pliegos. |
| `[ISO20000]` | ISO/IEC 20000-1:2018. *Tecnología de la información — Gestión del servicio — Parte 1: Requisitos del sistema de gestión del servicio (SGS)*. Norma **certificable**; su cláusula 8.6 (resolución y cumplimiento) exige gestión de incidencias, de peticiones de servicio y de problemas. |
| `[ISO27001]` | ISO/IEC 27001:2022 e ISO/IEC 27002:2022. *Sistemas de gestión de la seguridad de la información* y catálogo de controles (control de accesos, registro de eventos, gestión de incidentes de seguridad de la información). |
| `[COBIT2019]` | ISACA. *COBIT 2019 Framework: Governance and Management Objectives*. Objetivos **DSS01** (gestionar operaciones), **DSS02** (gestionar peticiones de servicio e incidentes), **DSS03** (gestionar problemas) y **DSS05** (gestionar servicios de seguridad). |
| `[ENS]` | Real Decreto **311/2022, de 3 de mayo**, por el que se regula el **Esquema Nacional de Seguridad**. Principios básicos, requisitos mínimos, dimensiones de seguridad, categorización de sistemas y medidas del Anexo II (marco organizativo, marco operacional y medidas de protección). |
| `[CCN-STIC]` | Centro Criptológico Nacional. *Guías CCN-STIC serie 800* — en particular **803** (valoración de sistemas), **804** (implantación del ENS) y **817** (gestión de ciberincidentes: taxonomía, peligrosidad e impacto, y notificación al CCN-CERT). |
| `[RGPD]` | Reglamento (UE) **2016/679** (RGPD). Principios del art. 5 (minimización, limitación de la finalidad, integridad y confidencialidad), art. 25 (protección desde el diseño y por defecto), art. 28 (encargado del tratamiento), art. 30 (registro de actividades), art. 32 (seguridad del tratamiento) y arts. 33-34 (notificación de brechas). |
| `[LOPDGDD]` | Ley Orgánica **3/2018**, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales. Deber de confidencialidad y derechos digitales en el ámbito laboral (arts. 87-91: intimidad frente al uso de dispositivos digitales y frente a la videovigilancia y la geolocalización). |
| `[ENI]` | Real Decreto **4/2010**, de 8 de enero, por el que se regula el **Esquema Nacional de Interoperabilidad**, y sus Normas Técnicas de Interoperabilidad. |
| `[L39-2015]` | Ley **39/2015**, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas. Derecho de la ciudadanía a relacionarse electrónicamente y a ser asistida en el uso de medios electrónicos. |
| `[L40-2015]` | Ley **40/2015**, de 1 de octubre, de Régimen Jurídico del Sector Público. Título preliminar, capítulo V: funcionamiento electrónico del sector público (sede, firma, archivo, seguridad e interoperabilidad). |

## Tier 2 — Herramientas, productos y guías concretas

| ID | Referencia |
|---|---|
| `[MS-RDPBCGR]` | Microsoft. *Remote Desktop Protocol: Basic Connectivity and Graphics Remoting (MS-RDPBCGR)*, Open Specifications. Protocolo **RDP**, puerto TCP/UDP 3389, canales virtuales y redirección de dispositivos. |
| `[MS-RDS]` | Microsoft. *Remote Desktop Services documentation* — sesiones, *Connection Broker*, *RD Gateway* (RDP sobre HTTPS), escritorios y aplicaciones publicadas. learn.microsoft.com. |
| `[MS-QUICKASSIST]` | Microsoft. *Quick Assist (Asistencia rápida)* y *Windows Remote Assistance*: asistencia **atendida** con código de sesión y consentimiento explícito del usuario. |
| `[MS-WINRM]` | Microsoft. *Windows Remote Management (WinRM)* y *PowerShell Remoting*. Implementación de WS-Management; puertos TCP 5985 (HTTP) y 5986 (HTTPS). |
| `[MS-INTUNE]` | Microsoft. *Microsoft Intune* y *Microsoft Configuration Manager (SCCM/MECM)*: inventario, despliegue de software, líneas base de configuración, parcheo y asistencia remota integrada. |
| `[MS-GPO]` | Microsoft. *Group Policy (directivas de grupo)* y *Active Directory Domain Services*: configuración centralizada del puesto y de los permisos de escritorio remoto. |
| `[OPENSSH]` | The OpenBSD Project. *OpenSSH Manual Pages* (`ssh`, `sshd`, `sshd_config`, `ssh-keygen`, `scp`, `sftp`). Implementación de referencia de SSH en sistemas Unix y Linux. |
| `[TIGERVNC]` | TigerVNC / RealVNC / x11vnc. Documentación de implementaciones del protocolo RFB y de sus modos de acceso (sesión de consola compartida frente a sesión virtual independiente). |
| `[XRDP]` | Proyectos *xrdp* y *X2Go*. Acceso a escritorios Linux mediante RDP o mediante el protocolo NX sobre SSH. |
| `[X11]` | X.Org Foundation. *X Window System Protocol, versión 11*. Modelo cliente-servidor **invertido** y reenvío de X11 sobre SSH (`ssh -X`). Puertos TCP 6000+N. |
| `[SPICE]` | Red Hat. *SPICE (Simple Protocol for Independent Computing Environments)*. Protocolo de acceso a escritorios de máquinas virtuales. |
| `[APPLE-ARD]` | Apple. *Apple Remote Desktop* y *Compartir pantalla* (basado en VNC/RFB con extensiones de autenticación de Apple). |
| `[VDI-VENDORS]` | Documentación de plataformas de virtualización del puesto: *Citrix Virtual Apps and Desktops* (protocolo ICA/HDX), *VMware Horizon* (Blast/PCoIP) y *Azure Virtual Desktop*. Citadas como ejemplos de VDI, RDSH y DaaS. |
| `[UEM]` | Documentación de plataformas de gestión unificada de dispositivos (**UEM/MDM**) y de inventario y despliegue: Intune, Jamf, Ivanti, GLPI con FusionInventory, OCS Inventory. |
| `[ANSIBLE]` | Red Hat. *Ansible Documentation* — gestión de configuración **sin agente** sobre SSH (Linux) o WinRM (Windows), con idempotencia. Alternativas: Puppet, Chef, Salt. |
| `[ITSM-TOOLS]` | Documentación de herramientas ITSM de registro y seguimiento de incidencias: ServiceNow, Jira Service Management, GLPI, Znuny/OTRS, BMC Remedy. Citadas como ejemplo de implementación de las prácticas de ITIL. |
| `[NAGIOS]` | Documentación de plataformas de monitorización y gestión de eventos: Nagios, Zabbix, Prometheus, Grafana. Origen de las incidencias detectadas automáticamente. |
| `[WSUS]` | Microsoft. *Windows Server Update Services* y equivalentes en Linux (repositorios internos, `apt`/`dnf` con réplica local). Distribución controlada de actualizaciones al puesto. |
| `[TPM20]` | Trusted Computing Group. *TPM 2.0 Library Specification*. Módulo de plataforma segura del puesto: almacenamiento de claves, cifrado de disco y arranque medido. |
| `[UEFI]` | UEFI Forum. *Unified Extensible Firmware Interface Specification* — arranque seguro (*Secure Boot*) y arranque por red **PXE** para el aprovisionamiento del puesto. |

## Tier 3 — Marco administrativo y organizativo (contexto)

| ID | Referencia |
|---|---|
| `[IAM-MAD]` | Organismo Autónomo **Informática del Ayuntamiento de Madrid (IAM)** — organismo responsable de los sistemas de información y del soporte al puesto de trabajo municipal. Contexto institucional de los ejemplos del tema. |
| `[ROGA]` | Reglamento Orgánico del Gobierno y de la Administración del Ayuntamiento de Madrid, de 31 de mayo de 2004. Áreas de Gobierno y Distritos: estructura sobre la que se distribuye el parque de puestos de usuario. Ver Temas 3 y 4. |
| `[TRANSP-MAD]` | Portal de Transparencia y sede electrónica del Ayuntamiento de Madrid. Servicios electrónicos municipales a los que da soporte el puesto de usuario. |
| `[BOAM10032]` | BOAM 10.032 (23-dic-2025). Bases específicas TIC C1 Ayto. Madrid — temario oficial y estructura del ejercicio. |

---

*Las referencias Tier 1 fijan el fundamento del tema por sus dos mitades: por el lado técnico, las especificaciones de los protocolos con los que se toma control de un puesto o se gestiona a distancia (RFB, SSH, TLS, Kerberos, LDAP, SNMP, WS-Management, Redfish/IPMI); por el lado organizativo, los marcos canónicos de gestión de servicios TI (ITIL 4, ISO/IEC 20000-1, COBIT 2019) y la normativa española que condiciona cualquier asistencia remota en el sector público (ENS, RGPD y LOPDGDD). Tier 2 documenta productos y herramientas concretas —RDP, VNC, OpenSSH, WinRM, Intune, plataformas VDI y suites ITSM— citadas como ejemplos sin que el tema dependa de ninguna en particular; el opositor debe reconocer el mecanismo, no memorizar una marca. Tier 3 sitúa el supuesto municipal: el IAM como responsable del soporte al puesto de trabajo del Ayuntamiento de Madrid y los servicios electrónicos a los que ese puesto da servicio.*
