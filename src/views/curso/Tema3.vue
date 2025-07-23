<template lang="pug">
.curso-main-container.pb-3
  BannerInterno(:subTitulo="'3. Evaluación de la viabilidad de estrategias a largo plazo'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5

    .row.mb-5
      .col-lg-4.order-lg-2
        figure
          img(src="@/assets/curso/tema3/1.png", data-aos="zoom-in").mb-4.mb-lg-0
      .col-lg-8.order-lg-1
        p(data-aos="fade-left").mb-4 La evaluación de la #[b viabilidad de estrategias a largo plazo], es fundamental para determinar si las iniciativas estratégicas pueden sostenerse y ser efectivas con el tiempo. 

        .bg-color-1.p-4(data-aos="fade-left").mb-4
          .row.align-items-center
            .col-lg-auto
              img(src="@/assets/curso/tema3/2.svg", style="max-width: 90px").mx-auto
            .col-lg
              p.mb-0 Esta evaluación considera diversos factores económicos, sociales y ambientales, asegurando que las decisiones sean sólidas y adaptativas a las condiciones cambiantes del entorno.

        p(data-aos="fade-left") #[b Los componentes claves de la evaluación, son:]

    .row.align-items-center.mb-5.pb-4
      .col-lg-4
        figure
          img(src="@/assets/curso/tema3/3.png", alt="", data-aos="zoom-in").mb-4.mb-lg-0
      .col-lg-8
        LineaTiempoD.color-primario.large(data-aos="fade-left")
          div(numero="1" titulo="Análisis de factibilidad económica")
            p Este análisis se enfoca en el retorno de la inversión (ROI), los costos asociados, y la escalabilidad de la estrategia. Según Sánchez González (2018), “una evaluación financiera sólida es esencial para asegurar la sostenibilidad económica a largo plazo” (p. 45). Herramientas como el análisis de flujo de caja descontado, permiten prever los beneficios futuros y determinar si los recursos financieros serán suficientes.

          div(numero="2" titulo="Impacto ambiental y social")
            p Evaluar los efectos ambientales y sociales, implica medir la huella de carbono y los beneficios para las comunidades locales. Boada y Cardona Montoya (2020), destacan que “el éxito de una estrategia a largo plazo depende de su capacidad para generar un impacto positivo en el entorno y en las personas afectadas” (p. 78). El cumplimiento de las regulaciones ambientales y la aceptación por parte de las comunidades, son esenciales para la viabilidad.

          div(numero="3" titulo="Análisis de riesgos y oportunidades")
            p La identificación y gestión de riesgos ayuda a preparar a la organización para enfrentar desafíos futuros. Bas Amorós (2013), sugiere que “las empresas deben anticipar cambios regulatorios y tecnológicos, creando planes de mitigación que protejan sus estrategias” (p. 92). Al mismo tiempo, identificar oportunidades como avances tecnológicos o incentivos gubernamentales, puede fortalecer la estrategia.

          div(numero="4" titulo="Simulación de escenarios y análisis de sensibilidad")
            p Utilizar simulaciones permite prever cómo las variaciones en las condiciones de mercado, podrían afectar la estrategia. El análisis de sensibilidad, como menciona López Segrera et al. (2004), “es vital para entender qué variables son críticas y cómo pequeños cambios pueden tener un impacto significativo” (p. 112).

          div(numero="5" titulo="Consulta y retroalimentación de <em>stakeholders</em>")
            p Fernández (2016), enfatiza que “la retroalimentación de los <em>stakeholders</em> aporta una perspectiva externa que puede revelar aspectos que no se habían considerado internamente” (p. 53). Asegurar la transparencia y mantener una comunicación abierta con los <em>stakeholders</em>, ayuda a ganar su apoyo.

    
    .bg-full-width.border-top.actividad.bg-color-actividad.mb-0
      .p-4.p-md-5
        #Actividad                
          <Actividad :cuestionario="cuestionario"/>

    .bg-full-width.border-top.color-primario
      .p-4.p-md-5
        h2(data-aos="fade-left") MATERIAL COMPLEMENTARIO
        .row.material-complementario
          .col-12.col-md-6.col-lg-7
            p Los invitamos a explorar el material complementario de este curso, en esta sección encontrará recursos que le permitirán profundizar  y enriquecer su aprendizaje en los temas tratados en esta unidad.

            p.d-flex.my-4
              img.me-3(src='@/assets/componentes/link.svg' :style="{'max-width':'16px'}")
              a(href="https://elibro.net/en/lc/tecnologicadeloriente/titulos/217714" target="_blank" rel="noopener noreferrer") Boada, A. J. & Cardona Montoya, G. Y. M. (2020). La prospectiva: más allá de las proyecciones: (1 ed.). Fondo Editorial CEIPA.

            p.d-flex.my-4
              img.me-3(src='@/assets/componentes/icono-yt.svg' :style="{'max-width':'16px'}")
              a(href="https://youtu.be/lTBKkZwU9mM?si=I4xR2JL0-l57o6Oy" target="_blank" rel="noopener noreferrer") EOI (2013, 27 de mayo) Ecoinnovación (RSC) y Competitividad. [video] YouTube.

            p.d-flex.my-4
              img.me-3(src='@/assets/componentes/link.svg' :style="{'max-width':'16px'}")
              a(href="https://www.obsbusiness.school/blog/estudio-de-viabilidad-de-un-proyecto-estructura-e-importancia" target="_blank" rel="noopener noreferrer") Pérez A. (2021) Estudio de viabilidad de un proyecto: ¿qué es y cómo hacerlo?  Bussines school [blog]

          .col-12.col-md-6.col-lg-3.offset-lg-1
            figure
              img(src='@/assets/componentes/material-complementario.svg', alt='')
</template>

<script>
export default {
  name: 'Tema3',
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
}
</script>

<script>
import Actividad from '@/components/actividad/Actividad.vue'
export default {
  name: 'Tema3',
  components: {
    Actividad,
  },
  data() {
    return {
      cuestionario: {
        tema: 'Pensamiento estratégico y prospectivo',
        titulo: 'Ponte a prueba',
        introduccion:
          'Demuestra lo que aprendiste en esta unidad y pon a prueba tus conocimientos.',
        barajarPreguntas: true,
        preguntas: [
          {
            id: 1,
            texto: '¿Qué se busca con el desarrollo sostenible?',
            imagen: '',
            barajarRespuestas: true,
            opciones: [
              {
                id: 'a',
                texto: 'Maximizar beneficios económicos exclusivamente.',
                esCorrecta: false,
              },
              {
                id: 'b',
                texto:
                  'Equilibrar crecimiento económico, protección ambiental y bienestar social.',
                esCorrecta: true,
              },
              {
                id: 'c',
                texto:
                  'Reducir la participación comunitaria en proyectos organizacionales.',
                esCorrecta: false,
              },
              {
                id: 'd',
                texto: 'Descartar el uso de energías renovables.',
                esCorrecta: false,
              },
            ],
            mensaje_correcto:
              '¡Correcto! El desarrollo sostenible busca equilibrar el crecimiento económico, la protección ambiental y el bienestar social.',
            mensaje_incorrecto:
              'Incorrecto. Revisa el concepto de desarrollo sostenible.',
          },
          {
            id: 2,
            texto:
              '¿Qué empresa es un ejemplo destacado de economía circular en la moda?',
            imagen: '',
            barajarRespuestas: true,
            opciones: [
              { id: 'a', texto: 'Tesla.', esCorrecta: false },
              { id: 'b', texto: 'Ecoalf.', esCorrecta: true },
              { id: 'c', texto: 'Amazon.', esCorrecta: false },
              { id: 'd', texto: 'Microsoft.', esCorrecta: false },
            ],
            mensaje_correcto:
              '¡Correcto! Ecoalf es un ejemplo destacado de economía circular en la moda.',
            mensaje_incorrecto:
              'Incorrecto. Revisa ejemplos de economía circular en la moda.',
          },
          {
            id: 3,
            texto:
              '¿Qué impacto genera la responsabilidad social corporativa (RSC) en la sostenibilidad?',
            imagen: '',
            barajarRespuestas: true,
            opciones: [
              {
                id: 'a',
                texto: 'Aumenta exclusivamente la rentabilidad a corto plazo.',
                esCorrecta: false,
              },
              {
                id: 'b',
                texto:
                  'Promueve prácticas éticas y mejora la relación con comunidades.',
                esCorrecta: true,
              },
              {
                id: 'c',
                texto:
                  'Reduce la importancia de cumplir con normativas ambientales.',
                esCorrecta: false,
              },
              {
                id: 'd',
                texto: 'Limita la creatividad en procesos organizacionales.',
                esCorrecta: false,
              },
            ],
            mensaje_correcto:
              '¡Correcto! La RSC promueve prácticas éticas y mejora la relación con comunidades.',
            mensaje_incorrecto:
              'Incorrecto. Revisa el impacto de la RSC en la sostenibilidad.',
          },
          {
            id: 4,
            texto: '¿Qué componente clave incluye el desarrollo sostenible?',
            imagen: '',
            barajarRespuestas: true,
            opciones: [
              {
                id: 'a',
                texto: 'Sostenibilidad ambiental.',
                esCorrecta: false,
              },
              {
                id: 'b',
                texto: 'Reducción exclusiva de costos operativos.',
                esCorrecta: false,
              },
              {
                id: 'c',
                texto: 'Dependencia de recursos no renovables.',
                esCorrecta: true,
              },
              {
                id: 'd',
                texto: 'Planificación interna aislada.',
                esCorrecta: false,
              },
            ],
            mensaje_correcto:
              '¡Correcto! La dependencia de recursos no renovables es un componente clave a considerar en el desarrollo sostenible.',
            mensaje_incorrecto:
              'Incorrecto. Revisa los componentes clave del desarrollo sostenible.',
          },
          {
            id: 5,
            texto:
              '¿Qué estrategia fomenta la sostenibilidad en las cadenas de suministro?',
            imagen: '',
            barajarRespuestas: true,
            opciones: [
              {
                id: 'a',
                texto: 'Aumento de transporte de alta emisión.',
                esCorrecta: false,
              },
              {
                id: 'b',
                texto: 'Reducción de prácticas colaborativas.',
                esCorrecta: false,
              },
              {
                id: 'c',
                texto: 'Priorizar proveedores con prácticas sostenibles.',
                esCorrecta: true,
              },
              {
                id: 'd',
                texto: 'Exclusión de objetivos ambientales.',
                esCorrecta: false,
              },
            ],
            mensaje_correcto:
              '¡Correcto! Priorizar proveedores con prácticas sostenibles fomenta la sostenibilidad en las cadenas de suministro.',
            mensaje_incorrecto:
              'Incorrecto. Revisa las estrategias para fomentar la sostenibilidad en las cadenas de suministro.',
          },
        ],
        mensaje_final_aprobado:
          '¡Felicidades! Has superado la prueba con éxito.',
        mensaje_final_reprobado:
          'Te recomendamos repasar nuevamente la unidad para reforzar los conceptos clave antes de volver a intentarlo.',
      },
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
}
</script>

<style lang="sass">
.bg-color-actividad
  background-color: #EBF1F5
</style>
