<template>
    <header class=" ">
        <div>
            <MyTopHeader/>
        </div>
        
        <nav  class="flex justify-center bg-yellow-100 ">
            <div class="my-2" v-for="(link, i) in links" :key="i">
                <NuxtLink :to="link.path" exact active-class="text-blue-300 border-b-2 border-yellow-300" class=" mx-4 px-3  text-lg text-gray-500 hover:text-blue-300 ">
                    {{ link.text }} 
                </NuxtLink>
            </div>
            
            <i class="fa fa-bars text-xl right-0" aria-hidden="true" v-on:click="drawer=!drawer"></i>
            
        </nav>
    <!-- мобильное меню  -->
        <div v-show="drawer" class="fixed  top-0 bottom-0 left-0 right-0 overflow-auto w-full h-full bg-black bg-opacity-50" v-on:click="drawer=!drawer">
            <div class="h-full w-96 bg-blue-50 " >

            </div>
        </div>
    </header>
  
</template>

<script>
import MyTopHeader from '@/components/site/layouts/Header/TopHeader.vue'
export default {
    components:{
        MyTopHeader,
    },
    data(){
        return {        
            links: [
                {text: 'Главная', path:'/'},
                {text: 'Проекты', path:'/site/projects'},
                {text: 'Примеры работы', path:'/site/examples'},
                {text: 'Отзывы клиентов', path:'/site/reviews'},
                {text: 'Цены', path:'/site/other/prices'},
                {text: 'Контакты', path:'/site/other/contacts'},
            ],
            drawer: false,
        }
    }

}
</script>

<style>
.nuxt-link-active {
  color: rgb(17, 224, 69);
}

</style>