# WebHealth - Sistema de Gestión de Citas Médicas

## 📋 Descripción del Proyecto

WebHealth es un sistema web completo para la gestión de citas médicas desarrollado en PHP con arquitectura MVC (Modelo-Vista-Controlador). El sistema permite a los pacientes reservar citas médicas en línea y proporciona un panel de administración para gestionar todos los aspectos de una clínica médica.

## 🏗️ Arquitectura del Proyecto

El proyecto está estructurado en dos partes principales:

### 1. Frontend Público (`webhealth/`)
- **Página principal** para pacientes
- **Sistema de reserva de citas**
- **Información sobre especialidades médicas**
- **Perfiles de médicos**
- **Contacto y ubicación**

### 2. Backoffice de Administración (`webhealth/backoffice/`)
- **Panel de control** para administradores
- **Gestión de usuarios** (médicos, pacientes, personal)
- **Administración de citas**
- **Control de especialidades y salas**
- **Gestión de enfermedades y síntomas**

## 🛠️ Tecnologías Utilizadas

### Backend
- **PHP 7+** - Lenguaje principal del servidor
- **MySQL** - Base de datos relacional
- **PDO** - Para conexiones seguras a la base de datos
- **Arquitectura MVC** - Separación clara de responsabilidades

### Frontend
- **HTML5, CSS3, JavaScript** - Tecnologías web estándar
- **Bootstrap 4** - Framework CSS para diseño responsive
- **jQuery** - Biblioteca JavaScript para interactividad
- **Vendor Libraries**:
  - IcoFont, Boxicons, Remixicon (iconos)
  - Owl Carousel (carruseles)
  - Venobox (lightbox)
  - Bootstrap Datepicker (selector de fechas)

## 📁 Estructura de Directorios

```
webhealth/
├── backoffice/                # Panel de administración
│   ├── ajax/                  # Peticiones AJAX
│   ├── controllers/           # Controladores del backoffice
│   ├── extension/             # Extensiones y librerías externas
│   ├── models/                # Modelos del backoffice
│   ├── views/                 # Vistas del backoffice
│   ├── .htaccess              # Configuración Apache
│   └── index.php              # Punto de entrada del backoffice
├── controllers/               # Controladores del frontend
├── database/                  # Scripts de base de datos
├── models/                    # Modelos del frontend
├── views/                     # Vistas del frontend
│   ├── css/                   # Estilos CSS
│   ├── img/                   # Imágenes y recursos gráficos
│   ├── js/                    # JavaScript personalizado
│   ├── pages/                 # Páginas parciales
│   ├── vendor/                # Librerías de terceros
│   └── plantilla.php          # Plantilla principal
├── .htaccess                  # Configuración Apache
└── index.php                  # Punto de entrada principal
```

## 🗄️ Base de Datos

El sistema utiliza una base de datos MySQL llamada `proyectocitasmedicas` que incluye tablas para:

- **Usuarios** - Médicos, pacientes, administradores
- **Especialidades** - Áreas médicas disponibles
- **Salas** - Consultorios y áreas de atención
- **Citas** - Reservas de pacientes
- **Enfermedades base** - Catálogo de diagnósticos
- **Síntomas** - Registro de síntomas de pacientes
- **Personas** - Información personal de usuarios

## 🔧 Instalación y Configuración

### Requisitos Previos
- Servidor web (Apache, Nginx)
- PHP 7.0 o superior
- MySQL 5.6 o superior
- Extensión PDO para PHP

### Pasos de Instalación

1. **Clonar o copiar el proyecto** en el directorio web del servidor
2. **Crear la base de datos**:
   ```sql
   CREATE DATABASE proyectocitasmedicas;
   ```
3. **Importar la estructura** (si existen scripts SQL en `database/`)
4. **Configurar conexión a BD** en `models/conexionDB.php`:
   ```php
   $link = new PDO("mysql:host=localhost;dbname=proyectocitasmedicas", "usuario", "contraseña");
   ```
5. **Configurar permisos** de escritura en directorios necesarios
6. **Acceder al sistema**:
   - Frontend: `http://tudominio.com/webhealth/`
   - Backoffice: `http://tudominio.com/webhealth/backoffice/`

## 🚀 Características Principales

### Para Pacientes
- ✅ Registro y autenticación de pacientes
- ✅ Búsqueda de especialidades médicas
- ✅ Visualización de perfiles de médicos
- ✅ Reserva de citas en línea
- ✅ Historial de citas anteriores
- ✅ Información de contacto y ubicación

### Para Administradores
- ✅ Gestión completa de usuarios
- ✅ Administración de citas (crear, modificar, cancelar)
- ✅ Control de especialidades médicas
- ✅ Gestión de salas y consultorios
- ✅ Registro de enfermedades y síntomas
- ✅ Reportes y estadísticas

## 🔐 Seguridad

- **Conexiones PDO** para prevenir inyecciones SQL
- **Validación de formularios** tanto en cliente como servidor
- **Protección contra XSS** (Cross-Site Scripting)
- **Manejo de sesiones** seguras
- **Configuración .htaccess** para restricciones de acceso

## 📱 Diseño Responsive

El sistema está diseñado para funcionar en:
- ✅ Computadoras de escritorio
- ✅ Tablets
- ✅ Teléfonos móviles

## 🧪 Pruebas y Mantenimiento

### Pruebas Recomendadas
1. **Pruebas de funcionalidad** - Todas las características principales
2. **Pruebas de seguridad** - Validación de entradas y autenticación
3. **Pruebas de rendimiento** - Tiempos de carga y respuesta
4. **Pruebas de compatibilidad** - Diferentes navegadores y dispositivos

### Mantenimiento
- Actualizar regularmente las librerías de terceros
- Realizar copias de seguridad de la base de datos
- Monitorear logs de errores
- Actualizar credenciales de acceso periódicamente

## 🤝 Contribución

1. Fork del proyecto
2. Crear rama de características (`git checkout -b feature/NuevaCaracteristica`)
3. Commit de cambios (`git commit -am 'Agrega nueva característica'`)
4. Push a la rama (`git push origin feature/NuevaCaracteristica`)
5. Crear Pull Request

## 📄 Licencia

Este proyecto está bajo licencia propietaria. Todos los derechos reservados.

## 📞 Contacto y Soporte

Para soporte técnico o consultas sobre el proyecto, contactar: María García mailto:mariajhosegarcia@gmail.com

---

**Nota**: Este sistema está diseñado para uso en entornos médicos y debe cumplir con las regulaciones locales de protección de datos de salud (como HIPAA en EE.UU. o GDPR en Europa).
