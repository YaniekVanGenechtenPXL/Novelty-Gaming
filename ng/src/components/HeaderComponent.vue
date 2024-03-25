<template>
  <header>
    <img id="img_logoExt" src="../assets/logos/Logo_Black_Ext.png" alt="Logo" />
    <img id="img_logoMin" src="../assets/logos/Logo_Black.png" alt="Logo" />
    <nav>
      <div id="nav__main">
        <ul>
          <NavMainItem v-for="(item, index) in navItems" :key="index" :item="item" />
        </ul>
      </div>
      <div id="nav__sub">
        <ul>
          <NavSubItem
            v-for="(item, index) in navSubItems"
            :key="index"
            :item="item"
            @click="toggleMobileMenu"
          />
        </ul>
      </div>
      <div id="nav__main__mobile" :style="dynamicStyle">
        <ul>
          <NavMainItem v-for="(item, index) in navItems" :key="index" :item="item" />
        </ul>
      </div>
    </nav>
  </header>
</template>
  
  <script>
import NavMainItem from './NavMainItem.vue'
import NavSubItem from './NavSubItem.vue'

import homeIcon from '../assets/icons/home.png';
import keycapsIcon from '../assets/icons/keycaps.png';
import keyboardIcon from '../assets/icons/keyboard.png';
import mousepadIcon from '../assets/icons/mousepad.png';
import cableIcon from '../assets/icons/cable.png';
import aboutIcon from '../assets/icons/about.png';

import favouriteIcon from '../assets/icons/favourite.png';
import cartIcon from '../assets/icons/cart.png';
import accountIcon from '../assets/icons/account.png';
import menuIcon from '../assets/icons/menu.png';


export default {
  components: {
    NavMainItem,
    NavSubItem
  },
  data() {
    return {
      navMainMobileVisible: 'false',
      dynamicStyle: {
        top: '-300px'
      },

      navItems: [
        { label: 'Home', url: '/', icon: homeIcon },
        { label: 'Keycaps', url: '/', icon: keycapsIcon },
        { label: 'Keyboards', url: '/', icon: keyboardIcon },
        { label: 'Mousepads', url: '/', icon: mousepadIcon },
        { label: 'Cables', url: '/', icon: cableIcon },
        { label: 'About us', url: '/', icon: aboutIcon }
      ],
      navSubItems: [
        { label: 'Favourite', url: '/', icon: favouriteIcon },
        { label: 'Shopping Cart', url: '/', icon: cartIcon },
        { label: 'Account', url: '/', icon: accountIcon },
        {
          label: 'Main navigation',
          url: '/',
          icon: menuIcon,
          click: 'toggleMobileMenu'
        }
      ]
    }
  },
  methods: {
    toggleMobileMenu() {
      if (this.navMainMobileVisible === 'true') {
        this.dynamicStyle = { top: '-300px' }
        this.navMainMobileVisible = 'false'
      } else {
        this.dynamicStyle = { top: '90px' }
        this.navMainMobileVisible = 'true'
      }
    }
  }
}
</script>
  

<style lang="scss" scoped>
header {
  width: 100vw;
  height: 95px;
  padding: 0 40px;
  display: flex;
  align-items: center;
  position: fixed;
  top: 0;
  background-color: var(--white);
  z-index: 100;
  img {
    height: 70px;
  }
  img#img_logoMin,
  div#nav__main__mobile {
    display: none;
  }
  nav {
    margin: 0 20px 0 auto;
    display: flex;
    gap: 80px;
    div#nav__main,
    div#nav__sub {
      ul {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        gap: 20px;
      }
    }
    div#nav__sub {
      ul {
        position: relative;
        top: 3px;
      }
    }
  }
}

@media (max-width: 1220px) {
  header {
    img#img_logoExt {
      display: none;
    }
    img#img_logoMin {
      display: block;
    }
  }
}

@media (max-width: 1100px) {
  header {
    div#nav__main {
      display: none;
    }
    div#nav__sub {
      ul {
        gap: 0 !important;
      }
    }
    div#nav__main__mobile {
      display: block;
      position: absolute;
      background-color: var(--white);
      top: 90px;
      left: 0;
      width: 100vw;
      padding: 20px 10vw;
      z-index: 9;
      box-shadow: 0px 3px 6px rgba($color: #000000, $alpha: 0.16);
      transition: 0.3s ease;
      ul {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
      }
    }
  }
}
</style>