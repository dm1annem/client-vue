<template>
  <div>
    <MyHeader/>
    <Nuxt />
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from '@/components/site/layouts/Header/Header.vue'
import MyFooter from '@/components/site/layouts/footer/Footer.vue'
export default {
  components:{
    MyHeader,
    MyFooter
  }
  
}
</script>

<style>
</style>

