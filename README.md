# PROYECTO RED - FORMATIVO (SENA)
Un proyecto colaborativo de enfoque a una empresa de estampación textil, ubicada en el area de medellin con el objetivo de tener mas alcance en el area web y avance en la tecnologia 3D para la modificacion, creacion y compra de camisetas a su gusto

Markdown
# 🚀 Guía de Inicio del Proyecto Django

Este documento contiene las instrucciones paso a paso para configurar e iniciar el entorno de desarrollo local para el proyecto.

---

## 📋 Requisitos Previos

- **Python 3.10+** instalado en el sistema.
- **Git** instalado para control de versiones.

---

## 🛠️ Paso a Paso para la Configuración

### 1. Clonar el repositorio y acceder a la carpeta
```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_PROYECTO>
2. Crear y activar el entorno virtual
Crear un entorno virtual aísla las dependencias del proyecto de tu sistema global.

En macOS / Linux:

Bash
python3 -m venv venv
source venv/bin/activate
En Windows (Git Bash):

Bash
python -m venv venv
source venv/Scripts/activate
En Windows (CMD / PowerShell):

3. Instalar dependencias
Instala la versión específica de Django para este proyecto (Django 5.2.16):

Bash
pip install Django==5.2.16
(Opcional: Si cuentas con un archivo requirements.txt, ejecuta):

Bash
pip install -r requirements.txt
4. Inicializar la estructura del proyecto (Solo la primera vez)
Nota: Ejecuta este paso únicamente si estás iniciando el repositorio desde cero.

Bash
# Crear el proyecto base (el punto . evita carpetas anidadas innecesarias)
django-admin startproject config .

# Crear la primera aplicación
python manage.py startapp mi_app
Recuerda registrar la aplicación en config/settings.py:

Python
INSTALLED_APPS = [
    # Aplicaciones por defecto...
    'django.contrib.admin',
    'django.contrib.auth',
    '...',
    
    # Aplicaciones del proyecto
    'mi_app',
]
5. Ejecutar migraciones
Prepara y sincroniza la base de datos local:

Bash
python manage.py migrate
6. Crear un superusuario (Administrador)
Crea una cuenta de acceso para el panel de administración de Django:

Bash
python manage.py createsuperuser
7. Iniciar el servidor de desarrollo
Levanta el servidor local para comenzar a trabajar:

Bash
python manage.py runserver
