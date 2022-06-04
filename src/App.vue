<template>
  <div id="app">
    <HeaderBar />
    <router-view path="$router.key" />
    <FooterBar />
    </div>
</template>


<script>
import'./styles/global.css';

import HeaderBar from './components/Header';
import FooterBar from './components/Footer';


export default {
  name: 'App',
  components: {
    HeaderBar,
    FooterBar,
    }
}

</script>


