# 🤖 Proyecto Integrador: Agente de IA para Orientación Académica

**Institución:** Instituto Superior de Formación Técnica Nº 151 (ISFT Nº 151)  
**Carrera:** Tecnicatura Superior en Análisis de Sistemas  
**Espacio Curricular:** Sistemas y Organizaciones - Ciclo Lectivo 2026 - Segundo Cuatrimestre  
**Alumno:** David Hernan Bravo  
**Bibliografía Base:** Lorenzón, E. E. (2020). *Sistemas y Organizaciones*. EDULP.  
**Última actualización:** Clase 2 de Octubre (Secuencia, reglas y control sobre el caso integrador)  

---

## 📌 Síntesis del Proyecto (Problema Elegido)

En el ámbito del ISFT Nº 151, los estudiantes de la Tecnicatura Superior en Análisis de Sistemas enfrentan demoras e incertidumbre al consultar condiciones de inscripción, régimen de correlatividades, cargas horarias, pautas de acreditación y procedimientos administrativos, debido a que la información normativa se encuentra dispersa en múltiples documentos (Diseño Curricular `IF-2019-36021554-GDEBA-CPEYTDGCYE`, Régimen Académico Marco, calendario académico y comunicados internos) que incluso presentan inconsistencias terminológicas y numéricas entre sí. Este proyecto modela, diseña, prototipa y evalúa sistémicamente un **Agente de Inteligencia Artificial de Orientación Académica** que opera sobre un corpus documental autorizado, garantizando trazabilidad normativa, control de errores y derivación humana ante situaciones fuera de alcance.

---

## 🗂️ Estructura General del Proyecto (Recorrido Sugerido por la Cátedra)

Para mantener la trazabilidad exigida por la cátedra y a la vez conservar una arquitectura modular de documentación, cada eje del proyecto se encuentra vinculado directamente a las entregas correspondientes dentro de los directorios `/docs` y `/prototipo`:

1. **[00-presentacion](./README.md):** Datos académicos, encuadre del repositorio y registro de actualizaciones.

2. **[01-problema](./docs/clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema):** Situación problemática inicial ([Clase 12](./docs/clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema)), revisión de evidencia vs. hipótesis ([Clase 13](./docs/clase_13.md#1-revisión-y-evolución-del-modelo-de-la-clase-12)) y ficha consolidada del problema ([Clase 25/09](./docs/clase_25_09.md#1-ficha-consolidada-del-proyecto-y-delimitación-del-problema)).

3. **[02-modelo-sistemico](./docs/clase_13.md#2-estructura-y-organización-del-sistema-capítulo-10):** Frontera, área gris, sinergia y recursividad ([Clase 12](./docs/clase_12.md#2-delimitación-y-modelo-sistémico-02-modelo-sistemico)); estructura funcional y organización ([Clase 13](./docs/clase_13.md#2-estructura-y-organización-del-sistema-capítulo-10)); variantes de contexto y decisiones de frontera ([Clase 25/09](./docs/clase_25_09.md#2-la-vista-de-los-intercambios-diagrama-de-contexto-y-variantes)).

4. **[03-flujos-y-control](./docs/clase_02_10.md):** Flujos de caja negra ([Clase 12](./docs/clase_12.md#3-representación-de-flujos-apertura-y-control-03-flujos-y-control)); ciclo básico de control ([Clase 13](./docs/clase_13.md#3-el-control-en-el-sistema-y-ciclo-básico-capítulo-11)); Casos de Uso UML con `«include»`/`«extend»` ([Clase 25/09](./docs/clase_25_09.md#3-la-vista-de-los-objetivos-casos-de-uso-uml-y-especificación-completa)); y recorridos en Diagrama de Secuencia, reglas de negocio y pruebas de control ([Clase 02/10](./docs/clase_02_10.md)).

5. **[04-investigacion](./docs/clase_13.md#7-fundamentación-teórica-por-capítulo-secuencia-concepto--decisión--consecuencia):** Fundamentación teórica con Emilio Lorenzón (Parte I: Caps. 7 a 13; Parte II: Caps. 5 y 8) y resolución de situaciones de autoevaluación ([Clase 25/09](./docs/clase_25_09.md#5-resolución-de-situaciones-de-autoevaluación-y-desafío-final-de-fronteras)).

6. **[05-prototipo-y-pruebas](./docs/clase_02_10.md#4-registro-de-las-tres-pruebas-comparación-y-corrección):** Prototipo inicial en Gemini Gems ([Taller de Integración](./docs/taller_integracion.md)), pruebas del caso integrador real con detección y corrección de contradicciones ([Clase 02/10](./docs/clase_02_10.md#4-registro-de-las-tres-pruebas-comparación-y-corrección)) e [Instrucciones actualizadas del Gem](./prototipo/instrucciones_gem.md).

---

## 📚 Bitácora de Entregas por Clase (`/docs`)

| Encuentro | Tema Central | Estado | Documento de Entrega | Diagramas / Artefactos Asociados |
| :--- | :--- | :---: | :--- | :--- |
| **Clase 12** | *Del sistema al agente de IA: Contexto, frontera, sinergia, recursividad y apertura* | ✅ Completado | [📄 Ver Entrega Clase 12](./docs/clase_12.md) | • [📐 Flujos y Caja Negra](./diagramas/clase_12_flujos_caja_negra.svg) |
| **Clase 13** | *El agente de IA como sistema: Estructura, control, contexto y casos de uso UML* | ✅ Completado | [📄 Ver Entrega Clase 13](./docs/clase_13.md) | • [📐 Ciclo de Control](./diagramas/clase_13_ciclo_control.svg)<br>• [📐 Contexto Inicial](./diagramas/clase_13_diagrama_contexto.svg)<br>• [📐 Casos de Uso Inicial](./diagramas/clase_13_casos_de_uso.svg) |
| **Taller 12-13** | *Del modelo al prototipo: Gemini Gems y pruebas de orientación académica* | ✅ Completado | [📄 Ver Taller de Integración](./docs/taller_integracion.md) | • [⚙️ Instrucciones del Gem](./prototipo/instrucciones_gem.md) |
| **Clase 25/09** | *Del agente de IA a sus diagramas: Contexto y Casos de Uso UML paso a paso* | ✅ Completado | [📄 Ver Entrega Clase 25/09](./docs/clase_25_09.md) | • [📐 Contexto Ampliado](./diagramas/clase_25_09_contexto.svg)<br>• [📐 Casos de Uso UML 2.5.1](./diagramas/clase_25_09_casos_de_uso.svg) |
| **Clase 02/10** | *Secuencia, reglas y control: Dos recorridos, tres reglas y tres pruebas* | ✅ Completado | [📄 Ver Entrega Clase 02/10](./docs/clase_02_10.md) | • [📐 Diagrama de Secuencia](./diagramas/clase_02_10_secuencia.svg)<br>• [⚙️ Instrucciones Gem v2.1](./prototipo/instrucciones_gem.md) |
| **Clase 09/10** | *Integración y preparación del trabajo final: Auditoría de coherencia y mejora* | ⏳ Pendiente | *Próximamente* | — |
|  |  |  |  |  |

---

## 🛠️ Estructura de Directorios del Repositorio

```text
🤖 AGENTE_IA/
├── 📖 README.md                                        # Portada, índice maestro y bitácora de seguimiento
├── 📁 docs/
│   ├── 📄 clase_12.md                                  # Desarrollo completo y fundamentación de la Clase 12
│   ├── 📄 clase_13.md                                  # Desarrollo completo y fundamentación de la Clase 13
│   ├── 📄 taller_integracion.md                        # Prototipado en Gemini Gems, pruebas y ciclo de control
│   ├── 📄 clase_25_09.md                               # Contexto, Casos de Uso UML (include/extend), proceso y contraste
│   └── 📄 clase_02_10.md                               # Diagrama de secuencia, reglas de negocio y pruebas del caso real
├── 📁 diagramas/
│   ├── 🖼️ clase_12_flujos_caja_negra.svg               # Modelo de sistema abierto y caja negra (Clase 12)
│   ├── 🖼️ clase_13_ciclo_control.svg                   # Ciclo básico de control y adaptador (Clase 13 - Cap. 11)
│   ├── 🖼️ clase_13_diagrama_contexto.svg               # Diagrama de contexto preliminar (Clase 13 - Cap. 10/12)
│   ├── 🖼️ clase_13_casos_de_uso.svg                    # Diagrama de casos de uso UML preliminar (Clase 13 - Cap. 12)
│   ├── 🖼️ clase_25_09_contexto.svg                     # Diagrama de contexto completo con Servicio Externo de IA
│   ├── 🖼️ clase_25_09_casos_de_uso.svg                 # Diagrama de casos de uso UML 2.5.1 con include y extend
│   └── 🖼️ clase_02_10_secuencia.svg                    # Diagrama de secuencia con recorridos normal y alternativos
└── 📁 prototipo/
    └── 📄 instrucciones_gem.md                         # Prompts de sistema (versión base, ajustada y caso real v2.1)
```