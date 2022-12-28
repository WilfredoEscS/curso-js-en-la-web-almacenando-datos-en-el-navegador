**📅 Viernes, 23 de diciembre de 2022 17:21**
**🏷️ #JavaScript #Métodos #UUID #Biblioteca**
# Tareas completas en el Storage
## 💡Ideas clave
- ### Identificadores únicos
- ### Buscar elemento en un arreglo
## 📓Notas
#### findIndex()
El método [`findIndex()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex) devuelve el **índice** del **primer elemento** de un array que cumpla con la función de prueba proporcionada. En caso contrario devuelve -1.
```JavaScript
//Obtiene un string tipo JSON y lo transforma en un objeto de JavaScript 
const tasks = JSON.parse(localStorage.getItem("tasks"));
//devuelve el indice del objeto cuya valor de la clave "id" es igual al parametro del mismo nombre
const index = tasks.findIndex((item) => item.id === id);
```
#### Alternar valores
Es posible alternar el valor booleano de un elemento con el operador de negation `!`
```JavaScript
//Si el valor es "true" lo torna en "false" y viceversa 
tasks[index]["complete"] = !tasks[index]["complete"];
```
#### Identificadores únicos 
Existe una biblioteca que genera identificadores únicos , para usarla basta con instalarla o referenciarla en el proyecto y llamar a los métodos y obtienes el identificador
```javascript
uuid.v1();// UUID v1: 5c4bfd70-8336-11ed-bc31-9553e0acad85
uuid.v4();// UUID v4: db77eaa2-e289-4c04-9f3b-61b62989c9b6
```
Son muy útiles cuando se gestionan varios elementos y es necesario diferenciarlos unos de otros
Enlace al repo de la biblioteca:[GitHub - uuidjs/uuid](https://github.com/uuidjs/uuid?utm_source=cdnjs&utm_medium=cdnjs_link&utm_campaign=cdnjs_library) 
## 📝Resumen

Para marcar o desmarcar la tarea como completa fue necesario guardar nuevos datos en el Local Storage primero un identificador para diferenciarlos y el estado de la tarea(si esta completa o no), el ultimo se alternaria del mismo botón de la tarea. Luego definir que al iniciar la aplicación esta leyera esos datos, relacionara el elemento html cons su respectiva información en el Local Storage y de esta forma le aplicara los estilos correspondientes a la tarea, para ellos se hizo uso de varios métodos de manipulación de arrays y una biblioteca para generar los identificadores 