<script>
export default {
  props: {
    moviedObj: Object,
  },
  
  data() {
    return {
    
   
    };
  },
  computed: {
    cardTitle() {
      return !!this.moviedObj.title ? this.moviedObj.title : this.moviedObj.name;

    },
    cardOriginalTitle() {
      return !!this.moviedObj.original_title ? this.moviedObj.original_title : this.moviedObj.original_name;
    }
    
  },
  methods: {
    // bandiera 
    getFlag(language) {
      if (!language) return "";
      switch (language.toLowerCase()) {
        case 'it':
        return new URL(`../assets/img/italy.png`, import.meta.url).href;
        case 'en':
          return new URL(`../assets/img/england.png`, import.meta.url).href;
        case 'es':
          return new URL(`../assets/img/spain.png`, import.meta.url).href;
        default:
          return new URL(`../assets/img/other.png`, import.meta.url).href;
      }
    },
  },
  
 
 
};


</script>

<template>

</template>


<style>
.flagMovie{
  width: 15%;
  margin: 10px;
}
</style>