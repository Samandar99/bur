<template>
  <header class="header">
    <nav class="navbar">
      <a href="#" class="nav-branding"
        ><img src="@/assets/img/EFood.svg" alt=""
      /></a>
      <ul
        class="nav-menu"
        @click="navOpen = !navOpen"
        :class="{ active: navOpen }"
      >
        <li class="nav-item">
          <a href="#" class="nav-link">Home</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Service</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Top cities</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Contract</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link"
            ><img src="@/assets/img/Search.svg" alt=""
          /></a>
        </li>
        <li class="nav-item counts">
          <button
            class="btn-cart"
            @click="openCart((this.opens = !this.opens))"
          >
            <p class="count">{{ numbers }}</p>
            <img src="@/assets/img/Buy.svg" alt="" />
          </button>
        </li>
        <li class="nav-item btn-sign">
          <a href="#" class="nav-link2">Sign Up</a>
        </li>
      </ul>
      <div
        class="hamburger"
        @click="navOpen = !navOpen"
        :class="{ active: navOpen }"
      >
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  props: {
    numbers: {
      typeof: Number,
    },
    open: {
      typeof: Boolean,
    },
  },

  data() {
    return {
      navOpen: true,
      opens: false,
    };
  },
  methods: {
    openCart(opens) {
      this.$emit("isopen", opens);
    },
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.counts {
  position: relative;
}

.count {
  position: absolute;
  right: -10px;
  top: -9px;
  background: #ff6838;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
  color: #fff;
}

.btn-cart {
  background: none;
  border: none;
  cursor: pointer;
}
.btn-sign {
  background: #ff7a50;
  padding: 12px 20px;
  box-shadow: 0px 22px 40px rgba(255, 104, 56, 0.19);
  border-radius: 5px;
}
.nav-link2 {
  color: #fff;
  text-decoration: none;
  font-size: 16px;
}
.nav-link {
  color: #363853;
  text-decoration: none;
}

li {
  list-style: none;
}

.navbar {
  min-height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 24px;
  max-width: 1170px;
  width: 100%;
  margin: auto;
  background-color: #fff;
}

.nav-menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 60px;
}

.nav-branding {
  font-size: 2rem;
}

.nav-link {
  transition: 0.7s ease;
}

.hamburger {
  display: none;
  cursor: pointer;
  width: 50px;
}

.bar {
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  -webkit-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
  background-color: #ff7a50;
}

.header {
  position: -webkit-sticky;
  position: sticky;
  top: 0;

  z-index: 99;

  background-color: #fff;
}

@media (max-width: 900px) {
  .hamburger {
    display: block;
  }
  .hamburger.active .bar:nth-child(2) {
    opacity: 0;
  }
  .hamburger.active .bar:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
  }
  .hamburger.active .bar:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
  }
  .nav-menu {
    position: absolute;
    left: -100%;
    top: 70px;

    gap: 0;
    flex-direction: column;
    /* filter: drop-shadow(6px 6px 15px rgba(132, 132, 132, 0.3)); */
    width: 50%;
    text-align: center;
    transition: 0.3s;
    background-color: #fff;
    z-index: 99;
  }

  .nav-item {
    margin: 16px 0;
  }

  .nav-menu.active {
    left: 0;
  }
}
</style>