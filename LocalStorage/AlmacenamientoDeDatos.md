# Almacenando Datos 
---
#JavaScript #Objetos #WebStorage #JSON #LocalStorage
## Ideas clave
---
### Tipos de almacenamiento en el navegador | 
## Notas
---
##### Web Storage API[ ](https://developer.mozilla.org/es/docs/Web/API/Web_Storage_API)
Permite que el navegador almacene información de tipo **clave/valor**, 
de una forma mucho más intuitiva que utilizando cookies.

Para almacenar datos en el navegador empezamos por identificar la 
información que queremos guardar 
En nuestro gestor de tareas nos importa la tarea y la fecha de esta
```JavaScript
//Tarea:Curso de JavaScript 
const value = input.value;
//Fecha:27/12/2022
const dateformat = moment(date).format("DD/MM/YYYY");
```
Y se almacenan en un objeto
```JavaScript
 const taskObj = {
    value,
    dateformat,
  };
```
Pero como lo necesitamos en formato `string` hacemos uso 
[`JSON.stringify()`](https://developer.mozilla.org/es/docs/Learn/JavaScript/Objects/JSON#conversiones_entre_objetos_y_texto) Para convertirlo el objeto de JavaScript en una 
cadena `JSON`
```JavaScript
console.log(JSON.stringify({ x: 5, y: 6 }));
// expected output: "{"x":5,"y":6}"
```
`sessionStorage.setItem()` permite acceder a un objeto [`Storage`](https://developer.mozilla.org/es/docs/Web/API/Storage) 
asociado a la sesión actual, la information que almacena es eliminada 
al finalizar la sesión de la página
```JavaScript 
  sessionStorage.setItem("task", JSON.stringify(taskObj));
```

## Resumen
---
Session Storage permite guardar información en el navegador hasta 
que este se cierra y finaliza la sesión
JSON es un tipo de dato string con la estructura de un objeto de JavaScript 