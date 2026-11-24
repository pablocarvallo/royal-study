# The Royal Study

Rompecabezas de ajedrez en un tablero de 3 × 3 para jugar en el iPhone, inspirado en el juego de mesa *The Royal Study* (Philos) y en su versión web [the-royal-study-chess.vercel.app](https://the-royal-study-chess.vercel.app/).

**Jugar:** https://pablocarvallo.github.io/royal-study/

## Cómo instalarlo en el iPhone

1. Abre el enlace de arriba en **Safari**.
2. Toca el botón **Compartir** y elige **Agregar a inicio**.
3. Toca **Agregar**. El juego queda con su icono y se abre a pantalla completa, sin la barra de Safari.

Después de abrirlo una vez con conexión, también se puede jugar sin internet.

El juego sigue el modo claro u oscuro del iPhone. En **Ajustes → Apariencia** puedes dejarlo fijo en **Claro** o **Nocturno**.

## Reglas

- Mueve las piezas hasta que cada una quede en la casilla que marca la **carta objetivo**.
- Las piezas se mueven como en el ajedrez, pero **no hay capturas**: solo a casillas vacías y sin pasar por encima de otra pieza, salvo el caballo.
- El **alfil** siempre está en casillas oscuras y el **caballo** nunca puede pisar el centro.
- Antes de mover fijas tu **límite de jugadas**. Si lo superas o se acaba el reloj de arena, pierdes el estudio.
- En **Maestro** puedes girar la carta y en **Gran Maestro** también reflejarla. Cada cambio cuesta 1 jugada.

### Niveles en solitario

| Nivel | Piezas | Carta |
|---|---|---|
| Aprendiz | Rey, torre y caballo | Fija |
| Maestro | Rey, dama, torre y caballo | Se puede girar |
| Gran Maestro | Las cinco | Se puede girar y reflejar |

### Puntos

| Resultado | Puntos |
|---|---|
| Tu límite era exactamente el mínimo posible | 3 |
| Tu límite era el mínimo más 1 | 2 |
| Resuelto dentro de un límite mayor, con pista o al repetir | 1 |
| Sin resolver | 0 |

### Duelo para 2

Un jugador apuesta en cuántas jugadas resuelve la carta; el otro acepta o apuesta menos. Quien tiene la apuesta más baja resuelve: si lo logra gana el punto, si no, el punto es para el rival. Las piezas quedan donde terminaron y se reparte una carta nueva. Gana quien llega primero a 6 puntos.

## Ajedrez guiado

Partida completa de ajedrez contra una máquina de nivel bajo, pensada para aprender de a poco. Se abre desde **Más juegos** en el inicio de The Royal Study, o directo en https://pablocarvallo.github.io/royal-study/ajedrez/ (también se puede agregar a inicio como app aparte).

- Después de cada jugada de la máquina, una tarjeta explica qué hizo y por qué (capturas, amenazas, jaques, clavadas, desarrollo, centro, errores).
- En tu turno aparecen hasta tres opciones sugeridas con su explicación; al tocarlas se ven en el tablero con una flecha verde.
- Si tu jugada pierde material, permite un mate o ahoga al rey rival, avisa antes de que responda la máquina. «Deshacer» funciona siempre.
- Tres niveles: **Primeros pasos**, **Aprendiz** y **Aficionado**. Se puede jugar con blancas, negras o al azar.
- La partida en curso se guarda en el iPhone y se retoma al volver a abrir.

## Archivos

- `index.html`: el juego completo (reglas, generador de estudios y cálculo del mínimo de jugadas).
- `manifest.webmanifest`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`: datos e iconos para instalarlo como app.
- `sw.js`: guarda una copia para jugar sin conexión.
- `ajedrez/`: Ajedrez guiado. `index.html` trae el motor (`/*MOTOR:START*/`), el profesor y la máquina (`/*PROFESOR:START*/`) y la interfaz; tiene su propio `sw.js`, manifiesto e iconos (rey negro sobre fondo blanco).

Proyecto personal sin afiliación con la marca *The Royal Study*.
