# Principio de Sustitucion de Liskov (LSP)
__Proposito:__ Su propósito es garantizar que las clases derivadas puedan ser utilizadas en lugar de sus clases base sin alterar el comportamiento correcto del sistema. Es decir, una subclase debe ser un sustituto válido de su superclase.

__Problema que soluciona:__ En ocasiones, al extender una clase base, se introduce un comportamiento en la subclase que rompe las expectativas del código que utiliza la clase original. Esto genera errores sutiles, difíciles de detectar, y debilita la reutilización del código. Además, puede derivar en sistemas frágiles, donde el uso de la herencia no respeta la lógica establecida por la clase padre.

__Como lo soluciona:__ El LSP obliga a diseñar subclases que mantengan las invariantes, contratos y expectativas definidos por la clase base. Esto significa que los métodos heredados no deben cambiar su comportamiento esencial y que las nuevas clases deben respetar la funcionalidad esperada por cualquier parte del sistema que utilice la clase base. De este modo, el código puede trabajar de forma genérica con abstracciones sin preocuparse por los detalles de las implementaciones específicas.
# Motivacion

# Estructura de Clases
