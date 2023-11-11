# Descripción de la Aplicación "Running Car"

La aplicación "Running Car" es un juego simple en el que controlas un coche y debes esquivar obstáculos en la carretera. El coche puede cambiar de carril  para evitar colisiones.

##BOCETO
<img width="506" alt="BOCETO__" src="https://github.com/Raaul04/Trabajo_carrera/assets/144156038/2d51e55a-6705-468f-91e1-5a4d97012adc">



## Descripción detallada de la aplicación
<img width="507" alt="UML_NUEVO" src="https://github.com/Raaul04/Trabajo_carrera/assets/144156038/b27e75db-fb37-4541-91fd-b55790418635">


La aplicación "Running Car" es un juego de conducción en el que debes guiar un coche a través del tráfico, evitando colisiones con otros vehículos. Algunas características clave incluyen:

- Control del coche mediante eventos de teclado.
- Obstáculos en movimiento que representan el tráfico en la carretera.
- Cambio aleatorio de carril del coche para dificultar el adelantamiento.
- El objetivo es llegar lo más lejos posible sin colisiones.

## Componentes del Juego

La aplicación "Running Car" consta de los siguientes componentes:

- Clase `Juego`: Interfaz principal del juego.
- Clase `Coche`: Representa el vehículo del jugador.
- Clase `Moto`: Representa un tipo de vehículo que puede cambiar de carril aleatoriamente.
- Clase `Camion`: Representa un tipo de vehículo que puede cambiar de carril aleatoriamente.
- Clase `Trafico`: Gestiona la posición de obstáculos en el juego y lleva un registro de puntos.
- Clase `Ventana`: Representa la ventana principal del juego.
- Clase `Player`: Representa al jugador en el juego y gestiona su movimiento.
- Clase `Title`: Representa la pantalla de inicio del juego con un botón de inicio.
- Clase `TitleManagement`: Gestiona la pantalla de inicio y la transición al juego principal.

## Uso

Para jugar a "Running Car," sigue estos pasos:

1. Ejecuta la aplicación.
2. Utiliza las teclas de dirección para controlar el coche y evitar colisiones.
3. Disfruta del juego y trata de llegar lo más lejos posible.

## Arquitectura y tecnologías

La aplicación "Running Car" está implementada en Java y utiliza la biblioteca Swing para la interfaz gráfica.

## Ejecutar el Juego

Para ejecutar el juego, puedes utilizar la clase `Main`. Ejecuta el método `main` de la siguiente manera:

```java
package Juego;
import Title.TitleManagement;
import javax.swing.*;

public class Main {

    public static void main(String[] args) {
        SwingUtilities.invokeLater(new Runnable() {
            @Override
            public void run() {
                // Crear una instancia de TitleManagement para gestionar la transición entre la pantalla de título y el juego
                TitleManagement titleManagement = new TitleManagement();

                // Configurar y mostrar la ventana principal
                titleManagement.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
                titleManagement.setSize(400, 400);
                titleManagement.setVisible(true);
            }
        });
    }
}