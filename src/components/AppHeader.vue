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
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            }
        }
    }
</script>

<template>
    <div class="header-bg">
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
    </div>
</template>

<style scoped lang="scss">

@use "../style/style.scss" as *;

.header-bg {
    width: 100%;
    background-color: white;
    .header {
    @include flex(row, space-between, center);
    @include containerWdt(80%);
    height: 115px;
    margin: 0 auto;
    padding: 10px 0;

    .logo {
        width: 80px;
    }

    .list-container {
        @include flex(row, flex-end, center);
        width: 100%;
        ul {
            @include flex(row, space-between, center);
            list-style-type: none;

            li {
                cursor: pointer;
                font-size: 0.8rem;
                margin: 0 5px;
            }
        }
    }
}
}
</style>