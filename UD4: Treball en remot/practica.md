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

#### Ahora obtenemos nuestra dirección IP para permitir al otro ordenador conectarse a nosotros.
~~~
ifconfig
~~~
