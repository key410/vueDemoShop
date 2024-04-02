<script setup>
import {ref, computed, defineProps, watch} from "vue";
const onItem = ref(false);
const props = defineProps(["itemName", "imagePath", "price"])
const formatPrice = computed(
    () => {return props.price.toLocaleString()}
) 

</script>
<template>
    <button class="item" @click="onItem=true">
        <img :src="imagePath" class="item_img">
        <div>{{ itemName }}</div>
        <div>￥{{ formatPrice }} (税込)</div>
    </button>
    <div class="modal overlay" v-show="onItem" @click="onItem=false">
      <img :src="imagePath" class="modal_img">
    </div>
</template>

<style>
.item {
    margin: 50px 20px 80px 20px;
}
.item_img {
    inset: 0;
    margin: auto;
    width: 300px;
    height: 300px;
    object-fit: cover;
    border-radius: 15px;
    transition: filter 0.5s ease;
}
.item_img:hover {
    filter: brightness(50%);
}
.overlay {
    z-index:1;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background-color:rgba(0, 0, 0, 0.541);
    display: flex;
    align-items: center;
    justify-content: center;
}
.modal_img {
    z-index:2;
    width: 600px;
    height: 600px;
    object-fit: cover;
    border-radius: 15px;
}
</style>