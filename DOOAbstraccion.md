# Abstraccion

La abstracción es el principio que permite representar objetos del mundo real resaltando solo los aspectos esenciales y relevantes para el sistema. En términos prácticos, se trata de definir qué hace un objeto, sin entrar en los detalles de cómo lo hace. Esto se logra principalmente mediante:
* Clases abstractas e interfaces, que definen contratos o comportamientos comunes sin especificar implementaciones concretas.
* Jerarquías de clases, donde las generalizaciones capturan lo común y las especializaciones lo particular.

### Importancia en el diseño
* Reduce la complejidad al ocultar detalles de implementación innecesarios.
* Facilita el cambio y la extensión del sistema, ya que el código depende de abstracciones y no de detalles específicos.
* Promueve la reutilización y el mantenimiento del código, ya que se pueden intercambiar implementaciones sin afectar el resto del sistema.

### Relacion con los principios SOLID
La abstracción está fuertemente vinculada con varios principios SOLID:

* S (Principio de Responsabilidad Unica): Al abstraer correctamente, cada clase puede tener una única responsabilidad bien definida.
* O (Principio de Abierto/Cerrado): Un diseño basado en abstracciones permite extender comportamientos sin modificar el código existente.
* D (Principio de Inversion de Dependencia): Este principio directamente promueve que los módulos dependan de abstracciones y no de implementaciones concretas.

### Relacion con los patrones de diseño
Muchos patrones de diseño se basan en el uso de abstracciones para resolver problemas comunes de manera flexible:

* Factory Method o Abstract Factory: utilizan abstracciones para crear objetos sin acoplarse a clases concretas.
* Strategy: define una interfaz comun para algoritmos intercambiables, permitiendo cambiar su comportamiento en tiempo de ejecucion.
* Adapter y Decorator: usan abstracciones para transformar o extender el comportamiento de clases sin alterar su código original.





## Ejemplo en el proyecto


## Ejemplo de codigo

