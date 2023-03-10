<template>
  <div class="mt-4">
    <div class="wrapper-foo">
      <ul class="links-foot">
        <li class="logo-foo"><img src="@/assets/img/EFood.svg" alt="" /></li>
        <li class="link-foots">
          <img src="@/assets/img/Location.svg" alt="" />
          <span>Dhaka, Bangladesh</span>
        </li>
        <li class="link-foots">
          <img src="@/assets/img/Calling.svg" alt="" />
          <span>Dhaka, Bangladesh</span>
        </li>
        <li class="link-foots">
          <img src="@/assets/img/Message.svg" alt="" />
          <span>Dhaka, Bangladesh</span>
        </li>
        <li class="icons-links">
          <a href="#" class="icon-fa">
            <img src="@/assets/img/ic-facebook.svg" alt="" />
          </a>
          <a href="" class="icon-fa">
            <img src="@/assets/img/ic-twitter.svg" alt="" />
          </a>
          <a href="" class="icon-fa">
            <img src="@/assets/img/ic-instagram.svg" alt="" />
          </a>
          <a href="" class="icon-fa">
            <img src="@/assets/img/ic-pinterset.svg" alt="" />
          </a>
        </li>
      </ul>
      <ul class="aboutli">
        <li><a href="#" class="ser">Service</a></li>
        <li><a href="#" class="se1">How it works</a></li>
        <li><a href="#" class="se1">Home delivery</a></li>
        <li><a href="#" class="se1">Prducts</a></li>
        <li><a href="#" class="se1">Menu</a></li>
      </ul>
      <ul class="aboutli">
        <li><a href="#" class="ser">Company</a></li>
        <li><a href="#" class="se1">About Us</a></li>
        <li><a href="#" class="se1">News</a></li>
        <li><a href="#" class="se1">Our trusted partner</a></li>
        <li><a href="#" class="se1">New users FAQ</a></li>
      </ul>

      <ul class="aboutli">
        <li><a href="#" class="ser">Supports</a></li>
        <li><a href="#" class="se1">Help center</a></li>
        <li><a href="#" class="se1">Feedbcak</a></li>
        <li><a href="#" class="se1">Contact us</a></li>
        <li><a href="#" class="se1">Terms conditins</a></li>
      </ul>

      <ul class="aboutli">
        <li><a href="#" class="ser">Resources</a></li>
        <li><a href="#" class="se1">Download app</a></li>
        <li><a href="#" class="se1">Blog</a></li>
        <li><a href="#" class="se1">What’s new</a></li>
        <li><a href="#" class="se1">Sitemap</a></li>
      </ul>
    </div>
    <div class="main-footer"></div>
    <div class="info-foot">
      <p class="efood">© 2021 EFood - All rights reserved.</p>
      <ul class="db-link">
        <li>Privacy</li>
        <li>Security</li>
        <li>Terms</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrapper-foo {
  max-width: 1170px;
  width: 100%;
  margin: auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

li {
  list-style: none;
}
.link-foots {
  display: flex;
  align-items: center;
  gap: 7px;
}
.links-foot {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.logo-foo {
  margin-bottom: 29px;
}

.icon-fa {
  width: 39px;
  height: 39px;
  background-color: #eeeeef;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
}
.icons-links {
  display: flex;
  align-items: center;
  gap: 13px;
  margin-top: 13px;
}

.ser {
  text-decoration: none;
  color: #37383d;
  font-weight: 600;
}

.aboutli {
  display: flex;
  flex-direction: column;
  gap: 36px;
}

.se1 {
  text-decoration: none;
  color: #37383d;
}

.mt-4 {
  margin-top: 120px;
}
.main-footer {
  width: 100%;
  border-top: 1px solid #969696;

  margin-top: 25px;
  opacity: 0.2;
}

.efood {
  color: #646464;
}
.info-foot {
  width: 100%;
  max-width: 1170px;
  margin: 21px auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.db-link {
  display: flex;
  gap: 51px;
}

@media (max-width: 792px) and (min-width: 673px) {
  .wrapper-foo {
    max-width: 770px;
    width: 100%;
    gap: 40px;
    margin: auto;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
}

@media (max-width: 672.9px) {
  .wrapper-foo {
    max-width: 770px;
    width: 100%;
    gap: 40px;
    margin: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    flex-wrap: wrap;
  }
  
  .info-foot {
  width: 100%;
  max-width: 1170px;
  margin: 21px auto;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  align-content: center;
  flex-wrap: wrap;
  gap: 20px;
}
}
</style>