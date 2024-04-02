<script setup>
import {ref} from "vue";
import Item from "./Item.vue";

var id = 0;
var Items = ref([
    {id: id++, itemName:"珈琲", imagePath:"/src/static/coffee.jpeg", price:500},
    {id: id++, itemName:"紅茶", imagePath:"/src/static/tea.jpg", price:500},
    {id: id++, itemName:"花", imagePath:"/src/static/flower.jpg", price:800},
    {id: id++, itemName:"ビール", imagePath:"/src/static/beer.jpg", price:700},
    {id: id++, itemName:"兎", imagePath:"/src/static/rabi.jpg", price:36000},
    {id: id++, itemName:"フレーバーティー", imagePath:"/src/static/flavortea.jpg", price:550}
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