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
nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
