**📅 Viernes, 23 de diciembre de 2022 15:45**
**🏷️ #JavaScript #Arreglos #Métodos **
# Ordenando arreglos
## 💡Ideas clave
- ### Ordenar arreglo con el método `arrary.sort()`
- ### Funciones de comparación
## 📓Notas
El método **`sort()`** ordena los elementos de un arreglo localmente y devuelve el arreglo ordenado
Sintaxis
```JavaScript
array.sort([compareFunction])
```
`compareFunction` define el modo de ordenamiento, hace uso de dos elementos de comparación (`a`,`b`)
Para comparar números la función de comparación puede simplemente restar `b` de `a`
```JavaScript
//Retorna las fechas en orden ascendente
dates.sort((a, b) => {
  const firstDate = moment(a, "DD/MM/YYYY");
  const secondDate = moment(b, "DD/MM/YYYY");
  return firstDate - secondDate;
});
```
Si se invierte la resta el orden cambia a descendente
## 📝Resumen
1. El método `sort()` toma los elementos de un arreglo y lo devuelve ordenado
2. EL `compareFunction` define el modo de ordenamiento, este parámetro es opcional 
3. Éste posee dos parámetros, entre los que se realiza la comparación y define el orden de los elementos
4. Al comparar números se puede definir el orden con una resta