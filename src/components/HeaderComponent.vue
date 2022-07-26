<template lang='pug'>
div.container.header-container
  div.header__top-part
    a(href='/').header__logo
    form.header__form
      input(type="text", id="search").header__input
      button(type="submit").header__btn Поиск
  button.header__btn-burger(@click="show = !show")
  nav.header__nav(:class="{'header__nav--opacity': !show}")
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
    
    data() {
        return {
            show: false,
        }
    },
    
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.header-container {
  padding-top: 25px;
}

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
    margin-bottom: 20px;
  }

.header__input {
  width: 213px;
  border: 1px solid $grayTextColor;
  margin-right: 10px;
  padding: 2px 10px;
  color: $grayTextColor;
  font-size: 11px;
}

.header__btn {
  font-size: 11px;
  border: none;
  background-color: transparent;
  color: $grayTextColor;

  &:hover {
    color: black;
  }
}

.header__list {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 25px;
  border-bottom: 1px solid $grayTextColor;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.header__item {
  position: relative;
  &:not(:last-child)::after {
    content: '|';
    position: absolute;
    top: 2px;
    right: -15px;
    color: $grayTextColor;
  }
}

.header__link {
  font-size: 11px;

  &:hover {
    color: black;
  }
}

.header__link {
  text-transform: uppercase;
  color: $grayTextColor;
}

.header__btn-burger {
  display: none;
}

@media (max-width: 830px) {

.header-container {
  position: relative;
}

.header__nav {
  display: flex;
}

.header__btn-burger {
  display: block;
  position: absolute;
  right: 50px;
  top: 20px;
  width: 30px;
  height: 30px;
  border: none;
  background: transparent url('../assets/burger-menu.svg') no-repeat center;
}

.header__btn-burger--opacity {
  display: none;
}

.header__top-part {
  flex-direction: column;
  padding: 0 30px;
}

.header__list {
  flex-direction: column;
  position: absolute;
  background-color: white;
  width: 100%;
  top: 45px;
}

.header__nav--opacity {
  display: none;
}

.header__item:not(:last-child)::after {
  display: none;
}

}
</style>
