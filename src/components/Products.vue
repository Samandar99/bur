<template>
  <div class="wrap-product">
    <h3 class="title-product"><span class="top">Top Food</span> restaurant</h3>
    <div class="conatiner-product">
      <div class="box-p" v-for="product in products" :key="product.id">
        <img class="foto-rest" :src="product.images" alt="" />
        <div class="pizz">
          <span>{{ product.name }}</span>
          <div class="times">
            <div class="timesin">
              <img src="@/assets/img/timers3.svg" alt="" />
              <span>11.00 AM - 10.00 PM </span>
            </div>
            <a href="#">
              <div class="btn-links">
                <img src="@/assets/img/arrowrights.svg" alt="" />
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    products: {
      typeof: Array,
    },
  },
};
</script>

<style scoped>
.title-product {
  text-align: center;
  font-weight: 900;
  font-size: 36px;
  color: #363853;
  margin-bottom: 50px;
}

.conatiner-product {
  width: 100%;
  max-width: 1170px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(361px, 300px));
  gap: 40px;
  justify-content: center;
}

.box-p {
  background: #ffffff;
  border-radius: 53px 5px;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}
.top {
  color: #ff7a50;
}

.btn-links {
  padding: 7px 30px;
  display: inline;
  background: #ff7a50;
  box-shadow: 0px 5px 12px rgba(255, 104, 56, 0.19);
  border-radius: 20px 20px 0px 20px;
}

.times {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 14px;
}
.timesin {
  display: flex;

  gap: 9px;
}
.pizz {
  padding-left: 20px;
  padding-right: 28px;
  padding-bottom: 26px;
  padding-top: 17px;
}

@media (max-width: 1084px) {
  .title-product {
    text-align: center;
    font-weight: 900;
    font-size: 36px;
    color: #363853;
    margin-top: 50px;
    margin-bottom: 50px;
  }
}
@media (max-width: 378px) {
  .conatiner-product {
    width: 100%;
    max-width: 1170px;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 300px));
    gap: 40px;
    justify-content: center;
  }
  .foto-rest {
    max-width: 300px;
  }
}
</style>