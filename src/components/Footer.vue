<template>
  <footer>
    <ul>
      <li><a :href="`https://oxoformdocs.fra1.digitaloceanspaces.com/${game_id}/reglement.pdf`" target="_blank">**Règlement du jeu</a></li>
      <li><router-link to="/mentions">Mentions légales</router-link></li>
      <li><a :href="`https://oxoformdocs.fra1.digitaloceanspaces.com/${game_id}/politique.pdf`" target="_blank">Politique de confidentialité</a></li>
      <li><router-link to="/contact">Contactez-nous</router-link></li>
    </ul>

    <cookie-law theme="blood-orange--rounded" storageName="cookies">
      <div class="cookie-banner" slot-scope="props">
        <div>
          Ce site web stocke des cookies sur votre ordinateur. Ces cookies sont utilisés pour collecter des informations
          sur la façon dont vous interagissez avec notre site Web et nous permettent de nous souvenir de vous. Nous
          utilisons ces informations afin d'améliorer et de personnaliser votre expérience de navigation et pour des
          analyses et des mesures sur nos visiteurs à la fois sur ce site Web et d'autres médias. Pour en savoir plus
          sur les cookies que nous utilisons, consultez notre <a
            href="https://oxoformdocs.fra1.digitaloceanspaces.com/5f06c5465d5be80017612beb/politique.pdf"
            target="_blank">politique de
            confidentialité</a>.
          <br /><br />
          Si vous refusez, vos informations ne seront pas suivies lorsque vous visitez ce site Web. Un seul cookie sera
          utilisé dans votre navigateur pour mémoriser votre préférence de ne pas être suivi.
          <br />
          <br />
        </div>
        <div>
          <button class="skew" @click="props.accept"><span>J'accepte</span></button>
          <button class="skew" @click="props.close"><span>Je refuse</span></button>
        </div>
      </div>
    </cookie-law>

  </footer>
</template>
<script>
var consts = require('../config');
import CookieLaw from 'vue-cookie-law'
export default {
  components: { CookieLaw },
    data() {
        return {
            game_id : consts.GAME_ID
        }
    }  
}
</script>