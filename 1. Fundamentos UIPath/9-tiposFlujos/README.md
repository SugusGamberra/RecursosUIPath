# 🔁 Tipos de flujo

En **UIPath** trabajamos con **flujos condicionales** e **iterativos**. Cada cual sirve para controlar cómo avanza la automatización!!

Debemos conocer bien los **operadores numéricos** y **lógicos** para comparar numeros o combinar condiciones:

## ▶️ Operadores numéricos

- `<`: Menor que
- `>`: Mayor que
- `=`: Igual
- `<>`: Distinto
- `>=`: Mayor o igual que
- `<=`: Menor o igual que

## ▶️ Operadores lógicos

- `AND`: Solo devuelve _true_ si todas las condiciones son _true_.
- `OR`: Devuelve _true_ si **al menos una** es _true_.
- `NOT`: Invierte el resultado (si es _true_ → se vuelve _false_).

---

## 🧩 [Flujos condicionales](./flujosCondicionales.xaml)

### ✔️ If/ Else if

Ejecuta un bloque **si** la condición es _true_. Si **no** lo es, pasa el bloque a `else`.

### ✔️ Switch

Evalúa una expresión (texto, número...) y ejecuta un caso concreto. Incluye un **default** por si no coincide con ningún valor!

---

## 🔂 [Flujos iterativos](./flujosIterativos.xaml)

Sirven para **repetir** acciones automáticamente.

### ✔️ For Each

Repite un bloque _una vez por cada elemento_ de un contenedor: arrays, listas, diccionarios...  Por ejemplo, si tu lista tiene 5 elementos el for each se ejecuta 5 veces.

### ✔️ While

Repite el flujo _mientras se cumpla una condición_. Si la condición siempre es _true_ se crea un **bucle infinito**, por eso la importancia del `break` que hablamos en la leccion anterior xd

---

> Yastaria por hoy! Muy sencillito, a que sí? Tienes los ejemplos en los archivos .xaml, que irán enlazados en los títulos de las secciones para que puedas ir a ellos y descargarlos y probarlos ;3