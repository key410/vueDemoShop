<script setup>
</script>

<template>
    <ul class="menu_list">
        <li><button class="menu_link">About</button></li>
        <li><button class="menu_link" onclick="location.href='https://github.com/key410/vueDemoShop/tree/main/vuePort'">Git</button></li>
        <li><img src="./../static/cart.svg" class="icon"></li>
    </ul>
</template>

<style>
.menu_list {
    display: flex;
    width: 300px;
    margin: 0 0 0 auto;
    list-style: none;

}
.menu_list li{
    width: 100%;
    text-align: center;
    padding: 10px;
    margin: 0;
}
.menu_link {
    font-size:medium;
    cursor: pointer;
    transition: all 1s;
}
.menu_link:hover {
    transform: rotateX(360deg);
}
</style>