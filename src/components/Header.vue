<template>
  <div class="header">
    <div class="header__logo"></div>
    <div class="header__title">
      <p class="header__title--spacing">CURSO AUTOINSTRUCIONAL</p>
      <p class="header__title--blue">
        Enfrentamento da Covid-19 no Sistema Prisional
      </p>
      <p>Carga Horária: XX horas</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header {
  padding: 32px;
  display: flex;
}
.header__logo {
  width: 658px;
  height: 341px;
  left: 0px;
  top: 46px;
  background: url(../assets/img-cerca.png);
  background-repeat: no-repeat;
  border-radius: 0px 30px 30px 0px;
  flex: 1;
}
.header__title {
  margin: 32px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.header__title--spacing {
  font-size: 16px;
  font-weight: 400;
  line-height: 26px;
  letter-spacing: 0.6em;
  text-align: center;
  padding-bottom: 8px;
}
.header__title--blue {
  font-weight: 900;
  font-size: 42px;
  align-items: center;
  text-align: center;
  color: #2f80ed;
  padding-bottom: 8px;
}

@media (max-width: 1024px) {
  .header {
    display: flex;
    flex-direction: column;
    width: 100%;
    margin: 0;
    align-items: center;
  }
  .header__logo {
    padding-bottom: 300px;
    width: 100%;
    border-radius: 30px;
    background-size: cover;
  }
  .header__title--spacing {
    font-size: 12px;
  }
  .header__title--blue {
    font-size: 18px;
  }
}

@media (max-width: 320px) {
  .header__title {
    margin: 16px;
  }
}
</style>
