# 🔌 db_manager_app

Bienvenido a `db_manager_app`, una aplicación desarrollada en **Python 3.11** con **Flet** para conectarse y gestionar diferentes tipos de bases de datos (MySQL, SQLite, PostgreSQL, SQL Server y MongoDB). Su diseño busca ofrecer una experiencia de usuario intuitiva, segura, extensible y portable.

---

## 🎯 Objetivo

El objetivo principal es centralizar la gestión de bases de datos en una sola aplicación amigable, compatible con múltiples motores, permitiendo:

- Visualización de tablas, vistas, funciones, procedimientos, índices y disparadores.
- Gestión de usuarios y roles (según el motor).
- Importación y exportación de datos y estructuras.
- Administración visual con interfaz Flet.

---

## ⚙️ Funcionalidades

  🔌 Conexión a múltiples motores de base de datos: MySQL, SQLite, PostgreSQL, SQL Server y MongoDB

  📂 Exploración visual de objetos de bases de datos:

    - Tablas, Vistas, Procedimientos, Funciones, Disparadores, Índices

  👥 Gestión de Usuarios y Roles (según compatibilidad del motor)

  🔄 Importación y Exportación:

    - CSV, JSON, y scripts SQL

  📊 Visualización interactiva de resultados

  💾 Múltiples conexiones guardadas y seguras

  💡 Interfaz moderna y responsiva con Flet

  🧩 Arquitectura modular y extensible

  🛡 Seguridad en manejo de contraseñas y consultas

---

## 📂 Estructura del Proyecto

```bash
db_manager_app/
├── main.py                         # Punto de entrada principal con Flet
├── ui/                             # Módulo de interfaces de usuario 
│ ├── layout.py                     # Layout general (sidebar, navbar)
│ ├── db_viewer.py                  # Panel para ver Tablas, Vistas, etc.
│ └── dialogs.py                    # Diálogos para importar/exportar
├── controllers/                    # Módulo de controladores
│ ├── db_controller.py              # Lógica de conexión y ejecución de queries
│ └── export_import.py              # Funcionalidades de importación/exportación
├── models/                         # Módulo de modelos
│ ├── database.py                   # Definición abstracta y clases específicas para MySQL, SQLite, etc.
├── services/                       # Módulo de servicios
│ └── utils.py                      # Validaciones, encriptación, helpers
├── assets/                         # Archivos estáticos
│ ├── icons/                        # Íconos personalizados
│ └── styles/                       # Estilos CSS si usas HTML embebido
├── data/                           # Archivos exportados/importados
├── tests/                          # Módulo de pruebas unitarias
│ ├── init.py                       # Iniciador de pruebas
│ ├── test_connections.py           # Pruebas de conexión y ejecución de queries
│ ├── test_export_import.py         # Pruebas de importación y exportación
│ └── test_utils.py                 # Pruebas de utilidades
├── setup.py                       # Script para empaquetar como módulo instalable
├── requirements.txt                # Dependencias
├── pyproject.toml                  # Configuración estándar de empaquetado (PEP 621)
├── pytest.ini                      # Configuración para la ejecucion de los test
└── .gitignore                      # Ignora archivos y carpetas para Git

```

---

## 📚 Requisitos

- Python 3.10 o superior (desarrollado y probado en Python 3.11)
- Navegador moderno o entorno gráfico compatible con Flet
- Controladores para los SGBD que se deseen usar
- Conexión a Internet para instalación de librerías (primera vez)
- Virtualenv o entorno similar
- Navegador web moderno o entorno de escritorio para Flet

> **Librerías necesarias:**
> - flet
> - pandas
> - mysql-connector-python / PyMySQL
> - psycopg2
> - pyodbc
> - pymongo
> - openpyxl
> - cryptography
> - python-dotenv
> - pyinstaller
> - pytest (para pruebas)

---

## 🚀 Instalación rápida

```bash
git clone https://github.com/deytonriasco/db_manager_app.git
cd db_manager_app
python -m venv env
source env/bin/activate   # Windows: env\Scripts\activate
pip install -r requirements.txt
python main.py
```

---

## 🛠️ Empaquetado (Opcional)

### ♻️ Opcion 1: Instalador Python (.whl / .tar.gz)

Empaqueta el proyecto:
```bash
python setup.py sdist bdist_wheel
```

Instala localmente:
```bash
pip install dist/db_manager_app-1.0.0-py3-none-any.whl
```

### 🔗 Opcion 2: Ejecutable (.exe para Windows)

Instala PyInstaller:
```bash
pip install pyinstaller
```

Genera el ejecutable:
```bash
pyinstaller --onefile --noconsole main.py --name db_manager_app
```

---

### ✅ Pruebas

- El proyecto incluye pruebas unitarias utilizando unittest.
```bash
python -m unittest discover -s tests
```

### 🔌 Librerías principales
- flet – interfaz gráfica reactiva
- pymysql, mysql-connector-python – MySQL
- psycopg2 – PostgreSQL
- sqlite3 – SQLite
- pyodbc – SQL Server
- pymongo – MongoDB
- pandas – manejo de datos
- cryptography – seguridad de credenciales

---

## 🛠️ ¿Cómo contribuir?
-Haz un fork del repositorio.
-Crea una nueva rama (git checkout -b feature-nueva).
-Realiza tus cambios y haz commit (git commit -m 'Agrega nueva funcionalidad').
-Sube la rama (git push origin feature-nueva).
-Abre un Pull Request.

---

## 📜 Licencia

Este proyecto está licenciado bajo la **MIT License**.

---

## ✍️ Autor

✍️ **Desarrollado por:** **Deyton Riasco Ortiz**  
🗓️ **Fecha:** 2025  
📧 **Contacto:** [deyton007@gmail.com](mailto:deyton007@gmail.com)

---

# 🌐 Feedback
¿Tienes ideas, sugerencias o encontraste un error?
¡Haz un fork, crea un issue o envía un pull request!

---