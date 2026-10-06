# Tema 29 — Checklist de Validación

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
> **Versión**: v1.0 — Pendiente validación
> **Fecha**: 2026-08-20
> **Revisores**: María y Ana (eTrivium) · revisión técnica IAM (Jesús Cuadrado)
> **Instrucciones**: marcar cada ítem. Los cambios no se guardan en la web (imprimir o exportar a PDF si se desea fijarlos).

---

## 1. Cobertura del temario oficial

- [ ] **Arquitectura y modelos del puesto**: escritorios tradicionales y virtualizados (VDI, RDSH, DaaS), componentes hardware y software — §1.1
- [ ] **Fundamentos del control remoto**: arquitecturas cliente-servidor y punto a punto, autenticación, autorización y sesión — §1.2
- [ ] **Protocolos de nivel de aplicación** para gestión remota: RFB, RDP, SSH, WinRM, SNMP, NETCONF, IPMI/Redfish, X11, Wake-on-LAN — §1.3.1
- [ ] **Canales seguros y cifrado**: TLS, SSH, tunelización, fortificación del canal de asistencia — §1.3.2
- [ ] **Herramientas de asistencia en sistemas operativos**: Windows, Unix/Linux, macOS y multiplataforma — §1.3.3
- [ ] **Soluciones centralizadas de gestión de puestos**: inventario, despliegue, configuración, parcheo, seguridad y soporte — §1.3.4
- [ ] **Marcos de referencia**: ITIL 4, ISO/IEC 20000-1, COBIT 2019; ciclo de vida y flujos de trabajo — §2.1
- [ ] **El CAU**: funciones, modelos organizativos, niveles de soporte, canales, registro y categorización — §2.2
- [ ] **Proceso de gestión de incidencias**: priorización, diagnóstico, escalado, resolución, cierre, matriz de escalado y SLA — §2.3
- [ ] **Peticiones de servicio y eventos**: diferencias entre incidencia, problema y petición; integración con la gestión de problemas — §2.4
- [ ] **Seguridad en la asistencia remota**: control de accesos, mínimo privilegio, trazabilidad y auditoría — §3.1
- [ ] **Cumplimiento normativo**: requisitos del ENS y protección de datos personales en la atención de incidencias — §3.2
- [ ] **Medición y mejora continua**: KPI y métricas, gestión del conocimiento y base de soluciones — §3.3

## 2. Contenido teórico

- [ ] El nivel de profundidad (3 secciones, 34 epígrafes, ~21.100 palabras) es adecuado para C1 (¿hay que ampliar o recortar alguna sección?)
- [ ] El **equilibrio entre las dos mitades del tema** —la técnica (§1) y la organizativa (§2)— es el correcto: ¿debería pesar más una de las dos, dado que el enunciado oficial les da el mismo rango?
- [ ] Las **distinciones nucleares** quedan nítidas y sin ambigüedad: control remoto / acceso remoto / gestión remota; atendido / desatendido; dentro de banda / fuera de banda; VNC (píxeles, sesión compartida) / RDP (primitivas, sesión independiente); incidencia / problema / error conocido / petición / evento; escalado funcional / jerárquico; SLA / OLA / UC; impacto / urgencia; respuesta / resolución
- [ ] Los **puertos y números de RFC** citados son correctos y están actualizados (5900, 3389, 22, 23, 5985/5986, 161/162, 830, 623, 443, 6000+N, 7/9)
- [ ] La descripción de **ITIL 4** (SVS, cadena de valor, cuatro dimensiones, siete principios guía, prácticas frente a procesos) es fiel y su contraste con ITIL v3 es útil y no confuso
- [ ] Los datos del **ENS (RD 311/2022)** son correctos: cinco dimensiones, tres niveles, tres categorías, bloques de medidas del Anexo II, auditoría bienal para media y alta, autoevaluación para básica, figuras de responsable
- [ ] Las referencias al **RGPD y a la LOPDGDD** son correctas: arts. 5, 25, 28, 30, 32, 33-34 RGPD y arts. 87-91 LOPDGDD; plazo de 72 horas para la notificación de brechas
- [ ] Los bloques añadidos más allá del enunciado literal del esqueleto (gestión fuera de banda, Wake-on-LAN, modelos organizativos del CAU, flujos diferenciados de incidencia grave y de seguridad, malas prácticas de medición) aportan valor y no desbordan el nivel C1
- [ ] La frontera con los Temas 11 y 12 (arquitectura y periféricos), 14 (sistemas operativos), 27 (administración del SO), 28 (virtualización), 30 (administración de redes locales), 31 (cloud), 32 (seguridad de sistemas), 34 y 35 (TCP/IP, HTTP/TLS), 36 (acceso remoto seguro y VPN) y 39 (ENS/ENI) está clara y sin duplicidades innecesarias
- [ ] Los ejemplos Ayto Madrid (CAU municipal, Oficinas de Atención a la Ciudadanía, firma electrónica en la tramitación) son verosímiles y coherentes entre secciones
- [ ] **Especialmente a validar por el IAM**: la distinción que hace §2.2.1 entre el **CAU interno** (atiende a empleados municipales) y los **servicios de atención a la ciudadanía** es correcta en su formulación general y no atribuye al Ayuntamiento de Madrid ninguna estructura organizativa concreta que no proceda

## 3. Fuentes

- [ ] Todas las afirmaciones técnicas están respaldadas por fuente Tier 1 (IETF, DMTF, ISO/IEC, ITIL 4, ENS, RGPD)
- [ ] Las referencias inline se corresponden con `tema-29-fuentes.md`
- [ ] Los productos concretos citados (RDP, VNC, OpenSSH, WinRM, Intune, plataformas VDI y suites ITSM) figuran como **ejemplos ilustrativos** y el tema no depende de ninguna marca

## 4. Test (60 preguntas)

- [ ] Cada pregunta tiene una sola respuesta correcta e inequívoca
- [ ] Los distractores (A/B/C) son plausibles
- [ ] La distribución de la opción correcta entre A/B/C está equilibrada (**verificada 20/20/20** por el generador)
- [ ] Las explicaciones y referencias de cada respuesta son correctas
- [ ] El reparto por bloques (P1-P10 puesto y fundamentos, P11-P22 protocolos y herramientas, P23-P32 marcos y CAU, P33-P44 proceso y SLA, P45-P50 peticiones y problemas, P51-P60 seguridad, ENS, datos y KPI) es proporcionado al peso de cada sección

## 5. Casos prácticos (3)

- [ ] Realistas y propios del Ayuntamiento (diagnóstico y asistencia remota en una Oficina de Atención a la Ciudadanía; priorización, escalado y SLA ante una caída del servicio de firma; seguridad, cumplimiento y mejora continua en la licitación del soporte)
- [ ] Soluciones orientativas técnica y jurídicamente correctas
- [ ] La puntuación de cada caso suma 10 puntos

## 6. Diagramas (16 SVG)

- [ ] Cada diagrama es correcto y legible (también impreso en blanco y negro)
- [ ] Accesibilidad: todos tienen `role="img"` y `aria-label`
- [ ] Sin desbordes de texto ni colisiones de estilo entre SVG (clases con sufijo único, QA de caja contenedora con render en navegador)
- [ ] D5 (mapa de protocolos y puertos) y D13 (matriz impacto × urgencia) son los dos diagramas de memorización directa: verificar cifra a cifra

## 7. Referencias cruzadas a otros temas

- [ ] Validadas contra BOAM 10.032 (T11, T12, T14, T27, T28, T30, T31, T32, T34, T35, T36, T39)
- [ ] Ninguna referencia cruzada cita un enunciado de tema incorrecto

## 8. Calidad editorial

- [ ] Ortografía verificada (tildes y ñ) — sin diacríticos perdidos, también dentro de los `aria-label` de los SVG
- [ ] Coherencia de versión (v1.0) en title, badges, banner y footer del `index.html`
- [ ] El `index.html` abre, navega entre las 8 pestañas y el motor de test funciona
- [ ] Las listas anidadas del Contenido se muestran con sus niveles (sin aplanar)
- [ ] Las tablas comparativas se muestran correctamente y sin markdown crudo filtrado

---

## Observaciones abiertas

_(Espacio para anotaciones de María, Ana y la revisión IAM.)_

- Pendiente confirmar con el IAM si interesa **desarrollar más la parte de virtualización del puesto** (§1.1.1) o si conviene dejarla apuntada aquí y remitirla íntegramente al **Tema 28**, evitando duplicidad.
- Pendiente confirmar si conviene detallar el **catálogo de medidas del Anexo II del ENS** medida a medida en §3.2.1, o si el nivel actual —bloques y grupos, con las medidas relevantes citadas— es el adecuado al existir ya el **Tema 39** dedicado al ENS y al ENI.
- Los **valores de tiempo del SLA** de §2.3.4 y de D13 son **ilustrativos**. Si el IAM facilita los tiempos reales comprometidos en su contrato de soporte al puesto, conviene sustituirlos para que el opositor estudie las cifras reales.
- Este tema, junto al 31 (cloud) y al 24 (desarrollo móvil), es sensible a la **obsolescencia tecnológica** en su primera mitad (§1); la segunda (§2 y §3) es mucho más estable. Conviene revisar §1.3 antes de cada convocatoria.
