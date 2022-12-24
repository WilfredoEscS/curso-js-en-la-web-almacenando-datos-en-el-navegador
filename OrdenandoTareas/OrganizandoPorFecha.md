**📅 Viernes, 23 de diciembre de 2022 9:00**
**🏷️ #JavaScript #MomentJs**
# Organizando por fecha 
## 💡Ideas clave
- ### Agrupar elementos por fecha
- ### Filtrar elementos repetidos
## 📓Notas
Crear un arreglo para guardar las fechas que servirán como etiquetas de agrupación 
```JavaScript
const unique = [];
```
Filtrar las fechas repetidas y después almacenarlas en el arreglo
```JavaScript
//Para cada tarea
tasks.forEach((tasks) => {
  //Si el arreglo no la incluye actualmente, agregar la fecha especificada
  if (!unique.includes(tasks.dateFormat)) unique.push(tasks.dateFormat);
  });
```
Retornar el arreglo
```JavaScript 
return unique;
```
Luego para cada fecha:
- Convierte la fecha e un elemento moment
```JavaScript
const dateMomment = moment(date, "DD/MM/YYYY");
```
- Crea un elemento con la fecha 
```JavaScript
    list.appendChild(dateElement(date));
```
- Finalmente verifica entre todas las tareas cuales tienen la misma fecha que ele elemento creado y las agrega debajo de él
```JavaScript
taskList.forEach((task) => {
  const taskDate = moment(task.dateFormat, "DD/MM/YYYY");
  const diff = dateMomment.diff(taskDate);
  if (diff === 0) list.appendChild(createTask(task));
});
```
Este procedimiento agrega las tareas independientemente de si estas ya estan en la lista cuando se ejecuta por lo que se debe inicializar el elemento html como vacío, para agregarlas ordenadas nuevamente
## 📝Resumen
1. La librería moment tiene un método para comparar fechas
2. El método `arreglo.includes(elemento)` evita repetir datos  en el arreglo
3. Repite procesos para varios elementos sutilizando bucles