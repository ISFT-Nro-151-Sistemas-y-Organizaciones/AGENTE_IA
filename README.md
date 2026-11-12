# 🤖 Proyecto Integrador: Agente de IA para Orientación Académica

**Institución:** Instituto Superior de Formación Técnica Nº 151 (ISFT Nº 151)  
**Carrera:** Tecnicatura Superior en Análisis de Sistemas  
**Espacio Curricular:** Sistemas y Organizaciones - Ciclo Lectivo 2026 - Segundo Cuatrimestre  
**Alumno:** David Hernan Bravo  
**Bibliografía Base:** Lorenzón, E. E. (2020). *Sistemas y Organizaciones*. EDULP.  
**Última actualización:**Última actualización:** Clase 13 (Estructura, Control, Contexto y Primera Vista UML)  

---

## 📌 Síntesis del Proyecto (Problema Elegido)

En el ámbito del ISFT Nº 151, los estudiantes de la Tecnicatura Superior en Análisis de Sistemas enfrentan demoras e incertidumbre al consultar condiciones de inscripción, régimen de correlatividades, cargas horarias, pautas de acreditación y procedimientos administrativos, debido a que la información normativa se encuentra dispersa en múltiples documentos (Diseño Curricular `IF-2019-36021554-GDEBA-CPEYTDGCYE`, Régimen Académico Marco, calendario académico y comunicados internos) que incluso presentan inconsistencias terminológicas entre sí. Este proyecto modela, diseña y evalúa sistémicamente un **Agente de Inteligencia Artificial de Orientación Académica** que opera sobre un corpus documental autorizado, garantizando trazabilidad normativa, control de errores y derivación humana ante situaciones fuera de alcance.

---

## 🗂️ Estructura General del Proyecto (Recorrido Sugerido por la Cátedra)

Para mantener la trazabilidad exigida por la cátedra y a la vez conservar una arquitectura modular de documentación, cada eje del proyecto se encuentra vinculado directamente a las entregas correspondientes dentro del directorio `/docs`:

1. **[00-presentacion](./README.md):** Datos académicos, encuadre del repositorio y registro de actualizaciones.

2. **[01-problema](./docs/clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema):** Situación problemática inicial ([Clase 12](./docs/clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema)) y revisión de evidencia vs. hipótesis ([Clase 13](./docs/clase_13.md#1-revisión-y-evolución-del-modelo-de-la-clase-12)).

3. **[02-modelo-sistemico](./docs/clase_13.md#2-estructura-y-organización-del-sistema-capítulo-10):** Frontera, área gris, sinergia y recursividad ([Clase 12](./docs/clase_12.md#2-delimitación-y-modelo-sistémico-02-modelo-sistemico)); estructura funcional, organización, acoplamientos, conexiones y diagrama de contexto ([Clase 13](./docs/clase_13.md#4-modelo-de-contexto-y-diccionario-de-flujos)).

4. **[03-flujos-y-control](./docs/clase_13.md#3-el-control-en-el-sistema-y-ciclo-básico-capítulo-11):** Flujos de caja negra ([Clase 12](./docs/clase_12.md#3-representación-de-flujos-apertura-y-control-03-flujos-y-control)); ciclo básico de control (adaptador), tiempos de respuesta (retraso y rezago), primera vista de Casos de Uso UML y validación por escenarios ([Clase 13](./docs/clase_13.md#5-primer-acercamiento-a-uml-vista-de-casos-de-uso-capítulo-12)).

5. **[04-investigacion](./docs/clase_13.md#7-fundamentación-teórica-por-capítulo-secuencia-concepto--decisión--consecuencia):** Fundamentación teórica con Emilio Lorenzón (Capítulos 7 al 12), preguntas abiertas de investigación y análisis de recursos audiovisuales.

6. **[05-prototipo-y-pruebas](./prototipo/):** *(Se incorporará en las etapas correspondientes al Taller de Integración y pruebas con Gemini Gems).*

---

## 📚 Bitácora de Entregas por Clase (`/docs`)

| Encuentro | Tema Central | Estado | Documento de Entrega | Diagramas Asociados (`.svg`) |
| :--- | :--- | :---: | :--- | :--- |
| **Clase 12** | *Del sistema al agente de IA: Contexto, frontera, sinergia, recursividad y apertura* | ✅ Completado | [📄 Ver Entrega Clase 12](./docs/clase_12.md) | • [📐 Flujos y Caja Negra](./diagramas/clase_12_flujos_caja_negra.svg) |
| **Clase 13** | *El agente de IA como sistema: Estructura, control, contexto y casos de uso UML* | ✅ Completado | [📄 Ver Entrega Clase 13](./docs/clase_13.md) | • [📐 Ciclo de Control](./diagramas/clase_13_ciclo_control.svg)<br>• [📐 Diagrama de Contexto](./diagramas/clase_13_diagrama_contexto.svg)<br>• [📐 Casos de Uso UML](./diagramas/clase_13_casos_de_uso.svg) |
| **Taller 12-13** | *Del modelo al prototipo: Gemini Gems y pruebas de orientación académica* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 25/09** | *Del agente de IA a sus diagramas: Contexto y Casos de Uso en profundidad* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 02/10** | *Secuencia, reglas y control: Recorridos, reglas de negocio y casos de prueba* | ⏳ Pendiente | *Próximamente* | — |
| **Clase 09/10** | *Integración y preparación del trabajo final: Auditoría de coherencia y mejora* | ⏳ Pendiente | *Próximamente* | — |


---

## 🛠️ Estructura de Directorios del Repositorio

```text
🤖 AGENTE_IA/
├── 📖 README.md                                        # Portada, índice maestro y bitácora de seguimiento
├── 📁 docs/
│   ├── 📄 clase_12.md                                  # Desarrollo completo y fundamentación de la Clase 12
│   └── 📄 clase_13.md                                  # Desarrollo completo y fundamentación de la Clase 13
├── 📁 diagramas/
│   ├── 🖼️ clase_12_flujos_caja_negra.svg               # Modelo de sistema abierto y caja negra (Clase 12)
│   ├── 🖼️ clase_13_ciclo_control.svg                   # Ciclo básico de control y adaptador (Clase 13 - Cap. 11)
│   ├── 🖼️ clase_13_diagrama_contexto.svg               # Diagrama de contexto del servicio (Clase 13 - Cap. 10/12)
│   └── 🖼️ clase_13_casos_de_uso.svg                    # Diagrama de casos de uso UML inicial (Clase 13 - Cap. 12)
└── 📁 prototipo/
    └── 📌 .gitkeep                                     # Espacio reservado para prompts, corpus y pruebas
```