# 🐛 Try Catch Finally aka manejo de excepciones

Es una estructura que nos permite manejar **excepciones** por lo que nos otorga una capa de seguridad en nuestros bots!

Es nuestra **red de seguridad** ya que nos permite controlar qué pasa cuando algo peta (un error) para que el bot no se quede tirao, sino que sepa reaccionar, limpiarse y seguir (o avisarnos :P)

---

## 👀 Estructura del bloque

Como imaginarás, este bloque se divide en 3 partes fundamentales:

* **Try** (intentar): Aquí metemos el código susceptible a fallos, la zona de riesgo. El bot ejecuta toda la lógica de aquí dentro
* **Catch** (capturar): Si algo falla en el `Try`, el bot salta inmediatamente aquí. Es donde decidimos qué hacer con el error (bien mandar un email, registrar el fallo, reintentar...). Podemos tener varios tipos diferentes de `catch` para diferentes tipos de errores que ahora veremos ;3
* **Finally** (finalmente): Este bloque se ejecuta **SIEMPRE**, pase lo que pase, haya habido o no errores. Es ideal para cerrar apps, limpiar variables o desconectar bbdd!

---

## 👩🏻‍⚖️ Tipos de excepciones

* **System exception** (excepciones de sistema): Son fallos técnicos. El programa se cierra, la web no carga, el selector no se encuentra... El mensaje viene del sistema y nosotros no solemos tener la culpa. Por ejemplo, *timeout reached*, *selector not found*... Estas las identificamos con `SL-00` siempre.
* **Business exception** (excepciones de negocio): Estas son las que definimos nosotros. El bot funciona teóricamente bien, pero los datos no cumplen nuestras reglas, por ejemplo, si intentas hacer una transferencia y el saldo es 0, técnicamente la app funciona pero si no tienes dinero pa qué mondá intentas hacer una transferencia, por ende no es error de uipath sino "error" de la lógica del proceso. Estas se identifican ya con `SL-01`, `SL-02`, etc.

---

## Actividad `Throw` (lanzar)

A veces queremos provocar un error nosotros mismos, para eso usamos `throw`.
- Para lanzar un error de negocio (lo más común): `New BusinesssRuleException("Tu mensaje de error" + exception.Message)`.
- Para lanzar un error de sistema (menos común manual, pero factible): `New SystemException("Tu mensaje de error aquí" + exception.Message)`.

---

## 😍 Cómo montar un try-catch-finally

Vamos a crear un flujo para provocar un errror y que así veas como de útil es esto. Ah! **Sugutip**: A partir de ya, todo lo que ahgas en uipath tiene que pasar por aquí sí o sí. Vamos al lio!

1. Como siempre, **organisasions**, ubica tu carpeta donde vayas a guardar este proyecto y dale un nombre que la identifique bien. Ya dentro creas una **Sequence** con un nombre descriptivo, en mi caso le pondré `tryCatchFinally`. En el panel activities, como siempre, arrastra una `secuencia` a tu área de trabajo.
2. Buscamos `Try Catch` en el panel de actividades y la arrastramos dentro de nuestra secuencia.
3. Dentro del `Try` vamos a pedir un numero por ejemplo, asi que metemos un `input dialog` y ya lo rellenas como quieras! La idea es hacer algo sencillito para probar, este caso será de una calculadora que sume lo q el usuario meta + 100. Así que vamos rellenando el bloque, recuerda que puedes descargar el archivo para cotillearlo y probar de hacer lo mismo que yo!
4. Para hacer nuestro `throw` hare algo sencillito, y es que en mi bot no quiero que sumes un número mayor a 50, así que condicional `if` y le decimos que si `int_numeroUser > 50`, en `then` le metemos el susodicho. En el panel de actividades buscamos `throw` y lo arrastramos a la parte del then, importante, dentro escribes lo siguiente: `New BusinessRuleException("El número no puede ser mayor a 50")`. Y yasta. 
5. Dentro del `catch` empezamos con una System.Exception, que como verás ya esta seleccionada en el desplegable, y arrastramos dentro un log message y le ponemos `New SystemException("SL-00: " + exception.Message)`.
6. Le damos al `+` de abajo y añadimos la businesss, que eso abres el desplegable y como seguramente no te aparezca, le das a **browse for types** y en la ventana que se te abra le escribes `BusinessRuleException`, y ahí te saldrá, seleccionas la de UiPath.Core y palante! Ahora metes un log message y dentro escribes `New BusinessRuleException("SL-01: " + exception.Message)`.
7. En el `finally` para que lo veas bien añade un log message con cualquier parafernalia que quieras.

Ahora cuando lo pruebes verás que si introduces un número menor a 50, te hace el cálculo. Si pones un número mayor a 50 te tira el throw con la business exception. Si pones un double (por ejemplo 6,8) te salta la sistem exception y asi la ves!

---

> Y listo por hoy!!! Esto es super importante implementarlo, ya te digo, así que a sacar la costumbre!