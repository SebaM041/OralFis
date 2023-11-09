# <ins>Glosario:</ins>

# <ins>Comandos GIT:</ins>

- git clone "Clona el repositorio a local lo utilizamos para clonar el repositorio cada vez que trabajamos en una computadora distinta"
- git merge "Fusiona 2 ramas conservando los cambios que se indiquen, lo utilizamos para luego de trabajar en nuestra rama personal, pasar esos cambios a la rama principal"
- git commit "Guarda los cambios en el repositorio local"
- git push "Envia el ultimo commit al repositorio remoto"
- git add . "Añade los ultimos archivos y cambios al dominio del commit"
- git branch "Crea una nueva rama a partir de la rama en la que se encuentra, lo utilizamos para crear las ramas Seba y Emi"
- git checkout "Se mueve a la rama designada, lo utilizamos a la hora de movernos entre ramas"
- git status "Devuelve informacion de la diferencia de estado entre la actualidad y el ultimo commit"
- git log "Devuelve un historial de cambios"
- git pull "Traer la ultima version remota al repositorio local, lo utilizamos a la hora de trabajar en conjunto para poder recibir los cambios de el otro integrante"

# <ins>Versionado: </ins>

### Buenas practicas :

Utilizamos Git para la el versionado y Github como herramienta para el uso de repositorios remotos

Nos dividimos en 2 ramas, una para cada integrante en la que cada uno hiciera sus respectivos commits para luego tomar decisiones antes de cada merge

Para los commits se utilizaria "feature: descripcion" para agregar algo y "fix: descripcion" para correciones


 ### Resumen de commits

 A contunuacion les dejamos una screenshot con la evolucion de los commits y merges

 # <ins>Elicitacion:</ins>

 #### Investigacion:

 Investigacion:
 
Aprovechando que nosotros mismos somos parte del público objetivo de nuestra aplicación nos pusimos a observar como eran nuestras salidas con amigos para así poder encontrar funcionalidades para nuestra aplicación

Principalmente viendo que problemas nos encontrábamos a la hora de salir con nuestros amigos, como por ejemplo no contar con el dinero para poder pagar el producto y tener que esperar, pasar cuentas de banco todo el tiempo, pagar comisiones de uno a otro, problemas de deudas que pueden afectar relaciones etc

![Imgur](https://i.imgur.com/nJv4zXa.png)

Como se puede ver en las capturas es un problema muy común en mi grupo y que termina en que alguien tenga que pagar por otro.

1.	Se puede observar como “franki” expresa la necesidad de que se le ingrese el dinero lo antes posible ya que sin el no podría hacer la compra expresando también que no tiene el dinero como para poner por los demás 
2.	Podemos ver las complicaciones que lleva pagar las cosas en efectivo en este caso temas de cambio
3.	El contexto de esta imagen es que paso mucho tiempo desde la deuda hasta el pago ya que no se tenia cuenta en el mismo banco, con nuestra app no habría problema en este sentido
4.  Relacionada de la imagen 1
5.	Podemos ver como las deudas de una noche se van aplazando para después 
6.	Acá podemos ver la razón principal de nuestra app, una persona teniendo que pagar por todos para después sufrir la espera de que uno por uno los deudores paguen


#### Entrevista:


Realizamos una entrevista a uno de nuestros compañeros (Manuel Graña) que consideramos entraría dentro de nuestro publico objetivo. Hablamos con el acerca de sus experiencias en situaciones de salidas y como se maneja el a la hora de pagar los gastos con amigos.
Esta entrevista sirvió para tener otro punto de vista pero a la vez confirmo en gran parte nuestros supuestos, a continuación algunas de las preguntas mas importantes y lo que pudimos extraer de ellas.

##### Pregunta 1)

¿A la hora de salir hay algún inconveniente que se te haga habitual? 
En esta pregunta surgió una charla variada pero lo relevante para nosotros fue lo siguiente
“también me pasa que pagar es un quilombo, no queremos molestar a la moza pidiéndole que divida mucho la cuenta entonces suele pagar todo uno, y cuando no te toca ser el que paga no es mucho problema vos haces una transferencia y te olvidas, pero cuando te toca ser el que paga es un problema, tenes que andar atrás de el resto para que te paguen y la verdad que eso a veces es para problemas”

##### Conclusión:

Esto nos confirmo la necesidad de nuestra app y que la idea iba bien encaminada además de que una de las necesidades era como transferir la plata de esa cuenta común a un local como un restaurante

##### Pregunta 2)

¿Y estos problemas relacionados a el dinero se dan solo en salidas a comer?
“En realidad se dan en muchas situaciones, por ejemplo cuando nos juntamos para hacer un asado, la persona que lo compra tiene que pagar porque la gente no suele transferir antes de el día y esto es un problema porque uno termina poniendo mas y se vuelve a dar el problema de esperar por los demas”

##### Conclusión:

La aplicación no debía orientarse solo a pagar a un restaurante sino también a pagarle a una persona particular o que esta persona pudiera usar la app para pagar en un supermercado, carniceria, etc.
Esto nos dejo pensando cual seria el método mas eficiente para extraer dinero del fondo


#### Lluvia de ideas:
A partir de la entrevista y nuestra investigación hicimos una lluvia de ideas para poder discutir cuales habían sido nuestras conclusiones individuales, las cuales fueron:

- La necesidad de lograr solucionar el problema con gran comodidad, ya nuestra app no es la única solución a el problema, pero queremos que sea la mas cómoda, por lo tanto decidimos agregar cosas como la lista de amigos para facilitar la creación del fondo

- Debía haber una forma para pagar tanto en efectivo como online, por lo que decidimos que se pueda usar tanto un QR de un local como transferir a una cuenta por lo que optamos por asociarla a mercado pago que soluciona las 2 cosas a través del QR

- Necesitábamos poder tener una noción de los gastos realizados, por lo que decidimos agregar un historial de pagos en la aplicación 

- Queríamos poder pagar desde varios métodos por lo que optamos que aunque la salida de la cuenta será por mercado pago la entrada pudiera ser a través de múltiples plataformas


# <ins> Modelado de usuarios: </ins>

![Imgur](https://i.imgur.com/Rk9TxDS.jpg)

![Imgur](https://i.imgur.com/doPSG7y.jpg)

<!---  
TODO : PRUEBA
!-->
 

# <ins>Especificacion: </ins>

#### User Stories:

**ID #1:**

**Titulo:** Creación de fondo compartido

**Narrativa:** Yo como usuario quiero poder crear un nuevo fondo compartido con su respectivo nombre y descripción y eligiendo un monto inicial

**Criterios de aceptación:**
- El nombre del fondo no puede ser vacio y debe tener un máximo de 20 caracteres
- La descripción puede ser o no nula
- El monto debe ser mayor a 0

**ID #2:**

**Titulo:** Ingresar dinero al fondo

**Narrativa:** Como usuario debo poder agregar dinero al fondo desde varios métodos de pago distintos como mercadopago, paypal, tarjeta o una red de cobranza 

**Criterios de aceptación:** 

- El monto a ingresar debe ser menor al monto faltante en el fondo
- Debe aceptar tarjeta de múltiples servicios financieros(Visa, Mastercard, Oca, etc)

**ID #3:**

**Titulo:** Pagar con el fondo 

**Narrativa:** Como usuario quiero poder utilizar los fondos compartidos para pagar una cuenta o producto con una confirmación previa de los usuarios que son parte del fondo utilizando un escáner de qr desde la aplicación.

**Criterios de aceptación:**
- Todos los usuarios deben aceptar para liberar los fondos
- El monto a pagar debe ser menor a el monto del fondo

<!---
BUG: ERROR 
!-->





**ID #4:**

**Titulo:** Agregar amigos a la lista

**Narrativa:** Como usuario quiero poder agregar amigos a partir de un link o nombre de usuario para agregarlos a mi lista y facilitar su agregación a futuros fondos
**Criterios de aceptación:**

- El nombre a buscar debe ser valido
- A partir del link debo poder encontrar y agregar al usuario

**ID #5:**

**Titulo:** Agregar amigos al fondo

**Narrativa:** Como usuario quiero poder seleccionar amigos de mi lista para poder agregarlos al fondo

**Criterios de aceptación:**

- El usuario debe poder acceder a su lista de amigos o contactos dentro de la aplicación.
-El sistema debe proporcionar una función de búsqueda que permita al usuario encontrar amigos específicos en su lista

**ID #6:**

**Titulo:** Revisar el historial de gastos

**Narrativa:** Como usuario quiero poder ver el historial de pagos para poder controlar mis gastos

**Criterios de aceptación:**

- El usuario debe poder acceder a una lista con todos los gastos que a hecho.
- Se debe ofrecer un sistema de paginado para poder organizar asi el historico.

#### Casos de uso:


##### Caso 1:

**Titulo:** Agregar un amigo

**Actor:** Usuario

**Curso Normal:**
| Accion de los actores                     | Respuesta del sistema                                  |
|-------------------------------------------|--------------------------------------------------------|
| 1. El usuario ingresa a la seccion de amigos | 2. Sistema muestra la seccion de amigos                |
| 3. El usuario presiona el boton de mas       | 4. Sistema abre pestaña para insertar datos de usuario |
| 5. El usuarios ingresa datos                 | 6. Sistema agrega usuario a la lista de amigos         |


**Curso Alternativo:**
| Accion de los actores                          | Respuesta del sistema                                         |
|------------------------------------------------|---------------------------------------------------------------|
| 5.1 El usuario no ingresa los datos pero envia | 5.2 El sistema notifica al usuario que falta rellena un campo |



##### Caso 2:

**Titulo:** Crear fondo 

**Actor:** Usuario

| Accions de los actores                     | Respuesta del sistema                                                 |
|--------------------------------------------|-----------------------------------------------------------------------|
| 1. El usuario ingresa a la seccion fondos  | 2. Sistema muestra la seccion de fondos                               |
| 3. El usuario presiona el boton mas           | 4. Sistema abre pestana para ingresar  Nombre y descripcion del fondo |
| 5. El usuario ingresa los datos               | 6. Sistema agrega el fondo                                            |

**Curso Alternativo:**
| Accions de los actores                          | Respuesta del sistema                                      |
|-------------------------------------------------|------------------------------------------------------------|
| 5.1 El usuario no ingresa algun dato pero envia | 5.2 El sistema notifca al usuario que falta rellenar campos |

##### Caso 3:

**Titulo:** Agregar amigos al fondo

**Actor:** Usuario

**Curso Normal:**
| Accions de los actores                       | Respuesta del sistema                              |
|----------------------------------------------|----------------------------------------------------|
| 1. El usuario entra al fondo                 | 2. Sistema muestra la interfaz del fondo           |
| 3. El usuario selecciona el boton de agregar | 4. Sistema muestra la lista de amigos del ususario |
| 5. El usuario elige un amigo de la lista     | 6. Sistema agrega al amigo al fondo                |

**Curso Alternativo:**

4.1) La lista esta vacia por lo que se muestra un mensaje con el aviso respectivo




##### Caso 4:

**Titulo:** Ingresar dinero al fondo

**Actor:** Usuario

**Curso Normal:**

| Accions de los actores                                | Respuesta del sistema                                   |
|-------------------------------------------------------|---------------------------------------------------------|
| 1. El usuario entra al fondo                          | 2. Sistema muestra la interfaz del fondo                |
| 3. El usuario selecciona el boton de agregar dinero   | 4. Sistema muestra la pestaña de metodos de pago        |
| 5. El usuario elige la cantidad de dinero y el metodo | 6. Sistema redirige a la pagina de pago correspondiente |

**Curso Alternativo:**

5.1) La cantidad es mayor a la faltante en el fondo por lo que el sistema muestra un aviso y no procede hasta que se cambie la cantidad

##### Caso 5:

**Titulo:** Pagar con el fondo  

**Actor:** Usuario

**Curso Normal:**
| Accions de los actores                     | Respuesta del sistema                                |
|--------------------------------------------|------------------------------------------------------|
| 1. El usuario entra al fondo               | 2. Sistema muestra la interfaz del fondo             |
| 3. El usuario selecciona el boton de pagar | 4. Sistema muestra la pestaña de pago y confirmacion |
| 5. El usuario escanea el Qr de mercadopago | 6. Sistema envia el dinero del fondo a la cuenta     |

**Curso Alternativo:**

5.1) No todos los integrantes confirmaron el pago por lo que el scanner no esta habilitado


##### Caso 6:

**Titulo:** Revisar el historial
 
**Actor:** Usuario

**Curso Normal:**

| Accions de los actores                        | Respuesta del sistema                                |
|-----------------------------------------------|------------------------------------------------------|
| 1. El usuario entra a la pestaña de historial | 2. Sistema muestra la interfaz del historial         |

**Curso Alternativo:**

2.1) El historial esta vacio por lo que se muestra un aviso correspondiente


# <ins>VALIDACIÓN Y VERIFICACIÓN</ins>

### Validacion con usuarios:

Se realizo la validacio con 2 posibles usuarios: el primero fue Manuel Graña, un hombre de 19 años que suele salir con amigos y luego de un rato moviendose por las interfazes y probando las features nos comento que le gusto mucho lo intuitiva que le resulto, y que la opcion de poder agregar amigos para asi poder agregarlos con rapidez luego de la primera vez le parecio un gran acierto.

Nuestra segunda posible usuario fue Maria Fernandez quien luego de hacer uso de la app opino que el diseño le parecia excelente y que la posibilidad de pagar con QR le parecio genial ya que estaba acostumbrada al uso de mercado pago por lo que se le hacia muy familiar la opcion, ademas nos dijo que no podia esperar a que la app saliera al publico para comenzar a utilizarla con sus amigos

### Verificacion de Casos de uso:

| Casos de Uso                               | Caso 1                                               | Caso 2 | Caso 3 | Caso 4 | Caso 5 | Caso 6 |
|--------------------------------------------|------------------------------------------------------|--------|--------|--------|--------|--------|
|¿Cumple un único objetivo?|Si  |      Si   |  Si      |   Si      |    Si     |   Si      |
|¿Queda claro quiénes son los actores? | Si |    Si     |   Si      |     Si    |  Si       | Si        |
| ¿Existe una secuencia lógica de los pasos? |Si     |    Si     |    Si     |   Si      |     Si    |        Si |Si 
| ¿Se documentaron todos los cursos alternativos? | Si    |    Si     |   Si      |  Si       |       Si  |   Si      |