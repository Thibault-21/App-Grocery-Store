<template>
  <div class="main">
      <Fruit :key="fruit.id" v-for="fruit in fruits" :fruit="fruit"></Fruit>
    </div>
</template>

<script>
// import {mapGetters} from 'vuex'
import Fruit from './Fruit'
export default {
  components: {
    Fruit, 
  }, 
  computed: {
    fruits(){
      return this.$store.getters.getFruits;
       /*eslint-disable */
    },
  }
}

</script>

<style scoped>
.main {
  /* background-color: lightgray; */
  padding: 0px;
  margin: 0px 70px 0 0; 
  border-radius: 5px;
}
</style>
