# Tema 29 — Casos Prácticos

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
>
> **Formato**: 3 casos prácticos sobre supuestos reales del Ayuntamiento de Madrid. Cada caso suma **10 puntos**.
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

Los tres casos recorren el supuesto de referencia del tema (ver tema-29-contenido.md, «Convenciones»): el **CAU municipal atendiendo al puesto de trabajo de una Oficina de Atención a la Ciudadanía**. El **Caso 1** trabaja el **diagnóstico y la asistencia remota**; el **Caso 2**, la **priorización, el escalado y el acuerdo de nivel de servicio** ante una incidencia grave; y el **Caso 3**, la **seguridad, el cumplimiento normativo y la mejora continua**.

---

## Caso 1 — Diagnóstico y asistencia remota en el puesto de una Oficina de Atención a la Ciudadanía

### Enunciado

Son las 9:40 de la mañana. Una **tramitadora de una Oficina de Atención a la Ciudadanía de un distrito** llama al CAU: **no consigue firmar electrónicamente** un expediente con su certificado, alojado en una **tarjeta criptográfica**, y tiene a un vecino esperando en el mostrador. El resto de sus aplicaciones funcionan con normalidad. Su puesto es un **equipo tradicional** conectado a la red corporativa municipal, con agente de gestión instalado. En la misma oficina hay otras cinco personas que, de momento, no han informado de nada.

### Cuestiones

**Cuestión 1 — Registro y acotación (2 puntos).** Indique los **datos mínimos** que debe recoger el técnico antes de tocar el equipo y **dos preguntas** de acotación que reorienten el diagnóstico.

**Cuestión 2 — Hipótesis por capas (3 puntos).** Enumere **cinco hipótesis** de causa, cada una en una capa distinta del puesto, y señale cuál de ellas **no** podría resolverse en remoto.

**Cuestión 3 — Modo de asistencia (3 puntos).** Justifique **qué tipo de sesión** de control remoto debe abrirse y por qué **no sirve** una conexión de escritorio remoto estándar. Enumere los **controles** que deben aplicarse durante esa sesión.

**Cuestión 4 — Cierre de la actuación (2 puntos).** Suponiendo que el fallo se debía a una versión desactualizada del componente criptográfico, describa cómo debe **cerrarse** la incidencia y qué debe **quedar** de ella más allá del tique cerrado.

### Solución orientativa

- **C1**: (§2.2.2) Datos mínimos: **identificación de la usuaria** (número de empleada, unidad, ubicación exacta y teléfono de contacto), **fecha, hora y canal** de entrada, **descripción del síntoma en sus palabras** («no me deja firmar, sale un error al pulsar Firmar»), **identificación del equipo** en el inventario y **servicio afectado** (firma electrónica en la tramitación de expedientes). Dos preguntas de acotación válidas: *¿desde cuándo ocurre y qué ha cambiado —una actualización, un traslado, un cambio de contraseña—?* y *¿le ocurre solo a usted o también a sus compañeros de la oficina?* La segunda es la más rentable: si afecta a toda la oficina, la hipótesis se desplaza a una capa compartida y el impacto sube.

- **C2**: (§1.1.2) Cinco hipótesis, una por capa:

| Capa | Hipótesis | ¿Remoto? |
|---|---|---|
| Hardware / periférico | El lector de tarjetas está desconectado o no es reconocido | **No**: puede exigir presencia o la colaboración de la usuaria |
| Aplicaciones | El componente criptográfico (*middleware*) está desactualizado o desinstalado | Sí |
| Identidad | El certificado ha caducado o ha sido revocado | Sí |
| Configuración y seguridad | Una directiva o el antivirus bloquean el complemento de firma del navegador | Sí |
| Conectividad | No se alcanza el servicio de validación de certificados de la sede | Sí |

  La hipótesis de la primera fila es la única que puede no admitir resolución remota, y por eso conviene descartarla pronto —basta con pedir a la usuaria que confirme que el lector está conectado y con comprobar en remoto si el sistema lo reconoce—.

- **C3**: (§1.2, §1.3.3) Debe abrirse una sesión de **asistencia atendida en modo control compartido sobre la sesión existente** de la usuaria. Una conexión de **escritorio remoto estándar por RDP no sirve** por dos razones acumuladas: abriría una **sesión nueva e independiente**, de modo que el técnico no vería el escritorio que la usuaria tiene delante ni reproduciría el fallo; y, además, **la tarjeta criptográfica y su lector están asociados a la sesión de la usuaria**, por lo que en una sesión nueva ni siquiera estarían disponibles. Controles aplicables durante la sesión: **identificación nominal** del técnico con segundo factor; **código de sesión de un solo uso** facilitado por la usuaria como materialización del **consentimiento**; **indicador visible permanente** de que la sesión está activa; posibilidad de **corte unilateral** por la usuaria; petición expresa de que **cierre los documentos con datos de terceros** que no sean necesarios (**minimización**); **canal cifrado**; **bloqueo del puesto** al desconectar; y **registro** de la sesión asociado al número de tique.

- **C4**: (§2.3.3, §3.3.2) La incidencia se cierra **verificando técnicamente** que la firma funciona y, sobre todo, **pidiendo a la usuaria que firme el expediente pendiente** y confirme que puede trabajar: la verificación técnica y la del usuario no son la misma cosa. Se documenta en el tique **qué se hizo exactamente** y se le asigna una **categorización de cierre** (que en este caso probablemente diferirá de la de apertura). Más allá del tique cerrado deben quedar: **(1)** un **artículo de base de conocimiento** redactado **desde el síntoma** («no puedo firmar con la tarjeta»); **(2)** un **artículo de autoservicio** en el portal para que el siguiente usuario compruebe él mismo la versión antes de llamar; **(3)** la **consulta al inventario** de cuántos puestos más tienen la versión afectada, que es lo que permite decidir si estamos ante un caso aislado o ante un **problema**; y **(4)**, si hay más puestos afectados, la **apertura del problema** correspondiente.

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Datos mínimos de registro completos y dos preguntas de acotación pertinentes | 2 |
| Cinco hipótesis en capas distintas e identificación correcta de la no resoluble en remoto | 3 |
| Tipo de sesión correctamente justificado, descarte razonado de RDP y controles de la sesión | 3 |
| Cierre con confirmación de la usuaria y salidas duraderas de la resolución | 2 |

---

## Caso 2 — Priorización, escalado y acuerdo de nivel de servicio ante una caída del servicio de firma

### Enunciado

A las 10:15 el CAU ha recibido **catorce llamadas** de Oficinas de Atención a la Ciudadanía de **seis distritos distintos** con el mismo síntoma: **no se puede firmar electrónicamente** en la tramitación de expedientes. Hay ciudadanos esperando en los mostradores. Las aplicaciones internas de gestión funcionan con normalidad y el problema no se reproduce en los puestos del propio CAU.

El acuerdo de nivel de servicio vigente establece, para las incidencias **críticas**, un tiempo de respuesta de **15 minutos**, un tiempo de resolución de **4 horas** y escalado automático a nivel 2 a los **30 minutos** y jerárquico a la **hora**.

### Cuestiones

**Cuestión 1 — Registro y agrupación (2 puntos).** Indique cómo deben tratarse las catorce llamadas y qué efecto tiene esa decisión sobre la prioridad.

**Cuestión 2 — Prioridad (2 puntos).** Valore el **impacto** y la **urgencia** y determine la **prioridad** justificando cada eje por separado.

**Cuestión 3 — Escalados (3 puntos).** Indique **qué escalados** procede activar, de qué tipo es cada uno, a quién se dirige y **qué información** debe acompañarlos.

**Cuestión 4 — Comunicación y cierre del ciclo (3 puntos).** Describa las obligaciones de **comunicación** durante la incidencia y qué debe ocurrir **después** de restablecer el servicio.

### Solución orientativa

- **C1**: (§2.3.1) Las catorce llamadas **no** son catorce incidencias independientes ni deben descartarse como duplicados sin registro. Cada contacto se **registra** —hay catorce usuarios que esperan respuesta— pero todos se **vinculan a una única incidencia** que representa el fallo del servicio, con los catorce como afectados. La agrupación tiene dos efectos: **eleva el impacto** de «un usuario» a «varias unidades de atención al ciudadano de seis distritos», y permite **comunicar de una sola vez** a todos los afectados cuando se restablezca el servicio.

- **C2**: (§2.3.1) **Impacto ALTO**: está afectado un servicio esencial —la firma electrónica en la tramitación—, en múltiples unidades y distritos, con **interrupción de la atención al ciudadano** y con posible afectación a plazos administrativos. **Urgencia ALTA**: el daño se está produciendo ahora mismo, hay vecinos esperando en el mostrador y **no consta un rodeo** disponible. Cruzando ambos ejes en la matriz, **prioridad 1 — crítica**. Además, por número de afectados, criticidad del servicio e impacto en la atención al ciudadano, se cumplen los criterios para activar el **procedimiento de incidencia grave**, que no es lo mismo que la prioridad 1: es un flujo con procedimiento propio.

- **C3**: (§2.3.2) Procede activar **los dos escalados, y simultáneamente**:

  - **Escalado funcional (horizontal)** al equipo de **administración electrónica o de la plataforma de firma**: el fallo no está en el puesto —no se reproduce en los puestos del CAU, afecta a seis distritos a la vez y solo a un servicio— sino en un componente central o en un despliegue reciente sobre el parque. El primer nivel no tiene ni el conocimiento ni los permisos necesarios. Motivo: *no sé o no puedo resolverlo*.
  - **Escalado jerárquico (vertical)** al **responsable del CAU** y, a través de él, a la dirección: hay que **activar el procedimiento de incidencia grave**, designar un responsable de la incidencia, decidir sobre una eventual comunicación institucional y, en su caso, autorizar una parada o una reversión de emergencia. Motivo: *hace falta quien decida y quien aporte recursos*. Nótese que este escalado **no aporta conocimiento técnico**.

  Información que debe acompañar a ambos: **síntoma exacto**, **alcance confirmado** (catorce avisos, seis distritos, un solo servicio afectado), **hora de inicio**, **comprobaciones ya realizadas y descartadas** (no se reproduce en el CAU, el resto de aplicaciones funciona), **cambios recientes** consultados en el registro de cambios, y **qué se pide** exactamente a cada destinatario. La **propiedad del tique sigue siendo del CAU**, que continúa siendo responsable del seguimiento y de informar a los usuarios.

- **C4**: (§2.1.2, §2.3.3, §2.4.2) **Durante** la incidencia: comunicación **proactiva y periódica** a las oficinas afectadas —que necesitan poder decir algo al ciudadano que espera—, con una previsión realista y actualizaciones a intervalos fijos aunque no haya novedades; información a la dirección por el canal jerárquico; y aviso al resto del CAU para que las llamadas nuevas se vinculen a la incidencia existente en lugar de abrir tiques sueltos. **Después** del restablecimiento: **confirmar con una muestra de usuarios** que efectivamente pueden firmar antes de dar por resuelta la incidencia; **comunicar el cierre** a todos los afectados; realizar la **revisión posterior** propia del procedimiento de incidencia grave; **abrir el problema** correspondiente si el servicio se restableció con un rodeo o si la causa raíz no está determinada; **documentar el error conocido** y su rodeo en la KEDB mientras la solución definitiva se despliega; y tramitar esa solución definitiva a través de la **gestión de cambios**, con evaluación de riesgo, ventana y plan de reversión. Finalmente, revisar si el **SLA se cumplió** y, si no, analizar por qué: puede ser un problema de tiempos de escalado, de disponibilidad de la guardia o de un contrato de soporte que no sostiene el compromiso.

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Registro de los catorce contactos con vinculación a una única incidencia y efecto sobre el impacto | 2 |
| Impacto y urgencia justificados por separado, prioridad correcta y mención del flujo de incidencia grave | 2 |
| Los dos escalados identificados, correctamente tipificados y con la información que deben llevar | 3 |
| Comunicación durante la incidencia y cierre del ciclo con problema, error conocido y cambio | 3 |

---

## Caso 3 — Seguridad, cumplimiento normativo y mejora continua del servicio de asistencia

### Enunciado

El Ayuntamiento va a **licitar** el servicio de soporte al puesto de trabajo, que incluye asistencia remota **atendida y desatendida** sobre todo el parque municipal. La herramienta propuesta por uno de los licitadores es un **servicio en la nube** con servidor de mediación del propio fabricante y **grabación en vídeo** de todas las sesiones. El sistema al que dan soporte los puestos trata **expedientes con datos personales de ciudadanos**.

Durante una prueba piloto se detecta, además, que **varios técnicos comparten una misma cuenta** para conectarse a los puestos y que **el 18 % de las sesiones registradas no tiene un tique asociado**.

### Cuestiones

**Cuestión 1 — Hallazgos del piloto (3 puntos).** Analice los dos hallazgos detectados, indicando qué principio o requisito incumple cada uno y cómo se corrige.

**Cuestión 2 — Requisitos del ENS (3 puntos).** Indique la **categoría** previsible del sistema y **cuatro requisitos** derivados del Esquema Nacional de Seguridad que deben exigirse en el pliego.

**Cuestión 3 — Protección de datos (2 puntos).** Analice la propuesta del licitador desde la perspectiva del RGPD, con especial atención al servidor de mediación en la nube y a la grabación de sesiones.

**Cuestión 4 — Indicadores (2 puntos).** Proponga **cuatro indicadores** para el seguimiento del contrato y explique por qué deben equilibrarse entre sí.

### Solución orientativa

- **C1**: (§3.1.1, §3.1.2)

  - **Cuentas compartidas**: incumplen la exigencia de **identificación nominal** y, con ella, la dimensión de **trazabilidad** del ENS: las actuaciones dejan de ser atribuibles a una persona determinada, de modo que ni puede auditarse ni puede exigirse responsabilidad. Corrección: **cuentas nominales** para cada técnico, provenientes del directorio corporativo, con **autenticación multifactor** para el perfil con capacidad de control remoto, separación entre la cuenta ofimática y la de administración, y **perfiles por rol (RBAC)** con alcance limitado al conjunto de equipos que a cada uno le corresponde.
  - **Sesiones sin tique asociado**: revelan **accesos sin justificación registrada**, es decir, sin causa documentada que legitime el tratamiento. Es el hallazgo de auditoría más significativo en este ámbito, y afecta a la vez al ENS (trazabilidad) y al RGPD (**limitación de la finalidad**). Corrección: configurar la herramienta para que **exija un tique válido** como condición para iniciar la sesión, y establecer una **revisión periódica** de las sesiones sin tique, de los accesos desatendidos y de los accesos fuera de horario, con alertas ante patrones anómalos.

- **C2**: (§3.2.1) Al tratar **expedientes con datos personales de ciudadanos**, el sistema alcanzará al menos **nivel medio** en confidencialidad, integridad y trazabilidad, lo que sitúa la **categoría en MEDIA o superior** —la categoría la fija el nivel más alto de cualquier dimensión—. Cuatro requisitos exigibles en el pliego (bastan cuatro; se enumeran seis posibles):

  1. **Conformidad con el ENS del propio proveedor**, acreditada mediante certificación, dado que las obligaciones se trasladan **contractualmente** a la cadena de suministro.
  2. **Control de acceso** conforme al marco operacional: identificación nominal, requisitos de acceso, **segregación de funciones**, gestión reglada de derechos y mecanismos de autenticación reforzados.
  3. **Registro de la actividad** de todas las sesiones, con **protección de los registros** frente a manipulación —incluida la del administrador—, centralización en un sistema independiente, sincronización horaria común y plazo de conservación definido.
  4. **Protección de las comunicaciones**: cifrado del canal, autenticidad e integridad, y **separación de la red de gestión** respecto de la red de usuarios.
  5. **Gestión de incidentes de seguridad** con procedimiento documentado y criterios de **notificación al CCN-CERT**.
  6. **Auditoría bienal** del sistema y compromiso del proveedor de someterse a ella y de subsanar los hallazgos.

- **C3**: (§3.2.2) El proveedor actúa como **encargado del tratamiento** (art. 28 RGPD), por lo que debe suscribirse un **contrato de encargo** que fije objeto, duración, finalidad, tipo de datos, obligaciones de seguridad, régimen de **subcontratación** y devolución o supresión al terminar. Respecto del **servidor de mediación en la nube**: todo el tráfico de las sesiones —es decir, las pantallas de los puestos municipales— pasaría por infraestructura del fabricante, lo que obliga a analizar **dónde se tratan y almacenan los datos** y, si están fuera del Espacio Económico Europeo, la **base de la transferencia internacional**; la alternativa preferible y habitual en el sector público es exigir el **despliegue del servidor de mediación en las instalaciones del Ayuntamiento** o su alojamiento en la Unión Europea. Respecto de la **grabación de todas las sesiones**: es desproporcionada como configuración por defecto, porque captura la pantalla del empleado con su correo, sus documentos y datos personales de terceros. Su implantación exige **base jurídica**, **información previa** al personal y a la representación de los trabajadores (arts. 87-91 LOPDGDD, derecho a la intimidad frente al uso de dispositivos digitales), **finalidad limitada** a la auditoría de seguridad y no al control laboral encubierto, **plazo de conservación** definido, cifrado y acceso restringido a los auditores. Lo proporcionado es **grabar solo los accesos de mayor privilegio y los desatendidos**, y aplicar la **protección de datos desde el diseño y por defecto** (art. 25 RGPD): consentimiento obligatorio en la asistencia atendida, indicador visible y transferencia de ficheros deshabilitada de fábrica.

- **C4**: (§3.3.1) Cuatro indicadores adecuados: **(1) FCR**, resolución en primer contacto, que mide la eficacia y el coste del modelo; **(2) cumplimiento del SLA**, informado **por separado para respuesta y para resolución** y **segmentado por prioridad**, porque la media global oculta el comportamiento en lo crítico; **(3) tasa de reapertura**, que detecta cierres prematuros; y **(4) CSAT** o satisfacción declarada tras la resolución. Deben **equilibrarse entre sí** porque cualquier indicador aislado puede maximizarse a costa del servicio: medir solo el volumen resuelto por técnico premia cerrar rápido y mal, y por eso la productividad se contrasta con la reapertura y con la satisfacción; medir solo el cumplimiento del SLA incentiva abusar del estado «en espera del usuario» para detener el reloj. Como indicador adicional de madurez conviene incluir la **proporción de trabajo proactivo** —procedente de eventos de advertencia— frente al reactivo, y la **tasa de desvío al autoservicio**, que mide si la gestión del conocimiento está funcionando.

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Los dos hallazgos analizados con el requisito incumplido y su corrección concreta | 3 |
| Categoría previsible justificada y cuatro requisitos del ENS correctamente exigidos | 3 |
| Encargo de tratamiento, ubicación del servidor de mediación y proporcionalidad de la grabación | 2 |
| Cuatro indicadores pertinentes y explicación razonada de su equilibrio | 2 |
