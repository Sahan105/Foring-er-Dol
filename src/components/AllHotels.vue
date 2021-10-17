<template>
   <div>
    <div class="section notopmargin notopborder">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Hotels</h3>
        </div>
      </div>
    </div>
    <div class="shop grid-container clearfix">
      <div
        class="product clearfix"
        v-for="hotel in hotels"
        :key="hotel"
      >
        <HotelCart :hotel = "hotel" />
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
import HotelCart from "../components/carts/HotelCart"
export default {
  computed: {
    ...mapState("productbox", ["hotels"]),
  },
  components: {
    HotelCart
  }
};
</script>
<style scoped>
#hotel-image {
  height: 230px;
}
#product {
  text-align: left;
  height: 230px;
}
#hotel {
  margin-left: 10%;
  margin-top: -3%;
}

#content {
  margin-right: 33%;
}
</style>
