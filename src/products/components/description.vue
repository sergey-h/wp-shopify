<template>
    <span class="product-description-wrap">
        <slot name="before"></slot>
        <span class="wpshop-product-description" v-html="description"></span>
        <slot></slot>
    </span>
</template>

<script>
    export default {
        name: 'description',
        computed: {
            description () { return _.get(this.$root, 'product.attrs.body_html') }
        }
    }
</script>
