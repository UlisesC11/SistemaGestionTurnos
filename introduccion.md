# Anexo - Introduccion al Diseño Orientado a Objetos
El paradigma orientado a objetos (POO) es un modelo de desarrollo de software basado en la organización de datos y funcionalidades en entidades llamadas __objetos__, los cuales se definen a partir de __clases__. Este enfoque permite construir sistemas más modulares, reutilizables y escalables, facilitando su mantenimiento y evolución.
Su importancia radica en que, a diferencia del modelo estructurado, el POO promueve una forma de desarrollo más cercana a la realidad, donde los objetos interactúan entre sí de manera similar a como lo hacen en el mundo real. Esto facilita la comprensión del sistema y mejora la organización del código.
Además, el uso de conceptos como __herencia__, __encapsulamiento__ y __polimorfismo__ permite crear software más flexible y adaptable a cambios. El estudio de estos principios, junto con técnicas como el modelado de casos de uso, es fundamental para diseñar sistemas eficientes y alineados con los requisitos del negocio.

## Los cuatro fundamentos de POO
Este enfoque se basa en cuatro principios fundamentales: __encapsulación__, __abstracción__, __herencia__ y __polimorfismo__. Estos conceptos proporcionan una estructura sólida para el diseño y desarrollo de sistemas complejos, permitiendo la modularidad, reutilización y mantenibilidad del código.
El modelo orientado a objetos revoluciona la forma en que concebimos y desarrollamos software, permitiendo una mayor flexibilidad y adaptabilidad a medida que los sistemas crecen en tamaño y complejidad

1. __Encapsulación__: Es el proceso de ocultar la implementación interna de un objeto y exponer sólo las interfacespúblicas. Esto permite que los objetos mantengan su estado interno protegido de accesos no autorizados, promoviendo así la modularidad y la seguridad del sistema.
    * Ejemplo, Cajero Automático: Un cajero automático expone solo ciertas funciones al usuario, como retirar dinero o consultar el saldo, pero oculta la lógica interna de seguridad, validación de PIN y comunicación con el banco.

      ![image](https://github.com/user-attachments/assets/df60ad8d-d2dc-4fe5-b264-2d2d091dff98)

2. __Abstracción__: Consiste en simplificar la complejidad del mundo real modelando solo los aspectos esenciales relevantes para el sistema. Los objetos abstractos representan entidades del dominio de aplicación y sus interacciones, lo que facilita la comprensión y el diseño del software.
    * Ejemplo, Vehículo: Al modelar un sistema de transporte, no necesitamos todos los detalles físicos de un auto. Solo consideramos aspectos esenciales como marca, modelo, velocidad y funciones como acelerar o frenar.

      ![image](https://github.com/user-attachments/assets/991a0a17-673e-4f2a-a1d2-16247526d450)

4. __Herencia__: Es un mecanismo que permite que un objeto herede propiedades y comportamientos de otro objeto. Esto fomenta la reutilización del código y la creación de jerarquías de clases, donde las clases secundarias pueden extender o modificar el comportamiento de las clases primarias.
    * Ejemplo, Animales: Un perro y un gato son animales y comparten características como "nombre" y "edad", pero cada uno tiene comportamientos distintos, como "ladrar" o "maullar".

      ![image](https://github.com/user-attachments/assets/0789ad77-ce2d-4309-abb7-d1c7e866c568)

      
5. __Polimorfismo__: Se refiere a la capacidad de los objetos de una misma jerarquía de clases para responder de manera diferente a un mismo mensaje. Esto permite escribir código genérico que puede funcionar con varios tipos de objetos, promoviendo la flexibilidad y la extensibilidad del sistema.
    * Ejemplo, Pago en una tienda: Un cliente puede pagar con tarjeta de crédito, débito o efectivo. Aunque cada método funciona de manera diferente, el sistema simplemente llama al método pagar(), sin importar el tipo de pago.

      ![image](https://github.com/user-attachments/assets/cd425c7a-2c19-49f7-bce9-eae3bd7210d2)

## Requisitos iniciales del sistema

* 1er requisito: el sistema debe permitir asignar turnos a los pacientes
* 2do requisito: enviar notificaciones a los pacientes y medicos cuando los turnos se confirman, cancelan o modifican
* 3er requisito: registrar pacientes con sus datos personales y tener asociado un historial de turnos
* 4to requisito: registrar medicos con sus datos personales, especialidad y horarios de atencion
* 5to requisito: tener un sistema de autentificacion para poder diferenciar entre pacientes, medicos y personal autorizado

## Casos de uso

__1er caso de uso__
* Nombre: Registrar un paciente
* Actores involucrados: Personal autorizado
* Descripcion: permite registrar pacientes con sus datos personales al sistema
* Flujo principal de eventos:
1. el personal autorizado ingresa al sistema y elige la opcion "registrar paciente"
2. ingresa los datos personales del paciente
3. confirma los datos y guarda la informacion
* Precondiciones: el personal autorizado debe estar registrado
* Postcondiciones: el paciente queda registrado en el sistema


__2do caso de uso__
* Nombre: Agendar un turno
* Actores involucrados: personal autorizado, paciente
* Descripcion: permite asignar un turno a un paciente 
* Flujo principal de eventos:
1. el paciente solicita un turno
2. el personal autoriazado se fija que turnos estan disponibles
3. el personal autoriazado elige fecha y hora del turno disponible
4. se le asigna el turno al paciente
5. se envia notificacion al paciente y medico sobre el turno
* Precondiciones: el paciente tiene que estar registrado en el sistema
* Postcondiciones: el turno queda agendado y se notifica

__3er caso de uso__
* Nombre: confirmar turno
* Actores involucrados: paciente
* Descripcion: permite que el paciente confirme el turno que se le asigno
* Flujo principal de eventos:
1. el sistema envia una notificacion al paciente para confirmar
2. el paciente responde la confirmacion, puede ser mediante mensaje o correo
3. se actualiza el estado del turno a "confirmado"
* Precondiciones: el paciente debe tener un turno asignado
* Postcondiciones: el turno cambia de estado a "confirmado"

__4to caso de uso__
* Nombre: cancelar turno
* Actores involucrados: paciente, medico
* Descripcion: permite que el paciente cancele el truno que se le asigno
* Flujo principal de eventos:
1. el paciente ingresa al sistema
2. elige la opcion de "cancelar turno"
3. selecciona el turno que tenia asignado
4. se actualiza el estado del turno a "cancelado"
5. se notifica al paciente y medico que el turno fue cancelado
* Precondiciones: el paciente debe tener un turno ya confirmado
* Postcondiciones: el turno cambia de estado a "cancelado"

__5to caso de uso__
* Nombre: historial de turnos del paciente
* Actores involucrados: personal autorizado, medico
* Descripcion: permite ver el historial de los turnos que tuvo y tendra un paciente
* Flujo principal de eventos:
1. el personal autorizado o medico ingresan al sistema
2. buscan al paciente en el sistema
3. eligen la opcion de "historial de turnos"
4. muesta los turnos asociados al paciente
* Precondiciones: el paciente tiene que estar registrado en el sistema
* Postcondiciones: se muestra el historial de turnos en pantalla
  
## Boceto inicial del diseño de clases
Identificacion de las clases, atributos y metodos
1. ![image](https://github.com/user-attachments/assets/b3398e77-8732-43fa-b05c-596f88762900)   2. ![image](https://github.com/user-attachments/assets/0c6800a7-66e5-42ea-8e1b-2bc1b65b5fdd)   3. ![image](https://github.com/user-attachments/assets/8713c935-16e8-406c-a261-aa2f4136d7c7)   4. ![image](https://github.com/user-attachments/assets/096fdfa8-cf31-4c58-b5f6-7dcf21470160)   5. ![image](https://github.com/user-attachments/assets/6a0aa8b7-6fed-4701-bf05-85223304d46f)

Visualizar el boceto inicial en [linea](https://drive.google.com/file/d/1KmyeonzRwn870MeYciVwaSlAxfXEdGyh/view?usp=sharing)
