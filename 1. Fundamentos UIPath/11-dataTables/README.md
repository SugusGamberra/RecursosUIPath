# 💹 DATA TABLE

## 🦍 Qué es?

Es una estructura de datos en forma de tabla, igual que un excel, se compone de filas y columnas. En ella puedes almacenar, manipular y procesar info de forma estructurada, así como nuestro botito :3

---

## 🧑🏻‍🏫 Actividades principales

Son las que más se suelen usar, pero si pones data table verás chorrocientas más, según necesidades elige la que mejor te venga! Esto que propongo es como yo aprendí a manejarlas, y es una buena forma de empezar ^^

### 👷🏻‍♀️ Build Data Table

Con esta creamos la tabla desde 0.

1. Recordemos que el primer paso siempre es organización: ubícalo donde tengas dispuesto todo esto, y crea la secuencia en uipath, arrastra una secuencia al área de trabajo y palante!
2. Busca en **Activities** `Build Data Table`, arrástrala dentro de tu secuencia!
3. Dale al botoncito de `Data Table`. Te aparecerá un pop-up en la que ves 2 columnas con el tipo `string` e `int32` predeterminado y las filas! Puedes cambiar el tipo y el título de las columnas así como el contenido de las filas, te dejo via libre ahora que ya estás manejando todo dpm! Yo haré una columna de tipo `string` con atributos de mi ex y en la columna 2 `int32` con puntuaciones a sus atributos (verá que rápido te andas bajando el archivo, COTILLA jijijijijiji)
4. Verás que al editar las columnas puedes poner pues eso, el nombre que le asignas, el tipo de dato que manejas, el `allow null` (esto si lo marcas permites que ese campo quede vacío, si lo desmarcas tiene que ir un valor dentro x cojones), `auto increment` en caso de que elijas tipos numéricos (esto hace que automáticamente el siguiente valor numérico incremente), puedes ponerle un valor por defecto (`default value`), hacerlo `único` (esto significa que el valor de esta columna es único e irrepetible) y el `max lenght` (máximo de texto que le puedes poner). Te darás cuenta si has estudiado DAM o DAW que esto es muy **BBDD** 🫦
5. En el panel de propiedades a la derecha, en `output` no te olvides de crearle una variable para que almacene los datos ahí y puedas trabajar sobre ella!! Recordemos la utilidad de la **notación húngara**, yo le pondré `dt_ex`

Y listo, tienes tu primera tablita :P

### 📋 Output Data Table as TExt

UIPath no te deja leer tal que así la tabla en consola, la tienes que convertir en texto (`string`).

1. Arrastra debajo la actividad `Output Data Table as Text`.
2. Dentro, escribe tu data table que creaste, en mi caso `dt_ex`.
3. Ahora, a la derecha en **properties**, en el `output`, crea una nueva variable que es la que usarás en el log message para mostrar la tabla en la consola! En mi caso le pondre `dt_exLectura`.
4. Sencillamente añade un `Message Box` o `Log Message` e introduce en él esta nueva variable para visualizarla ;D

### ➕ Add Data Row

Con esta añades datos a tu datatable!

1. Busca `Add Data Row` y arrástrala debajo del output data table (asi al final podemos comparar :P)
2. En **ArrayRow** es donde añadimos los valores usando la fórmula `New Object() {valorCol1, valorCol2, ...}`.
3. En **DataTable** es donde pones la variable de la tablita que creaste, en mi caso `dt_ex`.
4. Ahora debajito vamos a copiar el método anterior con el output datatable as text! Pones la variable de tu datatable y creas una nueva de lectura :D y ahí ve la comparación ^^ (recordaba que antes se podía usar la misma variable del **output** pero o tengo el uipath to peio o tengo mala memoria HAHAHAH)

### 🔁 For each Row in Data Table

Es básicamente un bucle **for each** hecho actividad para recorrer la tabla fila por fila y trabajar sobre los datos ^^

1. Arrastramos `For Each Row in Data Table` debajo.
2. En **datatable** pon tu variable de tu tabla, en mi caso `dt_ex`.
3. En **item name** o bien lo dejas tal cual o le asignas tu cualquier cosa, según tu tabla, x ejemplo persona, edad o en mi caso `atributos`.
4. Dentro del Body le metes un `Assign`, crea una variable en mi caso `str_atributo` y dale un valor, en mi caso `atributos("Atributos de mi ex").ToString`.
5. Para mostrarlo en un log message tan solo ponle la variable `str_atributo` o la que hayas creado :D

Aquí los estamos mostrando, pero realmente con esto puedes operar por cada elemento de la forma que precises ^^

### ⌛ Filter Data Table

Esto es pa quedarnos solo con lo que nos interesa.

1. Arrastra la actividad `Filter Data Table` debajo!
2. Le damos a **configure filter**, y nos salen diversaas opciones.
   1. **Pestaña `Filter Rows`**: `Keep` para mantener, `remove para quitar`. Columna a ingresar, la operación de comparación o filtro, el `valor` a mantener o quitar.
   2. **Pestaña `Output Columns`**: `Keep` y `Remove`, y la columna a ingresar.
3. Nosotros vamos a hacer un ejemplo, pero deja volar tu imaginación como quieras :D Primero arribita elijo mi `dt_ex`. En **filter rows** me quedo en `keep`, en la columna pongo `Puntuación (sobre 10)`. Si esto te sale que no lo soporta uipath (y la queso), le metes un número que es la posición de tu columna, como los arrays aqui cuenta desde 0 tb, en mi caso tengo que poner `1`. La **operation** la pongo en `>` y en **value** le digo `10`.
4. Le damos a ok y en **properties** - **output** creamos una variable que almacene el filtro, en mi caso `dt_exFiltro`. Así podemos leerlo con el método de output data table as text!

Y ya puedes ver tus datitos filtrados :P

### 🗃️ Sort Data Table

Esto te ordena tu contenido por orden alfabético (ascendente, descendente), número, etc.

1. Arrastra `Sort Data Table`.
2. Pon tu datatable, en mi caso `dt_ex`!
3. En **properties** es donde vas eligiendo como la vas a ordenar. Empezamos creando una variable en **otuput** para que almacene las cosicas, yo le pondre `dt_tablaOrdeanda`. En **name** pon el nombre de tu columna y en order pondré `descending` mismamente.
4. Con el método de **output data table as text** podemos ver que ahora la tabla se ordena con los pares de numeros mayores a menores!

---

> Y yastaria!! Sencillito verdad?? :P
> Ahora a disfrutar de lo aprendido y descansar muchito uwu