# Proyecto de Control de Actividades (Tracking) :hourglass_flowing_sand:
Tracking es una aplicación de control de actividades, en el que nos ayudará a tener un mejor manejo diario de las metas que se desea realizar en el día.
Este Tracking nos permitirá llevar un registro en una base de datos de cada uno de los objetivos que fueron agregados, se mostrará la meta que se insertó, la fecha con su respectiva hora y si se logró cumplir con lo deseado.

A continuación, se les mostrará un grafico en base al UML del proyecto (Control de Actividades o Tracking):

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/UML_Tracking.jpg)

### Actividad

Como podemos observar la clase **Actividad** es la clase padre y hereda sus atributos (meta, prioridad, duracion, animo) a sus descendientes **Estudio y Personal**.

<ins>Propósito de los atributos de la clase padre Actividad</ins>:
* **meta**: Se agregará uno o mas objetivos  que desea cumplir en el día.
* **prioridad**: Se le indicará de que nivel de importancia de dicho objetivo.
* **duracion**: Se determinará cuanto tiempo se duró en los objectivos.
* **animo**: Se podrá comentar el ánimo de haber realizado las metas.

Se utilizó los métodos **get** para que los atributos se muestren y el método **set** para modificar los atributos que pueden llegar a cambiar en ciertos momentos.

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Actividad.jpg)

### Estudio

En seguida podemos ver que en la clase **Estudio** se le agregaron dos atributos mas (materia, tarea), sin eliminar ni modificar los atributos que la clase **Actividad** le heredó.

<ins>Propósito de los atributos de la clase Estudio</ins>:
* **materia**: Se indica el tema del proyecto de estudio.
* **tarea**: Se comenta cuál es la intención del estudio (repaso, examen, tarea etc.)

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Estudio.jpg)

### Personal

La clase **Personal** al igual que **Estudio** se le añadieron dos atributos más (ejercicio, hogar) aparte de los que la clase padre (Actividad) le heredó.

<ins>Propósito de los atributos de la clase Personal</ins>:
* **ejercicio**: Se le agregará los datos del tipo de ejercicios que se realizó (pesas, cardio, caminar, etc.)
* **hogar**: Se comentará que labores del hogar o personales se efectuó.

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Personal.jpg)

### BitacoraTracking

Por último vamos analizar la clase BitacoraTracking, dicha clase no esta ligada o relacionada directamente de la clase padre Actividad, por eso observamos que no esta heredando ningún atributo, así teniendo sus propios atributos que serán agregados en el registro como información adicional a los atributos anteriores.
Se utilizó los métodos **get** para que los atributos se muestren.

<ins>Propósito de los atributos de la clase BitacoraTracking</ins>:
* **actividad**: En este atributo se llamara la clase padre **Actividad** para que los datos se lleguen a relacionar.
* **fecha**: Java proporciona una clase de fecha bajo el paquete java.util, así es cómo obtendremos la fecha actual.
* **realizado**: Es un atributo de tipo de dato, en donde se llama boolean y puede almacenar unicamente dos valores: verdadero o falso. Es decir que en esta opción se seleccionará si la meta se cumplió o no.

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/BT.jpg)

##Ejemplo

En seguida se mostrará un ejemplo de como llenar la información con la explicacioón anterior:

En la primera escena se registro la información en cada uno de los atributos, siendo:
**Meta**: Estudio  |  **Ánimo**: Tranquila  |  **Prioridad**: Alta  |  **Duracion**: 7
**Es Estudio?**: Se seleccionó la opción porque la meta es en base a Estudio.
**Materia**: Java  |  Tarea: Proyecto  |  **Realizado**: Se selccionó porque se cumplió los objetivos en el día.

** La opción <ins>Es Estudio?</ins>, al seleccionarlo se mostrará solo los atributos que estan relacionados con el <ins>Estudio (materia, tarea)</ins>, y al no seleccionarlo se desplegará los atributos de <ins>Personal</ins>.**

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Ejemplo_Estudio.jpg)

El resultado de dicha información se registró de la siguiente manera:

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/registro_estudio.jpg)

**Se muestra True porque la meta fue exitosa**

En esta escena se presentará la información en base a los atributos de la clase Personal:

**Meta**: Ejercicio y Limpieza  |  **Ánimo**: Triste  |  **Prioridad**: Medio  |  **Duracion**: 0
**Es Estudio?**: No se seleccionó la opción porque la meta es en base a Personal.
**Ejercicio**: 0  |  Hogar: 0  |  **Realizado**: No se seleccionó la opcioón porque no se cumplió la meta.

**Al no haberse cumplido la meta se decidió llenar la información <ins>Ejercicio y Hogar</ins> en 0 porque no se completó ninguna de ellas**

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Ejemplo_Personal.jpg)

El resultado de dicha información se registró de la siguiente manera:

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/Personal_registro.jpg)

**Se muestra False porque la meta no se completó**


### Importante
Al ingrsar en la opción **Duración** informacioón que no sea un numero entero, se mostrará un error con la falla como el siguiente:

![Image text](https://github.com/Laura27-89/Project/blob/main/src/com/ucreativa/imagenes/error.jpg)




