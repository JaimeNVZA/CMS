# CMS
Sistema de gestión de contenidos
# Instrucciones para configurar el proyecto

1. **Clona el repositorio** en tu máquina local.

2. **Crea una base de datos nueva** en PostgreSQL.

3. **Configura la base de datos**:
   - Dirígete a `cms/settings.py`.
   - En las líneas aproximadamente 179, configura los siguientes parámetros de acuerdo a tu configuración de PostgreSQL:
     - `NAME`: El nombre de tu base de datos.
     - `USER`: Tu nombre de usuario de PostgreSQL.
     - `PASSWORD`: La contraseña de tu usuario de PostgreSQL.
     - `HOST` (opcional): El host de la base de datos (si no es el predeterminado, usa `localhost`).
     - `PORT` (opcional): El puerto de PostgreSQL (por defecto es `5432`).

4. **Ejecuta las migraciones** y crea los roles:
   - Abre una terminal y ejecuta los siguientes comandos:
     ```bash
     py manage.py migrate
     py manage.py create_roles
     ```

5. **Ejecuta el servidor**:
   - Ejecuta el siguiente comando para iniciar el servidor:
     ```bash
     py manage.py runserver
     ```
   - Dirígete a la URL `http://localhost:8000` en tu navegador para acceder al programa.

Listo, Ahora el proyecto debería estar funcionando en tu entorno local!
