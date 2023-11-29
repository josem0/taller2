<!-- LOGO -->
<br />
<a name="arriba"></a>
<div align="center">
    <img src="imagenes/logo.png" alt="Logo" width="180" height="80">
 <!-- TITULO -->   
  <p align="center">
    Estructura de Datos Taller 2 - Anais Rodriguez
  </p>
</div>
<!-- INDICE -->
<details>
  <summary>Indice</summary>
  <ol>
    <li>
        <a href="#resumen-del-taller">Resumen del Taller</a>
      <ul>
          <li><a href="#consideraciones-extras">Consideraciones Extras</a></li>
      </ul>
    </li>
    <li>
        <a href="#librerías">Librerías</a>
    </li>
    <li>
        <a href="#código">Código</a>
        <ul>
          <li><a href="#main">main</a></li>
          <li><a href="#printheader">printHeader</a></li>
          <li><a href="#printbroad">printBroad</a></li>
          <li><a href="#game">game</a></li>
          <li><a href="#iscolumnfull">isColumnFull</a></li>
          <li><a href="#makemove">makeMove</a></li>
          <li><a href="#undomove">undoMove</a></li>
          <li><a href="#cpumove">cpuMove</a></li>
          <li><a href="#setlistproductiontoadd">setListProductionsToAdd</a></li>
          <li><a href="#setlistbrowsertoadd">setListBrowsersToAdd</a></li>
          <li><a href="#setlistsecuritiestoadd">setListSecuritiesToAdd</a></li>
          <li><a href="#setlistsocialstoadd">setListSocialsToAdd</a></li>
          <li><a href="#deletesoftware">deleteSoftware</a></li>
          <li><a href="#addsoftware">addSoftware</a></li>
      </ul>
    </li>
  </ol>
</details>

<!-- RESUMEN DEL TALLER -->
## Resumen del Taller
Se desarrolló el algoritmo para el juego Conecta 4 según los siguientes requerimiento:

* Se debe generar un menú para elegir la dificultad del juego (fácil, medio, difícil).
* Por consola se debe poder visualizar el estado de la partida en el momento (tablero de 6x7).
* Se debe generar un csv que guarde todas las partidas hasta el momento.
* se debe poder ver la puntuación de jugador vs máquina.
* Se debe poder guardar el estado de la partida,y después cargarlo al momento de iniciar el programa.

### Consideraciones Extras
* Se debe incluir en el algoritmo la lógica Minimax
* Se debe implementar PODA
* Se debe analizar el desempeño con y sin PODA
<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

# Librerías
Se están utilizando un total de 8 librerías, las cuales se muestran a continuación.
<div align="center">
    <img src="imagenes/Library.png" alt="Library" width="400" height="200">
    <p>main.cpp</p>
</div>

# Código
A continuación se detallan las funcionas usadas en la creación del taller.

## main
Función de tipo `int`, utilizada para mostrar el menú al usuario.
Permite seleccionar la dificultad del juego así como también regresar luego de cada partida para intentarlo nuevamente. 

<div align="center">
    <img src="imagenes/Main.png" alt="Main" width="800" height="350">
    <p>main.cpp</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## printHeader
Función de tipo `void`, utilizada para mostrar en la interfaz del tablero el nombre de las columnas.
Las columnas están nombras desde la 'A' hasta la 'G' para que haya una diferencia notoria con el resto del tablero.

<div align="center">
    <img src="imagenes/printHeader.png" alt="Broad" width="800" height="350">
    <p>board.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## printBoard

Función de tipo `int`, utilizada para mostrar en la interfaz el tablero, el cual se va actualizando con cada jugada que se realizan.
Las dimensiones del tablero pueden ser modificadas en los parámetros del algoritmo. 

<div align="center">
    <img src="imagenes/printBroad.png" alt="Broad" width="800" height="400">
    <p>board.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## game

Función de tipo `int`, donde se invoca toda la lógica del juego: 

* Movimientos
* Puntuación
* Minimax y PODA

<div align="center">
    <img src="imagenes/game.png" alt="Ofimatica" width="800" height="300">
    <p>game.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## isColumnFull

Función de tipo `int`, utilizada para evaluar si la posición ingresada por ambos jugadores pertenece a una columna que se encuentra llena. 

<div align="center">
    <img src="imagenes/isColumnFull.png" alt="Produccion" width="850" height="250">
    <p>moves.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## makeMove

Función de tipo `void`, utilizada para colocar en el tablero la ficha correspondiende a cada jugador dependiendo de la posición que ingresaron. 

<div align="center">
    <img src="imagenes/makeMove.png" alt="Navegador" width="800" height="400">
    <p>moves.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## undoMove

Función de tipo `void`, utilizada para permitirle a la CPU modificar su jugada por una más conveniente según su constante evaluación de nodos. 

<div align="center">
    <img src="imagenes/undoMove.png" alt="Seguridad" width="850" height="300">
    <p>moves.cpp</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## cpuMove

Función de tipo `int`, utilizada para evaluar la jugada de la CPU aplicando Minimax y PODA.

<div align="center">
    <img src="imagenes/setListSocials.png" alt="Social" width="800" height="300">
    <p>moves4.cpp</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## isGameOver

Función de tipo `int`, utilizada para revisar el resultado del juego por cada jugador o si fue un empate. 

* Verificación de arriba a abajo
* Verififcación en diagonales
* Juego aún en cursp
* Empate
<div align="center">
    <img src="imagenes/setListGamesToAdd.png" alt="setListGamesToAdd" width="800" height="300">
    <p>scores.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## minimax

Función de tipo `int`, utilizada por la CPU para la evaluación de nodos en función de Alpha y Beta, en base a los resultados toma el resultado que mejor le convenga.
Se incluye también la PODA para optimización análisis de nodos. 

<div align="center">
    <img src="imagenes/setListProductionsToAdd.png" alt="setListProductionsToAdd" width="800" height="200">
    <p>minimax.c</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## evaluatePosition

Función de tipo `int`, utilizada por la CPU para la evaluación del estado del tablero, haciendo uso de puntajes para determinar que jugador está más cerca de ganar. 

<div align="center">
    <img src="imagenes/setListBrowsersToAdd.png" alt="setListBrowsersToAdd" width="800" height="300">
    <p>minimax2.cpp</p>
</div>

<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

###Valores definidos

Permite la modificación sobre el tamaño del tablero.

<div align="center">
    <img src="imagenes/setListSecuritiesToAdd.png" alt="setListSecuritiesToAdd" width="800" height="300">
    <p>values.h</p>
	
</div>
<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## setListSocialsToAdd

Función de tipo `vector<Software*>`, utilizada para creación de objetos, relacionar la lista de amigos con el software y posteriormente agregar nuevos software sociales en un vector.

* social3: {nombre: "Facebook"; developer: "Meta Platforms, Inc."; clasificacionEdad: "18"; listaUsuarios: "listUsers"; precio: "0"; usuarios: "listfriends18"}.
* social4: {nombre: "Instagram"; developer: "Meta Platforms, Inc."; clasificacionEdad: "17"; listaUsuarios: "listUsers"; precio: "0"; usuarios: "listfriends"}.
<div align="center">
    <img src="imagenes/setListSocialsToAdd.png" alt="setListSocialsToAdd" width="800" height="300">
    <p>main.cpp</p>
</div>
<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## deleteSoftware

Función de tipo `vector<Software*>`, utilizada para eliminar un software de la biblioteca, con la condición de que es necesaria la aprobación de todos los usuarios. 
<div align="center">
    <img src="imagenes/deleteSoftware.png" alt="deleteSoftware" width="800" height="350">
    <p>main.cpp</p>
</div>
<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>

## addSoftware

Función de tipo `vector<Software*>`, utilizada para agregar un software de la biblioteca. 
<div align="center">
    <img src="imagenes/addSoftware.png" alt="addSoftware" width="800" height="300">
    <p>main.cpp</p>
</div>
<p align="right">(<a href="#arriba">Ir a Inicio</a>)</p>
