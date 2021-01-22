<template>
  <div id="app">
    <headerElem></HeaderElem>
      <transition name="fade" mode="out-in">
        <router-view/>
      </transition>
    <FooterElem></FooterElem>
 </div> 
</template>

<script>
import HeaderElem from '@/components/Header'
import FooterElem from '@/components/Footer'

export default {
  name: 'App',
  data: function () {
    return {
      menu: false
    }
  },  
  components: {
    HeaderElem,
    FooterElem,
  }
}
</script>