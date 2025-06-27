# Anexo - Aplicacion de Patron de Diseño Estructural - Facade

Proposito de los patrones estructurales: Organizar las relaciones entre clases y objetos, facilitando la reutilización y el mantenimiento del codigo.

Relacion con SOLID:
* Principio de Abierto/Cerrado (OCP): Permiten extender funcionalidades sin modificar el codigo existente.
* Principio de Sustitución de Liskov (LSP): Facilitan el uso de estructuras intercambiables de manera segura.

Propósito  y  Tipo  del  Patrón:  El patrón Facade proporciona una interfaz simplificada y unificada para un conjunto de subsistemas complejos. Su objetivo es ocultar la complejidad interna del sistema y ofrecer una forma clara de acceso para los clientes o usuarios externos.

## Motivacion
En el sistema de gestión de turnos, existen múltiples módulos que interactúan entre sí, como el registro de pacientes, la asignación de turnos, el envío de notificaciones, el control de disponibilidad médica y la gestión de historiales. Permitir que los actores del sistema (como el recepcionista o el administrador) interactúen directamente con todos estos componentes genera un sistema difícil de mantener y propenso a errores. El uso del patrón Facade permite encapsular toda esa lógica detrás de una clase central, como "SistemaTurnosFacade" que expone métodos simples como registrarPaciente(), registrarMedico(), registrarTurno(), cancelarTurno(), verHistorial(). De esta manera, el usuario o módulo externo no necesita conocer la estructura interna ni la secuencia de llamadas necesarias, reduciendo el acoplamiento y mejorando la organización del sistema.


## Estructura de Clases
[Enlace del diagrama](https://drive.google.com/file/d/1XXEPMDmZOtIwPil2EGjq1OKOeWUhc7oy/view?usp=sharing)
![image](https://github.com/user-attachments/assets/b1eed268-ac0e-4f77-8d2f-34aca5dafcc3)
