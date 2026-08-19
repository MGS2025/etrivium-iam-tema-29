# Tema 29 — Índice

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
>
> **Bloque**: Parte II — Técnico (Temas 11-40)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

---

## Estructura del tema

1. **El puesto de usuario y la asistencia técnica remota**
   1.1. Arquitectura y modelos del puesto de trabajo digital
   1.1.1. Entornos de escritorio tradicionales y virtualizados
   1.1.2. Componentes hardware y software del puesto de usuario
   1.2. Fundamentos del control remoto
   1.2.1. Arquitecturas cliente-servidor y punto a punto
   1.2.2. Mecanismos de autenticación, autorización y sesión
   1.3. Protocolos y tecnologías de control remoto
   1.3.1. Protocolos de nivel de aplicación para gestión remota
   1.3.2. Canales de comunicación seguros y cifrado
   1.3.3. Herramientas de asistencia remota en sistemas operativos
   1.3.4. Soluciones centralizadas de gestión de puestos de trabajo

2. **Gestión de la resolución de incidencias en los servicios TI**
   2.1. Marcos de referencia para la gestión de servicios TI
   2.1.1. Principios de ITIL aplicados a la gestión de incidencias
   2.1.2. Ciclo de vida y flujos de trabajo de atención al usuario
   2.2. El Centro de Atención a Usuarios (CAU)
   2.2.1. Funciones, modelos organizativos y niveles de soporte
   2.2.2. Canales de entrada, registro y categorización
   2.3. Proceso de gestión y resolución de incidencias
   2.3.1. Priorización, impacto y urgencia
   2.3.2. Diagnóstico, escalado funcional y jerárquico
   2.3.3. Resolución, restablecimiento del servicio y cierre
   2.3.4. Matriz de escalado y Acuerdos de Nivel de Servicio (SLA)
   2.4. Gestión de peticiones de servicio y eventos
   2.4.1. Diferencias entre incidencia, problema y petición
   2.4.2. Integración de la gestión de incidencias con la gestión de problemas

3. **Marco normativo, seguridad y calidad en la Administración Pública**
   3.1. Seguridad en la asistencia remota
   3.1.1. Control de accesos y principio de mínimo privilegio
   3.1.2. Trazabilidad, auditoría y registro de actividades de asistencia
   3.2. Cumplimiento normativo y Esquema Nacional de Seguridad
   3.2.1. Requisitos del Esquema Nacional de Seguridad (ENS)
   3.2.2. Protección de datos personales en la atención de incidencias
   3.3. Medición y mejora continua del servicio
   3.3.1. Indicadores clave de rendimiento (KPI) y métricas de servicio
   3.3.2. Gestión del conocimiento y base de soluciones

---

## Conceptos clave para memorizar

| Concepto | Dato clave |
|---|---|
| Incidencia (ITIL) | **Interrupción no planificada** de un servicio o **reducción de su calidad**. Objetivo de su gestión: **restablecer el servicio lo antes posible**, no averiguar la causa |
| Problema (ITIL) | **Causa, o causa potencial**, de una o varias incidencias. Su gestión sí busca la **causa raíz** y produce **errores conocidos** y **soluciones temporales** (*workarounds*) |
| Petición de servicio | Solicitud **prevista y acordada** en la prestación normal del servicio (alta de usuario, restablecer contraseña, instalar software del catálogo). **No hay interrupción** |
| Evento | **Cambio de estado significativo** de un elemento de configuración o servicio. Tipos: **informativo**, **advertencia** y **excepción**; solo la excepción suele generar incidencia |
| Prioridad | **Prioridad = impacto × urgencia**. El **impacto** mide a cuánto afecta (personas, servicios, criticidad); la **urgencia**, con qué rapidez se degrada si no se actúa |
| Escalado funcional | **Horizontal**: se pasa a un grupo con **más conocimiento técnico** (N1 → N2 → N3). No implica más autoridad |
| Escalado jerárquico | **Vertical**: se avisa a un **nivel de autoridad superior** para decidir, autorizar o aportar recursos. No implica más conocimiento técnico |
| SLA / OLA / UC | **SLA** con el cliente o usuario del servicio; **OLA** entre equipos **internos** de la propia organización; **UC** (contrato de soporte) con un **proveedor externo**. Los OLA y los UC deben sostener el SLA |
| RFB (VNC) | **RFC 6143**. Transmite el **framebuffer** (píxeles) y eventos de teclado y ratón; independiente del sistema operativo; **comparte la sesión de consola**. Puerto TCP **5900** |
| RDP | Microsoft, puertos TCP/UDP **3389**. Transmite **primitivas gráficas y canales virtuales** (no píxeles en bruto); crea por defecto una **sesión independiente** y redirige impresoras, discos y portapapeles |
| SSH | **Puerto TCP 22**, RFC 4251-4254. Terminal remoto **cifrado y autenticado**, con **túneles** y transferencia de ficheros (SCP/SFTP). Sustituye a **Telnet** (puerto 23, texto en claro) |
| WinRM | Implementación Microsoft de **WS-Management**; puertos **5985** (HTTP) y **5986** (HTTPS). Base de *PowerShell Remoting* |
| Gestión fuera de banda | **IPMI/BMC** (UDP 623) y **Redfish** (HTTPS/REST): permiten actuar sobre el equipo **apagado o con el sistema operativo caído**, por una vía independiente |
| Wake-on-LAN | **Paquete mágico** enviado a los puertos UDP **7 o 9** que enciende el equipo por red para parchearlo o darle soporte fuera del horario laboral |
| Atendido / desatendido | **Atendido**: el usuario está delante y **consiente** cada sesión. **Desatendido**: el agente permite conectarse sin usuario; exige controles reforzados y justificación |
| VDI / RDSH / DaaS | **VDI**: una máquina virtual completa por usuario. **RDSH**: sesiones múltiples sobre un mismo servidor. **DaaS**: lo anterior consumido como servicio en la nube |
| Dimensiones ENS | **Disponibilidad, Autenticidad, Integridad, Confidencialidad y Trazabilidad**. Categorías del sistema: **BÁSICA, MEDIA y ALTA** [ENS] |
| Mínimo privilegio | Cada técnico debe tener **solo** los permisos imprescindibles y **solo** durante el tiempo necesario; se apoya en RBAC, segregación de funciones y elevación temporal |
| KPI del CAU | **FCR** (resolución en primer contacto), **MTTR** (tiempo medio de restablecimiento), **ASA** (tiempo medio de respuesta), **cumplimiento de SLA**, **tasa de reapertura**, **CSAT** |
| Base de conocimiento | Convierte cada resolución en **conocimiento reutilizable**; alimenta el autoservicio (N0) y eleva la **FCR** sin aumentar la plantilla |

---

*Tiempo estimado de estudio: 14-16 horas*
*Extensión del contenido: ~21.100 palabras · 16 diagramas SVG embebidos*
