<template>
    <header class=" shadow-md">
        <div>
            <MyTopHeader
                @openDrawer="openDrawer"
            />
        </div>
        
        <nav  class="hidden lg:flex justify-center bg-green-100 ">
            <div class="my-2" v-for="(link, i) in links" :key="i">
                <NuxtLink :to="link.path" exact active-class="text-blue-300 border-b-2 border-yellow-300" class=" mx-4 px-3  text-lg text-gray-500 hover:text-blue-300 ">
                    {{ link.text }} 
                </NuxtLink>
            </div>
            
            
            
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
            <div v-show="drawer" class="fixed  inset-0 overflow-auto w-full h-full bg-black bg-opacity-50" v-on:click="openDrawer"></div>
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
            <aside v-show="drawer" class="fixed  top-0 h-full w-full bg-green-50 z-40" >
                <div class="flex justify-end">
                    <div >
                        <i class="fa fa-times  text-4xl mr-5 mt-1 text-gray-500" aria-hidden="true" v-on:click="openDrawer"></i>
                    </div>
                    
                </div>
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
    },
    methods:{
        openDrawer(){
            this.drawer=!this.drawer
        }
    }

}
</script>

<style>
.nuxt-link-active {
  color: rgb(17, 224, 69);
}

</style>