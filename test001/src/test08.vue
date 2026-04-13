<script setup>
    import { ref } from 'vue';

    const score =  ref(75) ;
    
</script>
<template>
    <div>
        <h1>分數 : {{ score }} <span v-show="score == 100">⭐</span> <span v-show="score <60">🚫</span></h1>
        <div v-if="score >= 90 ">優等</div>
        <div v-if="score >= 80 && score < 90">甲等</div>
        <div v-if="score >= 60 && score < 80">乙等</div>
        <div v-if="score < 60 && score >= 0">不及格</div>
        <input type="number" v-model.number="score" min="0" max="100" >
    </div>
</template>
<style scoped></style>