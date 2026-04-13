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
        <div class="row">
            <button @click="count > 0 && count--">-</button>
            <h1>{{ count }}</h1>
            <button @click="count++">+</button>
        </div>
        <button @click="handleClick">呼叫方法</button>
        <button @click="count++">直接增加</button>
        <button @click="handleClick2(5)">傳參數增加</button>
        <button @click="restCount">重製</button>
    </div>
</template>
<style scoped>
.row{
    display: flex;
    
    align-items: center;

    h1{
        width: 100px;
        text-align: center;
    }
}
</style>