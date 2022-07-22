<template>
  <header :class="{'scrolledNav' : scrollPosition}">
    <nav>
      <div class="branding">
        <a href="https://metaform.ru/"><img src="@/assets/logo/metaform.png" alt="Metaform logo" /></a>
      </div>
      <ul v-show="!mobile" class="navigation">
        <li><router-link class="link" :to="{name: 'Home'}">Главная</router-link></li>
        <li><router-link class="link" :to="{name: ''}">О компании</router-link></li>
        <li><router-link class="link" :to="{name: ''}">Каталог</router-link></li>
        <li><router-link class="link" :to="{name: ''}">Контакты</router-link></li>
      </ul>
      <div class="icon">
        <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active' : mobileNav}"></i>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li><router-link class="link" :to="{name: 'Home'}">Главная</router-link></li>
          <li><router-link class="link" :to="{name: ''}">О компании</router-link></li>
          <li><router-link class="link" :to="{name: ''}">Каталог</router-link></li>
          <li><router-link class="link" :to="{name: ''}">Контакты</router-link></li>
      </ul>
      </transition>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'navigation',
  data() {
    return {
      scrollPosition: null,
      mobile: false,
      mobileNav: false,
      windowWidth: null
    };
  },
  created() {
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen();
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav; 
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if(this.windowWidth <= 820) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    } 

  },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header {
    background: url("../assets/background/bgpattern1.png") repeat;
    //background-color: rgba(0,0,0,0.8);
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: .5s ease all;
    nav {
      position: relative;
      display: flex;
      flex-direction: row;
      padding: 12px 0;
      width: 90%;
      margin: 0 auto;
      @media(min-width: 1140px) {
        max-width: 1140px;
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
        img {
          transition: .5s ease all;
        }
      }

      .navigation {
        display: flex;
        align-items: center;
        flex: 1;
        justify-content: flex-end;
      }

      .icon {
        display: flex;
        align-items: center;
        position: absolute;
        top: 0;
        right: 24px;
        height: 100%;

        i {
          cursor: pointer;
          font-size: 24px;
          color: #fff;
          transition: 0.8s ease all;
        } 
      }

      .icon-active {
        transform: rotate(0.25turn);
      }

      .dropdown-nav {
        display: flex;
        flex-direction: column;
        position: fixed;
        width: 100%;
        max-width: 250px;
        height: 100%;
        background-color: #fff;
        top: 0;
        left: 0;

        li {
          margin-left: 0;
          .link {
            color: #000;
          }
        }

      }
    }
  }

</style>
