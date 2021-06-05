<template>
    <header class=" ">
        <div>
            <MyTopHeader/>
        </div>
        
        <nav  class="flex justify-center w-full bg-yellow-100 ">
            <span>menu</span>
        </nav>
    </header>
  
</template>

<script>
import MyTopHeader from '@/components/site/layouts/Header/TopHeader.vue'
export default {
    components:{
        MyTopHeader,
    }

}
</script>

<style>

</style>