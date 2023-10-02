<template>
  <header>
    <nav id="menu">
      <div @click="clickMenu" class="mobile-menu">
        <img src="@/assets/images/bars.svg" alt="" />
      </div>
      <div class="logo">
        <div class="l-container">
          <img src="@/assets/images/logo.svg" alt="" />
          <p>Web builders</p>
        </div>
      </div>
      <ul class="nav-list">
        <li>
          <router-link @click="clickMenu" to="/" exact>Início</router-link>
        </li>
        <li>
          <router-link @click="clickMenu" to="/sobre" exact>Sobre</router-link>
        </li>
        <li>
          <router-link @click="clickMenu" to="/proposito" exact
            >Propósito</router-link
          >
        </li>
        <li>
          <router-link @click="clickMenu" to="/Serviços" exact
            >Segmentos</router-link
          >
        </li>
        <li>
          <router-link @click="clickMenu" to="/contato" exact
            >Contato</router-link
          >
        </li>
      </ul>
      <button class="btn-primary">Ligue para nós</button>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      text: null,
    };
  },
  methods: {
    clickMenu() {
      const nav = document.querySelector(".nav-list");
      if (!nav.classList.contains("active")) {
        nav.classList.toggle("active");
      } else {
        nav.classList.remove("active");
      }
    },
  },
};
</script>

<style lang="scss">
header {
  width: 100%;
  z-index: 3;
  @media (max-width: 999px) {
    z-index: 1;
    top: 0;
  }
  nav {
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 80px;
    background: $background;
    @media (max-width: 999px) {
      width: 95%;
      justify-content: flex-start;
      column-gap: 2%;
      padding-left: 1%;
      height: 80px;
    }
    .logo {
      font-size: 22px;
      letter-spacing: 4px;
      text-transform: uppercase;
      text-decoration: none;
      display: flex;
      align-items: center;
      @media (max-width: 999px) {
        font-size: 16px;
        letter-spacing: 2px;
        z-index: 2;
      }

      @media (max-width: 999px) {
        font-size: normal;
        padding-right: 16px;
      }
      .l-container {
        display: flex;
        align-items: center;
        img {
          width: 60px;
          height: 50px;
        }
        p {
          color: $dark;
          font-weight: 600;
          margin-left: 24px;
          font-size: 20px;
          @media (max-width: 999px) {
            font-size: 14px;
            padding-right: 10px;
          }
        }
      }
    }

    .mobile-menu {
      width: 48px;
      height: 48px;
      display: none;
      cursor: pointer;
      border-radius: 50%; /* Tornar a div redonda */
      cursor: pointer; /* Mostrar o cursor de mão quando passar o mouse */
      transition: background-color 0.3s ease;
      @media (max-width: 999px) {
        display: block;
        z-index: 2;
        padding: 5px;
        &:hover {
          background-color: $grey-2;
          opacity: 0.7;
        }
      }

      div {
        width: 32px;
        height: 2px;
        background: $dark;
        margin: 8px;
      }
    }

    .nav-list {
      display: flex;
      list-style: none;
      @media (max-width: 999px) {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        background: $background;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        transform: translateY(-100%);
        transition: 0.3s ease-in-out;
        padding: 16px 0;
        z-index: 1;
      }
      li {
        letter-spacing: 3px;
        margin-left: 32px;
        @media (max-width: 999px) {
          margin-left: 0;
          opacity: 0;
        }

        a {
          text-align: center;
          position: relative;
          text-decoration: none;
          color: $dark;
          display: inline-block;
          padding: 5px 10px;
          overflow-x: hidden;
          &:hover {
            background: $primary;
            color: #fff;
            border-radius: 5px;
          }
          &.router-link-exact-active::before {
            width: 100%;
            transform: translateX(0);
          }
        }
      }
    }
    .active {
      transform: translateY(0);
      &.nav-list {
        top: 80px;
        li {
          opacity: 1;
        }
      }
    }
  }
}
</style>