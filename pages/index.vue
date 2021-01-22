<template>
  <div id="container">
    <NavBar/>
    <div class="flex flex-col w-4/5 ml-auto mr-auto ">
    <Right/>
    <Left/>
    </div>
    <Contact/>
    <p class="text-center mt-5 mb-5 font-sans">tout droit réservé timothé david 2020-{{date}}</p>
  </div>

</template>

<script lang="ts">
import Vue from 'vue'
import NavBar from '@/components/NavBar.vue'
import Right from '@/components/Right.vue'
import Left from '@/components/Left.vue'
import Contact from '@/components/Contact.vue'

export default{
  components :{
    NavBar,
    Right,
    Left,
    Contact
  },
  data(){
    return {
      date : new Date().getFullYear(),
    }
  },

}
</script>

<style>
*{
  margin : 0;
  padding : 0;
}


</style>
