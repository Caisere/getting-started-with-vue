<template>
    <div>
        <h2>Vue Directives</h2>
        <input  v-model="userName" type="text" />
        <p>{{ productsLeft }}</p>
        <button @click="productsLeft++">Increase Product value to see changes in the UI</button>
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
                userName: ''
            }
        },
        directives: {
            focus: {
                inserted: function (el) {
                    el.focus()
                }
            }
        }
    }
</script>