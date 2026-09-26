**Taller: Interesados de nuestro proyecto**

*Lección 2 --- Proyecto: CosechaIA CR*

Estudiantes: Joshua Quesada Madrigal / José Fabio Oconitrillo Salazar

# **Contexto del proyecto**

CosechaIA CR es una plataforma móvil offline-first que usa Inteligencia
Artificial para que pequeños productores agrícolas de Costa Rica
registren su producción (cultivo, cantidad y fecha estimada de cosecha)
y reciban alertas personalizadas sobre oportunidades de
comercialización, con base en precios y tendencias del CENADA/SIMM,
además de un módulo de vinculación con compradores interesados.

La aplicación funciona sin conexión para las funciones básicas y
sincroniza cuando hay conectividad.

# **Registro de interesados**

  -------------------------------------------------------------------------------------------------------------------------------------
  **\#**   **Interesado**     **Rol /        **Necesidad**       **Poder   **Interés   **Actitud**   **Estrategia**   **Responsable**
                              relación**                         (1-5)**   (1-5)**                                    
  -------- ------------------ -------------- ------------------- --------- ----------- ------------- ---------------- -----------------
  1        Pequeños           Usuario        Acceder a           2         5           Mixta         Mantener         Joshua Quesada
           productores        primario /     información                                             informado;       
           agrícolas          cliente final  oportuna de                                             involucrarlos en 
                                             precios, tendencias                                     pruebas de       
                                             y compradores,                                          usabilidad y     
                                             incluso sin                                             validaciones de  
                                             conexión a                                              campo.           
                                             Internet.                                                                

  2        Compradores        Usuario        Encontrar oferta    3         3           Neutral       Monitorear;      José Fabio
           formales           secundario /   confiable, con                                          mantener         Oconitrillo
           (agroindustrias,   lado de la     cantidades y fechas                                     informado sobre  
           mayoristas)        demanda        reales, reduciendo                                      el módulo de     
                                             costo de búsqueda.                                      vinculación.     

  3        Intermediarios     Actor externo  Mantener su rol y   2         3           Resistente    Monitorear;      Joshua Quesada
           tradicionales      del entorno de margen actual en la                                     buscar puntos de 
           (acopiadores)      mercado        cadena de                                               colaboración en  
                                             comercialización.                                       vez de           
                                                                                                     confrontación    
                                                                                                     directa.         

  4        CENADA / PIMA --   Proveedor      Uso correcto y      4         2           Neutral       Mantener         José Fabio
           SIMM               externo de     autorizado de su                                        satisfecho;      Oconitrillo
                              datos de       información pública                                     formalizar       
                              mercado        de precios.                                             condiciones de   
                                                                                                     uso de los       
                                                                                                     datos.           

  5        Transportistas /   Actor externo, Que la app refleje  2         2           Neutral       Monitorear.      Joshua Quesada
           logística agrícola insumo de      con precisión                                                            
                              datos de       costos y tiempos de                                                      
                              costo/tiempo   transporte.                                                              

  6        MAG y              Institución    Alineación con la   4         3           Favorable     Mantener         José Fabio
           extensionistas     pública del    política agrícola y                                     satisfecho;      Oconitrillo
           agrícolas          sector /       un posible canal de                                     explorar alianza 
                              aliado         difusión con                                            de difusión.     
                              potencial      productores.                                                             

  7        Equipo de          Equipo del     Tiempo,             5         5           Favorable     Gestionar de     Ambos
           desarrollo (Joshua proyecto       conocimiento                                            cerca            
           y José Fabio)                     técnico (IA,                                            (autogestión,    
                                             desarrollo móvil                                        revisión         
                                             offline-first) y                                        periódica de     
                                             alcance claro.                                          avance).         

  8        UTN -- Sede        Institución    Cumplimiento        3         2           Neutral       Mantener         José Fabio
           Regional de San    académica      normativo del curso                                     informado.       Oconitrillo
           Carlos                            y uso adecuado del                                                       
                                             nombre                                                                   
                                             institucional.                                                           

                                                                                                                      
  -------------------------------------------------------------------------------------------------------------------------------------

# 

# 

# **Justificación de valoraciones y casos discutibles**

-   **Pequeños productores (Poder = 2, Interés = 5):**

> No tienen autoridad formal para aprobar presupuesto ni alcance del
> proyecto, por lo que se les asignó poder bajo. Sin embargo, su
> decisión de adoptar o no la aplicación determina el éxito real del
> producto; ese \"poder de adopción\" no es poder formal de gobernanza,
> por lo que se mantiene separado del interés, que sí es el más alto del
> registro.

-   **CENADA / PIMA -- SIMM (Poder = 4, Interés = 2):**

> Al ser una entidad pública con su propia agenda, el proyecto académico
> no es prioritario para ellos (interés bajo). No obstante, se les
> asignó poder alto porque son la única fuente disponible de precios
> mayoristas: si restringen, cambian de formato o no autorizan el uso
> sistemático de sus datos, el motor de IA del proyecto queda
> comprometido.

-   **Intermediarios tradicionales / acopiadores (Poder = 2, Interés =
    3, actitud \"Resistente\"):**

> Se incluyen aun sin relación contractual con el proyecto porque la
> propuesta original señala la dependencia de intermediarios como parte
> del problema. No tienen poder formal sobre el proyecto, pero sí pueden
> influir informalmente sobre los productores (con quienes ya tienen
> relación de confianza) para desincentivar el uso de la plataforma.

# **Mapa Poder-Interés**

Para graficar el mapa se simplificó la escala 1-5 a Bajo (1-3) / Alto
(4-5).

+-------+------------------------------+------------------------------+
|       | **INTERÉS BAJO (1-3)**       | **INTERÉS ALTO (4-5)**       |
+=======+==============================+==============================+
| **    | **Mantener satisfecho**      | **Gestionar de cerca**       |
| PODER |                              |                              |
| ALTO  | 4\. CENADA / PIMA -- SIMM    | 7\. Docente ISW-912          |
| (4    |                              |                              |
| -5)** | 6\. MAG y extensionistas     | 8\. Equipo de desarrollo     |
+-------+------------------------------+------------------------------+
| **    | **Monitorear**               | **Mantener informado**       |
| PODER |                              |                              |
| BAJO  | 2\. Compradores formales     | 1\. Pequeños productores     |
| (1    |                              |                              |
| -3)** | 3\. Intermediarios           |                              |
|       | tradicionales                |                              |
|       |                              |                              |
|       | 5\. Transportistas           |                              |
|       |                              |                              |
|       | 9\. UTN Sede San Carlos      |                              |
+-------+------------------------------+------------------------------+

# **Tres interesados críticos y estrategia de involucramiento**

**1. Pequeños productores agrícolas**

**Por qué es crítico:** Son la razón de ser del proyecto: sin adopción
real de este grupo, la plataforma no genera el valor esperado, sin
importar qué tan bien funcione la IA.

**Cómo se involucrará:** Entrevistas y pruebas de usabilidad con
productores de la zona de San Carlos; prototipos simples (mockups) antes
de programar; lenguaje claro y capacitación básica; canal de
retroalimentación accesible (p. ej. WhatsApp o visitas de campo); piloto
con un grupo reducido antes de escalar.

**2. CENADA / PIMA -- SIMM**

**Por qué es crítico:** Son la fuente de datos que alimenta el motor de
IA (precios, tendencias, estacionalidad); sin una relación clara con
ellos, el análisis pierde confiabilidad.

**Cómo se involucrará:** Investigar y documentar formalmente las
condiciones de uso de sus datos abiertos; diseñar la integración de
forma tolerante a cambios de formato (plan de contingencia); mantener
registro de la fuente y frecuencia de actualización usada en el
proyecto.

**3. Docente del curso ISW-912**

**Por qué es crítico:** Es quien aprueba, evalúa y puede exigir ajustes
de alcance o enfoque; su satisfacción condiciona el avance académico del
proyecto.

**Cómo se involucrará:** Entregar evidencias en cada hito del curso
(registro de interesados, mapa Poder-Interés, prototipo); solicitar
retroalimentación temprana antes de las entregas finales; comunicar de
inmediato cualquier cambio relevante de alcance.

# **Enfoque de gestión: Predictivo, Adaptativo o Híbrido**

**Decisión del equipo:** enfoque **Híbrido**.

## **Elementos que justifican la parte predictiva**

-   El proyecto se desarrolla con fechas de entrega fijas ya impuestas,
    no negociables.

-   Los tres objetivos específicos de la propuesta ya delimitan un
    alcance macro relativamente estable (interfaz offline de registro,
    motor de IA de alertas, módulo de vinculación productor-comprador),
    lo que permite planificar fases y entregables generales con
    anticipación.

## **Elementos que justifican la parte adaptativa**

-   Alta incertidumbre en los requisitos de UX del segmento de usuario
    (productores rurales, posible baja alfabetización digital,
    conectividad intermitente): requiere prototipos y ciclos cortos de
    retroalimentación antes de converger en una solución definitiva.

-   El componente de Inteligencia Artificial (análisis de precios,
    tendencias y alertas personalizadas) es experimental: su precisión
    depende de datos reales del CENADA/SIMM y debe ajustarse
    iterativamente conforme se validen resultados con usuarios.

-   El módulo de vinculación productor-comprador depende de la adopción
    real de ambos lados del mercado, un comportamiento que no puede
    planificarse con certeza desde el inicio.

-   El contexto rural con conectividad limitada añade incertidumbre
    técnica en la sincronización offline-first, que se resuelve mejor
    con iteraciones sucesivas que con un plan detallado desde el
    principio.

**Conclusión:** planificación predictiva a nivel de hitos académicos,
alcance macro y cronograma general del curso, combinada con ciclos
adaptativos/iterativos para el diseño con productores, el ajuste del
modelo de IA y la validación del módulo de vinculación con compradores.

# **Participación del equipo**

Ambos integrantes participaron en al menos una decisión clave:

-   Joshua Quesada lideró la valoración de los interesados orientados al
    usuario final (productores, intermediarios, transportistas)

-   José Fabio Oconitrillo lideró la valoración de los interesados
    institucionales y de datos (CENADA/PIMA, MAG, UTN).

-   La decisión sobre el enfoque de gestión (Híbrido) y la selección de
    los tres interesados críticos se tomaron en conjunto.
