# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-15
1. Entidades Principales
videojuego

Almacena el catálogo de títulos de videojuegos competitivos disponibles para las ligas.

Campos: id_juego (clave primaria), nombre, genero y desarrollador.

torneo

Registra las competencias o torneos organizados bajo un videojuego específico.

Campos: id_torneo (clave primaria), nombre, fecha_inicio, fecha_fin y id_juego (clave foránea).

equipos

Controla las organizaciones, clubes y rosters de eSports participantes.

Campos: tag_equipo (clave primaria), razon_social, pais_origen, fecha_fundacion y cantidad_jugadores.

jugadores

Contiene la información personal, apodos y afiliación de los atletas electrónicos.

Campos: id_jugador (clave primaria), nombre_real, apellido_real, nickname, nacionalidad y equipo (clave foránea).

2. Partidos y Rendimiento Competitivo
partido

Administra los encuentros individuales llevados a cabo dentro de un torneo.

Campos: id_partido (clave primaria), fecha, hora, equipo_ganador y id_torneo (clave foránea).

detalles_partido

Especifica los dos equipos contendientes que se enfrentan directamente en cada partido oficial.

Campos: Clave primaria en id_partido, junto con tag_equipo_1 y tag_equipo_2 (claves foráneas hacia equipos).

estadisticas_jugador


IMAGEN DE EJEMPLO DE UNA CONSULTA:
<img width="1037" height="361" alt="image" src="https://github.com/user-attachments/assets/e800c40c-ee29-4b7e-9c64-531e9aafc19d" />

Registra las métricas de rendimiento individual de cada competidor por cada partido disputado.

Campos: Clave primaria compuesta por (id_partido, id_jugador), además de tag_equipo, bajas, muertes, asistencias y danio.
