# PendienteU

Aplicación móvil para ayudar a estudiantes universitarios a organizar sus tareas y fechas de entrega.

## Usuario primario

Estudiantes universitarios que necesitan organizar las tareas y actividades pendientes de sus diferentes cursos.

## Problema

Los estudiantes universitarios manejan múltiples tareas y fechas de entrega de diferentes cursos, lo que puede dificultar llevar un control claro de sus actividades pendientes y provocar que algunas entregas se olviden o se realicen fuera de tiempo.

## Evidencia

Se observó que algunos estudiantes llegan a faltar con tareas por falta de organización, ya sea por una mala gestión del tiempo o por confusión en las fechas de entrega.

## Flujo principal del MVP

Consultar lista de tareas -> registrar una nueva tarea indicando curso, descripción y fecha de entrega -> la tarea queda almacenada y visible en la lista de pendientes.

## Alcance del MVP

### Incluye

1. Registrar tareas indicando curso, descripción y fecha de entrega.
2. Consultar las tareas registradas en una lista de pendientes.
3. Marcar las tareas como completadas.

### No incluye todavía

1. Inicio de sesión y cuentas de usuario.
2. Sincronización de información en la nube.
3. Notificaciones y recordatorios automáticos.

## Equipo y roles

| Integrante | Rol |
|---|---|
| Andrea | Producto / PM |
| Kenneth | Arquitectura |
| Luis | UX / Investigación |
| Luis | QA / Release |

## Flujo de trabajo

Todo cambio realizado en el proyecto seguirá el siguiente proceso:

Issue -> Rama -> Pull Request -> Revisión -> Merge

Nadie trabaja directamente sobre la rama `main`.

## Decisiones técnicas iniciales

### Manejo de estado

Durante el MVP, PendienteU utilizará `setState` de Flutter para manejar los cambios de estado de las tareas dentro de la aplicación.

Se eligió esta alternativa porque el flujo inicial de la aplicación es pequeño y no requiere una solución de gestión de estado más compleja.

### Almacenamiento de datos

Para el MVP se utilizará almacenamiento local mediante `shared_preferences`, guardando la información de las tareas en el dispositivo.

Esta alternativa permite conservar los datos sin implementar autenticación, servidores o sincronización en la nube, manteniendo el alcance inicial del proyecto sencillo.
