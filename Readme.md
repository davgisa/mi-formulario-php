# Funcionamiento de la práctica con formularios e include en PHP
### Víctor Santos Sánchez-2ºAsir

Este proyecto combina el uso de archivos reutilizables con el procesamiento de formularios web utilizando PHP dentro de un entorno con Docker. El objetivo es mostrar cómo un usuario puede introducir información en una página y cómo el servidor recoge y muestra esos datos en una pantalla diferente.

## Estructura de la página principal y los includes

Cuando entramos a la dirección local en el navegador, el servidor carga el archivo index.php como página de inicio. Este archivo utiliza la instrucción include al principio y al final del cuerpo del documento para insertar el contenido de encabezado.html y pie.html respectivamente. De esta forma, se mantiene el diseño visual organizado en bloques independientes mientras que en el centro se presenta un formulario HTML completo.

## El envío de datos desde el formulario

El formulario contiene distintos tipos de campos para recoger datos como el nombre, la contraseña, el nivel educativo, la nacionalidad, los idiomas, el correo electrónico y el sitio web. Al pulsar el botón de enviar, el navegador empaqueta toda esa información y la manda de forma oculta utilizando el método POST hacia el archivo crear.php, tal como se indica en el atributo action del formulario.

## Recepción y lectura de la información en el servidor

Una vez que el archivo crear.php recibe la petición, utiliza la variable especial POST de PHP para capturar cada uno de los valores escritos por el usuario y guardarlos en variables locales. Finalmente, el código imprime una frase confirmando los datos recibidos y recorre la lista de idiomas seleccionados mediante un bucle para mostrarlos uno por uno en pantalla.