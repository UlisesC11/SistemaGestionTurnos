# Principio de Inversion de Dependencias (DIP)
__Proposito:__ Se centra en la separación de dependencias dentro del sistema. Su propósito es garantizar que las entidades de software dependan de abstracciones (interfaces o clases abstractas) y no de implementaciones concretas. Además, plantea que los módulos de alto nivel no deben depender de los módulos de bajo nivel, sino que ambos deben depender de abstracciones.

__Problema que soluciona:__ Sin aplicar este principio, las clases de alto nivel (que contienen la lógica central del negocio) tienden a depender directamente de clases de bajo nivel (como implementaciones concretas de bases de datos, servicios externos, o componentes de hardware). Esto genera un sistema rígido y difícil de modificar, ya que cualquier cambio en los detalles de implementación afecta a los módulos de alto nivel. Además, el código se vuelve difícil de probar porque es complicado reemplazar las dependencias reales por mock objects en pruebas unitarias.

__Como lo soluciona:__ El DIP promueve que las dependencias sean invertidas. En lugar de que los módulos de alto nivel dependan directamente de las clases de bajo nivel, ambas partes deben depender de abstracciones. Esta separación permite que las implementaciones concretas sean intercambiables sin afectar la lógica del negocio. De este modo, el sistema se vuelve más flexible, reutilizable y fácil de mantener.

# Motivacion

# Estructura de Clases
