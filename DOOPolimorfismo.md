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





## Ejemplo en el proyecto 
IIncluir un diagrama UML que muestra cómo la clase o las clases del proyecto se
relacionan entre sí al aplicar abstracción. Incluir una imagen incrustada, así como el
enlace correctamente referenciado para ver el diagrama en detalle. Describe cómo
el diagrama de las clases seleccionadas refleja el polimorfismo. Incluir
justificación técnica de cómo esas clases seleccionadas del proyecto cumplen
el fundamento.

## Ejemplo en codigo
Incluir un fragmento de código que demuestre la implementación de Polimorfismo en
el proyecto (puede ser pseudocódigo o un lenguaje como JavaScript, Python o
Java).
