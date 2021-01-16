<template>
  <Layout>
    <div class="px-4 py-8">

      <div class="text-xl font-bold text-center">
        <div>La santé a bon goût</div>
         <div>et en plus, elle est locale !</div>
      </div>

      <div class="p-4">
        <div>Je crois que nous ne devrions pas avoir à choisir entre le bon gout des aliments et notre santé. </div>
        <br>
        <div>
          C'est pourquoi je fais de delicieuses confitures produites avec des fruits direct producteur du Lot et Garonne.
        </div>

      </div>
    </div>

    <div class="p-4" v-for="confiture in confitures" :key="confiture.url">
        
        <router-link :to="'/produit/' + confiture.url">
            <div class="flex flex-col justify-center py-4">
                <img class="rounded-t-lg" :src="confiture.imageUrl"/>
                <div class="flex justify-center py-2 font-semibold bg-gray-200 rounded-b-lg">{{ confiture.name }} </div>
            </div>
        </router-link>
        
      </div>

  </Layout>
</template>
<script>
import Layout from "@/components/layout"
import json from "@/data.json"

export default {
  components: {
    Layout
  },
  data() {
    return {
      confitures: json.confitures
    }
  }

}
</script>

<style>

</style>