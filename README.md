DOCUMENTACIÓN COMPLETA Y DOCUMENTO DE DISEÑO

JUEGO: ERROR 404: LOST

1. Requerimientos Funcionales del Sistema

1. Gestión de Estado e Integridad del Jugador:** El sistema debe registrar y actualizar en tiempo real el porcentaje de vida del personaje (de 100% a 0%). Cuando el nivel de integridad llega a cero debido a ataques de la entidad o a errores al ingresar contraseñas, el sistema debe interrumpir la partida y desplegar la pantalla de colapso o *Game Over*.
2. Control de Recursos de la Linterna:** El sistema debe gestionar el nivel de batería de la linterna (de 100% a 0%), reduciendo automáticamente dos unidades de carga por cada dos segundos en los que la luz permanezca encendida. Si la batería se agota por completo, el sistema debe forzar el apagado de la linterna y bloquear su encendido hasta el reinicio de la partida.
3. Movimiento y Detección de Colisiones:** El sistema debe capturar las entradas del teclado (`WASD` o flechas de dirección) para desplazar la posición del jugador en un plano bidimensional a una velocidad constante de 3 píxeles por fotograma. Adicionalmente, el motor de físicas debe evaluar colisiones por cajas alineadas (AABB) para impedir que el personaje atraviese paredes, límites del lienzo o estructuras sólidas.
4. Iluminación Dinámica y Máscara de Visibilidad:** El sistema debe mantener el escenario bajo una capa de oscuridad casi total (*Fog of War*). Al activar la linterna con la tecla `F`, el motor debe renderizar una máscara de luz circular con un radio de 80 píxeles centrada en el jugador para hacer visibles los elementos del mapa comprendidos dentro de ese radio.
5. Mecánica de Interacción con el Entorno:** El sistema debe medir la distancia entre el jugador y los objetos interactivos (terminales, notas, puertas o entidades). Si el jugador se encuentra a menos de 40 píxeles de distancia y presiona la tecla `E`, el sistema debe ejecutar la acción asociada, como desplegar mensajes en la consola de texto o activar paneles de entrada de datos.
6. Validación de Contraseñas y Control de Acceso:** El sistema debe proveer una interfaz de entrada de texto donde el jugador pueda ingresar cadenas alfanuméricas. Al enviar el texto, el sistema debe comparar la entrada con la clave almacenada para el nivel actual; si la clave es correcta, debe abrir la puerta correspondiente y autorizar el avance, mientras que si es incorrecta, debe denegar el acceso y aplicar una penalización de 10% de daño a la vida del jugador.
7. Progresión de Niveles y Temporizadores:** El sistema debe controlar el flujo entre las 5 salas del juego, limpiando el lienzo y cargando la configuración de mapa, obstáculos y puntos de interacción correspondientes al nivel alcanzado. Para niveles de amenaza específicos (como el Nivel 4), el sistema debe ejecutar un temporizador en cuenta regresiva que obligue al jugador a resolver el sector antes de que el contador llegue a cero, desencadenando la derrota en caso de expiración.
8. Toma de Decisiones y Múltiples Desenlaces:** En la etapa final del juego (Nivel 5), el sistema debe ofrecer opciones de elección interactiva que determinen la pantalla de cierre mostrada al usuario, diferenciando entre la destrucción del sistema (Final Bueno: Purgar) y la asimilación del jugador dentro de la red (Final Alternativo: Reboot).

2. Historia y Universo del Juego

La narrativa sitúa al jugador en el papel de un estudiante de desarrollo de software que, durante una sesión nocturna de exploración en la red, tropieza con una dirección IP no indexada. Al cargar el sitio web, la pantalla despliega únicamente la leyenda `ERROR 404`. Al intentar cerrar la pestaña o apagar el equipo, el sistema operativo colapsa por completo, atrapando la conciencia del usuario dentro de la infraestructura interna de un servidor abandonado.
A medida que el jugador recorre los sectores de memoria infectados, descubre registros antiguos que revelan la verdadera naturaleza de la red: el protocolo ERROR 404 no es una falla común del sistema, sino un entorno de contención cibernético diseñado para aprisionar procesos intrusos. Además, los sectores centrales están bajo la patrulla constante de `ERROR.EXE`, una entidad hostil formada por código corrupto que busca purgar cualquier presencia extraña en la memoria RAM.
El clímax de la historia ocurre en el núcleo del servidor (Nivel 5), donde el jugador obtiene acceso raíz (*Root*) y enfrenta la decisión final. Puede ejecutar el comando de purga total para destruir el código fuente y despertar en el mundo real, o puede reiniciar el sistema para tomar el control de la red, convirtiéndose voluntariamente en el nuevo administrador y quedando atrapado para siempre en el entorno digital.


3. Jugabilidad Detallada

El bucle central de juego combina la exploración cautelosa, la gestión rápida de recursos y la resolución de acertijos bajo presión. El jugador inicia cada nivel en un punto de entrada a oscuras. La primera acción consiste en evaluar el uso de la linterna, encendiéndola de forma intermitente para ubicar pistas sin agotar la batería de forma innecesaria.
Una vez identificado un punto de interés —representado por bloques de colores que simbolizan terminales, notas en el suelo o puertas de enlace—, el personaje se desplaza hacia él y presiona la tecla `E` para abrir el panel de inspección. La información obtenida en la consola de mensajes revela códigos parciales, combinaciones numéricas o advertencias sobre peligros cercanos.
El avance entre salas requiere ingresar la clave correcta en el panel de la puerta principal. Si el usuario escribe una contraseña errónea, la terminal emite una descarga que resta un 10% de la vida del personaje. En niveles avanzados, la jugabilidad se vuelve más intensa al sumar la presencia de la entidad corrupta, a la cual se debe esquivar físicamente en el mapa mientras se busca la clave de salida antes de que expire el temporizador del sector.


4. Plataforma, Lenguaje y Motor de Desarrollo

El videojuego está diseñado para ejecutarse de manera nativa en la **plataforma Web**, lo que permite abrirlo directamente en navegadores como Google Chrome, Microsoft Edge o Mozilla Firefox, sin necesidad de instalaciones previas ni componentes adicionales. Se puede jugar tanto de forma local desde un archivo ejecutable `.html` como alojado en servidores en la nube.
El desarrollo se realiza utilizando exclusivamente **JavaScript Vanilla (ES6+)** para la programación de la lógica, la física y el bucle de juego, acompañado de **HTML5** para la estructura de la página y **CSS3** para los efectos visuales de interfaz (*glitch*, fuentes tipográficas monospaciadas y maquetación de paneles).
Para evitar el uso de motores pesados como Unity o Godot, la producción utiliza un **Motor Web Nativo apoyado en la API Canvas 2D de HTML5**. Esta tecnología permite dibujar cuadros por segundo, procesar colisiones en tiempo real y aplicar efectos de iluminación mediante operaciones de composición gráfica directamente desde el código fuente editado en Visual Studio Code o Replit.

5. Entorno Gráfico, Escala y Especificaciones de Píxeles

El apartado visual se define bajo una estética **Top-Down Pixel Art / Retro Cyber-Horror**, inspirada en las terminales informáticas de los años 80 combinada con elementos de terror digital moderno.
El lienzo de dibujo (Canvas) opera sobre una resolución fija de **600 × 400 píxeles** con una relación de aspecto 3:2, lo que garantiza que el juego se mantenga fluido y ligero en cualquier computadora. Los elementos del mapa se construyen a partir de las siguientes dimensiones de sprites:

Jugador:** Representado por un bloque móvil de $16 \times 16$ píxeles.
  Objetos e Ítems (Notas, Terminales):** Dimensionados en $30 \times 30$ píxeles.
  Puertas de Acceso:** Estructuras rectangulares de $30 \times 60$ píxeles.
  Área de Iluminación:** Un círculo proyectado con un radio de $80$ píxeles alrededor del personaje.

La paleta de colores se limita a tonos contrastantes de alto impacto cibernético: un fondo profundo negro (`#030303`), elementos de interfaz y jugador en verde fósforo CRT (`#00ff66`), datos y terminales en cian neón (`#00ffff`), y alertas de peligro o entidades enemigas en rojo neón (`#ff0055`).
