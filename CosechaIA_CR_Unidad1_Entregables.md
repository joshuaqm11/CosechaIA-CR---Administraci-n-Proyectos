# CosechaIA CR — Unidad I: Marco conceptual de los proyectos

**ISW-912 · Administración de Proyectos Informáticos · UTN Sede San Carlos · III Cuatrimestre 2026**  
**Equipo:** Joshua Quesada Madrigal · José Fabio Oconitrillo Salazar

---

## 1. Acta de Inicio (Project Charter)

**Proyecto:** CosechaIA CR — plataforma móvil *offline-first* con IA para la comercialización anticipada de productos agrícolas de pequeños productores costarricenses.  
**Director del proyecto:** Joshua Quesada Madrigal · **Patrocinador:** Docente del curso · **Duración:** 14 semanas · **Ciclo de vida:** adaptativo (Scrum)

### Justificación

Los pequeños productores no cuentan con información integrada y personalizada sobre precios, mercado, compradores y transporte. Las fuentes públicas (CENADA, SIMM del PIMA) están dispersas. Esto los lleva a vender en momentos poco favorables o a depender de intermediarios. CosechaIA CR busca darles una herramienta simple, que funcione sin Internet, para decidir mejor cuándo y a quién vender.

### Objetivos

- **General:** desarrollar una plataforma móvil inteligente que facilite la comercialización anticipada de productos agrícolas mediante el análisis de precios, tendencias y demanda con IA.
- **Específicos:**

    1. Interfaz móvil sencilla para registrar producción, incluso sin conexión.
    2. Herramientas de IA que generen alertas personalizadas de comercialización.
    3. Módulo de vinculación entre productores y compradores.

### Límites generales

| Dentro del alcance | Fuera del alcance |
|---|---|
| App móvil con registro de producción y modo *offline* | Pagos o transacciones monetarias |
| Análisis de precios CENADA/SIMM y alertas con IA | Logística y contratación de transporte |
| Registro de compradores y coincidencias | Comercio electrónico completo |
| Notificaciones al productor | Operación en producción tras el cierre del curso |

**Restricciones:** tiempo fijo (14 semanas), equipo de 2 personas, sin presupuesto externo. El alcance es la variable flexible.

| Aprobación | Firma | Fecha |
|---|---|---|
| Joshua Quesada Madrigal | | |
| José Fabio Oconitrillo Salazar | | |
| Docente ISW-912 | | |

---

## 2. Definición del Scrum Team

Con dos integrantes, los roles se comparten.

| Integrante | Roles Scrum | Rol adicional |
|---|---|---|
| **Joshua Quesada Madrigal** | **Product Owner** y **Developer** | Director del proyecto (PM) |
| **José Fabio Oconitrillo Salazar** | **Scrum Master** y **Developer** | QA |

**Responsabilidades**

- **Product Owner / PM (Joshua):** gestiona el Product Backlog, maximiza el valor del producto, define criterios de aceptación y coordina plan, riesgos y comunicación con el docente.
- **Scrum Master (Fabio):** facilita los eventos, remueve impedimentos y protege la capacidad del equipo.
- **Developers (ambos):** construyen los incrementos de cada Sprint y se comprometen con el Sprint Goal.
- **QA (Fabio):** verifica las pruebas y el cumplimiento de la Definition of Done.

**Regla para roles compartidos:** lo que desarrolla uno lo prueba el otro, y en cada evento de Scrum se declara con qué rol se participa.

---

## 3. Análisis de Entorno (Lean Canvas y EEFs)

### Lean Canvas

| Bloque | Contenido |
|---|---|
| **Problema** | Información de mercado dispersa y no personalizada; dependencia de intermediarios; dificultad para hallar compradores |
| **Segmentos** | Pequeños productores agrícolas (principal); compradores de productos agrícolas (secundario) |
| **Propuesta de valor** | Decidir cuándo y a quién vender con alertas personalizadas, desde una app sencilla que funciona sin Internet |
| **Solución** | Registro de producción offline, alertas con IA sobre precios CENADA/SIMM, vinculación con compradores |
| **Canales** | App móvil; difusión por asociaciones de productores y ferias agrícolas *(hipótesis)* |
| **Ingresos** | Gratuita para el productor; suscripción o comisión a compradores *(hipótesis, fuera del alcance académico)* |
| **Costos** | Horas del equipo, nube/almacenamiento, mantenimiento del modelo de IA |
| **Métricas** | Productores y compradores registrados, alertas generadas, coincidencias logradas *(por definir)* |
| **Ventaja diferencial** | Offline-first + personalización por cultivo + vinculación directa con compradores en una sola herramienta |

### Factores Ambientales de la Empresa (EEFs)

| Tipo | Factor | Efecto en el proyecto |
|---|---|---|
| Interno | Equipo pequeño y autoorganizado | Favorece Scrum; riesgo de sobrecarga por roles compartidos |
| Interno | Calendario fijo de 14 semanas | Tiempo fijo; el alcance se ajusta |
| Interno | Infraestructura gratuita o de código abierto | Limita servicios de pago y decisiones de arquitectura |
| Externo | Disponibilidad de datos CENADA/SIMM | Insumo clave para la IA; riesgo si cambia el acceso o formato |
| Externo | Normativa de protección de datos personales | Restringe qué datos se recolectan y cómo se usan |
| Externo | Conectividad rural limitada | Justifica el enfoque offline-first y complica la sincronización |
| Externo | Baja alfabetización digital de algunos productores | Exige una interfaz muy simple |
| Externo | Estacionalidad y volatilidad del mercado agrícola | Condiciona la calidad de las alertas |

### Stakeholders

| Interesado | Interés principal | Influencia | Interés | Estrategia |
|---|---|---|---|---|
| Docente ISW-912 (patrocinador) | Cumplimiento de objetivos del curso | Alta | Alto | Gestionar de cerca |
| Equipo (Joshua y Fabio) | Producto funcional y aprobar el curso | Alta | Alto | Gestionar de cerca |
| Pequeños productores | Vender mejor y con más información | Media | Alto | Mantener informados e involucrados |
| Compradores | Encontrar proveedores y producto | Media | Medio | Mantener informados |
| CENADA / PIMA (SIMM) | Fuente de datos de precios | Alta | Bajo | Monitorear acceso y términos de uso |
| Asociaciones del sector agrícola *(posible canal)* | Apoyar a los productores | Media | Medio | Mantener informados |
