<template>
  <div class="job-card">

    <h4>{{ job.title }}</h4>

    <p class="code">{{ job.code }}</p>

    <span class="type">
      {{ job.type }}
    </span>

  </div>
</template>

<script setup>
defineProps({
  job: Object
})
</script>

<style scoped>

.job-card{
  background:white;
  border:1px solid #ececec;
  border-radius:10px;
  padding:14px;
  margin-bottom:12px;
}

.job-card h4{
  font-size:14px;
  line-height:1.4;
  margin-bottom:8px;
}

.code{
  color:#777;
  font-size:13px;
  margin-bottom:8px;
}

.type{
  display:inline-block;
  background:#eef5ff;
  color:#2f90e8;
  font-size:12px;
  padding:4px 10px;
  border-radius:20px;
}

</style>