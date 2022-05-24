<template>
    <p class="cart">Panier <span class="nb-products" >{{ nbProductInCart }}</span></p>
</template>

<script>
export default {
    name: 'TheHeaderCartIcon',
    data() {
        return {
            nbProductInCart: 0,
        };
    },
}
</script>

<style lang="scss" scoped>
.cart {
    padding: 0.5rem;
    border: 1px solid white;
    color: white;
    margin: 0;
    cursor: pointer;
    position: relative;

    .nb-products {
        position: absolute;
        right: -5px;
        top: -5px;
        display: inline-block;
        color: white;
        background: red;
    }
}
</style>