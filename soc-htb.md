## Especializacion SOC HTB

### Ejercicios de Purple Team
- **Qué demuestra:** Evaluaciones de seguridad realizadas por el equipo Red Team que informan al equipo azul sobre sus acciones y hallazgos, identificando vulnerabilidades mientras se prueba la capacidad defensiva.
- **Evidencia/herramientas:** Señal de práctica `resultado` — ejercicios que entregan hallazgos a los gestores de incidentes y mantienen involucrados a ambos equipos.

### Evaluación de seguridad de Active Directory
- **Qué demuestra:** Revisar la configuración de AD desde la perspectiva de un atacante para evitar que un endpoint comprometido permita escalada en un solo paso a privilegios altos.
- **Evidencia/herramientas:** Señal de práctica `escalada` — eliminación de vías fáciles y objetivos de baja complejidad en la red.

### Gestión de identidades con privilegios MFA
- **Qué demuestra:** El robo de credenciales de usuarios con privilegios es la ruta de escalada más común; contraseñas débiles o compartidas entre cuentas administrador y regular son un error común.
- **Evidencia/herramientas:** Señal de práctica `escalada` — implementación de MFA para todo acceso administrativo a aplicaciones y dispositivos.

### Investigación Inicial.
- **Qué demuestra:** Cuando se detecta un incidente, se debe establecer contexto antes de convocar al equipo de respuesta (ej.: una cuenta administradora accediendo desde una IP sin saber a qué sistema ni zona horaria puede llevar a conclusiones equivocadas).
- **Evidencia/herramientas:** Imagen incluida; señales de práctica `captura`, `lab`, `payload` — recopilación inicial de información, capturas y payload del incidente.

### dato inicial de la investigación.
- **Qué demuestra:** Proceso cíclico de 3 pasos que se repite a medida que la investigación evoluciona: creación y uso de IOC, identificación de nuevas pistas y sistemas afectados, y recolección/análisis de datos de esas pistas.
- **Evidencia/herramientas:** Imagen incluida (diagrama del proceso de investigación) que ilustra el flujo cíclico.

### Preguntas sobre la severidad y el alcance del incidente.
- **Qué demuestra:** Preguntas clave para valorar la severidad: impacto de la explotación, requisitos, sistemas críticos afectados, paso de remediación, número de sistemas afectados, uso del exploit en ataques reales y capacidad de gusano.
- **Evidencia/herramientas:** Señal de práctica `exploit` — marco de evaluación de impacto y severidad del incidente (incluye referencia a IDOR).

### Recolección y análisis de datos de las nuevas pistas y sistemas afectados.
- **Qué demuestra:** Una vez identificados los sistemas con IOCs, se recolecta y preserva su estado para análisis posterior; la respuesta en vivo es el enfoque más común, aunque en algunos casos se apaga el sistema primero.
- **Evidencia/herramientas:** Señal de práctica `evidencia` — procedimientos de recolección forense y preservación de sistemas afectados.

### Uso de IA en la Detección de amenazas.
- **Qué demuestra:** La IA transforma la detección, triage y respuesta a incidentes automatizando el análisis manual de logs y alertas, reduciendo el tiempo de respuesta y aprendiendo de incidentes históricos.
- **Evidencia/herramientas:** Imagen incluida; ejemplo concreto de la función "attack discovery" de Elastic Security que utiliza IA generativa.

### Escenario del incidente
- **Qué demuestra:** Caso práctico de la empresa Insight Nexus (investigación de mercado, Singapur) con una pila de aplicaciones interna, servidor ManageEngine y portal de informes en PHP; se menciona una vulnerabilidad IDOR.
- **Evidencia/herramientas:** Imagen incluida — escenario del incidente con infraestructura afectada (aplicaciones, ManageEngine, portal PHP).

### Contención.
- **Qué demuestra:** Etapa de contención dividida en corto plazo (huella mínima) y largo plazo; las acciones se coordinan y ejecutan simultáneamente en todos los sistemas para evitar alertar al atacante.
- **Evidencia/herramientas:** Señal de práctica `evidencia` — procedimientos de contención a corto/largo plazo y coordinación de acciones.

### Informe final
- **Qué demuestra:** Informe completo que responde qué pasó y cuándo, el desempeño del equipo frente a planes/playbooks/políticas, información a la gestión, acciones de contención/erradicación y medidas preventivas para evitar incidentes similares.
- **Evidencia/herramientas:** Señal de práctica `resultado` — plantilla de informe final post-incidente con lecciones aprendidas.
