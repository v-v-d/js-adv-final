<template>
  <div>
    <Header/>
    <NavBar/>
    <CatalogTitleCategory/>
    <ProductImageSlide/>
    <ProductDescription/>
    <ProductYouMayLike :products="products" @buy="buyButtonHandler"/>
    <Footer/>
  </div>
</template>

<script>
  import Header from '../elements/Header.vue';
  import NavBar from '../elements/NavBar.vue';
  import CatalogTitleCategory from '../elements/CatalogTitleCategory.vue';
  import ProductImageSlide from '../elements/ProductImageSlide.vue';
  import ProductDescription from '../elements/ProductDescription.vue';
  import ProductYouMayLike from '../elements/ProductYouMayLike.vue';
  import Footer from '../elements/Footer.vue';

  export default {
    name: 'ProductPage',
    props: ['products'],
    methods: {
      buyButtonHandler(product) {
        this.$emit('buy', product);
      },
    },
    components: {
      Header,
      NavBar,
      CatalogTitleCategory,
      ProductImageSlide,
      ProductDescription,
      ProductYouMayLike,
      Footer,
    }
  };
</script>

<style lang="sass">

</style>