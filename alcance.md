# VALL PALA — Definición del alcance (MoSCoW)

**Proyecto:** Plataforma web de gestión de pistas, reservas y partidas de pádel  
**Cliente:** VALL PALA  
**Ubicación:** La Vall d'Uixó (Castellón)  
**Asignatura:** Proyecto Intermodular · 2.º DAW · Curso 2026/2027  
**Estado:** Propuesta académica inicial, pendiente de validación con el propietario.

## 1. Objetivo del documento

Este documento delimita las funcionalidades previstas para la plataforma web de VALL PALA y las clasifica mediante el método **MoSCoW**. La priorización distingue las funciones imprescindibles, las importantes, las deseables y las que quedan fuera de las entregas actuales.

El proyecto se plantea en dos entregas: una **Fase 1 (MVP)** y una **Fase 2** de ampliación. Que una funcionalidad sea *Must Have* significa que forma parte del alcance previsto del proyecto, pero no implica necesariamente que se implemente en el MVP.

## 2. Contexto y alcance general

VALL PALA dispone de siete pistas exteriores: seis pistas de dobles y una pista individual. Actualmente, las reservas se solicitan por WhatsApp y el administrador las registra en Excel. La propuesta consiste en centralizar la información, la disponibilidad, las reservas y la gestión de usuarios en una aplicación web responsive.

La plataforma contemplará:

- Información pública del club, sus instalaciones, ubicación, horarios y tarifas.
- Registro, inicio de sesión, recuperación de acceso y gestión del perfil.
- Un único rol de cliente. La condición de socio o no socio será un atributo de la cuenta y determinará la tarifa aplicable.
- Consulta de disponibilidad y realización de reservas para las pistas.
- Un panel privado para que el administrador gestione pistas, horarios, tarifas, usuarios y reservas.
- Partidas abiertas para publicar encuentros, buscar plazas e inscribirse.
- Una evolución posterior con pagos online dentro de la plataforma y valoración dinámica del nivel de los jugadores.

## 3. Priorización MoSCoW

### 3.1. MUST HAVE — Imprescindible

Funcionalidades necesarias para que el proyecto cumpla sus objetivos. Se indica en qué fase se prevé cada una.

**Fase 1 — MVP**

- **Web informativa responsive:** mostrar la información de VALL PALA, las instalaciones, la ubicación, los horarios y las tarifas, adaptándose a móvil, tablet y ordenador.
- **Registro y acceso:** permitir el registro, el inicio de sesión y la recuperación del acceso de los usuarios.
- **Perfil y condición de socio:** gestionar un único rol de cliente y distinguir si su cuenta tiene una condición de socio vigente o no socio. Aplicar automáticamente la tarifa correspondiente.
- **Calendario y disponibilidad:** consultar las pistas disponibles por fecha y franja horaria.
- **Reservas online:** permitir que los clientes realicen y consulten sus reservas. La reserva solo podrá hacerse con un máximo de **14 días (dos semanas) de antelación**.
- **Panel de administración:** permitir al administrador gestionar pistas, horarios, tarifas, usuarios y reservas; también crear, modificar y cancelar reservas.
- **Partidas abiertas:** permitir publicar partidas, buscar encuentros e inscribirse individualmente desde el MVP.
- **Cierre de partidas abiertas:** cerrar las inscripciones **3 horas antes** del inicio. Si faltan plazas por cubrir en ese momento, cancelar la partida y liberar la pista.
- **Nivel manual del jugador:** permitir que cada jugador indique manualmente su nivel hasta un máximo de nivel 5. Los niveles 6 y 7 solo podrán ser asignados por el administrador.
- **Integridad de reservas e inscripciones:** evitar reservas coincidentes para una misma pista y horario, inscripciones duplicadas y superar las plazas disponibles.
- **Acceso de usuarios no registrados:** limitar su participación a partidas cerradas. No podrán participar en partidas abiertas ni torneos.

**Fase 2 — Ampliación incluida en el proyecto**

- **Pagos online:** incorporar la gestión de pagos dentro de la plataforma. En la Fase 1, los pagos se mantienen fuera de la plataforma.
- **Valoración dinámica del nivel:** aplicar la regla acordada de variación del valor interno del jugador: cada tres victorias consecutivas suman 0,1 y cada tres derrotas consecutivas restan 0,1. El nivel visible subirá al alcanzar el entero siguiente y bajará al alcanzar el umbral x,9 del nivel inferior.
- **Historial de valoración:** conservar el valor interno y el historial de cambios para aplicar los umbrales de subida y bajada.

### 3.2. SHOULD HAVE — Importante

Funcionalidades relevantes que mejoran la experiencia, pero cuya implementación se priorizará después de asegurar las funciones imprescindibles y dependerá de la complejidad y de los servicios externos disponibles.

- Enviar avisos y confirmaciones automáticas por correo electrónico.
- Comunicar cambios y cancelaciones de reservas o partidas a los usuarios afectados.

### 3.3. COULD HAVE — Deseable

Mejoras que aportan valor, pero que pueden incorporarse después de validar las funciones principales.

- Integración con AEMET para consultar información meteorológica.
- Alertas meteorológicas personalizadas.
- Monedero virtual o sistema de bonos.
- Integración con WhatsApp.
- Automatismos complementarios relacionados con las comunicaciones y la gestión del club.

### 3.4. WON'T HAVE — Fuera del alcance actual

Estas funcionalidades no se desarrollarán en las entregas actuales. Podrán estudiarse en futuras versiones.

- Integración con Garmin u otros relojes Bluetooth y registro de actividad física.
- Visualización 3D de la incidencia del sol y las sombras sobre las pistas.
- Gestión de clases.
- Gestión avanzada de torneos y ligas.

## 4. Reglas funcionales y restricciones que delimitan el alcance

- **Membresía:** existe un único rol de cliente. Ser socio o no socio es una condición asociada a la cuenta, no un rol independiente.
- **Antelación de reserva:** no se podrá reservar con más de 14 días de antelación.
- **Partidas abiertas:** forman parte de la Fase 1. Se publican, buscan y completan mediante inscripciones; el cierre se produce tres horas antes del comienzo y, si quedan plazas libres, la partida se cancela y la pista se libera.
- **Pagos:** el pago online dentro de la plataforma se aplaza a la Fase 2. Durante la Fase 1 se mantiene fuera de la plataforma.
- **Niveles:** en la Fase 1 el jugador puede indicar manualmente un nivel de hasta 5; los niveles 6 y 7 solo los asigna el administrador. La valoración dinámica se reserva para la Fase 2.
- **Usuarios sin registro:** solo pueden apuntarse a partidas cerradas; no pueden participar en partidas abiertas ni torneos.

## 5. Aspectos pendientes de confirmación con el cliente

El dosier identifica cuestiones que deben concretarse antes de cerrar el diseño y el desarrollo. Entre ellas:

- Escala de niveles de referencia, asignación del nivel inicial y tratamiento de resultados anulados, disputados o corregidos.
- Procedimiento de asignación administrativa de los niveles 6 y 7 y condiciones de progresión desde el nivel 5.
- Confirmación de tarifas, duración de las reservas individuales y de dobles, y si los importes corresponden al precio total de la pista o a cada jugador.
- Fechas exactas de los horarios de verano e invierno, festivos y cierres.
- Condiciones para hacerse socio, renovación y comprobación de la cuota anual.
- Política de cancelaciones, plazos, reembolsos y posibles bonos.
- Proveedor de pagos y canales de comunicación que se utilizarán.
- Tratamiento de datos personales, plazos de conservación y textos legales necesarios.

## 6. Nota de coherencia con las historias de usuario

En el dosier, las reglas funcionales acordadas y la tabla MoSCoW sitúan las **partidas abiertas en la Fase 1**, mientras que el apartado de historias de usuario agrupa actualmente HU13–HU19 bajo la Fase 2. Conviene revisar esa clasificación antes de crear las Issues: las historias relativas a publicar, buscar, inscribirse y administrar partidas abiertas deben quedar alineadas con la Fase 1; los pagos online y la valoración dinámica corresponden a la Fase 2.

---

**Documento académico de trabajo.** La priorización es una propuesta inicial del equipo y queda pendiente de validación con el propietario de VALL PALA.
