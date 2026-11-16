# Estudio de viabilidad y fases de VALL PALA

VALL PALA se plantea como una aplicación web para consultar la disponibilidad de pistas de pádel y gestionar reservas. La primera versión permitirá iniciar sesión, consultar franjas libres, reservar una pista y ver las reservas propias. El perfil administrador podrá gestionar pistas y consultar las reservas.

## 1. Fases del proyecto

| Fase | Trabajo previsto | Resultado |
|---|---|---|
| **1. Preparación y autenticación** | Configurar el entorno de desarrollo y la base de datos. Implementar el inicio y cierre de sesión y los permisos de usuario y administrador. | Cada perfil accede a las pantallas que le corresponden. |
| **2. Panel principal y disponibilidad** | Crear el panel principal y mostrar las pistas y franjas disponibles para la fecha seleccionada. | El usuario puede consultar qué pistas están libres y a qué horas. |
| **3. Reservas** | Implementar el formulario, validar los datos en el servidor, guardar la reserva y mostrar las reservas propias. | El usuario puede reservar una franja libre y comprobar su reserva desde el panel. |
| **4. Administración** | Crear una pantalla para dar de alta o desactivar pistas y consultar las reservas. | El administrador puede gestionar las pistas y revisar su ocupación. |
| **5. Pruebas y despliegue** | Probar los permisos, las reservas simultáneas y el uso desde el móvil. Desplegar la aplicación y documentar su instalación en el README. | La aplicación queda disponible para la demostración y el equipo puede instalarla. |

## 2. Viabilidad técnica

| Componente | Tecnología propuesta | Uso |
|---|---|---|
| **Frontend** | HTML, CSS y JavaScript | Construir el inicio de sesión, el panel y el formulario. JavaScript actualizará las franjas visibles al cambiar de fecha o pista. |
| **Backend** | PHP 8 | Gestionar las sesiones, comprobar permisos y validar las reservas antes de guardarlas. |
| **Base de datos** | MySQL | Guardar usuarios, pistas, franjas y reservas. |
| **Control de versiones** | Git y GitHub | Compartir el código, revisar cambios y mantener la documentación. |

El equipo necesita un entorno local con PHP y MySQL y, para la demostración, un alojamiento compatible con ambas tecnologías y con HTTPS. La disponibilidad se calcula a partir de las franjas y las reservas guardadas en la base de datos, por lo que la primera versión puede funcionar sin APIs externas.

El principal riesgo técnico es que dos usuarios intenten reservar la misma pista a la misma hora. La primera versión utilizará **franjas horarias fijas** y una **restricción de unicidad en MySQL para la combinación de pista, fecha y franja**. Si coinciden dos solicitudes, solo se guardará una reserva y la otra recibirá un aviso para escoger otro horario.

La demostración cubrirá el recorrido **iniciar sesión → consultar disponibilidad → reservar → ver la reserva**. Los pagos y las notificaciones automáticas quedan para una posible ampliación.
