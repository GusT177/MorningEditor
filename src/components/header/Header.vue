<script>
export default{
    name: 'Language',
    data(){
        return{
            languages: ["JS", "Python", "Java", "C++", "Ruby", "PHP"],
        }
    },
    props: [],
}

</script>

<template>
 <header class="menu">
      <nav class="options">
        <ul>
          <li>
            <select>
                <option value="File">{{ FileOptions }}</option>
            </select>
          </li>
          <li>
            <select>
            </select>
          </li>
        </ul>
        <select name="" id="">
            <option value="Language" v-for="language in languages" :key="index">{{ language }}</option>
        </select>
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
    background-color: rgb(41, 40, 40);
    width: 5rem;
    padding: 0.5rem;
    color: yellow;
}

</style>