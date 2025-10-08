# VARIABLES Y ASSIGN

## Introducción

Las variables se usan para guardar datos que el programa necesita durante la ejecución (números, textos, fechas...). Son como cajitas donde guardas información temporal.

## Estructura de la variable

- Nombre: Cómo la identificas (str_usuario, int_manzanas, dou_dinero...)
- Tipo de datos que almacena: 
    - String: Texto "Hola"
    - Int32: Numeros enteros 10
    - Double: Números decimales 3.21
    - Boolean: Valores lógicos (true or false)
    - Hay muchos más, iremos viendo a medida que creemos cositas!
- Valor: Lo que guarda la variable

## Cómo crear la actividad Assign

1. Nos vamos al Explorer - clic derecho - Add -  Folder, y le pones un nombre con el que no te pierdas, yo le puse Assign_Y_Variables
2. Clic derecho en tu nuevo Folder - Add - Sequence, y le nombras también como mejor te organices, yo le puse AssignYVariables
3. Nos vamos a Activities, y en el buscador ponemos "Sequence", arrastramos esa actividad a la zona del centro
4. Recordemos buenas prácticas: Renombrar y comentar todo lo que hagamos para entender nuestros códigos ;D
5. También en Activities, buscamos "Assign" y arrastramos al área de trabajo.
6. Ahora viene la chicha, en el primer recuadrito hacemos Ctrl+K, y empezamos con una variable de tipo String, como buena práctica añadiremos notación str_nombreVariable, en mi caso pondré "str_usuario", y le doy a enter
7. Por defecto todas las variables que creemos son de tipo String, y como es lo que buscamos no tocamos nada. En el segundo cuadro ponemos entre comillas un texto que quieras almacenar, como el "Hola Mundo" que hiciste tu primer día jiji Yo pondré "Sahoro" como valor de mi variable
8. TADAAAA!!! Si quieres verlo en consola o pop-up, añade la actividad log message o message box respectivamente. Yo usaré Log Message.
9. En el cuadro para escribir el mensaje sencillamente vamos a poner nuestra variable, en mi caso, escribo str_usuario
10. Para probarlo, en la flechita azul de arriba, clic en el desplegable y Run File.

Felicidadessss!!

## Cómo crear una variable desde Data Manager

1. Abajo de nuestro flujo de trabajo está el Data Manager, a la izquierda del output. Clic en Data Manager.
2. Veras tu primera variable ahí, pero justo arribita verás "Create Variable", dale ahí y podrás escribir. Para este ejemplo yo haré  un int32:
    - Lo llamo int_edad
    - A la derecha te sale Data Type, clic al desplegable y elige el tipo que corresponda :3 yo elegí int32
    - A la derecha del todo sale Default Value, a mí no me gusta asignarle valores aquí porque permanece fijo y a lo mejor yo quiero cambiarlo por necesidad del flujo, pero ahí como te quieras gestionar, yo asignaré el valor con la actividad assign, escribo en ella el nombre de esta nueva variable y abajo le pongo un valor como antes, esta vez va sin "". Yo escribí 22.
3. ¡TADAAAA! Ya tienes tu segunda variable ;D

## Secuencia con tus 2 variables (CONCATENAR)

1. Tenemos 2 variables, es momento de usar ambas a la vez. Añadimos un Log Message o Message Box debajo de nuestra ultima variable. Aquí empieza a importar el orden, la estructura sería:
    - Secuencia Principal
        - Variable 1
        - Log Message/Message Box
        - Variable 2
        - Log Message/Message Box
2. Escribimos nuestro mensaje dentro, para concatenar un mensaje con una variable usamos esta estructura:
    - "Mensaje 1" + variable1 + "Mensaje 2" + variable2
    - En mi caso pondré "¡Hola! Me llamo " + str_usuario + " y tengo " + int_edad + " años."
    - Verás que te sale error, cierto? Eso ocurre porque Log Message/Message box solo muestran tipo string, y tenemos una variable string y una int32... 
    - Convertimos la variable int32 en string, sencillamente poniendole al final de la variable .toString
    - Quedaría así el mensaje: "¡Hola! Me llamo " + str_usuario + " y tengo " + int_edad.ToString + " años."

Ole tú!!! Ya tienes tus primeras variables y tus primeros mensajitos concatenados haciendo uso de las variables! 