# Sistema de Tareas

Aplicación de escritorio desarrollada con **JavaFX** y **Spring Boot** para la administración de tareas. El proyecto implementa operaciones CRUD utilizando **Spring Data JPA** y una base de datos **MySQL**, siguiendo una arquitectura por capas.

## Características

- Agregar tareas.
- Modificar tareas existentes.
- Eliminar tareas.
- Listar tareas en una tabla.
- Seleccionar una tarea para editarla.
- Validación básica de formularios.
- Integración de JavaFX con Spring Boot.

## Tecnologías utilizadas

- Java 21
- JavaFX
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- Lombok

## Arquitectura

El proyecto está organizado en capas para facilitar el mantenimiento y la escalabilidad.

```
gm.tareas
│
├── controlador
│   └── IndexControlador
│
├── modelo
│   └── Tarea
│
├── repositorio
│   └── TareaRepositorio
│
├── servicio
│   ├── ITareaServicio
│   └── TareaServicio
│
├── presentacion
│   └── SistemasTareasFx
│
└── TareasApplication
```

## Funcionalidades

- CRUD completo de tareas.
- Persistencia de datos mediante Spring Data JPA.
- Inyección de dependencias con Spring.
- Interfaz gráfica desarrollada con FXML.
- Actualización automática de la tabla después de cada operación.

## Interfaz

La aplicación permite administrar tareas mediante una interfaz sencilla donde se pueden:

- Registrar nuevas tareas.
- Consultar todas las tareas.
- Editar una tarea seleccionada.
- Eliminar tareas.
- Limpiar el formulario.

## Base de datos

El proyecto utiliza MySQL.

Ejemplo de estructura de la tabla:

```sql
CREATE TABLE tarea (
    id_tarea INT AUTO_INCREMENT PRIMARY KEY,
    nombre_tarea VARCHAR(100),
    responsable VARCHAR(100),
    estatus VARCHAR(50)
);
```

## Instalación

1. Clonar el repositorio.

```bash
git clone https://github.com/usuario/sistema-tareas.git
```

2. Crear la base de datos en MySQL.

```sql
CREATE DATABASE tareas_db;
```

3. Configurar las credenciales en:

```
src/main/resources/application.properties
```

Ejemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tareas_db
spring.datasource.username=root
spring.datasource.password=tu_password

spring.jpa.hibernate.ddl-auto=update
```

4. Ejecutar la aplicación desde:

```
TareasApplication.java
```

## Aprendizajes

Durante el desarrollo de este proyecto se implementaron conceptos como:

- Integración de JavaFX con Spring Boot.
- Inyección de dependencias.
- Arquitectura por capas.
- Persistencia con JPA/Hibernate.
- Uso de FXML y controladores.
- Manejo de componentes JavaFX.
- CRUD completo utilizando Spring Data JPA.

## Autor

**Juan Carlos Hernández Montero**

Estudiante de Ingeniería en Sistemas Computacionales.
