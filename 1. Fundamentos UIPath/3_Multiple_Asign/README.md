# MULTIPLE ASIGN

## Introducción

Esta actividad nos sirve para asignar varios valores en un mismo espacio.

De esta forma queda todo más ordenadito sin necesidad de usar mogollón de asigns.

Dentro puedes añadirle tantas variables con su correspondiente valor como creas necesario.

## Cómo usar Multiple Assign

1. Como siempre empezamos por crear una carpeta (Add folder) en nuestra sección Explorer. Clic derecho en ella y "Add - Squence".
2. Nos vamos a Activities y en el buscador ponemos "multiple asign". Seleccionamos la del desplegable "workflow" - "control".
3. Arrastramos a nuestra área de trabajo.
4. Clicamos en el área "Save to" para escribir, usamos un shortcut que es pulsando Ctrl + K en tu teclado y de esta forma creamos nuestra primera variable, yo usaré diferentes tipos. A la derecha le asignamos un valor según el tipo de variable.
5. Para seguir añadiendo variables en Multiple Asign le pinchamos al botón "add" y ahí le vas creando ;3
6. Y listooo!! Si quieres probarlo puedes añadir debajo un Log message y concatenar todas tus variables! Recordemos que para concatenar necesitmaos str_tuVariable + int_tuVariable2 , ¿qué ocurría si la variable no es de tipo string? Que se agobia uipath, entonces al final de tu variable por ejemplo numerica añade .toString, quedaría así: int_tuVariable2.toString

## Tipos de variables

- String: str_texto | Esto es puro texto. Siempre que le asignes un valor va entre comillas, ejemplo "Holiwi".
- Int32: int_numero | Números enteros, ejemplo 32.
- Double: dou_decimal | Números decimales, ejemplo 4.9
- Boolean: boo_estado | Variable de lógica, solo tienes 2 opciones: True o False.
- Array of... (te sale una ventana emergente para que elijas el tipo): arr_int_diaSemana | Conjunto de valores del mismo tipo. Se usan las arrays para cosas que sabemos que son finitas, como los días de la semana o los meses del año, ya que esta variable consume el espacio justo y necesario. Puedes elegir una variable de tipo Int32 o de tipo String. Ejemplo {1, 2, 3, 4, 5, 6, 7}
- Object: obj_coche | Para cualquier tipo de dato genérico, poco recomendable y el gran olvidado de uipath HAHAHAHA

Y ya está! Eso es todo! Irán saliendo más variables a medida que sigamos avanzando en el curso ;D y según salgan, se explican ^^

Ten buena semanaaa!