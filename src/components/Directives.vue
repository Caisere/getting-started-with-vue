<template>
    <div>
        <h2>Vue Directives</h2>
        <p v-if="productsLeft > 10">There are more than 10 products left in stock.</p>
        <p v-else-if="productsLeft === 10">There are exactly 10 products left in stock.</p>
        <p v-else>There are less than 10 products left in stock.</p>
    </div>
</template>


<script>
    export default {
        name: 'VueDirectives',
        data() {
            return {
                productsLeft: 9,
            }
        }
    }
</script>