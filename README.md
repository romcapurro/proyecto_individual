# API de Análisis de Datos de Juegos de Steam

Este proyecto consiste en una API desarrollada con **FastAPI** para realizar análisis y consultas de datos relacionados con juegos de la plataforma Steam. La API se conecta a una base de datos SQLite y utiliza archivos Parquet para almacenar y procesar información. Permite realizar operaciones de almacenamiento, análisis de datos y recomendaciones de juegos.

## Documentación en Swagger
`https://app.swaggerhub.com/apis-docs/ROMCAPURRO_1/steam-data_api/1#/`

## Endpoints Principales

### Documentación de la API

- **Descripción:** Muestra la documentación para los endpoints disponibles.

    **Endpoint:** `/` [GET]

### Consultas y Análisis

- **Endpoint:** `https://proyecto-individual-dqlw.onrender.com/PlayTimeGenre/{genre}` [GET]
- **Descripción:** Obtiene el año de lanzamiento con más horas jugadas para un género específico.

- **Endpoint:** `https://proyecto-individual-dqlw.onrender.com/UserForGenre/{genre}` [GET]
- **Descripción:** Obtiene al usuario con más horas jugadas para un género específico.

- **Endpoint:** `https://proyecto-individual-dqlw.onrender.com/UsersRecommend/{year}` [GET]
- **Descripción:** Obtiene los 3 juegos más recomendados para un año específico.

- **Endpoint:** `https://proyecto-individual-dqlw.onrender.com/UsersNotRecommend/{year}` [GET]
- **Descripción:** Obtiene los 3 juegos menos recomendados para un año específico.

- **Endpoint:** `https://proyecto-individual-dqlw.onrender.com/SentimentAnalysis/{year}` [GET]
- **Descripción:** Realiza análisis de sentimiento para un año específico.

- **Endpoint:** `/RecommendedGames/{id}` [GET]
- **Descripción:** Obtiene juegos similares basados en un juego específico.

## ETL - Procesos de Extracción, Transformación y Carga

El proyecto incluye una serie de procesos ETL que se encargan de cargar, transformar y almacenar datos para su posterior análisis. A continuación, se describen los ETL realizados:

- **ETL output_steam_games.json:** Proceso de limpieza y transformación del archivo JSON de juegos de Steam para generar archivos Parquet.

- **ETL australian_users_items.json:** Proceso de normalización y división del archivo JSON de elementos de usuarios para generar archivos Parquet.

- **ETL australian_user_reviews.json:** Proceso de análisis de sentimiento y transformación del archivo CSV de reseñas de usuarios para generar archivos Parquet.

- **Generación de Modelos:** Creación de archivos Parquet para modelado de juegos y análisis de similitud.

## Notas

El proyecto hace uso de múltiples bibliotecas y tecnologías, tales como FastAPI para la creación de la API, Pandas para el manejo de datos, SQLite para la base de datos, entre otras.