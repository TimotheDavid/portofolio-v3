<template>
      <div id="project">
        <navbar/>
        {{this.$route.params.id}}
        <p>project</p>
      </div>
</template>

<script>

import navbar from '@/components/NavBar'
export default {
  name: "index",
  components : {
    navbar
  },
  data(){
    return{
      params : this.$route.params.id
    }
  },
}
</script>

<style scoped>

</style>
