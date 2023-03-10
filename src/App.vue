<template>
  <Navbar :numbers="numbers" :open="open" @isopen="getopen" />
  <Sidebar :side="side" :cartP="cartP" />
  <Banner />
  <Categories :productsCategories="productsCategories" @send="getTitle" />
  <Deliver />
  <Products :products="products" />
  <Donwload />
  <AboutClient />
  <Emailsen />
  <Footer />
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->

  <router-view />
</template>

<style>
</style>


<script>
import Navbar from "@/components/Navbar.vue";
import Banner from "@/components/Banner.vue";
import Categories from "@/components/Categories.vue";
import Deliver from "@/components/Deliver.vue";
import Products from "@/components/Products.vue";
import Donwload from "@/components/Donwload.vue";
import AboutClient from "@/components/AboutClient.vue";
import Emailsen from "@/components/Emailsen.vue";
import Footer from "@/components/Footer.vue";
import Sidebar from "./components/Sidebar.vue";

export default {
  components: {
    Navbar,
    Banner,
    Categories,
    Deliver,
    Products,
    Donwload,
    AboutClient,
    Emailsen,
    Footer,
    Sidebar,
  },
  data() {
    return {
      productsCategories: [
        {
          id: 1,
          name: "Cheeseburger With Salad",
          price: "15.00",
          img: require("@/assets/img/newburger.png"),
        },
        {
          id: 2,
          name: "Beef Burger",
          price: "18.00",
          img: require("@/assets/img/Burger2.png"),
        },
        {
          id: 3,
          name: "Royel Cheeseburger",
          price: "15.00",
          img: require("@/assets/img/burgerlast.png"),
        },
        {
          id: 4,
          name: "Black Gambugrer ",
          price: "14.00",
          img: require("@/assets/img/burger3.png"),
        },
        {
          id: 5,
          name: "Chicken Burger",
          price: "16.00",
          img: require("@/assets/img/burger4.png"),
        },
        {
          id: 6,
          name: "Beef Burger",
          price: "15.00",
          img: require("@/assets/img/burgerimg.png"),
        },
      ],

      products: [
        {
          id: 1,
          name: "Blaze Pizza",
          images: require("@/assets/img/Rectangle1.png"),
        },
        {
          id: 2,
          name: "Pizza Ranch",
          images: require("@/assets/img/Rectangle2.png"),
        },
        {
          id: 3,
          name: "Dion’s Pizza Hut",
          images: require("@/assets/img/Rectangle3.png"),
        },
        {
          id: 4,
          name: "Royel Burger",
          images: require("@/assets/img/Rectangle4.png"),
        },
        {
          id: 5,
          name: "KFC Restaurant",
          images: require("@/assets/img/Rectangle5.png"),
        },
        {
          id: 6,
          name: "Star Food",
          images: require("@/assets/img/Rectangle6.png"),
        },
      ],

      numbers: 0,
      open: this.name,
      side: "",
      cartP: [],
    };
  },
  methods: {
    getTitle(name, num, id) {
      console.log(name, num);
      this.numbers = num;
      this.cartP.push(id);

      let uniq = this.cartP.filter((element, index) => {
        return this.cartP.indexOf(element) === index;
      });

      this.cartP = uniq
    },
    getopen(opens) {
      this.side = opens;
      console.log(this.side);
    },
  },
};
</script>
