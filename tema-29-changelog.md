# Tema 29 — Changelog

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.

---

## v1.0 — 2026-08-20 — Primera versión

**Estado**: pendiente de validación por María y Ana, y de revisión técnica del IAM (Jesús Cuadrado).

**Motivo**: desarrollo del Tema 29, dentro de la serie de temas técnicos generados desde cero, replicando la estructura y el formato de los Temas 1, 11 y 17-24 ya consolidados. Se genera **saltando los Temas 27 y 28**, cuyos esqueletos están disponibles pero aún no desarrollados (T25 y T26 sí lo están, publicados el 2026-08-19 y el 2026-08-20). El bloque técnico queda por tanto **completo de T11 a T26**, con **hueco en T27 y T28** y con T29 ya cerrado.

### Alcance de la v1.0

| Entregable | Cantidad |
|---|---|
| Contenido teórico | ~21.100 palabras · 3 secciones (fieles al esqueleto oficial) con 34 epígrafes numerados |
| Diagramas SVG inline | 16 (accesibles con `role`/`aria-label`, clases con sufijo único anti-colisión) |
| Banco de preguntas tipo test | 60 preguntas A/B/C con explicación y referencia, balanceadas **20/20/20** (verificado por el generador) |
| Casos prácticos | 3 (diagnóstico y asistencia remota en una Oficina de Atención a la Ciudadanía; priorización, escalado y SLA ante una caída del servicio de firma; seguridad, cumplimiento y mejora continua en la licitación del soporte) · 10 puntos cada uno |
| Fuentes Tier 1 | 29 referencias canónicas (IETF, DMTF, Intel/IPMI, ITIL 4, ISO/IEC 20000-1, ISO/IEC 27001, COBIT 2019, ENS, CCN-STIC, RGPD, LOPDGDD, ENI, Leyes 39 y 40/2015) |

### Decisiones de generación

1. **Sin material de cliente**: solo el esqueleto `Test_Prompting/temas agosto/29.md`. Desarrollado desde fuentes canónicas (RFC de IETF, especificaciones de DMTF, marcos ITIL 4 / ISO/IEC 20000-1 / COBIT 2019 y normativa española ENS y RGPD/LOPDGDD), todas referenciadas.
2. **Estructura fiel al esqueleto oficial**: sus 3 secciones de primer nivel, 10 subsecciones y 24 epígrafes, respetados uno a uno sin añadir secciones nuevas de primer nivel ni reordenar.
3. **Tema explícitamente presentado como "de dos mitades"** (técnica y organizativa) desde las Convenciones, porque el enunciado oficial une deliberadamente ambas y un opositor que domine solo una suspende la otra. La tercera sección se plantea como la costura normativa entre las dos.
4. **Sin snippets de código** (decisión de generación, a diferencia de T21, T23 y T24): este tema no compara lenguajes ni plataformas de desarrollo, sino protocolos, herramientas y procesos. Lo memorizable aquí son **puertos, números de RFC, definiciones y matrices**, no sintaxis. Se ha priorizado en su lugar la **densidad de tablas comparativas**.
5. **Caso de referencia único para todo el tema**: el **CAU municipal atendiendo el puesto de una tramitadora de una Oficina de Atención a la Ciudadanía** que no puede firmar electrónicamente un expediente, con un vecino esperando. Planteado como **supuesto simplificado**, no como descripción de una organización real concreta. Concentra casi todas las dificultades del tema: identificación, consentimiento, acceso a datos de terceros, priorización con atención al ciudadano afectada, escalado, SLA, trazabilidad ENS y aprovechamiento posterior del conocimiento.
6. **Distinciones nucleares tratadas como eje**, porque son lo que más rinde en examen y la fuente más frecuente de error: control remoto / acceso remoto / gestión remota; atendido / desatendido; dentro de banda / fuera de banda; VNC (píxeles, sesión compartida) frente a RDP (primitivas, sesión independiente); incidencia / problema / error conocido / petición / evento; escalado funcional / jerárquico; SLA / OLA / UC; impacto / urgencia; tiempo de respuesta / tiempo de resolución. Cada una tiene su callout de DATO CLAVE y, la mayoría, su diagrama dedicado.
7. **Puertos y RFC como material de memorización directa**, concentrados además en el diagrama **D5** para permitir el repaso rápido: 5900 (RFB), 3389 (RDP), 22 (SSH), 23 (Telnet, obsoleto), 5985/5986 (WinRM), 161/162 (SNMP), 830 (NETCONF), 623 (IPMI), 443 (Redfish), 6000+N (X11) y 7/9 (Wake-on-LAN).
8. **ENS citado por bloques y grupos de medidas** (org / op / mp, con `op.acc`, `op.exp`, `op.mon`, `mp.com`, `mp.eq`) en lugar de enumerar el Anexo II medida a medida: el detalle exhaustivo corresponde al **Tema 39**, y desarrollarlo aquí duplicaría contenido. Queda anotado en la validación por si el IAM prefiere ampliarlo.
9. **Frontera con temas vecinos** cuidada: la virtualización como tecnología al Tema 28; la administración del sistema operativo al Tema 27; arquitectura y periféricos a los Temas 11 y 12; los sistemas operativos al Tema 14; la administración de redes locales y la monitorización de tráfico al Tema 30; el cloud al Tema 31; la seguridad de sistemas y la criptografía al Tema 32; TCP/IP y HTTP/TLS a los Temas 34 y 35; el **acceso remoto seguro y las VPN al Tema 36** (frontera especialmente vigilada, por ser el tema más próximo); y el ENS y el ENI al Tema 39.
10. **Referencias cruzadas validadas contra BOAM 10.032**: T11, T12, T14, T27, T28, T30, T31, T32, T34, T35, T36 y T39. Todas comprobadas contra el enunciado oficial de cada tema.
11. **Anti-colisión de SVG**: las clases CSS de cada diagrama llevan **sufijo numérico único** (`.t1`…`.t16`, `.h1`…`.h16`), evitando el fallo sistémico de estilos que se filtran de un SVG a otro al estar todos embebidos en la misma página (lección de T5). Los marcadores de flecha (`marker`) llevan también identificador único por diagrama (`a3`, `a4`, `a9`…).
12. **Distribución A/B/C fijada ANTES de redactar** (lección de T23 y práctica ya consolidada en T24): se predefinió la secuencia completa de 60 letras con 20 de cada una y se redactó cada pregunta contra su letra asignada. `build_t29.py` confirma **20/20/20 a la primera**, sin necesidad de permutaciones correctoras.
13. **Cómputo de extensión medido, no estimado**: la cifra de ~21.100 palabras procede de `wc -w` sobre el `.md`. Medido con el mismo criterio, T24 —hasta ahora el más extenso de la serie técnica— arroja ≈12.300, de modo que **este tema pasa a ser, con diferencia, el más extenso de la serie**. La causa es estructural: el enunciado oficial une dos materias completas (una técnica y una de gestión de servicios) que en otros temarios se tratan por separado.
14. **Valores de SLA declarados como ilustrativos** en §2.3.4 y en D13, en lugar de presentarlos como datos del Ayuntamiento: no se dispone del contrato real de soporte al puesto. Queda anotado en la validación para sustituirlos si el IAM los facilita.

### Pendientes para QA / próxima iteración

- Validación de profundidad por María/Ana/IAM (¿alguna sección a ampliar o recortar? ¿el equilibrio entre la mitad técnica y la organizativa es el adecuado?).
- **Generar T27 y T28** para cerrar el hueco del bloque técnico y dejar T11-T29 sin huecos: sus esqueletos ya están en `Test_Prompting/temas agosto/`.
- Confirmar con el IAM si conviene sustituir los tiempos ilustrativos del SLA por los reales de su contrato de soporte.
- Confirmar si el detalle del Anexo II del ENS debe ampliarse aquí o queda mejor remitido al Tema 39.
- Verificación ortográfica con corrector es_ES (cuidado con falsos positivos por términos técnicos en inglés: *framebuffer*, *shadowing*, *broker*, *relay*, *workaround*, *backlog*, *service desk*, *major incident*, *follow the sun*, *jump host*…).

### Origen

Generado el 2026-08-20 en el flujo de trabajo de eTrivium, replicando el patrón de los Temas 1 (v2.1), 11 (v3.2) y 17-24 (v1.0). `build_t29.py` y `_build_css.txt` persistidos en el repo.
