<template>
  <header class="header">
    <div class="header__wrap">
      <ul class="header__wrap-nav">
        <li class="header__wrap-nav-item">
          <a href="./" class="header__wrap-nav-link">
            <img src="@/assets/images/logo.png" alt="Логотип" class="header__logo" />
          </a>
        </li>
        <li v-for="(link, index) in linksArray" :key="index" class="header__wrap-nav-item">
          <a :href="link.url" class="header__wrap-nav-link">{{ link.text }}</a>
        </li>
      </ul>
      <div class="header__wrap-info">
        <a href="tel:+74951184442" class="header__phone"> +7 495 118-44-22</a>
        <button class="header__wrap-login">Вход</button>
        <BaseButton text="Регистрация"/>
      </div>
    </div>
  </header>
</template>

<script>
import BaseButton from '../components/ui/BaseButton.vue';
export default {
  components: {
    BaseButton,
  },
  data() {
    return {
      linksArray: [
        { text: 'Тарифы', url: 'https://example.com/link1' },
        { text: 'Контакты', url: 'https://example.com/link2' },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  padding-left: 374px;
  align-items: center;
  width: 100%;
  height: 60px;
  background: linear-gradient(90deg, #000 30%, #1c2734 73%);
    &__phone {font-family: var(--font-family);
        font-weight: 700;
        font-size: 1.12rem;
        color: #fff;
    }
}

.header__wrap {
  max-width: var(--site-width);
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &-nav {
    display: flex;
    align-items: center;
    gap: 30px;

    &-item {
      list-style: none;
    }

    &-link {
      font-family: var(--font-family);
      font-weight: 400;
      font-size: 1.12rem;
      color: #fff;
      text-decoration: none;
    }
  }

  &__logo {
    max-height: 100%;
  }

  &-info {
    display: flex;
    align-items: center;
    gap: 30px;
  }
  &-login{
    font-family: var(--font-family);
    font-size: 1.12rem;
    color: #fff;
  }
}
</style>