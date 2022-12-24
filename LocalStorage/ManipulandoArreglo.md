# Manipulando Arreglo
---
#WebStorage #JavaScript #Objetos #JSON #LocalStorage
## Ideas clave
---
### Almacenar datos en un arreglo | Evitar sobreescritura
## Notas
---
Para agregar la información en vez de sobrescribirla, empezamos creando un arreglo para almacenar los objetos 
```JavaScript
const taskList = [];
```
Luego se agregan los objetos al arreglo
```JavaScript
taskList.push(taskObj);
```
Y se guarda el arreglo en local Storage
```JavaScript
localStorage.setItem(task, JSON.stringify(taskList));
```
## Resumen
---
Al almacenar los objetos en un arreglo y almacenar este en Local Storage se 
evita la sobreescritura de los datos, sin embargo al refrescar la pagina los 
datos se limpian también.