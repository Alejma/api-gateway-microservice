# 🔄 API Gateway Microservice

Este microservicio funciona como puerta de entrada (API Gateway) para una arquitectura de microservicios, implementado con Spring Cloud Gateway siguiendo principios de Clean Architecture.

## 📋 Tabla de Contenidos
- [Tecnologías principales](#-tecnologías-principales)
- [Configuración requerida](#-configuración-requerida)
- [Endpoints principales](#-endpoints-principales)
- [Seguridad](#-seguridad)
- [Estructura de Clean Architecture](#-estructura-de-clean-architecture)
- [Dockerización](#-dockerización-opcional)
- [Testing](#-testing)
- [Notas importantes](#-notas-importantes)

## 📦 Tecnologías principales

| Tecnología | Uso |
|------------|-----|
| Java 17+ | Lenguaje base |
| Spring Boot 3 | Framework principal |
| Spring Cloud Gateway | Enrutamiento dinámico |
| Spring Security | Autenticación y autorización |
| JWT | Manejo de tokens |
| Maven | Gestión de dependencias |
| Lombok | Reducción de código boilerplate |
| Docker | Containerización |

## ⚙️ Configuración requerida

### Variables de entorno esenciales

```env
JWT_SECRET=myVerySecretKeyForHS512
AUTH_SERVICE_URL=http://localhost:8081
USER_SERVICE_URL=http://localhost:8082
```
## 🚀 Endpoints Principales

### 🔐 Microservicio de Autenticación
| Método | Endpoint       | Descripción                     | Autenticación Requerida |
|--------|----------------|---------------------------------|-------------------------|
| `POST` | `/auth/login`  | Autentica usuario y devuelve JWT | ❌ No                   |
