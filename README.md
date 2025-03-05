# Proyecto intermodular DAW 🐱


## 4 Despliegue en internet
# Despliegue

## A - Mi dominio.  

He decidio que el dominio seria scats.es, puesto que el proyecto tiene como nombre StreetCats, es facil de recordar y escribir ademas de una extension española.

<hr>

## B - Despliegue en local



<hr>

## C - Despliegue en internet🐾

 Vamos a aprovisionar una instancia del Amazon EC2 en AWS Academy.  
 Empezamos creando la instancia y conectandola.  
 ![IMG1](./IMG/C1_IMG.png)  
 Aqui vemos la instancia conectada y las claves.  
![IMG1](./IMG/C1_IMG2.png)  

<hr>

### Vamos a asignar una IP elastica a una estancia EC2 en AWS

Vamos a navegar a el apartado **EC** a la izquierda y seguiremos las marcas purpuras.
![IMG1](./IMG/C2_IMG1.png)
![IMG2](./IMG/C2_IMG2.png)
![IMG3](./IMG/C2_IMG3.png)
![IMG4](./IMG/C2_IMG4.png)
![IMG5](./IMG/C2_IMG5.png)
![IMG6](./IMG/C2_IMG6.png)
![IMG7](./IMG/C2_IMG7.png)  
En esta ultima imagen ya podemos ver la instancia con la ip elastica, deberia tener la ip en la seccion de DNS.
![IMG8](./IMG/C2_IMG8.png)

<hr>

### Conectaremos con ssh, via terminal  

* Vamos a empezar usando ssh 🐱  
  
  Vamos a recordar que en mi caso la instancia que servira apache sera [98.85.89.85] y la maquina slave o servidor para backend sera [3.86.78.176] las dos utilizando ip elastica.   
  ![IMG1](./IMG/C3_IMG1.png)
  Ahora haremos la conexion con la primera maquina;  
  ```console
     ssh -i .\VisualKeys.pem ubuntu@ec2-98-85-89-85.compute-1.amazonaws.com
    ```
    Y para la siguiente seria lo mismo sustituyendo el dns tras la @:
    ```console
     ssh -i .\VisualKeys.pem ubuntu@ec2-3-86-78-176.compute-1.amazonaws.com
    ```
    - Para ayudarnos un poco con ese lio de ips, podemos crear un profile en windows y un .sh en linux.

<hr>

###  Ahora realizaremos un scp para copiar archivos entre anfitrion y maquina remota  

  ![IMG1](./IMG/C4_IMG1.png)

