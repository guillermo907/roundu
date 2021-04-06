<template>
    <div class="navbar">
        <div class="navbar-left">
            Icon
        </div>
        <div class="navbar-right">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style scoped>
.navbar{
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgb(38, 183, 113);
    color: white;
    padding: 10px;
}
.navbar-right a{
    text-decoration: none;
    margin: 0 10px;
    color: white;
}
</style>