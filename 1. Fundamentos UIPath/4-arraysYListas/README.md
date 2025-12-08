# Arrays y listas

## Qué son? En qué se diferencian?

Ambas son colecciones de datos: almacenan varios valores en vez de uno.

Se diferencian en que una array tiene un tamaño fijo, es más rápida y simple y sus datos no cambian, mientras que la lista es dinámica (puedes añadir o quitar valores a tu antojo), más flexible y son datos suceptibles a modificación.

## Casos de usos

Entendiendo las diferencias podemos aplicar las arrays para almacenar valores conocidos y fijos, como por ejemplo días de la semana, los meses del año... Y las listas para cosas que irás generando, como una lista de correos electrónicos o usuarios.

## Arrays

### Cómo crearlas en uipath

1. Como siempre organizamos nuestros archivos para mantener un espacio de trabajo limpio: creas una carpeta y dentro una sequence que nombrarás a tu gusto, yo le puse ArraysYListas.
2. Arrastramos una sequence de las activities al área de trabajo. Dentro, arrastramos assign para crear la variable.
3. Hacemos Ctrl + K para crear la variable, le asignamos un nombre, yo por ejemplo le pondré arr_str_diasSemana.
4. En el Data Manager cambiamos el Data Type a "Array of [T]", recuerda que puedes crear tu variable aquí también y asignarle los valores en tu área de trabajo con un assign!
5. Como en este caso quiero poner los días de la semana en tipo texto, al seleccionar "Array of [T]" nos aparecerá un pop-up para elegir el subtipo, pondré "String", pero puedes usar por ejemplo Int32 para poner 1,2,3,4,5,6,7!
6. En Set value escribimos entre corchetes nuestros valores separados por una coma, recuerda que si es tipo string cada valor irá entre comillas viéndose de este modo: {"Lunes", "Martes", "Miércoles", "jueves", "Viernes", "Sábado", "Domingo"}
7. ¡Tadaaaa! Podemos poner un log message para llamar a nuestra variable y ver el resultado ;D

Aquí menciono que a diferencia de otros tipos de variables, un array necesita otro formato para mostrarse en consola:

String.Join(", ", tuArray)

Esto lo que hace es separar con comas cada uno de tus datos, puedes usar comas, guiones, salto de linea (que se hace poniendo vbCrLf)... 

Si queremos leer un elemento concreto de nuestra array tenemos en cuenta que la posición inicial es 0, por ende en nuestros días de la semana el 0 = Lunes y se haría así en un Log Message:

"El primer día de la semana es " + arr_str_diasSemana(0) + " y Marzo es el mes número " + arr_int_meses(2).ToString + " del año!"

la fórmula es tuVariable(posiciónElemento), y si es de otro tipo que no sea string ya sabes: .toString al final!

Para modificar un elemento lo seleccionamos arrastrando Assign a nuestro área de trabajo, escribimos nuestra variable existente y la posición del elemento a modificar más el valor: tuArray(posiciónElemento) = "Modificación". Yo me equivoqué y escribí jueves con la primera en minúscula así que quedaría:

arr_str_diasSemana(3) = "Jueves"

Lo muestro en un log message y fino!

## Listas

### Cómo crearlas en uipath

1. Usaré el mismo área de trabajo, usted hágalo como mejor se gestione uwu
2. Arrastramos un assign a nuestro área de trabajo, Ctrl + K, asignamos un nombre (yo usaré lst_str_users) y vamos al paso chachi, definir el tipo de variable!
3. En Data Type seleccionamos la opción browse y escribimos system.collections.generic.list, también sirve poner generic.list pero vamos, cada cual a su estilo ;D seleccionamos el que pone List<T> y arribita sale un desplegable, ahí seleccionamos el tipo, yo usaré string!
4. Para asignar valores la vaina es difernete: le ponemos New List(Of String) From {"Aquí", "tus", "Elementos"}
5. Tadaaa! Ahora podemos probarlo con un log message: como antes, ponemos String.Join("separador", tuLista)

Para añadir nuevos elementos a tu lista buscamos en activities "Append Item to List", le indicas tu lista y le pones el elemento nuevo. También puedes usar "Append Item to Collection" ;3

Otra forma de crear listas es con "build collection", en el panel de la derecha de "Properties" creas la variable como antes y se añaden los items ya en la actividad: primero en First items y ya luego en Next items.

Para modificar elementos se hace con assign con la fórmula de tuLista(posicionElemento) = "Modificación"!

Para eliminar elementos usamos la actividad "Remove from collection": seleccionas tu lista, si quieres que sea 1 elemento, todos... y el elemento a borrar!

Y listo!

Espero que te haya gustado la lección de hoy :D