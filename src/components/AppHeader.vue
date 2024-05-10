<script >
import { store } from "../store";
export default {
  data() {
    return {
     store,
    };
  },

 
 
};

</script>

<template>
  <header>
  <div class=" container d-flex justify-content-between align-items-center"> 
  <div>
    <h1>BOOLFLIX</h1>
  </div>
   <div>
    <label for="search">Cerca il tuo film!</label>
                <div>
                    <input v-model="store.searchQuery" id="search" type="text" placeholder="scrivi qui..">
                    <button @click="$emit('cercaFilm')">Cerca</button>
   </div>
  </div>
  </div>
</header>
</template>

<style lang="scss" scoped>
header {
background-color: black;

  h1 {
  color:red;
}
}

</style>