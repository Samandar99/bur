<template>
  <div class="wrap-categories">
    <h3 class="title-cat">
      Our popular <span class="title-orange">Category</span>
    </h3>
    <div class="block-choice">
      <div class="categoriya__choice">
        <img src="@/assets/img/sendvich.svg" class="green" alt="" />
        <span>Burger</span>
      </div>
      <div class="categoriya__choice">
        <img src="@/assets/img/sendvich02.svg" alt="" />
        <span>Burger</span>
      </div>
      <div class="categoriya__choice">
        <img src="@/assets/img/sendvich3.svg" alt="" />
        <span>Burger</span>
      </div>
      <div class="categoriya__choice">
        <img src="@/assets/img/sendvich4.svg" alt="" />
        <span>Burger</span>
      </div>
      <div class="categoriya__choice">
        <img src="@/assets/img/sendvich5.svg" alt="" />
        <span>Burger</span>
      </div>
    </div>

    <Swiper
      :slidesPerView="5"
      :spaceBetween="30"
      :pagination="{
        clickable: true,
      }"
      :navigation="{
        prevEl: prev1,
        nextEl: next1,
      }"
      :modules="modules"
      class="swiper-wrapper"
    >
      <swiper-slide
        v-for="productsCat in productsCategories"
        :key="productsCat.id"
      >
        <div class="box">
          <img class="burgers" :src="productsCat.img" alt="" />
          <div class="stars">
            <img
              src="@/assets/img/Starb.svg"
              alt=""
              v-for="star in stars"
              :key="star"
            />
          </div>
          <p class="name_burger" title="Cheeseburger With Salad">
            {{ productsCat.name }}
          </p>
          <b class="price-burger">${{ productsCat.price }}</b>
          <button
            class="add-btn"
            @click="addCart(opencart, ++number, productsCat)"
          >
            Add to Cart
          </button>
        </div>
      </swiper-slide>

      <!-- <div class="button-swiperss">
        <div ref="prev1" class="swiper-button-next"></div>
        <div ref="next1" class="swiper-button-prev"></div>
      </div> -->
    </Swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper";
import { ref } from "vue";
import { Navigation } from "swiper";
import "swiper/css/navigation";
import "swiper/css";
import "swiper/css/pagination";

export default {
  components: { Swiper, SwiperSlide },
  props: {
    productsCategories: {
      typeof: Array,
    },
  },

  data() {
    return {
      stars: [
        { star: "" },
        { star: "" },
        { star: "" },
        { star: "" },
        { star: "" },
      ],

      number: 0,
      opencart: false,
    };
  },
  methods: {
    addCart(opencart, num, id) {
      this.$emit("send", opencart, num, id);
      // console.log(this.productsCategories);
      //console.log(id);
    },
  },

  setup() {
    const prev1 = ref(null);
    const next1 = ref(null);
    return {
      modules: [Pagination, Autoplay, Navigation],
      prev1,
      next1,
    };
  },
};
</script>

<style>
.swiper-button-next {
  color: #d1d2dc !important;
}

.swiper-button-prev {
  color: #d1d2dc !important;
}

.swiper-button-disabled {
  color: red !important;
}

.wrap-categories {
  width: 100%;
  max-width: 1170px;
  margin: 70px auto;
  /*  background: rebeccapurple; */
  overflow: hidden;
  position: relative;
}

.button-swiperss {
  width: 100px;
  position: absolute;
  top: 20rem;
  left: 30rem;
  display: flex;
}

.box {
  /* width: 210px; */
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #ffffff;
  border-radius: 12px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
  padding: 20px 0;
}

.burgers {
  width: 146px;
  height: 122px;
  object-fit: cover;
}

.title-cat {
  text-align: center;
  font-size: 36px;
  color: #363853;
  margin-bottom: 54px;
}

.title-orange {
  color: #ff7a50;
}

.mySwiper {
  display: flex;
  align-items: center;
}

.name_burger {
  color: #363853;
  margin-bottom: 9px;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.price-burger {
  color: #363853;
  margin-bottom: 11px;
}

.add-btn {
  background: #ff7a50;
  border-radius: 2px;
  border: none;
  padding: 10px 17px;
  color: #fff;
  font-size: 15px;
  cursor: pointer;
}

.swiper-pagination-bullet-active {
  background-color: #ff7a50;
}

.swiper-pagination-bullet {
  z-index: 99;
}

.swiper-wrapper {
  position: relative;
  width: 100%;
  height: 360px;
  z-index: 1;
  display: flex;
  transition-property: transform;
  transition-timing-function: var(
    --swiper-wrapper-transition-timing-function,
    initial
  );
  box-sizing: content-box;
  /* background: red; */
}

.swiper,
swiper-container {
  margin-left: auto;
  margin-right: auto;
  position: relative;

  list-style: none;
  padding: 0;
  z-index: 1;
  display: block;
}

.stars {
  margin-bottom: 29px;
}

.swiper {
  overflow: hidden !important;
  width: 1170px !important;
}

.block-choice {
  display: flex;
  gap: 26px;
  width: 100%;
  max-width: 1170px;
  /* background-color: red; */
  flex-wrap: wrap;
  justify-content: space-between;
  margin-bottom: 39px;
}

.categoriya__choice {
  background-color: #fff;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;

  align-items: center;
  border-radius: 8px;
  padding: 10px 54px;
  display: flex;
  gap: 9px;
  cursor: pointer;
}

.active22 {
  background: #ff7a50;
  color: #fff;
}

@media (max-width: 1178px) and (min-width: 786px) {
  .swiper {
    overflow: hidden !important;
    max-width: 970px !important;
  }

  .box {
    /* width: 210px; */
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
    padding: 20px 20px;
    text-align: center;
  }
}

@media (max-width: 688px) {
  .block-choice {
    display: flex;
    gap: 26px;
    width: 100%;
    max-width: 1170px;

    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 39px;
  }
}
</style>
