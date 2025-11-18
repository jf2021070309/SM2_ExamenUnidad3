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

<img width="303" height="369" alt="image" src="https://github.com/user-attachments/assets/90677803-239a-4be6-8c60-a05e5a3f22cf" />

---

**Captura de `test/main_test.dart`**

Captura que muestre el archivo `test/main_test.dart` con las pruebas unitarias:

**Contenido de `main_test.dart`**

<img width="241" height="119" alt="image" src="https://github.com/user-attachments/assets/4dfbafcb-9f8e-47b8-97b2-6887c4a491b1" />

Mock de una servicio simulado:

<img width="710" height="600" alt="image" src="https://github.com/user-attachments/assets/64e89219-dffb-4333-b179-c5a3e0543fd1" />

ViewModel de una clase para login:

<img width="692" height="557" alt="image" src="https://github.com/user-attachments/assets/848e8c2e-eb1c-4b6d-b54f-09632018fb40" />

Funcion de las 3 pruebas unitarias:

<img width="687" height="722" alt="image" src="https://github.com/user-attachments/assets/a78630e3-e12f-41de-b09f-095cc132ada3" />

**Contenido de `quality-check.yml`**

Captura de pantalla del contenido del archivo `quality-check.yml`:

<img width="664" height="858" alt="image" src="https://github.com/user-attachments/assets/491f83f3-64c3-4068-9f71-46b0f5755917" />

**Ejecución del workflow (evidencia)**

Captura de la pestaña `Actions` mostrando la ejecución del workflow y el resultado `100% passed`:

<img width="1167" height="699" alt="image" src="https://github.com/user-attachments/assets/2bea8c85-1405-477b-a9ea-d390b4b198d3" />

**Explicación de lo realizado**

- **¿Qué hace el workflow?**: Al hacer `git push` a `main` o crear un `pull_request` hacia `main`, GitHub Actions ejecuta los pasos: instalar Flutter, obtener dependencias, ejecutar `flutter analyze` y ejecutar `flutter test`. Esto permite detectar errores estáticos y regressiones en pruebas.
- **`flutter analyze`**: Verifica estilo, convenciones y errores estáticos.
- **`flutter test`**: Ejecuta las pruebas unitarias definidas en `test/`.
