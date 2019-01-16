# Evaluación
En este apartado se agrupan distintas evaluaciones para comprobar tus conocimientos.

Para evaluaciones prácticas mira en los distintos exámenes (pondré el de esta semana cuando haya acabado el exámen).

Para teoría pueden servirte de repaso las siguientes preguntas:
1. Diferencias al comparar entre `foo = bar`, `foo == bar` y `foo.equals(bar)`
'foo=bar ' ; se utiliza el operador de Asignación "=" . Se esta dando a foo el valor de bar;
'foo ==bar' ; Se utiliza el operador binario de comparación "==" : igual que, cuyo resultado es un boolean. Devolverá true cuando sus dos variable operandos apunten al mismo objeto/valor.
'foo.equals (bar)'; Se utiliza el método "equals" que bebe tener una lógica implementada. Devolverá true solo si el contenido que hemos definido como relevante en "foo" es el mismo que en "bar".

RaulG.

foo = bar. Operador de asignación =. Acceso al mismo objeto mediante distintas variables que almacenan la misma referncia. bar referencia al mismo objeto que foo, de esta manera podemos acceder al objeto de dos maneras, mediante foo o mediante bar. En ambos casos estamos utilizando el mismo objeto.

foo == bar. Operador de igualdad == (ser el mismo). La comparación se hará entre foo y bar (dos variables) y se dirá que es verdadero si apuntan al mismo objeto y sino devolverá falso.  


foo.equals(bar). Metodo equals (Object obj). Compara dos objetos y decide si son iguales, devolviendo true en caso afirmativo y false en caso contrario. Hay que decidir qué significa que bar y foo sean iguales.   

1. Diferencias entre una clase normal, una abstracta y una interfaz.

RaulG.

Clase normal: Una clase es un plano o prototipo a partir del cual se crean los objetos. Una clase modela el estado y el comportamiento de un objeto del mundo real.  

Clase abstracta: Una clase abstracta es una clase que se declara abstracta; puede incluir o no métodos abstractos. Las clases abstractas no pueden ser instanciadas.,pero pueden crearse subclases concretas sobre la base de una clase abstracta, y crear instancias de estas subclases. Para ello hay que heredar de la clase abstracta y anular los métodos abstractos, es decir, implementarlos.

Si una clase incluye métodos abstractos, entonces la clase misma debe ser declarada abstracta.

Interfaz: una interfaz es un tipo de referencia, similar a una clase, que puede contener solo constantes, firmas de métodos, métodos predeterminados, métodos estáticos y tipos anidados. Los cuerpos de método existen solo para métodos predeterminados y métodos estáticos. Las interfaces no pueden ser instanciadas, solo pueden implementarse por clases o extenderse por otras interfaces.

1. ¿Qué relación tiene el concepto "erasure" con la definición de clase:
`class MiClase implements Comparable<String>, Comparable<Integer> {...}`? Explícalo.

Quique
Type erasuse consiste en que en tiempo de ejecución se pierde la información de los tipos genéricos y para la máquina virtual no son distintos de un tipo no genérico, es un proceso que realiza el compilador. 

JuliusCMM
# TYPE ERASURE
Los genéricos se introdujeron en Java para proporcionar control de tipo más estricto durante la compilación y para dar cabida a la programación de tipos genéricos.
Para implementar genéricos, el compilador de Java aplica el TYPE ERASURE de la siguiente forma:

	1. Reemplaza todos los parámetros genéricos delimitados (bounded generics) como "T extends Comparable<T>>" por su propio límite.
		public class Node<T extends Comparable<T>> {
			private T data;
			private Node<T> next;

			public Node(T data, Node<T> next) {
				this.data = data;
				this.next = next;
			}
			public T getData() { return data; }
			// ...
		}
		
		queda tras el TYPE ERASURE como:
		
		public class Node {
			private Comparable data;
			private Node next;

			public Node(Comparable data, Node next) {
				this.data = data;
				this.next = next;
			}
			public Comparable getData() { return data; }
			// ...
		}
	1. Reemplaza todos los parámetro genéricos no delimitados (bounded generics) como "T, E, K, V" por Object (base de la jerarquía de objetos en java).
		public class Node<T> {
			private T data;
			private Node<T> next;

			public Node(T data, Node<T> next) {
				this.data = data;
				this.next = next;
			}

			public T getData() { return data; }
			// ...
		}
		
		queda tras el TYPE ERASURE como:
		
		public class Node {
			private Object data;
			private Node next;

			public Node(Object data, Node next) {
				this.data = data;
				this.next = next;
			}

			public Object getData() { return data; }
			// ...
		}
	1. Inserta conversión explícita de tipos (cast) si se necesita preservar la seguridad de tipos.
	1. Inserta métodos puente (bridge methods) que son métodos sintéticos generados por el compilador con el objetivo de preservar el polimorfismo en tipos genéricos extendidos.

El borrado de tipos garantiza que no se creen nuevas clases para tipos parametrizados; en consecuencia, los genéricos no incurren en gastos extra durante el tiempo de ejecución.
El bytecode(*.class) producido, por lo tanto, contiene solo clases ordinarias, interfaces y métodos.
------------------------------------------------------------------------------------------------------------------------------------



Hay un par más, pero como llevan código que si escribis en Eclipse os va a decir si hay fallos o no, esas no puedo darlas hasta el examen `¯\_(ツ)_/¯`
También pondré las respuestas de todas.
