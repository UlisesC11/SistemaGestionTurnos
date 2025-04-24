# Principio de Abierto/Cerrado (OPC)
__Proposito:__ su propósito es permitir que los módulos de software sean extensibles sin necesidad de ser modificados. En otras palabras, el comportamiento de una clase debe poder ampliarse sin alterar su implementación original.

__Problema que soluciona:__ A medida que un sistema crece y evoluciona, es común que se requieran cambios en su funcionalidad. Si estos cambios implican modificar directamente las clases existentes, el código se vuelve frágil, difícil de mantener y propenso a errores. Cada modificación puede romper funcionalidades previamente correctas, además de incrementar el costo de pruebas y mantenimiento.

__Como lo soluciona:__ El OCP propone que los módulos estén abiertos para la extensión (es decir, que podamos agregar nuevas funcionalidades) pero cerrados para la modificación (es decir, que el código existente no deba cambiar). Esto se logra mediante el uso de abstracciones, como interfaces o clases abstractas, y técnicas como herencia y polimorfismo. De esta forma, podemos extender comportamientos mediante nuevas clases que implementen o hereden de una clase base, sin tocar el código ya probado.

# Motivacion

# Estructura de Clases
