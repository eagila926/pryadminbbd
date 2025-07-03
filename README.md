# 🧭 Proyecto Integrador – Administración de Bases de Datos

## 📌 Introducción

Este proyecto tiene como finalidad la **modernización y optimización de la infraestructura de bases de datos** de una agencia de viajes regional. Se ha desarrollado una **plataforma de base de datos heterogénea** compuesta por tres sistemas gestores: **MariaDB**, **Oracle** y **SQL Server**, los cuales están interconectados mediante scripts en Python para lograr sincronización y cohesión entre sus componentes.

La solución permite administrar datos de clientes, reservas, paquetes turísticos y facturación, simulando un entorno real mediante la generación automática de datos con la librería `Faker`.

---

## 👥 Integrantes del Proyecto

- **Elvis Lenin Agila** – Administración y configuración de Oracle.
- **Renato Cardoza** – Documentación técnica e integración con Python.
- **Bryan Ricardo Mazabanda** – Configuración de SQL Server y generación de datos.

---

## ⚙️ Requisitos Técnicos

- **Sistemas Operativos**: Linux (máquinas virtuales)
- **Bases de datos**:
  - MariaDB 10.6
  - Oracle 19c XE
  - SQL Server 2022
- **Python 3.10+**
- **Librerías Python**:
  - `pymysql`
  - `oracledb`
  - `pyodbc`
  - `faker`
- **Herramientas**:
  - DBeaver / SQL Developer / SSMS
  - Trello, GitHub, Google Meet

---

🏗️ Instalación
3. Configurar las bases de datos
Crear las bases de datos ec_turismo_mariadb, turismoec_oracle y EcuatoursSQL.

Importar los scripts SQL de creación de tablas ubicados en /scripts_sql.

Asegúrate de configurar los siguientes puertos en cada máquina virtual:

Oracle → 1522

SQL Server → 1445

MariaDB → 3307

4. Ejecutar el script de interconexión

python insertar_cliente_reserva_factura.py
Este script solicitará los datos de un cliente, mostrará los paquetes disponibles y permitirá registrar una reserva y generar automáticamente una factura.

🔁 Sincronización
La sincronización entre bases se gestiona con scripts en Python programados con cron para ejecutarse cada minuto.

Los scripts leen desde MariaDB y replican información en Oracle y SQL Server según los casos de uso.

📦 Estructura del Repositorio
pgsql
Copiar
Editar
proyecto-bd-heterogenea/
│
├── scripts_sql/
│   ├── mariadb.sql
│   ├── oracle.sql
│   └── sqlserver.sql
│
├── insertar_cliente_reserva_factura.py
├── sync_mariadb_oracle.py
├── sync_sqlserver_mariadb.py
├── README.md
✅ Resultados
Plataforma funcional y robusta con tres SGBD interconectados.

Modelo de datos probado con inserciones reales.

Arquitectura escalable y modular para futuras expansiones.

