<template>
    <header class=" shadow-md">
        <div>
            <MyTopHeader/>
        </div>
        
        <nav  class="flex justify-center bg-indigo-50 ">
            <div class="my-2" v-for="(link, i) in links" :key="i">
                <NuxtLink :to="link.path" exact active-class="text-blue-300 border-b-2 border-yellow-300" class=" mx-4 px-3  text-lg text-gray-500 hover:text-blue-300 ">
                    {{ link.text }} 
                </NuxtLink>
            </div>
            
            <i class="fa fa-bars text-xl right-0" aria-hidden="true" v-on:click="drawer=!drawer"></i>
            
        </nav>
    <!-- Overlay  -->
        <transition
            enter-class="opacity-0"
            enter-active-class="transition-opacity ease-linear duration-300"
            enter-to-class="opacity-100"
            leave-class="opacity-100"
            leave-active-class="transition-opacity ease-linear duration-200"
            leave-to-class="opacity-0"
        >
            <div v-show="drawer" class="fixed  top-0 bottom-0 left-0 right-0 overflow-auto w-full h-full bg-black bg-opacity-50" v-on:click="drawer=!drawer"></div>
        </transition>
<!-- Боковое меню -->
        <transition
            enter-class="-translate-x-full"
            enter-active-class="transition ease-in-out duration-700 transform"
            enter-to-class="translate-x-0"
            leave-class="translate-x-0"
            leave-active-class="transition transform  ease-in-out duration-300"
            leave-to-class="-translate-x-full"
        >
            <aside v-show="drawer" class="fixed  top-0 h-full w-96 bg-blue-50 " >
                <p>nnnnnnffnfnfnfnsddddcdcdcdcdcdcdcdcdssss</p>
            </aside>
        </transition>
        
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