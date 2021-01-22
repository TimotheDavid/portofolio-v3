<template>
  <div id="navbar" class="flex flex-col items-center bg-blue-700 md:flex-row md:justify-between md:pr-4 md:pl-4 md:items-center">
    <div id="logo" class="mb-5 mt-5 text-white font-sans text-2xl md:text-3xl">
      Timothé David
    </div>
    <div class="flex flex-col items-center mb-5 md:flex-row md:items-center md:mb-0">
      <div class="mb-3 text-white font-sans text-sm md:mr-3 md:text-base md:mb-0" v-for="nav in data">
        <div v-if="nav.type === 'main'">
          <NuxtLink to="/">{{nav.label}}</NuxtLink>
        </div>
        <div v-else-if="nav.type === 'list'">
          <NuxtLink :to="{name: 'list', params: {id:nav.id}}">{{nav.label}} {{nav.id}}</NuxtLink>
        </div>
        <div v-else-if="nav.type === 'project'">
          <NuxtLink :to="{name: 'project', params:{id: nav.id}}">{{nav.label}} {{nav.id}}</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar.vue",
  props: ["navbar"],
  data(){
    return{
      data: [
        {
          "id" : 0,
          "label":  "A propos",
          "type" : "main"
        },{
          "id" : 1,
          "label":  "Veille technologique",
          "type": "project"
        },{
          "id" : 2,
          "label":  "Veille Juridique",
          "type" : "project"
        },{
          "id" : 3,
          "label":  "Projet",
          'type' : 'list'
        },{
          "id" : 4,
          "label":  "Epreuve E4",
          'type' : 'list'
        },{
          "id" : 5,
          "label":  "Epreuve E6",
          'type' : 'list'
        }
      ],
    }
  },
}
</script>

<style scoped>
#navbar{
  width : 100%;
}

#logo {
  font-family : Roboto, serif;
}


</style>
