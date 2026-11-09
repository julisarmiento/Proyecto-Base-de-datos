# Proyecto de Base de Datos

Aplicación de consola desarrollada en **Java** con conexión a una base de datos **PostgreSQL**, como parte de un proyecto académico.

## Sobre el proyecto

El proyecto consiste en el diseño e implementación de una base de datos para una organización que administra padrinos, donantes, programas de ayuda y aportes económicos.

## Funcionalidades

Desde la aplicación de consola es posible:

- Registrar nuevos padrinos.
- Consultar los donantes registrados y eliminar uno por su DNI.
- Listar padrinos junto con los programas a los que aportan, los montos y la frecuencia de los aportes.

## Tecnologías utilizadas

- **PostgreSQL:** sistema de gestión de bases de datos.
- **SQL:** creación de tablas, inserción de datos y consultas.
- **PL/pgSQL:** función y trigger de auditoría.
- **Java:** desarrollo de la aplicación de consola.
- **JDBC:** conexión entre Java y PostgreSQL.

## Instalación y ejecución

### Requisitos previos

- Java.
- PostgreSQL.
- Controlador JDBC de PostgreSQL.

### 1. Clonar el repositorio

### 2. Acceder al directorio

```bash
cd Proyecto-Base-de-datos
```

### 3. Crear la base de datos

Crear una base de datos en PostgreSQL llamada `proyecto`.

Luego, ejecutar los siguientes scripts en este orden:

1. `proyectoDDL.sql` para crear las tablas y demás objetos de la base de datos.
2. `proyectoDML.sql` para cargar los datos de prueba.

### 4. Configurar la conexión

Crear un archivo `datos.txt` en la raíz del proyecto con cuatro líneas:

```text
org.postgresql.Driver
localhost:5432/proyecto
USUARIO
CONTRASEÑA
```

Reemplazar `USUARIO` y `CONTRASEÑA` por las credenciales de la instalación local de PostgreSQL.

### 5. Compilar y ejecutar

En Linux o macOS:

```bash
javac -cp "lib/postgresql-42.7.5.jar" Main.java
java -cp ".:lib/postgresql-42.7.5.jar" Main
```

En Windows:

```bash
javac -cp "lib/postgresql-42.7.5.jar" Main.java
java -cp ".;lib/postgresql-42.7.5.jar" Main
```

Al iniciar, la aplicación muestra un menú con las operaciones disponibles.

## Consultas SQL

El archivo `Ejercicio6/ejercicio6.sql` contiene consultas para:

- Calcular el total de aportes mensuales por programa.
- Identificar donantes que aportan a más de dos programas.
- Consultar donantes con aportes mensuales y sus medios de pago.

---

Proyecto desarrollado con fines académicos.
