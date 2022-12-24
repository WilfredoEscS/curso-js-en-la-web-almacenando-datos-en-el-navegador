# Transformando formato de fecha
---
#MomentJs #Biblioteca #Fecha #JavaScript 
## Ideas clave
---
### Referencia y uso de bibliotecas |  Transformando formato de fecha
## Notas
---
##### Bibliotecas
Una biblioteca es un conjunto de implementaciones previamente 
creadas que estan disponibles para facilitar realizar tareas  o utilizar 
funcionalidades de manera mas eficiente

Las bibliotecas son referenciadas como scripts pero con una URL a la web donde esta alojada
```HTML
  <script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.29.4/moment.min.js"></script>
```

##### Moment.js[ ](https://momentjs.com/)
Es una biblioteca de JavaScript que trabaja con fechas en el 
navegador
Cuenta con muchos formatos de fecha predefinidos pero es posible
personalizarlo
```JavaScript
console.log(moment("20221220").format("DD/MM/YYYY"));
//20/12/2022
```
Hay bibliotecas mas modernas que son mejores alternativas a moment y hasta los desarrolladores recomiendan no implementarla en proyectos nuevos[ ](https://momentjs.com/docs/#/-project-status/)
## Resumen
---
Las librerías facilitan la implementación de nuevas funciones o 
características al proyecto
Una de las funciones de Moment.Js es definir el formato en el que se 
muestra la fecha 
Hay mejores alternativas a esta biblioteca