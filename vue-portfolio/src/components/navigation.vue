<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <button class="navbar-toggler" type="button" data-toggle="collapse"
              data-target="#navbarTogglerDemo03"
              aria-controls="navbarTogglerDemo03"
              aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <a class="navbar-brand" href="#">Preeti Arumalla</a>
            <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
                <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
                <li class="nav-item active">
                    <a class="nav-link" href="#">
                    <router-link to="/">Home</router-link>
                    <span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">
                    <router-link to="/about">About</router-link>
                    <span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item" @click="jumpToPortfolio" v-scroll-to="'#portf'" >
                    <a class="nav-link" href="#">Portfolio</a>
                </li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<script>
import Home from '../views/Home'
import Vue from 'vue'
import VueScrollTo from 'vue-scrollto'

Vue.use(VueScrollTo)

export default {
  methods: {
    jumpToPortfolio () {
      if (this.$route.path === '/about') {
        document.getElementById('portf').scrollIntoView()
      }
    }
  }
}
</script>
