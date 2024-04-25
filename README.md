# INTRODUCCION

## ***Que es PHP ?***
>  PHP -> Hypertext Preprocessor - Es un lenguaje de codigo abierto especialmente adecuado para el desarrollo web y que puede ser incrustado en HTML. 

### ***Caracteristicas***
> Lo particular de PHP es que se ejecuta del lado del servidor, genereando HTML y enviandolo al cliente. El cliente recibira la ejecucion del script, aunque no sabra el codigo que lo ejecuto.
>
> Otro punto a favor, es que se puede configurar el servidor para que procese todos los ficheros HTML con PHP, asi los usuarios no pueden acceder a estosc archivos.
> Tambien PHP tiene las capacidades como creacion de imagenes, ficheros PDF e incluso peliculas FLASH entre otras cosas.
> PHP es simple, pero a suvez ofrece muchas caracteristicas avanzadas. 
>
### ***¿Que se puede hacer con PHP?***
> Que se puede desarrolla con PHP:
> * Scripts del lado del servidor.
> * Scripts desde la linea de comandos.
> * Aplicaciones de escritorio.

>[!NOTE]

## ***Configuracion de Entorno de trabajo***

> Instalacion de PHP
> Instalacion de servidor (Apache - etc)
> Instalacion de Gestor de base de datos (mySQL, PstgreSQL, etc)

## ***Primer fichero PHP***

``` html
    <html>
        <head>
            <title>Primer Documento PHP</title>
        </head>

        <body>
            <?php echo "<p>Hello Word!</p>"; ?>

        </body>
    </html>

```
### ***Accediendo a los ficheros***

> Una vez levantado nuestro servidor (XAMP, AMPS, APACHE, etc) ya podemos acceder al archivo en la ruta indicada
> http://127.0.0.1/index.php
### ***Obtener informacion del sistema desde php***
```php
    <?php phpinfo();?>
```

### ***Extra***

Veamos que tipo de navegador esta utilizando el usuario visitante. Para hacerlo,corrobaremos un dato que el anvegador encia como poarte de la peticion HTTP. Esta variable contiene el navegador que utilizo el usuario para hacer la peticion.

```php
    $_SERVER['HTTP_USER_AGENT];
```


[!NOTE]
$_SERVER es una variable especial reservada por PHP que contiene la informacion del servidor web, asi como esta hay ***muchas mas***.




### ***Variables Predefinidas o Reservadas***
Las variables superglobales, son variables predefinidas en PHP que estan disponibes en todos lso ambitos.

* $GLOBALS - Hace referneica todas las variables disponibles en el ambito global.
* $_SERVER - Informacion del entorno del servidor y de ejecucion.
* $_GET - Variable HTTP GET.
* $_POST - Variable HTTP POST.
* $_FILES  - Variables de subida de ficheros HTTP.
* $_REQUEST - Variable HTTP request.
* $_SEESION - Variabler de sesion.
* $_ENV - Variable de entorno.
* $_COOKIE - Cookies HTTP.
* $php_errormsg - El mensaje de error anterior.
* $http_response_header - Encabezados de respuesta HTTP
* $argc - El numero de argumentos pasados a un script
* $argv - Array de argumentos pasados a un script.


### ***Ejemplo #2 - Usando estructuras de control***

```php
    <?php
    if( strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE){
        echo 'Esta usando Internet Explorer.';
    }
    ?>
```

```
Output: Esta usando Internet Explorer.
```