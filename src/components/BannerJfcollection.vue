<template>
  <!-- Women Banner Section Begin -->
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5" v-if="products.length > 0">
          <carousel class="product-slider" :items="3" :dots="false" :nav="false" :autoplay="true" :loop="true">

            <div class="product-item" v-for="itemProduct in Products" v-bind:key="itemProduct.id">
              <div class="pi-pic">
                <img v-bind:src="itemProduct.galleries[0].photo" alt />
                <ul>
                  <li class="w-icon active">
                    <a href="#">
                      <i class="icon_bag_alt"></i>
                    </a>
                  </li>
                  <li class="quick-view">
                    <router-link to="/product"> + Quick View</router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">{{ itemProduct.type }}</div>
                <a href="/#/product">
                  <h5>{{ itemProduct.name }}</h5>
                </a>
                <div class="product-price">
                  {{ itemProduct.price }}
                  <span>$35.00</span>
                </div>
              </div>
            </div>

          </carousel>
        </div>

        <div class="col-lg-12" v-else>
          <p>Produk terbaru belum tersedia untuk saat ini</p>
        </div>

      </div>
    </div>
  </section>
  <!-- Women Banner Section End -->
</template>

<script>
import carousel from 'vue-owl-carousel';
import axios from "axios";

export default {
    name: 'BannerJfcollection',
    components: {
        carousel
    },
    data() {
      return {
        products: []
      };
    },
    mounted() {
      axios
        .get("http://127.0.0.1:8000/api/products")
        .then(res => (this.products = res.data.data.data))
        // eslint-disable-next-line no-console
        .catch(err => console.log(err));
    }
}
</script>

<style scoped>
.product-item {
    margin-right: 25px;
}

</style>