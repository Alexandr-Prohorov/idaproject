<template>
  <div class="bascet__wrap__form">
    <div class="bascet__wrap__desc">Оформить заказ</div>
    <input type="text" class="bascet__input" id="input__name" placeholder="Ваше имя" required>
    <input type="text" class="bascet__input" id="input__name" placeholder="Телефон" required>
    <input type="text" class="bascet__input" id="input__name" placeholder="Адрес" required>
    <button type="submit" class="bascet__submit active">Отправить</button>
  </div>
</template>

<style>

.bascet__wrap__form{
  display: flex;
  flex-direction: column;
}

.bascet__input{
  background: #F8F8F8;
  border-radius: 8px;
  border: none;
  width: 364px;
  height: 50px;
  font-family: PT Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 21px;
  margin-left: 48px;
  margin-bottom: 8px;
  margin-top: 8px;
}

.bascet__submit{
  width: 364px;
  height: 50px;
  background: #1F1F1F;
  border-radius: 8px;
  color: #FFFFFF;
  border: none;

  margin-top: 16px;
  cursor: pointer;
}

.bascet__submit.active{
  background: #59606D;
}
</style>
