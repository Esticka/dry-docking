<template>
  <div class="column">

    <div class="column-header">
      <span>{{ ship.name }}</span>

      <button class="add-btn">
        +
      </button>
    </div>

    <div class="company-card">

      <img
        src="https://picsum.photos/60"
        alt="Ship"
      />

      <div>

        <h4>{{ ship.company }}</h4>

        <p>{{ ship.code }}</p>

      </div>

    </div>

    <QuoteCard />
    <QuoteCard />
    <QuoteCard />

  </div>
</template>

<script setup>
import QuoteCard from './quotecard.vue'

defineProps({
  ship: Object
})
</script>

<style scoped>

.column{
    width:320px;
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
    font-size:30px;
    color:#888;
    cursor:pointer;
}

.company-card{

    display:flex;

    gap:15px;

    align-items:center;

    background:white;

    border:1px solid #ececec;

    border-radius:10px;

    padding:12px;

    margin-bottom:15px;

}

.company-card img{

    width:55px;

    height:55px;

    border-radius:8px;

    object-fit:cover;

}

.company-card h4{

    margin-bottom:6px;

    font-size:16px;

}

.company-card p{

    color:#777;

    font-size:14px;

}

</style>