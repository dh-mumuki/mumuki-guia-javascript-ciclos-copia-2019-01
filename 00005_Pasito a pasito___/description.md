Antes de seguir avanzando con el `for`, tratemos de analizar bien qué es lo que sucede adentro del mismo.
Ya sabemos que ejecuta el código que nosotros le pedimos mientras se cumpla una determinada condición.

El `for` tiene una variable que va cambiando, y esta es `i`. Es importante entender el comportamiento de esta. Recordemos del apartado anterior que el valor `i` se va incrementando a medida que va iterando. 

```javascript
for(var i = 0; i < 4; i++) {
   console.log("Hola!")
}
```

> Sabiendo esto, escribí una función `pasitoAPasito`, que imprime 5 veces el contenido de i.
Por ejemplo: 
> 
> ```javascript
> ム pasitoAPasito()
> "01234"
> ```
> Esto hizo un console.log(valor) por cada iteracion.