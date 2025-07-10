# Anexo - Aplicacion de Patron de Diseño Creacional - Factory Method

Proposito de los patrones creacionales: Controlar como se crean los objetos, dando flexibilidad para instanciarlos sin acoplar el codigo a clases concretas.

Relacion con SOLID: 
* Principio de Responsabilidad Única (SRP): Separan la logica de creación del objeto de su uso.
* Principio de Inversión de Dependencia (DIP): Permiten depender de abstracciones en lugar de clases concretas.

Propósito  y  Tipo  del  Patrón:  El patrón Factory Method permite delegar la creación de objetos a subclases, encapsulando el proceso de instanciación y permitiendo que el código cliente dependa de abstracciones en lugar de clases concretas. Es útil cuando se desea crear objetos similares pero con algunas diferencias en su implementación o comportamiento, sin acoplar el sistema a tipos específicos.

## Motivacion
En el sistema de gestión de turnos, se deben crear distintos tipos de objetos como Paciente, Medico, Recepcion. Sin el patrón Factory Method, la lógica de creación de estos objetos estaría dispersa por todo el sistema, generando acoplamiento innecesario y dificultando la modificación o extensión futura. Al implementar el patrón, se centraliza la lógica de creación en clases específicas como: UsuarioFafrica con metodos crearUsuario().

## Estructura de Clases
[Enlace del diagrama](https://drive.google.com/file/d/155kK2KEtgsosS9zuiFfmieWMAB5BC32Q/view?usp=sharing)
<img width="998" height="380" alt="image" src="https://github.com/user-attachments/assets/e5b75e64-903c-4be7-961c-6e0433c8ffb7" />
