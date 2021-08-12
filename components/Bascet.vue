<template>
  <div class="bascet">
    <div class="bascet__overlay"></div>
      <div class="bascet__wrap">
        <div class="bascet__wrap__header">
          <div class="bascet__wrap__header__title">Корзина</div>
          <div class="bascet__wrap__header__close">+</div>
        </div>

        <div class="bascet__wrap__desc">Товары в корзине</div>

        <div class="bascet__wrap__body">
          <div class="bascet__wrap__body__cart"></div>
        </div>

        <div class="bascet__wrap__form">

        </div>
      </div>
  </div>
</template>



<style>

.bascet{
  position: fixed;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  z-index: 1000;
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
  height: 100%;
  right: 0;
  top: 0;
  background: #FFFFFF;
  box-shadow: -4px 0px 16px rgba(0, 0, 0, 0.05);
  border-radius: 8px 0px 0px 8px;
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
}

.bascet__wrap__body{
  margin-top: 16px;
  margin-left: 48px;
}

.bascet__wrap__desc{
  margin-left: 48px;
  font-size: 18px;
  line-height: 23px;
  color: #59606D;
}

.bascet__wrap__body__cart{
  width: 364px;
  height: 120px;
  background: #FFFFFF;
  box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.05);
  border-radius: 8px;
}

</style>
