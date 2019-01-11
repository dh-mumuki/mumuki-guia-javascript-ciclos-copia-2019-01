Hasta ahora nos enfocamos en comprender que el `for` nos sirve para repetir una acción X cantidad de veces.
En este ejercicio nos vamos a enforcar en la acción.
Hasta este momento solo imprimíamos por pantalla la palabra "Azul", ahora vamos a hacer algo más avanzado y la idea sería utilizar el `for` para obtener el resultado de una operación realizada una cantidad de veces.

Si quisiéramos contar cuantas calorias tienen 3 empanadas y cada empanada tiene 300 calorias, podríamos hacer dos cosas, una sería multiplicar, y otra sería sumar 3 veces 300 calorias.

Para hacer esto en código primero necesitamos hacer un `for` que se ejecute 3 veces:


```javascript
for(var i = 0; i < 3; i++) {
   //Hacer la sumatoria
}
```

Para hacer la suma, uno podría llega a sacar la siguiente conclusión:

```javascript
for(var i = 0; i < 3; i++) {
   var totalCalorias = totalCalorias + 300;
}
```

Donde por cada iteración estamos diciendo que el "totalCalorias" es igual al valor que había en "totalCalorias" más 300, de esta manera podríamos obtener el total de los valores.

Este código si bien parece que funcionaría si lo ejecutamos, no nos va a dar el valor que esperamos, por qué?

Esto se debe a que la variable "totalCalorias" está declarada dentro del `for` y esto trae dos consecuencias:

* La variable no existe / no puede ser llamada por fuera del for

```javascript
for(var i = 0; i < 3; i++) {
   var totalCalorias = totalCalorias + 300; //la variable totalCalorias esta declarada dentro del for y sólo puede ser usada ahí dentro
}

console.log(totalCalorias) //la variable totalCalorias acá ya no existe y no puede ser consultada
```

* La variable es inicializada cada vez que se ejecuta una iteracion del for

Dentro del `for` esta el código que queremos que se ejecute en CADA ITERACION, por lo cual en CADA ITERACION se vuelve a ejecutar el mismo código.
Por consecuencia, la primera vez que se ejecute el `for`

```javascript
   var totalCalorias = totalCalorias + 300; //totalCalorias podría terminar valiendo 300
}
```

Y la segunda vez que se ejecuta dentro del `for`

```javascript
   var totalCalorias = totalCalorias + 300; //Estamos volviendo a declarar la variable totalCalorias, por lo cual no logramos almacenar el valor anterior.
}
```

Cómo solucionamos esto?

Esto esta relacionado con la existencia de las variables, la variable totalCalorias es local al `for`, y por ende sólo la podemos usar ahí y se resetea por cada iteración. Si queremos mantener el valor por fuera de cada iteración, debemos hacer que esta varible sea global al `for`. Esto lo logramos de manera sencilla declarando la variable totalCalorias por fuera del `for`.

```javascript
var totalCalorias = 0; //Acá aprovecho e inicializo en 0 la variable totalCalorias.

for(var i = 0; i < 5; i++) {
  totalCalorias = totalCalorias + 0.25; //acá la variable, como ya esta declarada por fuera del for, puede ser modificada durante las iteraciones y no se "reinicia"
}

console.log(totalCalorias) //la variable totalCalorias acá ya existe y nos devuelve el valor total que buscábamos.
```

> Sabiendo esto, escribí una función `sumar5MonedasDe25Centavos`, que sume el valor de 5 monedas de 0.25 centavos y retorne el resultado.

Por ejemplo: 
> 
> ```javascript
> ム sumar5MonedasDe25Centavos()
> 1.25
> ```
> Esto hizo 0.25+0.25+0.25+0.25+0.25