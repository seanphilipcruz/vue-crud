<template>
    <div>
        <b-navbar toggleable="lg" type="dark" variant="secondary">
            <b-navbar-brand>Vue-Crud</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item to="/">Home</b-nav-item>
                </b-navbar-nav>

                <b-navbar-nav class="ml-auto">
                    <b-nav-item to="/create">Create Post</b-nav-item>
                    <b-nav-item to="/posts">Posts</b-nav-item>
                </b-navbar-nav>
            </b-collapse>

        </b-navbar>
        <br />

        <b-container>
            <transition name="fade">
                <router-view></router-view>
            </transition>
        </b-container>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('App.vue mounted');
        },
        name: "App"
    }
</script>

<style scoped>
    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s
    }

    .fade-enter, .fade-leave-active {
        opacity: 0
    }
</style>
