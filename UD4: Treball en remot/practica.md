#### Creamos un usuario nuevo en el ordenador que actuará de servidor. Esto lo hacemos en caso de que el usuairo actual tenga contraseña, ya que dará problemas al hacer la conexión. Por lo tanto, introducimos el siguiente comando:
~~~
sudo useradd usuario
~~~
  
#### A continuación instalamos SSH en el servidor.
~~~
sudo apt install apache2
~~~
![Instalar apache en servidor](https://github.com/user-attachments/assets/337f1f09-c295-46ac-b2e0-1d3558edafc5)  


#### Y ahora configuramos el firewall para permitir las conexiones TCP al puerto 22, que es el que usa SSH.
~~~
sudo ufw allow 22/tcp
~~~
![Permiso ssh en firewall](https://github.com/user-attachments/assets/1a1ba770-5bee-4d39-b6d7-a7df98c20ce9)  

#### Y ahora configuramos el firewall para permitir las conexiones TCP al puerto 22, que es el que usa SSH.
~~~
sudo ufw allow 22/tcp
~~~

#### Ahora obtenemos nuestra dirección IP para permitir al otro ordenador conectarse a nosotros. La ip debería de tener el formato 192.168.x.x, siendo las "x" dos números particulares a cada dispositivo de la red.
~~~
ifconfig -a
~~~

#### Luego creamos un HTML de una web sencilla, y lo mandaremos a la dirección /var/www/html/dominio.com/nombreDeTuArchivo.html
![Pagina web servidor](https://github.com/user-attachments/assets/d0776655-622a-4570-9e95-c97da3506196)


#### Ahora crearemos el virtualhost, en la dirección /etc/apache2/sites-available. Dentro del archivo cambiaremos el "ServerName", y añadiremos servidor.dominio.com, siendo dominio.com el mismo que en el paso previo. Y más abajo cambiaremos el DocumentRoot a la dirección al archivo html, es decir, la misma dirección que en el paso anterior.
![nuevoVirtualHost](https://github.com/user-attachments/assets/f507aff8-2d08-4fb7-9e78-e1e7ce47a20c)

#### Ahora, dentro del directorio donde se encuentra el archivo .conf, haremos click derecho y daremos a "Abrir en terminal". Dentro de la terminal escribiremos los siguientes comandos:
~~~
sudo a2ensite nombreDeTuArchivo.conf
systemctl reload apache2
~~~
![a2ensite](https://github.com/user-attachments/assets/b41c0fd7-907a-4d28-87f2-a0d8e8d4386b)

#### Con esos pasos dejaremos el servidor, y comenzaremos a trabajar con el cliente. Lo primero será instalar el cliente con este comando:
~~~
sudo apt install openssh-server
~~~
![Instalar ssg](https://github.com/user-attachments/assets/e8ab702a-1ad6-4055-852e-a277e67a31ee)


#### Ahora iniciaremos SSH con esta serie de comandos:
~~~
sudo systemctl start ssh
sudo cp /etc/sshd_config{,.bak}
sudo nano /etc/ssh/sshd_config
sudo systemctl reload ssh
~~~
![Iniciar_ssh](https://github.com/user-attachments/assets/7caf3a24-b2b8-4330-ac79-9cca99bebf3e)


#### Por último, añadimos el dominio del servidor al archivo de hosts. Para hacer esto, editaremos el archivo en /etc/hosts, y añadiremos la IP del ordenador servidor, junto con el nombre del dominio que le hayamos asignado en los pasos previos. 
![hosts disponibles](https://github.com/user-attachments/assets/cb49aca0-de36-4552-a038-f7828374bc80)


#### Por último, nos conectamos desde el cliente al servidor con este comando:
~~~
ssh nombreUsuarioServidor@direccionIP
~~~
Aquí, se tendría que escoger las variables adecuadas al servidor. Como en esta foto:
![Conecxion_a_servidor_compañero](https://github.com/user-attachments/assets/0c911da4-5ce1-40a1-8ae3-7485c39814ca)
