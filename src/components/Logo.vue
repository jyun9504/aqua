<template>
    <nav class="logo" id="nav">
        <router-link  to="/">
            <h1 class="logo__name">A qua</h1>
        </router-link>
    </nav>
</template>

<script>
export default {
    name: 'Logo',
    props: {},
    data () {
        return {
            
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .logo {
        display: inline-block;
        animation: fadeIn 1s linear;

        & a {
            text-decoration: none;
            color: #02696C;
        }

        &__name {
            text-transform: uppercase;
            font-size: 2rem;
        }
    }
</style>
