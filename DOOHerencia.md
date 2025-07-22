# Herencia

La herencia es el principio que permite crear una nueva clase (subclase o clase hija) a partir de una clase existente (superclase o clase padre), reutilizando atributos y comportamientos ya definidos. De esta forma, se puede extender o especializar el comportamiento de una clase base sin reescribir código. Se representa mediante relaciones como:
* class Animal {...}
* class Perro extends Animal {...}

### Importancia en el diseño
* Promueve la reutilización de código, al evitar repetir estructuras comunes.
* Facilita la extensión del sistema, ya que las subclases pueden añadir o modificar comportamientos.
* Permite crear jerarquías de clases, reflejando relaciones del mundo real (por ejemplo, "Empleado es una Persona").


Sin embargo, un mal uso de la herencia puede producir sistemas frágiles o con acoplamiento excesivo. Por eso, se recomienda usarla con precaución.

### Relación con los principios SOLID
La herencia se relaciona especialmente con:
* L (Principio de Sustitucion de Liskov): Una subclase debe poder sustituir a su clase base sin alterar el comportamiento esperado. Si no se respeta, se rompe la lógica del programa.
* O (Principio de Abierto/Cerrado): La herencia permite extender clases existentes (abiertas a extensión) sin modificarlas (cerradas a modificación).


Y de forma indirecta con:
* S (Principio de Responsabilidad Unica): Si una jerarquía de clases no respeta SRP, puede acumular múltiples responsabilidades, dificultando la mantenibilidad.

### Relación con los patrones de diseño
Muchos patrones de diseño aprovechan o se relacionan con la herencia:
* Template Method: define la estructura de un algoritmo en una clase base y permite que las subclases redefinan ciertos pasos sin cambiar la estructura general.
* Factory Method: se apoya en la herencia para permitir que las subclases decidan qué objeto crear.
* Strategy y State: son ejemplos de composición sobre herencia, lo cual es una buena práctica moderna que evita los problemas del acoplamiento fuerte en jerarquías complejas.



## Ejemplo en el proyecto


## Ejemplo de codigo
