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
1. El personal autorizado ingresa al sistema mediante su usuario y contraseña
2. El sistema verifica las credenciales y permite el acceso
3. El personal autorizado va hacia el apartado de gestión de pacientes
4. Selecciona la opción "Registrar paciente"
5. El sistema muestra un formulario para completar con los datos personales del paciente
6. Ingresa los datos personales del paciente: nombre completo, DNI, fecha de nacimiento, telefono, mail, etc
7. El sistema valida cada campo: formato, campos obligatorios, datos duplicados
8. Si hay errores, muestra mensajes específicos y permite corregirlos.
9. Una vez todos los datos están validados, el personal hace clic en "Guardar"
10. El sistema almacena los datos en la base de datos
11. Se muestra un mensaje de confirmación del registro exitoso
* Precondiciones: el personal autorizado debe estar registrado
* Postcondiciones: el paciente queda registrado en el sistema


__2do caso de uso__
* Nombre: Agendar un turno
* Actores involucrados: personal autorizado, paciente
* Descripcion: permite asignar un turno a un paciente 
* Flujo principal de eventos:
1. El paciente solicita un turno, ya sea presencial o por llamada
2. El personal autorizado accede al sistema
3. Va hacia el apartado de turnos
4. Verifica que el paciente este registrado en el sistema
5. En caso de no estarlo, se sugiere registrarlo previamente
6. Selecciona al paciente desde una lista o buscador despues de validar que esta registrado
7. Se abre una vista con los medicos disponibles
8. El personal autorizado consulta la disponibilidad de los medicos
9. Se selecciona el médico según especialidad o preferencia del paciente
10. Se elige una fecha y hora entre los horarios disponibles
11. Se ingresa el motivo de la consulta o atencion
12. El sistema valida que el turno no este duplicado ni se superponga
13. El turno se agenda y queda con estado "pendiente"
14. El sistema genera una notificacion con los detalles del turno
15. Se envia dicha notificación al paciente y al medico, por email o mensaje interno del sistema
* Precondiciones: el paciente tiene que estar registrado en el sistema
* Postcondiciones: el turno queda agendado con estado "pendiente"

__3er caso de uso__
* Nombre: confirmar turno
* Actores involucrados: personal autorizado, paciente, medico
* Descripcion: permite que el paciente confirme el turno que se le asigno
* Flujo principal de eventos:
1. El personal autorizado accede al sistema
2. Va hacia el apartado de agenda de turnos
3. Filtra los turnos por estado “pendiente”
4. Busca y selecciona el turno correspondiente
5. Se visualizan los detalles del turno (paciente, medico, fecha, hora, motivo)
6. El sistema solicita confirmacion del paciente (puede ser presencial, llamada u otro medio)
7. El personal hace clic en la opción "Confirmar turno"
8. El sistema actualiza el estado del turno a "confirmado"
9. Se registra la fecha y hora de confirmacion
10. Se notifica al paciente y al medico el cambio de estado
11. Se actualiza la agenda de turnos en tiempo real
* Precondiciones: el paciente debe tener un turno asignado con estado "pendiente"
* Postcondiciones: el estado del turno cambia a "confirmado"

__4to caso de uso__
* Nombre: cancelar turno
* Actores involucrados: personal autorizado, paciente, medico
* Descripcion: permite que el paciente cancele el truno que se le asigno
* Flujo principal de eventos:
1. El personal autorizado ingresa al sistema
2. Va hacia el apartado de agenda de turnos
3. Filtra los turnos por estado "confirmado"
4. Selecciona el turno a cancelar
5. El sistema muestra los detalles del turno y un boton para cancelar
6. Se despliega una ventana de doble confirmación con motivo de cancelacion
7. El personal confirma la cancelacion
8. El sistema actualiza el estado del turno a "cancelado"
9. Se registra la fecha, hora y motivo de la cancelacion
10. Se notifica al paciente y al medico sobre la cancelacion
11. Se libera el horario en la agenda del medico para futuros turno
* Precondiciones: el turno debe tener un estado de "confirmado"
* Postcondiciones: el turno cambia de estado a "cancelado" y se libera el horario de dicho turno

__5to caso de uso__
* Nombre: historial de turnos del paciente
* Actores involucrados: personal autorizado, medico
* Descripcion: permite ver el historial de los turnos que tuvo y tendra un paciente
* Flujo principal de eventos:
1. El personal autorizado accede al sistema
2. Va hacia el apartado de modulo de pacientes
3. Utiliza el buscador para localizar al paciente (DNI, nombre, etc)
4. Selecciona la opcion "ver historial de turnos"
5. El sistema muestra una lista de turnos pasados y futuros del paciente
6. Cada turno se muestra con el estado, fecha, hora, médico y motivo
7. Se habilitan filtros por fechas, estado, especialidad, medico, etc
8. El sistema permite exportar el historial en PDF o imprimirlo
* Precondiciones: el paciente tiene que estar registrado en el sistema
* Postcondiciones: se muestra el historial de turnos en pantalla con la opcion de poder exportarlo
  
## Boceto inicial del diseño de clases
Identificacion de las clases, atributos y metodos
1. ![image](https://github.com/user-attachments/assets/6b7a1290-6297-4de1-b9b4-4914560ab5b3)
2. ![image](https://github.com/user-attachments/assets/02340d58-21a3-46a6-9dcc-b0bd723c5874)
3. ![image](https://github.com/user-attachments/assets/c6f207ee-51cf-4b52-ae52-0c0f3caa1033)
4. ![image](https://github.com/user-attachments/assets/33f6308f-53a3-4543-bf5b-d7c8691eed8f)
5. ![image](https://github.com/user-attachments/assets/239831c3-8abb-441b-a9dd-4696b44ca0c1)


[Visualizar en linea](https://drive.google.com/file/d/1KmyeonzRwn870MeYciVwaSlAxfXEdGyh/view?usp=sharing)

