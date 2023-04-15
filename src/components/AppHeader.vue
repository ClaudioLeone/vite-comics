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
                    <li v-for="(item, index) in navList"  :key="index">{{ item }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;
@use "../style/colors.scss" as *;
.header-bg {
    height: var(--headerHeight);
    width: 100%;
    background-color: white;
    .header {
        width: 90%;
        height: var(--headerHeight);
        @include flex(row, space-between, center);
        @include containerWdt(80%);
        margin: 0 auto;
    }
    .logo {
        width: 80px;
    }

    .list-container {
        @include flex(row, flex-end, center);
        height: var(--headerHeight);
        width: 100%;
        ul {
            @include flex(row, space-between, center);
            list-style-type: none;

            li {
                text-align: center;
                line-height: var(--headerHeight);
                cursor: pointer;
                font-size: 0.7rem;
                height: var(--headerHeight);
                margin: 0 5px;
                padding: 0 10px
            }
            li:hover {
                @include colorize(#0282F9);
                border-bottom: 5px solid #0282F9;
            }
        }
    }
}
</style>