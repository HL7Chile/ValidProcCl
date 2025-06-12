# Proceso de balotaje asociado al pilotaje

- HL7 Chile habilita un formulario en línea para levantar el proceso de balotaje:
  - Tipo de balotaje: **STU** o **Normative**
  - URL canónica de la guía
  - Nombre, versión, `status` y `releaseLabel`
  - Responsable

- HL7 Chile alojará la guía en un entorno CI (`build.fhir.org`) u otro equivalente si el desarrollador no dispone de uno
- Se anunciará en el sitio web de HL7 Chile que la guía está en proceso de balotaje
- El sitio incluirá un formulario para que los participantes ingresen comentarios y emitan sus votos

## Detalles del proceso

- **Duración:** 30 días
- **Participantes:**
  - Emiten voto: aprobar, rechazar o abstenerse
  - Ingresan comentarios por sección de la guía

- **El equipo de desarrollo, junto con HL7 Chile, revisa:**
  - Resoluciones
  - Acciones a desarrollar

- **Al cierre del proceso se publica:**
  - Acta de resoluciones
  - Resultados del balotaje

- Si la guía es rechazada y se sugieren muchos cambios, se repite el balotaje
- Si es aprobada, la guía pasa a:
  - `status`: `active`  
  - `releaseLabel`: `STU1`, `STU2`, `STU3`,...., `Normative`

---

<div align="center" >
  {% include Evolucion.svg %}
</div>
<br clear="all"/>