# Encapsulamiento

El encapsulamiento es el principio que consiste en ocultar el estado interno de un objeto y restringir el acceso directo a sus datos, permitiendo interactuar con él solo a través de sus métodos públicos (interfaces). Esto asegura que el objeto controle su propio comportamiento y estado, protegiendo su integridad. Se implementa principalmente con:
* Modificadores de acceso (por ejemplo: private, protected, public).
* Métodos "getters" y "setters", para acceder o modificar atributos de forma controlada.

### Importancia en el diseño
* Protege los datos sensibles del objeto evitando modificaciones externas no controladas.
* Promueve la modularidad, ya que cada objeto gestiona su estado internamente.
* Facilita el mantenimiento y evolución del sistema, al permitir cambios internos sin afectar otras partes del código.
* Reduce el acoplamiento, ya que las clases interactúan entre sí solo mediante interfaces bien definidas.

### Relación con los principios SOLID
El encapsulamiento refuerza varios principios SOLID:

* S (Principio de Responsabilidad Unica): Al encapsular responsabilidades, cada clase se enfoca en una sola tarea.
* L (Principio de Sustitucion de Liskov): Las subclases que respetan el encapsulamiento pueden sustituir a sus superclases sin alterar el comportamiento del sistema.
* I (Principio de Segregacion de Interfaz): Fomenta el diseño de interfaces pequeñas y específicas, ocultando detalles innecesarios.
* D (Principio de Inversion de Dependencia): Al encapsular detalles, se puede trabajar con abstracciones en lugar de implementaciones concretas.

### Relación con los patrones de diseño
El principio de encapsulamiento es la base de varios patrones de diseño, por ejemplo:

* Facade: encapsula subsistemas complejos detrás de una interfaz simple y unificada.
* Mediator: centraliza la comunicación entre objetos, encapsulando las interacciones.
* Command: encapsula una petición como un objeto, permitiendo parametrizar acciones.
* Observer: encapsula el mecanismo de notificación, manteniendo objetos desacoplados.




## Ejemplo en el proyecto


## Ejemplo en codigo
