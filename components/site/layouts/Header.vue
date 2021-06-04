<template>
    <header class=" ">
        <div class="grid grid-cols-12  gap-x-2 justify-between mt-3 mx-4 md:mx-5">
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
                            <a href="tel:+79308200225" class="hover:underline hover:text-indigo-500 ">
                                <i class="fa fa-phone text-xl  ml-1 text-yellow-600 hover:text-indigo-500"></i> <span class="text-xl">+7(4832)30-02-25</span>
                            </a>	
                    </p>
                </div>   
            </div>
            
                
            <div>
                <NuxtLink to="#">
                    <i class="fa fa-sign-in  text-xl ml-1 text-gray-500 flex justify-end"></i>
                </NuxtLink>
            </div>
        </div>
        <nav  class="flex justify-center w-full bg-yellow-100 ">
            <span>menu</span>
        </nav>
    </header>
  
</template>

<script>
export default {

}
</script>

<style>

</style>