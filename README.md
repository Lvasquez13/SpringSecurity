# SpringSecurity
Objetivo del proyecto
El objetivo principal de este proyecto es crear una API REST segura y escalable que permita la autenticación y autorización de usuarios mediante JWT. Además, se busca estructurar el código de manera modular para facilitar el mantenimiento y la expansión futura del sistema.


Componentes clave

Spring Security: Se utiliza Spring Security para gestionar la autenticación y autorización en la API. Se configuran filtros de seguridad para interceptar las solicitudes y verificar la validez de los tokens JWT.
JWT (JSON Web Tokens): Se implementa la generación y validación de tokens JWT para la autenticación sin estado. Los tokens contienen información sobre el usuario y sus roles, lo que permite verificar la identidad y los permisos en cada solicitud.
Modularización: El proyecto se divide en módulos independientes para separar las responsabilidades y mejorar la organización del código. Algunos módulos comunes incluyen:
auth: Contiene la lógica relacionada con la autenticación y autorización, incluyendo la generación y validación de JWT.
user: Gestiona la información de los usuarios, como el registro, el inicio de sesión y la gestión de perfiles.
api: Define los controladores REST y los servicios que exponen la funcionalidad de la API.
Escalabilidad: Se aplican principios de diseño que favorecen la escalabilidad, como la arquitectura sin estado (stateless) y el uso de patrones de diseño como la inyección de dependencias.
Flujo de autenticación

El usuario envía sus credenciales (nombre de usuario y contraseña) al endpoint de inicio de sesión.
El servicio de autenticación verifica las credenciales y genera un token JWT.
El token JWT se devuelve al usuario.
En las solicitudes posteriores, el usuario incluye el token JWT en la cabecera "Authorization".
El filtro de seguridad de Spring Security intercepta la solicitud y valida el token JWT.
Si el token es válido, se permite el acceso al recurso solicitado.
Beneficios

Seguridad: Se garantiza la seguridad de la API mediante la autenticación y autorización basadas en JWT.
Escalabilidad: La arquitectura modular y sin estado facilita la escalabilidad del sistema.
Mantenibilidad: La separación de responsabilidades y la organización del código mejoran el mantenimiento y la evolución del proyecto.
Flexibilidad: Spring Security y JWT ofrecen una gran flexibilidad para adaptar la seguridad a las necesidades específicas de la aplicación.
