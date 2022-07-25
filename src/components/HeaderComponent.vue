<template lang='pug'>
div.container
  div.header__top-part
    a(href='/').header__logo
    form.header__form
      input(type="text", id="search").header__input
      button(type="submit").header__btn Поиск
  nav.header__nav
    ul.header__list
      li.header__item
        a(href="").header__link Аукционные каталоги
      li.header__item
        a(href="").header__link Коллекционирование
      li.header__item
        a(href="").header__link Колоbook
      li.header__item
        a(href="").header__link Разное
      li.header__item
        a(href="").header__link Авторы
      li.header__item
        a(href="").header__link Контакты

</template>


<script>
export default {
  name: 'HeaderComponent',
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.header__logo {
  display: block;
  width: 340px;
  height: 81px;
  background: transparent url('../assets/logo.png') no-repeat center;
}

.header__top-part {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

.header__input {
  border: 1px solid $grayTextColor;
  margin-right: 10px;
}

.header__btn {
  font-size: 11px;
  border: none;
  background-color: transparent;
  color: $grayTextColor;
}

.header__nav {
  margin-bottom: 10px;
}

.header__list {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 15px;
  border-bottom: 1px solid $grayTextColor;
  padding-bottom: 10px;
}

.header__item {
  position: relative;
  &:not(:last-child)::after {
    content: '|';
    position: absolute;
    top: -1px;
    right: -9px;
    color: $grayTextColor;
  }
}

.header__link {
  font-size: 11px;
}

.header__link {
  text-transform: uppercase;
  color: $grayTextColor;
}
</style>
