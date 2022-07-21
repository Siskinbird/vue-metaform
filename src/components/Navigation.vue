<template>
  <header :class="{'scrolledNav' : scrollPosition}">
    <nav>
      <div class="branding">
        <img src="@/assets/logo/metaform.png" alt="Metaform logo">
      </div>
      <ul v-shov="!mobile" class="navigation">
        <li><router-link class="link" :to="{name: 'Home'}">Главная</router-link></li>
        <li><router-link class="link" :to="{name: 'About'}">О компании</router-link></li>
        <li><router-link class="link" :to="{name: 'Production'}">Каталог</router-link></li>
        <li><router-link class="link" :to="{name: 'Contacts'}">Контакты</router-link></li>
      </ul>
      <div class="icon">
        <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active' : mobileNav}"></i>
      </div>
      <transition name="mobile-nav">
        <ul v-shov="mobileNav" class="dropdown-nav">
          <li><router-link class="link" :to="{name: 'Home'}">Главная</router-link></li>
          <li><router-link class="link" :to="{name: 'About'}">О компании</router-link></li>
          <li><router-link class="link" :to="{name: 'Production'}">Каталог</router-link></li>
          <li><router-link class="link" :to="{name: 'Contacts'}">Контакты</router-link></li>
      </ul>
      </transition>
    </nav>
  </header>

</template>

<script>
export default {
  name: 'Navigation'
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header {
    background: url("../assets/background/bgpattern1.png") repeat;
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: .5s ease all;
    nav {
      display: flex;
      flex-direction: row;
      padding: 12px 0;
      width: 90%;
      margin: 0 auto;
      @media(min-width: 1140px) {
        max-width: 1140px;
      }
    }

    ul,
    .link {
      font-weight: 500;
      color: #fff;
      list-style: none;
      text-decoration: none;
    }
    li {
      text-transform: uppercase;
      padding: 16px;
      margin-left: 16px;
    }
    .link {
      font-size: 14px;
      transition: .5s ease all;
      padding-bottom: 4px;
      border-bottom: 1px solid transparent;
      &:hover {
        color: #00afea;
        border-color: #00afea;
      }
    }
    .branding {
      display: flex;
      align-items: center;
    }
  }
</style>
