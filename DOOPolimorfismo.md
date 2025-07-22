# Polimorfismo

El polimorfismo es el principio que permite que una misma operación pueda tener diferentes comportamientos, dependiendo del objeto que la invoque. En otras palabras, diferentes clases pueden responder de manera distinta al mismo mensaje (método). Existen dos tipos principales:
* Polimorfismo de inclusión (subtipado): una clase hija puede ser tratada como si fuera de la clase padre. Ejemplo:\
  Animal a = new Perro();\
  a.hacerSonido(); 
* Polimorfismo paramétrico (genéricos): permite escribir código independiente del tipo de datos. Ejemplo:\
  List< T > en Java.

### Importancia en el diseño
* Aumenta la flexibilidad del código, ya que permite que una función trabaje con múltiples tipos de objetos.
* Facilita la extensibilidad, ya que se pueden agregar nuevas clases sin modificar el código existente que usa polimorfismo.
* Favorece el desacoplamiento, al trabajar con interfaces o clases abstractas en lugar de implementaciones concretas.

### Relación con los principios SOLID
El polimorfismo es clave para varios principios SOLID:
* O (Principio de Abierto/Cerrado): Gracias al polimorfismo, el comportamiento del sistema se puede extender a través de nuevas clases sin modificar las existentes.
* L (Principio de Sustitucion de Liskov): Este principio se basa directamente en el polimorfismo, garantizando que los objetos de una subclase puedan usarse donde se espera la superclase sin alterar el comportamiento.
* D (Principio de Inversion de Dependencia): Fomenta depender de abstracciones (interfaces) en lugar de clases concretas, lo cual es posible gracias al polimorfismo.

### Relación con los patrones de diseño
El polimorfismo es la base fundamental de muchos patrones de diseño, especialmente aquellos que dependen de interfaces para permitir el cambio de comportamiento:
* Strategy: permite seleccionar algoritmos en tiempo de ejecución mediante una interfaz común.
* State: cambia el comportamiento de un objeto según su estado actual, cada uno representado por una clase que implementa una interfaz.
* Command: encapsula una acción en un objeto y permite ejecutar comandos de manera polimórfica.
* Observer: permite que múltiples objetos reaccionen a un cambio, todos implementando una misma interfaz.



## Ejemplo en el proyecto 

## Ejemplo en codigo
