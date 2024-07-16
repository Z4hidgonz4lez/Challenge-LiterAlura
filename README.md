LiterAlura
Descripción
LiterAlura es una aplicación desarrollada para gestionar información de libros obtenida de una API externa y almacenada en una base de datos PostgreSQL. La aplicación utiliza Spring Framework y se centra en la obtención, persistencia y consulta de datos, así como en la interacción por consola.

Características
Obtener información de libros desde la API de Gutendex.
Persistir datos de libros en una base de datos PostgreSQL.
Consultar y generar estadísticas sobre los datos almacenados.
Interactuar con la aplicación a través de la consola.
Tecnologías Utilizadas
Java 17
Spring Boot
Spring Data JPA
PostgreSQL
Streams y Lambdas en Java
JPQL y Consultas Derivadas
Jackson para deserialización
Instalación
Clona el repositorio:
bash
Copiar código
git clone https://github.com/tu-usuario/literalura.git
Navega al directorio del proyecto:
bash
Copiar código
cd literalura
Configura la base de datos PostgreSQL en el archivo application.properties:
properties
Copiar código
spring.datasource.url=jdbc:postgresql://localhost:5432/literalura
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
Ejecuta el proyecto usando Maven:
bash
Copiar código
./mvnw spring-boot:run
Uso
Interacción por Consola
La aplicación permite interactuar con la base de datos de libros a través de la consola. Puedes realizar las siguientes acciones:

Obtener información de libros desde la API:
Ejecuta el método correspondiente en tu clase de servicio para obtener y almacenar libros en la base de datos.

Consultar libros en la base de datos:
Utiliza los métodos de consulta implementados en los repositorios para buscar y filtrar libros según tus necesidades.

Ejemplo de Configuración de URL de la API
Asegúrate de especificar la URL de la API de Gutendex en el código donde se realiza la llamada a la API externa. Por ejemplo:

java
Copiar código
String apiUrl = "https://gutendex.com/books/";
Contribución
Las contribuciones son bienvenidas. Para contribuir, por favor sigue los siguientes pasos:

Haz un fork del repositorio.
Crea una rama para tu nueva función (git checkout -b feature/nueva-funcion).
Haz commit de tus cambios (git commit -am 'Agrega nueva función').
Haz push a la rama (git push origin feature/nueva-funcion).
Abre un Pull Request.
Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
