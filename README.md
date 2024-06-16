# todo-list-db

Este proyecto proporciona una base de datos en MySQL para gestionar una lista de tareas (To-Do-List).

## Estructura de la Base de Datos

La base de datos contiene las siguientes tablas:

- `users`: Almacena la información de los usuarios.
- `tasks`: Almacena las tareas de los usuarios.

## Instalación

1. Clona el repositorio: `git clone https://github.com/josemortegam/todo-list-db.git`.
2. navega al directorio del proyecto: `cd todo-list-db`
3. Ejecuta el script SQL para crear la base de datos y las tablas.

## Uso

Para usar la base de datos, sigue las instruciones en el archivo `setup.sql`.

## Instalación detallada

Para configurar y ejecutar la base de datos en un entorno local, sigue estos pasos:

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/josemortegamm/todo-list-db.git
   ```

2. **Navegar al directorio del proyecto**:

   ```bash
   cd todo-list-db
   ```

3. **Ejecutar el escript SQL**:

   Abre tu cliente de Mysql (como MySQL Workbench, la linea de comandos de MySQL o   cualquier otra herramienta que prefieras) y ejecuta el script 'setup.sql':

   ```sql
   source /ruta/a/tu/proyecto/setup.sql;
   ```

## Esquema de la base de datos

### Tabla `users`

- `id`: Identificador único del usuario (INT, NOT NULL, AUTO_INCREMENT, PRIMARY KEY).
- `user_name`: Nombre de usuario (VARCHAR, NOT NULL, UNIQUE).
- `email`: Correo electronico del usuario (VARCHAR, NOT NULL, UNIQUE).
- `password`: Contraseña del usuario (VARCHAR, NOT NULL).
- `created_at`: Fecha y hora de creación del registro (TIMESTAMP).

### Tabla `tasks`

- `id`: Identificador único de la tarea (INT, NOT NULL, AUTO_INCREMENT, PRIMARY KEY).
- `user_id`: Identificador único del usuario que creó la tarea (INT, NOT NULL, FOREING KEY).
- `title`: Titulo de la tarea (VARCHAR, NOT NULL).
- `description`: Descripción de la tarea (TEXT).
- `due_date`: Fehca de vencimiento de la tarea (DATE).
- `status`: Estado de la tarea (`pending`, `completed`).
- `created_at`: Fecha y hora de creación del registro (TIMESTAMP).
- `updated_at`: Fecha y hora de la ultima actualización del registro (TIMESTAMP).

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio importante.
