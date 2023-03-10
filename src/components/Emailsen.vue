<template>
  <div class="wrap-email">
    <h3 class="title-email">Subscribe to get the Latest Offer</h3>
    <p class="text-email">
      Get our daily updates by subscribing to our newspaper, please drop your
      email below
    </p>

    <form action="" class="input-form">
      <input
        placeholder="Enter your email addres"
        type="text"
        class="inputsend"
      />
      <button class="btn-form">
        <img src="@/assets/img/telegram.svg" alt="" />
        <span>Subscribe</span>
      </button>
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style>
.wrap-email {
  max-width: 1170px;
  width: 100%;
  margin: auto;
  background-color: #ff7a50;
  border-radius: 15px;
  text-align: center;
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 50px 0px;
}

.input-form {
  max-width: 838.5px;
  width: 100%;
  background: #ffffff;
  box-shadow: 10px 24px 54px rgba(0, 0, 0, 0.07);
  border-radius: 70px;
  display: flex;
  justify-content: space-between;

  padding: 9px 9px 9px 40px;
}

.btn-form {
  background: #ff7a50;
  border: none;
  display: flex;
  align-items: center;
  padding: 15px 25px;
  border-radius: 70px;
  color: #ffffff;
  gap: 8px;
  cursor: pointer;
}

.inputsend {
  outline: none;
  width: 100%;
  border: none;
  color: #363853;
  font-size: 18px;
}
.title-email {
  font-size: 40px;
  color: #ffffff;
  margin-bottom: 12px;
}

.text-email {
  color: #ffffff;
  opacity: 0.8;
  margin-bottom: 30px;
}

@media(max-width: 408px){
  .inputsend {
  outline: none;
  width: 100%;
  border: none;
  color: #363853;
  font-size: 12px;
}
.btn-form {
  background: #ff7a50;
  border: none;
  display: flex;
  align-items: center;
  padding: 15px 10px;
  border-radius: 70px;
  color: #ffffff;
  gap: 8px;
  cursor: pointer;
}
.text-email {
  color: #ffffff;
  opacity: 0.8;
  margin-bottom: 30px;
  line-height: 25px;
}

}

</style>