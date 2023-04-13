<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                logoImg: 'dc-logo.png',
                navList: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP']
            }
        },
        methods: {
            getLogoImg(img) {
                return new URL(`../../public/img/${img}`, import.meta.url).href;
            }
        }
    }
</script>

<template>
    <div class="header">
        <div class="logo">
            <img :src="getLogoImg(logoImg)" alt="DC-logo">
        </div>
        <div class="list-container">
            <ul>
                <li v-for="(item, index) in navList">{{ item }}</li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">

</style>