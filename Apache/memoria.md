---
title: "MEMORIA"
date: 2020-10-20T11:46:20+02:00
draft: true
---


#	**MEMORIA WEB APACHE -- DAVID PÉREZ**
	
	
	
	
#	**1.- Instación apache.**

     1.1Para ver si tenemos una version instalada del apache, en el caso de que ya lo tuvieramos no haria falta a hacer nada.
     
     
     **PONEMOS EL SIGUIENTE COMANDO:**
      "Pondremos apt-cache policy apache2"


     - Hacemos un **sudo apt update** y seguido de esto ponemos el siguiente comando para instalarlo:
     
      **Sudo apt install apache2.**
      
       
#    **2.- Configuracion de "/var//www/html"**


    - Despues accederemos al directorio /var/www/html y cambiaremos el grupo propietario de la carpeta con: 
    
		**sudo chgrp eljust /var/www/html** 

    - Despues añadimos al usuario en nuestro grupo con:

     **sudo usermod -a -G eljust eljust**

    - Le damos los permisos de forma recursiva con: 

      **sudo chmod -R 775 /var/www/html** 

y **sudo chmod -R g+s /var/www/html** 

Nos añadiremos como dueños del directorio con:

  **sudo chown -R eljust s/var/www/html **


  **3.- Metemos nuestro contenido de hugo en "/var/www/html"**

  Ingresamos a la carpeta donde tenemos nuestro proyecto y metemos el siguiente comando:

  - **hugo -D**


Y nos creara una carpeta llamada "public".

El contenido de esta carpeta la copiaremos en "/var/www/html" e iniciaremos el servicio de apache si no lo tenemos ya iniciado.



  **4.-Apache en un servidor**

  Si quisieramos hacer esto en un servidor, o unico que tendriamos que hacer es instalar el seguir los pasos anteriores pero en el servidor y una vez esta configurado el apache en el servidor solo hariamos un rsync de nuestra maquina al servidor:

  **rsync -avh --progress Rutadelproyecto usuario@IPservidor:/var/www/html**


  Y ya lo tendriamos.


  **4.1 Meter contenido en un host gratuito** 


  Ingresaremos en la pagina "00WebHost.com", nos crearemos una cuenta y despues elegiremos la opcion:

![Opcion](./1.png)

  **seleccionamos la opcion "other".**

  **Ahora nos dira que elijamos un nombre y una contraseña.**

  ![Opcion](./3.png)

**Y le damos click en submit.**


  ![Opcion](./4.png)

  **Y elegimos la opcion "upload a file"**


  ![Opcion](./5.png)

**se nos abrira  esta ventana y accederemos a la carpeta "public_html"**

**Dentro de esta meteremos los archivos de dentro de la carpeta public**


  ![Opcion](./6.png)

**Y le daremos a "upload"**

**Volveremos a la pagina 00WebHost.com y veremos que sale nuestra pagina activa en la izquierda"**

 ![Opcion](./7.png)


**Entramos en el link que nos indicia donde esta nuestra pagina y confirmamos que funciona**


   ![Opcion](./9.png)
   
   
   **Codigo QR**
   
    ![Opcion](./10.png)




