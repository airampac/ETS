# Trabajo avanzado en Git

Para completar los ejercicios debemos clonar el repositorio sobre el que vamos a realizar los cambios, para ello utilizamos en el terminal la siguiente orden.

```
git clone https://github.com/jpexposito/libro.git
cd libro
```
![1](https://user-images.githubusercontent.com/61906112/140651493-df2c27ec-9239-414b-a3a9-d20d3ca6e85b.PNG)



# Ejercicio 1

• Mostrar el historial de cambios del repositorio
• Crear la carpeta capitulos y crear dentro de ella el fichero capito1.txt con el siguiente texto.
```  
Git es un sistema de control de versiones ideado por linus torvalds
```
• Añadir los cambios a la zona de intercambio temporal.
• Hacer un commit de los cambios con el mensaje Añadido capitulo 1.
• Volver a mostrar el historial de cambios del repositorio.

```
       git log
       mkdir capitulos
       cat > capitulos/capitulo1.txt
      Git es un sistema de control de versiones ideado por Linus Torvalds.
      Ctrl+D
       git add .
       git commit -m "Añadido capítulo 1."
       git log
```

![´2](https://user-images.githubusercontent.com/61906112/140651495-b631b8aa-8c27-4766-9dc9-d5fd979d3d53.PNG)



# Ejercicio 2
• Crear el fichero capitulo2.txt en la carpeta capítulos con el siguiente texto
```El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.
```
• Hacer un commit de los cambios con el mensaje “Añadido capítuto 2.”
• Mostrar las diferencias entre la última versión y dos versiones anteriores.
    
```
     cat > capitulos/capitulo2.txt
      El flujo de trabajo básico con Git consiste en:
       1- Hacer cambios en el repositorio.
       2- Añadir los cambios a la zona de intercambio temporal.
       3- Hacer un commit de los cambios.
       Ctrl+D (para guarda y salir)
       git add .
       git commit -m "Añadido capítulo 2."
       git diff HEAD~2..HEAD
```

![3](https://user-images.githubusercontent.com/61906112/140651498-04adf8a3-06a3-4a70-b7f2-681dd445ab9d.PNG)


# Ejercicio 3
• Crear el fichero capitulo3.txt en la carpeta capítulos con el siguiente texto.
```
      Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
```
• Añadir los cambios a la zona de intercambio temporal.
• Hacer un commit de los cambios con el mensaje Añadido capitulo 3.
• Mostrar las diferencias entre la primera y la ultima versión del repositorio.
      
      
```
       cat > capitulos/capitulo3.txt
       Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
       Ctrl+D
       git add .
       git commit -m "Añadido capítulo 3."
       git log
       git diff <codigo hash de la primera version>..HEAD
```    

![4](https://user-images.githubusercontent.com/61906112/140651507-4c709e78-8daa-42c9-99c0-878be8a07912.PNG)


![5](https://user-images.githubusercontent.com/61906112/140651525-8e7c0886-18a6-45f8-b19e-a95bd7bca707.PNG)


# Ejercicio 4
•  Crea el fichero índice.txt la siguiente línea: 
```
      Indice de los capítulos, con conceptos avanzados de git
```
• Añadir los cambios a la zona de intercambio temporal.
• Hacer un commit de los cambios con el mensaje "Indice de los capítulos, con conceptos avanzados de git.
• Mostrar quién ha hecho cambios sobre el fichero indice.txt.
```
      cat > indice.txt
       git add .
      git commit -m "Se crea el indice."
      echo "Indice de los cápitulos, con conceptos avanzados de git" >> indice.txt
      git add .
      git commit -m "Añadido el índice ."
      git annotate indice.txt
```

![6](https://user-images.githubusercontent.com/61906112/140651532-1e88031c-01fc-4d2b-b118-4c7c2e07979f.PNG)


# Ejercicio 5

Crear una nueva rama bibliográfica y mostrar las ramas del repositorio.
```
  git branch bibliografia
  git branch -av
```



![7](https://user-images.githubusercontent.com/61906112/140651543-bd75eb6c-8ce7-4a40-97e2-c03a4c5c0a59.PNG)




# Ejercicio 6

• Crear el fichero capitulos/capitulo4.txt y añadir el texto siguiente:
```
      En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
```
• Añadir los cambios a la zona de intercambio temporal.
• Hacer un commit con el mensaje “Añadido capítulo 4.”
• Mostrar la historia del repositorio incluyendo todas las ramas.
```
cat > capitulos/capitulo4.txt
En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
Ctrl+D
git add .
git commit -m "Añadido capítulo 4."
git log --graph --all –oneline
```
![8](https://user-images.githubusercontent.com/61906112/140651547-a3d4a5bd-ff55-4e09-afba-74d521386a89.PNG)



# Ejercicio 7
• Cambiar a la rama bibliografía
• Crear el fichero bibliografia.txt y añadir la siguiente referencia:
```
      Chacon, S. and Straub, B. Pro Git. Apress.
```
• Añadir los cambios a la zona de intercambio temporal.
• Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”
• Mostrar la historia del repositorio incluyendo todas las ramas.

```    
  git checkout bibliografia
  cat > bibliografia.txt
  Chacon, S. and Straub, B. Pro Git. Apress.
 Ctrl+D
  git add .
  git commit -m "Añadida primera referencia bibliográfia."
  git log --graph --all --oneline
```
![9](https://user-images.githubusercontent.com/61906112/140651568-189ba622-f7cd-4e7d-b9a0-0061e33fa5f8.PNG)



# Ejercicio 8

• Fusionar la rama bibliografía con la rama main.
• Mostrar la historia del repositorio incluyendo todas las ramas
• Eliminar la rama bibliografía.
• Mostrar de nuevo la historia del repositorio incluyendo todas las ramas.
```
      git checkout main
      git merge bibliografia
      git log --graph --all --oneline
      git branch -d bibliografia
      git log --graph --all --oneline
```

![10](https://user-images.githubusercontent.com/61906112/140651593-1f26f7fd-57f0-45d0-877b-6f6b8b4e6c39.PNG)


# Ejercicio 9

• Crear la rama bibliografia
• Cambiar a la rama bibliografia
• Cambiar el fichero bibliograia.txt para que contenga las siguientes referencias:
```
      Scott Chacon and Ben Straub. Pro Git. Apress.
      Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)
```
• Cambiar a la rama main.
• Cambiar el fichero bibliografia.txt para que contengo las siguientes referencias:
```
      Chacon, S. and Straub, B. Pro Git. Apress.
      Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
```
• Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Añadida nueva referencia bibliografia”
• Fusionar la rama bibliografia con la rama main
• Resolver el conflicto dejando el fichero bibliografia.txt con las referencias:
```
      Chacon, S. and Straub, B. Pro Git. Apress.
      Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
```
• Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Resulto conflicto de bibliograia.”
• Mostrar la historia del repositorio incluyendo todas las ramas.

```
      git branch bibliografia
      git checkout bibliografia
      cat > bibliografia.txt
      Scott Chacon and Ben Straub. Pro Git. Apress.
      Ryan Hodson. Ry's Git Tutorial. Smashwords (2014)
      Ctrl+D
      git commit -a -m "Añadida nueva referencia bibliográfica."
      git checkout main
      cat > bibliografia.txt
      Chacon, S. and Straub, B. Pro Git. Apress.
      Loeliger, J. and McCullough, M. Version control with Git. O'Reilly.
      Ctrl+D
      git commit -a -m "Añadida nueva referencia bibliográfica."
      git merge bibliografia
      git nano bibliografia
      git commit -a -m "Solucionado conflicto bibliografía."
      git log --graph --all --oneline
```

![11](https://user-images.githubusercontent.com/61906112/140651623-90062a80-9598-4890-a707-4912767320a9.PNG)

![12](https://user-images.githubusercontent.com/61906112/140651631-4ed1a4c9-83fa-4f07-9f3f-8536bd0d2a4e.PNG)

![13](https://user-images.githubusercontent.com/61906112/140651634-c6330850-beb7-472b-b98f-64b20443a57d.PNG)

![14](https://user-images.githubusercontent.com/61906112/140651637-9d6dd4f9-b919-4d99-bf7b-b547adeed144.PNG)

