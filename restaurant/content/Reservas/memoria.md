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
    
		**sudo chgrp eljust /var//www/html** 

    - Despues añadimos al usuario en nuestro grupo con:

     **sudo usermod -a -G eljust eljust**

    - Le damos los permisos de forma recursiva con: 

      **sudo chmod -R 775 /var/www/html** 

y **sudo chmod -R g+s /var/www/html** 

Nos añadiremos como dueños del directorio con:

  **sudo chown -R eljust s/var/www/html **
