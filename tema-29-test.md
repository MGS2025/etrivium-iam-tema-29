# Tema 29 — Test de Autoevaluación

> **Título**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
> **Formato**: 60 preguntas tipo test A/B/C (formato oficial oposición)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid
> **Versión**: v1.0 — Pendiente validación
> **Fecha**: 2026-08-20
> **Fuentes**: ver tema-29-fuentes.md

---

## Instrucciones

- Cada pregunta tiene **3 opciones** (A, B, C). Solo una es correcta.
- Penalización en examen real: respuesta incorrecta descuenta **1/3** del valor de una correcta.
- Tiempo orientativo: 1 minuto por pregunta.
- Distribución: El puesto y los fundamentos del control remoto (P1-P10), Protocolos, cifrado, herramientas y gestión centralizada (P11-P22), Marcos de referencia y el CAU (P23-P32), Priorización, escalado, cierre y SLA (P33-P44), Peticiones, eventos y problemas (P45-P50), Seguridad, ENS, protección de datos, KPI y conocimiento (P51-P60).

---

### Pregunta 1

**¿Cuál es la diferencia esencial entre VDI y RDSH?**

A) En VDI cada usuario dispone de una máquina virtual completa con su propio sistema operativo, mientras que en RDSH varias sesiones comparten un mismo sistema operativo de servidor
B) En VDI las aplicaciones se ejecutan en el equipo del usuario y en RDSH en el centro de datos
C) VDI exige cliente ligero y RDSH exige obligatoriamente un cliente pesado

<details><summary>Respuesta</summary>

**Correcta: A) En VDI cada usuario dispone de una máquina virtual completa con su propio sistema operativo, mientras que en RDSH varias sesiones comparten un mismo sistema operativo de servidor** De ahí que RDSH sea más eficiente en recursos por usuario pero ofrezca menor aislamiento: un usuario que consume memoria en exceso degrada a los demás.

*Referencia: §1.1.1 [MS-RDS]*
</details>

---

### Pregunta 2

**En un entorno de escritorio virtualizado, ¿qué viaja fundamentalmente por la red entre el centro de datos y el puesto del usuario?**

A) El código fuente de las aplicaciones que se van a ejecutar en local
B) La imagen de pantalla, las pulsaciones de teclado, el ratón, el audio y los periféricos redirigidos
C) Únicamente los ficheros de datos que el usuario abre y guarda

<details><summary>Respuesta</summary>

**Correcta: B) La imagen de pantalla, las pulsaciones de teclado, el ratón, el audio y los periféricos redirigidos** La aplicación se ejecuta en el servidor; el puesto solo transmite entradas y recibe la representación de la pantalla. Por eso sin red no hay puesto.

*Referencia: §1.1.1 [VDI-VENDORS]*
</details>

---

### Pregunta 3

**Un equipo cuyo agente de gestión ha dejado de comunicar con la plataforma centralizada, pero que el usuario sigue utilizando con normalidad, ¿en qué situación se encuentra?**

A) En una situación irrelevante mientras el usuario pueda trabajar
B) En una situación óptima, porque consume menos recursos al no ejecutar el agente
C) Fuera de control de la organización: no se parchea, no se inventaría y no admite asistencia desatendida

<details><summary>Respuesta</summary>

**Correcta: C) Fuera de control de la organización: no se parchea, no se inventaría y no admite asistencia desatendida** La pérdida de comunicación del agente es en sí misma una incidencia de soporte, aunque el usuario no perciba ningún síntoma.

*Referencia: §1.1.2 [MS-INTUNE]*
</details>

---

### Pregunta 4

**Tres usuarios de la misma planta informan a la misma hora de que la red va lenta, mientras que en otra sede no hay problemas. ¿Cuál es el orden de diagnóstico correcto?**

A) Revisar uno a uno los tres puestos, porque el fallo es siempre local
B) Confirmar el alcance real, comprobar el estado de los equipos de red de la sede, buscar una incidencia mayor ya abierta y solo entonces bajar al puesto individual
C) Escalar de inmediato al fabricante del equipamiento de red sin comprobar nada

<details><summary>Respuesta</summary>

**Correcta: B) Confirmar el alcance real, comprobar el estado de los equipos de red de la sede, buscar una incidencia mayor ya abierta y solo entonces bajar al puesto individual** La coincidencia de varios usuarios en el mismo emplazamiento y a la misma hora desplaza la hipótesis hacia una capa compartida. Además, los tres avisos deben agruparse bajo una única incidencia.

*Referencia: §1.1.2 [ITIL4]*
</details>

---

### Pregunta 5

**¿Cuál de estas afirmaciones distingue correctamente control remoto, acceso remoto y gestión remota?**

A) El control remoto sirve al soporte para ver y manejar el escritorio ajeno; el acceso remoto sirve al usuario para trabajar desde fuera; la gestión remota sirve al administrador para ejecutar tareas a escala
B) Son tres nombres del mismo concepto y se usan indistintamente en la práctica profesional
C) El acceso remoto se usa siempre para el soporte y el control remoto solo para el teletrabajo

<details><summary>Respuesta</summary>

**Correcta: A) El control remoto sirve al soporte para ver y manejar el escritorio ajeno; el acceso remoto sirve al usuario para trabajar desde fuera; la gestión remota sirve al administrador para ejecutar tareas a escala** Pueden compartir protocolos, pero responden a finalidades distintas y exigen autorizaciones distintas.

*Referencia: §1.2 [ITIL4]*
</details>

---

### Pregunta 6

**¿Qué caracteriza a la asistencia remota desatendida frente a la atendida?**

A) Que es más rápida porque no cifra el canal de comunicación
B) Que solo puede realizarse dentro de la red corporativa
C) Que permite conectarse sin que haya nadie delante del equipo, por lo que exige autorización previa, mínimo privilegio, registro completo y auditoría reforzada

<details><summary>Respuesta</summary>

**Correcta: C) Que permite conectarse sin que haya nadie delante del equipo, por lo que exige autorización previa, mínimo privilegio, registro completo y auditoría reforzada** La ausencia de consentimiento en cada sesión debe compensarse con controles más estrictos, y en todo caso la sesión debe quedar registrada y ser atribuible a una persona identificada.

*Referencia: §1.2 [ENS]*
</details>

---

### Pregunta 7

**En una conexión de control remoto, ¿quién actúa como servidor?**

A) Siempre el equipo del técnico, porque es quien inicia la conexión
B) El servidor de mediación, en todos los modelos de arquitectura
C) El equipo que es controlado, es decir, el del usuario, que sirve su pantalla al visor del técnico

<details><summary>Respuesta</summary>

**Correcta: C) El equipo que es controlado, es decir, el del usuario, que sirve su pantalla al visor del técnico** Es una inversión terminológica que se pregunta con frecuencia; en X Window ocurre algo análogo, con el servidor X ejecutándose donde está la pantalla del usuario.

*Referencia: §1.2.1 [RFC6143]*
</details>

---

### Pregunta 8

**¿Por qué las herramientas modernas de asistencia usan un servidor de mediación al que ambos extremos se conectan?**

A) Porque ambos extremos abren una conexión saliente, normalmente por HTTPS, lo que atraviesa NAT y cortafuegos sin necesidad de abrir puertos entrantes
B) Porque el cifrado solo es posible cuando existe un tercero que conserva las claves
C) Porque el protocolo RFB obliga a usar un intermediario según el RFC 6143

<details><summary>Respuesta</summary>

**Correcta: A) Porque ambos extremos abren una conexión saliente, normalmente por HTTPS, lo que atraviesa NAT y cortafuegos sin necesidad de abrir puertos entrantes** Además, centraliza la autenticación, la autorización y el registro. Su contrapartida es la dependencia de esa infraestructura de mediación.

*Referencia: §1.2.1 [MS-RDS]*
</details>

---

### Pregunta 9

**Una empleada en teletrabajo informa de que no le levanta la VPN y el CAU necesita ver su equipo. ¿Qué arquitectura de conexión es viable?**

A) La conexión directa cliente-servidor, publicando el puerto 3389 en su rúter doméstico
B) La conexión mediada, porque el agente del portátil abre una conexión saliente hacia el servidor de mediación sin depender de la VPN averiada
C) Ninguna: la incidencia exige necesariamente desplazamiento al domicilio

<details><summary>Respuesta</summary>

**Correcta: B) La conexión mediada, porque el agente del portátil abre una conexión saliente hacia el servidor de mediación sin depender de la VPN averiada** La regla general es que la herramienta de soporte no debe depender del servicio que puede estar averiado.

*Referencia: §1.2.1 [MS-QUICKASSIST]*
</details>

---

### Pregunta 10

**En el modelo AAA aplicado a una sesión de asistencia remota, ¿qué debe autenticarse?**

A) Tanto el técnico, con identidad nominal del directorio corporativo, como el equipo remoto, mediante certificado o huella de clave del servidor
B) Únicamente el técnico, ya que el equipo remoto pertenece a la organización
C) Únicamente el equipo remoto, ya que el técnico está en la red interna de administración

<details><summary>Respuesta</summary>

**Correcta: A) Tanto el técnico, con identidad nominal del directorio corporativo, como el equipo remoto, mediante certificado o huella de clave del servidor** Si el visor acepta cualquier certificado o clave de servidor sin verificación, un atacante puede interponerse y capturar la sesión completa.

*Referencia: §1.2.2 [RFC4253]*
</details>

---

### Pregunta 11

**¿Qué transmite el protocolo RFB, base de VNC, según el RFC 6143?**

A) Órdenes de dibujo de alto nivel y canales virtuales para redirigir impresoras y discos
B) Únicamente texto cifrado y flujos de terminal
C) El contenido del framebuffer, es decir, los píxeles de la pantalla, junto con los eventos de teclado y ratón en sentido inverso

<details><summary>Respuesta</summary>

**Correcta: C) El contenido del framebuffer, es decir, los píxeles de la pantalla, junto con los eventos de teclado y ratón en sentido inverso** De ahí su independencia del sistema operativo y su mayor consumo de ancho de banda frente a los protocolos de primitivas gráficas.

*Referencia: §1.3.1 [RFC6143]*
</details>

---

### Pregunta 12

**¿En qué puertos operan, respectivamente, RDP, VNC y SSH?**

A) 3306, 5432 y 22
B) 3389, 5900 y 22
C) 3389, 5900 y 23

<details><summary>Respuesta</summary>

**Correcta: B) 3389, 5900 y 22** RDP usa TCP y UDP 3389; VNC, TCP 5900 más el número de pantalla; SSH, TCP 22. El puerto 23 corresponde a Telnet, obsoleto por transmitir en claro.

*Referencia: §1.3.1 [MS-RDPBCGR]*
</details>

---

### Pregunta 13

**¿Cuál de estas afirmaciones sobre RDP es correcta?**

A) Transmite primitivas gráficas y multiplexa canales virtuales que permiten redirigir impresoras, discos, portapapeles y tarjetas inteligentes
B) Transmite píxeles en bruto y por eso comparte siempre la sesión de consola del usuario
C) Carece de cifrado propio, por lo que debe tunelizarse obligatoriamente sobre SSH

<details><summary>Respuesta</summary>

**Correcta: A) Transmite primitivas gráficas y multiplexa canales virtuales que permiten redirigir impresoras, discos, portapapeles y tarjetas inteligentes** Además, integra TLS y autenticación a nivel de red, y por defecto abre una sesión independiente en lugar de compartir la del usuario.

*Referencia: §1.3.1 [MS-RDPBCGR]*
</details>

---

### Pregunta 14

**Las tres capas en las que se estructura el protocolo SSH son:**

A) Física, de enlace y de red
B) Presentación, sesión y aplicación
C) Transporte, autenticación de usuario y conexión

<details><summary>Respuesta</summary>

**Correcta: C) Transporte, autenticación de usuario y conexión** La capa de transporte negocia claves y autentica al servidor; la de autenticación identifica al usuario; la de conexión multiplexa canales, incluido el reenvío de puertos.

*Referencia: §1.3.1 [RFC4251]*
</details>

---

### Pregunta 15

**¿Qué protocolo implementa Microsoft bajo el nombre de WinRM y en qué puertos opera?**

A) NETCONF, en el puerto 830
B) WS-Management de DMTF, en los puertos TCP 5985 para HTTP y 5986 para HTTPS
C) IPMI, en el puerto UDP 623

<details><summary>Respuesta</summary>

**Correcta: B) WS-Management de DMTF, en los puertos TCP 5985 para HTTP y 5986 para HTTPS** WinRM es la base de PowerShell Remoting y el equivalente funcional de SSH para la gestión sin interfaz gráfica en el mundo Windows.

*Referencia: §1.3.1 [MS-WINRM]*
</details>

---

### Pregunta 16

**Un equipo situado en una sede remota no arranca el sistema operativo. ¿Qué tecnología permite intervenir sin desplazamiento?**

A) La gestión fuera de banda mediante el controlador de gestión del equipo, con IPMI en el puerto UDP 623 o Redfish sobre HTTPS
B) Una sesión de RDP contra el puerto 3389 del equipo averiado
C) Una sesión de VNC sobre túnel SSH contra el puerto 5900

<details><summary>Respuesta</summary>

**Correcta: A) La gestión fuera de banda mediante el controlador de gestión del equipo, con IPMI en el puerto UDP 623 o Redfish sobre HTTPS** RDP, VNC y SSH son mecanismos dentro de banda: sus servidores son procesos del sistema operativo, de modo que si este no arranca no hay nada a lo que conectarse.

*Referencia: §1.3.1 [IPMI2]*
</details>

---

### Pregunta 17

**El paquete mágico de Wake-on-LAN se dirige convencionalmente a los puertos:**

A) TCP 22 y 23
B) UDP 7 y 9
C) UDP 161 y 162

<details><summary>Respuesta</summary>

**Correcta: B) UDP 7 y 9** Permite encender por red equipos apagados para parchearlos fuera del horario laboral. Los puertos UDP 161 y 162 corresponden a SNMP.

*Referencia: §1.3.1 [RFC862]*
</details>

---

### Pregunta 18

**Respecto de la seguridad de VNC clásico, ¿qué afirmación es correcta?**

A) Cifra todo el tráfico con TLS 1.3 desde la versión definida en el RFC 6143
B) No necesita protección adicional si se cambia el puerto por defecto
C) No cifra el tráfico y su autenticación es débil, por lo que debe tunelizarse sobre SSH o TLS y escuchar solo en la interfaz local

<details><summary>Respuesta</summary>

**Correcta: C) No cifra el tráfico y su autenticación es débil, por lo que debe tunelizarse sobre SSH o TLS y escuchar solo en la interfaz local** Un servidor VNC expuesto directamente a internet constituye un fallo grave de seguridad.

*Referencia: §1.3.2 [RFC6143]*
</details>

---

### Pregunta 19

**¿Qué aporta la confidencialidad hacia adelante (forward secrecy) en TLS a una sesión de asistencia?**

A) Que comprometer en el futuro la clave privada del servidor no permita descifrar sesiones pasadas que hubieran sido grabadas
B) Que la sesión pueda reanudarse automáticamente tras una caída de la red
C) Que el técnico no necesite autenticarse si el certificado del servidor es válido

<details><summary>Respuesta</summary>

**Correcta: A) Que comprometer en el futuro la clave privada del servidor no permita descifrar sesiones pasadas que hubieran sido grabadas** Es una propiedad del intercambio de claves, no del cifrado simétrico ni de la autenticación.

*Referencia: §1.3.2 [RFC8446]*
</details>

---

### Pregunta 20

**Un técnico necesita asistir a una usuaria y ver exactamente lo que ella ve en su pantalla. ¿Qué mecanismo NO le sirve?**

A) La herramienta de asistencia atendida con código de sesión y consentimiento
B) Una conexión de escritorio remoto estándar por RDP, que abre una sesión nueva e independiente
C) La observación de sesión (shadowing) en servicios de escritorio remoto

<details><summary>Respuesta</summary>

**Correcta: B) Una conexión de escritorio remoto estándar por RDP, que abre una sesión nueva e independiente** El técnico vería un escritorio distinto del que la usuaria tiene delante y no reproduciría su problema; además, ciertos periféricos como el lector de tarjeta criptográfica no estarían disponibles en esa sesión.

*Referencia: §1.3.3 [MS-RDS]*
</details>

---

### Pregunta 21

**En el reenvío de X11 sobre SSH, ¿dónde se ejecuta el servidor X?**

A) En el equipo remoto donde se ejecuta la aplicación gráfica
B) En el servidor de mediación que empareja ambos extremos
C) En la máquina del usuario, donde está la pantalla; la aplicación remota actúa como cliente

<details><summary>Respuesta</summary>

**Correcta: C) En la máquina del usuario, donde está la pantalla; la aplicación remota actúa como cliente** Es el modelo cliente-servidor invertido característico del sistema X Window, y una fuente habitual de confusión.

*Referencia: §1.3.3 [X11]*
</details>

---

### Pregunta 22

**¿Cuál es la principal aportación de una plataforma de gestión centralizada del puesto a la calidad del servicio?**

A) Que convierte el soporte reactivo en proactivo, reduciendo el número de incidencias y no solo el tiempo de resolución
B) Que sustituye por completo al Centro de Atención a Usuarios
C) Que elimina la necesidad de mantener un acuerdo de nivel de servicio

<details><summary>Respuesta</summary>

**Correcta: A) Que convierte el soporte reactivo en proactivo, reduciendo el número de incidencias y no solo el tiempo de resolución** Detectar el disco lleno, el parche que falta o el antivirus desactualizado antes de que provoquen la incidencia es más valioso que resolverla rápido.

*Referencia: §1.3.4 [MS-INTUNE]*
</details>

---

### Pregunta 23

**Según ITIL, ¿cuál es el objetivo de la gestión de incidencias?**

A) Identificar la causa raíz del fallo antes de actuar sobre el servicio
B) Restablecer el servicio normal lo antes posible, minimizando el impacto adverso en la actividad
C) Documentar el fallo para que no vuelva a producirse en el futuro

<details><summary>Respuesta</summary>

**Correcta: B) Restablecer el servicio normal lo antes posible, minimizando el impacto adverso en la actividad** Hallar la causa raíz corresponde a la gestión de problemas, que trabaja sin la urgencia del servicio caído.

*Referencia: §2.1.1 [ITIL4]*
</details>

---

### Pregunta 24

**Respecto de la certificación en gestión de servicios TI:**

A) ITIL certifica organizaciones y COBIT certifica personas
B) ISO/IEC 20000-1 certifica exclusivamente a personas mediante examen
C) ITIL certifica a personas, mientras que la certificación de una organización en gestión del servicio se obtiene con ISO/IEC 20000-1

<details><summary>Respuesta</summary>

**Correcta: C) ITIL certifica a personas, mientras que la certificación de una organización en gestión del servicio se obtiene con ISO/IEC 20000-1** ITIL propone buenas prácticas adaptables; ISO/IEC 20000-1 impone requisitos auditables de un sistema de gestión del servicio.

*Referencia: §2.1.1 [ISO20000]*
</details>

---

### Pregunta 25

**¿Qué cambio estructural introduce ITIL 4 respecto de ITIL v3?**

A) Suprime la figura del Centro de Atención a Usuarios y la sustituye por la automatización
B) Sustituye la estructura de procesos por fases del ciclo de vida por el Sistema de Valor del Servicio, y habla de prácticas en lugar de procesos
C) Elimina la distinción entre incidencia y problema por considerarla artificial

<details><summary>Respuesta</summary>

**Correcta: B) Sustituye la estructura de procesos por fases del ciclo de vida por el Sistema de Valor del Servicio, y habla de prácticas en lugar de procesos** En ITIL v3 el Service Desk era una función y la gestión de incidencias un proceso de la fase de operación; en ITIL 4 ambos son prácticas.

*Referencia: §2.1.1 [ITIL4]*
</details>

---

### Pregunta 26

**En un tique de incidencia, el estado «en espera del usuario» tiene la particularidad de que:**

A) Normalmente detiene el reloj del acuerdo de nivel de servicio, por lo que su uso debe estar reglado y auditado
B) Acelera el cómputo del tiempo de resolución para compensar la espera
C) Obliga automáticamente al cierre del tique transcurridas veinticuatro horas

<details><summary>Respuesta</summary>

**Correcta: A) Normalmente detiene el reloj del acuerdo de nivel de servicio, por lo que su uso debe estar reglado y auditado** Abusar de este estado para parar el reloj es una de las malas prácticas más habituales y falsea por completo los indicadores de cumplimiento.

*Referencia: §2.1.2 [ITIL4]*
</details>

---

### Pregunta 27

**El flujo de incidencia grave (major incident) se caracteriza por:**

A) Aplicarse automáticamente a todas las incidencias de prioridad 3 o superior
B) Prescindir del registro en la herramienta para ganar tiempo
C) Designar un responsable de la incidencia, establecer comunicación periódica a los afectados y a la dirección, y realizar una revisión posterior

<details><summary>Respuesta</summary>

**Correcta: C) Designar un responsable de la incidencia, establecer comunicación periódica a los afectados y a la dirección, y realizar una revisión posterior** Además, no espera al escalado normal: se escala de inmediato, tanto funcional como jerárquicamente.

*Referencia: §2.1.2 [ITIL4]*
</details>

---

### Pregunta 28

**El rasgo definitorio del Centro de Atención a Usuarios es:**

A) Resolver todas las incidencias sin escalar ninguna a otros grupos
B) Ser el punto único de contacto entre los usuarios y la organización de tecnología
C) Depender jerárquicamente del área de seguridad de la información

<details><summary>Respuesta</summary>

**Correcta: B) Ser el punto único de contacto entre los usuarios y la organización de tecnología** El usuario no tiene que saber a qué equipo técnico corresponde su problema: llama a un solo sitio y desde ahí se orquesta todo, conservando el CAU la propiedad del tique.

*Referencia: §2.2.1 [ITIL4]*
</details>

---

### Pregunta 29

**¿Cuál es el objetivo económico de la estructura por niveles de soporte?**

A) Resolver el mayor volumen posible en los niveles más bajos, que son los más baratos por contacto
B) Concentrar la resolución en el nivel 3, que es el más cualificado
C) Igualar el número de incidencias resueltas en cada nivel

<details><summary>Respuesta</summary>

**Correcta: A) Resolver el mayor volumen posible en los niveles más bajos, que son los más baratos por contacto** Cada escalado innecesario consume un recurso escaso, y por eso la tasa de resolución en primer contacto y la tasa de escalado son los dos indicadores que mejor miden la salud del modelo.

*Referencia: §2.2.1 [ITIL4]*
</details>

---

### Pregunta 30

**Un CAU multicanal debe garantizar que:**

A) Cada canal disponga de su propia herramienta y de su propio registro independiente
B) El teléfono sea el único canal admitido para incidencias críticas
C) Todos los canales desemboquen en un único registro y una única herramienta

<details><summary>Respuesta</summary>

**Correcta: C) Todos los canales desemboquen en un único registro y una única herramienta** La multicanalidad está en la entrada, nunca en el registro: registros separados por canal destruyen la trazabilidad, duplican incidencias e impiden medir.

*Referencia: §2.2.2 [ISO20000]*
</details>

---
### Pregunta 31

**La categorización de cierre de un tique difiere con frecuencia de la de apertura. Esto:**

A) Es siempre un error del técnico que debe corregirse retroactivamente
B) Es información valiosa: mide el acierto del primer nivel al clasificar y sirve para depurar la taxonomía y los guiones de diagnóstico
C) Impide utilizar los datos para el análisis de tendencias

<details><summary>Respuesta</summary>

**Correcta: B) Es información valiosa: mide el acierto del primer nivel al clasificar y sirve para depurar la taxonomía y los guiones de diagnóstico** La de apertura refleja lo que parecía; la de cierre, lo que era. Los análisis de tendencias deben apoyarse en la categorización de cierre.

*Referencia: §2.2.2 [ITIL4]*
</details>

---

### Pregunta 32

**Al diseñar la taxonomía de categorización de un CAU, la regla correcta es:**

A) Crear el máximo número posible de hojas para ganar precisión estadística
B) Permitir que cada técnico defina sus propias categorías según su experiencia
C) Definir pocas categorías, bien diferenciadas y mutuamente excluyentes

<details><summary>Respuesta</summary>

**Correcta: C) Definir pocas categorías, bien diferenciadas y mutuamente excluyentes** Una taxonomía con doscientas hojas se usa mal y produce datos inservibles; y si dos técnicos clasifican distinto el mismo caso, los indicadores mienten.

*Referencia: §2.2.2 [ITIL4]*
</details>

---

### Pregunta 33

**La prioridad de una incidencia se determina:**

A) Cruzando el impacto con la urgencia mediante una matriz y criterios objetivos escritos
B) Aplicando exclusivamente el número de usuarios afectados
C) Según la calificación que el propio usuario dé a su caso al llamar

<details><summary>Respuesta</summary>

**Correcta: A) Cruzando el impacto con la urgencia mediante una matriz y criterios objetivos escritos** La opinión del usuario es información a considerar, pero si la prioridad la fija quien más insiste, las incidencias verdaderamente críticas se retrasan.

*Referencia: §2.3.1 [ITIL4]*
</details>

---

### Pregunta 34

**Falla el proceso nocturno de copia de seguridad de un servidor de expedientes. Son las diez de la mañana y la próxima ventana de copia es a las once de la noche. ¿Cómo se valoran impacto y urgencia?**

A) Impacto bajo y urgencia baja, porque ningún usuario percibe el fallo
B) Impacto alto, porque afecta a la protección de todos los expedientes, y urgencia media, porque hay margen hasta la siguiente ventana
C) Impacto alto y urgencia alta, por tratarse de un servidor

<details><summary>Respuesta</summary>

**Correcta: B) Impacto alto, porque afecta a la protección de todos los expedientes, y urgencia media, porque hay margen hasta la siguiente ventana** Es el ejemplo canónico de que un impacto alto no implica automáticamente prioridad crítica. Si a las diez de la noche siguiera sin resolverse, la urgencia pasaría a alta y habría que reevaluar la prioridad.

*Referencia: §2.3.1 [ITIL4]*
</details>

---

### Pregunta 35

**Veinte usuarios llaman por separado informando del mismo fallo. La actuación correcta es:**

A) Cerrar diecinueve como duplicados sin registrarlos, para no inflar las estadísticas
B) Tratarlos como veinte incidencias independientes de impacto bajo
C) Vincularlos a una incidencia común cuyo impacto refleje a los veinte afectados, lo que eleva su prioridad

<details><summary>Respuesta</summary>

**Correcta: C) Vincularlos a una incidencia común cuyo impacto refleje a los veinte afectados, lo que eleva su prioridad** La agrupación eleva el impacto y permite comunicar de una sola vez a todos los afectados cuando se restablezca el servicio.

*Referencia: §2.3.1 [ITIL4]*
</details>

---

### Pregunta 36

**¿Qué es el escalado funcional?**

A) El traslado de la incidencia a un grupo con mayor conocimiento técnico o mayores permisos, del nivel 1 al 2, al 3 o al proveedor
B) El aviso a un nivel de autoridad superior para que decida o autorice
C) La reasignación del tique a otro técnico del mismo nivel por carga de trabajo

<details><summary>Respuesta</summary>

**Correcta: A) El traslado de la incidencia a un grupo con mayor conocimiento técnico o mayores permisos, del nivel 1 al 2, al 3 o al proveedor** Es horizontal y responde a «no sé o no puedo resolverlo»; no aporta autoridad, sino conocimiento.

*Referencia: §2.3.2 [ITIL4]*
</details>

---

### Pregunta 37

**El escalado jerárquico procede cuando:**

A) El técnico de primer nivel carece del conocimiento técnico necesario
B) Es preciso instalar un parche en un servidor gestionado por otro equipo
C) Se van a incumplir los plazos, hace falta autorizar una parada o un gasto, o el impacto exige comunicación a la dirección

<details><summary>Respuesta</summary>

**Correcta: C) Se van a incumplir los plazos, hace falta autorizar una parada o un gasto, o el impacto exige comunicación a la dirección** El escalado jerárquico no aporta conocimiento técnico: aporta decisión y recursos. Ambos escalados pueden coexistir en la misma incidencia.

*Referencia: §2.3.2 [ITIL4]*
</details>

---

### Pregunta 38

**Cuando una incidencia se escala a un nivel superior:**

A) La propiedad del tique se transfiere al grupo destinatario, que pasa a informar al usuario
B) El CAU conserva la propiedad del tique y sigue siendo responsable de su seguimiento y de informar al usuario
C) El tique se cierra y se abre uno nuevo a nombre del grupo resolutor

<details><summary>Respuesta</summary>

**Correcta: B) El CAU conserva la propiedad del tique y sigue siendo responsable de su seguimiento y de informar al usuario** Escalar no es quitárselo de encima; además, el escalado debe ir documentado con el síntoma, el alcance y las comprobaciones ya realizadas y descartadas.

*Referencia: §2.3.2 [ITIL4]*
</details>

---

### Pregunta 39

**¿Puede cerrarse una incidencia aplicando únicamente una solución temporal o rodeo?**

A) Sí, siempre que el servicio esté restablecido, el rodeo esté documentado y se haya abierto el problema correspondiente si la causa persiste
B) No: la gestión de incidencias solo puede cerrar tras eliminar la causa raíz
C) Sí, y sin necesidad de documentar nada, porque el usuario ya puede trabajar

<details><summary>Respuesta</summary>

**Correcta: A) Sí, siempre que el servicio esté restablecido, el rodeo esté documentado y se haya abierto el problema correspondiente si la causa persiste** Cerrar con rodeo sin abrir el problema es justamente la práctica que hace que la misma incidencia reaparezca indefinidamente.

*Referencia: §2.3.3 [ITIL4]*
</details>

---

### Pregunta 40

**Respecto del cierre de un tique, la regla general es:**

A) Cerrar en cuanto el técnico verifica que el servicio funciona, sin más trámite
B) No cerrar sin confirmación del usuario, salvo la regla de cierre automático tras un plazo pactado sin respuesta, dejando constancia de los intentos
C) Mantener el tique abierto indefinidamente hasta que el usuario solicite su cierre por escrito

<details><summary>Respuesta</summary>

**Correcta: B) No cerrar sin confirmación del usuario, salvo la regla de cierre automático tras un plazo pactado sin respuesta, dejando constancia de los intentos** La verificación técnica y la del usuario no son la misma cosa: es el usuario quien define si el servicio está restablecido.

*Referencia: §2.3.3 [ITIL4]*
</details>

---

### Pregunta 41

**Una tasa de reapertura alta es una señal de alarma porque indica que:**

A) Se está cerrando antes de tiempo, quizá para cumplir formalmente el acuerdo de nivel de servicio
B) El volumen de incidencias es superior al que el CAU puede absorber
C) La taxonomía de categorización tiene demasiadas hojas

<details><summary>Respuesta</summary>

**Correcta: A) Se está cerrando antes de tiempo, quizá para cumplir formalmente el acuerdo de nivel de servicio** Es un ejemplo del riesgo general de las métricas: medir mal induce a comportarse mal. Por eso la productividad se contrasta siempre con la reapertura y con la satisfacción.

*Referencia: §2.3.3 [ITIL4]*
</details>

---

### Pregunta 42

**¿Qué distingue a un OLA de un SLA y de un UC?**

A) El OLA se firma con el proveedor externo y el UC con el cliente
B) El OLA sustituye al SLA cuando el servicio está externalizado
C) El OLA es un acuerdo interno entre equipos de la propia organización; el SLA se pacta con el cliente y el UC es el contrato con un proveedor externo

<details><summary>Respuesta</summary>

**Correcta: C) El OLA es un acuerdo interno entre equipos de la propia organización; el SLA se pacta con el cliente y el UC es el contrato con un proveedor externo** Los OLA y los UC deben estar dimensionados de forma que permitan cumplir el SLA.

*Referencia: §2.3.4 [ITIL4]*
</details>

---

### Pregunta 43

**El SLA compromete resolver las incidencias críticas en cuatro horas, pero el contrato con el fabricante garantiza la sustitución de piezas al siguiente día laborable. ¿Qué falla y cómo se corrige?**

A) Nada falla: el plazo del fabricante no afecta al cómputo del SLA en ningún caso
B) El contrato de soporte no sostiene el SLA; se corrige elevando el UC o diseñando el servicio con redundancia para que el restablecimiento no dependa de la pieza
C) Falla el OLA interno, que debe reducirse a dos horas para compensar

<details><summary>Respuesta</summary>

**Correcta: B) El contrato de soporte no sostiene el SLA; se corrige elevando el UC o diseñando el servicio con redundancia para que el restablecimiento no dependa de la pieza** Lo que el SLA compromete es restablecer el servicio, no reparar el componente averiado: por eso la redundancia más un stock propio de repuestos suele ser más barata y fiable que un contrato de respuesta ultrarrápida.

*Referencia: §2.3.4 [ISO20000]*
</details>

---

### Pregunta 44

**La diferencia entre tiempo de respuesta y tiempo de resolución es que:**

A) El de respuesta mide hasta el primer contacto efectivo o la asignación, y el de resolución hasta el restablecimiento del servicio
B) El de respuesta mide el tiempo total del tique y el de resolución solo la parte trabajada
C) Son sinónimos y se informan de forma conjunta en un único indicador

<details><summary>Respuesta</summary>

**Correcta: A) El de respuesta mide hasta el primer contacto efectivo o la asignación, y el de resolución hasta el restablecimiento del servicio** Un CAU puede cumplir escrupulosamente el tiempo de respuesta e incumplir de forma sistemática el de resolución: por eso ambos se miden e informan por separado.

*Referencia: §2.3.4 [ITIL4]*
</details>

---

### Pregunta 45

**Un usuario solicita el alta de acceso a una carpeta compartida. Se trata de:**

A) Una incidencia de prioridad baja, por afectar a un solo usuario
B) Un problema, porque revela una carencia en la configuración de permisos
C) Una petición de servicio: nada está roto y es una solicitud prevista en el catálogo, que además exigirá autorización previa

<details><summary>Respuesta</summary>

**Correcta: C) Una petición de servicio: nada está roto y es una solicitud prevista en el catálogo, que además exigirá autorización previa** Las peticiones se miden por cumplimiento de plazo, no por rapidez de restablecimiento, y mezclarlas con las incidencias en un mismo indicador produce cifras sin sentido.

*Referencia: §2.4.1 [ITIL4]*
</details>

---

### Pregunta 46

**Los tres tipos de evento que distingue ITIL son:**

A) Crítico, mayor y menor
B) Informativo, advertencia y excepción
C) Preventivo, correctivo y evolutivo

<details><summary>Respuesta</summary>

**Correcta: B) Informativo, advertencia y excepción** El informativo registra algo previsto; la advertencia señala la proximidad de un umbral y permite actuar antes; la excepción indica que el umbral se ha superado y suele generar una incidencia automática.

*Referencia: §2.4.1 [ITIL4]*
</details>

---

### Pregunta 47

**¿Por qué el evento de advertencia es el de mayor valor económico?**

A) Porque permite evitar la incidencia en lugar de resolverla, habilitando el soporte proactivo
B) Porque siempre genera un tique de prioridad crítica que se atiende antes
C) Porque es el único tipo de evento que la monitorización puede correlacionar

<details><summary>Respuesta</summary>

**Correcta: A) Porque permite evitar la incidencia en lugar de resolverla, habilitando el soporte proactivo** Un servicio de soporte maduro se reconoce en que una parte creciente de su trabajo procede de eventos de advertencia y no de llamadas de usuarios.

*Referencia: §2.4.1 [NAGIOS]*
</details>

---

### Pregunta 48

**El riesgo característico de una monitorización mal ajustada es el exceso de alertas. ¿Qué técnica lo mitiga?**

A) Elevar todos los umbrales hasta que solo se notifiquen las caídas totales
B) Enviar todas las alertas al buzón del responsable del CAU para que las filtre
C) Correlacionar los eventos para emitir una única alerta con la causa, suprimirlas durante las ventanas de mantenimiento y ajustar los umbrales de forma continua

<details><summary>Respuesta</summary>

**Correcta: C) Correlacionar los eventos para emitir una única alerta con la causa, suprimirlas durante las ventanas de mantenimiento y ajustar los umbrales de forma continua** Un enlace caído genera cien alertas de los servicios que dependen de él; hay que emitir una sola con la causa, o el operador dejará de mirarlas.

*Referencia: §2.4.1 [NAGIOS]*
</details>

---

### Pregunta 49

**¿Qué es un error conocido?**

A) Una incidencia que se repite más de tres veces en el mismo mes
B) Un problema ya analizado, del que se conoce la causa y/o una solución temporal documentada
C) Un fallo del que se ha informado al fabricante y aún no ha respondido

<details><summary>Respuesta</summary>

**Correcta: B) Un problema ya analizado, del que se conoce la causa y/o una solución temporal documentada** Se registra en la base de datos de errores conocidos (KEDB), que la gestión de problemas escribe y la de incidencias consulta.

*Referencia: §2.4.1 [ITIL4]*
</details>

---

### Pregunta 50

**Ciento cuarenta incidencias idénticas resueltas una a una con el mismo rodeo indican que:**

A) La gestión de incidencias funciona pero el servicio falla: hay que abrir un problema, analizar la causa raíz y planificar la solución definitiva como un cambio
B) El acuerdo de nivel de servicio debe relajarse para absorber ese volumen
C) La categorización de apertura está mal diseñada y debe rehacerse la taxonomía

<details><summary>Respuesta</summary>

**Correcta: A) La gestión de incidencias funciona pero el servicio falla: hay que abrir un problema, analizar la causa raíz y planificar la solución definitiva como un cambio** El resultado se mide en la caída de una familia entera de incidencias, no en el tiempo de resolución de cada una.

*Referencia: §2.4.2 [ITIL4]*
</details>

---

### Pregunta 51

**El principio de mínimo privilegio aplicado a la asistencia remota tiene dos dimensiones:**

A) El número de técnicos autorizados y el número de equipos del parque
B) Qué permisos se conceden —los imprescindibles— y durante cuánto tiempo —solo el necesario—
C) El coste de la herramienta y la formación del personal que la utiliza

<details><summary>Respuesta</summary>

**Correcta: B) Qué permisos se conceden —los imprescindibles— y durante cuánto tiempo —solo el necesario—** Se completa con la segregación de funciones, que impide que una misma persona administre la herramienta de asistencia y audite sus registros.

*Referencia: §3.1.1 [ENS]*
</details>

---

### Pregunta 52

**En un servicio de soporte, el uso de cuentas genéricas compartidas por el equipo de técnicos:**

A) Está desaconsejado porque destruye la trazabilidad: las actuaciones dejan de ser atribuibles a una persona identificada
B) Es recomendable porque simplifica la gestión de altas y bajas de personal
C) Es indiferente siempre que la sesión vaya cifrada

<details><summary>Respuesta</summary>

**Correcta: A) Está desaconsejado porque destruye la trazabilidad: las actuaciones dejan de ser atribuibles a una persona identificada** La identidad debe ser nominal y provenir del directorio corporativo, con separación entre la cuenta ofimática del técnico y la cuenta con la que administra.

*Referencia: §3.1.1 [ENS]*
</details>

---

### Pregunta 53

**En una auditoría de las sesiones de asistencia remota, ¿cuál es el hallazgo más significativo?**

A) Que alguna sesión haya durado más de una hora
B) Que se hayan usado modos de solo visualización en lugar de control total
C) La sesión sin tique asociado, porque revela un acceso sin justificación registrada

<details><summary>Respuesta</summary>

**Correcta: C) La sesión sin tique asociado, porque revela un acceso sin justificación registrada** Toda sesión debe responder a una causa registrada; el tique es lo que convierte el acceso en legítimo y auditable.

*Referencia: §3.1.2 [ENS]*
</details>

---

### Pregunta 54

**Los registros de actividad de las sesiones de asistencia deben:**

A) Almacenarse en el propio equipo atendido, para facilitar su consulta local
B) Centralizarse en un sistema independiente del sistema auditado, con control de acceso propio y plazo de conservación definido
C) Borrarse al cerrar cada incidencia, para minimizar el tratamiento de datos

<details><summary>Respuesta</summary>

**Correcta: B) Centralizarse en un sistema independiente del sistema auditado, con control de acceso propio y plazo de conservación definido** Un registro que el propio administrador puede borrar no acredita nada. Además, sin sincronización horaria común los registros de distintos equipos no pueden correlacionarse.

*Referencia: §3.1.2 [ISO27001]*
</details>

---

### Pregunta 55

**Las cinco dimensiones de seguridad del Esquema Nacional de Seguridad son:**

A) Disponibilidad, autenticidad, integridad, confidencialidad y trazabilidad
B) Confidencialidad, integridad, disponibilidad, resiliencia y continuidad
C) Prevención, detección, respuesta, conservación y vigilancia

<details><summary>Respuesta</summary>

**Correcta: A) Disponibilidad, autenticidad, integridad, confidencialidad y trazabilidad** Cada una se valora en nivel bajo, medio o alto, y la categoría del sistema —básica, media o alta— la determina el nivel más alto alcanzado por cualquiera de ellas.

*Referencia: §3.2.1 [ENS]*
</details>

---

### Pregunta 56

**Respecto de la auditoría de seguridad exigida por el ENS:**

A) Todos los sistemas deben auditarse anualmente con independencia de su categoría
B) Solo se audita cuando se produce un incidente de seguridad notificable
C) Los sistemas de categoría media y alta se auditan al menos cada dos años, mientras que los de categoría básica admiten autoevaluación

<details><summary>Respuesta</summary>

**Correcta: C) Los sistemas de categoría media y alta se auditan al menos cada dos años, mientras que los de categoría básica admiten autoevaluación** Además, cualquier modificación sustancial del sistema obliga a repetir la auditoría, y la conformidad debe publicarse con su distintivo en la sede electrónica.

*Referencia: §3.2.1 [ENS]*
</details>

---

### Pregunta 57

**Si durante una asistencia remota se produce o se descubre una brecha de datos personales, el plazo de notificación a la autoridad de control es:**

A) De quince días naturales desde que se tuvo constancia
B) Sin dilación indebida y, de ser posible, en un plazo máximo de 72 horas desde que se tuvo constancia
C) De un mes, prorrogable por otro mes en casos complejos

<details><summary>Respuesta</summary>

**Correcta: B) Sin dilación indebida y, de ser posible, en un plazo máximo de 72 horas desde que se tuvo constancia** La comunicación a los propios interesados procede además cuando la brecha entrañe alto riesgo para sus derechos y libertades.

*Referencia: §3.2.2 [RGPD]*
</details>

---

### Pregunta 58

**Cuando el servicio de asistencia remota se presta mediante una herramienta en la nube de un tercero, ese proveedor:**

A) Queda al margen del RGPD por limitarse a transportar tráfico cifrado
B) Es responsable del tratamiento, y desplaza esa condición de la Administración
C) Es encargado del tratamiento y debe existir un contrato que fije objeto, finalidad, tipo de datos, obligaciones de seguridad y devolución o supresión al terminar

<details><summary>Respuesta</summary>

**Correcta: C) Es encargado del tratamiento y debe existir un contrato que fije objeto, finalidad, tipo de datos, obligaciones de seguridad y devolución o supresión al terminar** Además hay que analizar la ubicación del servidor de mediación y de las grabaciones por la eventual transferencia internacional de datos.

*Referencia: §3.2.2 [RGPD]*
</details>

---

### Pregunta 59

**Un CAU registra en un mes 6.000 incidencias, de las que el nivel 1 resuelve 4.200 en primer contacto. ¿Cuál es su FCR?**

A) 70 %
B) 30 %
C) 42 %

<details><summary>Respuesta</summary>

**Correcta: A) 70 %** La resolución en primer contacto es 4.200 dividido entre 6.000. El 30 % restante corresponde a la tasa de escalado, indicador complementario del anterior.

*Referencia: §3.3.1 [ITIL4]*
</details>

---

### Pregunta 60

**Un artículo de la base de conocimiento debe redactarse:**

A) Desde la causa técnica, para que sea preciso y verificable por el nivel 3
B) En inglés, para facilitar la búsqueda en la documentación del fabricante
C) Desde el síntoma, porque el técnico que lo busca sabe lo que ve, no lo que falla

<details><summary>Respuesta</summary>

**Correcta: C) Desde el síntoma, porque el técnico que lo busca sabe lo que ve, no lo que falla** Los artículos escritos desde la causa resultan invisibles en la búsqueda y no se usan, por muy correctos que sean. Además, deben tener responsable, fecha de caducidad y retirada activa cuando quedan obsoletos.

*Referencia: §3.3.2 [ITIL4]*
</details>
