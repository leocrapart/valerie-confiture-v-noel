<template>
    <div>
        <div>test page</div>
        <div v-for="confiture in confitures"
        :key="confiture.url">
            {{ confiture }}
            <div class="w-64">

                <img :src="confiture.imageUrl" alt="">
            </div>
        </div>

        <div>url</div>
        <div>
            {{ $route.path }}
        </div>
        

    </div>
</template>

<script>

import json from '@/data.json'
export default {
    data() {
        return {
            confitures: json.confitures
        }
    },
    mounted() {
       this.data = data
    }
}
</script>