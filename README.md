# EXAMEN PRÁCTICO – UNIDAD III

**Curso**: Desarrollo de Aplicaciones Móviles

**Fecha**: 18 de noviembre de 2025

**Estudiante**: Jaime Elias Flores Quispe

**Repositorio**: `https://github.com/jf2021070309/SM2_ExamenUnidad3`

**Entrega**: README.md convertido a PDF con evidencia y documentación

**Objetivo**: Implementar un flujo de trabajo (workflow) automatizado en GitHub Actions para realizar análisis de calidad sobre el proyecto móvil e integrar prácticas de DevOps.

**Actividades realizadas**

- **Crear repositorio**: Se creó el repositorio público con nombre exacto `SM2_ExamenUnidad3`.
- **Copiar proyecto**: Se copió todo el contenido del proyecto móvil al repositorio.
- **Crear carpetas**: Se añadieron las carpetas obligatorias: `/.github/workflows/` y `/test/`.
- **Crear archivos**: Se creó `quality-check.yml` en `/.github/workflows/` y `main_test.dart` en `/test/` con al menos 3 pruebas unitarias.

**Estructura relevante (evidencia)**

Captura de la estructura de carpetas mostrando ` .github/workflows/ `:

![alt text](image-1.png)

---

**Captura de `test/main_test.dart`**

Captura que muestre el archivo `test/main_test.dart` con las pruebas unitarias:

**Contenido de `main_test.dart`**

![alt text](image-5.png)

Mock de una servicio simulado:

![alt text](image-2.png)

ViewModel de una clase para login:

![alt text](image-3.png)

Funcion de las 3 pruebas unitarias:

![alt text](image-4.png)


**Contenido de `quality-check.yml`**

Captura de pantalla del contenido del archivo `quality-check.yml`:

![alt text](image.png)


**Ejecución del workflow (evidencia)**

Captura de la pestaña `Actions` mostrando la ejecución del workflow y el resultado `100% passed`:

![alt text](image-6.png)

**Explicación de lo realizado**

- **¿Qué hace el workflow?**: Al hacer `git push` a `main` o crear un `pull_request` hacia `main`, GitHub Actions ejecuta los pasos: instalar Flutter, obtener dependencias, ejecutar `flutter analyze` y ejecutar `flutter test`. Esto permite detectar errores estáticos y regressiones en pruebas.
- **`flutter analyze`**: Verifica estilo, convenciones y errores estáticos.
- **`flutter test`**: Ejecuta las pruebas unitarias definidas en `test/`.
