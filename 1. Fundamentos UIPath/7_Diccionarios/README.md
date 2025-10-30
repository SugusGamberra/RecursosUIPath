# 🧠 DICCIONARIOS

Un **diccionario** es como una libreta con dos columnas que almacenan pares **clave–valor** (key–value).  
⚠️ **Importante:** las claves son **únicas** y sirven para encontrar su valor de forma rápida.

---

## 🏗️ Cómo crearlos

1. Crea una variable llamada `dic_personas` desde el **Data Manager**.  
   - Pulsa **Browse for Types** y busca:  
     `System.Collections.Generic.Dictionary`  
   - Verás dos desplegables: ahí defines los tipos.  
     Ejemplo → `String` para la clave y `Int32` para el valor.

2. Añade una actividad **Assign** con este contenido:

   ```vb
   dic_personas = New Dictionary(Of String, Int32) From {
       {"Ana", 25},
       {"Luis", 30},
       {"Marta", 22}
   }


💡 Las actividades de tipo Collection son también optimas para esto, así que echales un vistazo y con lo que mejor te apañes ;3

## ⚙️ Que podemos hacer con ellos?

### ➕ Añadir o actualizar valores

Podemos añadir nuevos valores o actualizar los que tiene, si por ejemplo haces esto en un asign:

dic_personas("Juan") = 28

Si la clave no existe se crea, y si existe se actualiza!

### 👀 Mostrar datos

Para mostrarlos usaremos la fórmula de String.Join("separador", tuDiccionario). Si queremos mostrar un elemento concreto usamos tuDiccionario(Key)!

### 🗑️ Eliminar un valor

Si queremos eliminar un valor tan solo utilizaremos la función diccionario.Remove(Key). Esta función nos devolverá un boolean, por lo que deberemos generarlo previamente para almacenar el valor!!

### 🔍 Comprobar si existe una clave o valor

Si queremos comprobar si la clave o valor existen usamos las funciones tuDiccionario.ContainsKey(tuClave) o tuDiccionario.ContainsValue(tuValor), nos devuelve un boolean por lo que debemos generarlo antes tb para almacenar el valor!

| Acción              | Código                       | Devuelve       |
| ------------------- | ---------------------------- | -------------- |
| Añadir / actualizar | `dic("Clave") = Valor`       | —              |
| Eliminar            | `dic.Remove("Clave")`        | Boolean        |
| Buscar valor        | `dic("Clave")`               | Cualquier tipo |
| Comprobar clave     | `dic.ContainsKey("Clave")`   | Boolean        |
| Comprobar valor     | `dic.ContainsValue("Valor")` | Boolean        |

Hoy ha sido sencillito! Vamos a preparar los cuerpos para hacer una tandita de ejercicios en breves ;3 Así que a descansar mientras preparo los ejercicios de todo! (Ando en varios lenguajes a la vez jiji)