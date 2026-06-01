# 💻 SELECTORES E INTERACCIÓN CON LA UI

## Introducción

Esta es la última lección que vamos a ver y aprenderás cómo interactuar con el navegador y los elementos de la interfaz (UI). 
Lo primerísimo que hay que hacer es instalar la dependencia `UIPath.UIAutomation.Activities` y en el panel de actividades marcar en el filtro las actividades **Clásicas**.

Por si no te acuerdas de cómo preparar el entorno para este bloque, sigue estos pasos:

1. Abre tu proyecto en **UiPath Studio**.
2. En la barra de herramientas superior, haz clic en **Manage Packages** (Gestionar paquetes) o utiliza el atajo rápido `Ctrl + P`.
3. En la ventana que se abre, ve a la pestaña **All Packages** (Todos los paquetes) y busca `UiPath.UIAutomation.Activities`.
4. Selecciona el paquete, haz clic en el botón **Install** (Instalar) y luego pulsa en **Save** (Guardar). Intenta no escoger versiones betas o super recientes jeje. Acepta los términos de la licencia si te lo solicita.
5. Una vez instalado, ve al panel de **Activities** (Actividades) en la esquina izquierda, haz clic en el icono del filtro (el embudo) y marca la opción **Show Classic** (Mostrar clásicas).
6. Por último, abre tu navegador y comprueba en la barra de extensiones que la extensión de UiPath esté activa y funcionando (se tiene que ver el icono en color **azul**).

---

## 🛠️ Actividades del Bloque

* **Open Browser** Permite abrir un navegador en una URL específica y ejecutar múltiples actividades dentro de su contenedor.
  * **Browser Type:** Propiedad en el panel derecho para seleccionar el navegador web que vamos a utilizar.
  * **Output UiBrowser:** Permite crear una variable para almacenar la sesión del navegador y poder reutilizarla más adelante.
  * **Private:** Si se marca como `True`, abrirá la sesión directamente en modo incógnito. *(Nota: Recuerda ir a la gestión de extensiones de tu navegador y permitir que la extensión de UiPath se ejecute en modo incógnito para que funcione).*

* **Maximize Window** Sirve para maximizar la ventana del navegador web tan pronto como se abre. Se debe colocar siempre dentro del bloque **Do** de la actividad `Open Browser`.
  * *Nota:* También tienes disponible la actividad `Minimize Window` si necesitas realizar la acción contraria.

* **Attach Browser** Actividad clave para la modularización de proyectos. Sirve para conectarse a una sesión de navegador que ya ha sido abierta previamente. Para ello, utiliza la variable que guardamos en el *Output* de la actividad `Open Browser`.

---

## ⚙️ Propiedades de Interacción (Campos de Entrada / Type Into)

Al trabajar con interacciones en la UI, el panel de propiedades cuenta con opciones específicas para controlar cómo se introduce el texto:

* **Activate** Si está seleccionado (`True`), activa y pone el foco en el campo de entrada antes de proceder a escribir en él.  
  * *Valor por defecto:* `True`

* **ClickBeforeTyping** Realiza un clic físico en el campo de texto antes de escribir para asegurar que esté completamente activo.  
  * *Valor por defecto:* `True`

* **DelayBetweenKeys** Añade un retraso de tiempo (en milisegundos) entre cada pulsación de tecla para simular una escritura humana más natural o evitar saturar la aplicación.  
  * *Valor por defecto:* `0ms` (sin retraso)

* **EmptyField** Borra por completo todo el contenido previo que tenga el campo de texto antes de escribir el nuevo valor. Muy útil para limpiar formularios antes de rellenarlos.  
  * *Valor por defecto:* `False`

* **SendWindowMessages** Envía las pulsaciones de teclas utilizando mensajes internos del sistema operativo directos a la ventana. Es un método más rápido y eficiente para aplicaciones que no requieren una simulación exacta de teclado físico.  
  * *Valor por defecto:* `False`

* **SimulateType** Simula la inserción de texto en segundo plano modificando el valor directamente en la API de la interfaz web. Es el método de escritura más rápido de UiPath y permite que el bot escriba sin necesidad de que la ventana esté visible en la pantalla.  
  * *Valor por defecto:* `False` (si se desmarca, la escritura se realiza de forma visible y tradicional)

> Yastaria! Muy sencillito, a que sí? Ya tienes las bases para interactuar con la UI listas ;3
> Con esto estaría todo lo que necesitas para crear botardos desde 0! Ya cositas más específicas haces como buen programador y tiras de San Google HAHAHAHA
> Por último, en esta ocasión no pondré ejemplos con UIPath, directamente abres UIPath y ahí jugueteas, creo que a estas alturas lo tienes dominadísimo si me estás leyendo ;P
> Cuídate <3