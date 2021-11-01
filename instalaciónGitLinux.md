# Instalacion de Git en Linux


## indice
[Instalacion de Git basica](#id1) 

[Instalacion de Git desde la fuente](#id2)

[Configuracion de Git](#id3)



# Instalación de Git basica.<a name="id1"></a>

Si tenemos una versión de Linux reciente o actualizada es probable que ya dispongamos de una versión de git instalada, podemos comprobarlo con el comando:
git –version

![1-1](https://user-images.githubusercontent.com/61906112/139680307-70e67828-7382-40d4-a1ab-3adc6ccfb2b7.PNG)


En mi caso como podemos apreciar en la imagen no dispongo de una versión de git instalada, en caso de disponer ya del git en nuestro sistema nos mostrara la versión especifica.
El terminal nos muestra que se puede instalar con un simple comando, como siempre es recomendable actualizar el repositorio de Linux antes de realizar la instalación de git con:

```sudo apt update```

Ahora introducimos el comando recomendado por el terminal anteriormente.

```Sudo apt install git```




![1-2](https://user-images.githubusercontent.com/61906112/139680430-e17999e9-ab27-44b7-9026-c22ec4ad76fb.PNG)






Realizamos de nuevo la comprobación de que tenemos instalado git y en que versión concretamente.

![1-3](https://user-images.githubusercontent.com/61906112/139680477-1215a64c-29a3-4073-a443-2c368b76f3f4.PNG)


# Instalación de Git desde la fuente <a name="id2"></a>


Este proceso de instalación se realiza cuando queremos utilizar la versión mas reciente de Git o si necesitamos instalar una versión concreta.
Para ello debemos instalar software necesario para el correcto funcionamiento de Git, tras actualizar el repositorio con “sudo apt update” como hemos mostrado en pasos anteriores, procedemos a la instalación de los paquetes mencionados.

```sudo apt update```

```sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc```

![3](https://user-images.githubusercontent.com/61906112/139681276-e81c11f4-797b-4eb9-a265-467db48f0f59.PNG)


Ahora crearemos un directorio temporal y nos movemos a el para realizar la descarga de la versión de git a instalar.

```mkdir  tmp```

```cd /tmp```

![4](https://user-images.githubusercontent.com/61906112/139681336-98c26f6c-bc93-46b3-b1ed-0c58488a2c14.PNG)


Desde el siguiente enlace Versión Git podemos descargar la versión  que queremos instalar o visualizar las diferentes opciones. Nosotros vamos a instalar la ultima versión disponible en el momento de redactar la documentación, Git  2.29.3.


```curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz```


![5](https://user-images.githubusercontent.com/61906112/139681365-ae09fdd5-ce3b-4f68-9353-180604c9ea85.PNG)


Podemos no tener instalado “curl” en nuestro equipo y este no realizara la descarga del fichero, en ese caso instalaremos con el siguiente comando y una vez termine, volvemos al paso anterior para descargar el Git.

```Sudo apt install curl```

![5-1](https://user-images.githubusercontent.com/61906112/139681414-045fa38d-496e-4ccc-9e65-aa93fab8c2c3.PNG)


Descomprimimos el fichero con el siguiente comando:

```tar -zxf git.tar.gz```

![6](https://user-images.githubusercontent.com/61906112/139681620-ea71f381-ead8-4324-9f73-f92bf3fd60ee.PNG)


Nos movemos al directo de Git:

```cd git-*```

![7](https://user-images.githubusercontent.com/61906112/139681649-0109170b-d8df-446a-9284-a3fcfbbe63d3.PNG)


Debemos crear el paquete de instalar y ejecutarlo con estos dos comandos:

```make prefix=/usr/local all```

![8](https://user-images.githubusercontent.com/61906112/139681680-ece8084f-955f-4d6b-9137-48b3f229647b.PNG)

```sudo make prefix=/usr/local install```

![9](https://user-images.githubusercontent.com/61906112/139681808-13f0ed89-18c8-4b52-ae00-a12d4c6cf390.PNG)


Sustituimos el proceso de shell para que utilice la versión de Git que instalamos en los pasos anteriores.

```exec bash```
 
 y comprobamos la versión que tenemos funcionando en nuestro git.

```git –version```

![9-1](https://user-images.githubusercontent.com/61906112/139681837-4dfe208d-4c8e-486f-ab72-d97ea2c51b97.PNG)


## Configuración de Git <a name="id3"></a>

Procedemos ahora a configurar nuestro Git con los datos necesarios para poder enviar y recibir nuestros repositorios, eso se hace con los siguientes comandos, entre las “ ” añadiremos nuestro correo y usuario de Git para poder acceder a la documentación.

```git config --global user.name "Your Name"```
```git config --global user.email "youremail@domain.com"```

![10](https://user-images.githubusercontent.com/61906112/139681869-deb4e3a0-632f-459d-86f8-d1e6ec0c4912.PNG)


Podemos verificar que los elementos de configuración han sido creados adecuadamente con este comando.

```git config –list```


En caso de ser necesario modificar los datos introducidos, podemos modificar el fichero que almacena la informacion, por ejemplo usando un editor de texto como nano, adjunto captura del proceso.

```nano ~/.gitconfig```

![11](https://user-images.githubusercontent.com/61906112/139681888-66f121c7-2b06-4b67-a728-240a993b3643.PNG)


Dentro del documento encontraremos la siguiente información:

```
[user]
  name = (El nombre de usuario que indicaron en los pasos anteriores)
  email =  (El correo personal que indicaron paso anterior)
```

![12](https://user-images.githubusercontent.com/61906112/139681907-2ab57728-0a9b-44a1-ae5d-42c4ed7e652a.PNG)


Para guarda y salir del edito utilizaremos la tecla CTRL+X y pulsamos Y + ENTER para confirmar que queremos salir.
Con esto nuestro Git tiene la configuración básica para su uso, hay mas configuración y opciones a configurar en funcionan de nuestras necesidades, pero si no cumplimos estos mínimos, es bastante probable tener errores continuamente.
