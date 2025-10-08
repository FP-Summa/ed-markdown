
# Mini-guía de instalación: JDK 21 + Gradle 8.7
Instalaremos __OpenJDK 21__ y __Gradle 8.7__.

Luego validaremos que el sistema reconoce ambas herramientas.

---
## Pasos
1. Instala __OpenJDK 21__ (Windows 11).

2. Configura __JAVA_HOME__ y añade `%JAVA_HOME%\bin` al `PATH`.

3. Instala __Gradle 8.7__ (instalador o `winget`).

4. Crea o abre un proyecto mínimo para validar la build.
>Gradle usa el __JDK__ que tengas configurado en `JAVA_HOME`.

## Comprobación
Comandos en línea: `java -version`, `gradle -v`

```
java -version
gradle -v
```
__Resultado esperado:__ versiones mostradas y compilación mínima __correcta__.


