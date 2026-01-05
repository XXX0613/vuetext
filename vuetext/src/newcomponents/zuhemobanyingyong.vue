<template>
    <div class="zuhemobanyingyong">
        <h3>组合式---模板应用</h3>
        <p ref="message">这是组合模板应用的内容</p>
        <hr>
    </div>
</template>

<script setup>
import { ref, onMounted, watch } from 'vue';

const message = ref(null);

onMounted(() => {
    // console.log(message.value);
    message.value.style.color = 'Aqua';
    message.value.style.fontSize = '30px';
    message.value.style.innerHtml = '====666655556565++++';
})

</script>

<style scoped>
.zuhemobanyingyong{
    
    color: red;
}
</style>