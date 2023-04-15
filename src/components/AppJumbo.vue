<script>
    export default {
        name: 'AppJumbo',
        data() {
            return {
                title: '>>CONTENT GOES HERE<<'
            }
        }
    }
</script>

<template>
    <div class="headerNav">
        <div class="container">
            
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;

.headerNav {
    background-color: #1C1C1C;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    object-fit: fill;
    .container {
    @include containerWdt(80%);
    @include flex(row, left, center);
    height: 215px;
    margin: 0 auto;
    color: white;
}
}

</style>