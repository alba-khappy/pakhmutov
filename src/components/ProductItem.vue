<template lang='pug'>
li.product__item
    img(:src="require(`../assets/${img}`)").product__img
    p.product__content {{content}}

</template>


<script>
export default {
  name: 'ProductItem',
  props: {
            img: {
                type: String,
                required: true,
            },
            content: {
                type: String,
                required: true,
            }
        },
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.product__item {
    max-width: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.product__img {
    width: auto;
    height: 210px;
}

.product__content {
    text-align: center;
    font-size: 12px;
}

</style>
