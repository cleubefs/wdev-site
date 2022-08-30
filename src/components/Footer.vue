<template>
<footer>
 <a class="socialLink" v-for="(socialLink, index) in socialLinks" :key="index" :href="socialLink.link" target="_blank">
    <img :alt="socialLink.label" :title="socialLink.label" :src="socialLink.icon" >
     </a>   

</footer>
</template>

<script>
import api from  '@/services/api.js'

export default {
    name: 'TheFooter',
    data (){
        return {
            socialLinks:[]
        }
    },
    mounted (){
        api.get('/social-links.json').then(response=> {
            this.socialLinks = response.data; 
        })
    }
}

</script>

<style scoped>

 footer {
    height: 60px;
    width: 100%;
    background-color: var(--color-background-nav);
    display: flex;
    justify-content: center;
    align-items: center;
 }
    .socialLink img{
        width: 20px;
    }

    .socialLink{
        border: 3px solid var(--color-text-light);
        display: flex;
        align-items: center;
        justify-items: center;
        justify-content: center;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        margin: 0 10px;
    }
</style>