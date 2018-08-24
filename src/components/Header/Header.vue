<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
        <img src="https://bulma.io/images/bulma-logo.png" alt="Bulma: a modern CSS framework based on Flexbox" width="112" height="28">
        </a>

        <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" @click="isBurgerActive()" :class="{'is-active': isBurger}" >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        </a>
    </div>

    <div class="navbar-menu navbar-end" :class="{ 'is-active': isBurger }">
        <router-link class="navbar-item" to="/">Home</router-link>
        <router-link class="navbar-item" to="/weather">Weather</router-link>
        <router-link class="navbar-item" to="/about">About</router-link>
    </div>

    </nav>
</template>

<script>
export default {
    data() {
        return {
            isBurger: false
        }
    },

    methods: {
        isBurgerActive() {
            this.isBurger = this.isBurger ? false : true
        }
    }
}
</script>

