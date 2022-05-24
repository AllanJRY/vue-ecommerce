<template>
    <div class="container mt-3">
      <div class="row">
        <div class="col-12 mb-3" v-for="product in products" :key="product.name+quantity">
            <CartProductListItem />
        </div>
        <div class="col-12 mb-3 bg-primary">
            <p class="text-white m-0 py-3">Total : {{ totalPrice }} €</p>
        </div>
      </div>
    </div>
</template>

<script>
import CartProductListItem from './CartProductListItem.vue';

export default{
  components: { CartProductListItem },
    name: 'CartProductList',
    data() {
        return {
            products: [
                {
                    name: "Product",
                    price: 153.20,
                    quantity: 5,
                },
                                {
                    name: "Product 2",
                    price: 20.50,
                    quantity: 2,
                },
                                {
                    name: "Product 3",
                    price: 40.00,
                    quantity: 7,
                },
                                {
                    name: "Product 4",
                    price: 10.00,
                    quantity: 3,
                },
            ],
        }
    },
    computed: {
        totalPrice() {
            let totalPrice = 0;
            this.products.forEach(product => {
                totalPrice += product.price * product.quantity
            });

            return totalPrice;
        },
    },
}
</script>
