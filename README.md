Clonar repositorio

Para clonar el repositorio, una vez creado, he usado en la consola de Windows el comando "git clone https://github.com/JavierGarciaRuiz/masteruah/".

### Commit inicial

Usamos el comando "git add README.md" para prepararlo para realizar el commit y tras esto usaremos el comando "git commit -m "commit inicial"".

Una vez hemos realizado el commit subiremos el archivo README.md modificado al repositorio de GitHub mediante el comando "git push https://github.com/JavierGarciaRuiz/masteruah".

### Creación archivo .txt

En el siguiente apartado crearemos un archivo con formato .txt desde la consola, para ello ejecutaremos "type nul > 1.txt" y después lo añadiremos al repositorio local con el comando "git add 1.txt". Podemos comprobar que efectivamente se ha subido al repositorio local usando "git status". ![image-20220316112701996](C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316112701996.png)

### Creación de una etiqueta

Para crear un tag escribiremos "git tag v0.1 -m "Esta es la version inicial" y tras esto podremos mostrarlo usando "git show v0.1"

Para subirlo necesitamos el comando "git push origin v0.1"

![image-20220316113547436](C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316113547436.png)

### Crear una nueva rama y archivo .txt en ella

Si queremos crear una rama nueva introduciremos el código "git branch v0.2" y para posicionarnos en ella haremos uso de "git checkout v0.2". Podemos comprobar que nos encontramos en dicha rama con "git branch". Utilizaremos el mismo comando para crear el archivo2.txt (type nul > 2.txt)

### Merge directo

Nos posicionamos en la rama main con "git checkout main" y después usamos "git merge v0.2" para hacer merge directo.

### Merge con conflicto

Abrimos el archivo 1.txt mediante el comando "start 1.txt", lo modificamos, lo guardamos y hacemos commit y realizamos el mismo proyecto en la rama v0.2, para posicionarnos sobre ella recuerdo que debemos usar el comando "git checkout v0.2". Una vez que hayamos hecho "git push https://github.com/JavierGarciaRuiz/masteruah" y hayamos subido los archivos modificados en ambas ramas nos volvemos a posicionar en la rama main.

Para comprobar que efectivamente hay diferencias entre las ramas introducimos en la consola "git diff main v0.2" y se nos mostrarán todas las diferencias que existen en todos los archivos de cada rama.

Esto nos servirá para saber qué cambios tenemos que hacer y en qué rama para conservar la versión deseada. Una vez hayamos entrado en los archivos necesarios para modificarlos finalmente podremos hacer el merge que nos piden mediante el código ya visto estando antes posicionados en la rama main: "git merge v0.2" 

Para mostrar una lista de las ramas que hemos creado basta con introducir el siguiente comando:

### Eliminar rama y crear etiqueta

Para eliminar la rama v0.2 solamente tendremos que usar "git branch -d v0.2" o, como ha sido mi caso al no estar completamente sincronizada con la rama remota, "git branch -D v0.2". Una vez la hemos borrado a nivel local, para hacerlo a nivel remoto utilizaremos "git push origin --delete v0.2".

Para crear la etiqueta con el mismo nombre de la rama seguiremos el mismo proceso que con la etiqueta v0.1.

### Perfil de GitHub

Esta captura pertenece a mi perfil de github: <img src="C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316150539813.png" alt="image-20220316150539813" style="zoom:25%;" />

### Autenticación en dos factores

Para realizar la autenficacion en dos factores tenemos que acceder a ajustes>autenticacion en dos factores y seguir los pasos que nos indican. Al final nos aparecerá esta pantalla ![image-20220316150417157](C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316150417157.png)

### Perfil GitHub de mis compañeros

Compañeros elegidos: 

<img src="C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316154208894.png" alt="image-20220316154208894" style="zoom:33%;" /><img src="C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316154320574.png" alt="image-20220316154320574" style="zoom:33%;" /><img src="C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316154352218.png" alt="image-20220316154352218" style="zoom:33%;" />

Para añadir una estrella a sus repositorios hay que pulsar sobre ella cuando estemos en su perfil.

### Tabla con información de compañeros de clase

| NOMBRE                        | GITHUB                                                     |
| ----------------------------- | ---------------------------------------------------------- |
| Víctor Aljama Iglesias        | [GitHub Víctor Aljama](https://github.com/victor-aljama)   |
| Javier Escribano Claudel      | [GitHub Javier Escribano](https://github.com/javieresccla) |
| Rafael Damián Cristea Cristea | [GitHub Damián Cristea](https://github.com/MrDamian1723)   |

### Colaboradores

Si queremos añadir colaboradores al repositorio para que lo puedan modificar sin necesidad de realizar pull requests accederemos al repositorio deseado>ajustes>colaboradores>añadir. Una vez aquí necesitamos su email o nombre de usuario para enviar una invitación.

### Organizaciones

Crearemos una nueva organización pulsando en el símbolo + en la parte superior y posteriormente en nueva organización, desde aquí no tenemos más que seguir las instrucciones que nos dan y cumplir el requisito que nos piden del nombre, en mi caso "masteruah-JavierGarciaRuiz".

![image-20220316155432779](C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316155432779.png)

### Equipos

Para crear los equipos accederemos a la organización>equipos>nuevo. En este apartado crearemos ambos apartados y añadiremos a las personas deseadas. Tras esto pulsaremos sobre "ajustes" de la organización y configuraremos a nuestro gusto los permisos para miembros y administradores.

### Fork y pull request

Para hacer forks tendremos que buscar y acceder al repositorio de dos compañeros, después, en la esquina superior derecha pulsaremos sobre "fork", lo que hara que se descargue una copia del archivo en nuestro perfil. En este punto tendríamos que usar en la consola el comando "git clone https://github.com/masteruah-JavierGarciaRuiz/prueba1" para guardar una copia en nuestro repositorio local. Tras esto tenemos que guardar los cambios y enviar el html editado de vuelta al repositorio remoto y solicitar el pull request al autor para que añada al código los cambios que nosotros hemos realizado. Esto lo haremos pulsando sobre "pull request" en su repositorio donde tiene el código de la página web y elegir las ramas que queremos comparar, que en este caso serían su rama donde tiene almacenado el documento original y nuestra rama con el archivo modificado.

Una vez la otra persona nos envíe su pull request tendremos que acceder a nuestro repositorio y pulsar en el apartado de pull request, aquí nos aparecerán las solicitudes y tendremos que decidir su hacemos merge o no con la versión que hemos creado y la versión modificada por la otra persona. Llegados a este punto y después de aceptar la solicitud, nuestro archivo .html quedaría modificado.

![image-20220316162805065](C:\Users\Javi\AppData\Roaming\Typora\typora-user-images\image-20220316162805065.png)

