# Manipulación de repositorios en Git

Para empezar a trabajar con Git lo primero que debemos hacer es configurar nuestras credenciales, para manipular, descargar y enviar nuestros repositorios, ademas añadimos la configuración de colores automáticos y por ultimo listaremos la información añadida para revisar que todo este correcto.

```
git config --global user.name " Tu nombre de usuario en Git "
  git config --global user.email " Tu correo "
  git config --global color.ui auto
  git config --list
```
![1](https://user-images.githubusercontent.com/61906112/140201697-87dc4807-215a-4a63-bebf-3518de06abe9.PNG)

![2](https://user-images.githubusercontent.com/61906112/140201722-407371cc-ffda-430c-840e-ee94097428e0.PNG)


Creamos una una nueva carpeta con el nombre “dpl” y mostramos el contenido para revisar que se ha instalado correctamente.

```
 mkdir dpl
 cd dpl
 git init
 ls -la
```
![3](https://user-images.githubusercontent.com/61906112/140201842-afc101a1-b17b-4d1d-a5ae-d31f17f941c9.PNG)




Ahora comprobaremos nuestro repositorio con el comando “git status”, y procedemos a crear un “indice.txt” donde añadiremos información y la guardaremos. También comprobaremos de nuevo el estado del repositorio tras la modificación realizada, y y adjuntamos el fichero a la zona de intercambio de git.

```
git status
 cat > indice.txt
 Capítulo 1: Instalación de Git por el alumno XXX
 Capítulo 2: Flujo de trabajo básico
 Ctrl+D
 git status
 git add indice.txt
 git status
```
![4](https://user-images.githubusercontent.com/61906112/140201966-31f0c161-25de-4b6d-8980-70e1378ce80a.PNG)


Lo siguiente es utilizar  el commit comentándolo con el cambio realizado, en este caso seria “añadido índice de la asignatura DPL”. Y comprobamos que todo este en orden con el “git status”.
```
git commit -m "Añadido índice de la asignatura DPL."
git status
```
![5](https://user-images.githubusercontent.com/61906112/140202035-11aa058e-38d1-4076-9449-99759dcbb723.PNG)


Modificamos el fichero indice añadiendo dos nuevos capítulos esto realizaremos con la siguiente secuencia, mostraremos los cambios con “git diff” y actualizamos nuestro repositorio.
```
cat > indice.txt
Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Gestión de ramas
Capítulo 4: Repositorios remotos
Ctrl+D
git diff
git add indice.txt
git commit -m "Añadido los capitulos 3"
```
![6](https://user-images.githubusercontent.com/61906112/140202106-0cd94cc7-a784-49bc-8cce-0512d3efe41a.PNG)


Con las siguientes ordenes vamos a visualizar los cambios de la ultima versión en el repositorio,  modificamos también el últimos comentario que mandamos con el commit y comprobamos que ha cambiado.
```
git show
git commit --amend -m "Añadido el capitulo sobre gestión de ramas al índice."
git show
```
![7](https://user-images.githubusercontent.com/61906112/140202185-f2c545ec-e7d2-4d07-b25b-07de8497266c.PNG)

![8](https://user-images.githubusercontent.com/61906112/140202236-391bcb43-483f-42ed-a1b7-e8706238946a.PNG)
![9](https://user-images.githubusercontent.com/61906112/140202316-e1d40261-9109-4e73-8747-1139a2545311.PNG)
