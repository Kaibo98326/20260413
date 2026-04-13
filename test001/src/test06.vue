<script setup>
    const handleSubmit = (e) => {
        // e.preventDefault();
        console.log("wwww");
        
    }
</script>
<template>
    <form @submit.prevent>
        <div class="row">
            <label for="userId">ID : </label>
            <input type="text" id="userId" name="userId" placeholder="輸入使用者帳號" @keydown.shift.enter.prevent="handleSubmit">
        </div>
        <div class="row">
            <label for="userPWD">Password : </label>
            <input type="password" id="userPWD" name="userPWD" placeholder="輸入使用者密碼" @keydown.shift.enter.prevent="handleSubmit">
        </div>
        <div class="ctrl">
            <button @click="handleSubmit">送出</button>
        </div>
    </form>
</template>
<style scoped>
.row{
     display: flex;

     input{
        flex: 1 ;
     }
}
.ctrl{
    display: flex;
    justify-content: flex-end;
    
}

</style>