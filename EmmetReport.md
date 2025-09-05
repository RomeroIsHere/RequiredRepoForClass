# Reporte de Abreviaciones Emmet

###### Guillermo Romero Cuevas

Se vio la Sintaxis Necesaria para Crear HTML mediante Abreviaciones Emmet, Las cuales Pueden Aumentar la velocidad de desarollo de una Pagina web, quitando la necesidad de escribir Codigo de Boilerplate manualmente.

## Simbolos Especiales
- `tag` Cualquier Texto simple se toma como un Tag de HTML, automaticamente detectando si Necesita un Par de cerrado o si es Auto Cerrada (`<p></p>` vs `<input/>`).
- `>` Indica que Lo siguiente a escribirse se encuentra dentro de la Tag Anterior 'Bajando un nivel' para rellenar las Tags de Par Cerrador
```html
<!-- La siguiente Abreviacion Emmet Genera la estructura HTML Posterior -->
<!-- body>div>div>p -->
<body>
    <div>
        <div>
            <p></p>
        </div>
    </div>
</body>
```
- `+` es una Señal de composición, con el significado que Las Tags Posteriores deben de Estar al Mismo Nivel que La tag Anterior, pero en Orden consecutivo
```html
  <!-- h1+h2+h3+h4+h5+h6 -->
    <h1></h1>
    <h2></h2>
    <h3></h3>
    <h4></h4>
    <h5></h5>
    <h6></h6>
```
- `*` Indica Repeticion de la Estructura anterior, Repitiendo la Estructura Interna Posterior si es Necesario
- `^` 'Sube' de Nivel en el arbol de HTML, Permitiendo componer estructuras Internas Complejas, con Estructuras Adicionales en el Posterior de este Mismo simbolo
- `{text}` Permite Insertar Texto 'text' en la Ultima Tag que lo permita. Es Equivalente a Rellenar mediante innerhtml con JS.
- `$` Es un Numero Iterador, que sube de Valor con la Repeticion * de Nivel Mas Cercano. se puede Repetir tal como `$$$` Para dejar 'Leading Zeroes' (Ceros a la Izquierda)
- `()` Permite alterar el Orden de Operaciones de los Simbolos Anteriores, Permitiendo entidades Mas complejas. Muchas de las cosas que Se Pueden Crear mediante Parentesis tienen un equivalente si se Cambia el Orden de Operadores anteriores, o Mediante Composición mas Compleja
