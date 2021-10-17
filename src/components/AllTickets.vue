<template>
  <div>
    <div class="section notopmargin notopborder">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Tickets</h3>
        </div>
      </div>
    </div>
    <div class="shop grid-container clearfix">
      <div
        class="product clearfix"
        v-for="ticket in tickets"
        :key="ticket"
      >
        <TicketCart :ticket = "ticket" />
      </div>
    </div>
  </div>
</template>

<script>
import TicketCart from "../components/carts/TicketCart";
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("productbox", ["tickets"]),
  },
  components: {
    TicketCart
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