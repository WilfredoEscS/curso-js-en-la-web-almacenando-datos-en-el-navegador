# API de fecha de JavaScript 
---
#Fecha #API #Fecha #Métodos 
## Notas
---
Los navegadores permiten que nos comuniquemos con ellos a través 
de una interface con una lista de métodos de objetos accesibles con 
JavaScript.

El objeto llamado [`Date`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Date) devuelve varios datos de la fecha
```javascript
const data = new Date()
\\Tue Dec 20 2022 11:27:55 GMT-0600 (hora estándar central)
```
Para editar esa información para un formato distinto podemos utilizar el
método [`toLocaleDateString:`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)
```JavaScript
date.toLocaleDateString("es-MX")
//"20/12/2022"
```
Tambien puede configurarse de que manera se representan los elementos de la fecha
```JavaScript
const dataOptions = {
  weekend: "long",
  year: "numeric",
  month: "long",
  day: "numeric",
};
date.toLocaleDateString("es-MX", dataOptions);
//"20 de diciembre de 2022"
```
[`toLocaleTimeString()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString) muestra el horario del navegador
```JavaScript
date.toLocaleTimeString();
//11:44:55
```
Y es configurable al igual que la fecha
```JavaScript
const horarioOptions = {
   hour12: false,
   hour: 'numeric',
   minute: '2-digit',
   second: '2-digit', 
   timeZone: 'America/Sao_Paulo'
}
```
Es posible combinar todas esas opciones utilizando el método 
[`toLocaleString()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)
```JavaScript 
data.toLocaleString('es-MX', {
   ...dataOptions, 
   ...horarioOptions
})
//“28 de agosto de 2020 9:04:54”
```
`Intl.DateTimeFormat` es un constructor, recibirá informaciones iniciales 
de cómo queremos que la fecha esté formateada.
```javascript
const formataData = new Intl.DateTimeFormat('es-MX', {
   ...dataOptions,
   ...horarioOptions
})
```
llamando el método `format()` podemos formatear diferentes fechas 
caso sea necesario.
```JavaScript 
formataData.format(data)
// 20 de diciembre de 2022, 17:03:21
```
