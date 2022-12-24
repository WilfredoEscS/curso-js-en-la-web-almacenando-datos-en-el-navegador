**📅 viernes, 23 de diciembre de 2022 8:09**
**🏷️ #JavaScript #Métodos #PalabrasReservadas**
# Validación de tareas 
## 💡Ideas clave
### Validar inputs vacíos 
## 📓Notas
Una manera interrumpir una función para una situación especifica es agregar un condicional con un `return`
```JavaScript
//Si alguno de las variables esta vacía, se ejecuta un return
if (value === "" || date === "") {
    return;
  }
```
 Aunque no retorne nada detiene a ejecución del código 
## 📝Resumen
La palabra reservada `return` no solo devuelve un valor de la función cuando es necesario, también permite detener la ejecución de la misma si la incluimos en un condicional