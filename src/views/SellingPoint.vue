<template>
  <Layout>
      <div class="px-4">
        <div class="flex justify-center">
            <div class="text-lg py-4 font-semibold">
                Points de vente
            </div>
        </div>

        <div v-for="type in pointVente" :key="type.nomType">
            <div class="border-t-4"></div>

            <div class="flex justify-center">
                <div class="font-bold text-lg">{{ type.nomType }} </div>
            </div>
            
            
            <div class="border-t-4 pb-4"></div>

            <div v-for="pointVente in type.liste" :key="pointVente.rue">
                <div v-if="pointVente.site" class="font-bold underline"><a :href="pointVente.site">{{ pointVente.nom }} </a></div>
                <div v-else class="font-bold"> {{ pointVente.nom }} </div>

                <div>{{ pointVente.rue }} </div>
                <div>{{ pointVente.codePostal }} </div>
                <div v-if="pointVente.reseauSocial" class="underline"><a :href="pointVente.urlReseauSocial">{{ pointVente.reseauSocial }}</a>  </div>
                <br>
            </div>
            
        </div>
      </div>


  </Layout>
</template>

<script>
import Layout from '@/components/layout'

export default {
    components: {
        Layout
    },
    data() {
        return {
            pointVente: {
                type1: {
                    nomType: "Magasin Direct Producteur",
                    liste: [
                        {
                            nom: "Le Goût des Saisons",
                            site: "",
                            rue: "7 Loiseau",
                            codePostal: "33126 Fronsac",
                            reseauSocial: "Facebook: Le goût des saisons",
                            urlReseauSocial: "https://www.facebook.com/Le-go%C3%BBt-des-saisons-1708549259380560/",
                        },
                        {
                            nom: "Le Goût des Saisons",
                            site: "",
                            rue: "889-893 Avenue du Maréchal Foch",
                            codePostal: "40000 Mont-de-Marsan",
                            reseauSocial: "Facebook: Le Gout Des Saisons, Producteur De Saveurs",
                            urlReseauSocial: "https://www.facebook.com/legoutdessaisons/",
                        },
                        {
                            nom: "La Ferme De La Bergerie",
                            site: "",
                            rue: "D813 La Bergerie",
                            codePostal: "47180 Sainte-Bazeille",
                            reseauSocial: "Facebook: La Ferme De La Bergerie",
                            urlReseauSocial: "https://www.facebook.com/FermeDeLaBergerie"
                        },
                        {
                            nom: "Lou Paney",
                            site: "",
                            rue: "Lieu dit Petit Piis",
                            codePostal: "47200 Marcellus",
                            reseauSocial: "Facebook: Lou Paney",
                            urlReseauSocial: "https://www.facebook.com/Lou-Paney-fruitsl%C3%A9gumesplantes-555610938281207/"
                        },
                    ]
                },
                type2: {
                    nomType: "Boulangerie",
                    liste: [
                        {
                           nom: "Boulangerie Epi d'Or",
                           site: "",
                           rue:"Le bourg",
                           codePostal: "47430 Mas d'Agenais",
                           reseauSocial: "",
                           urlReseauSocial: "",
                        },
                    ]
                }
            }
        }
    }
}
</script>

<style>

</style>