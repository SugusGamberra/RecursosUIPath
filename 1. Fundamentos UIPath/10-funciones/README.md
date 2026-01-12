# 📚 Funciones

Las funciones son _trozos de código_ ya creados que nos sirven para _manipular datos_ sin tener que inventar la rueda cada vez. Imagina que son como herramientas especiales que transforman lo que metes en ellas en algo diferente (masomeno). Tienen 2 partes:

1. **Declaración**: Cómo funcionan por dentro (la mayoría vienen ya hechas por uipath)
2. **Llamada**: Cuando tú le indicas dónde usarse

---

## ⛓️ [`Funciones de cadenas`](./funcionesCadenas.xaml)

Estas son las más comunes para limpiar textos:
- `String.Join("separador", array)`: Une todos los elementos de un array, unidos por un separador que tú le definas
- `String.Split(" "c)`: Separa una cadena en función de un carácter concreto. Devuelve una array de cadenas con todos los fragmentos. La `c` sirve para indicar que transforme la cadena pasada como parámetro a tipo carácter.
- `Left(cadena, Entero)`: Extrae de una cadena una subcadena de caracteres hasta la posición dada, empezando a contar desde el inicio.
- `Right(cadena, Entero)`: Extrae de una cadena una subcadena de caracteres hasta la posición dada, empezando a contar desde el final.
- `cadena.Replace(cadenaVieja, cadenaNueva)`: Reemplaza una parte de la cadena por otra nueva.
- `cadena.Substring(posicionInicial, tamañoCadena)`: Extrae una subcadena definida por el carácter de inicio y el número de caracteres que tiene la nueva subcadena.
- `String.Length(cadena)`: Devuelve el número de elementos de una cadena de caracteres.
- `Trim(cadena)` / `cadena.Trim(carácter)`: Elimina los espacios en blanco del inicio y final. Si le añades un carácter, elimina ese en concreto.
- `cadena.ToUpper` / `cadena.ToLower`: Sustituye todos los caracteres a mayúsculas o minúsculas.
- `variable.toString`: Convierte una variable en una String.
- `String.Equals(String)`: Permite comparar dos cadenas.

> Vamos a jugar con los textos para que veas lo fácil que es ;P
> Recuerda que siempre te acompaña el `archivo.xaml` para q lo bajes y lo trastees
> Pero si eres más independiente, con que sigas esta guía te sirve ^^

### Cómo hacerlo

Como siempre, primer paso: **organización**: Ponlo en la carpetita que le hayas designado a esta lección, abre UIPath, crea la secuencia, etc. Una vez tengas tu workflow listo vamos palante!!

1. `Ejemplo String.Join`:
   1. Crea una variable (`arr_palabras`) de tipo `Array of String` con valor `{"Hola", "cara", "pito"}` (o lo q tu quieras xd)
   2. Usa un **Assign**: Crea una variable llamada `str_unido` (tal cual está, tipo string), y abajo le das el valor de `String.Join("-", arr_palabras)`.
   3. Lo mostramos en un `Log Message`, claro para poder ver el Array recordemos el truquillo de `String.Join(", ", tu_array)`, porque si no, no te lo muestra, lit venimos usando esto desde el inicio, peeero esta weno que quede aquí reflejado también ^^
2. `Ejemplo String.Split`:
   1. Crea una variable llamada `str_nombreCompleto` de tipo string y dale un valor, en mi caso `"Borja Santo Virgo"`
   2. Crea otra que sea un array de string llamada `arr_resultado`, y le metes el valor `str_nombreCompleto.Split(" "c)`
   3. Muestralo en el log, por ejemplo, `"El primer apellido es: " + arr_resultado(1)`, recordemos q los arrays empiezan a contar en 0
3. `Ejemplo Left y Right`:
   1. Crea 2 variables, una que sea `str_izq` y dentro `Left("Zagarita", 4)` y otra `str_dcha` con `Right("Zagarita")`
   2. Muestralo en un log message para ver lo que te recorta de un lado y de otro :3
4. `Ejemplo Replace y Substring`:
   1. Crea 2 variables, una que sea `str_saludo` y asignale `"Hola caretuco".Replace("caretuco", "perdon, quise decir Mario")`. La otra que sea `str_palabra` con `"Paracetamol".Substring(0,2)`
   2. Muestralos en un log message ;3
5. `Ejemplo ToUpper/ToLower y Trim`:
   1. Crea una variable que se llame `str_texto` y guárdale el valor `" Insertar Biblia aquí ".Trim.ToUpper` (date cuenta que al inicio y al final hay espacios), y otra que se llame `str_susurro` que albergue `"TE AMO CON TODA MI ALMA MI EVITATIVO FAVORITO".ToLower`
   2. Mostramos en el log para ver que la palabra de diosito, el que te da sus peores guerras, es la que importa, y que no debemos asustar al evitativo con tanta euforia uwu (aqui hasta psicologia aprendes)

---

## ✨ Otras funciones

> Además de las vistas, tenemos muchas otras funciones que también son muy útiles.
> Ya has visto como usarlas, sigue la misma lógica!
> Te darás cuenta el tipo de variables que son gracias a la **notación húngara**, ya ve que ni falta hace que le diga a estas alturas qué es qué
> Ahí ve la importancia de hacer las cosas bien crvrg 😡

- `list.Append(variable).ToList()`: Añade variable a la lista.
- `lst_animales.Count`: Cuenta el número de elementos de una lista.
- `diccionario.TryAdd(clave, valor)`: Añade un campo al diccionario (devuelve Boolean).
- `diccionario.Remove(clave)`: Elimina un campo (devuelve Boolean).
- `diccionario.ContainsKey(clave)`: Comprueba si la clave existe (devuelve Boolean).
- `ContainsValue(valor)`: Comprueba si el valor existe (devuelve Boolean).
- `Datetime.AddDays/AddMonth/AddYear`: Permite modificar fechas sumando o restando días, meses o años.
- `String.EndsWith(“cadena”)`: Comprueba si una cadena termina en una subcadena específica.
- `New BusinessRuleException(“Mensaje”)`: Añade una nueva excepción de negocio. Veremos en la próxima lección los Try Catch, esto será útil allí igual que el de abajo.
- `New SystemException("Mensaje")`: Añade una nueva excepción de sistema.
- `Regex IsMatch (Letras)` - `Not System.Text.RegularExpressions.Regex.IsMatch(str_entrada, "^[\p{L}\s]+$")` : Controla que solo sean letras.
- `Regex IsMatch (Números)` - `Regex.IsMatch(variable.ToString(), "^(\d)+([0-9]\d+)$")` : Controla que solo sean números.