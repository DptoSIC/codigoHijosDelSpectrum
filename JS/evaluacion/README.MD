# Evaluación
En este apartado se agrupan distintas evaluaciones para comprobar tus conocimientos.

Para evaluaciones prácticas mira en los distintos exámenes:
1. [TragaperraJS](https://github.com/Awes0meM4n/tragaperrajs#tragaperrajs): crea tu máquina tragaperras con JS
1. [EJStudia](https://github.com/Awes0meM4n/EJStudia#examen-javascript---ejstudia): minijuego para concienciar del éxito del estudio constante

Para teoría pueden servirte de repaso las siguientes preguntas:
1. Definición de Javascript (JS) y sus características
1. En términos de reparto de procesamiento ¿Cuál es la ventaja que puede aportar a una gran compañía el uso de JS frente a su ausencia en un sitio web y por qué?
1. ¿Cómo encaja JS con otros lenguajes como HTML y CSS?
1. ¿Qué ventaja ofrece enlazar un fichero JS frente a incrustar el código directamente en el HTML?
1. ¿Para qué podría servirnos usar código incrustado?
1. ¿Cómo puedo invertir el orden de los caracteres de una cadena?
1. Señalar la correcta: Los Arrays permiten almacenar…
   1. Un único tipo de datos igual para todos los elementos desde su creación.
   1.	Mientras esté vacío (`[]`) se puede añadir cualquier tipo pero luego deben ser todos del mismo tipo.
   1.	Se pueden mezclar elementos de cualquier tipo.
1. ¿Si quiero una copia de un Array qué debería hacer?
1. Si modifico un elemento (en sí mismo, no reemplazarlo por otro en su misma posición) en la copia de un Array ¿Queda modificado el elemento del Array original?
1. ¿Qué diferencia hay entre los términos *expresión* y *sentencia*?
1. Si tengo dos variables `var cadena1 = 'prueba'; var cadena2 = 'prueba';` Señale el resultado correcto para el siguiente código:
`alert((cadena1 == cadena2) + ' | ' + (cadena1 === cadena2));`
   1. `true | false`
   1. `false | true`
   1. `true | true`
1. Siguiendo con la pregunta anterior, explique la diferencia entre el resultado anterior y `alert(cadena1 == cadena2 + ' | ' + cadena1 === cadena2);`.
1. ¿Cuál es el resultado de las siguientes expresiones? `var mivariable = 'prueba';`
   1. `window.miVariable + 'true'`
   1. `window.miVariable + 0`
   1. `window.miVariable && true`
1. ¿Qué tipo de nodo devuelven las siguientes expresiones (en el supuesto que devuelven un valor válido)?
   1. `window.document`
   1. `capa = document.querySelector('div')`
   1. `capa.style`
   1. `document.createTextNode('span')`
1. ¿Qué ventajas y desventajas tiene usar `getElementByTagName()` respecto `queryselectorAll()`?
1. ¿Existe alguna forma de guardar datos con JS en el ordenador cliente que abre la página web?
1. ¿Qué diferencias hay entre `EventHandler` y `EventListener`?
1. ¿Qué diferencia hay entre los manejadores `onchange` y `oninput` para un control de formulario?
1. ¿Cómo puedo obtener una referencia al objeto que recibió el evento?
1. ¿Qué objeto obtengo con `event.currentTarget`?
1. ¿Qué ventajas nos ofrece usar el método `addEventListener()` frente a las otras formas de asignar un manejador?
1. Escribe tres ejemplos de tipos de eventos distintos con algún miembro exclusivo de ese tipo

Según este código HTML
```html
<div id="capa" style="color:white">
	Texto en <span><i>cursiva</i></span>
</div>
```
¿Qué relación tienen los siguientes nodos según DOM?
   1. `div` con `span`
   1. `div.id` con `div.style`
   1. `div.id` con `span`
   1. `i` con `span`
   1. “Texto en ” con `i`
   1. “Texto en ” con `span`
   1. `span` con “cursiva”
