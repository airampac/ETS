# Análisis  de aplicación

Para realizar esta aplicación, necesitamos que el programa en primera instancia nos solicite que operación queremos ejecutar dentro de las ocho posibles, una vez realizada la operación nuestra aplicación consultara al usuario si requiere alguna otra operación o si terminamos de usar la aplicación.
 

![diagrama analisis areas](https://user-images.githubusercontent.com/61906112/138600645-6ddc6c20-ab50-4e98-b7a6-251edcba8415.PNG)         
       
        
## Clases

Definimos las clases, una por cada operación que tendremos que solicitar mas adelante, en este caso son:
    • Triangulo
    • Cuadrado
    • Rectángulo
    • Rombo
    • Romboide
    • Trapecio
    • Pentágono
    • Circulo

Dentro de la clase realizaremos los métodos para resolver el problema y devolver el resultado solicitado al usuario.

## Métodos

Realizaremos un método dentro de cada clase que realice el calculo matemático solicitado por el usuario.
Como ejemplo pondremos el Triangulo realizando la siguiente operación:
El usuario inserta los datos de b (base del triangulo) y h  (altura) multiplicamos entre si, y dividimos  el resultado por las caras del triangulo(en este caso 2), devolviendo al usuario el resultado final de la operación.
					
          
                                                   Triangulo= (b*h)/2
