<template>
  <div id="app">
      <header-one  :isDark="isDark" @toggleTheme="toggleTheme"/>
      <section-one  :isDark="isDark" @toggleTheme="toggleTheme"/>
  </div>
</template>

<script>
import header from './components/header.vue'
import section from './components/section.vue'

export default{
  data(){
    return{
      isDark:false
    }
  },
  components:{
    "header-one":header,
    "section-one":section,
  },
  methods: {
    toggleTheme() {
      this.isDark = !this.isDark
    }
  }
}
</script> 

