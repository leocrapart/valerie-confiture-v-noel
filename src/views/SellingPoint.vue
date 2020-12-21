<template>
  <Layout class="px-4">
        <div class="flex justify-center">
            <div class="text-lg py-4 font-semibold">
                Points de vente
            </div>
        </div>

        <div v-for="type in pointVente" :key="type.nomType">
            <div class="border-t-4"></div>

            <div class="font-bold text-lg">{{ type.nomType }} </div>
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
                            site: "http://www.le-gout-des-saisons.com/",
                            rue: "7 Loiseau",
                            codePostal: "33126 Fronsac",
                            reseauSocial: "",
                            urlReseauSocial: "",
                        },
                        {
                            nom: "Le Goût des Saisons",
                            site: "http://www.le-gout-des-saisons.com/",
                            rue: "889-893 Avenue du Maréchal Foch",
                            codePostal: "40000 Mont-de-Marsan",
                            reseauSocial: "",
                            urlReseauSocial: "",
                        },
                        {
                            nom: "La Source Origin'elles",
                            site: "https://www.lasourceoriginelles.fr/",
                            rue: "5 Avenue des Martyrs de la Résistance",
                            codePostal: "47200 Marmande",
                            reseauSocial: "Facebook: Lasource Originelles",
                            urlReseauSocial: "https://www.facebook.com/SourceOriginelles"
                        },
                    ]
                },
                type2: {
                    nomType: "Point Poste",
                    liste: [
                        {
                           nom: "Point Poste",
                           site: "",
                           rue:"Le bourg",
                           codePostal: "47430 Caumont-Sur-Garonne",
                           reseauSocial: "",
                           urlReseauSocial: "",
                        },

                    ]

                },
                type3: {
                    nomType: "Boulangerie",
                    liste: [
                        {
                           nom: "Boulangerie La Panetière Valsesia",
                           site: "",
                           rue:"4 avenue Jacques Bordeneuve",
                           codePostal: "47300 Villeneuve Sur Lot",
                           reseauSocial: "Facebook: la panetiere valsesia",
                           urlReseauSocial: "https://www.facebook.com/la.panetiere.valsesia",
                        },
                        {
                           nom: "Boulangerie Epi d'Or",
                           site: "",
                           rue:"Le bourg",
                           codePostal: "47430 Mas d'Agenais",
                           reseauSocial: "",
                           urlReseauSocial: "",
                        },
                        {
                           nom: "Boulangerie-Patisserie Reboux-Denaules",
                           site: "",
                           rue:"52 avenue Garonne",
                           codePostal: "47430 Mas d'Agenais",
                           reseauSocial: "",
                           urlReseauSocial: "",
                        },
                        {
                           nom: "Boulangerie-Patisserie Varona Reboux",
                           site: "",
                           rue:"36 Avenue du Général de Gaulle",
                           codePostal: "47180 Sainte-Bazeille",
                           reseauSocial: "",
                           urlReseauSocial: "",
                        },
                        {
                           nom: "Pani Fournil 113",
                           site: "",
                           rue:"15 Avenue du Général de Gaulle",
                           codePostal: "47180 Sainte-Bazeille",
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