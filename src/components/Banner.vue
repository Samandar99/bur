<template>
  <section class="tm">
    <div class="wrap-banner">
      <div class="banner-left">
        <h1 class="banner-title">
          super fast <span>Food</span> <span>delivery</span> service
        </h1>
        <p class="text-about">
          We provide super fast-delivery service. Let’s use our services right
          now and get discounts of up to 50%
        </p>
        <div class="buttons">
          <button
            @click="changeClass = !changeClass"
            :class="changeClass == true ? 'app' : 'food'"
          >
            Explore Food
          </button>
          <button
            class="app"
            @click="changeClass = !changeClass"
            :class="{ food: changeClass }"
          >
            Download App
          </button>
        </div>
      </div>
      <div class="banner-right">
        <div class="banner-img">
          <div class="call-alex">
            <img src="@/assets/img/client.svg" alt="" />
            <div class="name-deliver">
              <b>Alex Smith</b>
              <span>Food Deliveryman </span>
            </div>
            <div class="img-call">
              <img src="@/assets/img/Call1.svg" alt="" />
            </div>
          </div>
          <div class="search">
            <img src="@/assets/img/search11.svg" alt="" />
          </div>
          <div class="times">
            <img src="@/assets/img/Time.png" alt="" />
          </div>
          <div class="chez">
            <img class="icon-chez" src="@/assets/img/buter2.svg" alt="" />
            <div>
              <span class="name-chez">Doubble sandwich</span>
              <ul class="icons-star">
                <li><img src="@/assets/img/Starsss.svg" alt="" /></li>
                <li><img src="@/assets/img/Starsss.svg" alt="" /></li>
                <li><img src="@/assets/img/Starsss.svg" alt="" /></li>
                <li><img src="@/assets/img/Starsss.svg" alt="" /></li>
                <li><img src="@/assets/img/Starsss.svg" alt="" /></li>
              </ul>
              <p class="price-chez"><span class="dolar">$</span>7.50</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      changeClass: false,
    };
  },

  methods: {
    // changecolor(){
    //   this.changeClass = true
    // }
  },
};
</script>

<style scoped>
.tm {
  margin-top: 120px;
}
.wrap-banner {
  width: 100%;
  max-width: 1170px;
  margin: auto;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  overflow: hidden;
}
.banner-title {
  text-transform: capitalize;
  font-size: 66px;
  line-height: 78px;
  width: 100%;
  max-width: 500px;
  color: #363853;
  margin-bottom: 23px;
}

.name-deliver {
  display: flex;
  flex-direction: column;
}
.name-deliver b {
  font-size: 10px;
}
.name-deliver span {
  font-size: 8px;
}

.banner-title span {
  color: #ff7a50;
}

.text-about {
  width: 100%;
  max-width: 400px;
  margin-bottom: 44px;
}
.food {
  background-color: #ff7a50 !important;
  box-shadow: 0px 22px 40px rgba(255, 104, 56, 0.19);
  border-radius: 5px;
  padding: 10px 15px;
  border: 1px solid #ff7a50;
  color: #fff !important;
  font-size: 20px;
  cursor: pointer;
  text-decoration: none !important;
}
.buttons {
  display: flex;
  gap: 30px;
}
.app {
  background: none;
  border: none;
  font-size: 20px;
  color: #363853;
  text-decoration: underline;
  cursor: pointer;
}
.banner-img {
  background: url(../assets/img/ScooterGuy.png);
  background-size: cover;
  width: 669px;
  height: 660px;
  position: relative;
}

.search {
  position: absolute;
  top: 40px;
  left: 220px;
}
.times {
  position: absolute;
  right: 5rem;
  top: 1rem;
}

.call-alex {
  position: absolute;
  top: 130px;
  left: 120px;
  background: radial-gradient(
    50% 50% at 50% 50%,
    #fef8f5 0%,
    rgba(255, 255, 255, 0.79) 100%
  );
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.12);
  border-radius: 6px;
  width: 100%;
  max-width: 154px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 7px;
}

.chez {
  position: absolute;
  right: -35px;
  top: 260px;
  background: radial-gradient(
    50% 50% at 50% 50%,
    #fef8f5 0%,
    rgba(255, 255, 255, 0.79) 100%
  );
  padding: 4px 0px;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.07);
  border-radius: 12px;
  width: 178px;
  height: 75px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.icons-star {
  display: flex;
  gap: 3px;
}
.icons-star li {
  list-style: none;
}
.name-chez {
  font-size: 11px;
}
.icon-chez {
  width: 60px;
  height: 60px;
  object-fit: cover;
}

.price-chez {
  font-size: 15px;
}

.dolar {
  font-size: 8px;
  color: #ff7a50;
}

.banner-left{
  padding: 0;
}


/* media */

@media (max-width: 1186px) and (min-width: 700px) {
  .wrap-banner {
    width: 100%;
    max-width: 1170px;
    margin: auto;
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    flex-wrap: wrap;
    overflow: hidden;
  }
}

@media (max-width: 699.9px) {
  .wrap-banner {
    width: 100%;
    max-width: 1170px;
    margin: auto;
    display: flex;
    flex-direction: column-reverse;
    align-content: center;
    
    flex-wrap: wrap;
    overflow: hidden;
  }
  .banner-img {
  background: url(../assets/img/ScooterGuy.png) center;
  background-size: cover;
  max-width: 469px;
  height: 460px;
  position: relative;
}
.tm {
  margin-top: 20px;
}

.banner-left{
  padding: 0px 10px;
}

}
</style>
