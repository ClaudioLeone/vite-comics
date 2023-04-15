<script>
    export default {
        name: 'AppBottomLinks',
        data() {
            return {

            }
        }
    }
</script>

<template>
    <div class="links-container flex">
        <div class="links">

        </div>

        <div class="dc-bottom-logo">
            
        </div>
    </div>
</template>

<style scoped lang="scss">
.flex{
    display: flex;
}
.links-container {
    width: 80%;
    margin: 0 auto;
    height: 350px;
}

.links {
    width: 50%;
}
.dc-bottom-logo{
    width: 50%;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-size: cover;
}
</style>