#Taller 1 Ecosistemas de aplicación.
##Juan Esteban Pérez-Luis Ángel Vivas

###Clase Main

En esta clase sucede todo lo relacionado con la ejecución de la aplicación, los metodos que se encuentran en la logica son llamados aquí para ser ejecutados por los metodos bases como el draw y el setup.

####Variables:

* Logica: log //Esta variable global es la que utilizo para llamar los metodos que he definido con anterioridad en la logica para realizar todo el proceso de ejecucion de estos metodos.

####Metodos:

*void main(String[] // Este metodo lo utilizo para llamar el package con el que voy a trabajar e incluir el core de proccessing mi PApplet.
*void settings() // Este metodo será utilizado para dar el tamaño al lienzo de la aplicación.
*void setup() // Este motodo será utilizado para inicializar las variables globales, para luego poder utilizarlas, como en el caso de la logica, para utilizar en los metodos de abajo.
*void draw() // Este metodo será utilizado para realizar todo el trabajo de pintado que he definido en la logica.

###Clase Logica

Esta clase contiene todos los metodos para que se ejecuten en el Main y así se ejecute la aplicación de manera adecuada. Es la clase donde contiene lo logico de la aplicación.

####Variables:
*PApplet app // Esta variable la utilizo para hacer uso del PApplet y así utilizar sus metodos en la logica.
*ArrayList sockets // Esta variable la utilizo para crear un ArrayList de sockets, es decir, crear una Lista con varios objetos sockets para crear la via de comunicacion de la aplicación.
*int pantalla // Con esta variable se realizara el cambio de pantallas entre la aplicación.
*PImage escenarios // Con esta variable segun la pantalla tambien se cambia su valor para pintar un determinado escenario.
*Personaje personaje // Con esta variable se crea un personaje llamado desde la clase Personaje, el cual sera utilizado por el usuario.
*String puntaje // Con esta variable se calcula el puntaje llevado por el usuario para luego pintarlo al final el puntaje acumulado.
*Servidor servidor // Se crea una variable servidor para definir la creacion de la aplicacion de eclipse como un servidor y lograr la comunicación.
*int contador // Variable para llevar la cuenta del tiempo de juego.
*ArrayList enemigos1 // Arraylist de Enemigo1, para crear los enemigos tipo 1 que iran en el primer nivel.
*ArrayList enemigos2 // Arraylist de Enemigo2, para crear los enemigos tipo 2 que iran en el segundo nivel.
*ArrayList enemigos3 // Arraylist de Enemigo3, para crear los enemigos tipo 3 que iran en el tercer nivel.
*ArrayList monedas // Arraylist de Moneda, para crear los objetos que sumarán puntaje al usuario.
*ArrayList hilos // Arraylist de Hilo, para crear los objetos que daran poder al usuario.
*ArrayList moodles // Arraylist de Moodle, para crear los objetos que aumentaran el tiempo del usuario.
*ArrayList vidas // Arraylist de Vidas, para crear los objetos que darán vida al usuario.

####Metodos:
*Logica (PApplet) // Este metodo me servira para inicializar todas las variables y así mismo, hacer uso de ellas.
*void pintar() // En este metodo realizare todo lo referente al pintar de la aplicacion, traere los metodos de pintar de la clase Elemento para que todo se piense en el lienzo de la aplicación.

###Clase Servidor

Esta clase será la que definirá a la aplicación de eclipse como el servidor. Mandando y recibiendo flujo de datos.

####Variables:
*Serversocket server // Este metodo sirve para definir el puerto donde escuchara el servidor.
*Socket socket // direccion ip y el puerto donde se conectará el cliente.
*Boolean conectado // para validar cuando el cliente se conecte al servidor para iniciar la transferencia.
*DataInputStream entrada // para la entrada del flujo de datos.
*DataOutputStream salida // para la salida del flujo de datos.

####Metodos:
*Servidor() // Constructor de la clase
*Recibir() // para recibir el flujo de datos enviado por el cliente.
*Enviar(String:string) // para enviar flujo de datos transformado en un string.
*Run() // para crear e inicializar el hilo para el funcionamiento de la clase. 

###Clase Objeto
Esta clase sera abstracta ya que sera la clase padre que definirá ciertas caracteristicas iguales que tendran las hijas, esta clase me sirve para no repetir lineas de codigos que son iguales en cada clase hija.

####Variables:
*Pvector pos // Variable para definir la posicion de los objetos.
*Boolean vivo // Para definir cuando un objeto esta vivo y cuando no.
*Logica log // Para estar referenciados de la logica todo el tiempo.
*Pvector vel // Para definir la velocidad a la que se mueven los objetos.
*int contadorVida // Para definir el contador de la vida que tendran los objetos.
*int tamVida // Definir el tamaño de la vida maxima.
*boolean colision // Para validar cuando dos objetos se chocan entre si.
*String vida // Para pintar la vida del objeto.

####Metodos:
*Objeto() // Constructor de la clase
*pintar() //Encargado de pintar las objetos
*mover() // Encargado de mover los objetos
*validarChoque() // Encargado de validar las colisiones