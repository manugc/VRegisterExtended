# VRegisterExtended

Métodos adiciones para facilitar el manejo de registro.

### find
Método para buscar un registro concreto.

```VRegister.prototype.find = function(indice, arrayParts, searchMode)```

Descripción de parámetros y valores por defecto.
indice: Índice que se usará para la búsqueda. (ID)
arrayParts: array con las partes a resolver ([])
searchMode: Tipo de búsqueda. (VRegister.SearchThis)

Devuelve el registro encontrado o false

```
registro.find("ID",[1]);
```

### set
Método para establecer el valor de los campos

```VRegister.prototype.set = function(data)```

Descripción de parámetros y valores por defecto.
data: JSON con los campos y dato a establecer

```
registro.set({
    ID: 1,
    NAME: "MANU"
});
```

### add
```VRegister.prototype.add = function(data, indice, indicePartes, searchMode)```

Método para añadir un nuevo registro.

Descripción de parámetros y valores por defecto.
data: JSON con los campos y dato a establecer
indice: Índice que se usará para la búsqueda. (ID)
arrayParts: array con las partes a resolver ([])
searchMode: Tipo de búsqueda. (VRegister.SearchThis)

Devuelve el registro encontrado o false

```
var data = {
    ID: 1,
    NAME: "MANU"
}
registro.add(data);
```

### update
```VRegister.prototype.update = function(data)```

Método para modificar un nuevo registro. La variable ya debe contener un registro tipo VRegister.

Descripción de parámetros y valores por defecto.
data: JSON con los campos y dato a establecer

Devuelve true o false.

```
var data = {
    ID: 1,
    NAME: "MANU"
}
registro.find("ID",[1])
registro.update(data);
```

### create
```VRegister.prototype.create = function(data, indice, indicePartes)```

Método para añadir o modificar un registro según si existe o no previamente.

Descripción de parámetros y valores por defecto.
data: JSON con los campos y dato a establecer
indice: Índice que se usará para la búsqueda. (ID)
arrayParts: array con las partes a resolver ([])

Devuelve el registro creado o modificado.

```
var data = {
    ID: 1,
    NAME: "MANU"
}
registro.create(data, "ID", [1]); // Modifica el registro con ID = 1
```
