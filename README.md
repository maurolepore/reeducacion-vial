# Educacion y reeducacion vial en CABA

Información sobre el sistema de scoring y recuperación de puntos en Buenos Aires. Incluye un AI skill para generar exámenes de práctica de reeducación vial, con los manuales de las dos empresas que ofrecen entrenamiento (Sistemas Reid y Creando Conciencia). Bonus: también puede generar exámenes para el examen de manejo normal (no de reeducación).

## Instalación del skill

```bash
npx skills add maurolepore/reeducacion-vial
```

O manualmente: copiar `skills/test/` al directorio de skills de tu agente (e.g. `.claude/skills/`, `.cursor/rules/`, etc.).

**En el browser** (Claude.ai, ChatGPT, Gemini): Pegar el contenido de `skills/test/SKILL.md` + los manuales como archivos adjuntos o en Project Knowledge.

TODO: Crear un pre-commit hook o script que genere automáticamente un archivo concatenado (SKILL.md + manuales) listo para usar en el browser.

## Material incluido

- Manuales de estudio de reeducación vial: [Sistemas Reid](skills/test/references/manual_reid_curso-de-reeducacion-vial.md) y [Creando Conciencia](skills/test/references/manual_creandoconciencia_curso-de-reeducacion-vial.md)
- [Manual del examen de conducir CABA](skills/test/references/manual_caba_examen-de-conduccion.md)
- [Preguntas reales del examen presencial](skills/test/references/examen-real.md) (basadas en mi memoria/experiencia)
- Data del [simulador de examen de conducir CABA](https://bandinopla.github.io/simulador-test-de-conducir/) (simulador-test-de-conducir/src/data/)

# **Como recuperar puntos por infracciones de tránsito (CABA)**

[Consulta de infracciones de tránsito y scoring](https://buenosaires.gob.ar/licenciasdeconducir/consulta-de-infracciones/?actas=transito)

Los puntos perdidos pueden recuperarse de tres formas:

1. Pago voluntario de cada infracción, seguido de un curso gratis online de 20’ y un examen gratis online de 5 preguntas. Permite recuperar el 50% de los puntos perdidos por la infracción. Notar que el pago voluntario solamente NO recupera puntos – hay que hacer el curso y aprobar el examen.  
2. Reeducación vial independiente de las infracciones, curso pago de 4h, examen gratis presencial en el gobierno. Recupera 4 puntos por cada ano calendario.  
3. Caducidad

## **Advertencias: No te apures a pagar**

Si la infracción la hizo otra persona 

* No pagues vos ni la otra persona. Primero hacé el descargo. Podés tomar una audiencia virtual. Se pierde el descuento por pago voluntario  
* Si ya pagó la otra persona (el que cometió la infracción): Escribí a [scoringdgai@buenosaires.gob.ar](mailto:scoringdgai@buenosaires.gob.ar) **ANTES** de hacer el curso para solicitar el traspaso de puntos. Una vez iniciado el curso, no se puede hacer el traspaso.

Si tenes muchas infracciones del mismo tipo o cercanas en tiempo (e.g. todas en Corrientes por ir a mas de 30km/h entre Callao y 9 de Julio), podes pedir una audiencia y pedir que te las agrupen como una sola.

## **1\. Pago voluntario de cada infracción (50% de los puntos perdidos)**

Para infracciones pagadas voluntariamente podes recuperar \~50% de los puntos descontados haciendo un curso online de \~20’ seguido de un examen online.

En teoría el sistem debería mandar dos emails:

1. Notificando la infracción y con links para hacer el pago voluntario.  
2. Después de hacer el pago voluntario, con el link al video para recuperar los puntos

Alternativa: Luego de haber hecho el pago voluntario, probar directamente en [Trámites Digitales](https://tramitesdigitales.buenosaires.gob.ar/formulario/formularioTemplate/charlaInfracciones). 

En la práctica yo no recibí el segundo email, me informe llamando al 147 y logre solicitarlo así:

1. Ir a [Mesa de ayuda](https://gestioncolaborativa.buenosaires.gob.ar/encuesta?id=484&nombre=Mesa%20de%20ayuda%20de%20sistemas%20y%20tr%C3%A1mites%20digitales)  
2. Seleccionar:  
   - Mesa de ayuda y tramites digitales  
   - Tramites digitales  
   - Sistema de Evaluación permanente de conductores (Scoring)  
   - "Tengo dudas sobre el curso virtual de reasignación de puntos por PV"  
3. Confirmar y solicitar curso

## **2\. Reeducación vial independiente (4 puntos por año calendario)**

Independiente de infracciones, no asociado a pago voluntario. Requisitos:

* No haber llegado a 0 puntos  
* Solo una vez por año  
* Si fuiste inhabilitado y ya tenés 10 puntos, no te acreditan 4 extras

Empresas que lo dictan:

* [Creando Conciencia](https://creandoconciencia.org.ar/courses/)  
* [Sistemas Reid (ConCodigo)](https://app.concodigo.com/scoring#scoringoptativo)

## **3\. Caducidad**

No estoy seguro de los detalles. Creo que es algo así: Luego de dos (o tres?) años …

* … sin infracciones se recuperan los 20 puntos totales.  
* … desde cada infracción se recuperan los puntos perdidos por esa infracción.

## **Links**

* Informacion  
* 147 y otros [teléfonos útiles](https://buenosaires.gob.ar/jefaturadegabinete/telefonos-utiles)  
* Boti CABA [online](https://buenosaires.gob.ar/innovacionytransformaciondigital/boti) y en whatsapp  
* [Sistema de evaluación permanente de conductores](https://buenosaires.gob.ar/gobierno/licencias-de-conducir/sistema-de-evaluacion-permanente-de-conductores)

## Disclaimer

Los manuales incluidos en este repositorio son material educativo de terceros, reproducidos con fines de estudio personal y uso educativo sin fines de lucro:

- **Manual Reid**: Material del curso de reeducación vial de [Sistemas Reid / ConCodigo](https://app.concodigo.com/scoring#scoringoptativo)
- **Manual Creando Conciencia**: Material del curso de [Creando Conciencia](https://creandoconciencia.org.ar/courses/), basado en contenido de la Secretaría de Transporte / Dirección de Seguridad Vial
- **Manual CABA**: Material del [examen de conducir de CABA](https://buenosaires.gob.ar/gobierno/licencias-de-conducir)
- **Datos del simulador**: Del proyecto open-source [bandinopla/simulador-test-de-conducir](https://github.com/bandinopla/simulador-test-de-conducir)

Todo el contenido de terceros pertenece a sus respectivos autores. Si sos titular de alguno de estos materiales y querés que se retire, abrí un issue o contactame.
