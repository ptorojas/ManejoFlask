# ManejoFlask
Zona Fit Gym es una aplicación web completa desarrollada con Flask que implementa un sistema CRUD (Crear, Leer, Actualizar, Eliminar) para la gestión de clientes de un gimnasio. Esta aplicación demuestra habilidades en desarrollo backend con Python/Flask, frontend con Bootstrap 5, y conexión a bases de datos MySQL con pooling de conexiones.

# Zona Fit - Aplicación Web de Gestión de Gimnasio

Una aplicación web desarrollada con Flask para la gestión de clientes de un gimnasio (Zona Fit). Permite realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre los clientes, almacenando la información en una base de datos MySQL.

## Características

- **Interfaz de usuario moderna y responsive**: Diseñada con Bootstrap 5 y CSS, adaptable a diferentes dispositivos.
- **Operaciones CRUD completas**:
  - Listar todos los clientes.
  - Agregar nuevos clientes.
  - Editar información de clientes existentes.
  - Eliminar clientes.
- **Validación de formularios**: Implementada con Flask-WTF y WTForms.
- **Conexión a base de datos MySQL con pooling de conexiones**: Para un manejo eficiente de las conexiones a la base de datos.

## Tecnologías Utilizadas

- **Backend**:
  - Python 3
  - Flask (Framework web)
  - Flask-WTF (Para formularios)
  - MySQL Connector/Python (Para la conexión a MySQL)
- **Frontend**:
  - HTML5
  - CSS3
  - Bootstrap 5
  - Bootstrap Icons
- **Base de datos**:
  - MySQL

## Estructura del Proyecto

zona-fit-gym/
├── app.py # Aplicación principal de Flask
├── cliente.py # Clase Cliente (modelo)
├── cliente_dao.py # Clase ClienteDAO (Data Access Object)
├── cliente_forma.py # Clase ClienteForma (formulario WTForms)
├── conexion.py # Clase Conexion (pool de conexiones a MySQL)
├── templates/
│ └── index.html # Plantilla HTML principal
├── static/ # (Opcional) Carpeta para archivos estáticos (CSS, JS, imágenes)
├── requirements.txt # Dependencias del proyecto
└── README.md # Este archivo


## Configuración y Ejecución

### Prerrequisitos

- Python 3.8 o superior.
- MySQL Server.
- Crear una base de datos llamada `zona_fit_db` (o ajustar el nombre en `conexion.py`).

### Pasos

1. Clonar el repositorio:
   ```bash
   git clone <url-del-repositorio>
   cd zona-fit-gym

2. Crear un entorno virtual (recomendado) y activarlo:

   python -m venv venv
  # En Windows:
    venv\Scripts\activate
  # En Linux/Mac:
    source venv/bin/activate

Instalar las dependencias:

bash
pip install -r requirements.txt
Si no tienes requirements.txt, instala las siguientes dependencias:

bash
pip install flask flask-wtf mysql-connector-python
Configurar la base de datos:

Asegúrate de que MySQL esté en ejecución.

Crea una base de datos llamada zona_fit_db (o la que hayas configurado).

Crea la tabla cliente con la siguiente estructura:

sql
CREATE TABLE cliente (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nombre VARCHAR(100) NOT NULL,
  apellido VARCHAR(100) NOT NULL,
  membresia INT NOT NULL
);
Configurar los datos de conexión a la base de datos en conexion.py:

python
DATABASE = 'zona_fit_db'
USERNAME = 'root'
PASSWORD = 'tu_contraseña'
DB_PORT = '3306'
HOST = 'localhost'
Ejecutar la aplicación:

bash
python app.py
Abrir en el navegador: http://localhost:5000

Uso
Agregar un nuevo cliente: Completa el formulario a la izquierda con el nombre, apellido y membresía (número) y haz clic en "Guardar".

Editar un cliente: Haz clic en el botón de editar (lápiz) en la tabla. Los datos se cargarán en el formulario. Modifica y guarda.

Eliminar un cliente: Haz clic en el botón de eliminar (basura) en la tabla.

Posibles Mejoras Futuras
Agregar autenticación de usuarios (administradores, empleados, clientes).

Implementar roles y permisos.

Agregar más entidades (clases, entrenadores, pagos, etc.).

Generar reportes (clientes por membresía, ingresos, etc.).

Mejorar la interfaz de usuario con más características de Bootstrap (modales para confirmar eliminación, etc.).

Agregar búsqueda y paginación en la tabla de clientes.

Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un issue para discutir los cambios que te gustaría hacer o envía un pull request.

Licencia
Este proyecto está bajo la licencia MIT. Ver el archivo 
