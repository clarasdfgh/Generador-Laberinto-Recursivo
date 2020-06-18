# Generador-Laberinto-Recursivo
Generador recursivo de laberintos perfectos. En un laberinto perfecto... 
- Todos los caminos están conectados entre sí: no tiene zonas inalcanzables
- Todos los puntos están conectados por un único camino: no tiene ciclos

Se distingue de otros generadores en su simplicidad: no es un enfoque de casillas con cuatro paredes, sólo una matriz de enteros en la que 1 == pared y 0 == pasillo.
<br/>
<br/>
Lo subo porque: 
1. No encontré ningún generador de laberintos en matrices de 0 y 1
2. Es una cosita guay que igual me viene bien más adelante
3. Me sirvió para reforzar lo que sabía sobre recursividad
4. *Me da la gana*

### Algunos laberintos:
```
0101010     0101010     0101010
0000000     0100000     0000010
0101110     0101110     0101110
0100010     0100010     0100000
0111011     0111110     0111111
0100000     0000000     0000000
0101010     0101010     0101010
```

Puedes ver como se resuelven en el repo de [Algorítmica](https://github.com/clarasdfgh/ALG/tree/master/P5)
<br/>
<br/>
Como todos terminan teniendo las 4 esquinas descubiertas, existe la posibilidad de combinarlos en una cuadrícula e incluso rotarlos para conseguir más variedad. Quizá me ponga este verano, pero requiere cierto estudio ver cómo superponerlos sobre una cuadrícula:
- La cuadrícula tendría que estar compuesta por habitaciones n\*n para que siguieran siendo pasillos (de otra forma se generarían "habitaciones" de ceros y "bloques" de unos)
- Las habitaciones tendrían que estar conectadas por puertas de forma que se siguieran cumpliendo las características de un laberinto perfecto
  - Y realmente, crear ese recorrido por habitaciones sería exactamente lo mismo que estamos intentando hacer con los pasillos del laberinto. 
  - *That's recursion, babey!!!* 

Así que, realmente, lo mejor para todos sería que arreglara los segfault. Así es la vida, pero el tema de la cuadrícula también me resulta lo suficientemente interesante como para mencionarlo como posibilidad. Además, probablemente haya un umbral a partir del cual sea mucho más rápido generar un puñado de laberintos pequeños, rotarlos y encajarlos en la cuadrícula, que generar un laberinto grande directamente. 

Pero bueno, que me enrollo. La conclusión es que quizá arregle los segfault, quizá haga la cuadrícula o quizá nunca más abra este repo. Ni siquiera tengo todavía la nota de la práctica a la que pertenece esto. Pero la verdad es que estaría guay poder tener un repo bonito y completo con algo útil, para variar. Realmente escribo esto para que, en el caso de que no lo toque más, al menos las conclusiones que he sacado queden en algún lado; y porque no quiero hacer cosas que debería estar haciendo. *En fin*.

<br/>
<br/>

###### Probablemente está plagado de errores (partiendo de que si n>7 da segfault....)
