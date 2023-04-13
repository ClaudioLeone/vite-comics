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
@mixin flex($flex-direction, $justify-content, $align-items) {
    display: flex;
    flex-direction: $flex-direction;
    justify-content: $justify-content;
    align-items: $align-items;
}

.header {
    @include flex(row, center, center);

    .list-container {
        @include flex(row, center, center);
        ul {
            @include flex(row, center, center);
            list-style-type: none;
        }
    }
}
</style>