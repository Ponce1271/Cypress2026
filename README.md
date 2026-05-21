# Cypress2026
Repo creado para guardar codigos cypress
## README — Cypress QA Automation (Technology with Purpose by Santex)

Descripción
- Repositorio para guardar ejercicios, ejemplos y notas de Cypress orientados a aprender lo relevante de QA Automation.
- Basado en el contenido y enfoque de "Technology with Purpose" por Santex.

Contenido del repositorio
- /cypress
  - /fixtures — datos de prueba (JSON, CSV, etc.)
  - /integration — specs/tests organizados por feature
  - /support — comandos personalizados y configuración global
  - /plugins — hooks y extensiones de Cypress
- /reports — resultados y artefactos de ejecución (allure, mochawesome, etc.)
- /docker — Dockerfiles y configuración para ejecutar tests en contenedores
- /scripts — scripts de utilidad (ejecutar, limpiar, generar reportes)
- README.md — este archivo
- package.json — dependencias y scripts de npm
- .github/workflows — CI/CD (GitHub Actions) para ejecución automática

Objetivos de aprendizaje
1. Configurar un proyecto de Cypress desde cero.
2. Escribir tests E2E, de integración y pruebas visuales básicas.
3. Manejar fixtures, datos dinámicos y stubbing/mocking de APIs.
4. Crear comandos personalizados y reutilizables.
5. Generar y publicar reportes (Mochawesome/Allure).
6. Integrar la ejecución en CI (GitHub Actions) y Docker.
7. Buenas prácticas de QA: flake handling, retries, paralelización, etiquetado de tests.

Requisitos
- Node.js >= 16
- npm o yarn
- Docker (opcional, para ejecución en contenedor)
- Cypress (se instala vía package.json)

Instalación rápida
1. Clonar el repo:
   git clone <REPO_URL>
2. Instalar dependencias:
   npm install
3. Abrir Cypress en modo interactivo:
   npx cypress open
4. Ejecutar tests en modo headless:
   npx cypress run

Estructura de ejemplo de tests
- integration/login.spec.js — tests del flujo de login (positivo/negativo)
- integration/dashboard.spec.js — validaciones de elementos y navegación
- integration/api-mock.spec.js — pruebas con intercept/fixture para APIs
- support/commands.js — ejemplo: cy.login(), cy.resetData()

Buenas prácticas y convenciones
- Nombres de archivos: feature.action.spec.js (e.g., checkout.success.spec.js)
- Tests pequeños y atómicos; un solo objetivo por spec.
- Usar fixtures para datos estáticos; usar factories para datos dinámicos.
- Evitar dependencias entre tests; limpiar estado en beforeEach/afterEach.
- Marcar tests lentos o inestables con tags (e.g., @flaky, @slow).
- Mantener selectores estables: preferir data-* (data-cy, data-test).

CI / GitHub Actions (ejemplo)
- workflow que instala dependencias, ejecuta tests headless y sube reportes.
- Uso opcional de Cypress Dashboard o ejecución en contenedor Docker.

Comandos npm recomendados (ejemplos en package.json)
- "test": "cypress run"
- "open": "cypress open"
- "report:generate": "node scripts/generate-report.js"
- "ci": "npm run test -- --record"

Cómo contribuir
1. Abrir un issue describiendo la mejora o bug.
2. Crear una branch con prefijo feature/ o fix/.
3. Enviar Pull Request con descripción y pasos para reproducir.
4. Mantener tests verdes en CI antes de mergear.

Recursos y referencias
- Documentación oficial de Cypress.
- Guías de testing E2E y patterns para automatización.
- Material de "Technology with Purpose" por Santex (apuntar a los módulos/temas usados).

Licencia
- MIT (o la que prefieras). Añade LICENSE si corresponde.

Plantilla de PR
- Resumen de cambios
- Issue relacionado
- Cómo probar localmente
- Capturas o enlaces a reportes (si aplica)

Notas finales
- Este repo está pensado como entorno de práctica y referencia para aprender QA Automation con enfoque práctico y reproducible.
- Ajusta scripts, configuraciones y versiones según tus necesidades y las versiones de Cypress/Node.

¿Querés que te genere:
1) un package.json inicial con scripts comunes,
2) un ejemplo de spec (login), o
3) el workflow de GitHub Actions para CI?
