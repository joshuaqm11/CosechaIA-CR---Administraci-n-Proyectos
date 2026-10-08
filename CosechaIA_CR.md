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
| Docente / patrocinador | Docente del curso ISW-912 |
| Versión del expediente | 1.1 |

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

**Total:** 33 historias · 143 SP comprometidos en 5 sprints + 5 SP en stretch.

### Distribución por sprint

| Sprint | Semanas | Historias | SP comprometidos |
|--------|---------|-----------|:----------------:|
| 1 | 1-2 | HU-01, 02, 03, 08, 16, 27, 28, 29 | 23 |
| 2 | 3-4 | HU-04, 05, 06, 07, 12, 15 | 27 |
| 3 | 5-6 | HU-09, 10, 13, 14, 17 | 26 |
| 4 | 7-8 | HU-11, 18, 19, 23, 24 | 26 |
| 5 | 9-10 | HU-20, 25, 26, 30, 31, 32, 33 (+ stretch HU-21, 22) | 31 |

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

### Criterios de aceptación por sprint

**Sprint 1**

| HU | Criterios de aceptación |
|----|-------------------------|
| HU-28 | Repositorio creado con ramas definidas; arquitectura base documentada; app móvil ejecutándose en un dispositivo o emulador. |
| HU-01 | El usuario puede registrarse e iniciar sesión; las contraseñas no se guardan en texto plano; los errores se muestran con mensajes claros. |
| HU-02 | El perfil guarda nombre, zona y cultivos de interés y puede consultarse luego. |
| HU-03 | El catálogo muestra los cultivos principales de la zona y permite seleccionar uno. |
| HU-08 | Guía de estilo con íconos, tamaños de letra y textos simples aplicada a las pantallas base. |
| HU-16 | Documento con fuente, licencia/condiciones de uso y frecuencia de actualización de los datos del CENADA/SIMM. |
| HU-27 | Pantalla de consentimiento obligatoria antes de usar la app; se registra la aceptación. |
| HU-29 | Mockups de las pantallas clave revisados con al menos 3 productores; ajustes documentados. |

**Sprint 2**

| HU | Criterios de aceptación |
|----|-------------------------|
| HU-04 | Se guarda cultivo, cantidad y fecha estimada; se validan campos vacíos y fechas inválidas. |
| HU-05 | El listado muestra todos los registros del usuario ordenados por fecha de cosecha. |
| HU-06 | Se puede editar y eliminar un registro con confirmación previa. |
| HU-07 | Con el dispositivo sin conexión se pueden crear, ver y editar registros; los datos persisten al cerrar la app. |
| HU-12 | Proceso que descarga y almacena precios del CENADA/SIMM; registra fecha y fuente de cada carga. |
| HU-15 | Ante un cambio de formato, la ingesta falla de forma controlada, registra el error y conserva los datos previos. |

**Sprint 3**

| HU | Criterios de aceptación |
|----|-------------------------|
| HU-09 | Los registros creados offline se envían al servidor al detectar conexión, sin duplicados. |
| HU-10 | Indicador visible: sincronizado, pendiente o error. |
| HU-13 | Histórico de precios consultable por producto y rango de fechas. |
| HU-14 | El productor ve el último precio disponible de su cultivo, con la fecha de la última actualización, incluso offline. |
| HU-17 | El modelo identifica tendencia (sube, baja, estable) y estacionalidad para al menos los cultivos del catálogo con datos suficientes; resultados documentados. |

**Sprint 4**

| HU | Criterios de aceptación |
|----|-------------------------|
| HU-18 | Dada una producción registrada y las tendencias, se genera una alerta con cultivo, mensaje claro y momento sugerido. |
| HU-19 | La alerta llega como notificación al dispositivo; si no hay conexión, se muestra al abrir la app. |
| HU-11 | Ante cambios en el mismo registro desde dos fuentes, se aplica una regla definida (p. ej. última modificación) y no se pierde información. |
| HU-23 | El comprador se registra con nombre, tipo y productos de interés. |
| HU-24 | El comprador publica una demanda con cultivo, cantidad y fecha; puede cerrarla o editarla. |

**Sprint 5**

| HU | Criterios de aceptación |
|----|-------------------------|
| HU-25 | Se listan demandas compatibles por cultivo, cantidad aproximada y fecha; se ordenan por relevancia. |
| HU-26 | El productor marca interés y el comprador recibe el aviso con los datos de contacto autorizados. |
| HU-20 | El productor puede activar/desactivar tipos de alerta y elegir frecuencia. |
| HU-30 | Prueba con grupo piloto; resultados y mejoras documentados; ajustes críticos aplicados. |
| HU-31 | Casos de prueba ejecutados; defectos críticos resueltos; DoD verificada por QA. |
| HU-32 | Manual breve con capturas de las funciones principales. |
| HU-33 | Demo preparada y presentada al docente; documento final y repositorio actualizados. |
| HU-21, HU-22 | _(Stretch)_ Se abordan solo si el sprint va holgado. |

---

## 07. Planificación temporal, estimaciones y costos

---

## 08. Riesgos y adquisiciones

---

## 09. Calidad y Definition of Done

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

---

## 11. Decisiones, cambios y evidencias — integración final

### Bitácora de cambios

| Versión | Fecha | Autor(es) | Entregable | Descripción del cambio |
|---------|-------|-----------|------------|------------------------|
| 0.1 | _(completar)_ | Joshua Quesada / José Fabio Oconitrillo | Primer entregable | Taller de interesados: registro de interesados, justificación de valoraciones, mapa Poder-Interés, tres interesados críticos y enfoque de gestión (Híbrido). |
| 0.2 | _(completar)_ | Joshua Quesada / José Fabio Oconitrillo | Segundo entregable | Unidad I: Acta de Inicio, definición del Scrum Team, Lean Canvas, EEFs y stakeholders (duración 14 semanas, ciclo adaptativo). |
| 1.0 | 2026-10-07 | Joshua Quesada / José Fabio Oconitrillo | Unificación | Se unifican ambos entregables en un solo documento. Se agrega el Product Backlog completo y el plan de 5 sprints. |
| 1.1 | 2026-10-07 | Joshua Quesada / José Fabio Oconitrillo | Reestructuración | El documento se reorganiza como Expediente del Proyecto (secciones 00 a 12). Las secciones 07, 08, 09 y 12 quedan solo con título hasta que correspondan. Se retiran del documento la Definition of Done, los eventos Scrum y la tabla de riesgos, que se incorporarán en sus secciones (09, 04 y 08) cuando se trabajen. |

### Decisiones y ajustes registrados

- **Duración:** pasa de 14 semanas a **10 semanas (5 sprints de 2 semanas)**.
- **Ciclo de vida:** se unifica en **Híbrido** (planificación predictiva de hitos y cronograma + ejecución iterativa con Scrum). El acta v0.2 decía "adaptativo"; el taller v0.1 decía "híbrido".
- **Interesados:** se unifican ambas tablas en un solo registro de 9 interesados. Se agrega al **Docente ISW-912** al registro y se agrupan MAG, extensionistas y asociaciones del sector en un solo interesado.
- **Poder/Interés:** se adopta la escala numérica 1-5 del taller (v0.1) en lugar de Alta/Media/Baja del acta (v0.2).
- **Mapa Poder-Interés:** se corrige la numeración, que no coincidía con el registro.
- **Código del curso:** se corrige a ISW-912 en todo el documento.

### Evidencias

_(Pendiente de registrar)_

---

## 12. Producto / Incremento final y cierre del proyecto
