# 🔧 Compilación Alternativa del Proyecto

## ⚠️ Maven No Disponible

Si no tienes Maven instalado en tu sistema, aquí tienes alternativas para compilar y ejecutar el proyecto.

## 🚀 Opción 1: Usar IDE (Recomendado)

### IntelliJ IDEA
1. Abrir el proyecto en IntelliJ IDEA
2. El IDE detectará automáticamente que es un proyecto Maven
3. Usar el botón "Import Maven Project" si es necesario
4. Compilar usando `Ctrl + F9` o `Build > Build Project`

### Eclipse
1. Importar como proyecto Maven existente
2. Usar `Project > Build Project`
3. Ejecutar en servidor Tomcat integrado

### NetBeans
1. Abrir como proyecto Maven
2. Compilar con `F11`
3. Ejecutar en servidor integrado

## 🐳 Opción 2: Usar Docker (Maven Wrapper)

Si tienes Docker instalado:

```bash
# Crear contenedor con Maven
docker run -it --rm -v "$(pwd):/app" -w /app maven:3.8-openjdk-11 mvn clean compile
```

## 📦 Opción 3: Descargar Maven Manualmente

### Windows
1. Descargar Maven desde: https://maven.apache.org/download.cgi
2. Extraer en `C:\Program Files\Apache\maven`
3. Agregar `C:\Program Files\Apache\maven\bin` al PATH
4. Reiniciar PowerShell/CMD

### Verificar Instalación
```bash
mvn --version
```

## 🎯 Opción 4: Usar Maven Wrapper

Si el proyecto incluye Maven Wrapper:

```bash
# Windows
.\mvnw.cmd clean compile

# Linux/Mac
./mvnw clean compile
```

## 🔍 Verificación de Compilación

### Archivos Generados
Después de compilar exitosamente, deberías ver:
```
target/
├── classes/
│   └── com/gusortiz/sitioweb/
│       ├── BiografiaServlet.class
│       └── TemasInteresServlet.class
├── maven-archiver/
└── sitio-personal-servlets-1.0-SNAPSHOT.war
```

### Verificar Compilación
```bash
# Verificar que las clases se generaron
dir target\classes\com\gusortiz\sitioweb

# Deberías ver:
# BiografiaServlet.class
# TemasInteresServlet.class
```

## 🚀 Ejecución del Proyecto

### Con Tomcat Integrado
1. Descargar Apache Tomcat 10+ (compatible con Jakarta EE 6.0)
2. Copiar el archivo WAR a `webapps/`
3. Iniciar Tomcat
4. Acceder a `http://localhost:8080/sitio-personal-servlets-1.0-SNAPSHOT/`

### Con IDE
- Usar el servidor integrado del IDE
- Configurar Tomcat 10+ como servidor de aplicaciones

## 📋 Verificación de Funcionalidad

### URLs a Probar
- **Página Principal**: `http://localhost:8080/sitio-personal-servlets-1.0-SNAPSHOT/`
- **Biografía**: `http://localhost:8080/sitio-personal-servlets-1.0-SNAPSHOT/biografia`
- **Temas de Interés**: `http://localhost:8080/sitio-personal-servlets-1.0-SNAPSTHOT/temas-interes`

### Funcionalidades a Verificar
1. ✅ Página principal se muestra correctamente
2. ✅ Enlaces de navegación funcionan
3. ✅ BiografiaServlet responde en `/biografia`
4. ✅ TemasInteresServlet responde en `/temas-interes`
5. ✅ Navegación bidireccional entre páginas

## 🐛 Solución de Problemas

### Error: "Maven no reconocido"
- Instalar Maven o usar IDE
- Verificar variables de entorno PATH

### Error: "Java no encontrado"
- Instalar Java 11 o superior
- Verificar JAVA_HOME

### Error: "Servlet no encontrado"
- Verificar que Tomcat sea versión 10+
- Confirmar que el WAR se desplegó correctamente

### Error: "Página no encontrada"
- Verificar rutas en anotaciones @WebServlet
- Confirmar que los servlets compilaron correctamente

## 📞 Soporte Adicional

Si continúas teniendo problemas:
1. Usar un IDE como IntelliJ IDEA (versión Community gratuita)
2. Verificar que Java 11+ esté instalado
3. Confirmar que Tomcat 10+ esté configurado
4. Revisar logs del servidor para errores específicos

---

**Nota**: El proyecto está diseñado para funcionar con cualquier servidor compatible con Jakarta EE 6.0, incluyendo Tomcat 10+, WildFly, y servidores integrados en IDEs modernos.
