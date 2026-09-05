# Microservicio de Pagos - Ingeniería DevOps

## 1. Modelo de Ramificación Elegido
Hemos seleccionado el modelo **GitFlow**. Esta decisión se justifica porque nuestro proyecto cuenta con ciclos de entrega muy claros y estructurados  (EP01, EP02, EP03). 

GitFlow nos permite trabajar de manera ordenada separando estrictamente el código en desarrollo activo (`develop`) del código de producción estable (`main`). De esta forma, evitamos subir código incompleto a la rama principal y garantizamos la trazabilidad total mediante ramas temporales de características (`feature/`) y reparaciones de emergencia (`hotfix/`).

## 2. Convención de Mensajes de Commit
Adoptamos el estándar de commits semánticos bajo la estructura: `tipo(alcance): descripcion`.
* **feat**: Nueva funcionalidad (Ej: `feat(ui): agregar pie de pagina`)
* **fix**: Solución de un error de software (Ej: `fix(home): corregir titulo`)
* **docs**: Modificaciones en documentación (Ej: `docs: agregar changelog`)
* **chore**: Labores de mantenimiento o archivos CI/CD (Ej: `chore(ci): agregar workflow`)

*Regla:* Todo el texto se escribe rigurosamente en minúsculas y omitiendo tildes para prevenir problemas de codificación.

## 3. Estructura de Ramas y Reglas de Naming
* **main**: Código productivo y completamente estable. No recibe código directo.
* **develop**: Rama integradora del proyecto escolar.
* **feature/<descripcion-corta>**: Ramas de desarrollo técnico individuales (Ej: `feature/pagina-presentacion`).
* **hotfix/<descripcion-corta>**: Corrección veloz ante fallas críticas detectadas en producción (Ej: `hotfix/titulo-pagina`).

## 4. Política de Fusión y Estrategia de Revisión
* Está prohibido hacer pushes directos sobre las ramas `main` y `develop`.
* Todo código nuevo entra exclusivamente mediante un Pull Request (PR).
* Se exige obligatoriamente la validación y aprobación de al menos 1 integrante antes de completar cualquier fusión.
* Tras concretar el proceso de unión, las ramas temporales utilizadas deben ser eliminadas de forma inmediata.
