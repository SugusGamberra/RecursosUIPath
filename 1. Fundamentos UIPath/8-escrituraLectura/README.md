# 🧠 ESCRITURA Y LECTURA

## 📝 Write text file

Esta actividad escribe texto en un archivo:

- Si el archivo **no** existe, lo crea automáticamente.
- Si ya **existe**, sobreescribe su contenido.

> Útil para guardar resultados, logs o datos temporales!!

**Ejemplo**: Con la actividad Write Text File rellenamos el espacio de `Write to file` con la ruta que queramos y en el cuadro para escribir en el buscador de la carpeta ponemos nombreArchivo.txt, y en `text` lo que queremos introducir entre "comillas"!
 

## 📖 Read Text file

Te permite leer el contenido de un archivo y guardarlo en una variable tipo String que luego puedes usar o mostrar :3

**Ejemplo**: Arrastramos la actividad Read Text File y ponemos la ruta de nuestro archivo para leerlo en `File`. A la derecha, en las propiedades, en la sección de `Output` le creamos una variable para que almacene la información y podamos leerlo en un log message!


## ⚙️ Date Time

Es un tipo de variable que maneja fechas y horas:

- **Fecha y hora actual**: Now
- **Fecha actual**: DateTime.Today
- **Fecha personalizada**: New DateTime(2025,10,28)

Para que el formato se adapte al idioma y localización puedes establecer la cultura en una actividad assign:

System.Threading.Thread.CurrentThread.CurrentCulture = New System.Globalization.CultureInfo("es-ES")

O en el mismo log message pones dt_tuVariable.toString("dd/MM/yyyy HH:mm:ss")

> **IMPORTANTE**: Importar System.Globalization si te lo requiere UIPath! Esto se hace desde el **Imports**.

**Ejemplo**: Creamos una variable que nombraremos siguiendo las buenas practicas: dt_tuVariable. Cambiamos el tipo de variable a System.DateTime! Y de ahí tan solo es darle el valor que elijas de los mencionados (Now, today o fecha concreta) y mostrarlo en un log message!

## ⌨️ Atajos de teclado

| Acción | Atajo | Descripción |
| :--- | :--- | :--- |
| Crear variable | **Ctrl + K** | Desde una propiedad, crea y asigna una variable. |
| Crear argumento | **Ctrl + M** | Igual que Ctrl + K, pero para argumentos. |
| Comentar actividad | **Ctrl + D** | Desactiva temporalmente una actividad. |
| Descomentar actividad | **Ctrl + E** | Reactiva la actividad comentada. |
| Autocompletar | **Ctrl + Espacio** | Muestra variables disponibles y sugerencias. |


## ⛔ Break

La próxima lección será control de flujos, así que quiero matizar la importancia de esta actividad a la hora de tratar con `bucles o condicionales`!! Ya lo veremos ;3

Y eso sería todo! Te dejo como siempre los ejemplos en el repositorio para que te bajes el [.xaml](./escrituraLectura.xaml) y puedas probarlo :3