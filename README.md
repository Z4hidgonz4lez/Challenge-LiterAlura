# LiterAlura

LiterAlura es una aplicación backend desarrollada en **Java con Spring Boot** que permite obtener información de libros desde una API externa, almacenarla en una base de datos PostgreSQL y consultarla mediante una interfaz de consola.

El proyecto integra el consumo de una API pública con la persistencia de datos y consultas a base de datos, permitiendo construir un pequeño sistema de gestión de libros.

---

# Objetivo del proyecto

El objetivo de este proyecto fue desarrollar una aplicación backend capaz de:

* consumir información desde una **API externa**
* procesar y transformar los datos recibidos
* almacenarlos en una **base de datos relacional**
* realizar consultas sobre los datos guardados

Este proyecto permitió practicar conceptos fundamentales de **desarrollo backend con Java y Spring Boot**, incluyendo el consumo de APIs, el manejo de entidades y la persistencia de datos.

---

# Problema que se busca resolver

Muchas APIs públicas ofrecen información útil, pero esa información normalmente se consume en tiempo real y no queda almacenada.

Este proyecto busca resolver ese problema permitiendo:

* obtener información de libros desde una API pública
* almacenar los datos en una base de datos local
* consultar la información posteriormente mediante diferentes criterios

De esta forma se construye un sistema simple para **gestionar información literaria obtenida desde una API externa**.

---

# Arquitectura del sistema

La aplicación sigue un flujo de trabajo sencillo:

```
API Gutendex → Servicio de consumo → Conversión de datos → Persistencia en base de datos → Consultas desde consola
```

Componentes principales:

* **APIConsumption**
  Encargado de realizar la solicitud a la API externa.

* **ConvertData / IConvertData**
  Procesan los datos recibidos en formato JSON.

* **Modelos (Book, Author)**
  Representan las entidades que serán almacenadas en la base de datos.

* **Repositories (BookRepository, AuthorRepository)**
  Permiten realizar operaciones de persistencia y consultas usando Spring Data JPA.

* **Principal**
  Controla la interacción del usuario mediante el menú en consola.

---

# Tecnologías utilizadas

### Lenguaje de programación

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat\&logo=openjdk\&logoColor=white)

### Framework Backend

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat\&logo=springboot\&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=flat)

### Base de datos

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat\&logo=postgresql)

### Manejo de datos

![JSON](https://img.shields.io/badge/JSON-000000?style=flat\&logo=json)
![Jackson](https://img.shields.io/badge/Jackson-000000?style=flat)

### Herramientas

![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat\&logo=apachemaven)
![Git](https://img.shields.io/badge/Git-F05032?style=flat\&logo=git)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat\&logo=github)
![IntelliJ](https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=flat\&logo=intellij-idea)

---

# API utilizada

La aplicación obtiene información de libros desde la siguiente API pública:

Gutendex API

https://gutendex.com/books/

Esta API proporciona datos como:

* título del libro
* autor
* idioma
* información bibliográfica

Los datos obtenidos se transforman y se almacenan en la base de datos PostgreSQL para su posterior consulta.

---

# Estructura del proyecto

El proyecto está organizado siguiendo una estructura típica de aplicaciones Spring Boot.

```
src/main/java/com/alura/Literature

models
  Author.java
  Book.java

repository
  AuthorRepository.java
  BookRepository.java

service
  APIConsumption.java
  ConvertData.java

principal
  Principal.java
```

Cada paquete tiene una responsabilidad específica:

* **models** → define las entidades del sistema
* **repository** → gestiona el acceso a la base de datos
* **service** → maneja la lógica de negocio y el consumo de la API
* **principal** → controla la interacción con el usuario

---

# Funcionalidades del sistema

La aplicación permite realizar las siguientes acciones desde la consola:

1 Buscar libros por título
2 Buscar libros por autor
3 Buscar libros por idioma
4 Buscar autores según su fecha de nacimiento y fallecimiento

Estas consultas se realizan utilizando **Spring Data JPA y consultas derivadas**.

---

# Configuración e instalación

### Clonar el repositorio

```
git clone https://github.com/tu-usuario/literalura.git
```

### Configurar la base de datos

En el archivo `application.properties` se deben configurar los datos de conexión:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/literalura
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
```

### Ejecutar el proyecto

```
./mvnw spring-boot:run
```

---

# Resultados del proyecto

El sistema permite obtener información de libros desde una API externa y almacenarla en una base de datos local para su posterior consulta.

Esto permite interactuar con los datos literarios de manera estructurada y realizar búsquedas mediante distintos criterios.

---

# Qué aprendí

Durante el desarrollo de este proyecto se reforzaron varios conceptos importantes de desarrollo backend:

* Consumo de APIs REST en Java
* Procesamiento de datos JSON
* Uso de Spring Boot para construir aplicaciones backend
* Persistencia de datos con Spring Data JPA
* Diseño de entidades y repositorios
* Organización de proyectos backend en capas

Este proyecto permitió comprender cómo **integrar servicios externos con una base de datos y una aplicación backend estructurada**.

---

# Licencia

Este proyecto se encuentra bajo la licencia MIT.
