# INDICE

[TOC]

# PREAMBULO

# DEFINICIONES

## CENSO

## VOTANTE

## CANDIDATO

## PAPELETA

## VOTO

## VALIDACION 

## EVENTO

## APODERADO

## FIRMA ELECTRONICA

## FIRMA ELECTRONICA CIEGA

## ENCRIPTACION

## DESENCRIPTACION

# PROCESO DE VOTACION

## EVENTO

### Articulo 1. Organización del Evento 

 El Consejo Ejecutivo será el responsable de la organización de los eventos de votación.

 Por cada evento nombrará una junta electoral, formada por 3 personas, que ejecutará el evento de votación.

 Los eventos tendrán una dirección física donde votar y permitirán el voto remoto

### Articulo 2. Notificación del Evento 

 La notificación de los eventos de votación se realizarán con al menos 10 días antes del inicio de censo asociado al proceso de votación.

 En una misma notificación se pueden incluir múltiples eventos.

### Articulo 3. Fases del Evento 

 Cada evento de votación tendra 3 fases que se realizarán en el siguiente orden:

1. Establecimiento del Censo. En el cual las personas afiliadas que quieran votar lo hacen saber, se verifica el cumplimiento de requisitos como votante y se le asignan los recursos tecnicos para poder realizar la votacion
2. Establecimiento de Validaciones. En el cual las personas afiliadas presentan de manera anonima pero verificable la información necesaria para poder verificar que su voto se contabilice y que no se haya producido una alteración del censo 
3. Votación. En el cual las personas afiliadas presentan su voto de manera anonima pero verificable mediante las validaciones establecidas previamente.

  Para un mismo evento no se podrá iniciar una fase sin haber finalizado la fase previa.

### Articulo 4. Detalles del Evento 

  El Consejo Ejecutivo presentara en la notificación la siguiente información por cada evento:

* Identificador del evento
* Propuesta detallada sometida a votación
* Miembros de la junta electoral y mecanismo de contacto
* Dirección del censo (URL censo)
* Fecha y hora de inicio censo
* Fecha y hora de fin de censo
* Dirección de validación (URL censo)
* Fecha y hora  de inicio de validación
* Fecha y hora de fin de validación
* Dirección de voto (URL y dirección física)
* fecha y hora de inicio de voto
* fecha y hora de fin de voto
* Formato de la papeleta
* Formato de la validación de la papeleta
* Algoritmo a usar en la encriptación por parte del votante
* Algoritmo a usar en la firma por parte del votante
* Algoritmo a usar en la firma por parte del censo

### Articulo 5. Tipos de Evento 

  Se definen 2 tipos de eventos de votación

- Votación a favor o en contra de una propuesta
- Selección de una entre varias propuestas

## FASE DE ESTABLECIMIENTO DEL CENSO

### Articulo 6. Inicio de la fase de censo 

  En la fecha y hora indicadas en el evento se permitirá la entrada de peticiones por parte de las personas afiliadas en la URL del censo, así mismo se ofrecerá la información para verificación de firma del censo.

### Articulo 7. Peticiones de censo 

  Cada persona afiliada realizará una única petición al censo que constara de 2 mensajes:

* Papeleta encriptada y firmada por la persona afiliada
* Validación de la papeleta encriptada y firmada por la persona afiliada 

   Una vez verificados los requisitos el censo devolverá una única respuesta que constará de 2 mensajes:

* Papeleta encriptada y firmada en ciego por el censo
* Validación encriptada y firmada en ciego por el censo

   Además incluirá el identificador de persona afiliada en un listado publico de censo junto con la Papeleta encriptada y firmada por la persona afiliada. El listado publico del censo ira firmado por el censo cada 1000 entradas.

### Articulo 8. Verificación de requisitos

  El censo verificará que:

* La persona que realiza la petición esta afiliada al partido y al corriente del pago de sus obligaciones.
* El formato de la información recibida se ajusta a lo esperado según los detalles del evento
* La firma de la papeleta encriptada corresponde con la persona afiliada
* La firma de la validación de papeleta encriptada corresponde con la persona afiliada
* La persona afiliada no ha realizado una petición previa al censo para este evento

En caso de que los requisitos no se cumplan se responderá a la petición con un mensaje firmado por el censo indicando el requisito no cumplido así como información adicional.

### Articulo 9. Fin de la fase de censo 

  En la fecha y hora indicadas en el evento como cierre no se permitirá la entrada de mas peticiones en la URL del censo

  La información para verificación de firma del censo así como el listado publico de censo generado seguirán estando disponibles.

### Articulo 10. Revisión del listado público de censo 

  Cualquier persona podrá acceder la listado público del censo y verificar:

* Que cada 1000 entradas están firmadas por el censo, esta validación la realizará también la junta electoral. En caso de que haya entradas no firmadas por el censo se invalidará el evento.
* Que cualquier entrada esta firmada por el afiliado que la realizó, esta validación la realizará también la junta electoral
* Que la entrada correspondiente a uno mismo esta presente

### Articulo 11. Alegaciones e incidencias  de censo 

  Cualquier afiliado podrá notificar las siguientes incidencia detectada a la junta electoral:

* La firma de una entrada no corresponde con la de la persona afiliada. En ese caso, tras verificar la veracidad de la incidencia, se invalidará la entrada
* No se encuentra la entrada correspondiente a una persona afiliada. La persona afiliada debe aportar la Validación encriptada y firmada en ciego por el censo. En ese caso,  tras verificar la veracidad de la incidencia, se añadirá la entrada

Las entradas añadidas o invalidadas se harán constar en otro listado publico firmado por la junta electoral

## FASE DE ESTABLECIMIENTO DE VALIDACIONES

### Articulo 12. Inicio de la fase de validaciones

### Articulo 13. Entrada de validaciones

### Articulo 14. Verificación de entradas de validaciones

### Articulo 15. Fin de la fase de entrada de validaciones

### Articulo 16. Revisión del listado de validaciones

### Articulo 17. Alegaciones e incidencias en la fase de validaciones

## FASE DE VOTO

### Articulo 18. Inicio de la fase de voto

### Articulo 19. Entrada de votos

### Articulo 20. Verificación de entrada de votos

### Articulo 21. Fin de la fase de entrada de votos

### Articulo 22. Revision de votos

### Articulo 23. Alegaciones e incidencias en la fase de votos

### Articulo 24. Presentación de resultados

# LISTADOS ASOCIADOS AL EVENTO

## LISTADO PUBLICO DE CENSO

### Articulo 25. Estructura del listado de censo

### Articulo 26. Publicidad y Mantenimiento del listado de censo

## LISTADO PUBLICO DE VALIDACIONES

### Articulo 27. Estructura del listado de validaciones

### Articulo 28. Publicidad y Mantenimiento del listado de validaciones

## LISTADO PUBLICO DE VOTOS

### Articulo 29. Estructura del listado de votos

### Articulo 30. Publicidad y Mantenimiento del listado de votos

### Articulo 31. Publicidad y Mantenimiento del resultado de la votación

# ALGORITMOS CRIPTOGRAFICOS

## FIRMA

### Articulo 32. Algoritmos de firma de censo

### Articulo 33. Algoritmos de firma de junta electoral

### Articulo 34. Algoritmos de firma de votantes

## ENCRIPTACION Y DESENCRIPTACION

### Articulo 35. Algoritmos de encriptación y desencriptación de votantes

## HASH

### Articulo 36. Algoritmos de Hash

