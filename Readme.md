## Proyecto de Programación II de Ciencia de la Computación.

*Equipo*
Maday Mircia Suárez Velázquez C-211
Kevin Majim Ortega Alvarez C-212

## Dominoes 

Este Readme tiene como objetivo dar todas las instrucciones necesarias para ejecutar la aplicación y dar una configuaración válida del juego (teniendo en cuenta las restricciones que decidimos poner).

**Este proyecto solo es válido abrirlo en `Sistema Operativo Windows`, debido a que fue programado en Visual Studio y la interfaz gráfica fue diseñada en WPF (Windows Presentation Fundation).


  --En primer lugar, los aspectos que varian  en nuestro dominó son:

  **Tipo de dominó** : Aquí el usuario decide que tipo de doble quiere jugar(introduciendo un valor numérico). Ej: Si se escribe 9, se estaría refiriendo al doble 9. En caso de que el usuario, introduzca un valor con letras ej. "2fr4" el código lo interpretará como que se quiere jugar el doble 24, es decir el toma los valores númericos de lo que se introduzca. Aparecerá en la interfaz como *TYPE OF DOMINO*.

  **Estructura** : En esta opción, se puede escoger entre el tipo matricial(simulando un tablero de ajedrez)que es donde sale el historial y las fichas jugadas por los jugadores(cabe mencionar que esta matriz es de 13x13) o el tablero abstracto, que es para las fichas no representables, donde solo aparecerá el historial de jugadas. Aparecerá en la interfaz como *STRUCTURE* y se deberá marcar una sola opción de las existentes, las cuales son:
  
   `Matrix`:

   `Abstract`:

  **Tipo de ficha** : Aqui varía lo contenido dentro de la ficha, si son fichas de letras, de números etc, en dependencia de la implementación que se haya programado. Aparecerá en la interfaz como *TOKEN TYPE* y se deberá marcar una sola opción de las existentes.
  Las opciones que aparecen son :

  `Leters`: Fichas que contienen las letras del abecedario `A - Z`.

  `Numbers`: Todos los numeros en dependencia de la modalidad.

  `Lemojis`: Fichas que contienen 12 emojis ej. :) , <3 etc.

  **Estilo de juego** : En esta opción, lo que varía es el estilo del juego, ya sea el clásico o alguna de las implementaciones de este estilo. Aparecerá en la interfaz como *PLAYING STYLE* y se deberá marcar una sola opción de las existentes. Las opciones que aparecen son:

  `Classic`: Consiste en jugar una ficha por turno a cada jugador.

  `Thief`: Este es el clasico *Robadito* donde si un jugador se pasa en un turno debe robar una ficha de las que esten fuera del juego.
  
  `KeepPlaying`: Estilo de juego que se basa en que cada jugador va a jugar en un mismo turno hasta que ya no lleve.

  **Tipos de jugadores y la cantidad de cada uno** : Para escoger que tipo de jugador quiere tener en juego, se deberá escribir la cantidad que se desea de cada jugador(valor numérico), si no quiere usar un jugador, se debe poner cero. Aparecerá en la interfaz como *TYPE OF PLAYERS*. Los tipos de jugadores disponibles son:

   `LigthPlayer`: Este es el tan conocido *Botagorda* que va soltando las fichas de mayor valor.

   `BankPlayer`: Jugador que trata de nunca quedarse sin algÚn valor de cada ficha, siempre quiere tener al menos una reserva de cada una. 

   `TrollPlayer`: Jugador que se va fijando por donde se estan pasando sus adversarios, para después ponerles esa ficha para que se pasen.

   `RandomPlayer`: Jugador que juega la primera ficha que ve que encaja en la mesa.

  **Forma de repartir** : En esta opción, lo que varía es la forma en que se reparten las fichas, ya sea por dirección, por cantidad, en dependecia de los tipos de implementaciones. Aparecerá en la interfaz como *WAY TO DISTRIBUTE* y se deberá marcar una sola opción de las existentes, que son:

   `Classic`: Se reparte de la forma típica, una ficha por jugador hasta llegar a la modalidad + 1, ej. en el doble 6 se dan 7 fichas por jugador.

   `All`: Se reparte de forma random una ficha por jugador, hasta que se acaban. Eso si cada jugador tendrá al menos una ficha

  **Condición de ganada** : En esta opción, lo que varía es la forma en la que se gana el juego, ya sea que gane el que menos o más puntuación tenga, o que gane el que se quede con una ficha en específico, en dependencia de los tipos de implementaciones. Aparecerá en la interfaz como *WINNERS CONDITION* y se deberá marcar una sola opción de las existentes. Las opciones que aparecen son:
  
   `Classic`: Gana el jugador que se quede sin fichas, o cuando se tranca el juego el jugador que menor cantidad de puntos tenga.
  
   `Inverter`: Aqui gana el jugador que mayor cantidad de puntos tiene es el que gana, los que se quedan sin fichas ya pierden automáticamente
   
   `Handed`: Aqui gana el jugador que nunca se pasa, si te pasas pierdes automaticamente.

  Ya sabiendo esto, podemos proceder a explicar como ejecutar el código (ya sea que se abra desde el archivo ejecutable o simplemente corriendo el código):
     Luego de tenerlo ejecutado, saldrá una ventana, que consta de dos botones, `LEAVE` (por si quieres salir) y `START` (para comenzar a personalizar el juego).
     Cuando se toque `Start`, aparece otra ventana, en la cual puedes personalizar tu juego escogiendo entre los aspectos que varían (ya mencionados anteriormente), luego de eso ya todo esta listo para ver la partida dando nuevamente en el botón `Start`, donde automáticamente aparece el tablero(en dependencia de la estructra que se escoja). En este Tablero aparecen dos botones, por si quiere salir y abandonar el juego `Leave`; y si quiere seguir jugando debe dar en el botón `Move` para ver la siguiente jugada.


  **AVISOS** En los casos en que las opciones de personalización, ya sea que no coincidan, o estén fuera de los rangos implementados por nosotros, aparecerán avisos ej. *FORMATO INCORRECTO* para que el usuario cambie la configuración introducida.  

  En que casos aparecen estos avisos:

  1-  Tipo de dominó.
      -Cuando se introduce un valor negativo. 
      -Cuando se introduce algo que no sea número.
      -Cuando se deja en cero.

  2-  Estructura.
      -En el caso que se ponga en la estructura `Matrix` una modalidad mayor o igual a 12.
      -En el caso que se ponga en la estructura `Abstract` una modalidad mayor o igual a 70. 

  3- Fichas. 
      -Cuando se quiera jugar con el tipo de fichas `Lemojis` y se ponga una modalidad mayor a 11.
      -Cuando se quiera jugar con el tipo de fichas `Leters` y se ponga una modalidad mayor a 26.

  4- Jugadores.
      -En caso de que se dejen todos los jugadores en 0.
      -En caso de que se quiera jugar con más jugadores que la cantidad de fichas. 


      Esperamos que el juego sea de su agrado ;)
