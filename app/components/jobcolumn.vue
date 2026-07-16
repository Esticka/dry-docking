<template>

<div class="column">

  <div class="column-header">

    <span>{{ title }}</span>

    <button class="add-btn">+</button>

  </div>

  <JobCard
    v-for="job in jobs"
    :key="job.id"
    :job="job"
  />

  <div class="placeholder">
    <input placeholder="Judul..." />
    <textarea placeholder="Deskripsi..."></textarea>
  </div>

</div>

</template>

<script setup>

import JobCard from './jobcard.vue'

defineProps({
  title:String,
  jobs:Array
})

</script>

<style scoped>

.column{
  width:330px;
  background:white;
  border:1px solid #e6e6e6;
  border-radius:10px;
  padding:15px;
  flex-shrink:0;
}

.column-header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:15px;
}

.column-header span{
  font-size:15px;
  font-weight:700;
}

.add-btn{
  border:none;
  background:transparent;
  font-size:28px;
  color:#888;
  cursor:pointer;
}

.placeholder{
  border:1px dashed #dcdcdc;
  border-radius:10px;
  padding:12px;
  margin-top:15px;
}

.placeholder input{

  width:100%;
  padding:8px;
  margin-bottom:8px;
  border:1px solid #ddd;
  border-radius:6px;

}

.placeholder textarea{

  width:100%;
  height:70px;
  resize:none;
  padding:8px;
  border:1px solid #ddd;
  border-radius:6px;

}

</style>