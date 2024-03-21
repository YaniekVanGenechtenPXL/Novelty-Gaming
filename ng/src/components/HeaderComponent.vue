<template>
  <header>
    <img id="img_logoExt" src="../assets/logos/Logo_Black_Ext.png" alt="Logo" />
    <img id="img_logoMin" src="../assets/logos/Logo_Black.png" alt="Logo" />
    <nav>
      <div id="nav__main" v-if="NavMainItemVisible === 'true'">
        <ul>
          <NavMainItem v-for="(item, index) in navItems" :key="index" :item="item" />
        </ul>
      </div>
      <div id="nav__sub">
        <ul>
          <NavSubItem v-for="(item, index) in navSubItems" :key="index" :item="item" @click="toggleMobileMenu" />
        </ul>
      </div>
    </nav>
  </header>
</template>
  
  <script>
import NavMainItem from './NavMainItem.vue'
import NavSubItem from './NavSubItem.vue'

export default {
  components: {
    NavMainItem,
    NavSubItem
  },
  data() {
    return {
      NavMainItemVisible: 'true',

      navItems: [
        { label: 'Home', url: '/', icon: 'src/assets/icons/home.png' },
        { label: 'Keycaps', url: '/', icon: 'src/assets/icons/keycaps.png' },
        { label: 'Keyboards', url: '/', icon: 'src/assets/icons/keyboard.png' },
        { label: 'Mousepads', url: '/', icon: 'src/assets/icons/mousepad.png' },
        { label: 'Cables', url: '/', icon: 'src/assets/icons/cable.png' },
        { label: 'About us', url: '/', icon: 'src/assets/icons/about.png' }
      ],
      navSubItems: [
        { label: 'Favourite', url: '/', icon: 'src/assets/icons/favourite.png' },
        { label: 'Shopping Cart', url: '/', icon: 'src/assets/icons/cart.png' },
        { label: 'Account', url: '/', icon: 'src/assets/icons/account.png' },
        { label: 'Main navigation', url: '/', icon: 'src/assets/icons/menu.png', click: 'toggleMobileMenu' }
      ]
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
  background-color: #FFF;
  img {
    height: 70px;
  }
  img#img_logoMin {
    display: none;
  }
  nav {
    margin: 0 20px 0 auto;
    display: flex;
    gap: 80px;
    div#nav__main, div#nav__sub {
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
  }
}
</style>