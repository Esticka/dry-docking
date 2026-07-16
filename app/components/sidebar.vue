<template>
  <aside class="sidebar">

    <div class="logo">
      <span>Dry Dock</span>
    </div>

    <nav class="menu">

      <a href="#" class="menu-item active">
        Dashboard
      </a>

      <a href="#" class="menu-item">
        Jobs
      </a>

      <a href="#" class="menu-item">
        Dry Docks
      </a>

    </nav>

  </aside>
</template>

<style scoped>

.sidebar{
    width:240px;
    min-height:100vh;
    background:#2f90e8;
    color:white;
    padding:25px 20px;
}

.logo{
    display:flex;
    align-items:center;
    gap:10px;
    font-size:24px;
    font-weight:bold;
    margin-bottom:40px;
}

.menu{
    display:flex;
    flex-direction:column;
    gap:10px;
}

.menu-item{
    text-decoration:none;
    color:white;
    padding:14px 16px;
    border-radius:8px;
    transition:.2s;
}

.menu-item:hover{
    background:rgba(255,255,255,.15);
}

.active{
    background:rgba(255,255,255,.2);
    font-weight:bold;
}

</style>