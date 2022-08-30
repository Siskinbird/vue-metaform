<template>
  <header :class="{'scrolledNav' : scrollPosition}">
    <nav class="container">
      <div class="branding">
        <a href="https://metaform.ru/"><img src="@/assets/logo/metaform_full.svg" alt="Metaform logo" /></a>
      </div>
      <ul v-show="!mobile" class="navigation">
        <li><a href="#" class="link">Главная</a></li>
        <li><a href="#" class="link">О компании</a></li>
        <li><a href="#" class="link">Каталог</a></li>
        <li><a href="#" class="link">Контакты</a></li>
      </ul>
      <div class="icon">
        <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active' : mobileNav}"></i>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
        <li><a href="#" class="link">Главная</a></li>
        <li><a href="#" class="link">О компании</a></li>
        <li><a href="#" class="link">Каталог</a></li>
        <li><a href="#" class="link">Контакты</a></li>
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
      if(this.windowWidth <= 865) {
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
    z-index: 6;
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
        cursor: pointer;
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
