# INDICE

[TOC]

# PREAMBULO

# DEFINICIONES

## AFILIADO

## DERECHO DE SUFRAGIO PASIVO

## LISTA ELECTORAL

## LISTADO DE REFERENCIA DE AFILIADOS

# ELABORACION DEL LISTADO DE REFERENCIA DE AFILIADOS

## CONTENIDO DE LA LISTA

### Articulo 1. Información de afiliado contenida en la lista

El listado estará formado por el numero de cada afiliado en una lista ordenada, exclusivamente, sin ningún tipo de información personal adicional.

### Articulo 2. Afiliados que pueden formar parte de la lista

La lista estará formada por aquellos militantes del partido que lo fueran en la semana previa a la elaboración del listado.

Los afiliados que se den de alta en la semana previa a la elaboración del listado no formarán parte de la elaboración de la lista y deberán esperar, no más de tres meses y una semana, a la elaboración del siguiente listado. 

La generación de una nueva lista invalida las listas anteriores para generar nuevas candidaturas a partir de la fecha de generación de la última lista.

## PERIODICIDAD DE LA ELABORACION DEL LISTADO

### Articulo 3. Periodicidad mínima

El listado se elaborará con una periodicidad mínima de 3 meses

### Articulo 4. Notificación de elaboración del listado

Con al menos una semana de antelación se notificará a los afiliados la fecha en la que se creará un nuevo listado de referencia de afiliados

## PROCESO DE ELABORACION DEL LISTADO

### Articulo 5. Responsable de la elaboración de listado 

El responsable de la elaboración de listado de referencia será el Responsable General de Organización y Campaña, miembro del Consejo Ejecutivo.

### Articulo 6. Algoritmo de mezclado

Se usara un algoritmo determinístico que en función de la lista de entrada ordenada por numero de afiliado y una clave de mezclado, obtenga la lista mezclada. 

Las potenciales mezclas, que dependen de las potenciales claves, deben ofrecer una probabilidad similar a todos los elementos de la lista de ocupar una determinada posición en la lista mezclada.

El grado de similitud en las probabilidades debe ser inferior a la mitad de la probabilidad de un sistema perfectamente aleatorio. De manera mas precisa, siendo N el numero de elementos en la lista y P(i,j) = probabilidad de que el elemento en la posición i termine en la posición j, entonces para todo i,j,k,l desde la posición 1 hasta la posición N
$$
|P(i,j)-P(k,l)|<1/(2N)
; P(i,j)>=1/(2N)
$$
Se usara python3 con la librería random que implementa el algoritmo Fisher-Yates en un entorno controlado que será publicado, este algoritmo podra ser revisado y actualizado, para mejorar la igualdad de probabilidades y la reproducibilidad

```python
import random
random.Random(clave).shuffle(listaDeEntrada)
```



### Articulo 7. Clave de mezclado

La clave de mezclado se generara concatenando:

* El día, mes y año en que se realiza el listado
* El primer premio del sorteo de Lotería Nacional del sábado anterior al día en el que se realiza el listado
* El segundo premio del sorteo de Lotería Nacional del sábado anterior al día en el que se realiza el listado. 

Por ejemplo si el listado se elabora el 19 de julio de 2019 la clave a usar será:

**190720190213730376**

ya que el día es **19**, el mes es **07** y el año es **2019**, el primer premio del sabado 13 de julio fue **02137** y el segundo premio del sabado 13 de julio fue **30376**

## PUBLICIDAD DEL LISTADO

### Articulo 8. Elementos a publicar

Una vez elaborado se publicara:

* El listado de entrada
* La clave utilizada
* El listado de salida
* Firma digital del Responsable General de Organización y Campaña

### Articulo 9. Visibilidad de la información

Los listados estarán disponibles vía web para los afiliados del partido

### Articulo 10. Impugnación del listado

El plazo para impugnar un listado será de 5 días a partir de su publicación. Y se podrá impugnar en el caso de que se detectase que el algoritmo no es determinista o que el algoritmo de mezclado no de una probabilidad similar a los afiliados tal y como se describe en el Articulo 6

El listado quedará impugnado por el Responsable General de Organización y Campaña o el Coordinador General, debiéndose publicar el estudio que verifique esa situación e indicar que el listado ha sido impugnado.

La impugnación del listado implicará la creación de una lista de referencia temporal para lo cual, se tomará la lista de entrada, siendo N el numero de afiliados en la lista de entrada y C la clave, se tomará como primera entrada en la lista de salida (C mod N)+1 y a partir de ahí en adelante hasta llegar a la posición N (ultima en la lista), y a partir de ahí de la posición 1 hasta la posición (C mod N)



# ELABORACION DE LA LISTA ELECTORAL

## FASE 1 - CREACION DE LAS LISTAS BASES

### Articulo 11. Creación de listas bases

El Responsable General de Organización y Campaña creara las listas bases al día siguiente de la convocatoria de elecciones.

### Articulo 12. Ámbitos de listas bases

Se elaborara una lista base por cada ámbito(nacional, autonómico, loca u otro) y por cada circunscripción 

### Articulo 13. Contenido de las listas bases

La lista base por cada circunscripción y ámbito estarán formadas por los números de afiliados de aquellos afiliados que pertenecen a la circunscripción ordenados según el listado de referencia vigente en el día de la convocatoria de elecciones

### Articulo 14. Publicación y notificación de las listas bases

El Responsable General de Organización y Campaña publicará las listas bases, visibles a todos los afiliados, y notificará a los afiliados que se encuentren en ellas, con instrucciones en cuanto a la exclusión voluntaria y la selección en concurrencia de listas.

## FASE 2 - MODIFICACIONES VOLUNTARIAS DE CANDIDATOS

### Articulo 15. Exclusión voluntaria

El afiliado que por voluntad propia no quiera o pueda ser candidato en uno o varios ámbitos, podrá notificar al Responsable General de Organización y Campaña su voluntad en el plazo de 10 días a partir de la publicación de las listas base.

El no participar en la exclusión voluntaria no obligará a la inclusión en la lista electoral, ya que en la fase de elaboración de la lista definitiva se requiere el consentimiento expreso por parte del candidato.

### Articulo 16. Modificación voluntaria

El afiliado que esté en alguna lista base que no corresponda a su lugar de empadronamiento, por haberlo cambiado y no notificado al partido, podrá notificar al Responsable General de Organización y Campaña su voluntad de cambiar de lista en el plazo de 10 días a partir de la publicación de las listas base.

## FASE 3 - SELECCION DE LISTA EN CONCURRENCIA DE PROCESOS ELECTORALES

### Articulo 17. Selección voluntaria

El afiliado que concurra en múltiples listas podrá notificar al Responsable General de Organización y Campaña su voluntad en el plazo de 10 días a partir de la publicación de las listas base en qué lista quiere estar presente, excluyéndose voluntariamente de las otras.

### Articulo 18. Selección por defecto

Si el afiliado que concurre en múltiples listas no notifica al Responsable General de Organización y Campaña su voluntad en el plazo de 10 días a partir de la publicación de las listas base, se dejará en manos del Responsable de Organización y Campaña la selección de la lista en la que participar, como parte del proceso de elaboración de la lista definitiva.

## FASE 4 - ELABORACION DE LA LISTA DEFINITIVA

### Articulo 19. Responsable

El responsable de la elaboración de las listas es el Responsable General de Organización y Campaña.

### Articulo 20. Plazos

La elaboración de las listas definitivas dará comienzo a los 11 días de la publicación de las listas bases y deberá realizarse en menos de 10 días.

### Articulo 21. Orden de Ámbitos

En el caso de concurrencia de elecciones, los listados definitivos se irán realizando de mayor a menor ámbito, primero nacional, segundo autonómico y tercero local.

### Articulo 22. Orden de Candidatos

El orden de candidatos será el que aparezca en las listas base, excluyendo a aquellos candidatos que ya se hayan seleccionado en un ámbito mayor.

Como orden principal se establecerá alternancia a partir del primer candidato verificado entre hombres y mujeres.

Por ejemplo en una lista formada por 1-M,2-M,3-H,4-M,5-M,6-H,7-H,8-H y asumiendo que todos quieren ser candidatos y cumplen los requisitos el orden de candidatos será: 1-M,3-H,2-M,6-H,4-M,7-H,5-M,8-H

### Articulo 23. Verificación del Candidato

El Responsable General de Organización y Campaña deberá verificar en base a los datos disponibles por el partido:

* Que está al corriente de pago
* Que pertenece a la circunscripción indicada
* Que tiene derecho de sufragio pasivo para las elecciones en las que es candidato

### Articulo 24. Consentimiento expreso del Candidato

El Responsable General de Organización y Campaña deberá aportar al candidato:

* Reglamento de Personas Electas
* Requisitos legales para ser candidato

El Responsable General de Organización y Campaña deberá obtener del candidato:

* Consentimiento a ser Candidato
* Documentación requerida por los organismos electorales para ser candidato
* Promesa de cumplir con los requisitos legales para ser candidato
* Compromiso a cumplir el Reglamento de Personas Electas en caso de salir elegido
* Curriculum Vitae actualizado y consentimiento para su publicación una vez entrada en campaña
* Áreas de interés en el ámbito político si las hay y consentimiento para su publicación una vez entrada en campaña

### Articulo 25. Cierre de Listas

Una vez que se obtenga un número de candidatos igual al numero de puestos o escaños menos uno, o se agoten los afiliados de la lista base, el Responsable General de Organización y Campaña cerrará la lista y la hará pública.

# PRESENTACION DE LA LISTA ELECTORAL

### Articulo 26. Información del proceso

El Responsable General de Organización y Campaña en base a la legislación aplicable informará al partido de los pasos a seguir, incluyendo la obtención de avales, para presentar la lista electoral.

### Articulo 27. Avales de la lista electoral

En caso de ser necesario avales, los afiliados de una determinada circunscripción deberán avalar las listas presentadas.

El Responsable General de Organización y Campaña publicará los medios mediante los cuales se pueden avalar las listas electorales, incluyendo información de contacto de los afiliados que compongan la lista electoral.

### Articulo 28. Presentación de listas

La presentación de las listas y la documentación pertinente se realizará por el Responsable General de Organización y Campaña o en su defecto las personas seleccionadas por esta para realizarlo.

