<template>
  <div class="d-wrap">
    <div class="left-d">
      <h3 class="d-wrap-title">
        Download Our <span class="mobile-p">Mobile App</span>
      </h3>
      <p class="about-app">
        It's all at your fingertips -- the restaurants you love. Find the right
        food to suit your mood, and make the first bite last. Go ahead, download
        app and get 50% discount
      </p>
      <div class="btn-app">
        <button class="btn-store">
          <img src="@/assets/img/Apple.svg" alt="" />
          <div>
            <span class="donw">Download on the</span>
            <p class="app-text">App Store</p>
          </div>
        </button>
        <button class="btn-store">
          <img src="@/assets/img/GooglePlaylogo.svg" alt="" />
          <div>
            <span class="donw">GET IT ON</span>
            <p class="app-text">Google Play</p>
          </div>
        </button>
      </div>
    </div>
    <div class="right-d">
      <img class="foto-mobile" src="@/assets/img/mobile.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.d-wrap {
  width: 100%;
  max-width: 1170px;
  margin: 150px auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.d-wrap-title {
  text-transform: capitalize;
  font-size: 36px;
  margin-bottom: 30px;
  color: #363853;
}

.mobile-p {
  color: #ff7a50;
}

.btn-store {
  background: #0c0d10;
  display: flex;
  gap: 6px;
  text-align: left;
  border: none;
  border-radius: 7px;
  padding: 3px 7px;
  align-items: center;
}
.donw {
  color: #fff;
  font-size: 10px;
}
.app-text {
  color: #fff;
  font-size: 18px;
}

.btn-app {
  display: flex;
  gap: 35px;
}

.about-app {
  font-size: 20px;
  line-height: 30px;
  color: #363853;
  width: 100%;
  max-width: 538px;
  margin-bottom: 30px;
}

.foto-mobile {
  max-width: 600px;
}

/* media */

@media (max-width: 1154px) and (min-width: 617px) {
  .d-wrap {
    width: 100%;
    max-width: 1170px;
    margin: 150px auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 70px;
    flex-direction: column-reverse;
  }
}

@media (max-width: 616.9px) {
  .d-wrap {
    width: 100%;
    max-width: 1170px;
    margin: 150px auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 70px;
    flex-direction: column-reverse;
  }
  .foto-mobile {
    max-width: 300px;
  }
  .left-d {
    padding: 0px 10px;
  }
}
</style>