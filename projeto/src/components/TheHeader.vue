<template>
  <div id="header" class="container-fluid p-0">
    <nav class="main-nav-container w-100 h-100 d-flex justify-content-center">
      <ul
        v-for="nav in navItems"
        :key="nav.id"
        class="desktop-nav-container h-100"
      >
        <li
          class="d-flex justify-content-center align-items-center h-100 px-2"
          :class="nav.id === 'user-menu' ? 'user-menu-bg' : 'nav-item'"
        >
          <div v-if="nav.id === 'user-menu'">
            <span>{{ nav.text }}</span>
            <span v-if="nav.id === 'user-menu'">▼</span>
          </div>

          <div v-else>
            <a :href="`#${nav.id}`" class="nav-link text-decoration-none">
              <span>{{ nav.text }}</span>
            </a>
          </div>
        </li>
      </ul>

      <div class="mobile-nav-container w-100">
        <div
          class="h-100 px-4 d-flex justify-content-between align-items-center"
        >
          <div
            class="mobile-logo-container d-flex justify-content-center align-items-center"
          >
            <img
              src="../assets/logo-mobile.png"
              alt=""
              class="hellmanns-logo"
            />
          </div>

          <button class="menu-button" @click="toggleMenu()">
            <svg
              style="height: 32px"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
            >
              <title>menu</title>
              <path d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z" />
            </svg>
          </button>

          <div v-if="showMenu" class="menu-container p-2">
            <ul
              v-for="nav in navItems"
              :key="nav.id"
              class="d-flex justify-content-center p-0 m-0 py-2"
            >
              <li class="nav-item">
                <div v-if="nav.id === 'user-menu'" class="user-menu-link">
                  <span>Perfil</span>
                </div>

                <div v-else>
                  <a
                    :href="`#${nav.id}`"
                    class="nav-link text-decoration-none"
                    @click="showMenu = false"
                  >
                    <span>{{ nav.text }}</span>
                  </a>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "TheHeader",

  data() {
    return {
      navItems: [
        { id: "home", text: "Home" },
        { id: "how-to-participate", text: "Como participar" },
        { id: "prizes", text: "Prêmios" },
        { id: "products", text: "Produtos participantes" },
        { id: "recipes", text: "Receitas" },
        { id: "nba-pills", text: "Pílulas NBA" },
        { id: "winners", text: "Ganhadores" },
        { id: "user-menu", text: "Olá, Ana" },
      ],

      showMenu: false,
    };
  },

  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style scoped>
#header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 64px;
  background-color: var(--secondary-color);
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
  font-size: 18px;
  line-height: 20px;
  box-shadow: 0 10px 16px -6px rgba(0, 0, 0, 0.6);
  z-index: 100;
}

.mobile-nav-container {
  display: none;
}

.nav-item {
  max-width: 174px;
}

.nav-link {
  color: var(--primary-color);
}

.user-menu-bg {
  background-color: var(--primary-color);
  color: var(--secondary-color);
}

.user-menu-link {
  background-color: var(--primary-color);
  color: var(--secondary-color);
  padding: 0 6px;
}

@media screen and (max-width: 1128px) {
  .desktop-nav-container {
    display: none;
  }

  .mobile-nav-container {
    display: block;
  }

  .menu-button {
    background-color: var(--secondary-color);
    border: none;
    fill: var(--primary-color);
    transition: all 250ms;
  }

  .menu-button:hover {
    fill: var(--primary-dark-color);
  }

  .mobile-logo-container {
    width: 80px;
  }

  .hellmanns-logo {
    width: 100%;
  }

  .menu-container {
    position: absolute;
    top: 60px;
    right: 10px;
    background-color: #fff;
    border: none;
    border-radius: 32px;
    padding: 10px;
    box-shadow: 10px 10px 16px -6px rgba(0, 0, 0, 0.6);
  }

  .menu-container li {
    list-style: none;
    font-size: 16px;
  }

  .user-menu-link {
    background-color: transparent;
    color: var(--primary-color);
  }
}
</style>
