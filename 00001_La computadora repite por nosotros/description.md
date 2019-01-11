Como te adelantamos en el ejercicio anterior, en Javascript existe una forma de decir "quiero que estos comandos se repitan esta cantidad de veces".

Entonces, cuando es necesario repetir un comando (como console.log) un cierto número de veces, en lugar de copiar y pegar como veníamos haciendo hasta ahora, podemos utilizar la sentencia `for`.

Por ejemplo, si queremos imprimir "Hola!" por pantalla 4 veces, podríamos escribir lo siguiente:

```javascript
for(var i = 0; i < 4; i++) {
   console.log("Hola!")
}
```
En el for tenés un contador de repeticiones, en el ejemplo anterior ese contador es la variable `i`. Tenés que indicar donde comienza a contar, cuál es la condición en donde dejará de contar, en este caso `i < 4` y cómo se modifica la i en cada repetición (en este caso se incrementa uno).

Sabiendo esto, ¿Cómo podemos hacer para imprimir 4 veces por pantalla la palabra Azul?

> Realizar una función llamada **imprimirAzul4** que muestre por consola **4 veces** la palabra **Azul**