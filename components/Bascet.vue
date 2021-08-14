<template>
  <div class="bascet" :class="{active:this.$parent.bascetOpen}">
    <div class="bascet__overlay"></div>
    <div class="bascet__wrap">
        <div class="bascet__wrap__header">
          <div class="bascet__wrap__header__title">Корзина</div>
          <div class="bascet__wrap__header__close" @click="$parent.bascetOpen = !$parent.bascetOpen">+</div>
        </div>



        <div class="bascet__wrap__body" v-if="count > 0">
          <div class="bascet__wrap__desc">Товары в корзине</div>
          <BascetCart/>
          <BascetCart/>
          <BascetCart/>
        </div>

        <div class="bascet__wrap__body" v-else>
          <div class="bascet__empty">Пока что вы ничего не добавили в корзину</div>
          <button class="bascet__submit" @click="$parent.bascetOpen = !$parent.bascetOpen">Перейти к выбору</button>
        </div>

        <BascetForm v-if="count > 0" />
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      count: 0
    }
  }
}
</script>

<style>

.bascet{
  position: fixed;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  z-index: 1000;
  visibility: hidden;

}

.bascet.active{
  visibility: visible;

}

.bascet__overlay{
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  background: #FFFFFF;
  opacity: 0.8;
}

.bascet__wrap{
  position: absolute;
  width: 460px;
  height: 100vh;
  right: 0;
  top: 0;
  background: #FFFFFF;
  box-shadow: -4px 0px 16px rgba(0, 0, 0, 0.05);
  border-radius: 8px 0px 0px 8px;
  overflow-y:auto;
}

.bascet__wrap__header{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 52px 48px 0 48px;
}

.bascet__wrap__header__title{
  font-size: 32px;
  font-weight: 700;
}

.bascet__wrap__header__close{
  font-size: 40px;
  transform: rotate(45deg);
  cursor: pointer;
}

.bascet__wrap__body{
  margin-top: 16px;
  margin-left: 48px;
  margin-right: 48px;

}

.bascet__wrap__desc{
  margin-bottom: 8px;
  font-size: 18px;
  line-height: 23px;
  color: #59606D;

}

</style>
