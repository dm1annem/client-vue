<template>
    <section>
        <!-- Хедер для мобильных -->
        <div class="fixed top-0 right-0 left-0 lg:hidden flex justify-between bg-gray-500 shadow-md">
            <div class="m-1">
                <NuxtLink  to="/">
                    <div class="font-semibold text-xl">
                        <span class=" text-gray-300 semibold">Каркас</span><span class="text-yellow-300">Центр</span>
                    </div>
                    <!-- <img src="@/static/img/logo3.jpg" class="w-auto"> -->
                </NuxtLink >
            </div>
            <div class="flex">
                <a href="https://wa.me/message/S2HVLZUQSNBBN1" >
                    <i class="fa fa-whatsapp text-lg mt-1 text-gray-400 font-thin" aria-hidden="true"></i> 
                </a>
                <a href="tel:+79308200225">
                    <i class="fa fa-phone text-lg  ml-7 mt-1 text-gray-400 font-thin"></i> 
                </a>
            </div>
            <div >
                <i class="fa fa-bars text-2xl mr-5 mt-1 text-gray-300" aria-hidden="true" v-on:click="$emit('openDrawer')"></i>
            </div>

        </div>

        <!-- топхедер для десктопов -->
        <div class="hidden lg:grid grid-cols-12  gap-x-2 justify-between mt-3 mx-4 md:mx-5">
            <div class="col-start-1 col-span-2 mt-1.5" >
                <NuxtLink  to="/">
                    <img src="@/static/img/logo3.jpg">
                </NuxtLink >
            </div>
            <div class="col-start-3 col-span-4 grid justify-self-start">
                <div class="inline-block align-top max-w-xs">
                    <span class=" text-gray-500 ">Проектирование и строительство загородных домов в Брянске</span>
                </div>
            </div>
            <div class="col-start-7 col-span-5 ">
                <div >
                    <a href="https://vk.com/karkascentr"><i class="fa fa-vk mx-1 text-gray-500 " aria-hidden="true" ></i></a>
                    <a href="https://ok.ru/karkascentr.ru" ><i class="fa fa-odnoklassniki mx-1 text-gray-500 " aria-hidden="true"></i></a>
                    <a href="https://www.youtube.com/channel/UCJoHMcmHq115v7XriMA5ZiQ?view_as=subscriber" ><i class="fa fa-youtube-square mx-1 text-gray-500 " aria-hidden="true"></i></a>
                    <a href="https://www.instagram.com/karkascentr.ru/"><i class="fa fa-instagram mx-1 text-gray-500 " aria-hidden="true"></i></a>
                    <a href="https://www.facebook.com/karkascentr/" ><i class="fa fa-facebook mx-1 text-gray-500 " aria-hidden="true"></i></a>
                </div>
                <div class=" flex justify-end text-gray-600">
                    <p class="flex-shrink-0 mr-10 border-2 border-yellow-100 hover:border-yellow-300 rounded-xl px-3 mb-1 bg-gray-100">
                        <a href="https://wa.me/message/S2HVLZUQSNBBN1" >
                            <i class="fa fa-whatsapp text-xl ml-1 text-yellow-600" aria-hidden="true"></i> <span>Написать в WhatsApp</span>
                        </a>
                    </p> 
                    <p class="flex-shrink-0">
                            <a href="tel:+79308200225" class="text-gray-500 hover:underline">
                                <i class="fa fa-phone text-xl  ml-1 text-gray-400 hover:text-blue-400"></i> <span class="text-xl">+7(4832)30-02-25</span>
                            </a>	
                    </p>
                </div>   
            </div>
            
                
            <div>
                <NuxtLink to="#">
                    <i class="fa fa-sign-in  text-xl ml-1 text-gray-500 flex justify-end hover:text-yellow-600"></i>
                </NuxtLink>
                
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

