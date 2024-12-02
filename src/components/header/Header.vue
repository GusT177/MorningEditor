<script>
</script>

<template>
 <header class="menu">
      <nav class="options">
        <ul>
          <li><button>File</button></li>
          <li><button>Edit</button></li>
        </ul>
        <select name="" id=""></select>
      </nav>
  </header>
</template>

<style scoped>
.menu{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    text-align: center;
    border-bottom: 2px solid yellow;
    padding: 1rem;
}

.options{
    display: flex;
    justify-content: center;
    list-style: none;
    gap: 1rem;
}

ul{
    display: flex;
    list-style: none;
    gap: 0.5rem;
    color: white;
}

button{
    background: none;
    outline: none;
    color: white;
    padding: 0.5rem;
    border-bottom: 1px solid yellow;
}

select{
    width: 3rem;
}

</style>