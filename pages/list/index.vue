<template>
    <div id="list">
      <NavBar/>
      <p>{{$route.params.id}}</p>
      <p>list</p>


    </div>
</template>

<script>
import NavBar from '@/components/NavBar'
export default {
  name: "index.vue",
  components: {
    NavBar

  },
  data(){
    return{
      params: this.$route.params.id
    }
  },

}
</script>

<style scoped>

</style>
