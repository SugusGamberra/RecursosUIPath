# Popurrí de tareas

Como ya hemos terminado **todos** los bloques, es hora de poner tareas. Aquí irá un poco de todo lo dado para que practiques bien.

Iba a poner las resoluciones como en la del primer bloque, pero hoy día con la **IA** diría que no hace falta. Lo suyo es que lo intentes por ti, sin ayuda, hasta que te bloquees o no te salgan las cosas!

---

### Bloque 1: Secuencias y Comentarios
1. Crea una secuencia principal llamada "Proceso_Inicial" y añádele una anotación (`Annotation`) que explique que este es el flujo de inicio. Dentro, usa un `Log Message` que diga "Inición ejecutada".
2. Crea una secuencia principal y dos secuencias secundarias. Pon un comentario en cada una de las secundarias indicando su función.
3. Desde la secuencia principal del ejercicio anterior, utiliza la actividad "`Invoke Workflow File`" para llamar a la primera secuencia secundaria.
4. Añade un `Log Message` con el nivel configurado en "`Warn`" (Advertencia) dentro de una secuencia y escribe un mensaje simulando una alerta de sistema.
5. Agrupa tres actividades `Log Message` dentro de una nueva Secuencia anidada, haz clic derecho sobre ella y ponle un nombre descriptivo para mantener el orden.

### Bloque 2: Assign y Variables
6. Usando el panel de variables, crea una variable de tipo `String` llamada "nombreCliente" y asígnale el valor "Juan Pérez" usando la actividad `Assign`.
7. Crea una variable de tipo `Int32` para almacenar el precio de un producto. Asígnale el valor 150 y muéstralo en un Message Box.
8. Crea una variable `booleana` llamada "procesoCompletado" y dale el valor inicial de False. Luego usa un Assign para cambiarlo a True.
9. Crea dos variables de tipo `String`: "saludo" y "despedida". Asigna valores a ambas y usa un `Log Message` para mostrarlas concatenadas.
10. Declara una variable de tipo `Double` para calcular el peso de una caja (por ejemplo, 14.5) y muéstrala en consola convirtiéndola a texto con `.ToString`.

### Bloque 3: Multiple Assign
11. Usa un solo `Multiple Assign` para declarar: nombre de un artículo (`String`), cantidad en stock (`Int32`) y si está disponible (`Boolean`).
12. Imagina que vas a calcular una factura. Usa `Multiple Assign` para definir: subtotal (200), impuesto (42) y total (subtotal + impuesto).
13. Usa un `Multiple Assign` para crear tres variables de texto que contengan tres colores diferentes. Muestra los tres concatenados en un solo `Log Message`.
14. En un `Multiple Assign`, crea una variable numérica iniciada en 0 y en la siguiente línea del mismo `Multiple Assign` súmale 10.
15. Registra los datos de un servidor usando `Multiple Assign`: dirección IP (`String`), puerto (`Int32`) y estado activo (`Boolean`).

### Bloque 4: Arrays y Listas
16. Crea un `Array` de tipo `String` con los nombres de 5 ciudades. Muestra la primera y la última ciudad en un `Message Box`.
17. Crea un `Array` de números enteros con 5 valores. Usa un `Assign` para cambiar el valor de la tercera posición por un 99.
18. Crea una Lista (`List<String>`) con 3 marcas de coches. Usa la actividad "`Append Item to Collection`" para añadir una cuarta marca.
19. A partir de la lista anterior, utiliza los métodos de las colecciones para eliminar el segundo elemento de la lista y muestra la lista resultante.
20. Crea una lista de correos electrónicos. Usa la propiedad `.Count` en un Log Message para mostrar cuántos correos hay guardados en la lista.

### Bloque 5: Scope de Variables
21. Crea un flujo con un `Sequence` padre y un `Sequence` hijo. Crea una variable llamada "rutaArchivo" en el padre. Modifica su valor en el hijo y comprueba en el padre si el cambio se ha aplicado.
22. Crea una variable "contadorLocal" con Scope únicamente en un `Sequence` hijo. Intenta usar un `Log Message` en el `Sequence` padre para imprimirla y observa el error de validación.
23. Define una variable global (Scope principal) para almacenar un número de factura. Accede a ella desde tres secuencias anidadas distintas.
24. Crea dos secuencias paralelas (una al lado de la otra). Crea una variable en la primera e intenta leerla desde la segunda. Corrige el scope pasándolo al contenedor principal para que funcione.
25. Usa el panel `Data Manager` (o el panel `Variables`) para cambiar rápidamente el Scope de 5 variables locales y pasarlas a globales.

### Bloque 6: Operadores Matemáticos
26. Crea dos variables `Int32`. Usa la actividad `Assign` para sumarlas, restarlas, multiplicarlas y dividirlas, guardando los resultados en 4 variables distintas.
27. Pide al usuario que introduzca un número. Usa el operador `Mod` (módulo) para saber si el número es par o impar (ej: `numero Mod 2 = 0`) y muéstralo en pantalla.
28. Crea una expresión lógica en un `Assign` para comprobar si una temperatura es `mayor a 25 AND menor a 35`. Guarda el resultado en un `Boolean`.
29. Calcula el área de un círculo usando `Math.PI * (radio * radio)` en un `Assign` y muestra el resultado truncado.
30. Utiliza el operador lógico `OR` para comprobar si un usuario tiene rol de "Administrador" o "Editor". Muestra `True` o `False`.

### Bloque 7: Diccionarios
31. Crea un Diccionario (`Dictionary<String, String>`) que asocie códigos de país ("ES", "FR", "IT") con sus nombres ("España", "Francia", "Italia").
32. Añade un nuevo par clave-valor al diccionario anterior usando la sintaxis `diccionario("PT") = "Portugal"`.
33. Usa el método `.ContainsKey("FR")` en un flujo `If` para comprobar si Francia está en el diccionario. Si está, muestra su valor.
34. Elimina la clave "`IT`" del diccionario usando el método correspondiente y muestra cuántos elementos quedan usando `.Count`.
35. Crea un Diccionario donde la clave sea un `String` (nombre del empleado) y el valor sea un `Int32` (sueldo). Modifica el sueldo de un empleado sumándole 100.

### Bloque 8: Escritura y Lectura de Archivos
36. Utiliza la actividad `Write Text File` para crear un archivo llamado "log_ejecucion.txt" y escribe en él "Proceso iniciado correctamente".
37. Usa la actividad `Append Line` para añadir una segunda línea al archivo "log_ejecucion.txt" que diga "Carga de datos completada".
38. Utiliza `Read Text File` para leer el archivo que acabas de crear, guárdalo en una variable `String` y muéstralo en un `Message Box`.
39. Crea un flujo que pida al usuario su nombre mediante un `Input Dialog` y guarde ese nombre en un archivo de texto llamado "usuario.txt".
40. Utiliza la actividad `File Exists` para comprobar si "usuario.txt" existe. Si es `True`, bórralo usando la actividad `Delete File`.

### Bloque 9: Tipos de Flujos
41. Pide un número del 1 al 10. Usa un bloque `If` para imprimir "Aprobado" si es mayor o igual a 5, y "Suspenso" si es menor.
42. Crea un contador en 0. Usa un bucle `While` que sume 1 al contador y muestre su valor hasta que el contador llegue a 10.
43. Usa un bucle `Do While` para pedirle al usuario una contraseña mediante `Input Dialog`. El bucle debe repetirse hasta que escriba "admin123".
44. Pide un número del 1 al 4. Usa un bloque `Switch` para mostrar un menú de opciones (1: Alta, 2: Baja, 3: Modificación, 4: Salida).
45. Construye un `For Each` para recorrer un `Array` de 5 nombres de carpetas y mostrar cada nombre por consola uno por uno.

### Bloque 10: Funciones de Cadenas
46. Dada la variable `texto = "   Hola Mundo   "`, usa un `Assign` con la función `.Trim()` para eliminar los espacios y muestra el resultado.
47. Dada la cadena "factura_12345_enero.pdf", usa `.Replace("_", " ")` para cambiar los guiones bajos por espacios.
48. Toma una cadena en minúsculas y conviértela completamente a mayúsculas usando `.ToUpper()`.
49. Usa la función `.Substring(0, 5)` para extraer solo los 5 primeros caracteres de una frase larga.
50. Dada una variable con el texto "Error en la línea 45", usa `.Contains("Error")` para devolver un booleano y actuar en consecuencia en un `If`.

### Bloque 11: DataTables
51. Usa `Build Data Table` para crear una tabla con tres columnas: "ID" (`Int32`), "Producto" (`String`) y "Precio" (`Int32`). Inserta 3 filas con datos.
52. Utiliza la actividad `Add Data Row` para añadir dinámicamente un cuarto producto a la tabla creada en el ejercicio anterior.
53. Usa `Output Data Table as Text` para convertir tu `DataTable` en una variable `String` y muéstrala completa en un `Log Message`.
54. Utiliza `Filter Data Table` para crear una nueva tabla que contenga solo los productos cuyo Precio sea mayor a 50.
55. Usa un `For Each Row in Data Table` para recorrer la tabla. Dentro del bucle, imprime en consola el nombre de cada producto seguido de su precio.

### Bloque 12: Try Catch
56. Intenta dividir 100 entre una variable numérica que valga 0. Usa un bloque `Try Catch` para capturar la `System.Exception` y mostrar "Error matemático".
57. Intenta leer un archivo de texto en una ruta que no existe. Captura el error específico (`System.IO.FileNotFoundException`) y muestra un aviso.
58. En un `Try Catch`, sin importar si el Try falla o tiene éxito, usa la sección `Finally` para imprimir un `Log Message` que diga "Liberando recursos de memoria".
59. Construye un `Try Catch` anidado: si el primer proceso falla, el `Catch` debe intentar un proceso alternativo, y si este también falla, lanzar una excepción personalizada (`Rethrow`).
60. Crea una variable `DataTable` vacía (nula). Intenta contar sus filas (`dt.Rows.Count`). Captura el `NullReferenceException` indicando que la tabla no fue inicializada.

### Bloque 13: Selectores e Interacción con UI
61. Usa `Open Browser` para abrir la página "google.com". Asegúrate de poner la propiedad `Maximize Window` para que ocupe toda la pantalla.
62. Dentro del navegador abierto, usa la actividad `Type Into` para buscar "Documentación de UiPath" en la barra de búsqueda y añade el envío de la tecla Enter (`[k(enter)]`).
63. Configura las propiedades de un `Type Into`: marca "`SimulateType`" como `True` y "`EmptyField`" como `True` para garantizar que el texto se escribe limpio y rápido.
64. Entra a una página de pruebas web, utiliza la actividad `Click` para pulsar un botón específico. Examina su selector en el `Editor de Selectores`.
65. Utiliza la actividad `Get Text` sobre el título de una página web para extraer su contenido, guárdalo en una variable `String` y muéstralo en un `Message Box`.