<template>
    <div id="app">
        <Header/>
        <Main/>
    </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
    name: 'App',
    
    components: {
        Header,
        Main,
    }
}
</script>

<style lang="scss">
@import '@/styles/Global.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';
</style>
