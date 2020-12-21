<template>
  <Layout>
    <div>
      <div class="px-4 pt-4 mx-4  bg-gray-200 rounded">
        <div class="mb-2 font-bold">Points de vente</div>
        <div class="mb-2">La liste est disponible <router-link class="text-blue-500" to="points-de-vente"> ici </router-link></div>
        <br>
        
        <div class="mb-2 font-bold">Où sont fabriquées toutes ces confitures?</div>
        <div>A Caumont sur Garonne (47300) </div>
        <br>

        <div class="mb-2 font-bold">Me contacter</div>
        <div class="mb-2">Par téléphone au 06 40 23 04 66</div>

        <div>Ou par mail à valdemeautis@gmail.com</div>
        <br>

        <div class="font-semibold">Merci pour votre soutien !</div>
        <br>
        <img src="https://ik.imagekit.io/pl6zwucqxr/maman_MhNM5tkEP.png">

      <img>
      </div>
    </div>

    
  </Layout>
</template>

<script>
import Layout from "@/components/layout"

export default {
  components: {
    Layout
  }
}
</script>
