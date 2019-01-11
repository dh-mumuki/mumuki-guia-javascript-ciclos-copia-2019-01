Con las ejercitaciones previas vimos cómo usar el `for` para ejecutar una acción una cantidad de veces fija y variable y cómo hacer algún procesamiento dentro del mismo.

En el ejercicio anterior supimos como calcular la sumatoria de 5 monedas de 25 centavos.
La idea sería que logremos hacer una función que calcule la sumatoria de cualquier cantidad de monedas.

Para esto vamos a expandir el ejemplo de las empanadas anterior en el cual calculabamos las calorías de 3 empanadas.

```javascript
var totalCalorias = 0; 

for(var i = 0; i < 3; i++) {
  totalCalorias = totalCalorias + 300;
}

console.log(totalCalorias)
```

Para lograr esto, lo que tenemos que modificar es algo similar al ejercicio 2 de Variables Repetidas.

Primero tenemos que sacar el numero 3 y hacer que este sea variable, por ejemplo "x" o "cantidadDeEmpanadas"

```javascript
var cantidadEmpanadas = 3;
var totalCalorias = 0; 

for(var i = 0; i < cantidadDeEmpanadas; i++) {
  totalCalorias = totalCalorias + 300;
}

console.log(totalCalorias)
```
Luego de hacer esta modificación, la variable cantidadEmpanadas podría ser un argumento de una función.

```javascript
function caloriasDeEmpanadas(cantidadDeEmpanadas){
  var totalCalorias = 0; 

  for(var i = 0; i < cantidadDeEmpanadas; i++) {
    totalCalorias = totalCalorias + 300;
  }

  console.log(totalCalorias)
}
```

Y de esta manera logramos hacer nuestra función, que al pasarle la cantidad de empanadas, esta imprime por pantalla la cantidad de calorías totales.

Te proponemos una última modificación. En vez de hacer que la función imprima, vamos a hacer que esta función **devuelva** un valor, para eso vamos a utilizar el `return`.  


```javascript
function caloriasDeEmpanadas(cantidadDeEmpanadas){
  var totalCalorias = 0; 

  for(var i = 0; i < cantidadDeEmpanadas; i++) {
    totalCalorias = totalCalorias + 300;
  }

  return totalCalorias;
}
```

> Sabiendo esto, escribí una función `sumarMonedasDe25(cantidadDeMonedas)`, que tome como parámetro un valor numérico y devuelva la sumatoria de las monedas de 25 centavos.
Por ejemplo: 
> 
> ```javascript
> ム sumarMonedasDe25(7)
> 1.75
> ```
> Esto hizo 0.25+0.25+0.25+0.25+0.25+0.25+0.25