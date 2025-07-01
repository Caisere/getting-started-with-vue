<template>
    <img src="../assets/myimg.jpeg" alt="user avatar" class="avatar">
</template>

<script>
    export default {
        name: 'UserAvatar',
    }
</script>

<style scoped>
    .avatar {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        border: 2px solid #42b983;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
</style>