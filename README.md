 - El componente sirve para validar una tarjeta bancaria, tenemos diferentes campos de texto, uno para introducir el 
   número de tarjeta, otros dos para el mes y año de caducidad, y uno más para el código CVC.

 - Los requisitos para tener un CVC válido son, que la cadena introducida sea numérica y tenga 3 o 4 cifras.
   Para el mes el valor debe ser en cifras, y puede introducirse o no un cero a la izquierda en los números menores a 10,
   y para el año, tiene que introducirse con cuatro cifras de la siguiente manera "2021".
   El número de tarjeta es validado mediante el objeto CreditCardValidator y el mismo hace la gestión de validamiento, 
   con lo cuál no entraremos en detalles.

 - La manera en la que sabremos si el texto introducido es un número de tarjeta/fecha/CVC válido es al perder el foco, 
   una vez perdido, el texto cambiará de color según el resultado, si es válido, el texto se pondrá verde, en su defecto 
   lo hará de rojo. 

 - El botón de reiniciar nos vaciará los campos de texto, ha sido simplemente una manera de agilizar el proceso de 
   comprobación manual a la hora de hacer pruebas de código

 - Para que el código funcione como componente, implementaremos Serializable, también haremos métodos getter and setter
   de las variables que nos sea necesario.
   En este caso el componente ha sido creado directamente sobre un JFrame dado que tiene varios componentes.

 - Por último los método que he tenido que crear son, el método reiniciar() para vacíar los campos de texto, conseguirAnhoActual(),
   que sirve para comprobaciones a la hora de valida la fecha, validarAnho() y validarMes() que nos indican si el texto puesto en sus 
   correcpondientes jTextField son aptos para la comprobación de fecha válida, validarCVC() y validarTarjeta() que nos indican si los 
   textos introducidos son válidos y por último validarFecha(), que hace las comprobaciones necesarias para saber si la fecha 
   introducida es superior a la actual, de no ser así el texo se pondrá rojo, como con los demás métodos.
   