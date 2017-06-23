# Tutorial sobre Markdown

# Índice

1. [¿Qué es Markdown?](#markdown)
2. [Sintaxis](#sintaxis)
	1. [Cabeceras](#cabeceras)
	2. [Enlaces](#enlaces)
	3. [Imágenes](#imagenes)
	4. [Citas](#citas)
	5. [Listas](#listas)
	6. [Tablas](#tablas)
	7. [Escapar caracteres](#escapar)
	8. [Cabeceras enlazadas](#anidadas)

---

# ¿Qué es Markdown? {#markdown}

Ligero y fácil de usar a la par que intuitivo, es un lenguaje de marcas de texto plano, limpio y sencillo sin necesidad de etiquetas o elementos parecidos.

# Sintaxis {#sintaxis}

La sintaxis utilizada por Markdown es fácil de recordar.

## Cabeceras {#cabeceras}

Las cabeceras en Markdown son sencillas, sabiendo que existen 6 tipos de cabeceras y éstas en Markdown se definen por la almohadilla (\#), vemos algunos ejemplos:

	# Cabecera de tipo 1 
	## Cabecera de tipo 2
	### Cabecera de tipo 3
	#### Cabecera de tipo 4
	##### Cabecera de tipo 5
	###### Cabecera de tipo 6

---

## Enlaces {#enlaces}

Para definir enlaces en Markdown, deberemos de hacerlo cómo vemos a continuación:

	[Texto a mostrar](dirección del enlace "Titulo alternativo")

Dónde:

- Texto a mostrar: será el texto del enlace, es decir, el texto que aparecerá y se verá de la siguiente forma [Ejemplo](https://www.google.com)
- Dirección del enlace: será la URL.
- Titulo alternativo: será el texto que aparece cuando posicionamos el ratón encima del enlace [Google](https://www.google.com "Ejemplo")

Otra alternativa para definir un enlace en Markdown sería de la siguiente manera:

	[Ejemplo1][ej1], [Ejemplo2][ej2]

	[ej1]: https://www.google.com "Google.com"
	[ej2]: https://www.google.es "Google.es"

[Ejemplo1][ej1], [Ejemplo2][ej2]

[ej1]: https://www.google.com "Google.com"
[ej2]: https://www.google.es "Google.es"

O si no queremos que aparezca ningún texto, es decir, sólo la URL:

	<https://www.google.com>

Ejemplo: <https://www.google.com>

---

## Imágenes {#imagenes}

Es prácticamente igual que la creación de enlaces a diferencia que en el enlazado de imágenes se define el cierre de la exclamación (!) al principio, ejemplo:
	
	![Google](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/1200px-Google_2015_logo.svg.png "Imagen 1")

Así se vería:
![Google](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/1200px-Google_2015_logo.svg.png "Imagen 1")

---

## Citas {#citas}

Para crear una cita con Markdown es bastante sencillo y fácil de recordar, tan sólo deberemos de introducir el símbolo > delante de lo que vayamos a citar, ejemplo:

	> Cita de alguien célebre.

Vista:
> Cita de alguien célebre.

Podemos hacer subcitas, agregando doble símbolo >, un ejemplo:

	>> Subcita de alguien célebre

Vista:
>> Subcita de alguien célebre.

---

## Listas {#listas}

Las listas que tiene son dos, listas ordenadas y no ordenadas.

Las ordenadas se definen mediante número enteros (1,2,3,4...) y las no ordenadas mediante un guión (-), asterisco (*) o suma (+). 

Las listas no ordenadas admiten los tres símbolos simultáneamente.

Ejemplo de ordenadas:

	1. Número 1
	2. Número 2
		1. Número 2.1
			1. Número 2.1.1
				1. etc...

Vista:

1. Número 1
2. Número 2
	1. Número 2.1
		1. Número 2.1.1
			1. etc...

Ejemplo de listas no ordenadas:

	- Número 1
	* Número 2
		+ Número 2.1
			- Número 2.1.1
				- etc...

Vista:

- Número 1
* Número 2
	+ Número 2.1
		- Número 2.1.1
			- etc...

---

## Tablas {#tablas}

La sintaxis de las tablas es sencilla. Primero deberemos de definir los elementos principales de las columnas y separarlos con |. También podemos alinear los elementos de toda la columna completa hacía la derecha, izquierda o centro (por defecto) con la ayuda de los dos puntos (:) definidos antes de los dos guiones (--)

Ejemplo

<pre>
Elemento1 | Elemento2 | Elemento 3
:--|--|--:
Contenido elemento1 | Contenido elemento2 | Contenido 3
</pre>

Vista:
Elemento1 | Elemento2 | Elemento 3
:--|--|--:
Contenido elemento1 | Contenido elemento2 | Contenido elemento 3

---

## Escapar caracteres {#escapar}

Podemos escarpar caracteres con la ayuda de la barra invertda o backslash ( \\ ). Ejemplo:

	\> Esto debería ser una cita, pero no lo es al escapar el símbolo >
    
Vista:

\> Esto debería ser una cita, pero no lo es al escapar el símbolo >

---

## Cabeceras anidadas {#anidadas}

Las cabeceras anidadas nos permiten la navegación dentro del propio fichero de Markdown con facilidad. 

Ejemplo:

	# Cabecera1 {#cabeceraanidada1}
	[Cabecera1](#cabeceraanidada1)

Vista:

#### Cabecera1 {#cabeceraanidada1)
[Cabecera1](#cabeceraanidada1)
