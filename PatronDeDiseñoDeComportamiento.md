# Anexo - Aplicacion de Patron de Diseño de Comportamiento - Observer

Proposito de los patrones de comportamiento: Definir como interactuan los objetos entre si, quien toma decisiones, como se comunican o como se reparten responsabilidades.

Relacion con SOLID:
* Principio de Abierto/Cerrado (OCP): Nuevos comportamientos se pueden agregar facilmente.
* Principio de Responsabilidad Única (SRP): Separan la logica de decisiones del resto del sistema.
* Principio de Inversión de Dependencias (DIP): Permiten comunicar objetos a traves de abstracciones.

Propósito  y  Tipo  del  Patrón:  El patrón Observer permite establecer una relación de suscripción entre objetos, de manera que cuando uno cambia su estado, todos sus observadores son notificados automáticamente. Es ideal para situaciones donde múltiples partes del sistema deben reaccionar a un evento sin estar acopladas entre sí.

## Motivacion
En el sistema de gestión de turnos, cada vez que se crea, modifica o cancela un turno, es necesario informar al médico y al paciente involucrados. Implementar el patrón Observer permite que los turnos actúen como sujetos (Subject) y que los médicos y pacientes se comporten como observadores (Observers). Esto asegura una notificación automática y desacoplada, el sistema no necesita saber cómo se notifica a cada observador, solo se encarga de informar que hubo un cambio.

## Estructura de Clases
[Enlace del diagrama](https://drive.google.com/file/d/1pbEuUfzRWZfqrHzj2tz5NFHcwwk31Ww_/view?usp=sharing)
![image](https://github.com/user-attachments/assets/46208e6d-fe01-4e8c-aa8b-69a57be22952)


