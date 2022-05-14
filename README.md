
<img src="https://user-images.githubusercontent.com/77643882/168439421-bcc9272e-fd9b-4fb3-bbc3-f883d037ad09.png" alt="logo" width="200" height="200"/><img src="https://user-images.githubusercontent.com/77643882/168439581-5196c03f-8fb5-47d2-966c-70213726eb4b.png" alt="doom-logo" width="400" height="200"/>


## La práctica se ha realizado en una máquina virtual Ubuntu-22.04-desktop-64.

Una ves instalado ***docker*** en nuestro sistema, ver **<a href="https://docs.docker.com/engine/install/ubuntu/" target="_blank" rel="noreferrer">Instalar docker en Ubuntu</a>** para más información.

![docker-hello-world](https://user-images.githubusercontent.com/77643882/168440191-9304f587-6e05-4a0a-8326-864c0ec060a2.png)

Levantamos el número de contedenores que queramos (teniendo en cuenta el consumo individual de cada uno y que será el número de enemigos) mediante la siguiente sentencia:

`for i in {1..2} ; do docker run -d -t ubuntu:14.04; done`

![loopCreation](https://user-images.githubusercontent.com/77643882/168440149-823b1adb-eebe-454a-aa84-3eaa9c53a50f.png)

Descargamos y descomprimimos el siguiente binario:

`gzip -d dockerdoomd.tar.gz`

![descomprimir01](https://user-images.githubusercontent.com/77643882/168440133-1d6d1637-d980-4878-b521-8a2e7514bdb2.png)

Extraemos los archivos del paquete *.tar*:

`tar -vxf dockerdoomd.tar`

![desenpaquetar](https://user-images.githubusercontent.com/77643882/168440235-6bb771a9-19bd-4a17-b821-b1946803c2fc.png)

Ejecutamos el servicio y comprobamos el puerto que se habilita:

![executeDaemon](https://user-images.githubusercontent.com/77643882/168440272-03b2594b-9da4-44d2-b1e5-4e98e227b82a.png)

Descargamos el cliente de VNC <a href="https://www.realvnc.com/en/connect/download/viewer/linux/" target="_blank" rel="noreferrer">VNC Viewer</a>

![downloadVNC](https://user-images.githubusercontent.com/77643882/168440325-b9a4eb21-f4c6-40ab-9f03-4b96109ea90a.png)

Creamos una nueva conexión e introducimos la url del server, en este ejemplo *localhost:5900* e iniciamos la conexión:

![VNC-Config](https://user-images.githubusercontent.com/77643882/168440334-306adf4d-9b7f-436e-8b55-242a701825a7.png)

La password por defecto es: **1234**

![VNC-Pass](https://user-images.githubusercontent.com/77643882/168440380-e4848f90-7d93-44d0-9a2e-22d0ef8a7bd2.png)

Una vez establecida la conexión ya se encuentra corriendo el contenedor con Doom:

![DoomGame](https://user-images.githubusercontent.com/77643882/168440415-2099d832-f58c-455f-99d6-05a214a97742.png)
