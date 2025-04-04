# README - Laboratorio 8 - Inteligencia Artificial

## Introducción
Este repositorio contiene el desarrollo del Laboratorio 8 para el curso de Inteligencia Artificial (Semestre I-2024). En este laboratorio se abordan dos grandes tareas:

1. **Task 1 (Teoría)**  
   - Investigar y explicar el algoritmo AC-3 y su relación con el algoritmo de backtracking search.  
   - Definir el concepto de "Arc Consistency" con sus propias palabras.

2. **Task 2 (Implementaciones de algoritmos CSP)**  
   - Modelar un problema de programación de exámenes para cuatro estudiantes y siete cursos/exámenes, definiendo:
     1. Las variables (cursos).
     2. El dominio (días posibles: lunes, martes, miércoles).
     3. Las restricciones (máximo un examen por día para cada estudiante, cada examen en día distinto y sin traslapes para quienes lleven los mismos cursos).
   - Implementar y comparar tres algoritmos para resolver el mismo problema:
     1. **Backtracking search**  
     2. **Beam search**  
     3. **Local search**  

A lo largo del Notebook se describen los pasos para modelar el problema, se implementan las soluciones y se comparan los resultados y tiempos de cómputo de cada enfoque.

---

## Estructura de la Solución

1. **Task 1: Teoría**
   - **Pregunta 1:** Se investiga el algoritmo AC-3, describiendo en qué consiste y cómo se relaciona con la técnica de backtracking search.  
   - **Pregunta 2:** Se define en palabras propias el concepto de "Arc Consistency" (consistencia de arcos) y por qué resulta relevante en la resolución de problemas CSP.

2. **Task 2: CSP con Backtracking, Beam y Local Search**
   1. **Definición de variables y dominios**  
      - Cada examen se trata como una variable.  
      - El dominio para cada variable son los días de la semana disponibles: {Lunes, Martes, Miércoles}.
   2. **Definición de restricciones**  
      - **Restricción 1:** Todos los exámenes deben realizarse en días diferentes.  
      - **Restricción 2:** Cada estudiante no puede tener más de un examen por día.  
      - **Restricción 3:** Estudiantes que comparten un curso no pueden tener sus exámenes el mismo día.
   3. **Implementación de Backtracking search**  
      - Se explora el espacio de búsqueda asignando días a cada examen y comprobando las restricciones.  
      - Si se viola alguna restricción, se hace retroceso (backtracking) para reintentar una asignación distinta.
   4. **Implementación de Beam search**  
      - Se configura un ancho (beam width) y se generan varios “caminos” prometedores simultáneamente.  
      - En cada paso se selecciona un conjunto limitado de mejores estados/soluciones parciales según una heurística (por ejemplo, la menor cantidad de conflictos).
   5. **Implementación de Local search**  
      - Se inicia con una asignación posible (aunque sea con violaciones de restricciones).  
      - Se define una función de evaluación (por ejemplo, el número de restricciones violadas).  
      - Iterativamente se intercambian asignaciones de exámenes a días con la esperanza de disminuir la cantidad de conflictos hasta encontrar una solución válida.

3. **Comparación de Resultados y Conclusiones**
   - Cada algoritmo registra el **tiempo** que tarda en llegar a una solución.  
   - Se verifica la **calidad de la solución** (asignación final y si cumple las restricciones).  
   - En una celda de Markdown se presentan las **conclusiones** sobre:
     - El método más rápido.  
     - La facilidad de implementación.  
     - La solución obtenida (y si existen diferencias en la distribución de exámenes).  

---

## Cómo Ejecutar
1. Clonar este repositorio o descargar el Notebook.
2. Instalar las dependencias necesarias (si las hay) o simplemente abrir el Jupyter Notebook en un entorno donde se tengan instaladas las bibliotecas requeridas (por ejemplo, Python 3.x con librerías estándar).
3. Ejecutar las celdas secuencialmente:
   - Las primeras celdas contienen la parte teórica y las respuestas a las preguntas de **Task 1**.
   - Posteriormente, se definen las variables, dominios y restricciones para el **Task 2**.
   - Se ejecutan las celdas con la implementación de **Backtracking**, **Beam search** y **Local search**.
   - Finalmente, se muestra la comparación de los métodos y las conclusiones.

---
