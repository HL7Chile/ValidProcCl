# Paso a paso

A continuación, se describe el proceso de validación de una Guía de Implementación (GI) nacional.

## Etapa 1: Insumos

En esta etapa se determinan las líneas base de la integración que se desea desarrollar. Para orientar adecuadamente el desarrollo de la Guía, se deben definir algunos aspectos clave:

- **Alcances:** Se debe establecer cuál es el alcance de la integración, incluyendo el ámbito del negocio y el tipo de proceso que se busca integrar (clínico, administrativo, financiero, etc.). Adicionalmente, se debe definir la jurisdicción del proyecto y los actores involucrados. Debe quedar claro el negocio que se desea abordar.

- **Objetivos:** Se deben precisar los objetivos que se espera alcanzar con el desarrollo del proyecto y sus integraciones. Con base en estos, se debe evaluar si el resultado del proyecto aporta valor.

- **Revisión de guías internacionales:** Es recomendable revisar guías de implementación FHIR existentes en repositorios oficiales que puedan tener similitudes o cercanía con el propósito del proyecto. Esto sirve como base para adoptar buenas prácticas.

- **Modelo conceptual del proyecto:** Este debe incluir:
  - Levantamiento del proceso
  - Identificación de los casos de uso
  - Determinación de actores y roles por caso de uso
  - Definición y caracterización del conjunto de datos
  - Identificación de las transacciones por caso de uso

- **Entregables esperados:**
  - Brochure de iniciación del proyecto
  - Documento con el modelamiento lógico y las transacciones por caso de uso

---

## Etapa 2: Primera versión de la Guía

Se desarrolla una versión preliminar de la guía con las siguientes características:

- `version`: 0.1.0  
- `status`: `draft`  
- `releaseLabel`: `ci-build`  

### Contenido

- Artefactos necesarios
- Contenido informativo:
  - Proceso
  - Casos de uso
  - Transacciones
  - Operaciones
  - Modelo lógico (si aplica)

### Revisión inicial por HL7 Chile

Una vez desarrollada esta versión, para incorporar el logo de HL7 Chile o del estándar FHIR, la guía debe pasar por una primera revisión formal a cargo de HL7 Chile.

### Insumos requeridos:

- Definición del negocio y objetivos
- Documento de modelamiento lógico
- Guía con el contenido completo especificado

### Proceso de revisión:

- Un equipo de tres expertos, una vez recibida la solicitud, será designado para revisar:
  - Existencia de todos los insumos
  - Coherencia entre el modelo lógico y el negocio definido
  - Coherencia entre el modelo lógico y el proceso descrito
  - Que la guía esté libre de errores de QA
  - Que no existan *warnings* críticos o que estos no comprometan la consistencia de la guía

- La evaluación tendrá una duración máxima de **7 días corridos**
- Se entregará un informe breve con alcances, correcciones sugeridas y definición sobre si la guía es validada en esta etapa preliminar
- Si es aprobada, HL7 Chile iniciará el proceso de **primer balotaje**

---

## Etapa 3: Guía para pilotaje

Luego de aplicar las correcciones derivadas de la primera revisión, se elabora una versión de la guía lista para pilotaje con las siguientes características:

- `version`: 0.x.y  
- `status`: `draft`  
- `releaseLabel`: `ci-build`  

### Contenido

- Artefactos necesarios
- Contenido informativo ampliado:
  - Proceso
  - Casos de uso
  - Transacciones
  - Operaciones
  - Modelo lógico (si aplica)
  - Menú de navegación ordenado
  - Descargas habilitadas
  - Template ajustado
  - Ejemplos desarrollados

Aunque aún puede estar sujeta a cambios, esta versión ya puede ser piloteada por actores previamente definidos por el desarrollador. El pilotaje debe ser acotado y tener objetivos específicos.

> *El pilotaje debe ser llevado a cabo conforme a los pasos descritos en XXXXXX.*

### Proceso de balotaje asociado al pilotaje
> *El balotaje debe ser llevado a cabo conforme a los pasos descritos en XXXXXX.*

El proceso se resume acá:

- HL7 Chile habilita un formulario en línea para levantar el proceso de balotaje y un formulario para comentarios y votos de participantes

- **Duración:** 30 días

- **El equipo de desarrollo, junto con HL7 Chile, revisa comentarios y verifica aprobación de la GI:**
 

- **Al cierre del proceso se publica resultados de balotaje**
- Si es aprobada, la guía pasa a:
  - `status`: `active`  
  - `releaseLabel`: `STU1`

---

## Etapa 4: Proceso de estabilización de la GI

El estado **STU (Standard for Trial Use)** se mantiene por un período determinado (recomendado: 6 meses), aunque puede ajustarse según las condiciones del proyecto.

### Durante este período, HL7 Chile:

- Mantiene la GI publicada en su sitio oficial de Guías Nacionales, junto con un formulario de comentarios
- Puede mantenerla en su entorno de construcción (CI), si se requiere

### Estado de la guía en esta fase

- `version`: 0.x.y  
- `status`: `active`  
- `releaseLabel`: `STU1` (o `STU2`, `STU3`, etc., según nuevas versiones)

La guía puede ser modificada según la retroalimentación obtenida en su uso. Si los cambios son significativos, el desarrollador podrá solicitar nuevos balotajes STU.

### Para solicitar balotaje normativo:

- Completar el formulario disponible en el sitio de HL7 Chile
- Publicar la guía en la página de balotaje con:
  - Formulario de observaciones
  - Sistema de votación
- Publicar resultados del proceso

### Si es aprobada, la guía pasa a:

- `version`: 1.0.0  
- `status`: `active`  
- `releaseLabel`: `normative`

---

## Etapa 5: Proceso evolutivo

Con el tiempo, los cambios en procesos, datos o tecnologías pueden hacer que una GI se vuelva obsoleta, activando un proceso de actualización.

### Pasos

- Modificar la guía actual
- Reiniciar el ciclo:
  - Pilotaje de la nueva versión
  - Nuevos balotajes STU
  - Nuevo balotaje normativo (si corresponde)

- Todos los balotajes se desarrollan en conjunto con HL7 Chile

- Una vez publicada una nueva versión normativa, se decide si la versión anterior:
  - Permanece como `active`  o pasa a `retired`
