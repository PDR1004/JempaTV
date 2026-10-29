JempaTV 📺

JempaTV es una aplicación web desarrollada con Angular y el ABP Framework, diseñada para ser una plataforma de streaming personalizada. Permite a los usuarios descubrir, gestionar y calificar series y películas, ofreciendo una experiencia de visualización rica e interactiva.

🚀 Características

Descubrimiento de Series: Explora y busca series utilizando IDs de IMDB, con detalles obtenidos de APIs externas.

Gestión de la Lista de Seguimiento (Watchlist): Añade series a una lista de seguimiento personal, haz un seguimiento del estado de visualización y elimínalas.

Recomendaciones Personalizadas: Recibe recomendaciones de series basadas en la actividad del usuario y sus calificaciones.

Autenticación y Autorización de Usuarios: Cuentas de usuario seguras con inicio de sesión, registro y control de acceso basado en roles (Administrador).

Panel de Estadísticas de la API: Monitorea el uso de la API, los errores y los tiempos de respuesta.

Gestión del Perfil de Usuario: Actualiza la información del perfil de usuario, incluyendo fotos de perfil y preferencias de correo electrónico.

Notificaciones: Recibe notificaciones dentro de la aplicación sobre eventos relevantes.

Soporte Multilingüe: La aplicación soporta múltiples idiomas, incluyendo inglés y español.

Panel de Administración: Acceso a funcionalidades administrativas para gestionar la aplicación.

🛠️ Tecnologías

Frontend: Angular, TypeScript, HTML, CSS, SCSS

Backend: .NET (ABP Framework)

Bases de Datos: Entity Framework Core (implícito por las migraciones)

Estilos: Bootstrap, SCSS Personalizado

Librerías: Swiper.js (carruseles), Chart.js (visualización de datos), Ngx-Datatable

Contenerización: Docker

📦 Instalación

Prerrequisitos

.NET 8.0+ SDK

Node.js v18 o v20

Yarn

Docker

Configuración del Backend

Clonar el repositorio:

git clone https://github.com/PDR1004/JempaTV.git
cd JempaTV


Instalar dependencias del lado del cliente (si clonaste el repositorio):

cd angular
yarn install


Ejecutar el migrador de la base de datos:

cd ../src/JempaTV.DbMigrator
dotnet run


Esto creará la base de datos inicial y poblará los datos iniciales.

Generar un certificado de firma (para producción):

dotnet dev-certs https -v -ep openiddict.pfx -p 86402479-7d42-49ac-a3f0-e8dc50579021


Reemplaza la contraseña (86402479-7d42-49ac-a3f0-e8dc50579021) según sea necesario.

Configurar las cadenas de conexión:
Actualiza appsettings.json y appsettings.Development.json en src/JempaTV.HttpApi.Host con los detalles de conexión de tu base de datos.

Configuración del Frontend

Navegar al proyecto Angular:

cd angular


Instalar dependencias:

yarn install


Ejecutar el servidor de desarrollo:

ng serve


La aplicación estará accesible en http://localhost:4200/.

Configuración de Docker

El proyecto incluye configuraciones Dockerfile tanto para el frontend en Angular como para los servicios backend en .NET.

Consulta los Dockerfile respectivos para las instrucciones de compilación y ejecución.

▶️ Uso

Desarrollo

Iniciar el servidor de desarrollo de Angular:

cd angular
ng serve


Navega a http://localhost:4200/.

Ejecutar los servicios backend:
Consulta src/JempaTV.HttpApi.Host/Dockerfile y src/JempaTV.DbMigrator/Dockerfile para ver las instrucciones.

Funcionalidades Principales

Página de Inicio:

Para los usuarios no autenticados, muestra contenido introductorio y una solicitud de inicio de sesión.

Para los usuarios autenticados, muestra las series destacadas con un carrusel y un carrusel con las 10 mejores series.

Series: Busca series por título, mira los detalles y añádelas a tu lista de seguimiento.

Lista de seguimiento (Watchlist): Ve tus series guardadas, califícalas, añade comentarios y elimínalas.

Gestión de API: Una sección exclusiva para administradores para ver las estadísticas de la API, errores y la actividad de los usuarios.

Notificaciones: Accede a tus notificaciones personales.

Configuración: Gestiona tu foto de perfil, preferencias de correo electrónico y el idioma de la aplicación.

📚 Tabla de Contenidos

Características

Tecnologías

Instalación

Uso

Estructura del Proyecto

Contribución

Licencia

Enlaces Importantes

Pie de página

🏗️ Estructura del Proyecto

El proyecto sigue una arquitectura en capas típica de las aplicaciones del ABP Framework:

angular/: Aplicación frontend construida con Angular.

src/JempaTV.Application/

src/JempaTV.Application.Contracts/

src/JempaTV.Domain/

src/JempaTV.Domain.Shared/

src/JempaTV.EntityFrameworkCore/

src/JempaTV.HttpApi/

src/JempaTV.HttpApi.Host/

src/JempaTV.DbMigrator/

test/: Pruebas unitarias y de integración.

🤝 Contribución

¡Las contribuciones son bienvenidas! Por favor, sigue estas pautas:

Haz un Fork del repositorio.

Crea una nueva rama para tu característica o corrección de errores.

Realiza tus cambios y asegúrate de que estén bien probados.

Envía un Pull Request con una descripción clara de tus cambios.

📜 Licencia

Este proyecto no tiene licencia especificada. (Basado en la información del repositorio)

🔗 Enlaces Importantes

Repositorio: https://github.com/PDR1004/JempaTV

ABP Framework: https://abp.io/

📝 Pie de página

© 2025 JempaTV

Este proyecto es mantenido por PDR1004.

Haz un Fork en GitHub

Generado por ReadmeCodeGen
