<template>
  <div :class="side == cartOpen ? 'cart-active' : 'wrap-sidebar'">
    <div>
      <div class="sidebar-head">
        <h3>CartBurger</h3>
        <img @click="iscart()" src="@/assets/img/closeCart.svg" alt="" />
      </div>
      <div class="block-carts" v-for="cart in cartP" :key="cart">
        <div class="carts">
          <img class="carts__img" :src="cart.img" alt="" />
          <div class="cart-text">
            <p class="cart__name">{{ cart.name }}</p>
            <b>{{ cart.price }} руб.</b>
          </div>
          <div>1x</div>
          <img class="dell-icon" src="@/assets/img/closeCart.svg" alt="" />
        </div>
      </div>
    </div>
    <div class="sidebar-footer">
      <div class="total-item">
        <p>Итого:</p>
        <div class="dot"></div>
        <p class="taxs">21 498 руб.</p>
      </div>
      <div class="tax-item">
        <p>Налог 5%:</p>
        <div class="dot"></div>
        <p class="taxs">1074 руб.</p>
      </div>
      <button class="add-orderbtn">Оформить заказ</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    side: {
      typeof: Boolean,
    },
    cartP: {
      typeof: Array,
    }
  },

  data() {
    return {
      isOpens: "",
      cartOpen: true,
    };
  },

  methods: {
    iscart() {
      this.cartOpen = !this.cartOpen;
    },
  },
};
</script>

<style>
.wrap-sidebar {
  width: 385px;
  height: 100vh;
  background-color: #fff;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  position: fixed;
  right: -380px;
  top: 0;
  z-index: 999;
  padding: 30px 30px;
  overflow: scroll;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.cart-active {
  max-width: 385px;
  width: 100%;
  height: 100vh;
  background-color: #fff;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  position: fixed;
  right: 0px;
  top: 0;
  z-index: 999;
  padding: 30px 30px;
  overflow: scroll;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: all 0.3s ease-in;
}

.sidebar-footer {
  margin-top: 40px;
}

.sidebar-head {
  display: flex;
  justify-content: space-between;
  margin-bottom: 30px;
}

.sidebar-head img {
  cursor: pointer;
}

.carts {
  width: 325px;
  background: #ffffff;
  border: 1px solid #c9c6c6;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 10px 10px 0px;
  margin-top: 20px;
}

.carts__img {
  width: 100px;
  object-fit: cover;
}

.cart__name {
  width: 150px;
  font-size: 14px;
  margin-bottom: 5px;
}

.dell-icon {
  cursor: pointer;
}

.add-orderbtn {
  padding: 15px 90px;
  background: #ff7a50;
  border-radius: 18px;
  border: none;
  color: #fff;
  font-size: 16px;
  cursor: pointer;
}

.dot {
  border: 2px dashed rgb(218, 213, 213);
  max-width: 100px;
  width: 100%;
  height: 0px;
}

.total-item {
  margin-bottom: 10px;

  align-items: center;
  display: flex;
  justify-content: space-between;
}

.tax-item {
  margin-bottom: 20px;
  align-items: center;
  display: flex;
  justify-content: space-between;
}

@media (max-width: 434px) {
  .wrap-sidebar {
    width: 100%;
  }

  .carts {
    max-width: 325px;
    width: 100%;
    background: #ffffff;
    border: 1px solid #c9c6c6;
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 10px 10px 0px;
    margin-top: 20px;
  }

  .carts__img {
    width: 70px;
    object-fit: cover;
  }

  .cart__name {
    width: 112px;
    font-size: 12px;
    margin-bottom: 5px;
  }

  .add-orderbtn {
    padding: 15px 40px;
    background: #ff7a50;
    border-radius: 18px;
    border: none;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
  }

  .taxs {
    font-size: 14px;
  }

  .dot {
    border: 2px dashed rgb(218, 213, 213);
    max-width: 50px;
    width: 100%;
    height: 0px;
  }
}
</style>