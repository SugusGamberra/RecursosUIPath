# SCOPE DE UNA VARIABLE

## Qué es?

El Scope es el alcance de la variable, dónde existe dentro del proyecto. Básicamente dónde puedes verla y usarla en tu flujo de trabajo. 

Me gusta imaginarlo como si fueran cajas, tipo si pones una caja azul dentro de una caja roja, solo la persona que abre la caja roja verá la caja azul. Si pones la caja roja dentro de una caja verde, verás la caja verde - roja - azul, y así.

- Scope local: Solo funciona dentro de una Sequence o Activity concreta, se usa en cosas temporales como el contador de un bucle.
- Scope amplio: Es visible y accesible en todo tu flujo de trabajo. Es útil para contextos donde necesitas usar tus variables en diferentes secuencias de tu archivo.
- Entre flujos de trabajos diferentes: Más adelante veremos que podemos hacer un proyecto con diferentes archivos .xaml, y dentro de tu archivo main.xaml puedes llamar el resto de tus otros .xaml. Como no es posible que las variables de tus otros .xaml se puedan usar directamente en el main.xmal lo que se usa son argumentos de entrada, salida, entrada-salida (in, out, in-out) o incluso el mismo orchestrator, ya lo veremos ;3

Según lo que tengamos que hacer podemos elegir el scope de nuestra variable: si solo la usas en una única secuencia ponlo para tu secuencia, si la usan varias secuencias ponlo a la secuencia principal o a todo el archivo, y si necesitas pasarla a otro .xaml tienes que hacer argumentos, no variables ;3

## Cómo se cambia el Scope?

1. Crea tu carpetita y archivo y nómbralos para que lo tengas todo ordenadito! 
2. Añadimos una secuencia y la nombramos como "Secuencia principal" (con esto caes en la cuenta de la importancia de nombrarlo TODO xd)
3. Dentro de esta secuencia vamos a añadir otras 2 secuencias: Una será "secuencia secundaria" y la otra "secuencia terciaria".
4. Para la creación de variables puedes hacerlas con la actividad assign o directamente en el data manager. Te recomiendo que lo hagas en Data Manager directamente, yo lo haré con assigns para que sea más visual.
5. Una vez creadas, en Data Manager verás la opción "Scope" a la derecha de "data type". Clicas en la de la variable que quieras modificar y verás un desplegable que te permite ir cambiando el alcance a donde tú quieras.

Y esta sería la lección de hoy! Muy sencilla, así le damos descanso al cerebro :3

Un abrazoteee!