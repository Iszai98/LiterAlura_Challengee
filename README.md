# Proyecto de Literalura

Aplicación de consola desarrollada en **Java 21** con **Spring Boot** y **Maven** que permite buscar, guardar y gestionar libros y autores desde la API pública [Gutendex](https://gutendex.com/), almacenando los datos en una base de datos **PostgreSQL**.

##  Autor

## isazai 98

---

##  Tecnologías utilizadas

- Java 21
- Spring Boot 4.0.3
- Maven
- Spring Data JPA / Hibernate
- PostgreSQL
- Jackson Databind 2.20.1 (deserialización de JSON)
- API Gutendex (`https://gutendex.com`)

///

##  Funcionalidades

- Todas las opciones a excepción de la primera utilizan los libros y autores guardados en la base de datos personal.
  
| Opción | Descripción |
|--------|-------------|
| 1 | Agregar un libro a la colección buscándolo en la API |
| 2 | Buscar un libro en la base de datos por título |
| 3 | Mostrar todos los libros guardados |
| 4 | Listar todos los autores guardados |
| 5 | Listar autores vivos en un año determinado |
| 6 | Listar libros por idioma |
| 7 | Ver el Top 10 de libros más descargados |
| 0 | Salir de la aplicación |

///

##  Configuración

### 1. Requisitos previos

- Tener Java 21 instalado
- PostgreSQL instalado y corriendo con una cuenta activa
- Una base de datos creada llamada `literalura` en PostgreSQL

### 2. Variables de entorno

La aplicación usa variables de entorno para proteger las credenciales. Te recomiendo configurarlas para tu IDE:

| Variable | Descripción |

| `DB_HOST` | Host de la base de datos (ej: `localhost`) |

| `DB_USER` | Usuario de PostgreSQL |

| `DB_PASSWORD` | Contraseña de PostgreSQL |

///

## Cómo ejecutar

1. Clona el repositorio o descarga el archivo WinRAR.

2. Configura las variables de entorno con tus credenciales de PostgreSQL.

3. Ejecuta la aplicación con Maven.

4. Sigue las instrucciones del menú en consola.

//

##  Notas importantes

- Al agregar un libro, si el autor ya existe en la base de datos se reutiliza para evitar duplicados.
- Si un libro ya fue guardado previamente, la aplicación lo notifica sin generar errores.
- Los libros con idiomas no registrados en el sistema se guardan con idioma `null`.
- La búsqueda por título es flexible e ignora mayúsculas/minúsculas.

//


Este proyecto esta desarrollado como parte del Challenge de Spring Boot de [Alura Cursos](https://www.aluracursos.com/).
