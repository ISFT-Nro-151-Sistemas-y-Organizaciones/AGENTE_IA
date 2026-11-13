# 9 de Octubre · Integración y Preparación para el Trabajo Final

**Materia:** Sistemas y Organizaciones  
**Carrera:** Tecnicatura Superior en Análisis de Sistemas (ISFT Nº 151)  
**Alumno:** David Hernan Bravo  
**Prototipo Evaluado:** `Orientador TSAS - ISFT 151 (Prototipo Acotado)` en Google Gemini Gems (modelo Gemini Flash, versiones `v2.0` y `v2.1`)  
**Bibliografía Oficial Aplicada:** Lorenzón, E. E. (2020). *Sistemas y Organizaciones*. EDULP (Parte I: Capítulos 7 a 13; Parte II: Capítulos 5 y 8).

---

## 1. Integración de lo Trabajado (En Tres Pasos)

### 1.1. Paso 1: Reunión de Avances y Mapa de Trazabilidad del Repositorio

A lo largo del segundo cuatrimestre se construyó de manera incremental el análisis sistémico, el modelado formal y el prototipo funcional acotado del **Agente de Orientación Académica TSAS**. A continuación se reúnen todos los componentes producidos con sus enlaces directos dentro del repositorio:

| Componente Exigido | Síntesis de lo Construido en el Proyecto | Enlace al Artefacto en el Repositorio |
| :--- | :--- | :--- |
| **1. Problema que atiende el agente** | Dispersión normativa e inconsistencias internas en la documentación oficial de la carrera (`IF-2019-36021554-GDEBA-CPEYTDGCYE`, RAM y calendario), que provocan incertidumbre en los alumnos al verificar correlatividades y sobrecarga de consultas operativas en Preceptoría/Secretaría. | • [Planteo inicial (Clase 12)](./clase_12.md#1-situación-problemática-y-formulación-del-problema-01-problema)<br>• [Hechos vs. Hipótesis (Clase 13)](./clase_13.md#1-revisión-y-evolución-del-modelo-de-la-clase-12)<br>• [Ficha consolidada (Clase 25/09)](./clase_25_09.md#1-ficha-consolidada-del-proyecto-y-delimitación-del-problema) |
| **2. Usuarios y Actores** | **Actores principales (Personas):** `Estudiante` (1.º, 2.º y 3.º año de TSAS) y `Secretaría Académica / Docente Orientador`.<br>**Actores de apoyo (Sistemas externos en modelo objetivo):** `Servicio Externo de IA`, `Repositorio Normativo / Campus` y `Sistema de Gestión Académica Oficial`. | • [Definición de Actores y Roles (Clase 25/09)](./clase_25_09.md#31-identificación-de-objetivos-por-actor-separando-objetivo-dato-y-paso-técnico) |
| **3. Diagrama de Contexto** | Delimita la frontera de la aplicación del agente como unidad central y especifica los 10 flujos de información (`1` a `10`) con las cinco entidades externas, diferenciando qué flujos están implementados en el prototipo, cuáles simulados y cuáles propuestos. | • [Explicación y Tabla de Intercambios](./clase_25_09.md#2-la-vista-de-los-intercambios-diagrama-de-contexto-y-variantes)<br>• [📐 Ver Diagrama de Contexto (SVG)](../diagramas/clase_25_09_contexto.svg) |
| **4. Casos de Uso UML** | Representa bajo UML 2.5.1 los objetivos `CU-01 Obtener orientación`, `CU-02 Solicitar revisión humana` (`«extend»` de `CU-01`), `CU-03 Configurar criterios y fuentes`, `CU-04 Revisar consultas, alertas y pedidos` y `CU-05 Registrar interacción` (`«include»` de `CU-01`), junto con la especificación detallada de `CU-01` y sus excepciones (`2a` a `7a`). | • [Vista de Objetivos y Especificación `CU-01`](./clase_25_09.md#3-la-vista-de-los-objetivos-casos-de-uso-uml-y-especificación-completa)<br>• [📐 Ver Casos de Uso UML (SVG)](../diagramas/clase_25_09_casos_de_uso.svg) |
| **5. Dos Recorridos (Secuencia)** | Diagrama de Secuencia UML sobre `CU-01` que modela el orden temporal de los mensajes entre `Estudiante` y `Agente` en el **Recorrido 1 (Normal)** y en el **Recorrido 2 (Alternativo: falta de datos y contradicción)**, ajustado estrictamente a lo que el prototipo Gem realiza. | • [Análisis de Secuencia (Clase 02/10)](./clase_02_10.md#2-paso-1-dos-recorridos-en-diagrama-de-secuencia-cu-01--obtener-orientación)<br>• [📐 Ver Diagrama de Secuencia (SVG)](../diagramas/clase_02_10_secuencia.svg) |
| **6. Tres Reglas de Control** | **Regla 1:** Orientación concluyente con datos completos sobre lista cerrada y taxativa.<br>**Regla 2:** Detención y pedido de aclaración ante información faltante o ambigua (*cursada* vs. *aprobada*).<br>**Regla 3:** Prevalencia de la pág. 9 del Diseño Curricular ante avisos informales y derivación a Secretaría ante discrepancias internas del PDF oficial (págs. 8 y 28). | • [Tres Reglas Condicionales (Clase 02/10)](./clase_02_10.md#3-paso-2-tres-reglas-del-caso-integrador)<br>• [⚙️ Instrucciones del Gem (`v2.1`)](../prototipo/instrucciones_gem.md) |
| **7. Tres Pruebas Reales** | Ejecutadas en **Google Gemini Gems (modelo Gemini Flash)** con datos ficticios: Prueba 1 (Normal: *Estadística*), Prueba 2 (Falta información: *Prácticas Profesionalizantes II*) y Prueba 3 (Contradicción: aviso informal + discrepancia horaria *128 hs vs. 64 hs* en *Algoritmos III*). | • [Pruebas iniciales en Taller](./taller_integracion.md#4-registro-de-pruebas-y-ciclo-de-control)<br>• [Pruebas Caso Real `v2.0` y `v2.1` (Clase 02/10)](./clase_02_10.md#4-paso-3-y-4-tabla-de-las-tres-pruebas-ejecutadas-y-ciclo-de-corrección) |
|  |  |  |

---

### 1.2. Paso 2: Auditoría de Coherencia entre Diagramas, Reglas y Pruebas

Seleccionamos el caso de uso principal **`CU-01 · Obtener orientación`** y verificamos la consistencia cruzada entre todas las representaciones construidas:

1. **¿Sus participantes aparecen de forma consistente en todos los diagramas?**

   * **Sí, con distinción explícita entre Modelo Objetivo y Prototipo Acotado:** En el Diagrama de Contexto (`clase_25_09_contexto.svg`) y en el Diagrama de Casos de Uso (`clase_25_09_casos_de_uso.svg`), `CU-01` tiene como actor principal al **`Estudiante`** y como actores de apoyo al `Servicio Externo de IA`, al `Repositorio Normativo` y a `Gestión Académica`. En la nota de alcance del Contexto, en la especificación de `CU-01` (paso alternativo `3a`) y en el Diagrama de Secuencia (`clase_02_10_secuencia.svg`), se documenta con total coherencia que en el **Prototipo Gem** las reglas normativas ya están inyectadas en las instrucciones y los antecedentes los declara el `Estudiante`, por lo que en la secuencia participan únicamente el `Estudiante` y el `Agente` (motorizado por Gemini Flash). No aparece ningún actor "fantasma" ni se atribuyen conexiones inexistentes.

2. **¿El recorrido de secuencia respeta las tres reglas?**

   * **Sí:**

     * El **Recorrido 1 (Normal, mensajes 1 a 3)** respeta la **Regla 1**: recibe la materia (*Estadística*) y sus dos correlativas aprobadas (*Análisis Matemático I* y *Álgebra*), verifica la lista cerrada de la pág. 9 y devuelve la confirmación con cita normativa y advertencia de alcance.

     * El **Recorrido 2 - Alternativa A (mensajes 4 a 6)** respeta la **Regla 2**: ante la omisión del estado de *Sistemas y Organizaciones* para *Prácticas Profesionalizantes II*, detiene el cálculo y envía el mensaje pidiendo el dato faltante.

     * El **Recorrido 2 - Alternativa B (mensajes 7 a 9)** respeta la **Regla 3**: frente al conflicto entre el aviso informal y la tabla oficial, o entre las páginas 8 y 28 del Diseño Curricular, señala la diferencia y deriva la definición administrativa a Secretaría Académica / Preceptoría.

3. **¿Las pruebas ejecutadas permiten comprobar efectivamente las tres reglas?**

   * **Sí, cada prueba audita una regla específica con evidencia observable:**
   
     * La **Prueba 1** comprueba la **Regla 1** (y fue justamente la que permitió detectar el fallo de sobrerrestricción de la `v2.0` y validar su solución en la `v2.1`).

     * La **Prueba 2** comprueba la **Regla 2** (verificando que el Gem no asume aprobación ni desaprobación cuando falta declarar una correlativa).

     * La **Prueba 3** comprueba la **Regla 3** (verificando que el Gem no convalida rumores ni inventa cuál de las dos cargas horarias contradictorias del PDF ministerial es la correcta).

---

### 1.3. Paso 3: Elección y Justificación de la Mejora Aplicada

Durante la revisión integradora se consolidaron **dos mejoras complementarias** (una sobre el **prototipo funcional** y otra sobre la **sincronización documental de los diagramas**):

1. **Mejora en el Prototipo (`v2.0` $\rightarrow$ `v2.1` en `prototipo/instrucciones_gem.md`):**

   * *¿Qué diferencia se encontró?* Al probar la Versión 2.0 en **Gemini Flash** con la Prueba 1 (Normal), el asistente reconoció que *Estadística* pedía *Análisis Matemático I* y *Álgebra*, pero en lugar de confirmar que el alumno cumplía el requisito, le pidió que confirmara *"todas las demás correlativas previas que pudiera exigir Estadística (es decir, las de 1.º año en general)"*.

   * *¿Qué se cambió y por qué?* Se modificó la **Regla 1** y el encabezado normativo en `prototipo/instrucciones_gem.md` (creando la **Versión 2.1**) para declarar que el listado de correlativas de cada materia es **cerrado, exhaustivo y taxativo** (`requiere únicamente tener aprobadas...`). Se realizó este cambio porque la instrucción anterior (*"Si falta algún dato, pedí aclaración"*) era demasiado abierta y provocaba un falso negativo por exceso de cautela en el modelo Flash. Al repetir la prueba con la `v2.1`, el Gem confirmó el cumplimiento en la primera línea sin pedir materias ajenas a la regla.

2. **Mejora de Coherencia en el Diagrama de Secuencia (`diagramas/clase_02_10_secuencia.svg`):**

   * *¿Qué se ajustó y por qué?* Se actualizaron los mensajes `2`, `3`, `8` y `9` y el espaciado visual del Diagrama de Secuencia para que reflejen exactamente el comportamiento verificado en la **Versión 2.1** (la aplicación de la lista taxativa en el caso normal y la distinción entre el aviso informal de correlativas y la derivación a Secretaría por la discrepancia de horas entre las páginas 8 y 28 del Diseño Curricular), garantizando una correspondencia 1 a 1 entre el dibujo de secuencia, la tabla de pruebas y las instrucciones reales del Gem.

---

## 2. Ficha Breve de Preparación: `9 de octubre · Integración`

Siguiendo el formato requerido en la **Sección 02** del encuentro para organizar la entrega final:

* **Mi agente ayuda a:** Los estudiantes de 1.º, 2.º y 3.º año de la Tecnicatura Superior en Análisis de Sistemas del **ISFT Nº 151** a verificar de manera inmediata, fundada y trazable si cumplen con el régimen de correlatividades del Diseño Curricular oficial (`IF-2019-36021554-GDEBA-CPEYTDGCYE`, pág. 9) según los antecedentes que declaran, reduciendo errores de interpretación antes de las inscripciones sin reemplazar las decisiones administrativas ni los registros oficiales de Secretaría Académica o Preceptoría.

* **El caso de uso que revisé es:** **`CU-01 · Obtener orientación`** (vinculado en el modelo objetivo con su caso incluido obligatorio `CU-05 · Registrar interacción` y su extensión condicional `CU-02 · Solicitar revisión humana`).

* **La prueba mostró que:** Al ejecutar las tres pruebas reales en **Google Gemini Gems (modelo Gemini Flash)** sobre la Versión 2.0 del prototipo, las reglas de contención funcionaron correctamente ante *datos faltantes* (**Prueba 2**: pidió el estado omitido de *Sistemas y Organizaciones* para *Prácticas Profesionalizantes II*) y ante *indicaciones contradictorias* (**Prueba 3**: hizo prevalecer la tabla de la pág. 9 frente a un aviso informal en *Estadística* y derivó a Secretaría la discrepancia real de carga horaria de *Algoritmos III* entre las páginas 8 y 28 del PDF ministerial); sin embargo, en el escenario *normal* (**Prueba 1**), el exceso de restricción del prompt hizo que el modelo dudara de si su lista era completa y pidiera confirmar *"el resto de las materias de 1.º año en general"* antes de dar por cumplido el requisito de *Estadística*.

* **La mejora que hice fue:** Actualizar las instrucciones del prototipo a la **Versión 2.1** ([`prototipo/instrucciones_gem.md`](../prototipo/instrucciones_gem.md)) declarando explícitamente el carácter **cerrado, único y taxativo** de las correlativas de cada unidad curricular en la Regla 1 y prohibiendo exigir el estado de asignaturas no listadas para esa materia; luego repetí la Prueba 1 en una conversación nueva con Gemini Flash comprobando que el asistente ahora responde de forma directa y concluyente (*«Sí, cumplís con los requisitos normativos para la materia Estadística de 2.º año, ya que tenés aprobadas las únicas dos correlativas exigidas: Análisis Matemático I y Álgebra»*), y sincronicé ese resultado con el Diagrama de Secuencia ([`clase_02_10_secuencia.svg`](../diagramas/clase_02_10_secuencia.svg)).

* **Para el final me falta:**

  1. Conocer las pautas específicas de formato o exposición oral de la consigna definitiva de evaluación final (cuando la cátedra la habilite).

  2. Definir si para la demostración final se mantendrá únicamente este alcance acotado a la tabla de correlatividades (que hoy garantiza 100% de precisión en las pruebas) o si se sumará una segunda regla de consulta sobre cargas horarias/campos de formación con su respectiva nota de advertencia sobre las páginas 8, 28 y 29 del Diseño Curricular.

  3. Relevar (en caso de ser requerido en las clases teóricas intermedias 14 y 15 cuando se habiliten) algún dato cuantitativo adicional sobre volumen de consultas en Preceptoría para complementar la evidencia empírica del problema.

### Enlaces Rápidos a Todos los Avances del Proyecto

* 📖 **[Índice General y Presentación (`README.md`)](../README.md)**

* 📄 **[Entrega Clase 12 — Modelo Sistémico Preliminar (`docs/clase_12.md`)](./clase_12.md)** | [📐 Diagrama Caja Negra (`SVG`)](../diagramas/clase_12_flujos_caja_negra.svg)

* 📄 **[Entrega Clase 13 — Estructura, Control y Primeros Modelos (`docs/clase_13.md`)](./clase_13.md)** | [📐 Ciclo de Control (`SVG`)](../diagramas/clase_13_ciclo_control.svg) | [📐 Contexto Inicial (`SVG`)](../diagramas/clase_13_diagrama_contexto.svg) | [📐 Casos de Uso Inicial (`SVG`)](../diagramas/clase_13_casos_de_uso.svg)

* 📄 **[Taller de Integración Clases 12 y 13 — Prototipo Inicial (`docs/taller_integracion.md`)](./taller_integracion.md)**

* 📄 **[Entrega Clase 25/09 — Contexto y Casos de Uso UML 2.5.1 (`docs/clase_25_09.md`)](./clase_25_09.md)** | [📐 Contexto Ampliado (`SVG`)](../diagramas/clase_25_09_contexto.svg) | [📐 Casos de Uso UML 2.5.1 (`SVG`)](../diagramas/clase_25_09_casos_de_uso.svg)

* 📄 **[Entrega Clase 02/10 — Secuencia, Reglas y Control (`docs/clase_02_10.md`)](./clase_02_10.md)** | [📐 Diagrama de Secuencia (`SVG`)](../diagramas/clase_02_10_secuencia.svg)

* ⚙️ **[Configuración e Instrucciones del Prototipo Gem (`v1.1`, `v2.0` y `v2.1`) (`prototipo/instrucciones_gem.md`)](../prototipo/instrucciones_gem.md)**

---

## 3. Cierre: Decisión Central del Proyecto y Fundamento que la Sostiene

* **Decisión arquitectónica y de control elegida:**

  En lugar de subir el archivo PDF crudo de 33 páginas del Diseño Curricular (`IF-2019-36021554-GDEBA-CPEYTDGCYE`) como documento adjunto abierto para que el modelo de lenguaje lo interprete libremente en cada consulta, decidimos **pre-procesar, normalizar y declarar de forma cerrada y taxativa la tabla de correlatividades dentro de las instrucciones de organización del Gem (`Versión 2.1`)**, incluyendo las reglas explícitas de equivalencia terminológica (*"Programación II" = "Algoritmos y Estructuras de Datos II"*) y de derivación humana ante discrepancias internas de carga horaria (páginas 8 vs. 28-29).

* **¿Qué prueba y qué conceptos teóricos de Lorenzón sostienen esta decisión?**

  1. **Desde la evidencia de las pruebas reales:** La auditoría previa del PDF ministerial demostró que el propio documento oficial contiene inconsistencias (nombres distintos entre páginas 8 y 9, y cargas horarias distintas entre páginas 8 y 28). A su vez, la **Prueba 1 en Gemini Flash** demostró que si las reglas de organización dejan el más mínimo margen de apertura sobre qué datos exige cada materia, el modelo neuronal introduce incertidumbre (pidiendo en la `v2.0` confirmar todas las materias de 1.º año). Al cerrar taxativamente la tabla en la `v2.1`, las tres pruebas (Normal, Falta de datos y Contradicción) se cumplieron con exactitud verificable.

  2. **Desde el marco teórico de Emilio Lorenzón:**

     * **Reducción de Variedad e Información como Neguentropía (Cap. 9, pp. 107–108 y Cap. 11, pp. 146–147):** Lorenzón explica que la variedad del entorno y los grados de libertad de una caja negra con *programa propio variable* tienden a la entropía (desorganización/alucinación) a menos que el diseñador imponga restricciones mediante información estructurada. Normalizar la tabla curricular y fijar las tres reglas condicionales actúa como un **reductor de variedad** que mantiene la salida del sistema dentro de su **dominio de estabilidad (meseta homeoquinética)** (Cap. 11, pp. 150–151).
     
     * **Distinción entre Estructura, Organización y Ciclo del Adaptador (Cap. 10, pp. 121–124 y Cap. 11, pp. 152–157):** Sin modificar la estructura tecnológica del asistente (el motor Gemini Flash provisto por el navegador), logramos corregir una falla real de comportamiento interviniendo únicamente sobre su **Organización** (las reglas funcionales del prompt) a través de las unidades del **Adaptador de control** (comparando la respuesta de la `v2.0` contra el estándar esperado, decidiendo el ajuste hacia la `v2.1` y comprobando experimentalmente el nuevo estado en la realidad, tal como exige el ciclo *Realidad–Modelo–Acciones* del **Cap. 12, pp. 179–181**).

---

## 4. Referencias Bibliográficas y Documentales

* **Lorenzón, E. E.** (2020). *Sistemas y Organizaciones*. Editorial de la Universidad Nacional de La Plata (EDULP).
  * *Parte I:* Capítulos 7, 8, 9, 10, 11, 12 y 13 (pp. 84–195).
  * *Parte II:* Capítulo 5 (Los Procesos, pp. 284–313) y Capítulo 8 (Reglas de negocio).

* **Dirección General de Cultura y Educación de la Provincia de Buenos Aires [DGCyE]** (2019). *Diseño Curricular de la Tecnicatura Superior en Análisis de Sistemas* (`IF-2019-36021554-GDEBA-CPEYTDGCYE`).
* **Object Management Group [OMG]** (2017). *OMG Unified Modeling Language (OMG UML), Version 2.5.1*. Capítulo 18: Use Cases.