# 🤖 Proyecto Integrador: Agente de IA para Orientación Académica

**Institución:** Instituto Superior de Formación Técnica Nº 151 (ISFT Nº 151)  
**Carrera:** Tecnicatura Superior en Análisis de Sistemas  
**Espacio Curricular:** Sistemas y Organizaciones - Ciclo Lectivo 2026 - Segundo Cuatrimestre  
**Alumno:** David Hernan Bravo  
**Bibliografía Base:** Lorenzón, E. E. (2020). *Sistemas y Organizaciones*. EDULP.  
**Última actualización:** Clase 12 (Lanzamiento y Modelo Sistémico Inicial)  

---

## 📌 Síntesis del Proyecto (Problema Elegido)

En el ámbito del ISFT Nº 151, los estudiantes de la Tecnicatura Superior en Análisis de Sistemas enfrentan demoras e incertidumbre al consultar condiciones de inscripción, régimen de correlatividades, cargas horarias, pautas de acreditación y procedimientos administrativos, debido a que la información normativa se encuentra dispersa en múltiples documentos (Diseño Curricular IF-2019-36021554-GDEBA-CPEYTDGCYE, Régimen Académico Marco, calendario académico y comunicados internos) que incluso presentan inconsistencias terminológicas entre sí. Este proyecto modela, diseña y evalúa sistémicamente un **Agente de Inteligencia Artificial de Orientación Académica** que opera sobre un corpus documental autorizado, garantizando trazabilidad normativa, control de errores y derivación humana ante situaciones fuera de alcance.

---

## 🗂️ Estructura General del Proyecto (Recorrido Sugerido por la Cátedra)

Para mantener la trazabilidad exigida por la cátedra y a la vez conservar una arquitectura modular de documentación, cada eje del proyecto se encuentra vinculado directamente a la entrega correspondiente dentro del directorio `/docs`:

1. **[00-presentacion](./README.md):** Datos académicos, encuadre del repositorio y registro de actualizaciones.

2. **[01-problema](./docs/clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema):** Situación problemática, actores involucrados, causas, efectos, evidencia y definición del objetivo verificable.

3. **[02-modelo-sistemico](./docs/clase_12.md#2-delimitación-y-modelo-sistémico-02-modelo-sistemico):** Frontera del sistema, dominio de cambios, variables endógenas/exógenas, área gris, contexto de interés, sinergia y niveles de recursividad.

4. **[03-flujos-y-control](./docs/clase_12.md#3-representación-de-flujos-apertura-y-control-03-flujos-y-control):** Modelo de sistema abierto, corrientes de entrada, conversión (FCP y FCS), salidas positivas/negativas, retroalimentación, perturbaciones y criterios de derivación humana.

5. **[04-investigacion](./docs/clase_12.md#5-relevamiento-e-investigación-cinco-preguntas-indispensables-04-investigacion):** Fundamentación teórica con la obra de Emilio Lorenzón (Capítulos 7, 8 y 9), preguntas abiertas de investigación y evaluación de fuentes técnicas.

6. **[05-prototipo-y-pruebas](./prototipo/):** *(Se incorporará en las etapas correspondientes al Taller de Integración y pruebas con Gemini Gems).*

---

## 📚 Bitácora de Entregas por Clase (`/docs`)

| Encuentro | Tema Central | Estado | Documento de Entrega | Diagramas Asociados |
| :--- | :--- | :---: | :--- | :--- |
| **Clase 12** | *Del sistema al agente de IA: Contexto, frontera, sinergia, recursividad y apertura* | ✅ Completado | [📄 Ver Entrega Clase 12](./docs/clase_12.md) | [📐 Flujos y Caja Negra (SVG)](./diagramas/clase_12_flujos_caja_negra.svg) |
| **Clase 13** | *El agente de IA como sistema: Estructura, control, contexto y casos de uso UML* | ⏳ Pendiente | *Próximamente* | — |
| **Taller 12-13** | *Del modelo al prototipo: Gemini Gems y pruebas de orientación académica* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 14** | *Del agente de IA a sus diagramas: Contexto y Casos de Uso en profundidad* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 15** | *Secuencia, reglas y control: Recorridos, reglas de negocio y casos de prueba* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 16** | *Integración y preparación del trabajo final: Auditoría de coherencia y mejora* | ⏳ Pendiente | *Próximamente* | — |

---

## 🛠️ Estructura de Directorios del Repositorio

```text
🤖 AGENTE_IA/
├── 📖 README.md                                        # Portada, índice maestro y bitácora de seguimiento
├── 📁 docs/
│   └── 📄 clase_12.md                                  # Desarrollo completo y fundamentación de la Clase 12
├── 📁 diagramas/
│   └── 🖼️ clase_12_flujos_caja_negra.svg               # Diagrama vectorial del modelo de sistema abierto y caja negra
└── 📁 prototipo/
    └── 📌 .gitkeep                                     # Espacio reservado para prompts, corpus y pruebas
```