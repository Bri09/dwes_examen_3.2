# Sakila
Durante esta prueba se llevará a cabo el desarrollo de una aplicación para un videoclub que consiste en una página de alquiler de películas, el resultado de su ejecución se puede ver en la siguiente URL:
<br>
https://dawsonferrer.com/allabres/mvc/sakila/Controllers/filmsController.php
<br><br>
Tal y como se puede observar disponemos de una página de login, el siguiente usuario ha sido creado por defecto. email: prova, password: prova.
<br>
https://dawsonferrer.com/allabres/mvc/sakila/Controllers/loginController.php
<br><br>
Aparte de la pagina de login disponemos de una página de signup que permite crear nuevos usuarios.
<br>
https://dawsonferrer.com/allabres/mvc/sakila/Controllers/signUpController.php
<br><br>
Por último disponemos de un controlador sin vista para hacer logout:
<br>
https://dawsonferrer.com/allabres/mvc/sakila/Controllers/logoutController.php
<br><br>
La base de datos presenta la siguiente estructura:
![DB](DB.png)
*PRESTAR ESPECIAL ATENCIÓN A MAYÚSCULAS Y MINÚSCULAS
<br><br>
Tal y como se puede observar en la base de datos, la tabla más importante es la de film, donde podemos encontrar el código de cada película, su título, su descripción, su usuario (usuario que ha alquilado la película, por defecto NULL), además de otros campos que mostrará nuestra aplicación. Mientras que las otras tablas son secundarias y están relacionadas directa o indirectamente con la tabla de películas mediante claves foráneas. La tabla users es donde crearemos nuestros usuarios, disponemos ya de un usuario de prueba tal y como se ha explicado con anterioridad (usuario creado con la función crypt) y que por defecto tiene alquilada la película Apache Divine.
<br>
Prestad especial atención a las tablas auxiliares film_actor y film_category que se emplean para crear una relación n-n.
<br><br>
Para alquilar una película, basta con hacer un UPDATE en la tabla film e introducir el identificador del usuario que ha alquilado la película, mientras que para devolver una película simplemente es necesario volver a establecer este campo a NULL. <strong>¡NO ES NECESARIO MODIFICAR LA ESTRUCTURA DE LA BASE DE DATOS!</strong>
<br><br>
Para optimizar la aplicación se puede poner un limitador en la consulta SQL de tal forma que devuelva únicamente 20 películas aleatorias, un ejemplo de consulta sería:
<br>
<strong>SELECT * FROM film ORDER BY RAND(1234) LIMIT 20;</strong>
<br><br>
Una vez que se crea un usuario ya se puede iniciar sesión e ir a la página del listado de películas, donde podremos alquilar y devolver películas y deberemos desarrollar la funcionalidad de la aplicación.
<br><br>
Para llevar a cabo este examen puede utilizar los manuales oficiales de PHP y de MySQL así como hacer uso de todos los recursos disponibles en la web de W3Schools.
<br><br>
PS: Id por partes, primero importad la base de datos, después cread la estructura de clases, próximamente pasad a implementar cada página en MVC, id página a página, no hace falta hacer consultas complejas en los modelos, un mismo problema siempre puede ser desglosado en problemas más pequeños e ir resolviendo uno a uno. No abandoneis antes de tiempo, <strong style="color:darkred;">gestionad la frustración</strong> y buscad soluciones alternativas cuando algo no salga. Ánimos y mucha suerte.