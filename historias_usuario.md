# VALL PALA — Historias de usuario y priorización MoSCoW

**Proyecto:** Plataforma web para la gestión de pistas, reservas y partidas abiertas de pádel  
**Asignatura:** Proyecto Intermodular · 2.º DAW · Curso 2026/2027  
**Cliente:** VALL PALA · La Vall d'Uixó (Castellón)  
**Equipo:** Marcos García, Miguel Ángel López, Daniel Marco y Roberto Redondo  
**Fecha:** Noviembre de 2026

---

## 1. Objetivo y criterios de organización

Este documento recoge las historias de usuario de VALL PALA y su prioridad según el método **MoSCoW**. Las historias Must Have se organizan además por fase de implantación.

La clasificación MoSCoW del dosier establece que:

- **Must Have:** funcionalidades imprescindibles para el proyecto. Algunas se desarrollan en la Fase 1 y otras, aunque son imprescindibles para el alcance previsto, se incorporan en la Fase 2.
- **Should Have:** funcionalidades importantes que no impiden que la primera versión funcione.
- **Could Have:** mejoras deseables que se pueden incorporar si hay tiempo y recursos.
- **Won't Have:** funcionalidades excluidas de las entregas actuales.

> **Decisión de planificación:** las **partidas abiertas forman parte de la Fase 1 (MVP)**. La Fase 2 queda reservada para los **pagos online dentro de la plataforma** y la **valoración dinámica de los jugadores**. Esta distribución sigue las reglas operativas y la priorización MoSCoW del dosier.

## 2. Resumen de prioridades MoSCoW

| Prioridad | Funcionalidades incluidas en el dosier | Fase / tratamiento |
|---|---|---|
| **MUST HAVE** | Web responsive; registro; rol único de cliente con condición de socio/no socio; calendario y reservas con un máximo de 14 días de antelación; panel de administración; partidas abiertas; cierre automático 3 horas antes y liberación de pista si no se completa; nivel manual hasta 5; pagos online y valoración dinámica. | Fase 1: web, usuarios, socios, reservas, administración, partidas abiertas y niveles manuales. Fase 2: pagos online y valoración dinámica. |
| **SHOULD HAVE** | Avisos y confirmaciones automáticas por correo electrónico y comunicaciones de cambios o cancelaciones. | Se priorizará si el calendario, los proveedores y las integraciones lo permiten. |
| **COULD HAVE** | Integración con AEMET, alertas personalizadas, monedero virtual o bonos, WhatsApp y automatismos complementarios. | Mejoras posteriores, una vez validadas las funciones principales. |
| **WON'T HAVE** | Integración con Garmin y relojes Bluetooth o registro de actividad física; visualización 3D de la incidencia solar y las sombras; gestión de clases; gestión avanzada de torneos y ligas. | Fuera de las entregas actuales. Podrán reconsiderarse en futuras versiones. |

---

## 3. Historias de usuario MUST HAVE — Fase 1: MVP

La Fase 1 incluye la web informativa, las cuentas de usuario, la condición de socio, el calendario, las reservas, el panel de administración, las partidas abiertas y la introducción manual del nivel.

### HU01 · Consultar la información del club

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** visitante, **quiero** consultar la información de VALL PALA, sus instalaciones, fotografías, ubicación, horarios y tarifas, **para** conocer los servicios antes de registrarme.

**Criterios de aceptación:**
- La página muestra información básica de la empresa y sus siete pistas: seis pistas de dobles y una individual.
- Se muestran la ubicación, los horarios y las tarifas vigentes.
- La web se adapta a móviles, tabletas y ordenadores.

### HU02 · Registrarse e iniciar sesión

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** crear una cuenta e iniciar sesión, **para** realizar reservas y consultar mi actividad.

**Criterios de aceptación:**
- El registro solicita los datos necesarios y valida los campos obligatorios.
- El usuario puede iniciar sesión con sus credenciales.
- Las funciones y los datos privados solo son accesibles después de la autenticación correspondiente.

### HU03 · Gestionar los datos del perfil

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** consultar y modificar los datos permitidos de mi perfil, **para** mantener actualizada mi información de contacto.

**Criterios de aceptación:**
- El usuario puede consultar y modificar los datos personales permitidos.
- El sistema valida los datos introducidos.
- Los cambios quedan guardados y aparecen al volver a consultar el perfil.

### HU04 · Identificar la condición de socio

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** que mi cuenta refleje si tengo la condición de socio vigente, **para** que se me aplique automáticamente la tarifa correspondiente.

**Criterios de aceptación:**
- El sistema utiliza un único rol de cliente; ser socio no constituye un rol diferente.
- La cuenta indica si la condición de socio está vigente.
- El administrador puede gestionar el estado de la membresía.
- El sistema aplica y muestra la tarifa de socio o no socio según corresponda.

### HU05 · Consultar el calendario y la disponibilidad

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** consultar un calendario con las pistas y sus horarios disponibles, **para** elegir cuándo jugar.

**Criterios de aceptación:**
- Se pueden consultar fechas y franjas horarias.
- Se distingue entre disponibilidad y ocupación de cada pista.
- La información se actualiza cuando se confirma o cancela una reserva.

### HU06 · Reservar una pista

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** reservar una pista disponible indicando fecha y hora, **para** asegurar mi partida sin contactar directamente con el administrador.

**Criterios de aceptación:**
- El usuario puede seleccionar una pista, una fecha y una hora disponibles.
- Solo se permite reservar con un máximo de **14 días de antelación**.
- El sistema comprueba que no exista otra reserva coincidente para la misma pista y franja horaria.
- La reserva queda registrada y puede consultarse posteriormente.

### HU07 · Consultar mis reservas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** cliente, **quiero** consultar mis reservas, **para** conocer los datos y el estado de cada una.

**Criterios de aceptación:**
- El usuario autenticado visualiza sus reservas.
- Se muestran la fecha, la hora, la pista y el estado de la reserva.
- El usuario no puede consultar las reservas privadas de otros clientes.

### HU08 · Gestionar pistas, horarios y tarifas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** gestionar las pistas, los horarios y las tarifas, **para** mantener actualizada la oferta de VALL PALA.

**Criterios de aceptación:**
- El administrador puede consultar y modificar los datos de gestión autorizados.
- Los cambios quedan reflejados en la información disponible para los clientes.
- Las modificaciones no generan solapamientos con las reservas existentes.

### HU09 · Consultar todas las reservas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** consultar todas las reservas desde un panel privado, **para** supervisar la ocupación de las instalaciones.

**Criterios de aceptación:**
- El panel muestra las reservas por fecha, hora y pista.
- Se identifica al cliente que ha realizado cada reserva.
- Se muestra el estado de la reserva y, cuando esté disponible, el estado del pago.

### HU10 · Gestionar reservas manualmente

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** crear, modificar y cancelar reservas manualmente, **para** resolver incidencias y atender solicitudes especiales.

**Criterios de aceptación:**
- El administrador puede localizar una reserva.
- Puede modificarla o cancelarla aplicando las validaciones necesarias.
- La disponibilidad se actualiza después de la operación.

### HU11 · Gestionar usuarios y membresías

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** consultar y gestionar los usuarios y su condición de socio, **para** mantener organizada la base de clientes.

**Criterios de aceptación:**
- El administrador puede localizar usuarios y consultar sus datos de gestión autorizados.
- Puede actualizar la condición de socio conforme a las reglas acordadas.
- Las acciones administrativas quedan restringidas a usuarios autorizados.

### HU12 · Consultar el estado de los pagos

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** consultar el estado de los pagos asociados a las reservas, **para** controlar qué operaciones están pagadas o pendientes.

**Criterios de aceptación:**
- Cada reserva puede mostrar un estado de pago.
- En la Fase 1, el pago se realiza fuera de la plataforma, en las instalaciones.
- El administrador puede consultar y actualizar el estado correspondiente.
- El sistema no marca como pagado un importe sin confirmación válida del medio de pago o del administrador.

### HU13 · Publicar una partida abierta

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** jugador, **quiero** publicar una partida abierta indicando modalidad, fecha, hora, plazas disponibles y nivel requerido, **para** encontrar a otros participantes.

**Criterios de aceptación:**
- El formulario permite definir los datos esenciales de la partida.
- La partida queda visible cuando se publica correctamente.
- El creador puede consultar la partida publicada.

### HU14 · Buscar y filtrar partidas abiertas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** jugador, **quiero** buscar y filtrar partidas abiertas por fecha, horario y nivel, **para** encontrar una partida que se adapte a mi disponibilidad y experiencia.

**Criterios de aceptación:**
- Se muestran las partidas abiertas que admiten nuevas inscripciones.
- Los filtros permiten acotar por fecha, franja horaria y nivel.
- La información muestra las plazas ocupadas y disponibles.

### HU15 · Inscribirse o retirarse de una partida abierta

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** jugador, **quiero** inscribirme o retirarme de una partida abierta, **para** participar en encuentros sin tener que organizar un grupo completo.

**Criterios de aceptación:**
- El sistema permite inscribirse si quedan plazas y se cumplen las condiciones.
- No se permiten inscripciones duplicadas ni superar el número de plazas.
- La baja actualiza las plazas disponibles y la lista de participantes.

### HU16 · Indicar el nivel manual de juego

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** jugador, **quiero** indicar manualmente mi nivel de pádel, **para** encontrar partidas adecuadas a mi experiencia.

**Criterios de aceptación:**
- El jugador puede introducir manualmente un nivel hasta el **nivel 5**.
- Los niveles **6 y 7** solo pueden ser asignados por el administrador.
- El nivel se utiliza como criterio para buscar y filtrar partidas.

### HU17 · Supervisar las partidas abiertas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** administrador, **quiero** consultar y gestionar las partidas abiertas, **para** supervisar su funcionamiento y resolver incidencias.

**Criterios de aceptación:**
- El administrador puede consultar las partidas y sus participantes.
- Puede modificar o cancelar una partida conforme a las reglas definidas.
- Los cambios se reflejan en la información de la partida y de sus participantes.

### HU18 · Cerrar y cancelar automáticamente las partidas incompletas

**Prioridad:** MUST HAVE · **Fase:** 1 (MVP)

**Como** sistema, **quiero** cerrar las inscripciones tres horas antes del inicio y cancelar las partidas que no estén completas, **para** liberar la pista y evitar mantener una reserva que no se va a jugar.

**Criterios de aceptación:**
- El cierre de inscripciones se produce **3 horas antes** del inicio de la partida.
- Si en ese momento la partida no está completa, el sistema la cancela automáticamente.
- Al cancelarse, la pista queda liberada y vuelve a estar disponible en el calendario.

---

## 4. Historias de usuario MUST HAVE — Fase 2

Estas funcionalidades se consideran imprescindibles para el alcance previsto, pero se desarrollarán después de validar y estabilizar el MVP.

### HU19 · Pagar una reserva online

**Prioridad:** MUST HAVE · **Fase:** 2

**Como** cliente, **quiero** pagar online una reserva mediante uno de los métodos habilitados, **para** completar el pago sin tener que realizarlo presencialmente en las instalaciones.

**Criterios de aceptación:**
- La plataforma permite iniciar el pago de una reserva mediante los métodos habilitados por el proveedor seleccionado.
- El resultado de la operación se comunica a la plataforma.
- La reserva solo figura como pagada cuando existe confirmación válida del pago.
- El cliente puede consultar el estado del pago.

### HU20 · Actualizar la valoración dinámica del jugador

**Prioridad:** MUST HAVE · **Fase:** 2

**Como** jugador, **quiero** que mi valoración se actualice según mis rachas de victorias y derrotas, **para** que mi nivel visible refleje la evolución de mi rendimiento.

**Criterios de aceptación:**
- El sistema conserva el valor interno del jugador y el historial de cambios.
- Cada **tres victorias consecutivas** incrementan el valor interno en **0,1**.
- El nivel visible sube cuando el valor interno alcanza el entero siguiente.
- Cada **tres derrotas consecutivas** reducen el valor interno en **0,1**.
- El nivel visible baja cuando se alcanza el umbral **x,9 del nivel inferior**, según la regla acordada.
- La aplicación de los cambios se basa en resultados válidos registrados en el sistema.

---

## 5. Historias de usuario SHOULD HAVE

Estas funcionalidades son importantes, pero no impiden que el MVP funcione si no están disponibles en la primera entrega.

### HU21 · Recibir avisos y confirmaciones

**Prioridad:** SHOULD HAVE · **Fase:** A concretar según disponibilidad y planificación

**Como** cliente o jugador inscrito, **quiero** recibir confirmaciones y avisos sobre cambios o cancelaciones relacionados con mis reservas y partidas, **para** estar informado y evitar desplazamientos innecesarios.

**Criterios de aceptación propuestos:**
- Se generan avisos ante los eventos que se definan, como confirmaciones, cambios y cancelaciones.
- El mensaje identifica la reserva o partida afectada y el cambio producido.
- Se prioriza el correo electrónico; otros canales dependerán de las integraciones disponibles.

---

## 6. Funcionalidades COULD HAVE y WON'T HAVE

El dosier no plantea estas funcionalidades como requisitos Must Have, por lo que no se desarrollan aquí como historias obligatorias.

### COULD HAVE — Deseables

- Integración meteorológica con AEMET.
- Alertas personalizadas.
- Monedero virtual o bonos para gestionar importes derivados de cancelaciones.
- Integración con WhatsApp.
- Automatismos complementarios.

### WON'T HAVE — Fuera del alcance actual

- Integración con Garmin o relojes Bluetooth y registro de actividad física.
- Visualización 3D de la incidencia del sol y las sombras en las pistas.
- Gestión de clases.
- Gestión avanzada de torneos y ligas.

---

## 7. Resumen de historias por fase y prioridad

| Fase | Historias | Prioridad | Contenido |
|---|---|---|---|
| **Fase 1 · MVP** | HU01–HU18 | MUST HAVE | Web, cuentas, perfil, socios, calendario, reservas, administración, estado de pagos fuera de la plataforma, partidas abiertas, niveles manuales y cierre automático. |
| **Fase 2** | HU19–HU20 | MUST HAVE | Pagos online dentro de la plataforma y valoración dinámica de jugadores. |
| **A concretar** | HU21 | SHOULD HAVE | Avisos y confirmaciones automáticas. |
| **Futuras mejoras** | — | COULD HAVE | AEMET, alertas personalizadas, monedero o bonos, WhatsApp y automatismos complementarios. |
| **Fuera del alcance actual** | — | WON'T HAVE | Garmin/relojes, actividad física, visualización 3D solar, clases y gestión avanzada de torneos y ligas. |

## 8. Reglas y decisiones pendientes de validación

Antes de programar, se deben confirmar con el propietario las cuestiones que el dosier deja abiertas:

- La escala de niveles de referencia y su correspondencia con los niveles conocidos por los jugadores.
- El procedimiento de asignación administrativa de los niveles 6 y 7 y las condiciones de progresión desde el nivel 5.
- El tratamiento de resultados anulados, disputados o corregidos y la conservación del historial de nivel.
- Las condiciones concretas de las tarifas, la duración de las reservas individuales y de dobles y si existen suplementos o reglas especiales.
- Si los importes indicados para las pistas corresponden al precio total de la pista o a cada jugador.
- Las fechas de inicio y fin de los horarios de verano e invierno, festivos y cierres.
- Las condiciones para hacerse socio, renovar la membresía y comprobar la cuota anual.
- La política de cancelaciones, plazos, reembolsos y emisión de bonos.
- El proveedor de pagos y los métodos que se habilitarán en la Fase 2.
- Los canales de notificación y las comunicaciones que se automatizarán.
- Las reglas de las partidas abiertas, incluida la inscripción, el cierre tres horas antes y la cancelación automática si la partida no se completa.
- El responsable de asignar los niveles 6 y 7 y supervisar las incidencias de resultados.

---

**Documento académico de trabajo.** Las historias y sus criterios de aceptación son una propuesta basada en el dosier de VALL PALA y quedan sujetos a validación con el cliente.
