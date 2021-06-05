<template>
    <header class=" ">
        <div>
            <MyTopHeader/>
        </div>
        
        <nav  class="flex justify-center bg-yellow-100 ">
            <div class="my-2" v-for="(link, i) in links" :key="i">
                <NuxtLink :to="link.path" exact active-class="text-gray-100 border-b-2 border-yellow-200" class=" mx-4 px-3  text-lg text-gray-500 hover:text-gray-300 ">
                    {{ link.text }} 
                </NuxtLink>
            </div>
            
        </nav>
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
            ]
        }
    }

}
</script>

<style>
.nuxt-link-active {
  color: rgb(17, 224, 69);
}

</style>