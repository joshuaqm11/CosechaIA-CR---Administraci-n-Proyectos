# Expediente del Proyecto — CosechaIA CR

> Documento vivo. Se acumula y revisa desde la Semana 1 hasta la Semana 11.
> ISW-912 · Proyecto Incremental

---

## 00. Portada e identificación del equipo

| Campo | Detalle |
|-------|---------|
| Proyecto | CosechaIA CR |
| Curso | ISW-912 · Administración de Proyectos Informáticos |
| Institución | UTN Sede San Carlos |
| Periodo | III Cuatrimestre 2026 |
| Docente | Yesenia Calvo |
| Versión del expediente | 1.3 |

**Integrantes**

| Integrante | Rol en el proyecto |
|------------|--------------------|
| Joshua Quesada Madrigal | Director del proyecto (PM), Product Owner y Developer |
| José Fabio Oconitrillo Salazar | Scrum Master, Developer y QA |

---

## 01. Problema, oportunidad y Product Goal

### Problema y justificación

Los pequeños productores no cuentan con información integrada y personalizada sobre precios, mercado, compradores y transporte. Las fuentes públicas (CENADA, SIMM del PIMA) están dispersas. Esto los lleva a vender en momentos poco favorables o a depender de intermediarios.

### Oportunidad

CosechaIA CR es una plataforma móvil **offline-first** que usa Inteligencia Artificial para que pequeños productores agrícolas de Costa Rica registren su producción (cultivo, cantidad y fecha estimada de cosecha) y reciban alertas personalizadas sobre oportunidades de comercialización, con base en precios y tendencias del CENADA/SIMM, además de un módulo de vinculación con compradores interesados. La aplicación funciona sin conexión para las funciones básicas y sincroniza cuando hay conectividad.

### Product Goal

Desarrollar una plataforma móvil inteligente que facilite la comercialización anticipada de productos agrícolas mediante el análisis de precios, tendencias y demanda con IA, dándoles una herramienta simple, que funcione sin Internet, para decidir mejor cuándo y a quién vender.

### Objetivos específicos

1. Interfaz móvil sencilla para registrar producción, incluso sin conexión.
2. Herramientas de IA que generen alertas personalizadas de comercialización.
3. Módulo de vinculación entre productores y compradores.

---

## 02. Contexto organizacional y restricciones

### Restricciones

Tiempo fijo (10 semanas), equipo de 2 personas, sin presupuesto externo. El alcance es la variable flexible.

### Lean Canvas

| Bloque | Contenido |
|--------|-----------|
| Problema | Información de mercado dispersa y no personalizada; dependencia de intermediarios; dificultad para hallar compradores |
| Segmentos | Pequeños productores agrícolas (principal); compradores de productos agrícolas (secundario) |
| Propuesta de valor | Decidir cuándo y a quién vender con alertas personalizadas, desde una app sencilla que funciona sin Internet |
| Solución | Registro de producción offline, alertas con IA sobre precios CENADA/SIMM, vinculación con compradores |
| Canales | App móvil; difusión por asociaciones de productores y ferias agrícolas (hipótesis) |
| Ingresos | Gratuita para el productor; suscripción o comisión a compradores (hipótesis, fuera del alcance académico) |
| Costos | Horas del equipo, nube/almacenamiento, mantenimiento del modelo de IA |
| Métricas | Productores y compradores registrados, alertas generadas, coincidencias logradas (por definir) |
| Ventaja diferencial | Offline-first + personalización por cultivo + vinculación directa con compradores en una sola herramienta |

### Factores Ambientales de la Empresa (EEFs)

| Tipo | Factor | Efecto en el proyecto |
|------|--------|-----------------------|
| Interno | Equipo pequeño y autoorganizado | Favorece Scrum; riesgo de sobrecarga por roles compartidos |
| Interno | Calendario fijo de 10 semanas | Tiempo fijo; el alcance se ajusta |
| Interno | Infraestructura gratuita o de código abierto | Limita servicios de pago y decisiones de arquitectura |
| Externo | Disponibilidad de datos CENADA/SIMM | Insumo clave para la IA; riesgo si cambia el acceso o formato |
| Externo | Normativa de protección de datos personales | Restringe qué datos se recolectan y cómo se usan |
| Externo | Conectividad rural limitada | Justifica el enfoque offline-first y complica la sincronización |
| Externo | Baja alfabetización digital de algunos productores | Exige una interfaz muy simple |
| Externo | Estacionalidad y volatilidad del mercado agrícola | Condiciona la calidad de las alertas |

---

## 03. Interesados / stakeholders

### Registro de interesados

| # | Interesado | Rol / relación | Necesidad | Poder (1-5) | Interés (1-5) | Actitud | Estrategia | Responsable |
|---|------------|----------------|-----------|:-----------:|:-------------:|---------|------------|-------------|
| 1 | Pequeños productores agrícolas | Usuario primario / cliente final | Acceder a información oportuna de precios, tendencias y compradores, incluso sin conexión a Internet. | 2 | 5 | Mixta | Mantener informado; involucrarlos en pruebas de usabilidad y validaciones de campo. | Joshua Quesada |
| 2 | Compradores formales (agroindustrias, mayoristas) | Usuario secundario / lado de la demanda | Encontrar oferta confiable, con cantidades y fechas reales, reduciendo costo de búsqueda. | 3 | 3 | Neutral | Monitorear; mantener informado sobre el módulo de vinculación. | José Fabio |
| 3 | Intermediarios tradicionales (acopiadores) | Actor externo del entorno de mercado | Mantener su rol y margen actual en la cadena de comercialización. | 2 | 3 | Resistente | Monitorear; buscar puntos de colaboración en vez de confrontación directa. | Joshua Quesada |
| 4 | CENADA / PIMA — SIMM | Proveedor externo de datos de mercado | Uso correcto y autorizado de su información pública de precios. | 4 | 2 | Neutral | Mantener satisfecho; formalizar condiciones de uso de los datos. | José Fabio |
| 5 | Transportistas / logística agrícola | Actor externo, insumo de datos de costo/tiempo | Que la app refleje con precisión costos y tiempos de transporte. | 2 | 2 | Neutral | Monitorear. | Joshua Quesada |
| 6 | MAG, extensionistas y asociaciones del sector agrícola | Institución pública / aliado potencial y posible canal de difusión | Alineación con la política agrícola y apoyo a los productores. | 4 | 3 | Favorable | Mantener satisfecho; explorar alianza de difusión con productores. | José Fabio |
| 7 | Equipo de desarrollo (Joshua y José Fabio) | Equipo del proyecto | Tiempo, conocimiento técnico (IA, desarrollo móvil offline-first) y alcance claro. | 5 | 5 | Favorable | Gestionar de cerca (autogestión, revisión periódica de avance). | Ambos |
| 8 | UTN — Sede Regional de San Carlos | Institución académica | Cumplimiento normativo del curso y uso adecuado del nombre institucional. | 3 | 2 | Neutral | Mantener informado. | José Fabio |
| 9 | Docente del curso ISW-912 | Patrocinador / evaluador | Cumplimiento de los objetivos del curso y entregables en cada hito. | 5 | 5 | Favorable | Gestionar de cerca. | Ambos |

### Justificación de valoraciones y casos discutibles

**Pequeños productores (Poder = 2, Interés = 5).** No tienen autoridad formal para aprobar presupuesto ni alcance del proyecto, por lo que se les asignó poder bajo. Sin embargo, su decisión de adoptar o no la aplicación determina el éxito real del producto; ese "poder de adopción" no es poder formal de gobernanza, por lo que se mantiene separado del interés, que sí es el más alto del registro.

**CENADA / PIMA — SIMM (Poder = 4, Interés = 2).** Al ser una entidad pública con su propia agenda, el proyecto académico no es prioritario para ellos (interés bajo). No obstante, se les asignó poder alto porque son la única fuente disponible de precios mayoristas: si restringen, cambian de formato o no autorizan el uso sistemático de sus datos, el motor de IA del proyecto queda comprometido.

**Intermediarios tradicionales (Poder = 2, Interés = 3, actitud "Resistente").** Se incluyen aun sin relación contractual con el proyecto porque la propuesta original señala la dependencia de intermediarios como parte del problema. No tienen poder formal sobre el proyecto, pero sí pueden influir informalmente sobre los productores (con quienes ya tienen relación de confianza) para desincentivar el uso de la plataforma.

### Mapa Poder-Interés

Para graficar el mapa se simplificó la escala 1-5 a Bajo (1-3) / Alto (4-5).

|  | **INTERÉS BAJO (1-3)** | **INTERÉS ALTO (4-5)** |
|--|------------------------|------------------------|
| **PODER ALTO (4-5)** | **Mantener satisfecho**<br>4. CENADA / PIMA — SIMM<br>6. MAG, extensionistas y asociaciones | **Gestionar de cerca**<br>7. Equipo de desarrollo<br>9. Docente ISW-912 |
| **PODER BAJO (1-3)** | **Monitorear**<br>2. Compradores formales<br>3. Intermediarios tradicionales<br>5. Transportistas<br>8. UTN Sede San Carlos | **Mantener informado**<br>1. Pequeños productores |

### Tres interesados críticos y estrategia de involucramiento

**1. Pequeños productores agrícolas**
- **Por qué es crítico:** son la razón de ser del proyecto; sin adopción real de este grupo, la plataforma no genera el valor esperado, sin importar qué tan bien funcione la IA.
- **Cómo se involucrará:** entrevistas y pruebas de usabilidad con productores de la zona de San Carlos; prototipos simples (mockups) antes de programar; lenguaje claro y capacitación básica; canal de retroalimentación accesible (p. ej. WhatsApp o visitas de campo); piloto con un grupo reducido antes de escalar.

**2. CENADA / PIMA — SIMM**
- **Por qué es crítico:** son la fuente de datos que alimenta el motor de IA (precios, tendencias, estacionalidad); sin una relación clara con ellos, el análisis pierde confiabilidad.
- **Cómo se involucrará:** investigar y documentar formalmente las condiciones de uso de sus datos abiertos; diseñar la integración de forma tolerante a cambios de formato (plan de contingencia); mantener registro de la fuente y frecuencia de actualización usada en el proyecto.

**3. Docente del curso ISW-912**
- **Por qué es crítico:** es quien aprueba, evalúa y puede exigir ajustes de alcance o enfoque; su satisfacción condiciona el avance académico del proyecto.
- **Cómo se involucrará:** entregar evidencias en cada hito del curso (registro de interesados, mapa Poder-Interés, prototipo); solicitar retroalimentación temprana antes de las entregas finales; comunicar de inmediato cualquier cambio relevante de alcance.

---

## 04. Ciclo de vida del proyecto y primer Sprint

### Enfoque de gestión: Híbrido

**Decisión del equipo:** enfoque **Híbrido**.

**Elementos que justifican la parte predictiva**

- Fechas de entrega fijas ya impuestas, no negociables.
- Los tres objetivos específicos delimitan un alcance macro relativamente estable (interfaz offline de registro, motor de IA de alertas, módulo de vinculación productor-comprador), lo que permite planificar fases y entregables generales con anticipación.

**Elementos que justifican la parte adaptativa**

- Alta incertidumbre en los requisitos de UX del segmento de usuario (productores rurales, posible baja alfabetización digital, conectividad intermitente): requiere prototipos y ciclos cortos de retroalimentación.
- El componente de IA (análisis de precios, tendencias y alertas personalizadas) es experimental: su precisión depende de datos reales del CENADA/SIMM y debe ajustarse iterativamente.
- El módulo de vinculación depende de la adopción real de ambos lados del mercado, un comportamiento que no puede planificarse con certeza desde el inicio.
- La conectividad limitada añade incertidumbre técnica en la sincronización offline-first, que se resuelve mejor con iteraciones sucesivas.

**Conclusión:** planificación predictiva a nivel de hitos académicos, alcance macro y cronograma general del curso (10 semanas), combinada con ciclos adaptativos (5 sprints de Scrum) para el diseño con productores, el ajuste del modelo de IA y la validación del módulo de vinculación.

### Cadencia de sprints

Duración total: 10 semanas, divididas en 5 sprints de 2 semanas.

| Sprint | Semanas | Sprint Goal |
|--------|---------|-------------|
| 1 | 1-2 | Dejar lista la base técnica, el diseño validado con productores y el acceso de usuarios a la app. |
| 2 | 3-4 | Registro y consulta de producción sin conexión, e ingesta de precios del CENADA/SIMM. |
| 3 | 5-6 | Sincronización de datos al volver la conexión y primer análisis de tendencias de precios. |
| 4 | 7-8 | Alertas personalizadas al productor; registro de compradores y publicación de demanda. |
| 5 | 9-10 | Conectar oferta y demanda, validar con productores y cerrar con producto estable y documentado. |

### Primer Sprint — Sprint 1 (semanas 1-2)

**Sprint Goal:** dejar lista la base técnica, el diseño validado con productores y el acceso de usuarios a la app.

**Historias comprometidas:** HU-01, HU-02, HU-03, HU-08, HU-16, HU-27, HU-28 y HU-29 (23 SP). El detalle está en las secciones 05 y 06.

**Entregable del sprint:** app base con inicio de sesión, perfil y mockups validados.

**Seguimiento:** el Sprint Backlog 1 está cargado en el Tablero de Trabajo de Trello (sección 10).

### Eventos Scrum

Los eventos de Scrum (Sprint Planning, Daily, Refinamiento, Sprint Review y Retrospectiva), con su frecuencia, duración, participantes y canal, se definen en el **Plan de Comunicaciones** (sección 10), porque son a la vez los principales eventos de comunicación del equipo.

---

## 05. Backlog inicial y Sprint Backlog

**Escala de puntos de historia (SP):** Fibonacci (1, 2, 3, 5, 8). **Prioridad:** MoSCoW (Must / Should / Could).
**Responsable:** J = Joshua, F = Fabio. Lo que desarrolla uno lo prueba el otro.

### Épicas

| ID | Épica | Objetivo específico |
|----|-------|---------------------|
| E1 | Cuenta, perfil y privacidad | Transversal |
| E2 | Registro de producción offline | OE 1 |
| E3 | Sincronización | OE 1 |
| E4 | Datos de mercado CENADA/SIMM | OE 2 |
| E5 | Alertas con IA | OE 2 |
| E6 | Vinculación productor-comprador | OE 3 |
| E7 | Calidad, UX y cierre | Transversal |

### Product Backlog inicial (todas las historias de usuario)

| ID | Épica | Historia de usuario | Prioridad | SP | Sprint | Resp. |
|----|-------|---------------------|-----------|:--:|:------:|:-----:|
| HU-01 | E1 | Como productor, quiero crear mi cuenta e iniciar sesión, para acceder a mi información de forma segura. | Must | 3 | 1 | F |
| HU-02 | E1 | Como productor, quiero registrar mi perfil (nombre, zona y cultivos de interés), para recibir información adaptada a mí. | Must | 2 | 1 | F |
| HU-03 | E2 | Como productor, quiero elegir mi cultivo desde un catálogo, para no escribirlo manualmente ni cometer errores. | Must | 2 | 1 | J |
| HU-08 | E7 | Como productor, quiero una interfaz con íconos y lenguaje claro, para usar la app aunque tenga poca experiencia digital. | Must | 3 | 1 | J |
| HU-16 | E4 | Como equipo, quiero documentar las condiciones de uso de los datos del CENADA/SIMM, para usarlos de forma autorizada. | Must | 2 | 1 | F |
| HU-27 | E1 | Como usuario, quiero aceptar un consentimiento sobre el uso de mis datos personales, para saber qué información se recolecta y cómo se usa. | Must | 3 | 1 | J |
| HU-28 | E7 | Como equipo, quiero configurar el repositorio, la arquitectura base y el flujo de trabajo, para construir de forma ordenada. | Must | 5 | 1 | Ambos |
| HU-29 | E7 | Como equipo, quiero validar mockups con productores de San Carlos, para confirmar el diseño antes de programar. | Must | 3 | 1 | J |
| HU-04 | E2 | Como productor, quiero registrar mi producción (cultivo, cantidad y fecha estimada de cosecha), para tener control de lo que voy a cosechar. | Must | 5 | 2 | J |
| HU-05 | E2 | Como productor, quiero ver el listado de mi producción registrada, para consultarla rápidamente. | Must | 3 | 2 | J |
| HU-06 | E2 | Como productor, quiero editar o eliminar un registro, para corregir errores o cambios. | Should | 3 | 2 | J |
| HU-07 | E2 | Como productor, quiero registrar y consultar mi producción sin Internet, para usar la app en el campo. | Must | 5 | 2 | F |
| HU-12 | E4 | Como sistema, quiero obtener los precios publicados por CENADA/SIMM, para alimentar el análisis de IA. | Must | 8 | 2 | F |
| HU-15 | E4 | Como equipo, quiero que la ingesta tolere cambios de formato en la fuente, para que el motor de IA no se rompa. | Should | 3 | 2 | F |
| HU-09 | E3 | Como productor, quiero que mis datos se sincronicen automáticamente al recuperar conexión, para no perder información. | Must | 8 | 3 | F |
| HU-10 | E3 | Como productor, quiero ver el estado de sincronización, para saber si mis datos están al día. | Should | 2 | 3 | J |
| HU-13 | E4 | Como sistema, quiero almacenar el histórico de precios por producto, para analizar tendencias y estacionalidad. | Must | 5 | 3 | F |
| HU-14 | E4 | Como productor, quiero consultar los precios actuales de mi cultivo, incluso sin conexión, para decidir cuándo vender. | Must | 3 | 3 | J |
| HU-17 | E5 | Como sistema, quiero analizar tendencias y estacionalidad de precios por cultivo, para generar recomendaciones de comercialización. | Must | 8 | 3 | J |
| HU-11 | E3 | Como productor, quiero que los conflictos entre datos locales y del servidor se resuelvan sin perder información, para confiar en la app. | Should | 5 | 4 | F |
| HU-18 | E5 | Como productor, quiero recibir alertas personalizadas según mi cultivo y fecha estimada de cosecha, para vender en el mejor momento. | Must | 8 | 4 | J |
| HU-19 | E5 | Como productor, quiero recibir notificaciones de las alertas, para enterarme a tiempo. | Must | 5 | 4 | F |
| HU-23 | E6 | Como comprador, quiero registrarme indicando los productos que necesito, para encontrar proveedores. | Must | 5 | 4 | F |
| HU-24 | E6 | Como comprador, quiero publicar una demanda (cultivo, cantidad y fecha), para que los productores la vean. | Must | 3 | 4 | F |
| HU-20 | E5 | Como productor, quiero configurar qué alertas recibir y con qué frecuencia, para evitar saturación. | Should | 3 | 5 | J |
| HU-25 | E6 | Como productor, quiero ver compradores cuya demanda coincide con mi producción, para contactarlos directamente. | Must | 8 | 5 | J |
| HU-26 | E6 | Como productor, quiero expresar interés en una demanda y contactar al comprador, para concretar la venta fuera de la app. | Must | 3 | 5 | J |
| HU-30 | E7 | Como equipo, quiero ejecutar pruebas de usabilidad con un grupo piloto de productores, para ajustar la app antes del cierre. | Must | 5 | 5 | J |
| HU-31 | E7 | Como equipo, quiero ejecutar pruebas funcionales y verificar la Definition of Done, para entregar un producto estable. | Must | 5 | 5 | F |
| HU-32 | E7 | Como usuario, quiero un manual breve de uso, para aprender a usar la app. | Should | 3 | 5 | F |
| HU-33 | E7 | Como equipo, quiero preparar la demo y el cierre del proyecto, para presentar resultados al docente. | Must | 2 | 5 | Ambos |
| HU-21 | E5 | Como productor, quiero ver por qué se generó una alerta, para confiar en la recomendación. | Could | 3 | Stretch S5 | J |
| HU-22 | E5 | Como productor, quiero indicar si una alerta me fue útil, para mejorar futuras alertas. | Could | 2 | Stretch S5 | J |

**Total:** 33 historias · 131 SP comprometidos en 5 sprints + 5 SP en stretch (136 SP en total).

### Distribución por sprint

| Sprint | Semanas | Historias | SP comprometidos |
|--------|---------|-----------|:----------------:|
| 1 | 1-2 | HU-01, 02, 03, 08, 16, 27, 28, 29 | 23 |
| 2 | 3-4 | HU-04, 05, 06, 07, 12, 15 | 27 |
| 3 | 5-6 | HU-09, 10, 13, 14, 17 | 26 |
| 4 | 7-8 | HU-11, 18, 19, 23, 24 | 26 |
| 5 | 9-10 | HU-20, 25, 26, 30, 31, 32, 33 (+ stretch HU-21, 22) | 29 (+5 stretch) |
| **Total** | | **31 historias + 2 stretch** | **131 (+5 stretch)** |

> La velocidad real se calibrará al cierre del Sprint 1. Si hay desviación, el alcance (no la fecha) se ajusta, moviendo primero las historias Should y Could.

### Sprint Backlog — Sprint 1

| HU | Tarea principal | SP | Resp. |
|----|-----------------|:--:|:-----:|
| HU-28 | Repositorio, ramas, arquitectura base y app ejecutándose | 5 | Ambos |
| HU-01 | Registro e inicio de sesión | 3 | F |
| HU-02 | Perfil del productor | 2 | F |
| HU-03 | Catálogo de cultivos | 2 | J |
| HU-08 | Guía de estilo: íconos, tamaños de letra y textos simples | 3 | J |
| HU-16 | Documento de condiciones de uso de datos CENADA/SIMM | 2 | F |
| HU-27 | Pantalla de consentimiento de datos personales | 3 | J |
| HU-29 | Mockups validados con productores | 3 | J |
| **Total** | | **23** | |

---

## 06. Alcance, Product Backlog priorizado y criterios de aceptación

### Alcance

| Dentro del alcance | Fuera del alcance |
|--------------------|-------------------|
| App móvil con registro de producción y modo offline | Pagos o transacciones monetarias |
| Análisis de precios CENADA/SIMM y alertas con IA | Logística y contratación de transporte |
| Registro de compradores y coincidencias | Comercio electrónico completo |
| Notificaciones al productor | Operación en producción tras el cierre del curso |

### Priorización

El Product Backlog se prioriza con MoSCoW (columna *Prioridad* de la sección 05). Si el tiempo no alcanza, se ajusta el alcance moviendo primero las historias **Could** (HU-21, HU-22) y luego las **Should**.

### Historias de usuario detalladas y criterios de aceptación

Cada historia sigue el formato **Como / Quiero / Para**, con criterios de aceptación en formato **Dado / cuando / entonces**.

> **Convenciones:** Prioridad MoSCoW → Must have (Alta), Should have (Media), Could have (Baja). Estimación en puntos de historia (Fibonacci). Lo que desarrolla uno lo prueba el otro.

### Sprint 1 (semanas 1-2)

#### HU-01: Creación de cuenta e inicio de sesión del productor

| Campo | Detalle |
|-------|---------|
| **Título** | Creación de cuenta e inicio de sesión del productor |
| **Historia de usuario** | **Como** productor,<br>**Quiero** crear mi cuenta e iniciar sesión,<br>**Para** acceder a mi información de forma segura. |
| **Criterios de aceptación** | 1. **Dado** que soy un productor que aún no tiene cuenta, **cuando** completo el formulario de registro con datos válidos, **entonces** el sistema crea mi cuenta y me permite ingresar a la aplicación.<br>2. **Dado** que tengo una cuenta registrada, **cuando** inicio sesión con mis credenciales correctas, **entonces** el sistema me da acceso a mi información.<br>3. **Dado** que ingreso credenciales incorrectas o dejo campos vacíos, **cuando** intento registrarme o iniciar sesión, **entonces** el sistema muestra un mensaje de error claro que me indica cómo corregirlo.<br>4. **Dado** que me registro en la aplicación, **cuando** el sistema guarda mi contraseña, **entonces** esta no se almacena en texto plano. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E1 – Cuenta, perfil y privacidad |
| **Dependencias** | HU-28 (repositorio, arquitectura base y app ejecutándose) |
| **Notas adicionales** | Diseños: mockups de la pantalla de registro e inicio de sesión, a validar en HU-29. |

#### HU-02: Registro del perfil del productor

| Campo | Detalle |
|-------|---------|
| **Título** | Registro del perfil del productor |
| **Historia de usuario** | **Como** productor,<br>**Quiero** registrar mi perfil (nombre, zona y cultivos de interés),<br>**Para** recibir información adaptada a mí. |
| **Criterios de aceptación** | 1. **Dado** que inicié sesión como productor, **cuando** completo mi nombre, zona y cultivos de interés y guardo, **entonces** el sistema almacena mi perfil.<br>2. **Dado** que ya registré mi perfil, **cuando** lo consulto posteriormente, **entonces** el sistema me muestra los datos que guardé.<br>3. **Dado** que dejo vacío un dato obligatorio del perfil, **cuando** intento guardar, **entonces** el sistema muestra un mensaje claro que indica qué dato falta. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E1 – Cuenta, perfil y privacidad |
| **Dependencias** | HU-01 (el productor debe haber iniciado sesión) |
| **Notas adicionales** | Relacionada con HU-03 (catálogo de cultivos), que puede usarse para elegir los cultivos de interés. |

#### HU-03: Selección de cultivo desde un catálogo

| Campo | Detalle |
|-------|---------|
| **Título** | Selección de cultivo desde un catálogo |
| **Historia de usuario** | **Como** productor,<br>**Quiero** elegir mi cultivo desde un catálogo,<br>**Para** no escribirlo manualmente ni cometer errores. |
| **Criterios de aceptación** | 1. **Dado** que necesito indicar un cultivo, **cuando** abro el catálogo, **entonces** el sistema muestra los cultivos principales de la zona.<br>2. **Dado** que estoy viendo el catálogo, **cuando** selecciono un cultivo, **entonces** el sistema lo registra como elegido sin que tenga que escribirlo.<br>3. **Dado** que el catálogo tiene varios cultivos, **cuando** lo recorro, **entonces** cada cultivo se muestra con nombre e ícono fácil de reconocer. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E2 – Registro de producción offline |
| **Dependencias** | HU-28 (arquitectura base) |
| **Notas adicionales** | Lo usan HU-02 (cultivos de interés) y HU-04 (registro de producción). Debe estar disponible sin conexión. |

#### HU-08: Interfaz con íconos y lenguaje claro

| Campo | Detalle |
|-------|---------|
| **Título** | Interfaz con íconos y lenguaje claro |
| **Historia de usuario** | **Como** productor,<br>**Quiero** una interfaz con íconos y lenguaje claro,<br>**Para** usar la app aunque tenga poca experiencia digital. |
| **Criterios de aceptación** | 1. **Dado** que el equipo diseña las pantallas, **cuando** se define la guía de estilo, **entonces** esta incluye íconos, tamaños de letra mínimos y textos simples.<br>2. **Dado** que existe la guía de estilo, **cuando** se revisan las pantallas base, **entonces** todas aplican esa guía.<br>3. **Dado** que soy un productor con poca experiencia digital, **cuando** uso las pantallas base, **entonces** puedo identificar cada acción por su ícono y texto sin términos técnicos. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | Se valida junto con HU-29 (mockups con productores) |
| **Notas adicionales** | La guía de estilo aplica a todas las pantallas que se construyan en sprints posteriores. |

#### HU-16: Documentación de condiciones de uso de datos CENADA/SIMM

| Campo | Detalle |
|-------|---------|
| **Título** | Documentación de condiciones de uso de datos CENADA/SIMM |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** documentar las condiciones de uso de los datos del CENADA/SIMM,<br>**Para** usarlos de forma autorizada. |
| **Criterios de aceptación** | 1. **Dado** que el proyecto usará datos del CENADA/SIMM, **cuando** se investiga la fuente, **entonces** se documenta la fuente oficial de los datos.<br>2. **Dado** que se revisó la fuente, **cuando** se completa el documento, **entonces** este incluye la licencia o condiciones de uso.<br>3. **Dado** que el documento está completo, **cuando** se consulta, **entonces** indica la frecuencia de actualización de los datos. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E4 – Datos de mercado CENADA/SIMM |
| **Dependencias** | Ninguna |
| **Notas adicionales** | Requisito previo de HU-12 (ingesta de precios). Parte de la estrategia de involucramiento con el interesado crítico CENADA/PIMA. |

#### HU-27: Consentimiento de uso de datos personales

| Campo | Detalle |
|-------|---------|
| **Título** | Consentimiento de uso de datos personales |
| **Historia de usuario** | **Como** usuario,<br>**Quiero** aceptar un consentimiento sobre el uso de mis datos personales,<br>**Para** saber qué información se recolecta y cómo se usa. |
| **Criterios de aceptación** | 1. **Dado** que abro la aplicación por primera vez, **cuando** intento usarla, **entonces** el sistema muestra obligatoriamente la pantalla de consentimiento.<br>2. **Dado** que leo el consentimiento, **cuando** lo acepto, **entonces** el sistema registra la aceptación y me permite continuar.<br>3. **Dado** que no acepto el consentimiento, **cuando** intento continuar, **entonces** el sistema no me permite usar la aplicación. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E1 – Cuenta, perfil y privacidad |
| **Dependencias** | HU-28 (arquitectura base) |
| **Notas adicionales** | Responde al EEF de normativa de protección de datos personales. Texto con lenguaje claro según HU-08. |

#### HU-28: Configuración del repositorio y arquitectura base

| Campo | Detalle |
|-------|---------|
| **Título** | Configuración del repositorio y arquitectura base |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** configurar el repositorio, la arquitectura base y el flujo de trabajo,<br>**Para** construir de forma ordenada. |
| **Criterios de aceptación** | 1. **Dado** que el proyecto inicia, **cuando** se configura el repositorio, **entonces** este queda creado con las ramas definidas.<br>2. **Dado** que se define la arquitectura, **cuando** se documenta, **entonces** la arquitectura base queda registrada en el repositorio.<br>3. **Dado** que la base está configurada, **cuando** se ejecuta la app, **entonces** esta corre en un dispositivo o emulador. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Joshua y Fabio / Revisión cruzada |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | Ninguna |
| **Notas adicionales** | Base para el resto de historias. La arquitectura debe contemplar el enfoque offline-first. |

#### HU-29: Validación de mockups con productores

| Campo | Detalle |
|-------|---------|
| **Título** | Validación de mockups con productores |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** validar mockups con productores de San Carlos,<br>**Para** confirmar el diseño antes de programar. |
| **Criterios de aceptación** | 1. **Dado** que existen mockups de las pantallas clave, **cuando** se presentan a productores, **entonces** son revisados por al menos 3 productores.<br>2. **Dado** que los productores dieron retroalimentación, **cuando** se analiza, **entonces** los ajustes acordados quedan documentados.<br>3. **Dado** que se documentaron los ajustes, **cuando** se actualizan los mockups, **entonces** la versión final se usa como referencia para el desarrollo. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 1 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | HU-08 (guía de estilo) |
| **Notas adicionales** | Cubre las pantallas de HU-01, HU-02, HU-03 y HU-27. Parte de la estrategia de involucramiento con los pequeños productores. |

### Sprint 2 (semanas 3-4)

#### HU-04: Registro de producción

| Campo | Detalle |
|-------|---------|
| **Título** | Registro de producción |
| **Historia de usuario** | **Como** productor,<br>**Quiero** registrar mi producción (cultivo, cantidad y fecha estimada de cosecha),<br>**Para** tener control de lo que voy a cosechar. |
| **Criterios de aceptación** | 1. **Dado** que inicié sesión, **cuando** registro cultivo, cantidad y fecha estimada de cosecha y guardo, **entonces** el sistema almacena el registro.<br>2. **Dado** que dejo un campo vacío, **cuando** intento guardar, **entonces** el sistema muestra un mensaje claro que indica qué dato falta.<br>3. **Dado** que ingreso una fecha inválida, **cuando** intento guardar, **entonces** el sistema rechaza el registro y me indica cómo corregirlo. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E2 – Registro de producción offline |
| **Dependencias** | HU-02 (perfil), HU-03 (catálogo de cultivos) |
| **Notas adicionales** | Insumo principal de las alertas (HU-18) y de la vinculación con compradores (HU-25). |

#### HU-05: Listado de producción registrada

| Campo | Detalle |
|-------|---------|
| **Título** | Listado de producción registrada |
| **Historia de usuario** | **Como** productor,<br>**Quiero** ver el listado de mi producción registrada,<br>**Para** consultarla rápidamente. |
| **Criterios de aceptación** | 1. **Dado** que tengo registros de producción, **cuando** abro el listado, **entonces** el sistema muestra todos mis registros.<br>2. **Dado** que veo el listado, **cuando** reviso el orden, **entonces** los registros aparecen ordenados por fecha de cosecha.<br>3. **Dado** que no tengo registros, **cuando** abro el listado, **entonces** el sistema muestra un mensaje que me invita a registrar mi producción. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E2 – Registro de producción offline |
| **Dependencias** | HU-04 (registro de producción) |
| **Notas adicionales** | Solo se muestran los registros del usuario que inició sesión. |

#### HU-06: Edición y eliminación de registros

| Campo | Detalle |
|-------|---------|
| **Título** | Edición y eliminación de registros |
| **Historia de usuario** | **Como** productor,<br>**Quiero** editar o eliminar un registro,<br>**Para** corregir errores o cambios. |
| **Criterios de aceptación** | 1. **Dado** que tengo un registro de producción, **cuando** lo edito y guardo, **entonces** el sistema actualiza los datos.<br>2. **Dado** que quiero eliminar un registro, **cuando** selecciono eliminar, **entonces** el sistema me pide confirmación antes de borrarlo.<br>3. **Dado** que confirmé la eliminación, **cuando** vuelvo al listado, **entonces** el registro ya no aparece. |
| **Prioridad** | Should have (Media) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E2 – Registro de producción offline |
| **Dependencias** | HU-04 (registro), HU-05 (listado) |
| **Notas adicionales** | Al editar se aplican las mismas validaciones de HU-04. |

#### HU-07: Registro y consulta de producción sin Internet

| Campo | Detalle |
|-------|---------|
| **Título** | Registro y consulta de producción sin Internet |
| **Historia de usuario** | **Como** productor,<br>**Quiero** registrar y consultar mi producción sin Internet,<br>**Para** usar la app en el campo. |
| **Criterios de aceptación** | 1. **Dado** que mi dispositivo no tiene conexión, **cuando** creo un registro de producción, **entonces** el sistema lo guarda localmente.<br>2. **Dado** que no tengo conexión, **cuando** abro el listado o edito un registro, **entonces** puedo ver y modificar mis registros.<br>3. **Dado** que guardé registros sin conexión, **cuando** cierro y vuelvo a abrir la app, **entonces** los datos siguen disponibles. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E2 – Registro de producción offline |
| **Dependencias** | HU-04 (registro), HU-05 (listado) |
| **Notas adicionales** | Núcleo del enfoque offline-first. La sincronización con el servidor se aborda en HU-09. |

#### HU-12: Obtención de precios CENADA/SIMM

| Campo | Detalle |
|-------|---------|
| **Título** | Obtención de precios CENADA/SIMM |
| **Historia de usuario** | **Como** sistema,<br>**Quiero** obtener los precios publicados por CENADA/SIMM,<br>**Para** alimentar el análisis de IA. |
| **Criterios de aceptación** | 1. **Dado** que hay precios publicados en la fuente, **cuando** se ejecuta el proceso de ingesta, **entonces** el sistema descarga y almacena los precios.<br>2. **Dado** que se completó una carga, **cuando** se consulta su registro, **entonces** se indica la fecha y la fuente de esa carga.<br>3. **Dado** que la fuente no está disponible, **cuando** se ejecuta la ingesta, **entonces** el sistema registra el error y conserva los datos previos. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 8 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E4 – Datos de mercado CENADA/SIMM |
| **Dependencias** | HU-16 (condiciones de uso de los datos) |
| **Notas adicionales** | Insumo de HU-13 (histórico) y HU-17 (análisis de tendencias). Riesgo externo: cambios de acceso o formato de la fuente. |

#### HU-15: Ingesta tolerante a cambios de formato

| Campo | Detalle |
|-------|---------|
| **Título** | Ingesta tolerante a cambios de formato |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** que la ingesta tolere cambios de formato en la fuente,<br>**Para** que el motor de IA no se rompa. |
| **Criterios de aceptación** | 1. **Dado** que la fuente cambia su formato, **cuando** se ejecuta la ingesta, **entonces** el proceso falla de forma controlada sin detener la aplicación.<br>2. **Dado** que la ingesta falló por formato, **cuando** se revisan los registros, **entonces** el error queda registrado con su detalle.<br>3. **Dado** que la ingesta falló, **cuando** se consultan los precios, **entonces** el sistema conserva y muestra los datos previos. |
| **Prioridad** | Should have (Media) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 2 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E4 – Datos de mercado CENADA/SIMM |
| **Dependencias** | HU-12 (ingesta de precios) |
| **Notas adicionales** | Plan de contingencia definido para el interesado crítico CENADA/PIMA. |

### Sprint 3 (semanas 5-6)

#### HU-09: Sincronización automática al recuperar conexión

| Campo | Detalle |
|-------|---------|
| **Título** | Sincronización automática al recuperar conexión |
| **Historia de usuario** | **Como** productor,<br>**Quiero** que mis datos se sincronicen automáticamente al recuperar conexión,<br>**Para** no perder información. |
| **Criterios de aceptación** | 1. **Dado** que creé registros sin conexión, **cuando** el dispositivo detecta conexión, **entonces** el sistema envía esos registros al servidor automáticamente.<br>2. **Dado** que la sincronización se completó, **cuando** reviso los datos en el servidor, **entonces** no existen registros duplicados.<br>3. **Dado** que la conexión se pierde durante la sincronización, **cuando** vuelve la conexión, **entonces** el sistema reintenta sin perder datos. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 8 puntos de historia |
| **Sprint** | 3 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E3 – Sincronización |
| **Dependencias** | HU-07 (registro offline) |
| **Notas adicionales** | La resolución de conflictos se aborda en HU-11. |

#### HU-10: Estado de sincronización visible

| Campo | Detalle |
|-------|---------|
| **Título** | Estado de sincronización visible |
| **Historia de usuario** | **Como** productor,<br>**Quiero** ver el estado de sincronización,<br>**Para** saber si mis datos están al día. |
| **Criterios de aceptación** | 1. **Dado** que mis datos están al día, **cuando** veo el indicador, **entonces** muestra "sincronizado".<br>2. **Dado** que tengo registros sin enviar, **cuando** veo el indicador, **entonces** muestra "pendiente".<br>3. **Dado** que la sincronización falló, **cuando** veo el indicador, **entonces** muestra "error". |
| **Prioridad** | Should have (Media) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | 3 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E3 – Sincronización |
| **Dependencias** | HU-09 (sincronización) |
| **Notas adicionales** | El indicador debe seguir la guía de estilo de HU-08 (ícono + texto simple). |

#### HU-13: Histórico de precios por producto

| Campo | Detalle |
|-------|---------|
| **Título** | Histórico de precios por producto |
| **Historia de usuario** | **Como** sistema,<br>**Quiero** almacenar el histórico de precios por producto,<br>**Para** analizar tendencias y estacionalidad. |
| **Criterios de aceptación** | 1. **Dado** que se cargan precios nuevos, **cuando** termina la ingesta, **entonces** se agregan al histórico sin borrar los anteriores.<br>2. **Dado** que existe histórico, **cuando** se consulta por producto, **entonces** se obtienen sus precios registrados.<br>3. **Dado** que existe histórico, **cuando** se consulta por rango de fechas, **entonces** se obtienen solo los precios de ese rango. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 3 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E4 – Datos de mercado CENADA/SIMM |
| **Dependencias** | HU-12 (ingesta de precios) |
| **Notas adicionales** | Insumo directo de HU-17 (análisis de tendencias). |

#### HU-14: Consulta de precios actuales del cultivo

| Campo | Detalle |
|-------|---------|
| **Título** | Consulta de precios actuales del cultivo |
| **Historia de usuario** | **Como** productor,<br>**Quiero** consultar los precios actuales de mi cultivo, incluso sin conexión,<br>**Para** decidir cuándo vender. |
| **Criterios de aceptación** | 1. **Dado** que tengo un cultivo registrado, **cuando** consulto su precio, **entonces** el sistema muestra el último precio disponible.<br>2. **Dado** que veo el precio, **cuando** reviso el detalle, **entonces** aparece la fecha de la última actualización.<br>3. **Dado** que no tengo conexión, **cuando** consulto el precio, **entonces** el sistema muestra el último precio guardado en el dispositivo. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 3 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E4 – Datos de mercado CENADA/SIMM |
| **Dependencias** | HU-13 (histórico de precios), HU-07 (almacenamiento offline) |
| **Notas adicionales** | Mostrar la fecha evita que el productor tome decisiones con precios desactualizados. |

#### HU-17: Análisis de tendencias y estacionalidad de precios

| Campo | Detalle |
|-------|---------|
| **Título** | Análisis de tendencias y estacionalidad de precios |
| **Historia de usuario** | **Como** sistema,<br>**Quiero** analizar tendencias y estacionalidad de precios por cultivo,<br>**Para** generar recomendaciones de comercialización. |
| **Criterios de aceptación** | 1. **Dado** que existe histórico suficiente de un cultivo, **cuando** se ejecuta el análisis, **entonces** el modelo identifica la tendencia (sube, baja o estable).<br>2. **Dado** que existe histórico suficiente, **cuando** se ejecuta el análisis, **entonces** el modelo identifica la estacionalidad del cultivo.<br>3. **Dado** que un cultivo no tiene datos suficientes, **cuando** se ejecuta el análisis, **entonces** el sistema lo indica en lugar de generar un resultado poco confiable.<br>4. **Dado** que el análisis se ejecutó, **cuando** se revisan los resultados, **entonces** quedan documentados para los cultivos del catálogo. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 8 puntos de historia |
| **Sprint** | 3 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-13 (histórico de precios) |
| **Notas adicionales** | Componente experimental; su precisión se ajusta iterativamente. Base de HU-18 (alertas). |

### Sprint 4 (semanas 7-8)

#### HU-11: Resolución de conflictos de sincronización

| Campo | Detalle |
|-------|---------|
| **Título** | Resolución de conflictos de sincronización |
| **Historia de usuario** | **Como** productor,<br>**Quiero** que los conflictos entre datos locales y del servidor se resuelvan sin perder información,<br>**Para** confiar en la app. |
| **Criterios de aceptación** | 1. **Dado** que un mismo registro se modificó desde dos fuentes, **cuando** se sincroniza, **entonces** el sistema aplica una regla definida (p. ej. última modificación).<br>2. **Dado** que se resolvió un conflicto, **cuando** reviso el registro, **entonces** no se perdió información.<br>3. **Dado** que ocurrió un conflicto, **cuando** se revisan los registros del sistema, **entonces** queda constancia de cómo se resolvió. |
| **Prioridad** | Should have (Media) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 4 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E3 – Sincronización |
| **Dependencias** | HU-09 (sincronización) |
| **Notas adicionales** | La regla de resolución debe documentarse en la arquitectura. |

#### HU-18: Alertas personalizadas de comercialización

| Campo | Detalle |
|-------|---------|
| **Título** | Alertas personalizadas de comercialización |
| **Historia de usuario** | **Como** productor,<br>**Quiero** recibir alertas personalizadas según mi cultivo y fecha estimada de cosecha,<br>**Para** vender en el mejor momento. |
| **Criterios de aceptación** | 1. **Dado** que tengo una producción registrada y existen tendencias de su cultivo, **cuando** el sistema detecta una oportunidad, **entonces** genera una alerta.<br>2. **Dado** que se generó una alerta, **cuando** la veo, **entonces** incluye el cultivo, un mensaje claro y el momento sugerido para vender.<br>3. **Dado** que mi cultivo no tiene datos suficientes, **cuando** se evalúan alertas, **entonces** el sistema no genera alertas sin respaldo. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 8 puntos de historia |
| **Sprint** | 4 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-04 (registro de producción), HU-17 (análisis de tendencias) |
| **Notas adicionales** | Historia central del valor del producto (OE 2). |

#### HU-19: Notificaciones de alertas

| Campo | Detalle |
|-------|---------|
| **Título** | Notificaciones de alertas |
| **Historia de usuario** | **Como** productor,<br>**Quiero** recibir notificaciones de las alertas,<br>**Para** enterarme a tiempo. |
| **Criterios de aceptación** | 1. **Dado** que se generó una alerta y tengo conexión, **cuando** se envía, **entonces** llega como notificación a mi dispositivo.<br>2. **Dado** que se generó una alerta y no tengo conexión, **cuando** abro la app, **entonces** el sistema me muestra la alerta pendiente.<br>3. **Dado** que toco una notificación, **cuando** se abre la app, **entonces** me lleva al detalle de la alerta. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 4 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-18 (alertas personalizadas) |
| **Notas adicionales** | Configuración de tipos y frecuencia en HU-20. |

#### HU-23: Registro de compradores

| Campo | Detalle |
|-------|---------|
| **Título** | Registro de compradores |
| **Historia de usuario** | **Como** comprador,<br>**Quiero** registrarme indicando los productos que necesito,<br>**Para** encontrar proveedores. |
| **Criterios de aceptación** | 1. **Dado** que soy un comprador sin cuenta, **cuando** completo nombre, tipo de comprador y productos de interés, **entonces** el sistema crea mi cuenta.<br>2. **Dado** que dejo un dato obligatorio vacío, **cuando** intento registrarme, **entonces** el sistema muestra un mensaje claro que indica qué falta.<br>3. **Dado** que ya me registré, **cuando** consulto mi perfil, **entonces** veo los productos de interés que indiqué. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 4 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E6 – Vinculación productor-comprador |
| **Dependencias** | HU-01 (mecanismo de cuentas), HU-03 (catálogo de cultivos) |
| **Notas adicionales** | Aplica el mismo consentimiento de datos de HU-27. |

#### HU-24: Publicación de demandas del comprador

| Campo | Detalle |
|-------|---------|
| **Título** | Publicación de demandas del comprador |
| **Historia de usuario** | **Como** comprador,<br>**Quiero** publicar una demanda (cultivo, cantidad y fecha),<br>**Para** que los productores la vean. |
| **Criterios de aceptación** | 1. **Dado** que inicié sesión como comprador, **cuando** publico una demanda con cultivo, cantidad y fecha, **entonces** el sistema la guarda y la deja visible para productores.<br>2. **Dado** que tengo una demanda publicada, **cuando** la edito, **entonces** el sistema actualiza sus datos.<br>3. **Dado** que tengo una demanda publicada, **cuando** la cierro, **entonces** deja de mostrarse a los productores. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 4 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E6 – Vinculación productor-comprador |
| **Dependencias** | HU-23 (registro de compradores) |
| **Notas adicionales** | Insumo de HU-25 (coincidencias). |

### Sprint 5 (semanas 9-10)

#### HU-20: Configuración de alertas

| Campo | Detalle |
|-------|---------|
| **Título** | Configuración de alertas |
| **Historia de usuario** | **Como** productor,<br>**Quiero** configurar qué alertas recibir y con qué frecuencia,<br>**Para** evitar saturación. |
| **Criterios de aceptación** | 1. **Dado** que estoy en la configuración, **cuando** activo o desactivo un tipo de alerta, **entonces** el sistema respeta mi elección.<br>2. **Dado** que estoy en la configuración, **cuando** elijo una frecuencia, **entonces** las alertas se envían según esa frecuencia.<br>3. **Dado** que guardé mi configuración, **cuando** vuelvo a abrir la app, **entonces** la configuración se mantiene. |
| **Prioridad** | Should have (Media) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-18 (alertas), HU-19 (notificaciones) |
| **Notas adicionales** | Candidata a moverse si el sprint se atrasa (prioridad Should). |

#### HU-25: Coincidencias entre producción y demanda

| Campo | Detalle |
|-------|---------|
| **Título** | Coincidencias entre producción y demanda |
| **Historia de usuario** | **Como** productor,<br>**Quiero** ver compradores cuya demanda coincide con mi producción,<br>**Para** contactarlos directamente. |
| **Criterios de aceptación** | 1. **Dado** que tengo producción registrada y existen demandas publicadas, **cuando** consulto coincidencias, **entonces** el sistema lista las demandas compatibles por cultivo, cantidad aproximada y fecha.<br>2. **Dado** que hay varias coincidencias, **cuando** veo el listado, **entonces** aparecen ordenadas por relevancia.<br>3. **Dado** que no hay demandas compatibles, **cuando** consulto coincidencias, **entonces** el sistema me lo indica con un mensaje claro. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 8 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E6 – Vinculación productor-comprador |
| **Dependencias** | HU-04 (registro de producción), HU-24 (demandas publicadas) |
| **Notas adicionales** | Historia central del OE 3. |

#### HU-26: Expresar interés y contactar al comprador

| Campo | Detalle |
|-------|---------|
| **Título** | Expresar interés y contactar al comprador |
| **Historia de usuario** | **Como** productor,<br>**Quiero** expresar interés en una demanda y contactar al comprador,<br>**Para** concretar la venta fuera de la app. |
| **Criterios de aceptación** | 1. **Dado** que veo una demanda compatible, **cuando** marco interés, **entonces** el sistema registra mi interés.<br>2. **Dado** que marqué interés, **cuando** se procesa, **entonces** el comprador recibe un aviso con mis datos de contacto autorizados.<br>3. **Dado** que ya marqué interés en una demanda, **cuando** la vuelvo a ver, **entonces** el sistema indica que ya expresé interés. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E6 – Vinculación productor-comprador |
| **Dependencias** | HU-25 (coincidencias) |
| **Notas adicionales** | La venta se concreta fuera de la app; pagos y transacciones están fuera del alcance. Solo se comparten datos autorizados según HU-27. |

#### HU-30: Pruebas de usabilidad con grupo piloto

| Campo | Detalle |
|-------|---------|
| **Título** | Pruebas de usabilidad con grupo piloto |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** ejecutar pruebas de usabilidad con un grupo piloto de productores,<br>**Para** ajustar la app antes del cierre. |
| **Criterios de aceptación** | 1. **Dado** que la app tiene sus funciones principales, **cuando** se prueba con un grupo piloto de productores, **entonces** se registran los resultados.<br>2. **Dado** que se obtuvieron resultados, **cuando** se analizan, **entonces** las mejoras identificadas quedan documentadas.<br>3. **Dado** que hay ajustes críticos, **cuando** se cierra la prueba, **entonces** esos ajustes quedan aplicados. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | Incrementos de los Sprints 1 a 4 |
| **Notas adicionales** | Parte de la estrategia de involucramiento con los pequeños productores. |

#### HU-31: Pruebas funcionales y verificación de la DoD

| Campo | Detalle |
|-------|---------|
| **Título** | Pruebas funcionales y verificación de la DoD |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** ejecutar pruebas funcionales y verificar la Definition of Done,<br>**Para** entregar un producto estable. |
| **Criterios de aceptación** | 1. **Dado** que existen casos de prueba, **cuando** se ejecutan, **entonces** sus resultados quedan registrados.<br>2. **Dado** que se encontraron defectos críticos, **cuando** se cierra el sprint, **entonces** esos defectos están resueltos.<br>3. **Dado** que las historias están terminadas, **cuando** QA revisa, **entonces** se verifica el cumplimiento de la Definition of Done. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 5 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | Historias funcionales del Sprint 5 |
| **Notas adicionales** | La Definition of Done se detalla en la sección 09 del expediente. |

#### HU-32: Manual breve de uso

| Campo | Detalle |
|-------|---------|
| **Título** | Manual breve de uso |
| **Historia de usuario** | **Como** usuario,<br>**Quiero** un manual breve de uso,<br>**Para** aprender a usar la app. |
| **Criterios de aceptación** | 1. **Dado** que la app está terminada, **cuando** se elabora el manual, **entonces** este cubre las funciones principales.<br>2. **Dado** que el manual está listo, **cuando** lo consulto, **entonces** incluye capturas de pantalla de cada función.<br>3. **Dado** que soy un productor con poca experiencia digital, **cuando** leo el manual, **entonces** está escrito con lenguaje claro. |
| **Prioridad** | Should have (Media) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Fabio / Lo prueba Joshua |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | Funciones principales terminadas |
| **Notas adicionales** | Sigue la guía de lenguaje de HU-08. |

#### HU-33: Demo y cierre del proyecto

| Campo | Detalle |
|-------|---------|
| **Título** | Demo y cierre del proyecto |
| **Historia de usuario** | **Como** equipo,<br>**Quiero** preparar la demo y el cierre del proyecto,<br>**Para** presentar resultados al docente. |
| **Criterios de aceptación** | 1. **Dado** que el producto está estable, **cuando** se prepara la demo, **entonces** esta muestra las funciones principales.<br>2. **Dado** que la demo está lista, **cuando** se presenta, **entonces** el docente la recibe en la fecha del hito.<br>3. **Dado** que se cierra el proyecto, **cuando** se revisa la entrega, **entonces** el documento final y el repositorio están actualizados. |
| **Prioridad** | Must have (Alta) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | 5 |
| **Responsable** | Joshua y Fabio / Revisión cruzada |
| **Épica** | E7 – Calidad, UX y cierre |
| **Dependencias** | HU-30, HU-31, HU-32 |
| **Notas adicionales** | Cierre ante el interesado crítico Docente ISW-912. |

### Stretch (Sprint 5, solo si el sprint va holgado)

#### HU-21: Explicación de las alertas

| Campo | Detalle |
|-------|---------|
| **Título** | Explicación de las alertas |
| **Historia de usuario** | **Como** productor,<br>**Quiero** ver por qué se generó una alerta,<br>**Para** confiar en la recomendación. |
| **Criterios de aceptación** | 1. **Dado** que recibí una alerta, **cuando** abro su detalle, **entonces** el sistema muestra en lenguaje claro el motivo (tendencia, estacionalidad o precio).<br>2. **Dado** que veo el motivo, **cuando** reviso el detalle, **entonces** se indica la fecha de los datos usados. |
| **Prioridad** | Could have (Baja) |
| **Estimación** | 3 puntos de historia |
| **Sprint** | Stretch S5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-18 (alertas personalizadas) |
| **Notas adicionales** | Primera historia en salir del alcance si falta tiempo. |

#### HU-22: Retroalimentación sobre la utilidad de las alertas

| Campo | Detalle |
|-------|---------|
| **Título** | Retroalimentación sobre la utilidad de las alertas |
| **Historia de usuario** | **Como** productor,<br>**Quiero** indicar si una alerta me fue útil,<br>**Para** mejorar futuras alertas. |
| **Criterios de aceptación** | 1. **Dado** que recibí una alerta, **cuando** indico si me fue útil, **entonces** el sistema registra mi respuesta.<br>2. **Dado** que ya respondí, **cuando** vuelvo a ver la alerta, **entonces** se muestra la respuesta que di. |
| **Prioridad** | Could have (Baja) |
| **Estimación** | 2 puntos de historia |
| **Sprint** | Stretch S5 |
| **Responsable** | Joshua / Lo prueba Fabio |
| **Épica** | E5 – Alertas con IA |
| **Dependencias** | HU-18 (alertas personalizadas) |
| **Notas adicionales** | Las respuestas pueden usarse para ajustar el modelo de HU-17. |

---

## 07. Planificación temporal, estimaciones y costos

### Matriz de Estimación

#### Escala e historia de referencia

- **Escala:** puntos de historia (SP) con Fibonacci (1, 2, 3, 5, 8), estimados por planning poker entre los dos integrantes.
- **Historia de referencia (3 SP):** HU-05 — Listado de producción registrada. Las demás historias se estiman comparándolas con ella.

#### Tabla de estimación

| ID | Historia (resumen) | SP | Prioridad | Dependencias |
|----|--------------------|:--:|-----------|--------------|
| HU-28 | Repositorio y arquitectura base | 5 | Must | Ninguna |
| HU-01 | Crear cuenta e iniciar sesión | 3 | Must | HU-28 |
| HU-02 | Perfil del productor | 2 | Must | HU-01 |
| HU-03 | Catálogo de cultivos | 2 | Must | HU-28 |
| HU-08 | Interfaz con íconos y lenguaje claro | 3 | Must | Se valida con HU-29 |
| HU-16 | Condiciones de uso de datos CENADA/SIMM | 2 | Must | Ninguna |
| HU-27 | Consentimiento de datos personales | 3 | Must | HU-28 |
| HU-29 | Validar mockups con productores | 3 | Must | HU-08 |
| HU-04 | Registro de producción | 5 | Must | HU-02, HU-03 |
| HU-05 | Listado de producción | 3 | Must | HU-04 |
| HU-06 | Editar y eliminar registros | 3 | Should | HU-04, HU-05 |
| HU-07 | Producción sin Internet | 5 | Must | HU-04, HU-05 |
| HU-12 | Obtención de precios CENADA/SIMM | 8 | Must | HU-16 |
| HU-15 | Ingesta tolerante a cambios de formato | 3 | Should | HU-12 |
| HU-09 | Sincronización automática | 8 | Must | HU-07 |
| HU-10 | Estado de sincronización | 2 | Should | HU-09 |
| HU-13 | Histórico de precios | 5 | Must | HU-12 |
| HU-14 | Precios actuales del cultivo | 3 | Must | HU-13, HU-07 |
| HU-17 | Tendencias y estacionalidad | 8 | Must | HU-13 |
| HU-11 | Conflictos de sincronización | 5 | Should | HU-09 |
| HU-18 | Alertas personalizadas | 8 | Must | HU-04, HU-17 |
| HU-19 | Notificaciones de alertas | 5 | Must | HU-18 |
| HU-23 | Registro de compradores | 5 | Must | HU-01, HU-03 |
| HU-24 | Publicación de demandas | 3 | Must | HU-23 |
| HU-20 | Configuración de alertas | 3 | Should | HU-18, HU-19 |
| HU-25 | Coincidencias producción-demanda | 8 | Must | HU-04, HU-24 |
| HU-26 | Expresar interés y contactar | 3 | Must | HU-25 |
| HU-30 | Pruebas de usabilidad (piloto) | 5 | Must | Incrementos S1-S4 |
| HU-31 | Pruebas funcionales y DoD | 5 | Must | Historias funcionales S5 |
| HU-32 | Manual breve de uso | 3 | Should | Funciones principales |
| HU-33 | Demo y cierre | 2 | Must | HU-30, HU-31, HU-32 |
| HU-21 | Explicación de las alertas | 3 | Could | HU-18 |
| HU-22 | Retroalimentación de alertas | 2 | Could | HU-18 |

#### Total del backlog y desglose por épica

| Épica | Historias | SP |
|-------|:---------:|:--:|
| E1 Cuenta, perfil y privacidad | 3 | 8 |
| E2 Registro de producción offline | 5 | 18 |
| E3 Sincronización | 3 | 15 |
| E4 Datos de mercado CENADA/SIMM | 5 | 21 |
| E5 Alertas con IA | 6 | 29 (24 + 5 stretch) |
| E6 Vinculación productor-comprador | 4 | 19 |
| E7 Calidad, UX y cierre | 7 | 26 |
| **Total** | **33** | **136** (131 comprometidos + 5 stretch) |

#### Supuestos y riesgos de la estimación

| Supuesto o riesgo | Respuesta |
|-------------------|-----------|
| El equipo no tiene velocidad histórica. | La velocidad se calibra al cierre del Sprint 1. |
| Los datos del CENADA/SIMM pueden cambiar de acceso o formato. | HU-15 (ingesta tolerante a cambios de formato). |
| El componente de IA (HU-17, HU-18) es experimental. | Se revisa en el refinamiento antes de su sprint. |
| La sincronización offline-first agrega incertidumbre técnica. | HU-11 es Should y puede moverse. |
| Los roles son compartidos en un equipo de 2. | Si hay desviación, se ajusta el alcance y no la fecha. |
| Se usa infraestructura gratuita o de código abierto. | Restricción de la sección 02. |

#### Velocidad inicial y cómo se actualizará

- **Velocidad inicial:** 26 SP por sprint (131 SP ÷ 5 sprints). La carga planificada va de 23 a 29 SP por sprint.
- **Actualización:** la velocidad real (SP en *Hecho* que cumplen la DoD) se calibra al cierre del Sprint 1 y se revisa en cada Sprint Review. Si hay desviación, se ajusta el alcance (no la fecha), moviendo primero las historias Should y Could.

#### Historias de más de 8 puntos

Ninguna historia supera los 8 SP, así que ninguna se marca para dividirse.

---

### Cronograma de Entregas (Release Plan)

#### Duración del sprint y fecha de inicio

- **Duración del sprint:** 2 semanas. Total: 10 semanas, 5 sprints.
- **Fecha de inicio del Sprint 1:** lunes 5 de octubre de 2026.
- **Fin del Sprint 5:** viernes 11 de diciembre de 2026 (semana del 7 al 13 de diciembre).

#### Sprints necesarios

| Velocidad | SP/sprint | Cálculo | Sprints |
|-----------|:---------:|---------|:-------:|
| Mínima | 23 | 131 ÷ 23 = 5,7 | 6 |
| Máxima | 29 | 131 ÷ 29 = 4,5 | 5 |

**Rango: entre 5 y 6 sprints.** Como el plazo es fijo en 5 sprints, con la velocidad mínima se ajusta el alcance moviendo primero las historias Should y Could.

#### Incremento por sprint

| Sprint | Semanas | Fechas | Historias | SP | Incremento |
|:------:|:-------:|--------|-----------|:--:|------------|
| 1 | 1-2 | 5 oct – 16 oct | HU-28, 01, 02, 03, 08, 16, 27, 29 | 23 | App base con inicio de sesión, perfil y mockups validados. |
| 2 | 3-4 | 19 oct – 30 oct | HU-04, 05, 06, 07, 12, 15 | 27 | Registro y consulta de producción sin conexión, e ingesta de precios del CENADA/SIMM. |
| 3 | 5-6 | 2 nov – 13 nov | HU-09, 10, 13, 14, 17 | 26 | Sincronización de datos al volver la conexión y primer análisis de tendencias de precios. |
| 4 | 7-8 | 16 nov – 27 nov | HU-11, 18, 19, 23, 24 | 26 | Alertas personalizadas al productor; registro de compradores y publicación de demanda. |
| 5 | 9-10 | 30 nov – 11 dic | HU-20, 25, 26, 30, 31, 32, 33 (+ stretch HU-21, 22) | 29 (+5) | Oferta y demanda conectadas, validación con productores y producto estable y documentado. |
| **Total** | | | **31 + 2 stretch** | **131 (+5)** | |

#### Hitos de entrega

| Hito | Cuándo | Con quién |
|------|--------|-----------|
| Validación de mockups (HU-29) | Sprint 1 | Productores de San Carlos |
| Sprint Review con el incremento | Último día de cada sprint | Equipo; docente cuando coincide con un hito |
| Prueba piloto (HU-30) | Sprint 5 | Grupo piloto de productores |
| Demo y cierre del proyecto (HU-33) | Sprint 5 | Docente |

#### Costo estimado por sprint y total del release

El proyecto no tiene presupuesto externo (sección 02). Los costos del Lean Canvas son las horas del equipo, la nube/almacenamiento y el mantenimiento del modelo de IA. Como la infraestructura es gratuita o de código abierto, el costo se estima solo con las horas del equipo.

| Concepto | Valor |
|----------|-------|
| Costo por hora | ₡3.510 (salario mínimo de Bachiller Universitario 2026, ₡664.078,07, más 26,83 % de cargas sociales, ÷ 30 días ÷ 8 h) |
| Dedicación | 9 h por semana por integrante (ISW-912 tiene 3 créditos; 1 crédito = 3 h de trabajo semanal del estudiante) |
| Horas por sprint | 2 integrantes × 9 h × 2 semanas = 36 h |
| **Costo por sprint** | **₡126.360** (36 h × ₡3.510) |
| **Total del release (5 sprints)** | **₡631.800** |

#### Seguimiento: burndown del release

Al cierre de cada sprint se registran los SP pendientes contra el plan.

| Momento | Pendiente según plan (SP) | Pendiente real (SP) |
|---------|:-------------------------:|:-------------------:|
| Inicio | 131 | 131 |
| Fin Sprint 1 | 108 | 108 |
| Fin Sprint 2 | 81 | 81 |
| Fin Sprint 3 | 55 | 55 |
| Fin Sprint 4 | 29 | 29 |
| Fin Sprint 5 | 0 | 0 |

---

## 08. Riesgos y adquisiciones

---

## 09. Calidad y Definition of Done

### Definition of Done (DoD)

Una historia de usuario está **Hecha** solo cuando cumple los siete puntos. La DoD es la misma para todo el proyecto; lo que cambia por historia son sus criterios de aceptación.

| # | Criterio | Quién lo verifica | Columna del tablero donde se verifica |
|:-:|----------|-------------------|---------------------------------------|
| 1 | Se cumplen todos los criterios de aceptación de la historia. | Developer responsable | Sale de *En progreso* |
| 2 | El código está en el repositorio e integrado a la rama `develop` mediante un pull request revisado por el otro integrante. | Integrante que no desarrolló | Sale de *En progreso* |
| 3 | La probó el integrante que no la desarrolló (pruebas cruzadas) y no hay defectos críticos abiertos. | Probador (QA cruzado) | Sale de *En pruebas cruzadas* |
| 4 | Corre en emulador o dispositivo y, cuando la historia lo exige, funciona sin conexión. | Probador | Sale de *En pruebas cruzadas* |
| 5 | Las pantallas cumplen la guía de estilo de HU-08 (íconos, letra legible, lenguaje claro). | Probador | Sale de *En pruebas cruzadas* |
| 6 | La documentación que corresponda está actualizada (README, arquitectura o expediente). | Developer responsable | Sale de *Revisión PO* |
| 7 | El Product Owner la aceptó frente a sus criterios de aceptación. | Product Owner (Joshua) | Entra a *Hecho* |

**Historias documentales o de investigación** (HU-16, HU-29 y similares): los puntos 2 y 4 se cumplen con el entregable subido al repositorio y revisado por el otro integrante; el punto 5 aplica solo si el entregable incluye pantallas.

**Aceptación cuando el PO es el autor:** si Joshua desarrolló la historia, Fabio la prueba y Joshua la acepta frente a los criterios escritos; la aceptación queda registrada como comentario en la tarjeta. Así se evita que alguien apruebe su propio trabajo sin una revisión independiente.

**Verificación al cierre:** en la Sprint Review solo se presentan historias en *Hecho*. Una historia que no cumple la DoD vuelve al Product Backlog y no suma puntos a la velocidad del sprint. HU-31 verifica formalmente el cumplimiento de la DoD en el Sprint 5.

---

## 10. Comunicación y responsabilidades del equipo

### Scrum Team

Con dos integrantes, los roles se comparten.

| Integrante | Roles Scrum | Rol adicional |
|------------|-------------|---------------|
| Joshua Quesada Madrigal | Product Owner y Developer | Director del proyecto (PM) |
| José Fabio Oconitrillo Salazar | Scrum Master y Developer | QA |

### Responsabilidades

- **Product Owner / PM (Joshua):** gestiona el Product Backlog, maximiza el valor del producto, define criterios de aceptación y coordina plan, riesgos y comunicación con el docente.
- **Scrum Master (Fabio):** facilita los eventos, remueve impedimentos y protege la capacidad del equipo.
- **Developers (ambos):** construyen los incrementos de cada Sprint y se comprometen con el Sprint Goal.
- **QA (Fabio):** verifica las pruebas y el cumplimiento de la Definition of Done.

**Regla para roles compartidos:** lo que desarrolla uno lo prueba el otro, y en cada evento de Scrum se declara con qué rol se participa.

### Participación del equipo en las decisiones

- Joshua Quesada lideró la valoración de los interesados orientados al usuario final (productores, intermediarios, transportistas).
- José Fabio Oconitrillo lideró la valoración de los interesados institucionales y de datos (CENADA/PIMA, MAG, UTN).
- La decisión sobre el enfoque de gestión (Híbrido) y la selección de los tres interesados críticos se tomaron en conjunto.

### Plan de Comunicaciones

#### Interesados, información que necesitan, frecuencia, canal y responsable

Se parte del registro de interesados de la sección 03 (poder e interés en escala 1-5).

| # | Interesado | Poder / Interés | Qué información necesita | Frecuencia y evento | Canal | Responsable |
|---|------------|:---------------:|--------------------------|---------------------|-------|-------------|
| 1 | Pequeños productores agrícolas | 2 / 5 | Qué hará la app, mockups para validar, avances que los afectan y resultados de las pruebas. | Sprint 1: sesión de validación de mockups (HU-29). Sprint 5: prueba piloto (HU-30). Aviso puntual cuando haya algo que validar. | Visita de campo o reunión presencial; WhatsApp para coordinar. | Joshua |
| 2 | Compradores formales | 3 / 3 | Alcance del módulo de vinculación y cómo publicar demandas. | Sprint 4 (registro de compradores y demandas, HU-23/24) y Sprint 5 (coincidencias). | Correo o llamada. | Fabio |
| 3 | Intermediarios tradicionales | 2 / 3 | No se les envía información programada; se monitorea su postura. | Se registran observaciones durante las visitas de campo. | Observación en campo. | Joshua |
| 4 | CENADA / PIMA — SIMM | 4 / 2 | Uso que el proyecto hará de sus datos; consulta sobre condiciones de uso. | Sprint 1: consulta formal (HU-16). Después, solo si cambia el acceso o el formato de la fuente. | Correo formal. | Fabio |
| 5 | Transportistas / logística | 2 / 2 | Ninguna planificada (logística fuera del alcance). | Solo monitoreo. | — | Joshua |
| 6 | MAG, extensionistas y asociaciones | 4 / 3 | Objetivo del proyecto; apoyo para contactar productores para la validación y el piloto. | Sprint 1 (antes de HU-29) y Sprint 5 (antes de HU-30). | Correo formal o reunión. | Fabio |
| 7 | Equipo de desarrollo | 5 / 5 | Avance, impedimentos, decisiones técnicas y estado de cada historia. | Diario (Daily) y eventos Scrum de cada sprint (ver tabla siguiente). | Tablero de Trello, WhatsApp del equipo, repositorio (pull requests) y videollamada. | Fabio (SM) |
| 8 | UTN — Sede San Carlos | 3 / 2 | Cumplimiento del curso y uso adecuado del nombre institucional. | Al cierre del proyecto, a través del docente. | Por medio del docente. | Fabio |
| 9 | Docente ISW-912 | 5 / 5 | Avance contra el plan, entregables de cada hito, cambios de alcance y riesgos. | Cada entregable o hito del curso; informe breve al cierre de cada sprint; aviso inmediato ante cambios de alcance. | Plataforma oficial del curso y correo institucional; acceso de lectura al tablero de Trello. | Joshua (PM) |

#### Eventos de comunicación del equipo (eventos Scrum)

| Evento | Frecuencia | Duración máx. | Participantes | Propósito | Canal | Facilita |
|--------|------------|:-------------:|---------------|-----------|-------|----------|
| Sprint Planning | Primer día de cada sprint (cada 2 semanas) | 1 h | Equipo | Definir el Sprint Goal y pasar historias del Product Backlog al Sprint Backlog. | Videollamada + Trello | Fabio (SM) |
| Daily Scrum | Días hábiles, horario acordado por el equipo | 15 min | Equipo | Qué hice, qué haré y qué me bloquea; revisar límites WIP del tablero. | Videollamada o WhatsApp (nota de voz/texto si no coinciden) | Fabio (SM) |
| Refinamiento del backlog | Una vez por semana | 30 min | Equipo | Revisar, estimar y ordenar las historias de los próximos sprints. | Videollamada + Trello | Joshua (PO) |
| Sprint Review | Último día de cada sprint | 45 min | Equipo; docente cuando coincide con un hito | Mostrar el incremento terminado (solo historias en *Hecho*). | Presencial o videollamada | Joshua (PO) |
| Retrospectiva | Después de cada Review | 30 min | Equipo | Mejorar la forma de trabajo; acordar una acción concreta. | Videollamada | Fabio (SM) |
| Informe de avance al docente | Al cierre de cada sprint | — | PM → docente | Resumen: Sprint Goal, historias terminadas, SP logrados, riesgos e impedimentos. | Plataforma del curso o correo + enlace al tablero | Joshua (PM) |

#### Reglas del equipo

**Tiempos de respuesta**

| Tipo de mensaje | Canal | Tiempo máximo de respuesta |
|-----------------|-------|----------------------------|
| Impedimento que bloquea una historia (mensaje con "BLOQUEO") | WhatsApp del equipo | 4 horas en días hábiles |
| Mensaje ordinario del equipo | WhatsApp o comentario en Trello | 12 horas |
| Revisión de un pull request | Repositorio | 24 horas |
| Correo del docente o de un interesado externo | Correo | 24 horas hábiles |

**Dónde se decide qué**

| Tipo de decisión | Quién decide | Dónde se decide | Dónde queda registrada |
|------------------|--------------|-----------------|------------------------|
| Prioridad y orden del Product Backlog | Product Owner (Joshua) | Refinamiento / Sprint Planning | Tablero de Trello (orden de la lista Product Backlog) |
| Qué entra al sprint y cómo se reparte el trabajo | Equipo | Sprint Planning | Tablero (Sprint Backlog) |
| Decisiones técnicas y de arquitectura | Equipo (Developers) | Daily o pull request | Repositorio (README / arquitectura) |
| Aceptación de una historia | Product Owner | Columna *Revisión PO* | Comentario en la tarjeta |
| Mejoras al proceso | Equipo | Retrospectiva | Expediente, sección 11 |
| Cambios de alcance que afectan un hito o entregable | Equipo, con aval del docente | Reunión del equipo + consulta al docente | Expediente, sección 11 (bitácora y decisiones) |

Ninguna decisión se da por tomada solo en una conversación de WhatsApp: si afecta el producto o el plan, se registra en el tablero o en el expediente.

#### Escalamiento de impedimentos

| Nivel | Qué se hace | Quién | Plazo |
|:-----:|-------------|-------|-------|
| 1 | El developer reporta el impedimento en la Daily o en WhatsApp con la palabra "BLOQUEO", marca la tarjeta con la etiqueta roja y explica el motivo en un comentario. | Developer afectado | En cuanto ocurre |
| 2 | El Scrum Master gestiona el impedimento (busca información, reorganiza el trabajo, pide apoyo). | Fabio (SM) | 24 horas |
| 3 | Si pone en riesgo el Sprint Goal, el PO ajusta el alcance del sprint: se mueven primero las historias Could y luego las Should. | Joshua (PO) | En la siguiente Daily |
| 4 | Si afecta un hito o entregable del curso, el PM informa al docente con la causa y una propuesta de ajuste. | Joshua (PM) | 48 horas |

Impedimentos externos previstos: si la fuente CENADA/SIMM cambia de formato o de acceso, se aplica el plan de contingencia de HU-15 y se informa al docente si afecta el plan.

#### Escalamiento de conflictos

| Nivel | Qué se hace | Quién |
|:-----:|-------------|-------|
| 1 | Conversación directa entre los dos integrantes, centrada en el problema y no en la persona, en un plazo máximo de 24 horas. | Ambos |
| 2 | Si no se resuelve, se trata en una sesión facilitada. La facilita el Scrum Master; si el conflicto involucra al Scrum Master en ese rol, la facilita el PM. Se decide con base en el Product Goal, la DoD y los criterios de aceptación. | Fabio (SM) o Joshua (PM) |
| 3 | Si persiste o afecta la entrega, se consulta al docente como mediador y su decisión es final. | Equipo → docente |

Los conflictos de prioridad del producto los decide el Product Owner; los conflictos técnicos, el equipo con evidencia (prueba de concepto o criterio de la arquitectura).

### Tablero de Trabajo

**Enlace al tablero:** [CosechaIA CR — Tablero de Trabajo (ISW-912)](https://trello.com/b/tDK73VQt/cosechaia-cr-tablero-de-trabajo-isw-912) — Trello, cuenta del equipo (administrador: Joshua Quesada).

#### Columnas y su significado (alineadas con la DoD)

| Columna | Qué significa | Para entrar a esta columna |
|---------|---------------|----------------------------|
| 📘 Reglas del tablero | Tarjetas de referencia: columnas, límites WIP, DoD y etiquetas. No es una etapa del flujo. | — |
| Product Backlog | Historias priorizadas (MoSCoW) que aún no están en un sprint. Las ordena el PO. | HU con formato Como/Quiero/Para, SP y prioridad. |
| Sprint Backlog (Por hacer) | Historias comprometidas en la Sprint Planning para el Sprint Goal vigente. | Criterios de aceptación definidos y dependencias identificadas. |
| En progreso · WIP 2 | Alguien construye la historia, en una rama propia. | Tiene responsable asignado. |
| En pruebas cruzadas · WIP 2 | La prueba el integrante que no la desarrolló. | DoD 1 y 2: criterios autoverificados y pull request abierto. |
| Revisión PO · WIP 2 | El PO verifica valor y criterios de aceptación. | DoD 3, 4 y 5: pruebas cruzadas aprobadas, funciona en dispositivo/sin conexión y guía de estilo aplicada. |
| Hecho ✅ | Incremento terminado, integrado y aceptado. | DoD completa (1 a 7). |

Si una historia se rechaza en pruebas o en revisión, vuelve a *En progreso* con un comentario que explica el motivo.

#### Límites WIP y su justificación

| Columna | Límite WIP | Justificación |
|---------|:----------:|---------------|
| Product Backlog | Sin límite | Es un inventario priorizado; no hay trabajo en curso. |
| Sprint Backlog | Sin límite (lo fija la capacidad del sprint, 23-29 SP) | El límite real es el compromiso de la Sprint Planning. |
| En progreso | 2 | Hay 2 developers: una historia por persona. Evita la multitarea y obliga a terminar antes de empezar otra. |
| En pruebas cruzadas | 2 | Cada uno prueba lo del otro, como máximo una historia por persona. Si la columna está llena, se prueba antes de seguir desarrollando. |
| Revisión PO | 2 | El PO es una sola persona que además desarrolla; más de 2 historias esperando aceptación crean un cuello de botella al final del sprint. |
| Hecho | Sin límite | Columna final. |

Cuando una columna llega a su límite no se agrega otra tarjeta: el equipo ayuda a vaciar la columna siguiente. Trello no bloquea el límite automáticamente, así que el Scrum Master lo revisa en cada Daily.

#### Historias del Sprint Backlog 1 cargadas

Las 8 historias del Sprint 1 (23 SP) están en la columna *Sprint Backlog*. Cada tarjeta incluye la historia, SP, prioridad, épica, dependencias, quién la prueba, un checklist con sus criterios de aceptación y un checklist con la Definition of Done. Las 25 historias restantes (Sprints 2 a 5 y stretch) están en *Product Backlog*.

| HU | Tarjeta | SP | Responsable | Prueba |
|----|---------|:--:|-------------|--------|
| HU-28 | Repositorio, arquitectura base y flujo de trabajo | 5 | Ambos | Revisión cruzada |
| HU-08 | Interfaz con íconos y lenguaje claro (guía de estilo) | 3 | Joshua | Fabio |
| HU-29 | Validar mockups con productores de San Carlos | 3 | Joshua | Fabio |
| HU-16 | Condiciones de uso de datos CENADA/SIMM | 2 | Fabio | Joshua |
| HU-01 | Crear cuenta e iniciar sesión | 3 | Fabio | Joshua |
| HU-27 | Consentimiento de uso de datos personales | 3 | Joshua | Fabio |
| HU-02 | Perfil del productor | 2 | Fabio | Joshua |
| HU-03 | Catálogo de cultivos | 2 | Joshua | Fabio |
| **Total** | | **23** | | |

#### Responsable visible por tarjeta

- El nombre de cada tarjeta termina con 👤 y el responsable (Joshua, Fabio o Ambos).
- Las tarjetas del sprint en curso llevan una etiqueta de color: morado = Joshua, azul = Fabio, verde = Ambos. Rojo = Bloqueado; amarillo = Should; naranja = Could.
- Cada integrante se asigna como miembro de sus tarjetas en Trello.

#### Regla para mover una tarjeta a "Hecho"

Una tarjeta solo pasa a **Hecho ✅** cuando su checklist de criterios de aceptación y su checklist de Definition of Done (sección 09) están completos. **Solo el Product Owner la mueve**, después de aceptarla, y deja un comentario de aceptación en la tarjeta. Si la historia la desarrolló el propio PO, la prueba Fabio antes de la aceptación.

---

## 11. Decisiones, cambios y evidencias — integración final

### Bitácora de cambios

| Versión | Fecha | Autor(es) | Entregable | Descripción del cambio |
|---------|-------|-----------|------------|------------------------|
| 0.1 | _(completar)_ | Joshua Quesada / José Fabio Oconitrillo | Primer entregable | Taller de interesados: registro de interesados, justificación de valoraciones, mapa Poder-Interés, tres interesados críticos y enfoque de gestión (Híbrido). |
| 0.2 | _(completar)_ | Joshua Quesada / José Fabio Oconitrillo | Segundo entregable | Unidad I: Acta de Inicio, definición del Scrum Team, Lean Canvas, EEFs y stakeholders (duración 14 semanas, ciclo adaptativo). |
| 1.0 | 2026-10-07 | Joshua Quesada / José Fabio Oconitrillo | Unificación | Se unifican ambos entregables en un solo documento. Se agrega el Product Backlog completo y el plan de 5 sprints. |
| 1.1 | 2026-10-07 | Joshua Quesada / José Fabio Oconitrillo | Reestructuración | El documento se reorganiza como Expediente del Proyecto (secciones 00 a 12). Las secciones 07, 08, 09 y 12 quedan solo con título hasta que correspondan. Se retiran del documento la Definition of Done, los eventos Scrum y la tabla de riesgos, que se incorporarán en sus secciones (09, 04 y 08) cuando se trabajen. |
| 1.2 | 2026-10-21 | Joshua Quesada / José Fabio Oconitrillo | Historias de usuario | En la sección 06, las tablas de criterios de aceptación por sprint se reemplazan por la ficha detallada de las 33 historias: formato Como/Quiero/Para, criterios Dado/cuando/entonces, prioridad, estimación, sprint, responsable, épica, dependencias y notas. |
| 1.3 | 2026-10-31 | Joshua Quesada / José Fabio Oconitrillo | Trabajo colaborativo | Se agregan a la sección 10 el Plan de Comunicaciones (interesados, información, frecuencia, canal, responsable, reglas del equipo y escalamiento) y el Tablero de Trabajo en Trello (columnas, límites WIP, Sprint Backlog 1, responsables y regla de "Hecho"). Se redacta la Definition of Done (sección 09) y se referencian los eventos Scrum en la sección 04. Se corrigen los totales de puntos de historia. |

### Decisiones y ajustes registrados

- **Duración:** pasa de 14 semanas a **10 semanas (5 sprints de 2 semanas)**.
- **Ciclo de vida:** se unifica en **Híbrido** (planificación predictiva de hitos y cronograma + ejecución iterativa con Scrum). El acta v0.2 decía "adaptativo"; el taller v0.1 decía "híbrido".
- **Interesados:** se unifican ambas tablas en un solo registro de 9 interesados. Se agrega al **Docente ISW-912** al registro y se agrupan MAG, extensionistas y asociaciones del sector en un solo interesado.
- **Poder/Interés:** se adopta la escala numérica 1-5 del taller (v0.1) en lugar de Alta/Media/Baja del acta (v0.2).
- **Mapa Poder-Interés:** se corrige la numeración, que no coincidía con el registro.
- **Código del curso:** se corrige a ISW-912 en todo el documento.
- **Historias de usuario:** se documentan con formato estándar Como/Quiero/Para y criterios Dado/cuando/entonces, manteniendo la asignación de responsables y sprints de la sección 05.
- **Puntos de historia (v1.3):** se corrige el total del Sprint 5 de 31 a **29 SP** (HU-20 3 + HU-25 8 + HU-26 3 + HU-30 5 + HU-31 5 + HU-32 3 + HU-33 2) y el total comprometido de 143 a **131 SP** (23 + 27 + 26 + 26 + 29), más 5 SP de stretch.
- **Herramienta de seguimiento:** se adopta Trello como Tablero de Trabajo, con límite WIP de 2 en las columnas activas.
- **Aceptación de historias:** solo el PO mueve tarjetas a "Hecho"; si el autor es el PO, la prueba primero el otro integrante.

### Evidencias

| Evidencia | Ubicación |
|-----------|-----------|
| Tablero de Trabajo (Trello) con Sprint Backlog 1 cargado | [CosechaIA CR — Tablero de Trabajo (ISW-912)](https://trello.com/b/tDK73VQt/cosechaia-cr-tablero-de-trabajo-isw-912) |
| Capturas del tablero y de una tarjeta con sus checklists | _(pendiente de adjuntar)_ |

---

## 12. Producto / Incremento final y cierre del proyecto
