J.S.S INCORPORATION — Documentación Completa
Prototipo jugable · Mundo abierto cenital · Bogotá 2077 · Sigilo/combate hardcore
---
1. Ficha técnica (resumen ejecutivo)
Campo	Valor
Título	J.S.S INCORPORATION
Género	Acción-aventura / sigilo / mundo abierto de arriba hacia abajo (top-down / cenital)
Ambientación	Cyberpunk latino · Bogotá, Colombia · año 2077
Plataforma	Navegador web (PC/desktop) — HTML5, Canvas 2D
Lenguaje	JavaScript (vanilla, sin frameworks ni dependencias)
Motor	Canvas 2D + Web Audio API (HTML5 nativo; sin motor externo)
Cámara	Vista cenital, zoom constante ×2.1, cámara sigue al jugador con suavizado
Idiomas	Español (neutral-colombiano: jerga bogotana: "sopita", "Badulaque", "pelao")
Estados	Prototipo jugable completo (historia principal jugable de punta a punta)
Guardado	Local (localStorage del navegador)
Duración estimada	20–60 min por partida completa
Frase de marca: "Todo lo privado es nuestro. Todo lo público, también."
---
2. Historia del juego
2.1 LORE
En Bogotá 2077 la mega-corporación J.S.S INCORPORATION lo privatizó todo: el agua, la luz,
el aire… hasta la lluvia. Reprimió barrios enteros, compró jueces, desplazó a la gente y convirtió
la ciudad en un territorio bajo control corporativo repartido en distritos con distinto nivel de sujeción
("control J.S.S").
2.2 Personaje
Encarnás a un "sopita" urbano (un parcero de la calle con nada que perder) que arranca la noche
con rumbo a La Candelaria para hablar con el informante conocido como "El Araña".
2.3 Trama principal (5 actos)
Fase	Nombre	Objetivo
0	El Informe	Hablar con "El Araña" en La Candelaria (marcador azul INFORME).
1	Sabotaje	Volar los 3 relés de comunicaciones de J.S.S en San Victorino. Sin señales, el control baja.
2	La Alianza	Rescatar y escoltar al Hacker "Peluquín" desde Chapinero hasta la guarida de La Candelaria.
3	El Final	Infiltrar la ZONA J.S.S y hackear la Terminal Maestra (con el hacker ya de aliado).
4	Victoria	J.S.S desmantelada. Los servicios vuelven a la gente. El juego continúa en modo "limpieza de distritos".
2.4 Tono
Combate crudo, mundo hostil, pero con humor y jerga bogotana (los diálogos usan "pelao",
"le echa vaina", "sapo", "aguapanela"). Existe la figura de la "Badulaque-Signal": entre más ruido
hagas, más te busca la corporación — como metáfora de la paranoia y la vigilancia corporativa.
---
3. Mapa, distritos y niveles
3.1 Mundo
Cuadrícula de 220 × 220 tiles, cada tile de 32 px (7.040 × 7.040 px de mundo).
Generación procedimental determinista con semilla fija (`20260904`): calles, manzanas, edificios,
parques, árboles y puertas estables entre partidas.
Red de avenidas: ejes principales (ancho 4–5 tiles) y calles (ancho 3 tiles).
4 distritos de 110×110 tiles cada uno.
3.2 Distritos
Distrito	Estilo	Color	Control J.S.S inicial	Descripción
ZONA J.S.S	Corporativo	Azul `#2b6ef0`	90%	Cuartel general; peligro máximo, sede de la Terminal Maestra.
CHAPINERO	Moderno	Cian `#59e3f0`	55%	Zona moderna, tienda, guarida y el Hacker "Peluquín".
LA CANDELARIA	Colonial	Ámbar `#ffb347`	70%	Zona histórica; aqui empieza la historia y vive "El Araña".
SAN VICTORINO	Mercado	Naranja `#ff8c3a`	45%	Sector comercial y de mercado negro; 3 relés de la trama.
> El **control (%)** por distrito regula peligro, precios y recompensas. Bajarlo es el motor de la "conquista".
3.3 Puntos de interés (interactuables)
Guaridas seguras (4): La Candelaria, San Victorino, Chapinero y Zona J.S.S. Guardan partida automáticamente al interactuar.
Vendedores (4): La Gorda del Bazar (San Victorino), Don Ramiro / Bodega (La Candelaria), La Tía Raquel (Chapinero) y El Mago de la 13 - mercado negro (Zona J.S.S).
Objetivos de trama: informante, relés, hacker, terminal maestra.
Elementos de contratos: cajas fuertes, rehenes, relés y laptops.
3.4 Niveles
No hay niveles lineales: es un mundo abierto por distritos. La progresión se mide por
avance de la historia (5 fases),
control por distrito (bajarlo con contratos),
equipo y dinero acumulado,
Badulaque-Signal (el "calor" que te sigue la corporación).
---
4. Jugabilidad detallada
4.1 Controles
Tecla	Acción
`W A S D` / flechas	Moverse
`Shift`	Correr (gasta aguante)
`LMB`	Disparar
`RMB`	Golpe cuerpo a cuerpo
`E`	Interactuar (hablar, guaridas, tiendas, objetivos)
`Space`	Activar/desactivar cobertura (−60% daño)
`C`	Agacharse / sigilo (te ven mucho menos)
`R`	Recargar
`1–4`	Seleccionar arma
`Q`	Usar botiquín / aguapanela (o cura menor sin items)
`TAB`	Mapa completo de la ciudad
`ESC`	Menú de pausa
4.2 Recursos del jugador (HUD)
Salud (HP): 100 máx. Borde rojo palpitante al estar al límite.
Aguante: correr lo consume; se regenera solo.
Badulaque-Signal (%): nivel de alerta corporativa. A 45%+ llegan refuerzos cada ~11 s; a 50%+ aparecen drones; a 100% te buscan la "pesada".
Temperatura / humedad: la lluvia moja y el frío produce hipotermia (pierde vida y aguante). Soluciones: aguapanela caliente, poncho, refugios techados.
Dinero (COP): precios en pesos colombianos formateados ($1.234.567).
4.3 Armas
Arma	Tipo	Daño	Ritmo	Cargador	Munición	Precio base
Cuchillo	Melee	110	—	—	—	(inicial)
Glock-17	Pistola	34	170 rpm	17	9mm	$4.200
P-90	Subametralladora (automática)	19	620 rpm	30	5.7mm	$9.800
Escopeta recortada	Escopeta (6 perdigones)	15×6	68 rpm	6	Cal.12	$7.600
Precisión mejorada agachado/en cobertura; peor corriendo. Disparar sube la Badulaque-Signal (cada 6 disparos).
Munición se compra o se recoge de enemigos caídos (cajas con botiquín o munición).
4.4 Consumibles y equipo
Item	Efecto
Botiquín	+80 salud (tecla Q)
Aguapanela caliente	Sube temperatura y aguante
Poncho impermeable	Reduce el efecto de la lluvia
Soborno policial	Pone la Badulaque-Signal en 0
4.5 Economía y tiendas
Precios dinámicos según `control` del distrito (más control = más caro) y tu notoriedad (sube el precio).
Cada tienda vende un surtido distinto y los contratos del distrito.
Comprar armas nuevas las agrega a tu arsenal; armas repetidas no se venden.
4.6 Contratos secundarios (misiones extra)
Tipo	Descripción	Bonus
Robo	Vaciar una caja fuerte J.S.S	—
Rescate	Liberar y escoltar a un contacto a la guarida del distrito	—
Zafra	Sabotear 2 relés de comunicaciones	—
Silencio	Extraer datos sin levantar la alarma	+70% si la señal sube menos de 12 puntos
Completar contratos: +plata y −10% control del distrito (pero +Badulaque-Signal).
4.7 Combate, sigilo y cobertura
Cobertura (`Space`): −60% de daño recibido (conveniente pegado a un muro).
Sigilo (`C`): el alcance de visión enemiga cae de ~310 px a 130 px; la niebla te cubre más.
Sistema de amenazas: los enemigos patrullan; al verte levantan "!" con sonido de alarma; si te pierden buscan tu última posición; civiles huyen y pueden testificar (sube señal).
4.8 IA de enemigos y NPCs
Tipo	HP	Vel	Comportamiento
Guardia J.S.S	70	92	Patrulla, persigue, dispara. Si te ve: alarma sonora + "!".
Pesado (heavy)	170	80	Más lento, más resistente, más daño, peor puntería.
Dron	50	130	Vuela, orbita al jugador, aparece con señal alta (1–3 drones).
Paraco de calle (thug)	55	110	Ataca a melee cuando estás cerca.
Civil	50	70	Huye con los disparos y puede llamar a J.S.S.
Hacker (aliado)	100	—	Se une al jugador en fase 3, te sigue y dispara enemigos.
Escolta	100	175	Contacto/trama que debés llevar a la guarida.
4.9 Clima y tiempo
Ciclo día/noche real (la partida arranca 09:00) y clima aleatorio: Despejado, Llovizna, Aguacero, Tormenta.
La lluvia: moja, baja temperatura, reduce visibilidad (niebla) y la puntería enemiga; la noche reduce visión y aumenta la caída de señal.
Línea de visión (LOS) calculada por tiles (detecta muros), afectada por clima y noche.
4.10 GPS / navegación
Flecha GPS circular en pantalla con distancia en cuadras al objetivo activo más cercano.
Triángulo direccional sobre tu personaje + contador en el HUD.
Minimapa (esquina) con distritos, % de control, objetivo y ruta punteada animada.
Mapa completo (TAB) con el % de control de cada distrito y los marcadores.
4.11 Muerte y dificultades
Modo	Penalización
Estándar	Pierdes 30% de dinero y parte de munición. Respawneas en la guarida inicial.
Purista	SECTOR REINICIADO: pierdes TODO el equipo y dinero, vuelves solo con $800 y munición básica.
Morir por frío: "Bogotá no perdona. Moriste de puro frío y mugre."
4.12 Guardado
Manual en guaridas seguras (tecla E) y desde el menú de pausa ("Guardar en guarida").
Almacenamiento local del navegador (`jss_save_v1`).
4.13 Flujo de pantallas
Menú principal → Nueva partida / Purista / Continuar → Intro (diálogo) → Mundo abierto (play) →
diálogos, tiendas, combate, mapa, pausa → Muerte (muerte) o Victoria (win).
---
5. Requerimientos funcionales (RF)
RF-01 Iniciar partida nueva en modo Estándar o Purista.
RF-02 Continuar la partida guardada (botón "CONTINUAR", solo visible si hay guardado).
RF-03 Mover al personaje con WASD/flechas, correr con Shift (gasta aguante, se regenera).
RF-04 Mantener la cámara centrada y suavizada sobre el jugador.
RF-05 Apuntar con el ratón y disparar con LMB (semilla de dispersión, cadencia por arma).
RF-06 Golpe cuerpo a cuerpo con RMB.
RF-07 Recargar (R) y cambiar de arma (1–4).
RF-08 Activar/desactivar cobertura (Space): −60% de daño recibido.
RF-09 Activar/desactivar sigilo (C): reduce el alcance de visión enemiga.
RF-10 Usar botiquín o aguapanela (Q); cura menor sin consumible.
RF-11 Interactuar (E) con NPC, guaridas, tiendas, relés, terminales, rehenes, cajas y laptops.
RF-12 Navegación: flecha GPS, distancia en cuadras, marcadores, minimapa y mapa completo (TAB).
RF-13 Sistema clima y tiempo: día/noche, 4 estados de clima, humedad, temperatura e hipotermia.
RF-14 Badulaque-Signal: sube al disparar/matar/atrapar/testigos; decae con el tiempo y el sigilo; a 45%+ refuerzos, a 50%+ drones.
RF-15 IA enemiga: patrulla → búsqueda → persecución → disparo; civiles que huyen y testifican.
RF-16 IA de aliado (hacker): sigue al jugador, selecciona enemigos y dispara.
RF-17 Escolta de NPCs hacia guaridas; su llegada activa eventos de trama.
RF-18 Sistema económico: precios dinámicos por control de distrito y notoriedad; 4 tiendas.
RF-19 Contratos secundarios (robo, rescate, zafra, silencio) con bonus de sigilo.
RF-20 Historia principal en 5 fases con diálogos, objetivos y marcadores.
RF-21 Guardado en guaridas (localStorage) y restauración completa de la partida.
RF-22 Muerte con penalizaciones distintas por modo; reaparición en guarida inicial.
RF-23 Victoria: pantalla "J.S.S DESMANTELADA" con opción de seguir explorando o volver al menú.
RF-24 Menú de pausa (reanudar, guardar, salir) y ayuda contextual ("?") con atajos.
RF-25 Efectos audiovisuales de feedback: flash rojo al recibir daño, sacudida de cámara, partículas, "!" de alarma, borde rojo palpitante, humo, neón, farolas.
---
6. Requerimientos no funcionales (RNF)
RNF-01 Rendimiento: correr a ~60 fps en hardware de gama media (Canvas 2D, solo se dibuja la zona visible).
RNF-02 Sin dependencias externas: un solo archivo `game.js` + `index.html`, funciona offline.
RNF-03 Compatibilidad: navegadores modernos (Chrome, Edge, Firefox, Safari) con Canvas 2D, Web Audio y `requestAnimationFrame`.
RNF-04 Resolución adaptativa: escalado por `devicePixelRatio` y redimensionado al cambiar ventana.
RNF-05 Escala/mundo determinista: generación procedural con semilla fija (misma ciudad en cada partida).
RNF-06 Usabilidad: controles mostrados en el menú, toasts informativos, banner de objetivos.
RNF-07 Accesibilidad de datos: guardado en localStorage (`jss_save_v1`).
---
7. Plataforma y motor
Plataforma: Juego web (HTML5) para navegador de escritorio; sin instalación, listo para
distribuirse como archivo local o publicarse en servicios como itch.io / Netlify / HTTP estático.
Motor de programación:
Canvas 2D (HTML5) para render (tiles, sprites vectoriales, partículas, niebla, minimapa).
Web Audio API para SFX sintetizados (efectos de disparo, explosiones, alarmas), sin archivos de audio.
requestAnimationFrame para el bucle de juego con delta-time.
No usa ningún motor externo ni biblioteca: es código vanilla autocontenido en un solo script.
7.1 Ciclo de juego
`boot()` → `resize()` → `bindUI()` → `loop(t)` con `update(dt)` (lógica, solo en `play`)
y `render()` (dibujado). Los estados globales: `menu, play, pause, shop, dialog, map, death, win`.
---
8. Lenguaje de programación
Aspecto	Detalle
Lenguaje	JavaScript (ECMAScript; estilo ES5/ES6, `'use strict'`)
Estructura	Un único módulo IIFE autocontenido
Paradigmas	Procedural orientado a datos; IA de estados finitos; generación procedural numérica
Nada de frameworks	Sin React/Vue, sin librerías, sin build tools, sin node_modules
RNG	`mulberry32` (PRNG con semilla) para ciudad y variaciones; `Math.random` para efectos efímeros
8.1 "Modelo de lenguaje" (aclaración)
No se usa ningún modelo de lenguaje o IA generativa dentro del juego. Los diálogos están escritos
a mano; la "inteligencia" del mundo viene de:
Generación procedural (función `mulberry32` + semilla) para la ciudad, edificios, props.
IA de comportamiento de estados finitos (patrulla/busca/caza/huye) en `updateEntity`.
Sistemas de simulación: clima, temperatura/humedad, energía (notoriedad), economía y línea de visión.
Eso mantiene el juego 100% determinista, liviano y sin costos de cómputo externos.
---
9. Entorno gráfico ("pixeles y todo eso")
Aspecto	Detalle
Vista	Cenital (top-down) estilo arcade; cámara fija ×2.1 con seguimiento suavizado
Tiles	32×32 px; tamaño visible aprox. coincidente con la ventana (rendering solo de tiles visibles)
Mundo	220×220 tiles = 7.040×7.040 px
Resolución	Adaptable al viewport con escalado por `devicePixelRatio`
Estética	Retro-corporativo low-fi: sprites vectoriales planos, paleta oscura con neón por distrito
Paleta	Fondos `#06080f`; acentos azul corporativo, cian Chapinero, ámbar Candelaria, naranja mercado; rojo alarma
Personaje	Ciudadano bogotano: ruana/poncho ocre, mochila, cachucha azul, piernas animadas al caminar
Enemigos	Formas vectoriales (triángulos) con colores por tipo; barra de vida; "!" de alarma
Entorno vivo	Farolas con halo (más fuerte de noche), neón de distritos (MERCA/BAR/CAFE), humo de chimeneas, papeles al viento, lluvia, niebla
Efectos	Cielo dinámico por hora/clima, tinte por distrito, sacudida de cámara, partículas, flash rojo de daño, borde rojo de vida baja
Overlay (CSS)	Líneas de escaneo + degradado "fotocopiadora" para look VHS corporativo
UI/HUD	Barras (salud, aguante, Badulaque-Signal), temp/humedad, reloj, clima, arma/municiones, dinero, minimapa, objetivos, prompts
---
10. Estado actual y próximos pasos
Actual: prototipo jugable con historia completa, economía, contratos, clima, IA, GPS, guardado y dos modos de dificultad.
Ideas de evolución (roadmap):
Música procedural y SFX por distrito.
Más armas, mejoras de personaje y árbol de habilidades.
Modos: "cacería de drones", desafíos speedrun, survivor nocturno.
Eventos dinámicos por hora (toques de queda, aguaceros torrenciales).
Soporte táctil/móvil y gamepad.
Versión con editor de mods o campañas definidas por distritos.
---
Documento generado a partir del estado real del prototipo (`index.html` + `game.js`, 2026).****
