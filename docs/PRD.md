# PRD — VideoMaker

**Product Requirements Document**

- **Proyecto:** VideoMaker
- **Versión:** 1.1.0
- **Estado:** Draft — Pendiente de revisión y aprobación final del Product Owner
- **Tipo:** Plataforma AI-Native de producción audiovisual
- **Producto de referencia:** Elftuber, pendiente de precisar atributos comparables
- **Plataforma inicial:** Aplicación web
- **Entorno inicial de desarrollo:** Windows
- **Usuario inicial:** Creador del canal Historia Financiera
- **Prioridad estratégica:** calidad audiovisual primero; automatización después; optimización de costos en tercer lugar

---

## 1. Visión del producto

VideoMaker es una plataforma de producción audiovisual asistida por inteligencia artificial, diseñada para crear documentales originales y de alta calidad para YouTube.

La visión de largo plazo es que el usuario pueda introducir un título o tema y que el sistema coordine la investigación, escritura del guion, narración, selección de recursos, construcción de gráficos y animaciones, edición, control de calidad y renderizado del video final.

Esta visión se desarrollará de forma incremental. La automatización completa no se considerará demostrada hasta que el producto mantenga el estándar audiovisual definido en este documento.

**Propuesta de valor:**

> Transformar una idea en un documental audiovisual de calidad editorial mediante un flujo asistido por IA, verificable y controlado por el usuario.

## 2. Decisión estratégica y principios de producto

El orden de prioridades de VideoMaker es:

1. **Calidad audiovisual:** el resultado debe ser publicable y editorialmente defendible.
2. **Automatización:** se automatizarán etapas solamente cuando la automatización conserve o mejore la calidad.
3. **Optimización de costos:** se medirá desde el inicio, pero no se sacrificará calidad para reducir costos durante las primeras validaciones.

Principios derivados:

- Quality-first: la calidad se valida con criterios técnicos y una rúbrica editorial.
- Human-in-the-loop: el usuario conserva la aprobación editorial final.
- Determinismo antes que autonomía: primero se valida un pipeline reproducible; después se incorporan decisiones automáticas.
- Specification-first: los contratos y criterios se definen antes de implementar.
- Incremental delivery: cada gate debe validarse antes de ampliar el alcance.
- Evidence-aware: hechos, datos y activos deben conservar evidencia de procedencia.
- Provider optionality: los proveedores podrán sustituirse cuando exista una necesidad demostrada.
- Observability and cost awareness: se registrarán estados, tiempos, errores y costos desde las primeras pruebas.

## 3. Problema que resolvemos

Los creadores de documentales para YouTube enfrentan un flujo fragmentado y costoso:

- Investigación y verificación manual de información.
- Escritura y revisión de guiones extensos.
- Generación y sincronización de narraciones.
- Búsqueda de B-roll relevante y legalmente reutilizable.
- Creación de gráficos, mapas y animaciones.
- Edición y montaje audiovisual.
- Control de calidad técnico y editorial.
- Tiempos de producción elevados.

Muchas soluciones de generación de video con IA priorizan la velocidad sobre la dirección audiovisual y producen resultados repetitivos, con imágenes estáticas, narración genérica o relaciones débiles entre voz e imagen.

VideoMaker busca reducir el trabajo manual sin degradar la originalidad, la precisión ni la calidad audiovisual.

## 4. Usuarios objetivo y caso de uso inicial

### 4.1 Usuario inicial

El primer entorno de validación será el canal Historia Financiera, con contenido documental en español sobre historia económica, financiera y empresarial.

### 4.2 Expansión futura

La plataforma podrá ampliarse posteriormente a tecnología, geopolítica, historia y documentales educativos. Estos dominios no forman parte de la validación inicial porque presentan necesidades distintas de investigación, licencias y tratamiento editorial.

### 4.3 Resultado futuro esperado

La Beta automatizada deberá orientarse a documentales de entre 15 y 25 minutos. Esta duración no constituye un criterio de aceptación para la PoC ni para el MVP editorial.

## 5. Etapas y gates de validación

Cada gate tiene un propósito, alcance y criterio de salida independiente. Completar un gate no implica haber validado los posteriores.

### 5.1 Gate A — PoC audiovisual determinista de 90 segundos

**Objetivo:** validar que el motor audiovisual puede producir de forma reproducible una pieza de 90 segundos que cumpla el estándar técnico y editorial inicial.

**Alcance:**

- Una pieza original de 90 segundos, con tolerancia de duración pendiente de fijar.
- Guion, narración y recursos preparados o seleccionados manualmente.
- Storyboard versionado y validable antes del renderizado.
- Al menos tres tratamientos visuales distintos.
- Al menos un gráfico animado basado en datos verificables.
- Tipografía dinámica y subtítulos sincronizados.
- Previsualización suficiente para realizar control de calidad.
- Exportación MP4 a 1920 × 1080, 30 fps y video H.264.
- Ejecución en el entorno inicial de desarrollo Windows.

**Fuera de alcance:**

- Investigación autónoma.
- Selección automática abierta de activos.
- Dashboard completo.
- Infraestructura cloud.
- Cola distribuida.
- Orquestación multiagente autónoma.
- Producción de videos de 3 minutos o más.

**Criterio de salida:** cumplimiento de los criterios QA-001 a QA-010 aplicables, aprobación mediante la rúbrica editorial y ausencia de defectos críticos técnicos, factuales o de derechos de uso.

### 5.2 Gate B — MVP editorial de 3–5 minutos

**Objetivo:** validar que el canal piloto puede utilizar VideoMaker para producir y corregir una pieza publicable de 3 a 5 minutos con menos trabajo manual, sin rebajar la calidad alcanzada en Gate A.

**Alcance:**

- Crear y conservar un proyecto de video.
- Generar o importar un guion estructurado y editable.
- Importar o generar narración.
- Crear un storyboard versionado.
- Cargar, asignar y sustituir recursos audiovisuales.
- Previsualizar escenas y el montaje.
- Corregir una escena individual sin reconstruir obligatoriamente el proyecto completo.
- Mantener procedencia, fuentes, licencias y atribuciones de los recursos.
- Renderizar una pieza de entre 3 y 5 minutos.
- Registrar estados, resultados, errores, duración de procesos y costos estimados.
- Mantener aprobación humana del guion y del resultado final.

**Automatización permitida:** asistencia en guion, narración, propuesta de storyboard y clasificación de recursos, siempre con revisión humana.

**Fuera de alcance:**

- Investigación autónoma de extremo a extremo.
- Dirección audiovisual completamente autónoma.
- Documentales de 15–25 minutos.
- Editor profesional de línea de tiempo.
- Generación masiva simultánea.
- Publicación automática en YouTube.
- Arquitectura distribuida obligatoria.

**Criterio de salida:** una pieza de 3–5 minutos cumple la rúbrica editorial, conserva trazabilidad de hechos y activos, permite correcciones individuales y demuestra un flujo utilizable por el canal piloto.

### 5.3 Gate C — Beta automatizada de 15–25 minutos

**Objetivo:** validar la visión de automatización integral en documentales largos sin degradar la calidad editorial.

**Alcance previsto:**

- Investigación asistida con afirmaciones vinculadas a fuentes.
- Generación y revisión de guion largo.
- Dirección audiovisual contextual.
- Recuperación o generación asistida de recursos.
- Narración y sincronización.
- Composición, renderizado y controles automáticos de calidad.
- Intervención humana en puntos de aprobación definidos.
- Ejecución cloud cuando haya sido validada técnica y operacionalmente.

**Condición de entrada:** Gate B aprobado y evidencia de que el sistema mantiene calidad, continuidad narrativa y confiabilidad al aumentar duración y automatización.

**Criterios de salida:** se definirán después de medir Gate B. Deberán incluir calidad sostenida, precisión factual, derechos de uso, capacidad de recuperación, tiempo de producción y costo por minuto.

## 6. Flujo principal objetivo

El flujo representa la visión completa. Cada gate implementará únicamente el subconjunto indicado en su alcance.

1. El usuario crea un proyecto e introduce un título o tema.
2. Define duración, estilo y restricciones editoriales.
3. El sistema prepara o ejecuta la investigación según el gate.
4. Se genera o importa un guion con referencias verificables.
5. El usuario revisa y aprueba el guion.
6. Se construye un storyboard versionado.
7. El sistema propone, obtiene, genera o permite cargar recursos visuales.
8. Se importa o genera la narración y sus marcas temporales.
9. Se compone y previsualiza cada escena.
10. Se validan el storyboard, los activos y los requisitos de renderizado.
11. Se renderiza el video.
12. Se ejecutan controles técnicos y editoriales.
13. El usuario identifica y corrige escenas individuales.
14. Se genera una nueva versión sin perder trazabilidad.
15. El usuario realiza la aprobación editorial final y exporta el MP4.

## 7. Capacidades conceptuales de IA

Las siguientes capacidades describen responsabilidades del producto. **No implican siete servicios, procesos o agentes autónomos separados.** Durante Gate A y Gate B podrán implementarse como pasos deterministas, módulos, herramientas o llamadas controladas a modelos. Su separación física será una decisión arquitectónica posterior basada en evidencia.

### Research

Investigar el tema, recopilar fuentes, identificar afirmaciones verificables, distinguir hechos de inferencias y registrar evidencia.

### Scriptwriting

Transformar investigación aprobada en una narrativa documental estructurada y original.

### Direction

Definir el tratamiento audiovisual de escenas: B-roll, material histórico, gráficos, mapas, líneas de tiempo, tipografía cinética o animaciones explicativas.

### Asset Management

Obtener, cargar y organizar recursos, conservando procedencia, autor, URL, licencia, fecha de consulta, restricciones y atribución requerida.

### Voice

Importar o generar narración, gestionar segmentación y producir o derivar marcas temporales para sincronización.

### Editing

Componer escenas, transiciones, subtítulos, gráficos, audio y efectos según el storyboard aprobado.

### Quality Control

Detectar problemas técnicos, audiovisuales, factuales y de trazabilidad. Este control asiste al usuario y no sustituye la revisión editorial o legal final.

## 8. Contrato funcional versionado del storyboard

El storyboard será el contrato funcional entre guion, recursos, narración, edición y renderizado. Su esquema técnico definitivo se diseñará posteriormente.

Como mínimo deberá permitir:

1. **Versionado:** identificar la versión del contrato y permitir evolución compatible o migraciones explícitas.
2. **Identificadores estables:** asignar identificadores únicos y persistentes a escenas y elementos relevantes para poder corregirlos y rastrearlos.
3. **Tiempo:** representar duración, inicio, fin y marcas temporales con una unidad no ambigua.
4. **Narración:** asociar texto, segmento de audio, voz y marcas temporales con cada escena.
5. **Subtítulos:** representar texto, intervalos temporales y relación con la narración.
6. **Recursos audiovisuales:** referenciar imágenes, clips, audio, música, documentos, gráficos y variantes, sin exigir que estén embebidos en el contrato.
7. **Tratamiento visual:** expresar encuadre, recorte, movimiento, capas, textos, gráficos y otros parámetros necesarios para la composición.
8. **Animaciones y transiciones:** identificar tipo, duración, parámetros y relación entre escenas.
9. **Fuentes y licencias:** vincular hechos, datos y activos con su procedencia, condiciones de uso y atribución.
10. **Corrección individual:** sustituir o modificar una escena manteniendo estable el resto del proyecto cuando sus dependencias no hayan cambiado.
11. **Validación previa:** detectar campos obligatorios ausentes, tiempos incoherentes, recursos inexistentes, incompatibilidades y ausencia de datos de procedencia antes del renderizado.
12. **Trazabilidad:** conocer qué versiones de guion, narración, datos y activos produjeron cada render.

El contrato no deberá depender innecesariamente de un proveedor de IA. La dependencia respecto del motor de composición se evaluará durante el diseño técnico.

## 9. Calidad audiovisual — Quality-First

Los siguientes umbrales son **hipótesis iniciales sujetas a validación** durante Gate A y Gate B. Podrán endurecerse o corregirse con evidencia, sin reducir silenciosamente el estándar para aprobar una entrega.

### QA-001 — Formato de exportación

El video deberá exportarse a 1920 × 1080, 30 fps y H.264. El contenedor, perfil, pixel format, bitrate y parámetros de audio quedan pendientes de definición técnica.

### QA-002 — Sincronización de subtítulos

El desfase máximo objetivo entre narración y subtítulos será de 200 ms. El método de medición y las excepciones editoriales deberán documentarse.

### QA-003 — Narración

La narración deberá ser inteligible y no presentar defectos audibles como cortes, clipping, distorsión, repeticiones involuntarias, pronunciaciones inaceptables o variaciones abruptas no justificadas.

### QA-004 — Ritmo visual

Todo plano o composición esencialmente estática que permanezca más de 8 segundos deberá tener una justificación editorial registrada o incluir evolución visual intencional. Este umbral no obliga a introducir cortes innecesarios.

### QA-005 — Variedad visual de la PoC

Gate A deberá incluir al menos tres tratamientos visuales distintos y editorialmente pertinentes.

### QA-006 — Gráfico animado verificable

Gate A deberá incluir al menos un gráfico animado cuyos datos, unidades, periodo y fuente sean verificables y estén documentados.

### QA-007 — Legibilidad y zonas seguras

Textos, subtítulos y elementos informativos deberán ser legibles en 1080p y permanecer dentro de zonas seguras definidas. Los parámetros concretos de contraste, tamaño mínimo y márgenes quedan pendientes de calibración.

### QA-008 — Integridad audiovisual

El video no deberá contener pantallas negras accidentales, frames corruptos, saltos no intencionales, silencios inesperados, activos faltantes ni placeholders visibles.

### QA-009 — Originalidad, procedencia y derechos

El guion deberá ser original. Los hechos, datos y activos deberán conservar procedencia documentada y someterse a revisión de derechos de uso. Registrar una licencia o citar una fuente no constituye por sí solo aprobación legal.

### QA-010 — Revisión editorial

La pieza deberá obtener una puntuación promedio mínima de 4/5 según la rúbrica editorial, sin dimensiones inferiores a 3/5 y sin defectos críticos técnicos, factuales o de derechos de uso.

## 10. Rúbrica editorial

Cada dimensión se calificará de 1 a 5:

- **1 — Deficiente:** impide publicar; requiere reconstrucción sustancial.
- **2 — Insuficiente:** presenta problemas mayores y requiere correcciones extensas.
- **3 — Aceptable:** cumple lo mínimo, con correcciones localizadas o margen claro de mejora.
- **4 — Bueno:** calidad publicable, coherente y con defectos menores.
- **5 — Excelente:** resultado especialmente sólido, pulido y editorialmente convincente.

### 10.1 Narrativa y claridad

Evalúa estructura, comprensión, progresión, precisión, originalidad, transiciones narrativas y adecuación al público.

### 10.2 Dirección audiovisual

Evalúa pertinencia entre imagen y narración, variedad con propósito, continuidad visual, elección de recursos y coherencia estilística.

### 10.3 Edición y ritmo

Evalúa duración de planos, cortes, transiciones, continuidad, densidad de información y capacidad de mantener atención sin introducir movimiento arbitrario.

### 10.4 Audio y narración

Evalúa inteligibilidad, interpretación, pronunciación, consistencia, sincronización, mezcla y ausencia de defectos audibles.

### 10.5 Gráficos y legibilidad

Evalúa exactitud de datos, claridad visual, jerarquía, contraste, tipografía, zonas seguras, animación y tiempo suficiente de lectura.

### 10.6 Criterio preliminar de aprobación

- Promedio mínimo: 4/5.
- Ninguna dimensión inferior a 3/5.
- Ningún defecto crítico técnico, factual o de derechos de uso.
- Las puntuaciones deberán incluir observaciones y responsable de la revisión.

Se considera defecto crítico cualquier problema que impida publicar de forma responsable, aunque el promedio numérico sea suficiente.

## 11. Requisitos funcionales por gate

### 11.1 Gate A

- GA-001: cargar o referenciar un guion aprobado.
- GA-002: cargar o referenciar narración y recursos preparados manualmente.
- GA-003: construir y validar el storyboard versionado.
- GA-004: previsualizar el resultado con fidelidad suficiente para revisión.
- GA-005: renderizar un MP4 de 90 segundos.
- GA-006: ejecutar controles QA técnicos y registrar resultados.
- GA-007: aplicar la rúbrica editorial y conservar su evaluación.

### 11.2 Gate B

- GB-001: crear, abrir y versionar un proyecto.
- GB-002: importar, generar y editar un guion estructurado.
- GB-003: importar o generar narración segmentada.
- GB-004: construir y editar el storyboard.
- GB-005: cargar, asignar y sustituir recursos con procedencia.
- GB-006: previsualizar escenas y montaje.
- GB-007: corregir y volver a procesar una escena individual cuando sus dependencias lo permitan.
- GB-008: renderizar una pieza de 3–5 minutos.
- GB-009: registrar errores, resultados, tiempos y costos estimados.
- GB-010: conservar versiones y trazabilidad de los inputs del render.
- GB-011: ejecutar revisión técnica y editorial antes de exportar.

### 11.3 Gate C

Los requisitos detallados se definirán tras Gate B. La automatización deberá integrarse por capacidades y demostrar que no degrada los criterios de calidad.

## 12. Requisitos no funcionales

### 12.1 Calidad y reproducibilidad

El sistema deberá conservar los inputs, versiones y parámetros necesarios para explicar y, cuando sea técnicamente posible, reproducir un render.

### 12.2 Confiabilidad

Los procesos deberán registrar fallos y permitir reintentos controlados. Las operaciones reintentables deberán evitar resultados duplicados o estados inconsistentes.

### 12.3 Validación temprana

El sistema deberá rechazar antes del render los storyboards inválidos, activos inaccesibles y parámetros incompatibles que puedan detectarse anticipadamente.

### 12.4 Observabilidad

Cada proceso relevante deberá registrar estado, duración, errores, versiones y costos estimados. Los formatos y herramientas se decidirán posteriormente.

### 12.5 Seguridad

Las credenciales de proveedores deberán almacenarse de forma segura y no aparecer en logs, storyboards ni archivos exportados.

### 12.6 Modularidad pragmática

Las fronteras entre proveedores y motores deberán permitir sustitución razonable, sin introducir abstracciones o servicios anticipados que no aporten valor al gate actual.

### 12.7 Derechos y procedencia

Cada activo deberá poder registrar, como mínimo, origen, autor cuando corresponda, URL o referencia, fecha de consulta, licencia declarada, restricciones conocidas, atribución requerida y evidencia disponible.

La revisión automática ayudará a detectar ausencias o inconsistencias, pero no sustituirá la responsabilidad editorial o legal.

### 12.8 Rendimiento y escalabilidad

Gate A podrá ejecutarse localmente en Windows. La separación entre aplicación, procesamiento y renderizado, así como la ejecución cloud, se evaluarán después de medir consumo de CPU, memoria, almacenamiento, tiempos y confiabilidad.

No se exige arquitectura distribuida para Gate A ni Gate B.

## 13. Tecnologías candidatas

Las tecnologías son hipótesis sujetas a pruebas técnicas, revisión de mantenimiento y revisión de licencias.

| Componente | Candidato inicial | Estado |
|---|---|---|
| Interfaz web | Next.js + TypeScript | Pendiente de validación en Gate B |
| Runtime de aplicación | Node.js | Pendiente de validación |
| Persistencia | PostgreSQL | Pendiente de justificar para Gate B |
| Composición de video | Remotion | Candidato para Gate A; pendiente de PoC y revisión de licencia |
| Procesamiento multimedia | FFmpeg / ffprobe | Candidato para Gate A; pendiente de configuración y revisión de licencia |
| Generación de voz | Proveedor intercambiable o audio importado | Pendiente de benchmark |
| Modelos de IA | APIs y, cuando se justifique, modelos locales | Pendiente por capacidad |
| Contenedores | Docker | No requerido para Gate A; pendiente de necesidad operacional |
| Infraestructura | Windows local inicialmente; nube posteriormente | Nube pendiente de métricas y diseño |

No se comprometen en esta versión Redis, BullMQ ni una arquitectura distribuida. La necesidad de una cola de trabajos y su tecnología se decidirán después de medir el pipeline y definir los requisitos de concurrencia, recuperación y despliegue.

Remotion y FFmpeg no se consideran aprobados automáticamente: deberán superar revisión técnica, de licencias, calidad de salida, rendimiento y sostenibilidad.

## 14. Fuera del alcance inicial

No se implementarán durante Gate A:

- Publicación automática en YouTube.
- Monetización mediante suscripciones.
- Aplicación móvil.
- Generación masiva simultánea.
- Editor profesional de línea de tiempo.
- Entrenamiento de modelos propios.
- Investigación autónoma.
- Generación completa de documentales largos.
- Infraestructura GPU permanente.
- Infraestructura cloud obligatoria.
- Microservicios o agentes desplegados de forma independiente por defecto.

Las exclusiones específicas de Gate B y Gate C se detallan en la sección 5.

## 15. Criterios de aceptación por gate

### 15.1 Gate A — PoC audiovisual

Gate A se considerará candidato a aprobación cuando:

1. Exista un storyboard versionado que cumpla los requisitos funcionales de la sección 8.
2. La validación previa al render no reporte errores bloqueantes.
3. Se produzca un MP4 de 90 segundos, dentro de la tolerancia que se defina, a 1920 × 1080, 30 fps y H.264.
4. La pieza incluya al menos tres tratamientos visuales pertinentes.
5. Incluya un gráfico animado con fuente y datos verificables.
6. Los subtítulos cumplan el objetivo inicial de desfase máximo de 200 ms.
7. La narración sea inteligible y no tenga defectos audibles detectados en la revisión.
8. No existan pantallas negras accidentales, saltos, silencios inesperados ni activos faltantes.
9. Los textos sean legibles y permanezcan dentro de las zonas seguras definidas.
10. La procedencia del guion, los datos y los activos esté documentada y revisada.
11. La rúbrica editorial obtenga promedio mínimo 4/5, ninguna dimensión inferior a 3/5 y ningún defecto crítico.
12. Se registren parámetros, duración, errores y resultado del render.

Gate A valida el motor audiovisual; no valida el MVP editorial ni la automatización de extremo a extremo.

### 15.2 Gate B — MVP editorial

Gate B se considerará candidato a aprobación cuando:

1. El usuario del canal piloto pueda completar el flujo de creación, revisión, corrección y exportación.
2. Se produzca una pieza publicable de entre 3 y 5 minutos.
3. Sea posible corregir una escena individual sin reprocesar etapas no afectadas, cuando las dependencias lo permitan.
4. El proyecto conserve versiones y trazabilidad del guion, narración, storyboard, datos y activos.
5. La pieza cumpla los criterios QA aplicables y la rúbrica editorial.
6. Los hechos y gráficos evaluados dispongan de referencias revisables.
7. Todos los activos utilizados dispongan de procedencia y estado de revisión de derechos.
8. Los fallos recuperables puedan reintentarse sin duplicar resultados ni corromper el proyecto.
9. Se registren tiempos de producción, tiempo de corrección manual, costos estimados y escenas aceptadas sin cambios.
10. El Product Owner determine, con evidencia del canal piloto, si el flujo aporta suficiente valor para iniciar Gate C.

### 15.3 Gate C — Beta automatizada

Sus criterios definitivos se redactarán después de Gate B. No heredará automáticamente los umbrales de duración, costo o autonomía del MVP; sí deberá conservar o superar su estándar de calidad.

## 16. Estrategia de pruebas

### 16.1 Pruebas del contrato

- Validación de campos obligatorios y versiones.
- Detección de tiempos negativos, solapamientos inválidos y duraciones incoherentes.
- Detección de activos ausentes o incompatibles.
- Validación de referencias de fuentes y licencias requeridas.
- Compatibilidad o migración explícita entre versiones del storyboard.

### 16.2 Pruebas audiovisuales

- Inspección automatizada de resolución, fps, codec, duración y streams.
- Detección de frames negros accidentales, silencios inesperados y media corrupta.
- Medición de sincronización de subtítulos con revisión humana de muestra.
- Validación de safe areas y legibilidad.
- Comparaciones de regresión sobre proyectos de referencia.

### 16.3 Pruebas editoriales

- Aplicación documentada de la rúbrica de cinco dimensiones.
- Verificación factual de afirmaciones y datos seleccionados.
- Revisión de originalidad, coherencia narrativa y pertinencia visual.
- Registro de defectos críticos y decisiones de excepción.

### 16.4 Pruebas de confiabilidad

- Reintento de procesos fallidos.
- Recuperación desde la última etapa válida.
- Corrección de una escena sin alterar innecesariamente las demás.
- Repetición de renders con inputs versionados.
- Manejo de activos no disponibles y errores de proveedores.

## 17. Indicadores de éxito

La calidad tendrá precedencia en la interpretación de métricas.

### 17.1 Indicadores primarios de calidad

- Puntuación total y por dimensión de la rúbrica editorial.
- Número de defectos críticos por render.
- Porcentaje de escenas aprobadas sin corrección.
- Número y severidad de defectos técnicos.
- Exactitud y trazabilidad de datos y afirmaciones revisadas.
- Porcentaje de activos con procedencia completa.

### 17.2 Indicadores secundarios de automatización

- Tiempo manual por minuto terminado.
- Número de intervenciones manuales por escena.
- Porcentaje de etapas completadas con asistencia automática y aceptadas sin cambios.
- Número de regeneraciones necesarias.

### 17.3 Indicadores terciarios de costo y rendimiento

- Costo estimado por minuto producido.
- Tiempo de render por minuto terminado.
- Tiempo total de producción.
- Consumo de CPU, memoria y almacenamiento.
- Tasa de fallos y reintentos.

Los objetivos numéricos de costo y rendimiento se fijarán después de obtener una línea base en Gate A. Esos objetivos no deberán reducir el estándar de calidad sin una decisión explícita del Product Owner.

## 18. Orden recomendado de implementación

1. Definir la pieza de referencia y completar la rúbrica de revisión.
2. Definir el contrato funcional y la primera especificación técnica del storyboard.
3. Construir el pipeline determinista de Gate A en Windows.
4. Validar composición, subtítulos, audio, gráfico, tipografía y exportación.
5. Incorporar validaciones previas y controles QA.
6. Iterar hasta cumplir el criterio de salida de Gate A.
7. Diseñar persistencia, versiones y corrección individual para Gate B.
8. Construir la experiencia editorial mínima de 3–5 minutos.
9. Medir calidad, trabajo manual, tiempos, fallos y costos.
10. Automatizar capacidades de una en una, manteniendo comparación contra la línea base.
11. Evaluar ejecución cloud y procesamiento asíncrono con datos reales.
12. Definir y ejecutar Gate C.

## 19. Decisiones pendientes

Las siguientes decisiones permanecen abiertas y no deberán asumirse durante la implementación:

1. Tolerancia exacta de duración para la pieza de 90 segundos y para el rango de 3–5 minutos.
2. Esquema técnico definitivo y formato de serialización del storyboard.
3. Grado de acoplamiento entre storyboard y Remotion.
4. Contenedor, perfil H.264, pixel format, bitrate y parámetros de audio.
5. Definición exacta de zonas seguras, tamaños mínimos y contraste.
6. Método de medición del desfase de subtítulos.
7. Criterios cuantitativos de loudness, true peak y silencios.
8. Política de música y efectos sonoros.
9. Licencias de activos permitidas, restringidas o sujetas a revisión manual.
10. Formato de evidencia de procedencia y atribución.
11. Procedimiento de revisión factual y tratamiento de fuentes contradictorias.
12. Proveedor o estrategia de narración y timestamps.
13. Necesidad y selección de base de datos para Gate B.
14. Necesidad de cola de trabajos y tecnología asociada.
15. Estrategia de almacenamiento, retención y eliminación.
16. Autenticación, autorización y aislamiento entre proyectos o usuarios.
17. Fronteras entre aplicación, worker y motor de render.
18. Momento y proveedor de infraestructura cloud.
19. Evaluación técnica y legal de Remotion y FFmpeg.
20. Atributos concretos del producto de referencia Elftuber que deben compararse.
21. Definición detallada y criterios de aceptación de Gate C.
22. Objetivos numéricos de costo, rendimiento y reducción de trabajo manual.

## 20. Riesgos abiertos

### 20.1 Calidad subjetiva

La rúbrica reduce ambigüedad, pero la evaluación continúa dependiendo del juicio editorial. Se necesitarán ejemplos de referencia y calibración entre revisores.

### 20.2 Escalado de duración

La calidad de una pieza de 90 segundos no garantiza continuidad, variedad ni precisión en 3, 5 o 25 minutos.

### 20.3 Sincronización y regeneración parcial

Modificar guion, narración o duración puede afectar escenas posteriores. La corrección individual requerirá reglas claras de dependencias y versionado.

### 20.4 Derechos de uso

Los metadatos de licencia pueden ser incompletos o incorrectos. También pueden existir restricciones de imagen, marcas, privacidad, derechos morales o condiciones específicas del proveedor.

### 20.5 Precisión factual

Los modelos pueden inventar, simplificar o descontextualizar información. La trazabilidad no garantiza por sí sola que una afirmación sea correcta.

### 20.6 Dependencia de proveedores

Voz, modelos, fuentes de activos y servicios cloud pueden cambiar precios, disponibilidad, calidad o términos.

### 20.7 Licencias y codecs

Remotion, FFmpeg, codecs y builds específicas pueden implicar obligaciones distintas que deben revisarse antes de comercializar o distribuir el producto.

### 20.8 Rendimiento en Windows

Diferencias de fuentes, paths, codecs, drivers y procesos pueden afectar reproducibilidad entre desarrollo local y nube.

### 20.9 Complejidad prematura

Introducir múltiples agentes, servicios o infraestructura distribuida antes de validar el pipeline puede aumentar fallos y mantenimiento sin mejorar el resultado.

### 20.10 Economía unitaria

La prioridad actual acepta costos mayores para alcanzar calidad. Aun así, una Beta de 15–25 minutos podría resultar económicamente inviable y requerir rediseño posterior.

## 21. Definición de terminado

Una funcionalidad estará terminada cuando:

- Pertenezca a un gate definido y no dependa de criterios de otro gate para declararse completa.
- Cumpla criterios de aceptación verificables.
- Tenga las pruebas pertinentes ejecutadas y registradas.
- No introduzca defectos críticos conocidos.
- Documente defectos no críticos aceptados y su justificación.
- Mantenga trazabilidad de inputs y versiones cuando corresponda.
- Tenga documentación actualizada.
- Haya sido revisada por el responsable definido.

Un gate solo podrá declararse aprobado mediante decisión explícita del Product Owner después de revisar sus evidencias. La publicación de este PRD no constituye aprobación automática.

---

**Fin del documento PRD — VideoMaker v1.1.0**
