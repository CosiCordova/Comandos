# Comandos


    1. Descarga la imagen 'httpd' y comprueba que está en tu equipo.
    2. Crea un contenedor con el nombre 'asir_httpd'.
        Ayuda
    3. Mapea el puerto 80 del contenedor con el puerto 8000 de tu máquina.
    4. Utiliza bind mount para que el directorio del apache2 'htdocs' este montado un directorio que tu elijas.

        Utiliza -v "$PWD"/htdocs:/usr/local/apache2/htdocs/

    5. Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
    6. Crea un volumen para este mismo fin.
    7. Crea un contenedor 'asir_web1' que use este volumen para el 'htdocs'
    8. Utiliza Code para hacer un hola mundo en html
    9. Crea otro contenedor 'asir_web2' con el mismo volumen y a otro puerto, por ejemplo 9080.
    10. Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
        http://localhost:9080 
        http://localhost:8000
    Tienen que salir la misma página web
