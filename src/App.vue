<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppCta from './components/AppCta.vue';
import DcCard from './components/DcCard.vue';
import AppBottomLinks from './components/AppBottomLinks.vue';

export default {
  components: {                                 
    AppHeader,
    AppJumbo,
    AppCta,
    DcCard,
    AppBottomLinks
  },

  data() {
    return {
      comics: [
        {
          thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book',
        },
        {
          thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book',
        },
        {
          thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
          price: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel',
        },
        {
          thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
          price: '$2.99',
          series: 'Batgirl',
          type: 'comic book',
        },
        {
          thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
          price: '$3.99',
          series: 'Batman',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
          price: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
          price: '$3.99',
          series: 'Batman/ Superman',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
          price: '$4.99',
          series: 'Batman/ Superman Annual',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
          price: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
          price: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
          price: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book',
        },
        {
          thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
          price: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel',
        },
      ],
      ctaIcons: [
        {
          src: "../src/assets/img/buy-comics-digital-comics.png",
          img: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS"
        },
        {
          src: "../src/assets/img/buy-comics-merchandise.png",
          img: "buy-comics-merchandise.png",
          title: "DC MERCHANDISE"
        },
        {
          src: "../src/assets/img/buy-comics-subscriptions.png",
          img: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION"
        },
        {
          src: "../src/assets/img/buy-comics-shop-locator.png",
          img: "buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR"
        },
        {
          src: "../src/assets/img/buy-dc-power-visa.svg",
          img: "buy-dc-power-visa.svg",
          title: "DC POWER VISA"
        }
      ]
    }
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  
  <section class="card-container">
    <div class="flex-wrap stretch">
      <DcCard v-for="(comic, index) in comics" :thumb="comic.thumb" :series="comic.series" :key="index"/>
    </div>
    <div class="loadMore-btn">
      <button><strong>LOAD MORE</strong></button>
    </div>
  </section>
  
  <section>
    <div class="cta-container flex">
        <div class="cta-box container flex">
          <AppCta v-for="(icon, index) in ctaIcons" :key="index" :src="icon.src" :title="icon.title"/>
        </div>
    </div>
  </section>

  <section class="bottom-page">
    <AppBottomLinks />
  </section>
</template>

<style lang="scss">
@use "./style/style.scss" as *;

.flex {
  display: flex;
}

.stretch {
  align-items: stretch;
}

.loadMore-btn {
  text-align: center;
  margin: 20px auto;
}

.loadMore-btn > button {
  padding: 5px 15px;
  font-family: 'Open Sans', sans-serif;
  font-size: 0.75rem;
  color: white;
  background-color: #0282F9;
  border: none;
  cursor: pointer;
}
.loadMore-btn > button:hover{
  background-color: #0A63BD;
}

.cta-container {
  background-color: #0282F9;
  align-items: center;

  .cta-box {
    justify-content: space-between
  }

  .container {
    @include containerWdt(80%);
    height: 150px;
    margin: 0 auto;
  }
}

.bottom-page {
  background-image: url(./assets/img/footer-bg.jpg);
  object-fit: cover;
}
</style>