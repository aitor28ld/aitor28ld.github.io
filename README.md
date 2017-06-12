# Tutorial de cómo crear nuestra propia Github Pages

---

*Autor*: Aitor León

*Creado*: 30/09/2016

*Contacto*:

- Twitter: [@2Ait8r](https://twitter.com/2Ait8r)
- E-mail: ldaitor28@gmail.com
- Blog: [Open Binary](https://openbinary20.wordpress.com)

---

# Índice

1. [Creación de repositorios en github](https://github.com/aitor28ld/aitor28ld.github.io/tree/master#creación-de-repositorios-en-github)
2. [Creación de plantillas automáticas en Github Pages](https://github.com/aitor28ld/aitor28ld.github.io/tree/master#creación-de-plantillas-automáticas-en-github-pages)
3. [Configuración de los ficheros con extensión Markdown](https://github.com/aitor28ld/aitor28ld.github.io/tree/master#configuración-de-los-ficheros-con-extensión-markdown)
4. [Modificando el código HTML de nuestra Github pages](https://github.com/aitor28ld/aitor28ld.github.io/tree/master#modificando-el-código-html-de-nuestra-github-pages)

---

# Creación de repositorios en Github

Los pasos a seguir para crear nuestro sitio y clonarlo en local son los siguientes:

1. Nos vamos a github y creamos un nuevo repositorio. Este será nuestro sitio web.
2. El repositorio debe de tener el nombre de la siguiente forma:

	```
	<nombre>.github.io
	```

3. Si queremos modificar cualquier fichero en nuestra máquina, podemos clonar el repositorio en local:

	```
	git clone https://github.com/<nombre>/<nombre>.github.io
	```

# Creación de plantillas automáticas en Github Pages

Una vez hemos creado el repositorio:

1. Dentro del repositorio, nos vamos a **Settings**
2. En la misma pestaña de **Options**, desplazamos hacía abajo la página web y pulsamos sobre **Launch automatic page generator**
3. Esto nos llevará a otra página dónde podremos configurar las opciones más básicas de nuestro Github Pages.

	![](http://i.imgur.com/fMKrUKx.png)

4. Modificamos las opciones de dicha página y le damos a **Continue to layouts**
5. Ahora elegiremos una plantilla, la que queramos y finalizaremos la modificación básica de nuestro Github pages.
6. Clonamos dicho repositorio en local y procedemos a configurar los ficheros.

# Configuración de los ficheros con extensión markdown

Con estos pasos, será fácil conseguir que nuestra Github pages funcione:

1. Una vez tengamos clonado el repositorio con los archivos necesarios, dentro del repositorio creamos un directorio llamado **\_layouts**
2. Movemos el fichero **index.html** dentro de dicho directorio:

	mv index.html _layouts/

3. Creamos una réplica de dicho fichero dentro del directorio:

	mv index.html old.index.html

4. Editamos el fichero **index.html** añadiendo las variables y eliminando el texto plano de tal forma que quede así:

    	<!DOCTYPE html>
    	<html lang="en-us">
      	<head>
    	<meta charset="UTF-8">
    	<title>{{page.tittle}}</title>
    	<link rel="stylesheet" href="stylesheets/styles.css">
    	<link rel="stylesheet" href="stylesheets/github-light.css">
    	<meta name="viewport" content="width=device-width">
    	<!--[if lt IE 9]>
    	<script src="//html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    	<![endif]-->
      	</head>
      	<body>
    	<div class="wrapper">
    	  <header>
    	<h1>{{page.title}}</h1>
    	<p>Creada Github pages por aitor28ld</p>
    	  </header>
    	  <section>
    	<h3>
    		{{content}}
    		</h3>
    	  </section>
    	<script src="javascripts/scale.fix.js"></script>
      	</body>
    	</html>

5. Guardamos y procedemos a crear en el directorio principal del repositorio los ficheros **index.md** y **about.md**

6. Creamos los ficheros anteriormente citados:

	touch index.md about.md

7. Editamos el fichero **index.md** y **about.md** para que, cómo mínimo, contenga lo siguiente:

	<pre>
	---
	layout: index
	title: Aitor León
	tagline: aitor28ld.github.io
	---
	</pre>

8. Ahora sólo nos quedaría introducir el contenido de Github pages dentro de los ficheros.
9. Así quedarían los míos. Resultado de **Index.md**

	    ---
	   	layout: index
    
    	title: Aitor León 
    	tagline: aitor28ld.github.io
    	---
    
    	Página de Inicio
    	----------------
    
    	> Esta es la página de inicio. Si quieres contactar conmigo envia un correo electrónico a aitor28ld@gmail.com
    
    
    	Si quieres saber más de mí, consulta este enlace [Curriculum](about)
    	![Imagen descriptiva](images/anonimo.jpg)

10. Podemos ver el resultado en [la web](https://aitor28ld.github.io)

# Modificando el código HTML de nuestra Github pages

Si queremos modificar los datos de la página principal, clonamos el repositorio en nuestra máquina local

	git clone git@github.com:<usuario\>/<usuario\>.github.io.git

En el directorio raiz del repositorio, creamos un directorio llamado *\_layouts* y dentro de dicho directorio, un fichero llamado *default.html*.

Nos vamos a la siguiente URL, cambiando *THEME\_NAME* por el nombre de nuestro tema.

	https://github.com/pages-themes/<THEME_NAME\>/blob/master/_layouts/default.html

Vemos el fichero en crudo pulsando sobre el botón *raw* y copiamos todo el contenido al fichero que creamos.

Ahora podemos editar todo su contenido y dejarlo a nuestro gusto.

Una vez hayamos modificado todo lo que quisimos, añadimos los ficheros con:

	git add .

Realizamos un comentario diciendo qué hemos añadido/modificado

	git commit -am "<Lo que queramos comentar\>"

Y subimos los cambios realizados a nuestro repositorio en Github

	git push
