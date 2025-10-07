# CREA TU PRIMER PROYECTO EN UIPATH

1. Abre UIPath Studio.
2. Inicia sesión si no la tienes iniciada ya.
3. En la interfaz, a la izquierda, busca "Settings", procura que esté en inglés y si quieres pon el "theme" en "dark" para que no se te agote la vista. Te pedirá reiniciar UIPath, acepta jeje.
4. En la parte de "Start" verás a la derecha de la interfaz una sección llamada "New Project".
5. Haz clic en Process.
	- Te pedirá el "Name" (nombre del proyecto). Yo le pondré Fundamentos_UIPath.
	- La descripción es opcional.
	- En "Location" elige la ruta donde quieras guardar tus proyectos, yo lo dejo por defecto que no me molesta ahí jeje.
	- En "Compatibility" deja Windows, y "Languaje" VB (Visual Basic).
	- Pulsa crear y empezará a crearte el entorno.

## Estructura del proyecto.

En la interfaz verás diferentes secciones. A la izquierda verás la estructura que sigue el proyecto:

- Dependencies: Librerías y paquetes que usa el proyecto (más adelante veremos que necesitaremos bajar ciertos paquetes para ciertas automatizaciones).
- Entities.
- Templates.
- Main.xaml: Archivo principal donde se diseña el flujo de trabajo.
- project.json: Contiene la config del proyecto.

Por temas de organización crearemos carpetitas y proyectos en esta parte de la interfaz.

## Interfaz de UIPath Studio

1. Paneles principales: A la izquierda, donde hablaba de la estructura del proyecto. Te puede aparecer una barra lateral a la izquierda de este con iconitos o arriba de esa sección de la estructura.
	- Explorer: Donde vemos la extrutura.
	- Activities: Son todas las actividades que existen para usar a la hora de crear tu botsito.
	- De aquí por el momento no miraremos más para no liarnos mucho.
2. Main: Verás un espacio en el centro, es ahí donde arrastramos las actividades. 
3. Properties: En esta parte, a la derecha, es donde configuraremos las propiedades de las actividades que usemos.
4. Data Manager: Justo debajo del espacio de Main verás esta sección. Ahí puedes ver las variables que vas creando, modificarlas, asignarles valores... Así como tus argumentos y demás cositas que más adelante veremos.
5. Output: A la derecha de Data Manager. Aquí vemos la consola.

## Diseñando tu primer flujo

1. En la sección de explorer, haz clic derecho. Busca la opción de "Add" - "Folder" y ponle un nombre que te sea fácil de identificar. Yo le pondré 1_Secuencia_Y_Comentarios. Por cierto, la idea de nombrar archivos con este método o similares es una buena práctica que evita en programación errores y tal. Más vale coger esa práctica pronto ;3
2. Encima de tu carpeta haz clic derecho, "Add" - "Squence" y dale un nombre. Yo le pondré "HelloWorld".
3. Nos vamos a la sección "Activities", en el buscador ponemos "Sequence", una vez lo encuentres, arrástralo al espacio del centro del programa.
4. Podemos nombrar nuestra secuencia, de hecho es recomendable ir nombrando nuestras actividades como buena práctica. Yo le pondré "Secuencia principal".
5. Para comentar en nuestras actividades de UIPath, podemos usar Shift+F2 o clic sobre los 3 puntitos en ella y en "Annotations" - "Add Annotation", ahí puedes ir explicando lo que vas haciendo, otra buena práctica si trabajas en equipo (bueno para ti también jeje).
6. Buscamos en el buscador de actividades "comment", te saldrán 20mil opciones, pliega la pestaña de "Excel", busca la pestañita de "Programming", ese es el bueno. Arrastra la actividad dentro de tu secuencia principal.
7. Modificamos el contenido del "Comment" (recuerda renombrarlo), y para escribir más cómodos a la derecha: clic a tu actividad Comment, en "Properties" verás unas opciones, para escribir dentro en la sección "Text" a su derecha verás un iconito como de dos flechitas, dale ahí y se te abre para que puedas comentar comodísimo.
8. Busca "Log Message" en Activities y arrástralo justo debajo de tu primer comentario, aún dentro de tu secuencia. Dentro escribe el típico "Hola Mundo" o "Hello World", o "me llamo PacoPepe", usted sabrá :D. Recuerda escribirlo entre comillas, ya que es de tipo String (texto) y este siempre va así, para que el programa lo entienda ^^. Log Level lo puedes dejar tal cual o elegir alguno por mero experimento y que veas en la consola como se visualizan.
9. Arriba de todo veras un botoncito de play, un triangulito azul, la flechita de al lado le tienes que dar eh? Te dará a elegir opciones, dale a "Run file", eso te corre solo este archivo, si le das normal te corre el main y no queremos eso. 
10. Abajo del área de trabajo (donde tu secuencia), en Output vemos que efectivamente, sale tu saludo muajaja! Ya tienes tu primer programa ;D Pero somos unos inconformistas, vamos a crear una ventana jeje.
11. Busca "Message Box", arrástralo justo debajo de Log Message, en este punto ignoramos un poco el orden porque estamos aprendiendo.
12. Escribimos lo que queramos, entre comillas, como "Hola Mundo" o cualquier cosita. A la derecha en propiedades puedes personalizar el botón en "Buttons", yo elegiré la opción de "Ok".

¡TADAAAA! Funcionó todo!! De todos modos vas a ver el archivo que adjunto para que puedas abrirlo y toquetearlo desde ahí :3

Me gusta que quede todo lo mejor explicado posible, mi querido lector si usted tiene dudas puede contactar conmigo, en mi perfil tienes mi contacto :D

Ten buen día, nos vemos pronto!