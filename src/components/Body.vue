<template>
  <div class="body">
    <div class="body__logo">
      <img alt="Logo Fundação Oswaldo Cruz" src="../assets/img-logo.svg" />
    </div>
    <div class="body__introduction">
      <div class="texto">
        <span>APRESENTAÇÃO</span>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec varius
          laoreet magna. In ac blandit ipsum, nec volutpat tortor. Maecenas
          feugiat, elit nec semper tempus, lorem erat dictum mauris, at
          vulputate nulla nisl consequat risus. Quisque mollis massa quis cursus
          hendrerit. Proin a porttitor enim, eu consequat ante. Curabitur ligula
          mauris, ornare et quam non, blandit vestibulum lorem. Curabitur in
          ipsum id ligula bibendum hendrerit et sit amet ligula. Aenean eu
          pretium tellus, ac ornare quam. Proin dictum dignissim ipsum quis
          tristique.
        </p>
      </div>
      <div class="image"></div>
    </div>
    <div class="body__courses">
      <div
        v-for="(item, index) in conteudo"
        :key="index"
        :class="`course-${index}`"
      >
        <span class="title">UNIDADE</span>
        <span class="subtitle">{{ item.titulo }}</span>
        <div class="buttons">
          <div
            class="button button__ementa"
            @click="(mostrarEmenta = true), adicionarEmenta(item.ementa)"
          ></div>
          <div
            class="button button__objetivo"
            @click="mostrarObjetivos = true"
          ></div>
        </div>

        <Modal v-if="mostrarEmenta" @close="mostrarEmenta = false">
          <div slot="body">
            <span class="modal__title">EMENTA</span>
            <span class="modal__content">{{ ementa }}</span>
          </div>
        </Modal>
        <Modal v-if="mostrarObjetivos" @close="mostrarObjetivos = false">
          <ul v-for="i in item.objetivos" :key="i" slot="body">
            <li>{{ i }}</li>
          </ul>
        </Modal>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "./Modal.vue";
export default {
  components: { Modal },
  name: "Body",
  data() {
    return {
      mostrarEmenta: false,
      mostrarObjetivos: false,
      ementa: "",
      conteudo: [
        {
          titulo: "Coronavírus e o Sistema Prisional",
          ementa:
            "Direitos humanos e à saúde no enfrentamento da pandemia. Caracterização da população carcerária e da organização do sistema prisional. Doenças respiratórias prevalentes, com ênfase na COVID-19, em ambiente prisional e suas consequências para a população privada de liberdade e para os trabalhadores. Experiências exitosas e legislação para a COVID-19.",
          objetivos: [
            "Reconhecer os direitos à vida e à saúde como direitos essenciais da população privada de liberdade e dos trabalhadores do sistema prisional, no enfrentamento da pandemia;",
            "Entender a composição da população carcerária e a organização do sistema prisional brasileiro;",
            "Compreender o comportamento das doenças respiratórias no ambiente prisional.",
          ],
        },
        {
          titulo: "Plano de Contingência no Ambiente Prisional",
          ementa:
            "Vigilância de Síndrome Gripal e Síndrome Respiratória Aguda Grave (SRAG). Investigação de surtos. Medidas para contenção e mitigação do surto por COVID-19. Medidas de biossegurança, de mitigação e sanitárias no ambiente prisional. Experiências exitosas e legislação para a COVID-19.",
          objetivos: [
            "Reconhecer a importância das ações de vigilância para prevenção e controle de síndromes gripais e respiratórias no sistema prisional;",
            "Entender as boas práticas relacionadas à investigação de surtos epidêmicos; ",
            "Entender as medidas de contenção e mitigação de um surto de COVID-19.",
          ],
        },
      ],
    };
  },
  methods: {
    adicionarEmenta(titulo) {
      this.ementa = titulo;
    },
  },
};
</script>
<style scoped>
.body {
  padding: 32px;
}
.body__logo {
  padding: 16px;
}
.body__introduction {
  background: #bfeafd;
  border-radius: 0px 30px 30px 0px;
  display: flex;
  margin-top: 48px;
  max-width: 1136px;
}
.texto {
  flex: 1;
  padding: 32px 32px 32px 96px;
}
.texto span {
  font-size: 18px;
  line-height: 21px;
  letter-spacing: 0.6em;
  color: #2f80ed;
  padding: 16px;
  display: flex;
  align-items: center;
  text-align: center;
}
.texto p {
  padding: 16px;
  text-align: left;
}
.image {
  flex: 1;
  background: url(../assets/img-3548878.png);
  background-repeat: no-repeat;
  margin: 32px;
}
.body__courses {
  margin-top: 48px;
}
.body__courses .title {
  font-size: 26px;
  line-height: 30px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.5em;
  color: #333333;
}

.body__courses .subtitle {
  font-weight: bold;
  font-size: 32px;
  line-height: 37px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #2f80ed;
}
div[class^="course-"] {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 48px;
}

.buttons {
  display: flex;
}
.button {
  height: 72px;
  margin: 16px;
}

.button:hover {
  cursor: pointer;
  opacity: 0.5;
}
.button__ementa {
  width: 62px;
  background: url(../assets/button-ementa.svg);
  background-repeat: no-repeat;
}
.button__objetivo {
  width: 108px;
  background: url(../assets/button-objetivo.svg);
  background-repeat: no-repeat;
}
.modal__title {
  font-size: 22px;
  line-height: 26px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.2em;
  color: #ffffff;
}
.modal__content {
  font-size: 17px;
  line-height: 21px;
  display: flex;
  align-items: center;
  color: #ffffff;
}
</style>
