# VALL PALA · Plan de ejecución

## 2. Recursos y logística por fase

El plan sigue los tres sprints de la planificación del proyecto. El Sprint 3 incluye el cierre automático del MVP (HU18) y las tareas de Fase 2 previstas en el tablero: pago online (HU19) y valoración del nivel (HU20). Los proveedores y las herramientas concretas que el equipo todavía no ha acordado se indican como propuestas o pendientes.

| Fase o actividad | Recursos materiales e infraestructura | Software y datos | Cuentas o servicios | Logística y momento de preparación |
|---|---|---|---|---|
| **Sprint 1 · Desarrollo local, tarea 1.01** | Un ordenador por integrante y conexión a Internet. | Git, editor de código y entorno de ejecución del proyecto. Archivo `.env.example` con las variables necesarias y sin valores secretos. | Cuenta individual de GitHub, acceso al repositorio y a GitHub Projects. | Al iniciar el sprint, cada integrante clona el repositorio y comprueba que puede arrancar la aplicación y acceder al tablero. Documentar las versiones y los comandos de instalación. |
| **Sprint 1 · Base de datos, tareas 1.02 y 1.03** | Base de datos local por integrante. | Motor acordado por el equipo, cliente SQL y scripts de creación o migración. Datos iniciales para seis pistas de dobles, una individual, horarios, tarifas y usuarios ficticios de prueba. | Credenciales locales de base de datos. | Versionar el esquema y los datos de prueba. Mantener el mismo motor y versión principal en desarrollo, pruebas y producción. |
| **Sprint 1 · Diseño y web pública, tareas 1.09 y 1.10** | Navegadores de escritorio y un móvil o emulador. | Figma o bocetos compartidos. Logotipo, fotografías autorizadas, dirección, horarios y tarifas facilitados por el club. | Acceso a la herramienta de diseño si se utiliza. | Recopilar el material del club antes de montar la página. Comprobar la navegación y el diseño en móvil y escritorio. |
| **Sprint 1 · Servidor de pruebas, tareas 1.17 y 1.18** | Entorno de alojamiento de pruebas con base de datos propia. | Aplicación desplegada, migraciones, datos ficticios y variables del entorno. | Acceso del equipo al alojamiento y a la URL de pruebas. | Prepararlo antes de probar los flujos de acceso y perfil. Usar credenciales distintas de las de producción. |
| **Sprint 2 · Reservas, administración y partidas abiertas** | Equipos locales, servidor de pruebas y dos sesiones de navegador para probar concurrencia. | Cuentas ficticias de administrador, socio y cliente. Pistas, reservas y partidas de prueba. Cliente HTTP o herramientas del navegador para revisar la API y pruebas automatizadas para sus reglas. | Acceso al entorno de pruebas. GitHub Actions si se adopta para ejecutar las comprobaciones. | Probar el límite de 14 días, las dobles reservas, los permisos del panel y la última plaza de una partida. Confirmar manualmente pagos presenciales con una cuenta de administrador de pruebas. |
| **Sprint 3 · Cierre automático, tareas 3.01 y 3.11** | Alojamiento con programador de tareas, como cron o un servicio equivalente. | Comando de cierre, registros de ejecución y partidas ficticias completas e incompletas con horas de inicio controladas. | Permiso para configurar y consultar la tarea programada. | Activar primero en pruebas. Verificar el cierre tres horas antes, la liberación de pista y que una ejecución repetida conserva el estado correcto. Replicar la configuración en producción. |
| **Sprint 3 · Pago online, HU19** | Entorno de pruebas accesible por HTTPS para recibir el webhook del proveedor. | Integración con el proveedor, tabla de pagos, credenciales de sandbox y medios de pago de prueba. | Cuenta de pruebas en la pasarela elegida. Cuenta comercial y credenciales de producción si se activa el cobro real. | Preparar el sandbox antes de la tarea 3.04. Probar pagos confirmados y fallidos y notificaciones repetidas. Validar la confirmación del proveedor antes de actualizar el estado del pago. |
| **Sprint 3 · Valoración del nivel, HU20** | Equipos locales y entorno de pruebas. | Base de datos de resultados, historial de valoraciones y datos ficticios con rachas de tres victorias y tres derrotas. | Acceso al entorno de pruebas. | Cargar casos de prueba para comprobar los ajustes de +0,1 y −0,1 y su visualización en el historial. |
| **Sprint 3 · Producción y entrega, tareas 3.14 a 3.16** | Alojamiento de producción, base de datos independiente y espacio para copias de seguridad. | Aplicación, migraciones, HTTPS, registros de errores y documentación de despliegue. | Cuenta de alojamiento, acceso al DNS del dominio o subdominio acordado y credenciales de los servicios activados. | Preparar el dominio y los accesos antes del despliegue. Tras las pruebas de regresión, configurar DNS y HTTPS, aplicar las migraciones y comprobar el acceso, las reservas, el panel y el cierre automático. Verificar el pago online si se activa. |

### Infraestructura y despliegue propuestos

Para este trabajo teórico, VALL PALA utilizará un **VPS L+ de IONOS con Linux y Docker Compose**, en una ubicación de la Unión Europea que se seleccionará al contratar. El VPS alojará pruebas y producción en proyectos de Compose independientes, con sus propias redes, credenciales y volúmenes. Ambos comparten el servidor y una incidencia del VPS afectaría a los dos.

| Concepto | Oferta de referencia aportada el 23/11/2026 |
|---|---|
| Recursos | 4 vCPU, 8 GB de RAM y 240 GB de almacenamiento NVMe |
| Cuota mensual | 22 € sin IVA |
| Alta | 10 € sin IVA, pago único |
| Primer mes con alta | 32 € sin IVA |
| Primer año con alta | 274 € sin IVA, si se mantiene la cuota durante 12 meses |

La capacidad se considera adecuada como punto de partida para el MVP, con la aplicación, la base de datos, el proxy y la tarea programada. En una implantación real, se comprobaría el consumo de los dos entornos durante las pruebas. El presupuesto del VPS se calcula a partir de la captura aportada. El dominio y el almacenamiento externo de copias se presupuestan aparte.

| Elemento | Propuesta para VALL PALA | Cuándo se prepara |
|---|---|---|
| Hosting y servidor | VPS L+ de IONOS con Linux y acceso administrativo. Comprobar el consumo de CPU, RAM y disco durante las pruebas. | Sprint 1 para pruebas. Confirmar capacidad y alojamiento de producción antes del Sprint 3. |
| Desarrollo local | Ejecutar la aplicación y su base de datos mediante Docker Compose. El repositorio incluirá `Dockerfile`, `compose.yaml` y `.env.example`. En macOS, usar un entorno compatible con Docker, como Docker Desktop. | Sprint 1. |
| Servidor de pruebas | Desplegar un proyecto de Compose con variables, red, credenciales, base de datos y volúmenes propios. Cargar datos ficticios y usar el sandbox de pagos. | Sprint 1 para el entorno básico. Sprints 2 y 3 para las integraciones. |
| Servidor de producción | Desplegar la misma versión de la imagen validada en pruebas, con configuración y secretos de producción. Si comparte VPS con pruebas, usar proyectos y volúmenes independientes y límites de recursos. | Sprint 3. |
| Dominio y DNS | Usar el dominio del club si está disponible y se tiene acceso al DNS. Reservar un subdominio como `pruebas.<dominio>` y el dominio principal o `reservas.<dominio>` para producción. Crear registros A o AAAA según las direcciones del servidor. | Acordar el nombre y los accesos en Sprint 1. Activar cada dirección cuando su entorno esté listo. |
| Proxy inverso y HTTPS | Usar un proxy como Caddy o Nginx para dirigir cada nombre al entorno correspondiente. Configurar certificados TLS y su renovación. Publicar la web mediante el proxy y mantener la base de datos en la red interna de Docker. | HTTPS en pruebas antes de integrar el webhook de pagos. HTTPS en producción antes de publicar. |
| Base de datos y copias | Ejecutar el motor acordado en un contenedor con volumen persistente por entorno. Programar copias fuera del VPS y probar la restauración. Guardar aparte los archivos subidos si la aplicación admite cargas. | Persistencia desde Sprint 1. Verificar copia y restauración antes de producción. |
| Cierre automático de partidas | Ejecutar el proceso mediante un servicio dedicado de Compose o un temporizador del servidor. Configurarlo para que se reinicie tras una caída y revisar sus registros. | Sprint 3. Validar primero en pruebas. |
| Accesos y mantenimiento | Designar una persona responsable del VPS, el DNS, las renovaciones y las copias. Usar acceso SSH con claves y guardar los secretos fuera del repositorio. | Desde la preparación de cada entorno. |
| Costes | Presupuestar el VPS mensual, el dominio anual si hace falta registrarlo y el almacenamiento externo de copias. Añadir las comisiones de la pasarela cuando se habiliten pagos reales. | Antes de contratar o activar servicios. |

### Protección de datos

En la implantación prevista, el club será el responsable del tratamiento y formalizará con IONOS el contrato de encargo para el alojamiento conforme al artículo 28 del RGPD. IONOS ofrece este contrato para sus VPS. Se documentará la ubicación del servidor y de las copias. El entorno de pruebas usará datos ficticios. En producción, el club aplicará las medidas de seguridad que correspondan al riesgo, entre ellas HTTPS, acceso restringido y copias con restauración verificada, y definirá los plazos de conservación de los datos.

- [Contrato de tratamiento de datos de IONOS](https://www.ionos.es/ayuda/proteccion-de-datos/informacion-general-sobre-el-rgpd/contrato-de-tratamiento-de-datos/)
- [RGPD, artículos 28 y 32](https://eur-lex.europa.eu/eli/reg/2016/679/oj?locale=es)

### Datos que debe confirmar el equipo

- Motor y versión de la base de datos, así como tecnologías y versiones del proyecto.
- Ubicación concreta del VPS y de las copias, dominio o subdominio y persona encargada de sus accesos.
- Pasarela de pago elegida y alcance de la entrega de HU19, con sandbox o cobro real habilitado.
