# Tunomático - Sistema de Gestión de Turnos Digitales

## 📌 Descripción General
Tunomático es un sistema de gestión de turnos diseñado para optimizar la administración de citas en entornos hospitalarios. Utiliza patrones de diseño como **Singleton**, **Prototype**, **Adapter** y **Bridge**, asegurando una arquitectura modular y escalable.  

El objetivo principal es ofrecer a **pacientes** y **administradores** una experiencia fluida para solicitar, modificar y gestionar turnos de forma eficiente, reduciendo la carga operativa del sistema hospitalario.  

---

## 🎯 **Diagrama de Caso de Uso**
![Diagrama de Caso de Uso]
![Image](https://github.com/user-attachments/assets/9f8b766e-5406-4fbd-bf7f-884ce21b62f3)

### 🔹 **Justificación de Relaciones**
✅ **Relaciones `<<include>>`** → Se usan para casos que dependen de otros procesos clave (ejemplo: verificar disponibilidad antes de seleccionar fecha y hora).  
✅ **Relaciones directas entre actores y casos de uso** → `Paciente` puede solicitar y cancelar turnos, mientras que `Administrador` los gestiona.  
✅ **Modularidad del sistema** → Cada acción es independiente, permitiendo futuras ampliaciones sin alterar la estructura.  

---

## 📜 **Diagrama de Clases**
![Diagrama de Clases](AQUÍ_DEBES_AGREGAR_LA_RUTA_DE_LA_IMAGEN_DEL_DIAGRAMA_DE_CLASES)

### 🔹 **Justificación de Patrones de Diseño**
✅ **`Singleton` (ConfiguraciónSistema)** → Se asegura que **solo exista una instancia** de la configuración global del sistema.  
✅ **`Prototype` (PlantillaTurno)** → Permite clonar modelos de turnos sin necesidad de crear nuevas instancias, optimizando el rendimiento.  
✅ **`Adapter` (AdaptadorHospital)** → Actúa como puente entre Tunomático y el sistema hospitalario, adaptando formatos de datos.  
✅ **`Bridge` (InterfazUsuario)** → Desacopla la lógica de presentación, permitiendo múltiples interfaces para distintos actores (`Paciente`, `Administrador`).  

---

## 🏗 **Diagrama de Implementación**
![Diagrama de Implementación]https://github.com/Que-Master/Sistema-Tunom-tico/issues/1#issue-3078676725

### 🔹 **Decisiones Técnicas**
✅ **Nodos físicos bien estructurados**, asegurando separación de responsabilidades entre servidores y estaciones cliente.  
✅ **Interacción entre `Servidor de Aplicaciones`, `Base de Datos` y `AdaptadorHospital`**, asegurando sincronización de turnos.  
✅ **Uso de componentes desacoplados**, mejorando la modularidad y mantenibilidad del sistema.  

---

## 🔍 **Reflexiones Finales sobre el Modelado**
El diseño de **Tunomático** se enfoca en la escalabilidad, modularidad y flexibilidad. La aplicación de patrones de diseño garantiza una arquitectura **clara**, **mantenible** y **eficiente**, permitiendo futuras mejoras sin alterar la base del sistema.  

Además, el enfoque en desacoplamiento asegura que la **interfaz**, **gestión de turnos** y **sincronización hospitalaria** puedan evolucionar independientemente, facilitando la integración con otros sistemas.  

Tunomático está listo para ser desplegado y mejorado con base en futuras necesidades hospitalarias. 🚀  

---

## 📜 **Licencia**
Tunomático es un proyecto de código abierto bajo la licencia **MIT**.
