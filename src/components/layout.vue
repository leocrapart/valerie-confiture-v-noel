<template>
  <div class="relative min-h-screen">
    <div class="fixed w-full bg-gray-100">
        <div class="flex justify-between py-4 mx-2 border-b-2 ">
        <div>
            <router-link to="/">
            Confitures
            </router-link>
        </div>

        <div>
            <a href="https://facebook.com">Facebook</a>
        </div>
        <div>
            <a href="https://instagram.com">Instagram</a>
        </div>

        <div>
            <router-link to="/A-propos">A propos</router-link>
        </div> 
        </div>
    </div>

    <div class="p-8"></div>
    
    <slot></slot>

    <!-- 
    <div class="">
        <div>
            <router-link to="/A-propos">
            <div class="absolute bottom-0 w-full h-10 bg-gray-300 hover:bg-gray-400">
                <div class="mt-2 ml-2 text-center">
                <div class="">
                    A propos
                </div>
                </div>
            </div>
            </router-link>
        </div>
        
    </div>
    -->

    

  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>