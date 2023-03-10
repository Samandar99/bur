<template>
  <div class="wrap-about">
    <h3 class="about-title">
      What Our Client Are <span class="say">Saying</span>
    </h3>
    <div class="block-carusel">
      <img class="client-ch" src="@/assets/img/client.png" alt="" />

      <div class="about-box">
        EFood has the most intriguing food order system in the country. UI in
        both their app and web Is very simple and easy to use, enhancing the UX.
        Their delivery men are also quite professional and knows the
        neighborhood well. Till now I never had to guide them to my address for
        delivery;

        <div class="avtor">
          <div>
            <p class="avtor-g">Anglina Jole</p>
            <span class="lover">Food lover</span>
          </div>
          <div></div>
        </div>
        <img class="icont" src="@/assets/img/kavichkat.svg" alt="" />
        <img class="iconb" src="@/assets/img/kavichkab.svg" alt="" />
      </div>
    </div>
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

  setup() {
    const prevs = ref(null);
    const nexts = ref(null);
    return {
      modules: [Pagination, Autoplay, Navigation],
      prevs,
      nexts,
    };
  },
};
</script>

<style>
.wrap-about {
  width: 100%;
  max-width: 1170px;
  margin: auto;
}
.lover {
  font-size: 14px;
  color: #aaa;
}

.client-ch {
  max-width: 433.38px;
  width: 100%;
}

.block-carusel {
  display: flex;
  margin: 35px 0;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.about-title {
  text-align: center;
  font-size: 36px;
  color: #363853;
}

.say {
  color: #ff7a50;
}
.about-box {
  width: 100%;
  max-width: 559px;
  font-size: 20px;
  line-height: 45px;
  position: relative;
  color: #363853;
}
.siw {
  padding: 0px 40px;
}

.icont {
  position: absolute;
  top: 0;
  left: -2.5rem;
}

.iconb {
  position: absolute;
  right: 0rem;
  bottom: 3rem;
}

.avtor-g {
  color: #ff7a50;
  font-weight: 500;
  font-size: 20px;
}

.avtor {
  margin-top: 40px;
}

@media (max-width: 1089px) {
  .block-carusel {
    display: flex;
    margin-top: 35px;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }
}

@media (max-width: 567px) {
  .about-box {
    padding: 0px 20px;
  }
}
</style>