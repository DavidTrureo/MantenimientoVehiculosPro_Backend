# 🛠️ MantenimientoVehiculosPro - Backend API

Este repositorio contiene el backend y la API RESTful para la aplicación móvil "MantenimientoVehiculosPro".
Desarrollado con **Java** y **Spring Boot**, este servicio gestiona la lógica de negocio, la seguridad y la
persistencia de datos en **MySQL** para usuarios, vehículos y registros de mantenimiento.

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/spring_boot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=Spring-Security&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white)
![Maven](https://img.shields.io/badge/maven-%23C71A36.svg?style=for-the-badge&logo=apachemaven&logoColor=white)

## 🚀 Características Principales

* 📡 **API RESTful Robusta**: Endpoints bien definidos para la comunicación con el frontend móvil.
* 🔐 **Seguridad Integrada**: Implementación de **Spring Security** para proteger rutas y gestionar la autenticación.
* 🗄️ **Persistencia con JPA/Hibernate**: Mapeo objeto-relacional eficiente para interactuar con la base de datos MySQL.
* 🔄 **CRUD Completo**: Gestión total del ciclo de vida de Usuarios, Vehículos y Mantenimientos.
* 🏗️ **Arquitectura en Capas**: Código organizado en Controladores, Servicios y Repositorios para mejor mantenibilidad.
* ⚡ **Lombok**: Reducción de código repetitivo (boilerplate) en los modelos y DTOs.

## 📋 Requisitos Previos

Para ejecutar este backend en tu entorno local, necesitas tener instalado:

* **Java Development Kit (JDK) 17** o superior.
* **MySQL Server** (ejecutándose localmente o accesible remotamente).
* **Git** para clonar el repositorio.

## 🛠️ Instalación y Configuración

Sigue estos pasos para levantar el servidor backend:

### 1. Clonar el repositorio

bash
git clone [https://github.com/DavidTrureo/MantenimientoVehiculosPro_Backend.git](https://github.com/DavidTrureo/MantenimientoVehiculosPro_Backend.git)
cd MantenimientoVehiculosPro_Backend


### 2. Configuración de Base de Datos

* Debes crear una base de datos vacía en MySQL. Spring Boot se encargará de crear las tablas automáticamente al iniciar.

* Ejecuta este comando en tu cliente MySQL (Workbench, terminal, etc.):

  SQL
CREATE DATABASE vehiculospro_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

### 3. Configurar Credenciales (Importante)

Debes configurar el acceso a tu base de datos. Abre el archivo src/main/resources/application.properties y edita las siguientes líneas con tu usuario y contraseña reales de MySQL:

src/main/resources/application.properties

Asegúrate que la URL apunta a tu base de datos creada:

spring.datasource.url=jdbc:mysql://localhost:3306/vehiculospro_db?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true

⚠️ CAMBIA ESTO por tu usuario real de MySQL:

spring.datasource.username=root

⚠️ CAMBIA ESTO por tu contraseña real de MySQL:

spring.datasource.password=tu_contraseña_aqui

### 4. Ejecutar la Aplicación

Usa el wrapper de Maven incluido para ejecutar el proyecto sin necesidad de instalar Maven globalmente.

* En macOS / Linux:

  ./mvnw spring-boot:run
  

* En Windows (CMD/PowerShell):

  .\mvnw.cmd spring-boot:run
  

* El servidor iniciará generalmente en http://localhost:8080.

### 📂 Estructura del Proyecto

El proyecto sigue la estructura estándar de directorios de Spring Boot:



```
src/main/java/com/mantenimiento/vehiculospro_api/
├── config/          # Clases de configuración (ej. SecurityConfig)
├── controller/      # Controladores REST (Endpoints de la API)
├── dto/             # Objetos de Transferencia de Datos (Request/Response)
├── model/           # Entidades JPA (Modelos de base de datos)
├── repository/      # Interfaces de acceso a datos (Spring Data JPA)
└── service/         # Lógica de negocio principal
```



## Enlace del Proyecto: https://github.com/DavidTrureo/MantenimientoVehiculosPro_Backend
