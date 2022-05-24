<template>
  <div class="product-row">
    <p>{{ name }}</p>
    <p>{{ price }} €</p>
    <p>
      <input
        type="number"
        name="quantity"
        class="form-control"
        :value="quantity"
      />
    </p>
  </div>
</template>

<script>
export default {
  name: "CartProductListItem",
  props: {
    name: {
      type: String,
      required: true,
    },
    price: Number,
    quantity: {
      type: Number,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.product-row {
  display: flex;
  justify-content: space-between;
  border: 1px solid black;
  border-radius: 7px;
  padding: 1rem;

  p {
    margin: 0;
  }
}
</style>