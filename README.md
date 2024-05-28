# display-grid

grid permite dar estructura a cualquier caja que imaginemos en filas y columnas con mucha libertad.

# grid-template-columns

permite indicar cuantas colums necesita y su respectiva medida en un contenedor con grid.

```
  display: grid;
  grid-template-columns: 25% 50% auto;
```

los elementos que no caben los va tirando por debajo creando filas auto, si desea tomar control de las filas tenemos...

# grid-template-rows

permite indicar cuantas filas necesita y su respectiva medida

# gap

usar margin es muy mala idea. gap permite dar espaciados de forma confiable entre los elementos de la grid.

tener algo como esto es de cuidado

```
  grid-template-columns: 25% 25% 50%;
```

lo anterior indica que la fila 1 del grid ocupará el 100% de su padre y no tendrá en cuenta lo que se haya puesto de gap o tamaño de borde. para evitar calculos es recomendable poner al menos 1 medida "automática"

```
  grid-template-columns: 25% 25% auto;
```

# fr

esta medida sirve para que el navegador calculé por nosotros cuando medirá cada fila o colum. viene de fracción.

por ej:

```
  grid-template-columns: 1fr 2fr 1fr;
```

el navegador ve el espacio disponible y lo divide entre las colums que hay, y a cada una le asigna la fr correspondiente. la primera y ultima colum le da 1 parte y a la segunda 2 partes.

# repeat(3, 1fr);

permite indicar de golpe: cantidad de colums y valor de cada una, el valor puede ser un patrón. igualmente funciona con filas.

```
grid-template-columns: repeat(3, 1fr);
```
