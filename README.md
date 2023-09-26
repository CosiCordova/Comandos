# Comandos


    1. Descarga la imagen 'httpd' y comprueba que está en tu equipo.

    La imagen se descarga con el siguiente comando: "docker pull httpd" y se puede comprobar en el apartado de docker  del Visual Studio Code donde se encuentra la carpeta de images la cual al abrir lleva los nombres de todas las imagenes descargadas.

    2. Crea un contenedor con el nombre 'asir_httpd'.
    3. Mapea el puerto 80 del contenedor con el puerto 8000 de tu máquina.
        
     Para crear un contenedor (asir_httpd) y mapear el puerto 80 con el puerto 800 de tu maquina aplicamos el siguinete comando: docker run -dit --name asir_httpd -p 800:80 httpd:2.4

     Para confirmar que funciona correctamente es necesario ingresar en el busacador de preferencia y colocar "localhost:800" si el procedimientop fue el adecuado dara como resultado el texto "It works!"

    4. Utiliza bind mount para que el directorio del apache2 'htdocs' este montado un directorio que tu elijas.
    5. Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
    6. Crea un contenedor 'asir_web1' que use este volumen para el 'htdocs'
    7. Utiliza Code para hacer un hola mundo en html

     Para que el el directorio que monte sea elegido  por mi se cambia el comando anterior de la siguiente forma: docker run -dit --name asir_web1 -p 8000:80 -v /home/asir2/Desktop/Apache/Paginas:/usr/local/apache2/htdocs httpd:2.4

     Para comprobar que el comando funciona primero deberia aparecer el nuevo contenedor activo, luego al ingresar en el buscador y poner localhost:8000/(nombre asignado al html escogido) y posteriormente deberia leerse lo escrito en el html (En nuestro caso "hola mundo").

    Todos los pasos anteriores los he realizado en el code al ofrecer la terminal, la edicion de html y el docker todo en el mismo espacio.
   
    8. Crea otro contenedor 'asir_web2' con el mismo volumen y a otro puerto, por ejemplo 9080.

    Para esto solo hace falta cambiearle al comando anterior el nombre del contenedor y del puerto de la siguinete forma: docker run -dit --name asir_web2 -p 9080:80 -v /home/asir2/Desktop/Apache/Paginas:/usr/local/apache2/htdocs httpd:2.4

    9. Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
    10. Tienen que salir la misma página web
        http://localhost:9080 
        http://localhost:8000

    Al consultar en el navegador me aparecen perfectamente la misma pagina desde cualquiera de los dos puertos. 
    
