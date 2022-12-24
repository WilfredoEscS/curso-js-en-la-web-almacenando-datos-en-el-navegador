**:date: 22/12/2022**
**:label: #JavaScript #WebStorage #LocalStorage** 
# Actualización de datos en pantalla
## :bulb:Ideas clave
- ### Recrear tareas
- ### Extraer información del almacenamiento del navegador 
- ### Recorrer el Local Storage 
## :notebook:Notas
Para que las tareas continúen mostrándose en pantalla al volver a iniciar la página hay que crear los elementos utilizando la información almacenada en `localStorage`
Primero obtenemos el arreglo con la información guardada en el `localStorage`
```JavaScript
const taskList = JSON.parse(localStorage.getItem("tasks")) || [];
```
Recorremos el arreglo y por cada elemento de este se crea una tarea en la lista utilizando la información del elemento para rellenar los datos de cada una
```JavaScript
const list = document.querySelector("[data-list]");
taskList.forEach((task) => {
    list.appendChild(createTask(task));
  });
```
Para que este proceso se ejecute al iniciar y recargar la pagina hay que importarlo en el **scope global** del script principal
## :memo: Resumen
1. Para que las tareas se muestren en la lista al abrir la página, hay que crearlos automáticamente usando la información del Local Storage
2. Recorriendo el arreglo con un bucle y creando la tarea por cada elemento
3. La idea no es guardar los elementos que se muestran en pantalla, sino la información que contienen, para poder recrearlos posteriormente utilizando esa información 