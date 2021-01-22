<template>
    <header>

        <svg class="menu-mobile" @click="toggle" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 384 384" style="enable-background:new 0 0 255 255;" xml:space="preserve">
        <g><g><g><rect x="0" y="277.333" width="384" height="42.667"/><rect x="0" y="170.667" width="384" fill="param(color)" height="42.667"/><rect x="0" y="64" width="384" fill="param(color)" height="42.667"/>
        </g></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>

        <Drawer @close="toggle" align="left" :closeable="true">
            <div v-if="open">
                <ul>
                    <li @click="toggle"><a :href="`https://oxoformdocs.fra1.digitaloceanspaces.com/${game_id}/reglement.pdf`" target="_blank">Règlement du jeu</a></li>
                    <li @click="toggle"><router-link to="/mentions">Mentions légales</router-link></li>
                    <li @click="toggle"><a :href="`https://oxoformdocs.fra1.digitaloceanspaces.com/${game_id}/politique.pdf`" target="_blank">Politique de confidentialité</a></li>
                    <li @click="toggle"><router-link to="/contact">Contact</router-link></li>
                </ul>
            </div>
         </Drawer>
         <router-link to="/">HOME</router-link>
    </header>
</template>
<script>
var consts = require('../config');
import Drawer from "vue-simple-drawer"

export default {
    name: 'HeaderElem',
    data() {
        return {
            game_id : consts.GAME_ID,
            open: false
        }
    },
    components: {
        Drawer
    },
    methods: {   
        toggle() {
            this.open = !this.open
        }
    }    
}
</script>