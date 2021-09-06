<template>
  <div class="header">
    <div class="header__logo" ></div>
    <div class="header__title" >
      <p class="header__title--spacing"> CURSO AUTOINSTRUCIONAL </p>
      <p class="header__title--blue">Enfrentamento da Covid-19 no Sistema Prisional</p>
      <p class="header__title--simple"> Carga Horária: XX horas</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  created() {
    
  },
  methods:{
    
  }
}
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
.header__title--spacing{
  font-family: Roboto;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 26px;
  letter-spacing: 0.6em;
  text-align: center;

}
.header__title--blue{
  font-family: Roboto;
  font-style: normal;
  font-weight: 900;
  font-size: 42px;
  align-items: center;
  text-align: center;
  color: #2F80ED;
}

@media (max-width:800px) {
  .header {
    display: flex;
    flex-direction: column;
  }
  .header__title--spacing{
    font-size: 14px;
  }
  .header__title--blue{
    font-size: 28px;
  }
}

</style>
