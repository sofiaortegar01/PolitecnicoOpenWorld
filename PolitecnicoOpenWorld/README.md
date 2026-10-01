# Entrega Examen Parcial - Politécnico Open World (POW)

## 1. Datos de Identificación
- **Institución:** Instituto Politécnico Nacional - ESCOM
- **Unidad de Aprendizaje:** Desarrollo de Aplicaciones Móviles Nativas
- **Estudiante:** Sofía Ortega García
- **Boleta:** 2024630517
- **Grupo:** 7CV4
- **Usuario GitHub:** [@sofiaortegar01](https://github.com/sofiaortegar01)

---

## 2. Objetivo y Alcance
- **Objetivo:** Implementar un mecanismo de navegación de salida seguro y accesible dentro del modo de exploración libre ("Mundo Libre" / Free Roam) en `WorldMapScreen.kt`.
- **Alcance:**
  - Integración de un `IconButton` con icono `ArrowBack` en la capa superior de controles.
  - Implementación de un cuadro de diálogo modal de confirmación (`AlertDialog`) para confirmar el abandono de la partida o continuar explorando.
  - Soporte de accesibilidad para lectores de pantalla (TalkBack) mediante `contentDescription`.
  - Reutilización del callback existente `onNavigateToMainMenu` sin alterar la arquitectura MVVM ni romper la compilación del proyecto.

---

## 3. Enlaces y Trazabilidad Git
- **Pull Request Oficial (POW):** [PR #159 en gabrielhuav/PolitecnicoOpenWorld](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159)
- **Rama de trabajo:** `fix/free-roam-exit-navigation`
- **Rama de entrega académica:** `entrega-examen`
- **SHA Base:** `7ed325393f82872c2be94ff2ada46948efa19152`
- **SHA Final (Commit de la funcionalidad):** `ebe4a27ee36b270026ef7175b810f789632de4ea`

---

## 4. Matriz de Pruebas y Evidencias (QA)
- **Documento completo de pruebas:** [docs/pruebas.md](docs/pruebas.md)
- **Resumen de casos ejecutados:**
  - **TC01 (Ruta Feliz):** Presionar botón de salida, confirmar en diálogo y retornar al menú principal [Aprobado].
  - **TC02 (Condición Alterna):** Presionar "Seguir explorando" o descartar el diálogo modal manteniendo el estado de juego [Aprobado].
  - **TC03 (Regresión):** Funcionamiento estable de controles adyacentes (botón de Ajustes) [Aprobado].
  - **TC04 (Navegación / Estado):** Manejo del ciclo de vida y navegación hacia atrás [Aprobado].
  - **TC05 (Accesibilidad):** Lectura correcta de TalkBack en el botón de salida [Aprobado].
  - **TC06 (Compatibilidad):** Renderizado correcto en emulador Pixel 7 (API 37) en orientación horizontal [Aprobado].

### Evidencias Visuales del Recorrido:
1. **Estado anterior (Sin botón de salida):**
   ![Antes](docs/images/01_antes_sin_boton.png)

2. **Estado actual (Con botón de salida implementado):**
   ![Después](docs/images/02_despues_con_boton.png)

3. **Diálogo de confirmación:**
   ![Aviso](docs/images/03_aviso_dialogo.png)

4. **Retorno al menú principal:**
   ![Menú](docs/images/04_menu_principal.png)

---

## 5. Bitácora Individual y Revisión por Pares
- **Commits realizados:**
  - `feat(map): add exit navigation button with confirmation dialog`
  - `docs: add QA test matrix with 6 test cases`
  - `docs: add QA visual evidence sequence`
- **Revisión Técnica por Pares (Peer Review):**
  - Registrada en el hilo de conversación del [PR #159](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159).

---

## 6. Declaración de Herramientas de IA
- **Herramienta utilizada:** Gemini (Google)
- **Propósito:** Asistencia en la estructuración de la matriz de casos de prueba de QA bajo estándares de la rúbrica, redacción técnica en inglés de la plantilla del Pull Request, y organización del índice de entrega académica