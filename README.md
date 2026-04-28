Una plataforma moderna y robusta para la creación, gestión y compartición de guías de videojuegos. Este proyecto combina una arquitectura de microservicios (Backend en Spring Boot) con una interfaz de usuario dinámica y reactiva (Frontend en Vue.js).

## ✨ Características Principales

- **Gestión de Guías**: Crea, edita y elimina guías detalladas para tus juegos favoritos.
- **Sistema de Comentarios**: Interactúa con otros usuarios y deja feedback en sus guías.
- **Valoraciones**: Sistema de "likes" para destacar las mejores guías de la comunidad.
- **Categorización**: Filtra guías por juego y categoría para encontrar exactamente lo que necesitas.
- **Autenticación de Usuarios**: Sistema seguro para el registro e inicio de sesión.

---

## 🛠️ Stack Tecnológico

### Backend
- **Lenguaje:** Java 17
- **Framework:** Spring Boot 3.2.4
- **Persistencia:** Spring Data JPA / Hibernate
- **Base de Datos:** MySQL
- **Herramientas:** Maven

### Frontend
- **Framework:** Vue.js 3 (Composition API)
- **Bundler:** Vite
- **Estado:** Pinia
- **Routing:** Vue Router
- **HTTP Client:** Axios

---

## 🚀 Configuración y Ejecución

### Requisitos Previos
- **JDK 17** o superior.
- **Node.js** (v18+) y npm.
- **MySQL Server** funcionando.

### 1. Base de Datos
Crea una base de datos llamada `foro_db` en tu servidor MySQL:
```sql
CREATE DATABASE foro_db;
```

### 2. Backend (Spring Boot)
Navega a la raíz del proyecto y configura tus credenciales en `src/main/resources/application.properties` (si son diferentes a las por defecto):
```bash
mvn spring-boot:run
```
El servidor se iniciará en `http://localhost:8080`.

### 3. Frontend (Vue.js)
Navega a la carpeta del frontend y arranca el servidor de desarrollo:
```bash
cd foro-frontend
npm install
npm run dev
```
La aplicación estará disponible en `http://localhost:5173` (o el puerto que asigne Vite).

---

## 📂 Estructura del Proyecto

```text
foro/
├── src/main/java/com/foro/
│   ├── controller/    # Endpoints de la API REST
│   ├── model/         # Entidades de JPA
│   ├── repository/    # Interfaces de acceso a datos
│   ├── service/       # Lógica de negocio
│   └── dto/           # Objetos de Transferencia de Datos
├── foro-frontend/
│   ├── src/
│   │   ├── components/ # Componentes reutilizables
│   │   ├── views/      # Páginas principales
│   │   ├── store/      # Gestión de estado (Pinia)
│   │   └── router/     # Configuración de rutas
└── pom.xml            # Configuración de Maven
```

---

## 📝 Notas de Desarrollo
- El proyecto utiliza `hibernate.ddl-auto=update`, por lo que las tablas se crearán automáticamente al iniciar el backend.
- Asegúrate de tener el backend corriendo antes de interactuar con el frontend para que las peticiones a la API funcionen correctamente.

---

Desarrollado con ❤️ para la comunidad de gaming.
