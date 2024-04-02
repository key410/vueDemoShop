<script setup>
import {ref} from "vue";
import Item from "./Item.vue";

var id = 0;
var Items = ref([
    {id: id++, itemName:"珈琲", imagePath:"/image/coffee.jpeg", price:500},
    {id: id++, itemName:"紅茶", imagePath:"/image/tea.jpg", price:500},
    {id: id++, itemName:"花", imagePath:"/image/flower.jpg", price:800},
    {id: id++, itemName:"ビール", imagePath:"/image/beer.jpg", price:700},
    {id: id++, itemName:"兎", imagePath:"/image/rabi.jpg", price:36000},
    {id: id++, itemName:"フレーバーティー", imagePath:"/image/flavortea.jpg", price:550}
])
</script>

<template>
    <div class="body_main">
        <Item 
            v-for="item in Items" 
            :itemName="item.itemName"
            :imagePath="item.imagePath"
            :price="item.price"
            />
    </div>
</template>
<style>
.body_main {
    display: grid;
    grid-template-columns:1fr 1fr 1fr;
}
</style>