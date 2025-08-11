# 🚀 Sitio Personal con Servlets - Gustavo Ortiz

Un sitio web personal completo desarrollado con **Jakarta EE** y **Servlets**, que demuestra habilidades en desarrollo web backend y frontend.

## 📋 Descripción del Proyecto

Este proyecto implementa un sitio web personal compuesto por tres páginas principales, conectadas mediante navegación interna y generadas parcialmente por servlets de Jakarta EE.

### 🎯 Características Principales

- **Página Principal (index.html)**: Saludo de bienvenida y navegación al sitio
- **Página de Biografía (BiografiaServlet)**: Información personal del estudiante
- **Página de Temas de Interés (TemasInteresServlet)**: Contenido sobre tecnología y desarrollo

## 🏗️ Estructura del Proyecto

```
SitioPersonalServlets/
├── src/
│   └── main/
│       ├── java/
│       │   └── com.gusortiz.sitioweb/
│       │       ├── BiografiaServlet.java
│       │       └── TemasInteresServlet.java
│       └── webapp/
│           ├── index.html
│           ├── img/
│           │   └── README.md
│           └── WEB-INF/
│               └── web.xml
├── pom.xml
└── README.md
```

## 🛠️ Tecnologías Utilizadas

- **Backend**: Jakarta EE 6.0, Servlets
- **Frontend**: HTML5, CSS3, JavaScript
- **Build Tool**: Maven 3.x
- **Java Version**: 11+
- **Servidor**: Cualquier servidor compatible con Jakarta EE (Tomcat 10+, WildFly, etc.)

## 🚀 Instalación y Ejecución

### Prerrequisitos

- Java 11 o superior
- Maven 3.6+
- Servidor de aplicaciones compatible con Jakarta EE

### Pasos de Instalación

1. **Clonar el repositorio**
   ```bash
   git clone <url-del-repositorio>
   cd SitioPersonalServlets
   ```

2. **Compilar el proyecto**
   ```bash
   mvn clean compile
   ```

3. **Empaquetar como WAR**
   ```bash
   mvn package
   ```

4. **Desplegar en el servidor**
   - Copiar el archivo `target/sitio-personal-servlets-1.0-SNAPSHOT.war` al directorio `webapps` de tu servidor
   - Reiniciar el servidor

### Ejecución Local con Maven

```bash
mvn tomcat7:run
```

El sitio estará disponible en: `http://localhost:8080/sitio-personal-servlets-1.0-SNAPSHOT/`

## 📱 Características del Sitio

### 🎨 Diseño y UX
- **Diseño Responsive**: Se adapta a todos los dispositivos
- **Interfaz Moderna**: Gradientes, sombras y efectos visuales atractivos
- **Navegación Intuitiva**: Enlaces claros entre todas las páginas
- **Animaciones CSS**: Transiciones suaves y efectos hover

### 🔧 Funcionalidades Técnicas
- **Servlets Jakarta EE**: Generación dinámica de contenido
- **Manejo de Sesiones**: Configuración de timeout y seguridad
- **Codificación UTF-8**: Soporte completo para caracteres especiales
- **Manejo de Errores**: Páginas de error personalizadas

## 📸 Imágenes Requeridas

Para que el sitio funcione correctamente, debes agregar las siguientes imágenes en `src/main/webapp/img/`:

1. **mi-foto.jpg** - Tu fotografía personal
2. **ai-ml.jpg** - Imagen de Inteligencia Artificial
3. **mobile-dev.jpg** - Imagen de desarrollo móvil

Ver `src/main/webapp/img/README.md` para más detalles.

## 🔍 Navegación del Sitio

### Flujo de Navegación
```
index.html → BiografiaServlet → TemasInteresServlet
     ↑           ↑                    ↑
     └───────────┴────────────────────┘
           Navegación bidireccional
```

### URLs de Acceso
- **Página Principal**: `/` o `/index.html`
- **Biografía**: `/biografia`
- **Temas de Interés**: `/temas-interes`

## 📚 Aprendizajes y Habilidades Demostradas

### Backend Development
- Implementación de Servlets Jakarta EE
- Manejo de requests HTTP GET
- Generación dinámica de contenido HTML
- Configuración de aplicaciones web

### Frontend Development
- HTML5 semántico y accesible
- CSS3 avanzado con Flexbox y Grid
- Diseño responsive y mobile-first
- Efectos visuales y animaciones CSS

### DevOps y Deployment
- Configuración Maven para proyectos web
- Empaquetado WAR para servidores Java
- Configuración de web.xml
- Manejo de dependencias y build

## 🐛 Solución de Problemas

### Errores Comunes

1. **Error 404 en servlets**
   - Verificar que el servidor soporte Jakarta EE 6.0
   - Confirmar que las anotaciones @WebServlet estén correctas

2. **Problemas de compilación**
   - Verificar versión de Java (debe ser 11+)
   - Ejecutar `mvn clean` antes de compilar

3. **Imágenes no se muestran**
   - Verificar que las imágenes estén en `src/main/webapp/img/`
   - Confirmar nombres de archivo exactos

## 📝 Personalización

### Cambiar Información Personal
- Editar `BiografiaServlet.java` para modificar datos personales
- Actualizar `index.html` para cambiar el saludo de bienvenida
- Modificar `TemasInteresServlet.java` para cambiar temas de interés

### Personalizar Estilos
- Los estilos CSS están integrados en cada archivo
- Modificar colores, fuentes y efectos en las secciones `<style>`

## 📄 Licencia

Este proyecto es para uso educativo y personal. Puedes modificarlo y adaptarlo según tus necesidades.

## 👨‍💻 Autor

**Gustavo Ortiz** - Estudiante de Ingeniería de Sistemas

## 🙏 Agradecimientos

- Jakarta EE Community
- Maven Community
- Profesores y compañeros de clase

---

**Nota**: Este proyecto cumple con todos los requisitos especificados para la asignación de Sitio Personal con Servlets, incluyendo la implementación de dos servlets, navegación entre páginas, y contenido informativo personal.
