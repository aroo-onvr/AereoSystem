# AereoSystem

Sistema de venta de boletos de avión desarrollado como proyecto escolar utilizando Python y Programación Orientada a Objetos (POO).

El sistema permite visualizar los asientos de un avión, consultar su disponibilidad, seleccionar uno o varios asientos y realizar la venta de boletos mediante una interfaz gráfica.

## Características

* Visualización del mapa de asientos del avión.
* Identificación de asientos disponibles, ocupados y seleccionados.
* Selección de uno o varios asientos.
* Consulta de información de cada asiento.
* Cálculo automático del precio de los boletos.
* Diferentes clases de asiento:

  * Primera Clase
  * Clase Media
  * Clase Comercial
* Recargo adicional para asientos de ventanilla.
* Registro del estado de los asientos.
* Persistencia de información mediante una base de datos SQLite.
* Interfaz gráfica desarrollada con CustomTkinter.
* Resumen de la compra antes de confirmar la venta.

## Tecnologías utilizadas

* **Python**
* **CustomTkinter** — Interfaz gráfica.
* **SQLite** — Base de datos.
* **Programación Orientada a Objetos (POO)**
* **Git / GitHub** — Control de versiones.

## Precios

Los precios base utilizados por el sistema son:

| Clase           | Precio base |
| --------------- | ----------: |
| Primera Clase   |       $1100 |
| Clase Media     |       $1050 |
| Clase Comercial |       $1000 |

Los asientos de ventanilla cuentan con un recargo del **15%** sobre el precio base.

## Distribución del avión

El avión cuenta con **90 asientos**, distribuidos en filas de la A a la O.

La distribución de clases es:

* **A - C:** Primera Clase
* **D - K:** Clase Media
* **L - O:** Clase Comercial

La interfaz representa la distribución de los asientos y el pasillo central para facilitar su selección.

## Estados de los asientos

El sistema utiliza diferentes colores para representar el estado de cada asiento:

* **Verde:** Disponible
* **Rojo:** Ocupado
* **Azul:** Seleccionado

Esto permite identificar rápidamente qué asientos pueden ser adquiridos.

## Base de datos

El proyecto utiliza **SQLite** para almacenar y administrar la información relacionada con los asientos y las ventas.

La conexión y las operaciones de la base de datos se encuentran principalmente en:

```text
dataBase.py
```

La información almacenada permite conservar el estado de los asientos incluso después de cerrar la aplicación.

## Estructura del proyecto

```text
AereoSystem/
│
├── app.py
├── avion.py
├── dataBase.py
├── funciones.py
├── main.py
├── venta.py
├── .gitignore
└── README.md
```

### Descripción de los archivos

| Archivo        | Descripción                                                             |
| -------------- | ----------------------------------------------------------------------- |
| `app.py`       | Contiene la interfaz gráfica principal de la aplicación.                |
| `avion.py`     | Maneja la información y lógica relacionada con el avión y sus asientos. |
| `dataBase.py`  | Gestiona la conexión y operaciones con la base de datos SQLite.         |
| `funciones.py` | Contiene funciones auxiliares utilizadas por el sistema.                |
| `venta.py`     | Gestiona la información relacionada con las ventas de boletos.          |
| `main.py`      | Punto de entrada para ejecutar la aplicación.                           |
| `.gitignore`   | Especifica archivos que no deben incluirse en el repositorio.           |

## Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/aroo-onvr/AereoSystem.git
```

### 2. Entrar al directorio

```bash
cd AereoSystem
```

### 3. Instalar las dependencias

El proyecto utiliza CustomTkinter. Puede instalarse mediante:

```bash
pip install customtkinter
```

SQLite forma parte de la biblioteca estándar de Python, por lo que no requiere una instalación adicional.

## Ejecución

Para iniciar el sistema:

```bash
python main.py
```

Al ejecutar el programa se abrirá la interfaz gráfica del sistema de venta de boletos.

## Flujo de uso

1. Iniciar la aplicación.
2. Visualizar el mapa del avión.
3. Seleccionar uno o varios asientos disponibles.
4. Consultar la información y precio de los asientos seleccionados.
5. Revisar el resumen de la compra.
6. Confirmar la selección.
7. El sistema actualiza el estado de los asientos y registra la venta.

## Arquitectura

El proyecto está organizado utilizando principios de **Programación Orientada a Objetos**, separando las responsabilidades principales del sistema.

De forma general:

```text
Interfaz gráfica
      │
      ▼
     App
      │
      ▼
    Avion
      │
      ├── Asientos
      │
      └── Ventas
      │
      ▼
   BaseDatos
      │
      ▼
    SQLite
```

Esta separación permite mantener la interfaz, la lógica del sistema y el almacenamiento de datos organizados en diferentes módulos.

## Metodología

El proyecto fue desarrollado como parte de un trabajo escolar utilizando la metodología **Scrum**.

El equipo se organizó en los siguientes roles:

* **3 Developers**
* **1 Scrum Master**
* **1 Product Owner**

El desarrollo se dividió en diferentes tareas relacionadas con la base de datos, lógica del sistema, gestión de ventas e interfaz gráfica.

## Objetivo del proyecto

El objetivo principal de AereoSystem es desarrollar un sistema funcional que simule el proceso de venta de boletos de una aerolínea, aplicando conocimientos de:

* Python
* Programación Orientada a Objetos
* Interfaces gráficas
* Bases de datos
* Gestión de información
* Metodologías ágiles
* Control de versiones con Git y GitHub

## Estado del proyecto

**Proyecto finalizado y funcional.**

El sistema cumple con las funciones principales planteadas para el proyecto escolar y se encuentra disponible públicamente en GitHub.

## Autor

**Aarón Vázquez**

Proyecto escolar desarrollado con fines educativos.

---

## Repositorio

[GitHub - AereoSystem](https://github.com/aroo-onvr/AereoSystem)