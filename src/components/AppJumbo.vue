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
            <div class="currentSeries-btn">
                <button><strong>CURRENT SERIES</strong></button>
            </div>
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
        height: 250px;
        margin: 0 auto;
        color: white;
        position: relative;
    }
}
.currentSeries-btn {
    position: absolute;
    bottom: -32px;
  margin: 20px auto;
}
.currentSeries-btn > button {
  padding: 5px 15px;
  font-family: 'Open Sans', sans-serif;
  color: white;
  background-color: #0282F9;
  border: none;
  cursor: pointer;
}
.currentSeries-btn > button:hover{
  background-color: #0A63BD;
}
</style>