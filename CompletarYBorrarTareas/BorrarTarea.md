**📅 Viernes, 23 de diciembre de 2022 21:11**
**🏷️ #JavaScript #Arreglos #Métodos #LocalStorage **
# Eliminación de tareas
## 💡Ideas clave
- ### Eliminar elementos de un arreglo
- ### Actualizar Local Storage  
## 📓Notas
#### array.splice()
Modifica el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.
```JavaScript
array.splice(start[, deleteCount[, item1[, item2[, ...]]]])
```
`start` es el índice desde donde empezara a cambiar el arreglo, si es negativo inicia desde el final del arreglo
`deleteCount` (opcional) indica el numero de elementos a eliminar
`item` (opcional) los elementos que se añaden al arreglo

## 📝Resumen
Para eliminar una tarea, se lee nuevamente el Local Storage, se modifica con el método splice y se sobrescribe el Local Storage con el arreglo actualizado
Esto debe ser representado en la pantalla de la aplicación de manera coherente , para ello se limpian los elementos visuales de la lista y se recrean a partir de la información actualizada del Local Storage, sin el elemento eliminado
Esta acción debe estar asignada al evento click del botón 'borrar tarea'