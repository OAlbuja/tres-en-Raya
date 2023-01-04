# tres-en-Raya
Integrante: Oscar Albuja

A.	Descripción del juego “Tres en Raya”.

Cómo jugar: Dibuja dos líneas horizontales y dos líneas verticales en una hoja de papel para hacer una cuadrícula de nueve espacios. Cada jugador se turna para colocar una X o una O en un intento de dibujar una línea vertical, horizontal o diagonal. 

El juego finaliza cuando se llenan todos los espacios, lo que puede resultar en un ganador o un empate, que suele ser lo más común si se conoce la mecánica del juego. 

Se implementará un programa en C++ usando minimax para simular este juego de mesa llamado tres en raya. Minimax es un algoritmo recursivo. La forma en que funciona minimax se puede resumir en elegir el mejor movimiento para ti suponiendo que el contrincante escogerá el peor para ti.

B.	Explicación de las principales rutinas
  
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

C. Tiempos de los peores casos y los mejores casos 

La inteligencia artificial está solo un nivel por encima de la programación informática básica. La gente está en un nivel superior. Los desarrollos y avances recientes en IA están más estrechamente relacionados que nunca con la inteligencia humana.
Sin embargo, las máquinas todavía están mucho más allá de las capacidades del cerebro humano. Los seres humanos se diferencian en nuestra capacidad para aplicar los conocimientos adquiridos a través de la lógica, el razonamiento, la comprensión, el aprendizaje y la experiencia.
Inteligencia artificial
Los robots no pueden procesar tanta información como los humanos. Inteligencia artificial
Los robots no pueden procesar tanta información como los humanos. Dado que la IA aún se encuentra en sus primeras etapas, el futuro dependerá de cómo los humanos controlen las aplicaciones de IA para respetar los valores humanos y las medidas de seguridad. Aunque las máquinas pueden imitar el comportamiento humano hasta cierto punto, su conocimiento puede corromperse al tomar decisiones racionales como las nuestras. Las máquinas impulsadas por IA toman decisiones basadas en eventos y su relación con ellos, pero carecen de "sentido común".

Se puede concluir que entre el humano y maquina existe una respuesta a los mejores o peores casos, la cual es abismal.
la computadora puede realizar analisis y acciones casi inmediatas tardando no mas de 1 seg segun la operacion que se le presente. en este caso del juego simulado la computadora es aun mas eficiente en sus tiempos de respuesta que el humano. El ser humano para dar un analisis concreto llega a tardar en promedio hasta 2 minutos en dar su respuesta mas larga. 

D. Estudio combinatorio del juego 


