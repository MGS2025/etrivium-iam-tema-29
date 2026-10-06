# Tema 29 — Catálogo de Diagramas

> **Título oficial**: Control remoto de puesto de usuario y gestión de la resolución de incidencias.
>
> **Versión**: v1.0
> **Fecha**: 2026-08-20
> **Autor**: ETRIVIUM
> **Formato**: SVG inline (zero-dependencias, escalable, imprimible, accesible con role/aria-label)
> **Paleta**: Ayuntamiento de Madrid #0055a0 (primario) + #d13c3c (alertas) + #2d8659 (ventajas) + #e89822 (callouts)
> **Nota técnica**: las clases CSS de cada SVG llevan sufijo numérico único (`.t1`, `.h1`…) para evitar colisiones de estilos entre los 16 diagramas embebidos en la misma página.

---

## Índice de diagramas

| ID | Título | Sección | Tipo | Formato |
|---|---|---|---|---|
| D1 | Modelos de puesto de trabajo: tradicional, VDI, RDSH y DaaS | §1.1.1 | Comparativa | 680×340 |
| D2 | Las capas del puesto de usuario y sus incidencias típicas | §1.1.2 | Capas | 680×360 |
| D3 | Tres arquitecturas de conexión de control remoto | §1.2.1 | Esquema de red | 680×370 |
| D4 | La cadena AAA de una sesión de asistencia remota | §1.2.2 | Flujo | 680×330 |
| D5 | Mapa de protocolos y puertos de gestión remota | §1.3.1 | Tabla visual | 680×380 |
| D6 | Gestión dentro de banda frente a fuera de banda | §1.3.1 | Comparativa | 680×300 |
| D7 | Del canal en claro al canal tunelizado | §1.3.2 | Flujo comparado | 680×300 |
| D8 | Herramientas de asistencia por sistema operativo | §1.3.3 | Bloques | 680×330 |
| D9 | Los seis bloques de la gestión centralizada del puesto | §1.3.4 | Ciclo | 680×320 |
| D10 | ITIL 4, ISO/IEC 20000 y COBIT: tres marcos, tres papeles | §2.1.1 | Comparativa | 680×320 |
| D11 | Ciclo de vida de una incidencia: ocho etapas y sus estados | §2.1.2 | Flujo | 680×340 |
| D12 | El CAU: canales de entrada y niveles de soporte | §2.2 | Embudo | 680×360 |
| D13 | Matriz impacto × urgencia y tiempos comprometidos | §2.3.1 | Matriz | 680×370 |
| D14 | Escalado funcional frente a escalado jerárquico | §2.3.2 | Ejes cruzados | 680×320 |
| D15 | Incidencia, problema, error conocido, petición y evento | §2.4.1 | Bloques | 680×340 |
| D16 | El círculo completo: seguridad, medición y mejora continua | §3 | Ciclo | 680×360 |

---

## D1 · Modelos de puesto de trabajo: tradicional, VDI, RDSH y DaaS

**Sección**: §1.1.1 — Entornos de escritorio tradicionales y virtualizados
**Propósito**: Fijar la diferencia entre los cuatro modelos de puesto, señalando dónde se ejecuta la aplicación en cada uno y qué consecuencia tiene para el soporte.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 346" role="img" aria-label="Comparativa de los cuatro modelos de puesto de trabajo: escritorio tradicional, infraestructura de escritorio virtual VDI, servicios de escritorio remoto por sesión RDSH y escritorio como servicio DaaS, indicando dónde se ejecuta la aplicación, qué viaja por la red y la consecuencia para el soporte técnico">
  <style>.t1{font:700 11px system-ui,sans-serif;fill:#fff}.s1{font:9px system-ui,sans-serif;fill:#fff}.d1{font:9px system-ui,sans-serif;fill:#333}.h1{font:700 13px system-ui,sans-serif;fill:#0055a0}.k1{font:700 9.5px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="340" y="20" text-anchor="middle" class="h1">Cuatro modelos de puesto de trabajo</text>
  <rect x="20" y="34" width="152" height="38" rx="5" fill="#0055a0"/><text x="96" y="50" text-anchor="middle" class="t1">TRADICIONAL</text><text x="96" y="64" text-anchor="middle" class="s1">cliente pesado (PC)</text>
  <rect x="187" y="34" width="152" height="38" rx="5" fill="#2d8659"/><text x="263" y="50" text-anchor="middle" class="t1">VDI</text><text x="263" y="64" text-anchor="middle" class="s1">1 máquina virtual/usuario</text>
  <rect x="354" y="34" width="152" height="38" rx="5" fill="#e89822"/><text x="430" y="50" text-anchor="middle" class="t1">RDSH</text><text x="430" y="64" text-anchor="middle" class="s1">N sesiones / 1 servidor</text>
  <rect x="521" y="34" width="152" height="38" rx="5" fill="#888"/><text x="597" y="50" text-anchor="middle" class="t1">DaaS</text><text x="597" y="64" text-anchor="middle" class="s1">lo anterior, en la nube</text>
  <text x="20" y="90" class="k1">DÓNDE SE EJECUTA LA APLICACIÓN</text>
  <rect x="20" y="96" width="152" height="30" rx="4" fill="#eef3f8"/><text x="96" y="115" text-anchor="middle" class="d1">En el equipo del usuario</text>
  <rect x="187" y="96" width="152" height="30" rx="4" fill="#eef3f8"/><text x="263" y="115" text-anchor="middle" class="d1">En el centro de datos</text>
  <rect x="354" y="96" width="152" height="30" rx="4" fill="#eef3f8"/><text x="430" y="115" text-anchor="middle" class="d1">En el centro de datos</text>
  <rect x="521" y="96" width="152" height="30" rx="4" fill="#eef3f8"/><text x="597" y="115" text-anchor="middle" class="d1">En la nube del proveedor</text>
  <text x="20" y="144" class="k1">QUÉ VIAJA POR LA RED</text>
  <rect x="20" y="150" width="152" height="30" rx="4" fill="#f5f5f5"/><text x="96" y="169" text-anchor="middle" class="d1">Datos de aplicación</text>
  <rect x="187" y="150" width="486" height="30" rx="4" fill="#f5f5f5"/><text x="430" y="169" text-anchor="middle" class="d1">Pantalla, teclado, ratón, audio y periféricos redirigidos</text>
  <text x="20" y="198" class="k1">AISLAMIENTO ENTRE USUARIOS</text>
  <rect x="20" y="204" width="152" height="30" rx="4" fill="#eef3f8"/><text x="96" y="223" text-anchor="middle" class="d1">Total (equipo propio)</text>
  <rect x="187" y="204" width="152" height="30" rx="4" fill="#eef3f8"/><text x="263" y="223" text-anchor="middle" class="d1">Alto (SO propio)</text>
  <rect x="354" y="204" width="152" height="30" rx="4" fill="#fbeaea"/><text x="430" y="223" text-anchor="middle" class="d1">Bajo (SO compartido)</text>
  <rect x="521" y="204" width="152" height="30" rx="4" fill="#eef3f8"/><text x="597" y="223" text-anchor="middle" class="d1">Según la modalidad</text>
  <text x="20" y="252" class="k1">CONSECUENCIA PARA EL SOPORTE</text>
  <rect x="20" y="258" width="152" height="44" rx="4" fill="#f5f5f5"/><text x="96" y="275" text-anchor="middle" class="d1">Equipo a equipo:</text><text x="96" y="290" text-anchor="middle" class="d1">parchear y reparar</text>
  <rect x="187" y="258" width="152" height="44" rx="4" fill="#f5f5f5"/><text x="263" y="275" text-anchor="middle" class="d1">Reasignar otra máquina</text><text x="263" y="290" text-anchor="middle" class="d1">virtual en minutos</text>
  <rect x="354" y="258" width="152" height="44" rx="4" fill="#f5f5f5"/><text x="430" y="275" text-anchor="middle" class="d1">Un usuario puede</text><text x="430" y="290" text-anchor="middle" class="d1">degradar a los demás</text>
  <rect x="521" y="258" width="152" height="44" rx="4" fill="#f5f5f5"/><text x="597" y="275" text-anchor="middle" class="d1">Capacidad y datos</text><text x="597" y="290" text-anchor="middle" class="d1">en manos del proveedor</text>
  <rect x="90" y="310" width="500" height="20" rx="4" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="324" text-anchor="middle" class="k1">Sin red no hay puesto en VDI, RDSH ni DaaS; el tradicional trabaja en local</text>
  <text x="670" y="343" text-anchor="end" style="font:10px system-ui;fill:#666">[Fuente: MS-RDS; VDI-VENDORS]</text>
</svg>
```

---

## D2 · Las capas del puesto de usuario y sus incidencias típicas

**Sección**: §1.1.2 — Componentes hardware y software del puesto de usuario
**Propósito**: Mostrar el puesto como una pila de capas y asociar a cada una la familia de incidencias que genera, que es el mapa mental del diagnóstico.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Las capas del puesto de usuario, desde el hardware y el firmware hasta los servicios corporativos, con la familia de incidencias típica de cada capa y la indicación de qué capas admiten intervención remota">
  <style>.t2{font:700 10.5px system-ui,sans-serif;fill:#fff}.d2{font:9px system-ui,sans-serif;fill:#333}.h2{font:700 13px system-ui,sans-serif;fill:#0055a0}.k2{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n2{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h2">El puesto de usuario, capa a capa</text>
  <text x="30" y="42" class="k2">CAPA</text><text x="250" y="42" class="k2">INCIDENCIAS TÍPICAS</text><text x="570" y="42" class="k2">¿EN REMOTO?</text>
  <rect x="20" y="50" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="70" text-anchor="middle" class="t2">Servicios corporativos</text>
  <rect x="243" y="50" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="70" text-anchor="middle" class="d2">Sede caída, aplicación lenta, servicio no disponible</text>
  <rect x="551" y="50" width="109" height="32" rx="4" fill="#2d8659"/><text x="605" y="70" text-anchor="middle" class="t2">Sí</text>
  <rect x="20" y="88" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="108" text-anchor="middle" class="t2">Conectividad</text>
  <rect x="243" y="88" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="108" text-anchor="middle" class="d2">Sin VPN, proxy, resolución de nombres, permisos</text>
  <rect x="551" y="88" width="109" height="32" rx="4" fill="#e89822"/><text x="605" y="108" text-anchor="middle" class="t2">Parcialmente</text>
  <rect x="20" y="126" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="146" text-anchor="middle" class="t2">Identidad y permisos</text>
  <rect x="243" y="126" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="146" text-anchor="middle" class="d2">Cuenta bloqueada, certificado caducado, sin permiso</text>
  <rect x="551" y="126" width="109" height="32" rx="4" fill="#2d8659"/><text x="605" y="146" text-anchor="middle" class="t2">Sí</text>
  <rect x="20" y="164" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="184" text-anchor="middle" class="t2">Aplicaciones</text>
  <rect x="243" y="164" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="184" text-anchor="middle" class="d2">Versión, complemento deshabilitado, error al abrir</text>
  <rect x="551" y="164" width="109" height="32" rx="4" fill="#2d8659"/><text x="605" y="184" text-anchor="middle" class="t2">Sí</text>
  <rect x="20" y="202" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="222" text-anchor="middle" class="t2">Configuración y seguridad</text>
  <rect x="243" y="202" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="222" text-anchor="middle" class="d2">Directiva nueva, antivirus bloquea, disco cifrado</text>
  <rect x="551" y="202" width="109" height="32" rx="4" fill="#2d8659"/><text x="605" y="222" text-anchor="middle" class="t2">Sí</text>
  <rect x="20" y="240" width="215" height="32" rx="4" fill="#0055a0"/><text x="128" y="260" text-anchor="middle" class="t2">Sistema operativo</text>
  <rect x="243" y="240" width="300" height="32" rx="4" fill="#eef3f8"/><text x="393" y="260" text-anchor="middle" class="d2">Servicio detenido, actualización fallida, error grave</text>
  <rect x="551" y="240" width="109" height="32" rx="4" fill="#e89822"/><text x="605" y="260" text-anchor="middle" class="t2">Si arranca</text>
  <rect x="20" y="278" width="215" height="32" rx="4" fill="#666"/><text x="128" y="298" text-anchor="middle" class="t2">Firmware (UEFI, TPM)</text>
  <rect x="243" y="278" width="300" height="32" rx="4" fill="#fbeaea"/><text x="393" y="298" text-anchor="middle" class="d2">No arranca, orden de arranque, clave de cifrado</text>
  <rect x="551" y="278" width="109" height="32" rx="4" fill="#e89822"/><text x="605" y="298" text-anchor="middle" class="t2">Fuera de banda</text>
  <rect x="20" y="316" width="215" height="32" rx="4" fill="#666"/><text x="128" y="336" text-anchor="middle" class="t2">Hardware y periféricos</text>
  <rect x="243" y="316" width="300" height="32" rx="4" fill="#fbeaea"/><text x="393" y="336" text-anchor="middle" class="d2">No enciende, disco, monitor, lector de tarjetas, cable</text>
  <rect x="551" y="316" width="109" height="32" rx="4" fill="#d13c3c"/><text x="605" y="336" text-anchor="middle" class="t2">No: presencial</text>
  <text x="670" y="356" text-anchor="end" class="n2">[Fuente: ITIL4; ENS]</text>
</svg>
```

---

## D3 · Tres arquitecturas de conexión de control remoto

**Sección**: §1.2.1 — Arquitecturas cliente-servidor y punto a punto
**Propósito**: Explicar por qué las herramientas modernas usan un servidor de mediación y cómo atraviesan el NAT y el cortafuegos sin abrir puertos entrantes.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 370" role="img" aria-label="Tres arquitecturas de conexión de control remoto: conexión directa cliente-servidor que exige puertos entrantes abiertos, conexión mediada por un servidor de intermediación con retransmisión, y conexión punto a punto establecida tras la mediación, indicando en cada caso el sentido de las conexiones">
  <style>.t3{font:700 10px system-ui,sans-serif;fill:#fff}.d3{font:9px system-ui,sans-serif;fill:#333}.h3{font:700 13px system-ui,sans-serif;fill:#0055a0}.k3{font:700 10px system-ui,sans-serif;fill:#0055a0}.n3{font:8.5px system-ui,sans-serif;fill:#666}.lb3{font:8.5px system-ui,sans-serif;fill:#0055a0}</style>
  <defs><marker id="a3" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h3">Cómo se ponen en contacto los dos extremos</text>
  <text x="20" y="46" class="k3">1 · CONEXIÓN DIRECTA CLIENTE-SERVIDOR</text>
  <rect x="20" y="54" width="130" height="44" rx="5" fill="#0055a0"/><text x="85" y="72" text-anchor="middle" class="t3">TÉCNICO</text><text x="85" y="88" text-anchor="middle" class="t3" style="font-weight:400">cliente / visor</text>
  <rect x="530" y="54" width="130" height="44" rx="5" fill="#2d8659"/><text x="595" y="72" text-anchor="middle" class="t3">PUESTO</text><text x="595" y="88" text-anchor="middle" class="t3" style="font-weight:400">servidor: escucha</text>
  <line x1="150" y1="76" x2="525" y2="76" stroke="#0055a0" stroke-width="2" marker-end="url(#a3)"/>
  <text x="337" y="70" text-anchor="middle" class="lb3">conexión entrante al puerto 3389 o 5900</text>
  <rect x="292" y="80" width="92" height="18" rx="3" fill="#d13c3c"/><text x="338" y="93" text-anchor="middle" class="t3">CORTAFUEGOS</text>
  <text x="20" y="118" class="d3">Requiere visibilidad de red y puertos entrantes abiertos. Inviable fuera de la red corporativa.</text>
  <line x1="20" y1="128" x2="660" y2="128" stroke="#ddd" stroke-width="1"/>
  <text x="20" y="150" class="k3">2 · CONEXIÓN MEDIADA CON RETRANSMISIÓN</text>
  <rect x="20" y="158" width="130" height="44" rx="5" fill="#0055a0"/><text x="85" y="176" text-anchor="middle" class="t3">TÉCNICO</text><text x="85" y="192" text-anchor="middle" class="t3" style="font-weight:400">salida por 443</text>
  <rect x="275" y="158" width="130" height="44" rx="5" fill="#e89822"/><text x="340" y="176" text-anchor="middle" class="t3">MEDIADOR</text><text x="340" y="192" text-anchor="middle" class="t3" style="font-weight:400">empareja y retransmite</text>
  <rect x="530" y="158" width="130" height="44" rx="5" fill="#2d8659"/><text x="595" y="176" text-anchor="middle" class="t3">PUESTO</text><text x="595" y="192" text-anchor="middle" class="t3" style="font-weight:400">salida por 443</text>
  <line x1="150" y1="180" x2="270" y2="180" stroke="#0055a0" stroke-width="2" marker-end="url(#a3)"/>
  <line x1="530" y1="180" x2="410" y2="180" stroke="#0055a0" stroke-width="2" marker-end="url(#a3)"/>
  <text x="20" y="222" class="d3">Ambos extremos abren conexión SALIENTE: atraviesa NAT y cortafuegos sin publicar puertos.</text>
  <text x="20" y="236" class="d3">Todo el tráfico pasa por el mediador, que centraliza autenticación y registro.</text>
  <line x1="20" y1="246" x2="660" y2="246" stroke="#ddd" stroke-width="1"/>
  <text x="20" y="268" class="k3">3 · PUNTO A PUNTO TRAS LA MEDIACIÓN</text>
  <rect x="20" y="276" width="130" height="44" rx="5" fill="#0055a0"/><text x="85" y="294" text-anchor="middle" class="t3">TÉCNICO</text><text x="85" y="310" text-anchor="middle" class="t3" style="font-weight:400">cliente / visor</text>
  <rect x="275" y="276" width="130" height="30" rx="5" fill="#888"/><text x="340" y="295" text-anchor="middle" class="t3">solo señalización</text>
  <rect x="530" y="276" width="130" height="44" rx="5" fill="#2d8659"/><text x="595" y="294" text-anchor="middle" class="t3">PUESTO</text><text x="595" y="310" text-anchor="middle" class="t3" style="font-weight:400">agente</text>
  <line x1="150" y1="286" x2="270" y2="286" stroke="#888" stroke-width="1.5" stroke-dasharray="4,3"/>
  <line x1="530" y1="286" x2="410" y2="286" stroke="#888" stroke-width="1.5" stroke-dasharray="4,3"/>
  <path d="M85,320 L85,338 L595,338 L595,320" fill="none" stroke="#2d8659" stroke-width="2.5" marker-end="url(#a3)"/>
  <text x="340" y="334" text-anchor="middle" class="lb3">canal directo tras perforar el NAT (si falla, cae en retransmisión)</text>
  <text x="20" y="356" class="d3">Mejor rendimiento y el mediador deja de ver el tráfico. Modelo dominante en herramientas comerciales.</text>
  <text x="670" y="366" text-anchor="end" class="n3">[Fuente: RFC6143; MS-RDS]</text>
</svg>
```

---

## D4 · La cadena AAA de una sesión de asistencia remota

**Sección**: §1.2.2 — Mecanismos de autenticación, autorización y sesión
**Propósito**: Ordenar los controles que deben cumplirse antes, durante y después de una sesión de control remoto, con el modelo AAA como esqueleto.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 330" role="img" aria-label="Cadena de controles de una sesión de asistencia remota agrupados en autenticación, autorización, control de la sesión y registro, con los mecanismos concretos de cada bloque y la advertencia de que hay que autenticar tanto al técnico como al equipo remoto">
  <style>.t4{font:700 11px system-ui,sans-serif;fill:#fff}.s4{font:9px system-ui,sans-serif;fill:#fff}.d4{font:9px system-ui,sans-serif;fill:#333}.h4{font:700 13px system-ui,sans-serif;fill:#0055a0}.k4{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n4{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a4" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h4">Antes, durante y después de la sesión</text>
  <rect x="20" y="36" width="150" height="40" rx="5" fill="#0055a0"/><text x="95" y="53" text-anchor="middle" class="t4">1 · AUTENTICACIÓN</text><text x="95" y="68" text-anchor="middle" class="s4">¿quién eres?</text>
  <rect x="185" y="36" width="150" height="40" rx="5" fill="#0055a0"/><text x="260" y="53" text-anchor="middle" class="t4">2 · AUTORIZACIÓN</text><text x="260" y="68" text-anchor="middle" class="s4">¿qué puedes hacer?</text>
  <rect x="350" y="36" width="150" height="40" rx="5" fill="#2d8659"/><text x="425" y="53" text-anchor="middle" class="t4">3 · SESIÓN</text><text x="425" y="68" text-anchor="middle" class="s4">¿cómo se controla?</text>
  <rect x="515" y="36" width="145" height="40" rx="5" fill="#e89822"/><text x="587" y="53" text-anchor="middle" class="t4">4 · REGISTRO</text><text x="587" y="68" text-anchor="middle" class="s4">¿qué has hecho?</text>
  <line x1="170" y1="56" x2="182" y2="56" stroke="#0055a0" stroke-width="2" marker-end="url(#a4)"/>
  <line x1="335" y1="56" x2="347" y2="56" stroke="#0055a0" stroke-width="2" marker-end="url(#a4)"/>
  <line x1="500" y1="56" x2="512" y2="56" stroke="#0055a0" stroke-width="2" marker-end="url(#a4)"/>
  <rect x="20" y="86" width="150" height="150" rx="4" fill="#eef3f8"/>
  <text x="30" y="104" class="d4">· Identidad NOMINAL</text>
  <text x="30" y="120" class="d4">· Directorio corporativo</text>
  <text x="30" y="136" class="d4">· Kerberos o clave pública</text>
  <text x="30" y="152" class="d4">· Segundo factor (MFA)</text>
  <text x="30" y="168" class="d4">· Código de sesión</text>
  <text x="30" y="184" class="d4">  de un solo uso</text>
  <text x="30" y="206" class="k4">Y TAMBIÉN:</text>
  <text x="30" y="222" class="d4">autenticar al EQUIPO</text>
  <rect x="185" y="86" width="150" height="150" rx="4" fill="#eef3f8"/>
  <text x="195" y="104" class="d4">· Perfiles por rol (RBAC)</text>
  <text x="195" y="120" class="d4">· Alcance: qué equipos</text>
  <text x="195" y="136" class="d4">· Modo: ver / controlar /</text>
  <text x="195" y="152" class="d4">  ficheros / órdenes</text>
  <text x="195" y="168" class="d4">· Segregación de</text>
  <text x="195" y="184" class="d4">  funciones</text>
  <text x="195" y="206" class="d4">· Elevación temporal</text>
  <text x="195" y="222" class="d4">  ligada a un tique</text>
  <rect x="350" y="86" width="150" height="150" rx="4" fill="#eaf3ee"/>
  <text x="360" y="104" class="d4">· Consentimiento</text>
  <text x="360" y="120" class="d4">· Indicador visible</text>
  <text x="360" y="136" class="d4">· Corte por el usuario</text>
  <text x="360" y="152" class="d4">· Expiración y duración</text>
  <text x="360" y="168" class="d4">  máxima</text>
  <text x="360" y="184" class="d4">· Bloqueo al desconectar</text>
  <text x="360" y="206" class="d4">· Canal cifrado</text>
  <text x="360" y="222" class="d4">  extremo a extremo</text>
  <rect x="515" y="86" width="145" height="150" rx="4" fill="#fdf3e6"/>
  <text x="525" y="104" class="d4">· Quién, cuándo,</text>
  <text x="525" y="120" class="d4">  sobre qué equipo</text>
  <text x="525" y="136" class="d4">· Tique asociado</text>
  <text x="525" y="152" class="d4">· Modo de la sesión</text>
  <text x="525" y="168" class="d4">· Ficheros y portapapeles</text>
  <text x="525" y="184" class="d4">· Elevación de privilegios</text>
  <text x="525" y="206" class="d4">· Registro íntegro y</text>
  <text x="525" y="222" class="d4">  centralizado</text>
  <rect x="20" y="250" width="640" height="30" rx="5" fill="#d13c3c"/>
  <text x="340" y="269" text-anchor="middle" class="t4">Autenticar solo al técnico no basta: si no se verifica el equipo remoto, cabe un ataque de intermediario</text>
  <rect x="90" y="288" width="500" height="26" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="305" text-anchor="middle" class="k4">Sesión sin tique asociado = acceso sin justificación: hallazgo crítico de auditoría</text>
  <text x="670" y="326" text-anchor="end" class="n4">[Fuente: RFC2865; ENS; RFC4253]</text>
</svg>
```

---

## D5 · Mapa de protocolos y puertos de gestión remota

**Sección**: §1.3.1 — Protocolos de nivel de aplicación para gestión remota
**Propósito**: Reunir en una sola imagen los protocolos, sus puertos y su naturaleza. Es el diagrama de memorización directa del bloque técnico.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 380" role="img" aria-label="Tabla visual de los protocolos de control y gestión remota con sus puertos: RFB VNC en el 5900, RDP en el 3389, SSH en el 22, Telnet en el 23 obsoleto, WinRM en el 5985 y 5986, SNMP en el 161 y 162, NETCONF en el 830, IPMI en el 623, Redfish en el 443, reenvío de X11 en el 6000 y Wake-on-LAN en los puertos 7 y 9">
  <style>.t5{font:700 10px system-ui,sans-serif;fill:#fff}.d5{font:9px system-ui,sans-serif;fill:#333}.p5{font:700 10px system-ui,sans-serif;fill:#0055a0}.h5{font:700 13px system-ui,sans-serif;fill:#0055a0}.k5{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n5{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h5">Protocolos y puertos de gestión remota</text>
  <rect x="20" y="32" width="130" height="20" rx="3" fill="#0055a0"/><text x="85" y="46" text-anchor="middle" class="t5">PROTOCOLO</text>
  <rect x="155" y="32" width="95" height="20" rx="3" fill="#0055a0"/><text x="202" y="46" text-anchor="middle" class="t5">PUERTO</text>
  <rect x="255" y="32" width="160" height="20" rx="3" fill="#0055a0"/><text x="335" y="46" text-anchor="middle" class="t5">QUÉ TRANSMITE</text>
  <rect x="420" y="32" width="240" height="20" rx="3" fill="#0055a0"/><text x="540" y="46" text-anchor="middle" class="t5">USO PRINCIPAL</text>
  <rect x="20" y="56" width="640" height="24" rx="3" fill="#eef3f8"/>
  <text x="30" y="72" class="d5">RFB (VNC)</text><text x="165" y="72" class="p5">TCP 5900+N</text><text x="265" y="72" class="d5">Píxeles del framebuffer</text><text x="430" y="72" class="d5">Asistencia compartiendo la sesión del usuario</text>
  <rect x="20" y="84" width="640" height="24" rx="3" fill="#f5f5f5"/>
  <text x="30" y="100" class="d5">RDP</text><text x="165" y="100" class="p5">TCP/UDP 3389</text><text x="265" y="100" class="d5">Primitivas y canales</text><text x="430" y="100" class="d5">Escritorio remoto; abre sesión independiente</text>
  <rect x="20" y="112" width="640" height="24" rx="3" fill="#eef3f8"/>
  <text x="30" y="128" class="d5">SSH</text><text x="165" y="128" class="p5">TCP 22</text><text x="265" y="128" class="d5">Texto cifrado + túneles</text><text x="430" y="128" class="d5">Administración de Unix, Linux y red</text>
  <rect x="20" y="140" width="640" height="24" rx="3" fill="#fbeaea"/>
  <text x="30" y="156" class="d5">Telnet</text><text x="165" y="156" class="p5">TCP 23</text><text x="265" y="156" class="d5">Texto EN CLARO</text><text x="430" y="156" class="d5" style="font-size:8.6px">Obsoleto y desaconsejado: debe estar deshabilitado</text>
  <rect x="20" y="168" width="640" height="24" rx="3" fill="#f5f5f5"/>
  <text x="30" y="184" class="d5">WinRM</text><text x="165" y="184" class="p5">TCP 5985/5986</text><text x="265" y="184" class="d5">WS-Management (DMTF)</text><text x="430" y="184" class="d5">Órdenes y automatización en Windows</text>
  <rect x="20" y="196" width="640" height="24" rx="3" fill="#eef3f8"/>
  <text x="30" y="212" class="d5">SNMP</text><text x="165" y="212" class="p5">UDP 161/162</text><text x="265" y="212" class="d5">Consultas y avisos</text><text x="430" y="212" class="d5">Monitorización; v3 es la única con seguridad real</text>
  <rect x="20" y="224" width="640" height="24" rx="3" fill="#f5f5f5"/>
  <text x="30" y="240" class="d5">NETCONF</text><text x="165" y="240" class="p5">TCP 830</text><text x="265" y="240" class="d5">XML sobre SSH</text><text x="430" y="240" class="d5">Configuración de dispositivos de red</text>
  <rect x="20" y="252" width="640" height="24" rx="3" fill="#fdf3e6"/>
  <text x="30" y="268" class="d5">IPMI (BMC)</text><text x="165" y="268" class="p5">UDP 623</text><text x="265" y="268" class="d5">Fuera de banda</text><text x="430" y="268" class="d5">Control con el equipo apagado o el SO caído</text>
  <rect x="20" y="280" width="640" height="24" rx="3" fill="#fdf3e6"/>
  <text x="30" y="296" class="d5">Redfish</text><text x="165" y="296" class="p5">TCP 443</text><text x="265" y="296" class="d5">REST sobre HTTPS</text><text x="430" y="296" class="d5">Sucesor moderno de IPMI</text>
  <rect x="20" y="308" width="640" height="24" rx="3" fill="#eef3f8"/>
  <text x="30" y="324" class="d5">X11 (reenvío)</text><text x="165" y="324" class="p5">TCP 6000+N</text><text x="265" y="324" class="d5">Objetos gráficos</text><text x="430" y="324" class="d5">Aplicación gráfica Unix remota, siempre sobre SSH</text>
  <rect x="20" y="336" width="640" height="24" rx="3" fill="#eaf3ee"/>
  <text x="30" y="352" class="d5">Wake-on-LAN</text><text x="165" y="352" class="p5">UDP 7 / 9</text><text x="265" y="352" class="d5">Paquete mágico</text><text x="430" y="352" class="d5">Encendido remoto para mantenimiento nocturno</text>
  <text x="670" y="374" text-anchor="end" class="n5">[Fuente: RFC6143; MS-RDPBCGR; RFC4253; DSP0226; IPMI2]</text>
</svg>
```

---

## D6 · Gestión dentro de banda frente a fuera de banda

**Sección**: §1.3.1 — Protocolos de nivel de aplicación para gestión remota
**Propósito**: Aislar la distinción que resuelve el caso típico de «el equipo no arranca y está a veinte kilómetros».

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Comparación entre gestión dentro de banda, que depende del sistema operativo del equipo y usa RDP, VNC, SSH o WinRM, y gestión fuera de banda, que usa un controlador dedicado con red y alimentación propias mediante IPMI o Redfish y funciona con el equipo apagado o con el sistema operativo caído">
  <style>.t6{font:700 11px system-ui,sans-serif;fill:#fff}.s6{font:9px system-ui,sans-serif;fill:#fff}.d6{font:9.5px system-ui,sans-serif;fill:#333}.h6{font:700 13px system-ui,sans-serif;fill:#0055a0}.k6{font:700 10px system-ui,sans-serif;fill:#0055a0}.n6{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a6" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h6">Dentro de banda frente a fuera de banda</text>
  <rect x="20" y="34" width="315" height="26" rx="5" fill="#0055a0"/><text x="177" y="52" text-anchor="middle" class="t6">DENTRO DE BANDA (in-band)</text>
  <rect x="345" y="34" width="315" height="26" rx="5" fill="#e89822"/><text x="502" y="52" text-anchor="middle" class="t6">FUERA DE BANDA (out-of-band)</text>
  <rect x="20" y="70" width="315" height="120" rx="5" fill="#eef3f8"/>
  <rect x="40" y="84" width="275" height="26" rx="4" fill="#2d8659"/><text x="177" y="102" text-anchor="middle" class="s6">Aplicación de gestión (servidor RDP, VNC, sshd)</text>
  <rect x="40" y="116" width="275" height="26" rx="4" fill="#0055a0"/><text x="177" y="134" text-anchor="middle" class="s6">Sistema operativo del equipo</text>
  <rect x="40" y="148" width="275" height="26" rx="4" fill="#666"/><text x="177" y="166" text-anchor="middle" class="s6">Hardware · tarjeta de red del sistema</text>
  <rect x="345" y="70" width="315" height="120" rx="5" fill="#fdf3e6"/>
  <rect x="365" y="84" width="275" height="26" rx="4" fill="#888" opacity="0.5"/><text x="502" y="102" text-anchor="middle" class="s6">Sistema operativo: puede estar caído o apagado</text>
  <rect x="365" y="116" width="275" height="58" rx="4" fill="#e89822"/><text x="502" y="136" text-anchor="middle" class="t6">CONTROLADOR DE GESTIÓN (BMC)</text><text x="502" y="152" text-anchor="middle" class="s6">procesador, memoria, red y alimentación propios</text><text x="502" y="168" text-anchor="middle" class="s6">IPMI · UDP 623 · Redfish · HTTPS</text>
  <text x="30" y="210" class="k6">PERMITE</text>
  <text x="30" y="228" class="d6">Ver el escritorio, ejecutar órdenes,</text>
  <text x="30" y="244" class="d6">instalar software, leer registros</text>
  <text x="355" y="210" class="k6">PERMITE ADEMÁS</text>
  <text x="355" y="228" class="d6">Encender y apagar, entrar en el firmware,</text>
  <text x="355" y="244" class="d6">ver la consola desde el arranque, montar imagen</text>
  <rect x="20" y="256" width="315" height="26" rx="4" fill="#d13c3c"/><text x="177" y="274" text-anchor="middle" class="t6">Si el sistema operativo no arranca, NO SIRVE</text>
  <rect x="345" y="256" width="315" height="26" rx="4" fill="#2d8659"/><text x="502" y="274" text-anchor="middle" class="t6">Funciona con el equipo apagado o averiado</text>
  <text x="670" y="296" text-anchor="end" class="n6">[Fuente: IPMI2; DSP0266]</text>
</svg>
```

---

## D7 · Del canal en claro al canal tunelizado

**Sección**: §1.3.2 — Canales de comunicación seguros y cifrado
**Propósito**: Mostrar por qué un protocolo sin cifrado no debe usarse desnudo y cómo se protege encapsulándolo.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Comparación entre una sesión de VNC o Telnet en claro, que un atacante situado en la red puede leer y modificar, y la misma sesión encapsulada dentro de un túnel SSH o TLS, con el servidor escuchando solo en la interfaz local, junto con las cuatro propiedades de seguridad que aporta el cifrado del canal">
  <style>.t7{font:700 10.5px system-ui,sans-serif;fill:#fff}.s7{font:9px system-ui,sans-serif;fill:#fff}.d7{font:9.5px system-ui,sans-serif;fill:#333}.h7{font:700 13px system-ui,sans-serif;fill:#0055a0}.k7{font:700 10px system-ui,sans-serif;fill:#0055a0}.n7{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a7" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h7">Proteger un protocolo que no cifra</text>
  <text x="20" y="44" class="k7">SIN PROTEGER</text>
  <rect x="20" y="52" width="120" height="38" rx="5" fill="#0055a0"/><text x="80" y="68" text-anchor="middle" class="t7">TÉCNICO</text><text x="80" y="82" text-anchor="middle" class="s7">visor VNC</text>
  <rect x="540" y="52" width="120" height="38" rx="5" fill="#2d8659"/><text x="600" y="68" text-anchor="middle" class="t7">PUESTO</text><text x="600" y="82" text-anchor="middle" class="s7">servidor VNC</text>
  <line x1="140" y1="71" x2="535" y2="71" stroke="#d13c3c" stroke-width="2.5" stroke-dasharray="6,3" marker-end="url(#a7)"/>
  <rect x="245" y="56" width="185" height="30" rx="4" fill="#d13c3c"/><text x="337" y="76" text-anchor="middle" class="t7">PANTALLA Y TECLAS EN CLARO</text>
  <text x="20" y="108" class="d7">Un atacante en la red lee la pantalla, captura lo tecleado y puede alterar la sesión.</text>
  <line x1="20" y1="118" x2="660" y2="118" stroke="#ddd" stroke-width="1"/>
  <text x="20" y="140" class="k7">PROTEGIDO POR TÚNEL</text>
  <rect x="20" y="148" width="120" height="38" rx="5" fill="#0055a0"/><text x="80" y="164" text-anchor="middle" class="t7">TÉCNICO</text><text x="80" y="178" text-anchor="middle" class="s7">visor a 127.0.0.1</text>
  <rect x="540" y="148" width="120" height="38" rx="5" fill="#2d8659"/><text x="600" y="164" text-anchor="middle" class="t7">PUESTO</text><text x="600" y="178" text-anchor="middle" class="s7">VNC solo en local</text>
  <rect x="150" y="144" width="380" height="46" rx="6" fill="#2d8659" opacity="0.15" stroke="#2d8659" stroke-width="2"/>
  <text x="340" y="162" text-anchor="middle" class="k7">TÚNEL SSH (22) o TLS 1.3 (443)</text>
  <line x1="165" y1="176" x2="520" y2="176" stroke="#2d8659" stroke-width="2.5" marker-end="url(#a7)"/>
  <text x="340" y="186" text-anchor="middle" class="n7">tráfico VNC encapsulado y cifrado</text>
  <text x="20" y="208" class="d7">El servidor VNC escucha solo en la interfaz local: es inalcanzable directamente desde la red.</text>
  <text x="20" y="234" class="k7">CUATRO PROPIEDADES QUE APORTA EL CANAL SEGURO</text>
  <rect x="20" y="242" width="155" height="40" rx="4" fill="#0055a0"/><text x="97" y="258" text-anchor="middle" class="t7">CONFIDENCIALIDAD</text><text x="97" y="273" text-anchor="middle" class="s7">nadie lee la pantalla</text>
  <rect x="182" y="242" width="155" height="40" rx="4" fill="#0055a0"/><text x="259" y="258" text-anchor="middle" class="t7">INTEGRIDAD</text><text x="259" y="273" text-anchor="middle" class="s7">nadie altera lo enviado</text>
  <rect x="344" y="242" width="155" height="40" rx="4" fill="#2d8659"/><text x="421" y="258" text-anchor="middle" class="t7">AUTENTICIDAD</text><text x="421" y="273" text-anchor="middle" class="s7">nadie suplanta un extremo</text>
  <rect x="506" y="242" width="154" height="40" rx="4" fill="#e89822"/><text x="583" y="258" text-anchor="middle" class="t7">TRAZABILIDAD</text><text x="583" y="273" text-anchor="middle" class="s7">registro nominal</text>
  <text x="670" y="296" text-anchor="end" class="n7">[Fuente: RFC6143; RFC4254; RFC9846]</text>
</svg>
```

---

## D8 · Herramientas de asistencia por sistema operativo

**Sección**: §1.3.3 — Herramientas de asistencia remota en sistemas operativos
**Propósito**: Ordenar las herramientas nativas de cada sistema y, sobre todo, separar las que **comparten** la sesión del usuario (válidas para asistir) de las que abren una sesión **nueva**.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 330" role="img" aria-label="Herramientas de asistencia remota nativas de Windows, Unix y Linux y macOS, separadas según compartan la sesión existente del usuario, lo que sirve para asistir, o abran una sesión nueva independiente, que sirve para administrar pero no para reproducir el problema del usuario">
  <style>.t8{font:700 10.5px system-ui,sans-serif;fill:#fff}.s8{font:9px system-ui,sans-serif;fill:#fff}.d8{font:9px system-ui,sans-serif;fill:#333}.h8{font:700 13px system-ui,sans-serif;fill:#0055a0}.k8{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n8{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h8">Herramientas nativas y modo de sesión</text>
  <rect x="20" y="34" width="210" height="28" rx="5" fill="#0055a0"/><text x="125" y="53" text-anchor="middle" class="t8">WINDOWS</text>
  <rect x="240" y="34" width="210" height="28" rx="5" fill="#0055a0"/><text x="345" y="53" text-anchor="middle" class="t8">UNIX / LINUX</text>
  <rect x="460" y="34" width="200" height="28" rx="5" fill="#0055a0"/><text x="560" y="53" text-anchor="middle" class="t8">macOS</text>
  <rect x="20" y="70" width="640" height="26" rx="4" fill="#2d8659"/>
  <text x="340" y="88" text-anchor="middle" class="t8">COMPARTEN LA SESIÓN DEL USUARIO → sirven para ASISTIR</text>
  <rect x="20" y="102" width="210" height="76" rx="4" fill="#eaf3ee"/>
  <text x="32" y="120" class="d8">· Asistencia rápida</text>
  <text x="32" y="136" class="d8">· Asistencia remota (msra)</text>
  <text x="32" y="152" class="d8">· Shadowing de RDS/VDI</text>
  <text x="32" y="170" class="k8">con código y consentimiento</text>
  <rect x="240" y="102" width="210" height="76" rx="4" fill="#eaf3ee"/>
  <text x="252" y="120" class="d8">· x11vnc sobre la consola</text>
  <text x="252" y="136" class="d8">· Reenvío X11 (ssh -X)</text>
  <text x="252" y="152" class="d8">· screen / tmux compartido</text>
  <text x="252" y="170" class="k8">la sesión sobrevive al corte</text>
  <rect x="460" y="102" width="200" height="76" rx="4" fill="#eaf3ee"/>
  <text x="472" y="120" class="d8">· Compartir pantalla (VNC)</text>
  <text x="472" y="136" class="d8">· Apple Remote Desktop</text>
  <text x="472" y="152" class="d8">  (asistencia + inventario</text>
  <text x="472" y="168" class="d8">  y despliegue)</text>
  <rect x="20" y="188" width="640" height="26" rx="4" fill="#e89822"/>
  <text x="340" y="206" text-anchor="middle" class="t8">ABREN UNA SESIÓN NUEVA → sirven para ADMINISTRAR, no para asistir</text>
  <rect x="20" y="220" width="210" height="62" rx="4" fill="#fdf3e6"/>
  <text x="32" y="238" class="d8">· Escritorio remoto (mstsc)</text>
  <text x="32" y="254" class="d8">· PowerShell Remoting</text>
  <text x="32" y="270" class="d8">· Consolas remotas (RSAT)</text>
  <rect x="240" y="220" width="210" height="62" rx="4" fill="#fdf3e6"/>
  <text x="252" y="238" class="d8">· SSH interactivo</text>
  <text x="252" y="254" class="d8">· Servidor VNC virtual</text>
  <text x="252" y="270" class="d8">· xrdp · X2Go · SPICE</text>
  <rect x="460" y="220" width="200" height="62" rx="4" fill="#fdf3e6"/>
  <text x="472" y="238" class="d8">· SSH (sesión de consola)</text>
  <text x="472" y="254" class="d8">· Órdenes remotas de ARD</text>
  <rect x="60" y="292" width="560" height="26" rx="5" fill="#d13c3c"/>
  <text x="340" y="310" text-anchor="middle" class="t8">Error frecuente: entrar por RDP para «asistir» y ver un escritorio distinto del que ve el usuario</text>
  <text x="670" y="326" text-anchor="end" class="n8">[Fuente: MS-QUICKASSIST; MS-RDS; OPENSSH; APPLE-ARD]</text>
</svg>
```

---
## D9 · Los seis bloques de la gestión centralizada del puesto

**Sección**: §1.3.4 — Soluciones centralizadas de gestión de puestos de trabajo
**Propósito**: Presentar las funciones de una plataforma de gestión unificada del puesto como un ciclo continuo que va del inventario al soporte y vuelve a empezar.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Los seis bloques funcionales de una plataforma de gestión centralizada del puesto de trabajo: inventario y descubrimiento, despliegue de sistemas y software, configuración y cumplimiento, parcheo y actualizaciones, seguridad del punto final y soporte integrado, dispuestos como un ciclo que convierte el soporte reactivo en proactivo">
  <style>.t9{font:700 10.5px system-ui,sans-serif;fill:#fff}.s9{font:9px system-ui,sans-serif;fill:#fff}.d9{font:9px system-ui,sans-serif;fill:#333}.h9{font:700 13px system-ui,sans-serif;fill:#0055a0}.k9{font:700 10px system-ui,sans-serif;fill:#0055a0}.n9{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a9" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h9">Gestión centralizada del parque de puestos</text>
  <rect x="20" y="36" width="205" height="52" rx="5" fill="#0055a0"/><text x="122" y="55" text-anchor="middle" class="t9">1 · INVENTARIO</text><text x="122" y="70" text-anchor="middle" class="s9">hardware, software, parches</text><text x="122" y="83" text-anchor="middle" class="s9">alimenta la CMDB</text>
  <rect x="237" y="36" width="205" height="52" rx="5" fill="#0055a0"/><text x="339" y="55" text-anchor="middle" class="t9">2 · DESPLIEGUE</text><text x="339" y="70" text-anchor="middle" class="s9">imagen base, PXE, catálogo</text><text x="339" y="83" text-anchor="middle" class="s9">de aplicaciones</text>
  <rect x="454" y="36" width="206" height="52" rx="5" fill="#0055a0"/><text x="557" y="55" text-anchor="middle" class="t9">3 · CONFIGURACIÓN</text><text x="557" y="70" text-anchor="middle" class="s9">directivas, líneas base</text><text x="557" y="83" text-anchor="middle" class="s9">y control de cumplimiento</text>
  <line x1="225" y1="62" x2="234" y2="62" stroke="#0055a0" stroke-width="2" marker-end="url(#a9)"/>
  <line x1="442" y1="62" x2="451" y2="62" stroke="#0055a0" stroke-width="2" marker-end="url(#a9)"/>
  <path d="M660,88 L668,88 L668,110 L12,110 L12,132 L17,132" fill="none" stroke="#0055a0" stroke-width="2" marker-end="url(#a9)"/>
  <rect x="20" y="126" width="205" height="52" rx="5" fill="#2d8659"/><text x="122" y="145" text-anchor="middle" class="t9">4 · PARCHEO</text><text x="122" y="160" text-anchor="middle" class="s9">despliegue por anillos</text><text x="122" y="173" text-anchor="middle" class="s9">y ventanas de mantenimiento</text>
  <rect x="237" y="126" width="205" height="52" rx="5" fill="#2d8659"/><text x="339" y="145" text-anchor="middle" class="t9">5 · SEGURIDAD</text><text x="339" y="160" text-anchor="middle" class="s9">antivirus, cifrado de disco</text><text x="339" y="173" text-anchor="middle" class="s9">y borrado remoto</text>
  <rect x="454" y="126" width="206" height="52" rx="5" fill="#2d8659"/><text x="557" y="145" text-anchor="middle" class="t9">6 · SOPORTE</text><text x="557" y="160" text-anchor="middle" class="s9">acciones remotas y sesión</text><text x="557" y="173" text-anchor="middle" class="s9">de control desde el tique</text>
  <line x1="225" y1="152" x2="234" y2="152" stroke="#0055a0" stroke-width="2" marker-end="url(#a9)"/>
  <line x1="442" y1="152" x2="451" y2="152" stroke="#0055a0" stroke-width="2" marker-end="url(#a9)"/>
  <path d="M557,178 L557,196 L5,196 L5,62 L17,62" fill="none" stroke="#888" stroke-width="1.5" stroke-dasharray="5,3" marker-end="url(#a9)"/>
  <text x="340" y="192" text-anchor="middle" class="n9">lo aprendido en el soporte actualiza el inventario y las líneas base</text>
  <rect x="20" y="210" width="315" height="60" rx="5" fill="#fbeaea"/>
  <text x="177" y="228" text-anchor="middle" class="k9">SIN GESTIÓN CENTRALIZADA</text>
  <text x="177" y="246" text-anchor="middle" class="d9">Soporte REACTIVO: se espera la llamada</text>
  <text x="177" y="262" text-anchor="middle" class="d9">del usuario cuando ya ha fallado algo</text>
  <rect x="345" y="210" width="315" height="60" rx="5" fill="#eaf3ee"/>
  <text x="502" y="228" text-anchor="middle" class="k9">CON GESTIÓN CENTRALIZADA</text>
  <text x="502" y="246" text-anchor="middle" class="d9">Soporte PROACTIVO: se detecta el disco lleno</text>
  <text x="502" y="262" text-anchor="middle" class="d9">o el parche que falta antes de la incidencia</text>
  <rect x="90" y="278" width="500" height="24" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="294" text-anchor="middle" class="k9">Reduce el NÚMERO de incidencias, no solo el tiempo de resolución</text>
  <text x="670" y="316" text-anchor="end" class="n9">[Fuente: MS-INTUNE; UEM; ITIL4]</text>
</svg>
```

---

## D10 · ITIL 4, ISO/IEC 20000 y COBIT: tres marcos, tres papeles

**Sección**: §2.1.1 — Principios de ITIL aplicados a la gestión de incidencias
**Propósito**: Evitar la confusión más frecuente del bloque organizativo: qué es cada marco, qué aporta y qué certifica.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Comparación de los tres marcos de referencia de gestión y gobierno de servicios de tecnología: COBIT 2019 en el plano del gobierno, ITIL 4 como buenas prácticas de gestión del servicio e ISO IEC 20000-1 como norma certificable de requisitos, con la indicación de que ITIL certifica personas e ISO certifica organizaciones, y con el Esquema Nacional de Seguridad como capa normativa obligatoria en el sector público">
  <style>.t10{font:700 11px system-ui,sans-serif;fill:#fff}.s10{font:9px system-ui,sans-serif;fill:#fff}.d10{font:9px system-ui,sans-serif;fill:#333}.h10{font:700 13px system-ui,sans-serif;fill:#0055a0}.k10{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n10{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h10">Tres marcos que no compiten: se superponen</text>
  <rect x="20" y="34" width="640" height="42" rx="5" fill="#888"/>
  <text x="340" y="52" text-anchor="middle" class="t10">COBIT 2019 · GOBIERNO</text>
  <text x="340" y="68" text-anchor="middle" class="s10">¿Qué debe hacer la tecnología para cumplir los objetivos de la organización? · DSS01 · DSS02 · DSS03 · DSS05</text>
  <rect x="20" y="84" width="640" height="42" rx="5" fill="#0055a0"/>
  <text x="340" y="102" text-anchor="middle" class="t10">ITIL 4 · BUENAS PRÁCTICAS DE GESTIÓN DEL SERVICIO</text>
  <text x="340" y="118" text-anchor="middle" class="s10">Sistema de Valor del Servicio · cadena de valor · 4 dimensiones · 7 principios guía · 34 prácticas</text>
  <rect x="20" y="134" width="640" height="42" rx="5" fill="#2d8659"/>
  <text x="340" y="152" text-anchor="middle" class="t10">ISO/IEC 20000-1:2018 · REQUISITOS CERTIFICABLES</text>
  <text x="340" y="168" text-anchor="middle" class="s10">Sistema de gestión del servicio (SGS) auditable · cláusula 8.6: incidencias, peticiones y problemas</text>
  <rect x="20" y="184" width="640" height="42" rx="5" fill="#d13c3c"/>
  <text x="340" y="202" text-anchor="middle" class="t10">ENS · RD 311/2022 · OBLIGATORIO EN EL SECTOR PÚBLICO</text>
  <text x="340" y="218" text-anchor="middle" class="s10">No es un marco de gestión del servicio, sino de seguridad: control de acceso, registro y gestión de incidentes</text>
  <text x="20" y="248" class="k10">QUÉ CERTIFICA CADA UNO</text>
  <rect x="20" y="256" width="205" height="42" rx="4" fill="#eef3f8"/><text x="122" y="274" text-anchor="middle" class="d10">ITIL 4 certifica a PERSONAS</text><text x="122" y="290" text-anchor="middle" class="d10">(no certifica organizaciones)</text>
  <rect x="237" y="256" width="205" height="42" rx="4" fill="#eaf3ee"/><text x="339" y="274" text-anchor="middle" class="d10">ISO/IEC 20000-1 certifica</text><text x="339" y="290" text-anchor="middle" class="d10">a ORGANIZACIONES</text>
  <rect x="454" y="256" width="206" height="42" rx="4" fill="#fbeaea"/><text x="557" y="274" text-anchor="middle" class="d10">ENS: conformidad y</text><text x="557" y="290" text-anchor="middle" class="d10">auditoría bienal (media/alta)</text>
  <text x="670" y="314" text-anchor="end" class="n10">[Fuente: ITIL4; ISO20000; COBIT2019; ENS]</text>
</svg>
```

---

## D11 · Ciclo de vida de una incidencia: ocho etapas y sus estados

**Sección**: §2.1.2 — Ciclo de vida y flujos de trabajo de atención al usuario
**Propósito**: Fijar la secuencia canónica del tique y señalar en qué estados se detiene el reloj del acuerdo de nivel de servicio.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Las ocho etapas del ciclo de vida de una incidencia, desde la detección y el registro hasta la recuperación y el cierre, con los estados asociados y la indicación de en cuáles se detiene el reloj del acuerdo de nivel de servicio, más los cuatro flujos diferenciados: estándar, incidencia grave, incidencia de seguridad y petición de servicio">
  <style>.t11{font:700 9.5px system-ui,sans-serif;fill:#fff}.d11{font:9px system-ui,sans-serif;fill:#333}.h11{font:700 13px system-ui,sans-serif;fill:#0055a0}.k11{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n11{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a11" markerWidth="7" markerHeight="7" refX="6" refY="2.5" orient="auto"><path d="M0,0 L6,2.5 L0,5 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h11">De la detección al cierre: ocho etapas</text>
  <rect x="20" y="34" width="152" height="36" rx="4" fill="#0055a0"/><text x="96" y="49" text-anchor="middle" class="t11">1 · DETECCIÓN</text><text x="96" y="63" text-anchor="middle" class="t11" style="font-weight:400">usuario o monitorización</text>
  <rect x="184" y="34" width="152" height="36" rx="4" fill="#0055a0"/><text x="260" y="49" text-anchor="middle" class="t11">2 · REGISTRO</text><text x="260" y="63" text-anchor="middle" class="t11" style="font-weight:400">lo no registrado no existe</text>
  <rect x="348" y="34" width="152" height="36" rx="4" fill="#0055a0"/><text x="424" y="49" text-anchor="middle" class="t11">3 · CATEGORIZACIÓN</text><text x="424" y="63" text-anchor="middle" class="t11" style="font-weight:400">taxonomía y encaminamiento</text>
  <rect x="512" y="34" width="148" height="36" rx="4" fill="#0055a0"/><text x="586" y="49" text-anchor="middle" class="t11">4 · PRIORIZACIÓN</text><text x="586" y="63" text-anchor="middle" class="t11" style="font-weight:400">impacto × urgencia</text>
  <line x1="172" y1="52" x2="181" y2="52" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <line x1="336" y1="52" x2="345" y2="52" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <line x1="500" y1="52" x2="509" y2="52" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <path d="M660,70 L668,70 L668,88 L12,88 L12,106 L17,106" fill="none" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <rect x="20" y="100" width="152" height="36" rx="4" fill="#2d8659"/><text x="96" y="115" text-anchor="middle" class="t11">5 · DIAGNÓSTICO</text><text x="96" y="129" text-anchor="middle" class="t11" style="font-weight:400">asistencia remota · N1</text>
  <rect x="184" y="100" width="152" height="36" rx="4" fill="#e89822"/><text x="260" y="115" text-anchor="middle" class="t11">6 · ESCALADO</text><text x="260" y="129" text-anchor="middle" class="t11" style="font-weight:400">funcional o jerárquico</text>
  <rect x="348" y="100" width="152" height="36" rx="4" fill="#2d8659"/><text x="424" y="115" text-anchor="middle" class="t11">7 · RESOLUCIÓN</text><text x="424" y="129" text-anchor="middle" class="t11" style="font-weight:400">solución o rodeo</text>
  <rect x="512" y="100" width="148" height="36" rx="4" fill="#2d8659"/><text x="586" y="115" text-anchor="middle" class="t11">8 · CIERRE</text><text x="586" y="129" text-anchor="middle" class="t11" style="font-weight:400">confirma el usuario</text>
  <line x1="172" y1="118" x2="181" y2="118" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <line x1="336" y1="118" x2="345" y2="118" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <line x1="500" y1="118" x2="509" y2="118" stroke="#0055a0" stroke-width="2" marker-end="url(#a11)"/>
  <text x="20" y="158" class="k11">ESTADOS Y RELOJ DEL SLA</text>
  <rect x="20" y="166" width="126" height="34" rx="4" fill="#eef3f8"/><text x="83" y="182" text-anchor="middle" class="d11">Nuevo · Asignado</text><text x="83" y="195" text-anchor="middle" class="d11">En curso</text>
  <rect x="152" y="166" width="126" height="34" rx="4" fill="#fdf3e6"/><text x="215" y="182" text-anchor="middle" class="d11">Espera del usuario</text><text x="215" y="195" text-anchor="middle" class="d11">Espera de terceros</text>
  <rect x="284" y="166" width="126" height="34" rx="4" fill="#eaf3ee"/><text x="347" y="182" text-anchor="middle" class="d11">Resuelto</text><text x="347" y="195" text-anchor="middle" class="d11">Cerrado</text>
  <rect x="416" y="166" width="126" height="34" rx="4" fill="#fbeaea"/><text x="479" y="182" text-anchor="middle" class="d11">Reabierto</text><text x="479" y="195" text-anchor="middle" class="d11">(penaliza calidad)</text>
  <rect x="548" y="166" width="112" height="34" rx="4" fill="#0055a0"/><text x="604" y="182" text-anchor="middle" class="t11" style="font-size:9px">EL RELOJ SE</text><text x="604" y="195" text-anchor="middle" class="t11" style="font-size:9px">DETIENE EN NARANJA</text>
  <text x="20" y="226" class="k11">CUATRO FLUJOS DIFERENCIADOS</text>
  <rect x="20" y="234" width="155" height="52" rx="4" fill="#0055a0"/><text x="97" y="252" text-anchor="middle" class="t11">ESTÁNDAR</text><text x="97" y="268" text-anchor="middle" class="t11" style="font-weight:400">la mayoría de casos</text>
  <rect x="182" y="234" width="155" height="52" rx="4" fill="#d13c3c"/><text x="259" y="252" text-anchor="middle" class="t11">INCIDENCIA GRAVE</text><text x="259" y="268" text-anchor="middle" class="t11" style="font-weight:400">responsable designado,</text><text x="259" y="281" text-anchor="middle" class="t11" style="font-weight:400">comunicación y revisión</text>
  <rect x="344" y="234" width="155" height="52" rx="4" fill="#e89822"/><text x="421" y="252" text-anchor="middle" class="t11">SEGURIDAD</text><text x="421" y="268" text-anchor="middle" class="t11" style="font-weight:400">preservar evidencias;</text><text x="421" y="281" text-anchor="middle" class="t11" style="font-weight:400">valorar notificación</text>
  <rect x="506" y="234" width="154" height="52" rx="4" fill="#2d8659"/><text x="583" y="252" text-anchor="middle" class="t11">PETICIÓN</text><text x="583" y="268" text-anchor="middle" class="t11" style="font-weight:400">nada está roto:</text><text x="583" y="281" text-anchor="middle" class="t11" style="font-weight:400">autorización y plazo</text>
  <rect x="90" y="298" width="500" height="24" rx="5" fill="none" stroke="#d13c3c" stroke-width="1.5"/>
  <text x="340" y="314" text-anchor="middle" class="k11">Abusar del estado «en espera» para parar el reloj falsea todos los indicadores</text>
  <text x="670" y="336" text-anchor="end" class="n11">[Fuente: ITIL4; ISO20000]</text>
</svg>
```

---

## D12 · El CAU: canales de entrada y niveles de soporte

**Sección**: §2.2 — El Centro de Atención a Usuarios (CAU)
**Propósito**: Mostrar el CAU como punto único de contacto que recoge todos los canales en un único registro y distribuye el trabajo entre niveles de coste creciente.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="El Centro de Atención a Usuarios como punto único de contacto: seis canales de entrada (teléfono, portal de autoservicio, correo, chat, monitorización automática y presencial) que confluyen en un único registro, y desde ahí la distribución entre los niveles de soporte 0, 1, 2 y 3 y el soporte de campo, con el coste por contacto creciendo de arriba abajo">
  <style>.t12{font:700 10px system-ui,sans-serif;fill:#fff}.s12{font:8.5px system-ui,sans-serif;fill:#fff}.d12{font:9px system-ui,sans-serif;fill:#333}.h12{font:700 13px system-ui,sans-serif;fill:#0055a0}.k12{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n12{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a12" markerWidth="7" markerHeight="7" refX="6" refY="2.5" orient="auto"><path d="M0,0 L6,2.5 L0,5 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h12">Punto único de contacto y niveles de soporte</text>
  <text x="20" y="42" class="k12">CANALES DE ENTRADA (multicanal)</text>
  <rect x="20" y="50" width="102" height="34" rx="4" fill="#0055a0"/><text x="71" y="65" text-anchor="middle" class="t12">Teléfono</text><text x="71" y="78" text-anchor="middle" class="s12">inmediato, caro</text>
  <rect x="130" y="50" width="102" height="34" rx="4" fill="#0055a0"/><text x="181" y="65" text-anchor="middle" class="t12">Portal</text><text x="181" y="78" text-anchor="middle" class="s12">24×7, barato</text>
  <rect x="240" y="50" width="102" height="34" rx="4" fill="#0055a0"/><text x="291" y="65" text-anchor="middle" class="t12">Correo</text><text x="291" y="78" text-anchor="middle" class="s12">desestructurado</text>
  <rect x="350" y="50" width="102" height="34" rx="4" fill="#0055a0"/><text x="401" y="65" text-anchor="middle" class="t12">Chat</text><text x="401" y="78" text-anchor="middle" class="s12">varios a la vez</text>
  <rect x="460" y="50" width="102" height="34" rx="4" fill="#2d8659"/><text x="511" y="65" text-anchor="middle" class="t12">Monitorización</text><text x="511" y="78" text-anchor="middle" class="s12">detecta antes</text>
  <rect x="570" y="50" width="90" height="34" rx="4" fill="#888"/><text x="615" y="65" text-anchor="middle" class="t12">Presencial</text><text x="615" y="78" text-anchor="middle" class="s12">el más caro</text>
  <path d="M71,84 L71,96 L609,96 L609,84" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <line x1="340" y1="96" x2="340" y2="108" stroke="#0055a0" stroke-width="2" marker-end="url(#a12)"/>
  <rect x="150" y="112" width="380" height="34" rx="5" fill="#e89822"/>
  <text x="340" y="127" text-anchor="middle" class="t12">UN ÚNICO REGISTRO · UNA ÚNICA HERRAMIENTA</text>
  <text x="340" y="140" text-anchor="middle" class="s12">la multicanalidad está en la ENTRADA, nunca en el registro</text>
  <line x1="340" y1="146" x2="340" y2="160" stroke="#0055a0" stroke-width="2" marker-end="url(#a12)"/>
  <text x="20" y="176" class="k12">NIVELES DE SOPORTE · el coste por contacto crece hacia abajo</text>
  <rect x="140" y="184" width="400" height="26" rx="4" fill="#2d8659"/><text x="340" y="202" text-anchor="middle" class="t12">N0 · AUTOSERVICIO: portal, contraseña, catálogo · coste casi nulo</text>
  <rect x="120" y="216" width="440" height="26" rx="4" fill="#0055a0"/><text x="340" y="234" text-anchor="middle" class="t12">N1 · CAU: casos frecuentes, guiones, ASISTENCIA REMOTA · objetivo FCR</text>
  <rect x="100" y="248" width="480" height="26" rx="4" fill="#0055a0"/><text x="340" y="266" text-anchor="middle" class="t12">N2 · ESPECIALISTAS: puesto, red, sistemas, aplicaciones, bases de datos</text>
  <rect x="80" y="280" width="520" height="26" rx="4" fill="#e89822"/><text x="340" y="298" text-anchor="middle" class="t12">N3 · EXPERTOS, DESARROLLO, FABRICANTE O PROVEEDOR (contrato UC)</text>
  <rect x="60" y="312" width="560" height="26" rx="4" fill="#d13c3c"/><text x="340" y="330" text-anchor="middle" class="t12">SOPORTE DE CAMPO: todo lo físico · coste dominado por el desplazamiento</text>
  <text x="670" y="354" text-anchor="end" class="n12">[Fuente: ITIL4; ISO20000]</text>
</svg>
```

---

## D13 · Matriz impacto × urgencia y tiempos comprometidos

**Sección**: §2.3.1 — Priorización, impacto y urgencia · §2.3.4 — SLA
**Propósito**: Unir en una imagen el cálculo de la prioridad y sus consecuencias contractuales: tiempo de respuesta, tiempo de resolución y escalado automático.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 370" role="img" aria-label="Matriz de prioridad de tres por tres que cruza impacto alto medio y bajo con urgencia alta media y baja, produciendo prioridades de la 1 crítica a la 5 muy baja, acompañada de una tabla con los tiempos de respuesta, de resolución y de escalado automático asociados a cada prioridad, y de la advertencia de que la prioridad no la decide el usuario">
  <style>.t13{font:700 10.5px system-ui,sans-serif;fill:#fff}.d13{font:9px system-ui,sans-serif;fill:#333}.h13{font:700 13px system-ui,sans-serif;fill:#0055a0}.k13{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.p13{font:700 12px system-ui,sans-serif;fill:#fff}.n13{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <text x="340" y="20" text-anchor="middle" class="h13">Prioridad = Impacto × Urgencia</text>
  <text x="20" y="42" class="k13">MATRIZ 3 × 3</text>
  <text x="112" y="60" text-anchor="middle" class="k13">URGENCIA ALTA</text>
  <text x="232" y="60" text-anchor="middle" class="k13">URGENCIA MEDIA</text>
  <text x="352" y="60" text-anchor="middle" class="k13">URGENCIA BAJA</text>
  <text x="20" y="88" class="k13">IMPACTO</text><text x="20" y="100" class="k13">ALTO</text>
  <rect x="70" y="68" width="112" height="40" rx="4" fill="#d13c3c"/><text x="126" y="93" text-anchor="middle" class="p13">1 · CRÍTICA</text>
  <rect x="188" y="68" width="112" height="40" rx="4" fill="#e89822"/><text x="244" y="93" text-anchor="middle" class="p13">2 · ALTA</text>
  <rect x="306" y="68" width="112" height="40" rx="4" fill="#0055a0"/><text x="362" y="93" text-anchor="middle" class="p13">3 · MEDIA</text>
  <text x="20" y="132" class="k13">IMPACTO</text><text x="20" y="144" class="k13">MEDIO</text>
  <rect x="70" y="112" width="112" height="40" rx="4" fill="#e89822"/><text x="126" y="137" text-anchor="middle" class="p13">2 · ALTA</text>
  <rect x="188" y="112" width="112" height="40" rx="4" fill="#0055a0"/><text x="244" y="137" text-anchor="middle" class="p13">3 · MEDIA</text>
  <rect x="306" y="112" width="112" height="40" rx="4" fill="#2d8659"/><text x="362" y="137" text-anchor="middle" class="p13">4 · BAJA</text>
  <text x="20" y="176" class="k13">IMPACTO</text><text x="20" y="188" class="k13">BAJO</text>
  <rect x="70" y="156" width="112" height="40" rx="4" fill="#0055a0"/><text x="126" y="181" text-anchor="middle" class="p13">3 · MEDIA</text>
  <rect x="188" y="156" width="112" height="40" rx="4" fill="#2d8659"/><text x="244" y="181" text-anchor="middle" class="p13">4 · BAJA</text>
  <rect x="306" y="156" width="112" height="40" rx="4" fill="#888"/><text x="362" y="181" text-anchor="middle" class="p13">5 · MUY BAJA</text>
  <rect x="436" y="68" width="224" height="128" rx="5" fill="#eef3f8"/>
  <text x="548" y="88" text-anchor="middle" class="k13">LOS DOS EJES SON INDEPENDIENTES</text>
  <text x="448" y="110" class="d13">IMPACTO: ¿a cuánto afecta?</text>
  <text x="448" y="126" class="d13">usuarios, criticidad, riesgo legal</text>
  <text x="448" y="150" class="d13">URGENCIA: ¿cuánto puede esperar?</text>
  <text x="448" y="166" class="d13">rapidez del daño, rodeo, plazo</text>
  <text x="448" y="188" class="d13">Impacto alto ≠ prioridad crítica</text>
  <text x="20" y="222" class="k13">TIEMPOS COMPROMETIDOS (valores ilustrativos: se pactan en cada SLA)</text>
  <rect x="20" y="230" width="140" height="20" rx="3" fill="#0055a0"/><text x="90" y="244" text-anchor="middle" class="t13">PRIORIDAD</text>
  <rect x="164" y="230" width="140" height="20" rx="3" fill="#0055a0"/><text x="234" y="244" text-anchor="middle" class="t13">RESPUESTA</text>
  <rect x="308" y="230" width="160" height="20" rx="3" fill="#0055a0"/><text x="388" y="244" text-anchor="middle" class="t13">RESOLUCIÓN</text>
  <rect x="472" y="230" width="188" height="20" rx="3" fill="#0055a0"/><text x="566" y="244" text-anchor="middle" class="t13">ESCALADO AUTOMÁTICO</text>
  <rect x="20" y="254" width="640" height="20" rx="3" fill="#fbeaea"/>
  <text x="30" y="268" class="d13">1 · Crítica</text><text x="174" y="268" class="d13">15 minutos</text><text x="318" y="268" class="d13">4 horas</text><text x="482" y="268" class="d13">N2 a los 30 min; jerárquico a la hora</text>
  <rect x="20" y="278" width="640" height="20" rx="3" fill="#fdf3e6"/>
  <text x="30" y="292" class="d13">2 · Alta</text><text x="174" y="292" class="d13">1 hora</text><text x="318" y="292" class="d13">8 horas laborables</text><text x="482" y="292" class="d13">N2 a las 2 h; jerárquico a las 6 h</text>
  <rect x="20" y="302" width="640" height="20" rx="3" fill="#eef3f8"/>
  <text x="30" y="316" class="d13">3 · Media</text><text x="174" y="316" class="d13">4 horas</text><text x="318" y="316" class="d13">2 días laborables</text><text x="482" y="316" class="d13">N2 al día; jerárquico al segundo día</text>
  <rect x="20" y="326" width="640" height="20" rx="3" fill="#eaf3ee"/>
  <text x="30" y="340" class="d13">4 · Baja</text><text x="174" y="340" class="d13">1 día laborable</text><text x="318" y="340" class="d13">5 días laborables</text><text x="482" y="340" class="d13">N2 a los 3 días</text>
  <rect x="120" y="350" width="440" height="18" rx="4" fill="#d13c3c"/>
  <text x="340" y="363" text-anchor="middle" class="t13">La prioridad NO la decide el usuario: se aplican criterios objetivos escritos</text>
</svg>
```

---

## D14 · Escalado funcional frente a escalado jerárquico

**Sección**: §2.3.2 — Diagnóstico, escalado funcional y jerárquico
**Propósito**: Separar visualmente los dos ejes del escalado, que es una de las confusiones más frecuentes.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Los dos ejes del escalado: el escalado funcional u horizontal, que traslada la incidencia a grupos con mayor conocimiento técnico del nivel 1 al nivel 3 y al proveedor, y el escalado jerárquico o vertical, que informa a niveles de autoridad superiores para decidir, autorizar o aportar recursos, con la indicación de que pueden coexistir y de que la propiedad del tique nunca se transfiere">
  <style>.t14{font:700 10px system-ui,sans-serif;fill:#fff}.s14{font:9px system-ui,sans-serif;fill:#fff}.d14{font:9px system-ui,sans-serif;fill:#333}.h14{font:700 13px system-ui,sans-serif;fill:#0055a0}.k14{font:700 10px system-ui,sans-serif;fill:#0055a0}.n14{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a14" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker><marker id="b14" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#d13c3c"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h14">Dos escalados que no se confunden</text>
  <text x="200" y="44" text-anchor="middle" class="k14">FUNCIONAL (horizontal) → busca QUIEN SEPA</text>
  <rect x="30" y="54" width="120" height="42" rx="5" fill="#0055a0"/><text x="90" y="72" text-anchor="middle" class="t14">NIVEL 1</text><text x="90" y="87" text-anchor="middle" class="s14">CAU generalista</text>
  <rect x="170" y="54" width="120" height="42" rx="5" fill="#0055a0"/><text x="230" y="72" text-anchor="middle" class="t14">NIVEL 2</text><text x="230" y="87" text-anchor="middle" class="s14">especialistas</text>
  <rect x="310" y="54" width="120" height="42" rx="5" fill="#0055a0"/><text x="370" y="72" text-anchor="middle" class="t14">NIVEL 3</text><text x="370" y="87" text-anchor="middle" class="s14">expertos</text>
  <rect x="450" y="54" width="120" height="42" rx="5" fill="#888"/><text x="510" y="72" text-anchor="middle" class="t14">PROVEEDOR</text><text x="510" y="87" text-anchor="middle" class="s14">contrato UC</text>
  <line x1="150" y1="75" x2="166" y2="75" stroke="#0055a0" stroke-width="2.5" marker-end="url(#a14)"/>
  <line x1="290" y1="75" x2="306" y2="75" stroke="#0055a0" stroke-width="2.5" marker-end="url(#a14)"/>
  <line x1="430" y1="75" x2="446" y2="75" stroke="#0055a0" stroke-width="2.5" marker-end="url(#a14)"/>
  <text x="30" y="116" class="d14">Motivo: NO SÉ o NO PUEDO resolverlo. Aporta conocimiento técnico y permisos. No aporta autoridad.</text>
  <line x1="20" y1="128" x2="660" y2="128" stroke="#ddd" stroke-width="1"/>
  <text x="200" y="150" text-anchor="middle" class="k14">JERÁRQUICO (vertical) → busca QUIEN DECIDA</text>
  <rect x="30" y="244" width="180" height="30" rx="5" fill="#0055a0"/><text x="120" y="264" text-anchor="middle" class="t14">TÉCNICO DEL CAU</text>
  <rect x="30" y="200" width="180" height="30" rx="5" fill="#e89822"/><text x="120" y="220" text-anchor="middle" class="t14">RESPONSABLE DEL CAU</text>
  <rect x="30" y="156" width="180" height="30" rx="5" fill="#d13c3c"/><text x="120" y="176" text-anchor="middle" class="t14">DIRECCIÓN / JEFATURA</text>
  <line x1="120" y1="243" x2="120" y2="232" stroke="#d13c3c" stroke-width="2.5" marker-end="url(#b14)"/>
  <line x1="120" y1="199" x2="120" y2="188" stroke="#d13c3c" stroke-width="2.5" marker-end="url(#b14)"/>
  <rect x="230" y="156" width="430" height="118" rx="5" fill="#fbeaea"/>
  <text x="245" y="176" class="k14">CUÁNDO SE ESCALA JERÁRQUICAMENTE</text>
  <text x="245" y="196" class="d14">· Se van a incumplir los plazos comprometidos en el SLA</text>
  <text x="245" y="214" class="d14">· Hace falta AUTORIZAR una parada, un gasto o una excepción</text>
  <text x="245" y="232" class="d14">· El impacto es institucional y exige comunicación a la dirección</text>
  <text x="245" y="250" class="d14">· Hay conflicto de prioridades entre áreas y alguien debe arbitrar</text>
  <text x="245" y="268" class="d14">· Se activa el procedimiento de incidencia grave</text>
  <rect x="20" y="286" width="315" height="26" rx="5" fill="#2d8659"/>
  <text x="177" y="304" text-anchor="middle" class="t14">Pueden coexistir en la misma incidencia</text>
  <rect x="345" y="286" width="315" height="26" rx="5" fill="#0055a0"/>
  <text x="502" y="304" text-anchor="middle" class="t14">La PROPIEDAD del tique nunca se transfiere</text>
</svg>
```

---

## D15 · Incidencia, problema, error conocido, petición y evento

**Sección**: §2.4.1 — Diferencias entre incidencia, problema y petición
**Propósito**: Fijar de una vez las cinco definiciones que más se confunden, con el criterio que las separa y un ejemplo de cada una.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Los cinco objetos de la gestión de servicios: incidencia como interrupción no planificada, problema como causa de una o varias incidencias, error conocido como problema ya analizado con rodeo documentado, petición de servicio como solicitud prevista en la que nada está roto, y evento como cambio de estado significativo con sus tres tipos informativo, advertencia y excepción">
  <style>.t15{font:700 10.5px system-ui,sans-serif;fill:#fff}.s15{font:9px system-ui,sans-serif;fill:#fff}.d15{font:9px system-ui,sans-serif;fill:#333}.h15{font:700 13px system-ui,sans-serif;fill:#0055a0}.k15{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n15{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a15" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h15">Cinco objetos que no deben confundirse</text>
  <rect x="20" y="34" width="200" height="60" rx="5" fill="#d13c3c"/>
  <text x="120" y="52" text-anchor="middle" class="t15">INCIDENCIA</text>
  <text x="120" y="68" text-anchor="middle" class="s15">Interrupción NO planificada</text>
  <text x="120" y="83" text-anchor="middle" class="s15">Objetivo: RESTABLECER</text>
  <rect x="240" y="34" width="200" height="60" rx="5" fill="#e89822"/>
  <text x="340" y="52" text-anchor="middle" class="t15">PROBLEMA</text>
  <text x="340" y="68" text-anchor="middle" class="s15">CAUSA de una o varias</text>
  <text x="340" y="83" text-anchor="middle" class="s15">Objetivo: CAUSA RAÍZ</text>
  <rect x="460" y="34" width="200" height="60" rx="5" fill="#2d8659"/>
  <text x="560" y="52" text-anchor="middle" class="t15">ERROR CONOCIDO</text>
  <text x="560" y="68" text-anchor="middle" class="s15">Problema YA analizado</text>
  <text x="560" y="83" text-anchor="middle" class="s15">con rodeo documentado</text>
  <line x1="220" y1="64" x2="236" y2="64" stroke="#0055a0" stroke-width="2" marker-end="url(#a15)"/>
  <line x1="440" y1="64" x2="456" y2="64" stroke="#0055a0" stroke-width="2" marker-end="url(#a15)"/>
  <path d="M560,94 L560,112 L120,112 L120,98" fill="none" stroke="#2d8659" stroke-width="2" marker-end="url(#a15)"/>
  <text x="340" y="109" text-anchor="middle" class="n15">la KEDB devuelve el rodeo al primer nivel: la siguiente incidencia se resuelve en minutos</text>
  <rect x="20" y="124" width="320" height="60" rx="5" fill="#0055a0"/>
  <text x="180" y="142" text-anchor="middle" class="t15">PETICIÓN DE SERVICIO</text>
  <text x="180" y="158" text-anchor="middle" class="s15">Solicitud prevista y acordada · NADA ESTÁ ROTO</text>
  <text x="180" y="174" text-anchor="middle" class="s15">Suele exigir autorización previa · se mide por plazo</text>
  <rect x="360" y="124" width="300" height="60" rx="5" fill="#888"/>
  <text x="510" y="142" text-anchor="middle" class="t15">EVENTO</text>
  <text x="510" y="158" text-anchor="middle" class="s15">Cambio de estado significativo</text>
  <text x="510" y="174" text-anchor="middle" class="s15">detectado por la monitorización</text>
  <text x="20" y="204" class="k15">LOS TRES TIPOS DE EVENTO</text>
  <rect x="20" y="212" width="205" height="46" rx="4" fill="#eef3f8"/>
  <text x="122" y="230" text-anchor="middle" class="k15">INFORMATIVO</text>
  <text x="122" y="248" text-anchor="middle" class="d15">Ocurrió lo previsto: no hay acción</text>
  <rect x="237" y="212" width="205" height="46" rx="4" fill="#fdf3e6"/>
  <text x="339" y="230" text-anchor="middle" class="k15">ADVERTENCIA</text>
  <text x="339" y="248" text-anchor="middle" class="d15">Se acerca a un umbral: ACTUAR ANTES</text>
  <rect x="454" y="212" width="206" height="46" rx="4" fill="#fbeaea"/>
  <text x="557" y="230" text-anchor="middle" class="k15">EXCEPCIÓN</text>
  <text x="557" y="248" text-anchor="middle" class="d15">Se superó el umbral: genera incidencia</text>
  <text x="20" y="278" class="k15">EJEMPLOS EN UNA MISMA IMPRESORA</text>
  <rect x="20" y="286" width="155" height="36" rx="4" fill="#f5f5f5"/><text x="97" y="302" text-anchor="middle" class="d15">Incidencia: no imprime</text><text x="97" y="316" text-anchor="middle" class="d15">y hay gente esperando</text>
  <rect x="182" y="286" width="155" height="36" rx="4" fill="#f5f5f5"/><text x="259" y="302" text-anchor="middle" class="d15">Problema: el controlador</text><text x="259" y="316" text-anchor="middle" class="d15">falla tras el último parche</text>
  <rect x="344" y="286" width="155" height="36" rx="4" fill="#f5f5f5"/><text x="421" y="302" text-anchor="middle" class="d15">Petición: instalar esa</text><text x="421" y="316" text-anchor="middle" class="d15">impresora a un usuario</text>
  <rect x="506" y="286" width="154" height="36" rx="4" fill="#f5f5f5"/><text x="583" y="302" text-anchor="middle" class="d15">Evento: la cola supera</text><text x="583" y="316" text-anchor="middle" class="d15">los 200 trabajos</text>
  <text x="670" y="336" text-anchor="end" class="n15">[Fuente: ITIL4; ISO20000]</text>
</svg>
```

---

## D16 · El círculo completo: seguridad, medición y mejora continua

**Sección**: §3 — Marco normativo, seguridad y calidad en la Administración Pública
**Propósito**: Cerrar el tema mostrando cómo la asistencia remota, la gestión de incidencias, el marco normativo y los indicadores forman un único ciclo que se realimenta.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 366" role="img" aria-label="El ciclo completo del servicio: la asistencia remota y la gestión de incidencias sometidas a los controles del Esquema Nacional de Seguridad y del RGPD, medidas mediante indicadores clave de rendimiento, y realimentadas por la gestión del conocimiento, la gestión de problemas, la satisfacción de los usuarios y las auditorías, con las cinco dimensiones de seguridad y las categorías del sistema">
  <style>.t16{font:700 10.5px system-ui,sans-serif;fill:#fff}.s16{font:9px system-ui,sans-serif;fill:#fff}.d16{font:9px system-ui,sans-serif;fill:#333}.h16{font:700 13px system-ui,sans-serif;fill:#0055a0}.k16{font:700 9.5px system-ui,sans-serif;fill:#0055a0}.n16{font:8.5px system-ui,sans-serif;fill:#666}</style>
  <defs><marker id="a16" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker></defs>
  <text x="340" y="20" text-anchor="middle" class="h16">El marco normativo envuelve toda la operación</text>
  <rect x="20" y="32" width="640" height="56" rx="5" fill="#d13c3c"/>
  <text x="340" y="50" text-anchor="middle" class="t16">ENS · RD 311/2022 · cinco dimensiones de seguridad</text>
  <text x="340" y="67" text-anchor="middle" class="s16">DISPONIBILIDAD · AUTENTICIDAD · INTEGRIDAD · CONFIDENCIALIDAD · TRAZABILIDAD</text>
  <text x="340" y="82" text-anchor="middle" class="s16">Categoría del sistema: BÁSICA · MEDIA · ALTA (la fija el nivel más alto de cualquier dimensión)</text>
  <rect x="20" y="94" width="315" height="46" rx="5" fill="#e89822"/>
  <text x="177" y="112" text-anchor="middle" class="t16">RGPD y LOPDGDD</text>
  <text x="177" y="129" text-anchor="middle" class="s16">minimización · finalidad · encargado · brecha en 72 h</text>
  <rect x="345" y="94" width="315" height="46" rx="5" fill="#888"/>
  <text x="502" y="112" text-anchor="middle" class="t16">MÍNIMO PRIVILEGIO Y TRAZABILIDAD</text>
  <text x="502" y="129" text-anchor="middle" class="s16">RBAC · alcance · elevación temporal · registro por tique</text>
  <rect x="20" y="152" width="205" height="60" rx="5" fill="#0055a0"/>
  <text x="122" y="172" text-anchor="middle" class="t16">ASISTENCIA REMOTA</text>
  <text x="122" y="189" text-anchor="middle" class="s16">consentimiento, canal cifrado</text>
  <text x="122" y="204" text-anchor="middle" class="s16">y modo mínimo suficiente</text>
  <rect x="237" y="152" width="205" height="60" rx="5" fill="#0055a0"/>
  <text x="339" y="172" text-anchor="middle" class="t16">GESTIÓN DE INCIDENCIAS</text>
  <text x="339" y="189" text-anchor="middle" class="s16">registrar, priorizar, escalar,</text>
  <text x="339" y="204" text-anchor="middle" class="s16">resolver y cerrar</text>
  <rect x="454" y="152" width="206" height="60" rx="5" fill="#2d8659"/>
  <text x="557" y="172" text-anchor="middle" class="t16">MEDICIÓN (KPI)</text>
  <text x="557" y="189" text-anchor="middle" class="s16">FCR · MTTR · ASA · SLA</text>
  <text x="557" y="204" text-anchor="middle" class="s16">reapertura · CSAT · backlog</text>
  <line x1="225" y1="182" x2="234" y2="182" stroke="#0055a0" stroke-width="2" marker-end="url(#a16)"/>
  <line x1="442" y1="182" x2="451" y2="182" stroke="#0055a0" stroke-width="2" marker-end="url(#a16)"/>
  <text x="20" y="234" class="k16">CUATRO FUENTES DE MEJORA QUE REALIMENTAN EL CICLO</text>
  <rect x="20" y="242" width="155" height="56" rx="4" fill="#eef3f8"/>
  <text x="97" y="260" text-anchor="middle" class="k16">INDICADORES</text>
  <text x="97" y="277" text-anchor="middle" class="d16">señalan dónde duele</text>
  <text x="97" y="291" text-anchor="middle" class="d16">y hay que segmentar</text>
  <rect x="182" y="242" width="155" height="56" rx="4" fill="#eaf3ee"/>
  <text x="259" y="260" text-anchor="middle" class="k16">PROBLEMAS</text>
  <text x="259" y="277" text-anchor="middle" class="d16">eliminan familias</text>
  <text x="259" y="291" text-anchor="middle" class="d16">enteras de incidencias</text>
  <rect x="344" y="242" width="155" height="56" rx="4" fill="#fdf3e6"/>
  <text x="421" y="260" text-anchor="middle" class="k16">USUARIOS</text>
  <text x="421" y="277" text-anchor="middle" class="d16">satisfacción y quejas:</text>
  <text x="421" y="291" text-anchor="middle" class="d16">lo que no capta el dato</text>
  <rect x="506" y="242" width="154" height="56" rx="4" fill="#fbeaea"/>
  <text x="583" y="260" text-anchor="middle" class="k16">AUDITORÍAS</text>
  <text x="583" y="277" text-anchor="middle" class="d16">detectan lo que la</text>
  <text x="583" y="291" text-anchor="middle" class="d16">operación normaliza</text>
  <path d="M97,298 L97,314 L583,314 L583,298" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <line x1="340" y1="314" x2="340" y2="322" stroke="#0055a0" stroke-width="2" marker-end="url(#a16)"/>
  <rect x="140" y="326" width="400" height="24" rx="5" fill="#0055a0"/>
  <text x="340" y="342" text-anchor="middle" class="t16">MEJORA CONTINUA · planificar, hacer, verificar, actuar</text>
  <text x="670" y="362" text-anchor="end" class="n16">[Fuente: ENS; RGPD; ITIL4; ISO20000]</text>
</svg>
```
