**ARRAY**

1. .groupBy()

    * El groupBy()es un método para agrupar los elementos de una matriz de llamada de acuerdo con los valores de cadena devueltos por una función de prueba proporcionada. 
    
    * El objeto devuelto tiene propiedades separadas para cada grupo, que contiene matrices con los elementos del grupo.

```javascript
    const inventory = [
    { name: 'asparagus', type: 'vegetables', quantity: 5 },
    { name: 'bananas',  type: 'fruit', quantity: 0 },
    { name: 'goat', type: 'meat', quantity: 23 },
    { name: 'cherries', type: 'fruit', quantity: 5 },
    { name: 'fish', type: 'meat', quantity: 22 }
    ];

    let result = inventory.groupBy( ({ type }) => type );

    /* Result is:
    {
    vegetables: [
        { name: 'asparagus', type: 'vegetables', quantity: 5 },
    ],
    fruit: [
        { name: "bananas", type: "fruit", quantity: 0 },
        { name: "cherries", type: "fruit", quantity: 5 }
    ],
    meat: [
        { name: "goat", type: "meat", quantity: 23 },
        { name: "fish", type: "meat", quantity: 22 }
    ]
    }
    */

```

2. .keys()

    * El método keys() devuelve un nuevo objeto Array Iterator que contiene las claves de índice con las que acceder a cada elemento en el array.

```javascript
    const array1 = ['a', 'b', 'c'];
    const iterator = array1.keys();

    for (const key of iterator) {
    console.log(key);
    }

    // expected output: 0
    // expected output: 1
    // expected output: 2
```

3. .splice()

    * El método splice() cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.

```javascript
    const months = ['Jan', 'March', 'April', 'June'];
    months.splice(1, 0, 'Feb');
    // inserts at index 1
    console.log(months);
    // expected output: Array ["Jan", "Feb", "March", "April", "June"]

    months.splice(4, 1, 'May');
    // replaces 1 element at index 4
    console.log(months);
    // expected output: Array ["Jan", "Feb", "March", "April", "May"]
```