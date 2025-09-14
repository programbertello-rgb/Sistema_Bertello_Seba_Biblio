📖 Sistema Bertello Seba Biblio

Sistema_Bertello_Seba_Biblio es un software de gestión bibliotecaria multiplataforma.
Incluye todas las funciones básicas para administrar libros, usuarios, préstamos y reservas, además de importación, exportación y notificaciones automáticas.

✨ Funcionalidades principales

📚 CRUD completo de libros, usuarios y préstamos/reservas

📥 Importación de lotes desde archivos CSV y MARC21

📤 Exportación a CSV

🏷️ Generación de etiquetas PDF con códigos de barras

📧 Notificaciones por correo electrónico (WhatsApp/Telegram con ganchos simulados listos para integrar)

⚙️ Panel de configuración de notificaciones

🔑 Control remoto de licencias y contribuciones (sincronización automática)

💻 Aplicación empaquetada con Electron → instaladores .exe (Windows) y .AppImage (Linux)

🛠️ Requisitos

Ninguno para el usuario final → el instalador incluye todo lo necesario.

Para desarrolladores:

Node.js 18+

npm

PostgreSQL

🚀 Instalación (usuarios)

Descargue el instalador desde la sección 👉 Releases
.

Windows: archivo .exe

Linux: archivo .AppImage

Ejecute el instalador.

Complete los datos iniciales de la institución en el primer inicio.

¡Listo! Puede comenzar a usar el sistema.

⚡ Instalación (desarrolladores)
# Clonar repositorio
git clone https://github.com/programbertello-rgb/Sistema_Bertello_Seba_Biblio.git
cd Sistema_Bertello_Seba_Biblio

# Instalar dependencias
npm install

# Configurar base de datos y notificaciones
nano config/settings.json

# Migraciones Prisma
npx prisma migrate deploy

# Iniciar backend
npm run start


Frontend:

cd src/ui
npm run start

🔔 Notificaciones

Correo SMTP → funcional real

WhatsApp / Telegram → simulados (ganchos listos para integrar APIs externas como Twilio o Telegram Bot API).

🔑 Licencias y control remoto

El sistema valida automáticamente la licencia en cada inicio.

Puede bloquear/desbloquear instalaciones editando el archivo licencia.json en el repositorio remoto.

Sincronización automática cada hora.

🧪 Pruebas automáticas
npm test


Backend: CRUD, importaciones, notificaciones.

Frontend: componentes y formularios principales.

📦 Flujo de publicación

Cada vez que se crea un nuevo Release, GitHub Actions:

Corre pruebas automáticas.

Compila el frontend con React.

Empaqueta backend + frontend con Electron.

Genera instaladores .exe y .AppImage.

Los adjunta al Release en la sección Assets.

📜 Licencia

Propietario: programbertello-rgb
Uso bajo condiciones de contribución y validación de licencia remota.
