<script setup>
    import { ref } from 'vue';

    const count = ref(0);
    
    function handleClick(){
        count.value++;
    
    }
    const handleClick2 = (num) => {
        count.value += num;
    }
    function restCount(){
        count.value = 0;
    }

</script>
<template>
    <div>
        <h1>{{ count }}</h1>
        <button v-on:click="handleClick">呼叫方法</button>
        <button v-on:click="count++">直接增加</button>
        <button v-on:click="handleClick2(5)">傳參數增加</button>
        <button v-on:click="restCount">重製</button>
    </div>
</template>
<style scoped></style>