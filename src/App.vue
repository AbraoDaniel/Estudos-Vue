<template>

  <div id="app">
    <HeaderOne />
    <HomeOne />
    <FooterOne />

  </div>
</template>

<script>
import './styles/global.css'

import HeaderOne from './components/HeaderOne';

import HomeOne from './pages/HomeOne';

import FooterOne from './components/FooterOne';



export default {
  name: 'App',
  components: {
    HeaderOne,
    HomeOne,
    FooterOne
}
}
</script>

