<template>
  <div class="container">
    <div class="row">
      <div class= "col-sm-12">
        <nav-header @pageWasChanged="currentPage=$event"></nav-header>
        <keep-alive>
          <component :is="currentPage"></component>
        </keep-alive>
        <cc-footer>
          <!-- content between the component tag will be inserted inside of the slot -->
          <p class="text-center" slot="app-name">&copy; {{appName}}</p>
          <nav>
            <ul class="nav justify-content-center">
              <li class="nav-item"><a class="nav-link">Home</a></li>
              <li class="nav-item"><a class="nav-link">About</a></li>
              <li class="nav-item"><a class="nav-link">Contact</a></li>
            </ul>
          </nav>
        </cc-footer>
      </div>
    </div>
  </div>
</template>

<script>
import FirebaseConfig from './firebaseConfig.js'
import Header from './components/Header.vue'
import CardFront from './components/card/CardFront.vue'
import CardInsideLeft from './components/card/CardInsideLeft.vue'
import CardInsideRight from './components/card/CardInsideRight.vue'
import CardBack from './components/card/CardBack.vue'
import Footer from './components/Footer.vue'

export default {
  data: function(){
    return{
      //default Value
      currentPage: 'cardFront',
      appName: 'Creative Cards'
    }
  },
  components: {
    navHeader: Header,
    cardFront: CardFront,
    cardInsideLeft: CardInsideLeft,
    cardInsideRight: CardInsideRight,
    cardBack: CardBack,
    ccFooter: Footer
  }
}
</script>

<style>
  body{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    color: #333;
  }
  a{
    cursor: pointer;
  }
</style>
