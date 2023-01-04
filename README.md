# tres-en-Raya
Integrante: Oscar Albuja

#A.	Descripción del juego “Tres en Raya”.

Cómo jugar: Dibuja dos líneas horizontales y dos líneas verticales en una hoja de papel para hacer una cuadrícula de nueve espacios. Cada jugador se turna para colocar una X o una O en un intento de dibujar una línea vertical, horizontal o diagonal. 

El juego finaliza cuando se llenan todos los espacios, lo que puede resultar en un ganador o un empate, que suele ser lo más común si se conoce la mecánica del juego. 

Se implementará un programa en C++ usando minimax para simular este juego de mesa llamado tres en raya. Minimax es un algoritmo recursivo. La forma en que funciona minimax se puede resumir en elegir el mejor movimiento para ti suponiendo que el contrincante escogerá el peor para ti.

#B.	Explicación de las principales rutinas
  
1	int main().-	La función principal inicia el menú del juego, luego se debe elegir que jugador inicia primero, ya sea el jugador o la computadora quiere comenzar el juego.

2	void showInstructions().-	Esta función imprime las instrucciones del juego para que el usuario conozca la forma en que se eligen las diferentes casillas

3	bool gameOver(char board[][SIDE]).-	función que retorna true or false cuando se ubican en linea 3 "X" o 3 "O" en la matriz. Es decir, si existe un ganador

4	bool rowCrossed(char board[][SIDE]).-	Esta función itera a través de cada fila y evalúa si la primera, segunda y tercera celdas son iguales y no están vacías, devolviendo verdadero en ese caso y falso en caso contrario.

5	bool columnCrossed(char board[][SIDE]).-	Esta función itera a través de cada fila y evalúa si la primera, segunda y tercera celdas son iguales y no están vacías, devolviendo verdadero en ese caso y falso en caso contrario.

6	bool diagonalCrossed(char board[][SIDE]).-	Esta función evalúa si la primera, segunda y tercera celdas de la diagonal principal son iguales y no están vacías, o si la primera, segunda y tercera celdas de la diagonal menor son iguales y no están vacías. Devuelve verdadero en este caso, falso en caso contrario.

7	int bestMove(char board[][SIDE], int moveIndex).-	La función devuelve un número entero que atraviesa la matriz y busca la posición cero para ejecutar la rutina minmax. Funciona cuando la computadora toma su turno.

8	void showBoard(char board[][SIDE]).-	La función imprime el estado actual del tablero. Refrescando la tabla en cada movimiento.

9	int minimax(char board[][SIDE], int depth, bool isAI ).-	La función devuelve un número entero y es recursiva. Aquí es donde se evalúa el estado del juego y se calcula la puntuación para el jugador o la computadora en función de si el juego aún está activo.

10	void declareWinner(int whoseTurn).-	La función muestra quien es el ganador la partida y lo imprime en pantalla.

11	void playTresEnRaya(int whoseTurn).-	Esta función inicializa el juego y es responsable de cambiar entre el jugador y la computadora, así como llamar a la mayoría de las funciones. Indica las posiciones disponibles del jugador en la matriz.

#C. Tiempos de los peores casos y los mejores casos 

La inteligencia artificial está solo un nivel por encima de la programación informática básica. La gente está en un nivel superior. Los desarrollos y avances recientes en IA están más estrechamente relacionados que nunca con la inteligencia humana.
Sin embargo, las máquinas todavía están mucho más allá de las capacidades del cerebro humano. Los seres humanos se diferencian en nuestra capacidad para aplicar los conocimientos adquiridos a través de la lógica, el razonamiento, la comprensión, el aprendizaje y la experiencia.
Inteligencia artificial
Los robots no pueden procesar tanta información como los humanos. Inteligencia artificial
Los robots no pueden procesar tanta información como los humanos. Dado que la IA aún se encuentra en sus primeras etapas, el futuro dependerá de cómo los humanos controlen las aplicaciones de IA para respetar los valores humanos y las medidas de seguridad. Aunque las máquinas pueden imitar el comportamiento humano hasta cierto punto, su conocimiento puede corromperse al tomar decisiones racionales como las nuestras. Las máquinas impulsadas por IA toman decisiones basadas en eventos y su relación con ellos, pero carecen de "sentido común".

Se puede concluir que entre el humano y maquina existe una respuesta a los mejores o peores casos, la cual es abismal.
la computadora puede realizar analisis y acciones casi inmediatas tardando no mas de 1 seg segun la operacion que se le presente. en este caso del juego simulado la computadora es aun mas eficiente en sus tiempos de respuesta que el humano. El ser humano para dar un analisis concreto llega a tardar en promedio hasta 2 minutos en dar su respuesta mas larga. 

#D. Estudio combinatorio del juego 

El modelo que puede encontrar aquí muestra el algoritmo minimax aplicado a un árbol de juego aleatorio para un juego donde los nodos finales tienen valores entre 0 y 10. Además, el modelo proporciona una manera fácil de permitir que los árboles se representen en un manera equilibrada.

![image](https://user-images.githubusercontent.com/121888131/210480478-b952dee2-8ec7-4bba-bc4e-a42106b241ee.png)

Los juegos más interesantes tienen árboles de juegos que son tan grandes que no podemos extender el árbol hasta los nodos finales. Por esta razón, generalmente se usa un algoritmo con restricciones de profundidad, que abarca solo unos pocos niveles del árbol sin llegar a los nodos finales. Pero, ¿cómo se calcula la utilidad operativa en este caso?
Por lo general, para poder usar expansiones acotadas y algoritmos como Minimax, las funciones de evaluación se usan para calcular la utilidad de los estados no terminales, es decir aprecian el valor de la acción.

![image](https://user-images.githubusercontent.com/121888131/210480566-26a4bdd9-ca73-4700-9398-21e54f6f04e9.png)

Otra posible generalización es para juegos de suma distinta de cero o juegos con más de 2 jugadores. En tales casos, los nodos con valores de utilidad a menudo se tratan como tuplas, y cada jugador intenta maximizar su componente, lo que a veces conduce a estrategias de jugador.

#E. Instrucciones para ejecutar el código en Windows y en Linux

Para compilar el programa, una opción es descargar un IDE con todas las configuraciones necesarias, como Visual Studio Code, abrir la documentación a través del IDE, verificar si el complemento de idioma está configurado, en este caso C, y compilar. Ademas existen opciones en linea para la compilacion de programas realizados en C++ como son Onlinegdb o replit. 
la opcion de replit permite trabajar de manera colaborativa con otros usuario para la creacion de codigo, esta el la forma mas viable para realizar codigo en C++ de forma cooperativa y rapida. Tan solo se necesita abrir un navegador e ingresar en cualquiera de las 2 opciones que tenemos disponibles para la ejecucion del codigo.


