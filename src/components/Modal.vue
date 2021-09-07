<template>
  <transition name="modal">
    <div class="modal__mask">
      <div class="modal__wrapper">
        <div class="modal__container">
          <div class="modal__header">
            <div class="modal__button" @click="$emit('close')"></div>
          </div>

          <div class="modal__body">
            <slot name="body">
              default body
            </slot>
          </div>

          <div class="modal__footer">
            <slot name="footer">
              
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>
<script>
export default {
  name: "Modal",
  created() {},
  methods: {},
};
</script>
<style scoped>
.modal__mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 254, 254, 0.84);
  display: table;
  transition: opacity 0.3s ease;
}

.modal__wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal__container {
  max-width: 940px;
  height: 274px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: rgba(47, 128, 237, 0.6);
  border-radius: 30px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal__header {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.modal__body {
  margin: 16px 0;
}

.modal__default-button {
  float: right;
}

.modal__enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal__enter .modal__container,
.modal-leave-active .modal__container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}

.modal__button {
  cursor: pointer;
  width: 42px;
  height: 42px;
  background: url(../assets/icon-close.svg);
  background-repeat: no-repeat;
}
@media (max-width: 860px) {
  .modal__container {
    max-width: 640px;
    min-width: 300px;
    height: auto;
  }
}
</style>
