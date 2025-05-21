# Sistema de Gestión de Turnos Digitales (Tunomático)

## 📌 Descripción General

Tunomático es un sistema orientado a la gestión eficiente de turnos digitales en un contexto hospitalario. Este proyecto representa una solución moderna y escalable para facilitar la asignación, modificación, confirmación y cancelación de turnos, integrando además la sincronización de datos con sistemas hospitalarios externos.

El sistema fue modelado arquitectónicamente siguiendo principios de diseño orientado a objetos, empleando patrones de diseño reconocidos como Singleton, Prototype, Adapter y Bridge. Se ha buscado una separación clara de responsabilidades, extensibilidad futura y una base sólida para la implementación física en servidores distribuidos.

---

## 🎯 Diagrama de Casos de Uso

![Image](https://github.com/user-attachments/assets/9f8b766e-5406-4fbd-bf7f-884ce21b62f3)

El diagrama presenta dos actores principales:

- **Paciente**: Interactúa con el sistema para solicitar o cancelar turnos.
- **Administrador**: Tiene privilegios para confirmar, modificar turnos y gestionar la configuración del sistema.

### Relaciones destacadas:

- `Solicitar Turno` incluye la verificación de disponibilidad y la selección de fecha/hora.
- `Confirmar Turno` y `Modificar Turno` incluyen la sincronización con el hospital, asegurando integridad en tiempo real.
- El uso de relaciones `<<include>>` indica acciones obligatorias durante el flujo de cada caso de uso, evidenciando modularidad y cohesión.

---

## 🧠 Diagrama de Clases UML

![Image](https://github.com/user-attachments/assets/03381c7a-836f-4933-9b56-b6afccc411b9)

Este diagrama modela la estructura lógica del sistema y aplica 4 patrones de diseño fundamentales:

- **Singleton (`ConfiguraciónSistema`)**: Asegura una instancia única que gestiona parámetros críticos del sistema, accedida por el administrador.
- **Prototype (`PlantillaTurno`)**: Permite clonar modelos de turno estándar para nuevas asignaciones, optimizando rendimiento y flexibilidad.
- **Adapter (`AdaptadorHospital`)**: Facilita la integración con sistemas hospitalarios externos sin alterar la lógica del sistema principal.
- **Bridge (`InterfazUsuario`)**: Desacopla las interfaces de usuario para `Paciente` y `Administrador`, permitiendo variaciones independientes de la lógica de turnos.

Las relaciones reflejan interacciones realistas entre usuarios, entidades y patrones. Ninguna clase se encuentra aislada o vacía, y todas contribuyen a una arquitectura cohesiva y mantenible.

---

## 🏗️ Diagrama de Implementación

![Image](https://github.com/user-attachments/assets/dc0ea07c-bd6b-4039-bda0-31271c37f176)

Este diagrama representa la arquitectura física del sistema distribuido:

- **Servidor de Aplicaciones**: Aloja la lógica central (`Módulo Turnos`, `PlantillaTurno`, `ConfiguraciónSistema`).
- **Servidor Hospitalario**: Encapsula el `AdaptadorHospital`, encargado de la comunicación externa.
- **Servidor de Base de Datos**: Contiene la persistencia de turnos y sincronización.
- **Estación de Usuario**: Representa el acceso del cliente a través de una GUI que usa la `InterfazUsuario`.

### Decisiones técnicas:

- La separación de componentes en distintos nodos garantiza escalabilidad y robustez.
- Se usaron estereotipos UML para destacar los patrones aplicados dentro de los nodos.
- Las conexiones reflejan el flujo lógico de información y responsabilidades entre módulos.

---

## 🔍 Reflexiones Finales del Modelado

El proceso de modelado arquitectónico de Tunomático permitió identificar los puntos clave de escalabilidad, integración y flexibilidad requeridos por un sistema hospitalario moderno. El uso de patrones de diseño no fue meramente académico, sino que resolvió necesidades reales de cohesión, reutilización y extensibilidad.

La combinación de visión funcional (casos de uso), lógica estructural (clases con patrones) y física (implementación distribuida) entrega un panorama completo y profesional del sistema.

Este modelo está preparado para evolucionar hacia una implementación real y servir de base para nuevos módulos como alertas, análisis de datos o atención multicanal.

