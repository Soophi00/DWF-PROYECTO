````markdown
#  User Subscription API

API REST desarrollada con **Spring Boot 3** para la gestión de **Usuarios** y sus **Suscripciones**.  
Incluye validaciones, manejo de excepciones, persistencia en **H2 Database**, y documentación con **Swagger UI**.  

---

## ⚙️ Tecnologías usadas
- Java 17
- Spring Boot 3
- Spring Data JPA
- H2 Database
- Lombok
- SpringDoc OpenAPI (Swagger UI)
- Maven

---

## 📋 Requisitos previos
Antes de ejecutar el proyecto asegúrate de tener instalado:
- **Java 17+**
- **Maven 3+**
- **Git**
- IDE recomendado: IntelliJ IDEA / Eclipse / VS Code

---

##  Ejecución del proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Soophi00/DWF-PROYECTO.git
````

2. Entra al directorio del proyecto:

   ```bash
   cd DWF-PROYECTO
   ```
3. Compila y ejecuta con Maven:

   ```bash
   mvn spring-boot:run
   ```

La aplicación correrá en:
 [http://localhost:8080](http://localhost:8080)

---

## 📖 Documentación Swagger

Cuando el proyecto esté corriendo, entra a:
[http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
o
[http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

---

##  Endpoints principales

###  Users

* **POST** `/api/users` → Crear usuario
* **GET** `/api/users/{id}` → Obtener usuario por ID
* **PUT** `/api/users/{id}` → Actualizar usuario
* **DELETE** `/api/users/{id}` → Eliminar usuario
* **GET** `/api/users?q=texto&page=0&size=10&sort=id,asc` → Listar usuarios con paginación y búsqueda

###  Subscriptions

* **POST** `/api/subscriptions` → Crear suscripción
* **GET** `/api/subscriptions/{id}` → Obtener suscripción por ID
* **PUT** `/api/subscriptions/{id}` → Actualizar suscripción
* **DELETE** `/api/subscriptions/{id}` → Eliminar suscripción
* **GET** `/api/subscriptions/user/{userId}?page=0&size=10` → Listar suscripciones por usuario

---

## 🧪 Ejemplo de request (Crear Suscripción)

```json
POST /api/subscriptions
{
  "plan": "PREMIUM",
  "startDate": "2025-09-23",
  "endDate": "2025-12-23",
  "userId": 1
}
```

### Ejemplo de response:

```json
{
  "id": 1,
  "plan": "PREMIUM",
  "startDate": "2025-09-23",
  "endDate": "2025-12-23",
  "userId": 1
}
```

---

##  Colección Postman

Se incluye una colección de **Postman** (`UserSubscriptionAPI.postman_collection.json`) con los endpoints listos para probar.

---

##  Autores

* Sophia Marcela Guzman Ayala
* Marcelo Jose Almendarez Ramirez

```

