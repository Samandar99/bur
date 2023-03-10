<template>
  <div class="deliver-wrap">
    <div class="left-deliver">
      <img class="deliver-foto" src="@/assets/img/food-delivery4.png" alt="" />
    </div>
    <div class="right-deliver">
      <h3 class="title-deliver">
        <span class="stay">Stay</span> at home, we will Provide
        <span class="good-d">good food</span>
      </h3>
      <p class="text-about_d">
        We provide tasty food and superfast delivery at your home. Let’s use our
        services right now and get discounts of up to 50%.
      </p>
      <div class="icon-deliver">
        <div class="time-deliver">
          <img src="@/assets/img/Timericon.svg" alt="" />
          <span>fasted delivery in 30 Minutes</span>
        </div>
        <div class="time-deliver">
          <img src="@/assets/img/deliverymoto1.svg" alt="" />
          <span>300+ delivery men</span>
        </div>
        <div class="time-deliver">
          <img src="@/assets/img/restaurnt1.svg" alt="" />
          <span>500+ restaurant & cafe shop</span>
        </div>
      </div>
      <button class="btn-dangers">
        <a href="#" class="se">See more</a>
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>
<style scoped>
.deliver-wrap {
  width: 100%;
  max-width: 1170px;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.btn-dangers {
  background: #ff7a50;
  border: none;
  box-shadow: 0px 22px 40px rgba(255, 104, 56, 0.19);
  border-radius: 30px 30px 1px 30px;
  color: #fff;
  font-size: 20px;
  padding: 15px 30px;
}

.title-deliver {
  font-size: 36px;
  line-height: 50px;
  max-width: 384px;
  color: #363853;
}

.stay {
  color: #ff7a50;
}

.good-d {
  color: #ff7a50;
}

.text-about_d {
  max-width: 440px;
  font-size: 20px;
  line-height: 30px;
  color: #363853;
  margin-top: 30px;
  margin-bottom: 30px;
}

.time-deliver {
  display: flex;
  align-items: center;
  gap: 20px;
}

.time-deliver img {
  width: 40px;
}
.icon-deliver {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-bottom: 49px;
}

.se{
  text-decoration: none;
  color: #fff;
}

/* media */

@media (max-width: 1083px) and (min-width: 310px) {
  .deliver-wrap {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
  .deliver-foto {
    width: 300px;
  }
  .right-deliver {
    padding: 0px 10px;
  }
}
</style>