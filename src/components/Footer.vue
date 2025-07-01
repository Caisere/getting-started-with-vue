<template>
    <footer class="footer">
        <p>&copy; {{year}} My Vue App. All rights reserved.</p>
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponent',
        data(){
            const currentYear = new Date().getFullYear();
            return {
                year: currentYear,
            };
        }
    }
</script>