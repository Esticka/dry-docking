<template>

<div class="card">

    <input
        type="text"
        placeholder="Title"
    >

    <textarea
        placeholder="Description"
    ></textarea>

</div>

</template>

<style scoped>

.card{

border:1px solid #ececec;

padding:14px;

border-radius:10px;

margin-bottom:15px;

}

input{

width:100%;

padding:10px;

margin-bottom:10px;

border:1px solid #ddd;

border-radius:8px;

}

textarea{

width:100%;

height:80px;

padding:10px;

resize:none;

border:1px solid #ddd;

border-radius:8px;

}

</style>

<script setup>

defineProps({

title:String,

description:String

})

</script>

<style scoped>

.card{

padding:15px;

border:1px solid #ececec;

border-radius:10px;

margin-bottom:15px;

background:white;

}

.status{

display:inline-block;

background:#fff4d6;

color:#d98a00;

padding:4px 10px;

border-radius:20px;

font-size:12px;

margin-bottom:10px;

}

.card h4{

margin-bottom:8px;

}

.card p{

font-size:13px;

color:#666;

margin-bottom:15px;

}

button{

width:100%;

background:#2f90e8;

border:none;

padding:10px;

color:white;

border-radius:8px;

cursor:pointer;

}

</style>