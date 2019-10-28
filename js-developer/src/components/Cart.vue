<template>
  <div class="cart"></div>
</template>

<script>
export default {
  name: "Cart",
  data: function() {
    return {
      total: 0,
      coupon: "",
      products: [
        {
          id: 1,
          name: "iPhone 8",
          code: "iphone-1",
          image: "#",
          price: 780,
          quantity: 1
        },
        {
          id: 2,
          name: "iPhone X",
          code: "iphone-2",
          image: "#",
          price: 900,
          quantity: 1
        },
        {
          id: 3,
          name: "Macbook Pro 2017",
          code: "mac-pro-1",
          image: "#",
          price: 1200,
          quantity: 1
        }
      ]
    };
  }
};
</script>

<style scoped></style>
