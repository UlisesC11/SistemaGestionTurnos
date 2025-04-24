# Principio de Segregacion de Interfaces (ISP)
__Proposito:__ Está orientado a mejorar el diseño modular y la independencia entre componentes del sistema. Su propósito es evitar que los clientes (clases que consumen interfaces) estén obligados a depender de métodos que no utilizan.

__Problema que soluciona:__ Cuando se diseña una interfaz general con muchos métodos, diferentes clases que implementan esa interfaz pueden verse forzadas a implementar funcionalidades innecesarias, lo cual genera un código redundante o incluso vacío. Además, los clientes que dependen de estas interfaces terminan acoplados a funcionalidades que no necesitan, lo que provoca que cambios en la interfaz afecten a múltiples clases que no deberían verse involucradas.

__Como lo soluciona:__ El ISP propone dividir las interfaces grandes en múltiples interfaces más pequeñas y específicas, de manera que cada cliente implemente únicamente la funcionalidad que realmente necesita. Esto reduce el acoplamiento innecesario, mejora la claridad del diseño, y permite una mayor flexibilidad y reutilización de componentes.
# Motivacion

# Estructura de Clases
